---
title: Обзор быстрого завершения работы
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: a7830d73-427c-4f8b-86f4-51e040c142c3
description: 'Дата последнего изменения: 26 июня 2012 года'
ms.openlocfilehash: 8c33214b04e7c41eab173196c09f145c20ddf219
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33427208"
---
# <a name="fast-shutdown-overview"></a>Обзор быстрого завершения работы

**Относится к**: Outlook 2013 | Outlook 2016 
  
Быстрое завершение работы — это механизм, с помощью которого клиент MAPI инициирует быстрое завершение клиентского процесса, уведомляя всех поставщиков, с которыми клиент ведет активный сеанс MAPI, для сохранения данных и параметров до завершения клиентского процесса. В этом разделе описывается базовый механизм быстрого завершения работы. 

Начиная с Microsoft Outlook 2010, русская версия и теперь, включая Microsoft Outlook 2013, подсистема MAPI предоставляет [интерфейс IMAPIClientShutdown : IUnknown.](imapiclientshutdowniunknown.md) Outlook и другие клиенты MAPI могут использовать быстрое завершение работы в качестве механизма по умолчанию для выхода из клиентского процесса. Параметр на уровне пользователя в реестре Windows клиентского компьютера управляет внедрением быстрого завершения работы для всех клиентов MAPI для этого пользователя на этом компьютере. Подробные сведения о параметрах реестра см. в параметрах пользователей быстрого [завершения работы.](fast-shutdown-user-options.md)
  
Если клиенту MAPI требуется быстрое завершение работы, он должен использовать **интерфейс IMAPIClientShutdown : IUnknown.** Ниже приводится типичный ход событий, когда клиент пытается закрыть работу: 
  
1. Клиент MAPI инициирует завершение работы, вызывая метод [IMAPIClientShutdown::QueryFastShutdown,](imapiclientshutdown-queryfastshutdown.md) чтобы определить, поддерживает ли подсистема MAPI быстрое завершение работы. 
    
2. Подсистема MAPI отвечает доступной поддержкой быстрого завершения работы вызова **IMAPIClientShutdown::QueryFastShutdown** клиента с помощью следующей процедуры: 
    
    1. Подсистема MAPI вызывает метод [IMAPIProviderShutdown::QueryFastShutdown](imapiprovidershutdown-queryfastshutdown.md) для каждого поставщика MAPI, с которым клиентский процесс MAPI имеет активный сеанс MAPI, если поставщик реализовал [интерфейс IMAPIProviderShutdown : IUnknown.](imapiprovidershutdowniunknown.md) 
        
       > [!NOTE]
       >  Подсистема MAPI всегда запрашивает и оповешает поставщиков MAPI через **интерфейс IMAPIProviderShutdown : IUnknown** в каждом сеансе MAPI в следующем порядке:
       > 1. Поставщики транспорта
       > 2. Поставщики адресных книг
       > 3. Поставщики магазина 
    
    2. В зависимости от параметра реестра быстрого завершения работы для этого пользователя на клиентском компьютере подсистема MAPI указывает соответствующий код возврата для **IMAPIClientShutdown::QueryFastShutdown.** Код возврата — S_OK или MAPI_E_NO_SUPPORT.
        
    3. Клиент MAPI вызывает метод [IMAPIClientShutdown::NotifyProcessShutdown,](imapiclientshutdown-notifyprocessshutdown.md) чтобы указать подсистеме MAPI намерение закрыть работу. 
        
    4. Подсистема MAPI указывает каждому загруженного поставщика MAPI, что клиент MAPI будет отключен. Для поставщиков, которые реализовали интерфейс **IMAPIProviderShutdown : IUnknown,** подсистема MAPI вызывает соответствующий метод [IMAPIProviderShutdown::NotifyProcessShutdown.](imapiprovidershutdown-notifyprocessshutdown.md) 
        
    5. Клиент MAPI вызывает метод [IMAPIClientShutdown::D oFastShutdown,](imapiclientshutdown-dofastshutdown.md) чтобы указать подсистеме MAPI, что клиентский процесс немедленно выходит из процесса. 
        
    6. Подсистема MAPI указывает каждому загруженного поставщика MAPI, что клиентский процесс MAPI выходит из процесса. Для поставщиков, которые реализовали интерфейс **IMAPIProviderShutdown : IUnknown,** подсистема MAPI вызывает соответствующий метод [IMAPIProviderShutdown::D oFastShutdown.](imapiprovidershutdown-dofastshutdown.md) На этом этапе эти поставщики MAPI должны убедиться, что все необходимые действия, например сохранение данных и параметров, завершены в процессе подготовки клиента MAPI к немедленному отключению всех ссылок и выходу. 
    
## <a name="see-also"></a>См. также

- [Завершение работы клиента в MAPI](client-shutdown-in-mapi.md)
- [Параметры пользователей быстрого завершения работы](fast-shutdown-user-options.md)
- [Рекомендации по быстрому завершению работы](best-practices-for-fast-shutdown.md)

