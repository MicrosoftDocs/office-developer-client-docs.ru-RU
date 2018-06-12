---
title: Обзор быстрое завершение работы
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: a7830d73-427c-4f8b-86f4-51e040c142c3
description: 'Последнее изменение: 26 июня 2012 г.'
ms.openlocfilehash: 17b1307427af2c35fe9ba8ee40dc78958e6b4a21
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19808405"
---
# <a name="fast-shutdown-overview"></a>Обзор быстрое завершение работы

**Применимо к**: Outlook 
  
Быстрое завершение работы — это механизм для клиента MAPI для инициации быстрого завершения процесса клиента, уведомления всех поставщиков, с которыми у клиента было активного сеанса MAPI для сохранения данных и параметров до завершения процесса клиента. В этом разделе описывается базовый механизм быстрое завершение работы. 

Начиная с Microsoft Outlook 2010, теперь включительно, Microsoft Outlook 2013, подсистема MAPI предоставляет [IMAPIClientShutdown: IUnknown](imapiclientshutdowniunknown.md) интерфейса. Outlook и другие клиенты MAPI могут принимают быстрое завершение работы как механизмом по умолчанию, чтобы завершить процесс клиента. Параметр уровня пользователя в реестре Windows на клиентском компьютере управляет внедрения быстрое завершение работы для всех клиентов MAPI для этого пользователя на этом компьютере. Для получения дополнительных сведений о параметрах реестра видеть [Fast параметры завершения работы пользователя](fast-shutdown-user-options.md).
  
Если клиент MAPI должен принять быстрое завершение работы, необходимо использовать **IMAPIClientShutdown: IUnknown** интерфейса. Ниже приведен типичный ход событий при попытке завершить работу. 
  
1. Клиент MAPI инициирует завершение работы путем вызова метода [IMAPIClientShutdown::QueryFastShutdown](imapiclientshutdown-queryfastshutdown.md) , чтобы определить, поддерживает ли подсистемы MAPI быстрое завершение работы. 
    
2. Подсистема MAPI с поддержкой доступные быстрое завершение работы отвечает на запросы с вызова **IMAPIClientShutdown::QueryFastShutdown** клиента с помощью следующей процедуры: 
    
    1. Подсистема MAPI вызывает метод [IMAPIProviderShutdown::QueryFastShutdown](imapiprovidershutdown-queryfastshutdown.md) для каждого поставщика MAPI, с которым процесс клиента MAPI имеет активного сеанса MAPI, если поставщик производитель реализовал [IMAPIProviderShutdown: IUnknown](imapiprovidershutdowniunknown.md) интерфейс. 
        
       > [!NOTE]
       >  Подсистема MAPI всегда запрашивает и уведомляет поставщики MAPI через **IMAPIProviderShutdown: IUnknown** интерфейс в пределах каждого сеанса MAPI в следующем порядке:
       > 1. Поставщиками транспорта
       > 2. Поставщиками адресных книг
       > 3. Поставщики хранилища 
    
    2. В зависимости от того, параметр реестра быстрое завершение работы для этого пользователя на клиентском компьютере в подсистеме MAPI указывает, что соответствующий код возврата для **IMAPIClientShutdown::QueryFastShutdown**. Код возврата — значение S_OK или MAPI_E_NO_SUPPORT.
        
    3. Клиент MAPI вызывает метод [IMAPIClientShutdown::NotifyProcessShutdown](imapiclientshutdown-notifyprocessshutdown.md) для указания подсистемы MAPI намерения завершить работу. 
        
    4. Подсистема MAPI указывает всех загруженных поставщиков MAPI, клиент MAPI завершит работу. Для поставщиков, реализованный **IMAPIProviderShutdown: IUnknown** интерфейс, подсистемы MAPI вызывает соответствующий метод [IMAPIProviderShutdown::NotifyProcessShutdown](imapiprovidershutdown-notifyprocessshutdown.md) . 
        
    5. Клиент MAPI вызывает метод [IMAPIClientShutdown::DoFastShutdown](imapiclientshutdown-dofastshutdown.md) для указания на подсистему MAPI сразу же выходе процесс клиента. 
        
    6. Подсистема MAPI указывает каждого загруженных поставщика MAPI, завершает работу процесс клиента MAPI. Для поставщиков, реализованный **IMAPIProviderShutdown: IUnknown** интерфейс, подсистемы MAPI вызывает соответствующий метод [IMAPIProviderShutdown::DoFastShutdown](imapiprovidershutdown-dofastshutdown.md) . На этом этапе поставщики MAPI следует убедитесь, что все необходимые действия, например сохранения данных и параметров, завершения при подготовке клиент MAPI немедленно отключите все ссылки и выйдите из. 
    
## <a name="see-also"></a>См. также

- [Завершение работы клиента в MAPI](client-shutdown-in-mapi.md)
- [Быстрое завершение работы пользовательских параметров](fast-shutdown-user-options.md)
- [Советы и рекомендации по быстрое завершение работы](best-practices-for-fast-shutdown.md)

