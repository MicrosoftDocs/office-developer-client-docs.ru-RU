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
  
Быстрое завершение работы — это механизм, позволяющий клиенту MAPI инициировать быстрое завершение работы клиентского процесса, уведомляя всех поставщиков, с которыми клиент имеет активный сеанс MAPI, чтобы сохранить данные и параметры до того, как клиентский процесс завершит работу. В этом разделе описывается базовый механизм быстрого завершения работы. 

Начиная с Microsoft Outlook 2010 и теперь включая Microsoft Outlook 2013, подсистема MAPI предоставляет интерфейс [метод imapiclientshutdown: IUnknown](imapiclientshutdowniunknown.md) . В качестве механизма по умолчанию для выхода из клиентского процесса можно применять быстрое завершение работы Outlook и других клиентов MAPI. Параметр уровня пользователя в реестре Windows клиентского компьютера управляет внедрением быстрого завершения работы всех клиентов MAPI для этого пользователя на этом компьютере. Сведения о параметрах реестра приведены в разделе [Параметры быстрого завершения работы пользователя](fast-shutdown-user-options.md).
  
Если клиент MAPI должен применять быстрое завершение работы, он должен использовать интерфейс **метод imapiclientshutdown: IUnknown** . Ниже приведен типичный порядок событий при попытке клиента завершить работу. 
  
1. Клиент MAPI инициирует завершение работы, вызывая метод [метод imapiclientshutdown:: QueryFastShutdown](imapiclientshutdown-queryfastshutdown.md) , чтобы определить, поддерживает ли подсистема MAPI быстрое завершение работы. 
    
2. Подсистема MAPI отвечает за доступную поддержку быстрого завершения работы для вызова **метод imapiclientshutdown:: QueryFastShutdown** клиента, используя следующую процедуру: 
    
    1. Подсистема MAPI вызывает метод [IMAPIProviderShutdown:: QueryFastShutdown](imapiprovidershutdown-queryfastshutdown.md) для каждого поставщика MAPI, с которым клиентский процесс MAPI имеет активный сеанс MAPI, если поставщик реализует интерфейс [IMAPIProviderShutdown: IUnknown](imapiprovidershutdowniunknown.md) . 
        
       > [!NOTE]
       >  Подсистема MAPI всегда запрашивает и уведомляет поставщиков MAPI с помощью интерфейса **IMAPIProviderShutdown: IUnknown** в каждом сеансе MAPI в следующем порядке:
       > 1. Поставщики транспорта
       > 2. Поставщики адресных книг
       > 3. Поставщики услуг хранения 
    
    2. В зависимости от параметра быстрого завершения работы реестра для этого пользователя на клиентском компьютере подсистема MAPI указывает соответствующий код возврата для **метод imapiclientshutdown:: QueryFastShutdown**. Код возврата либо S_OK, либо MAPI_E_NO_SUPPORT.
        
    3. Клиент MAPI вызывает метод [метод imapiclientshutdown:: нотифипроцессшутдовн](imapiclientshutdown-notifyprocessshutdown.md) , чтобы показать подсистеме MAPI намерение завершить работу. 
        
    4. Подсистема MAPI указывает каждому загруженному поставщику MAPI, что клиент MAPI завершает работу. Для тех поставщиков, которые реализовали интерфейс **IMAPIProviderShutdown: IUnknown** , подсистема MAPI вызывает соответствующий метод [IMAPIProviderShutdown:: нотифипроцессшутдовн](imapiprovidershutdown-notifyprocessshutdown.md) . 
        
    5. Клиент MAPI вызывает метод [метод imapiclientshutdown::D офастшутдовн](imapiclientshutdown-dofastshutdown.md) , чтобы указать подсистему MAPI, что клиентский процесс завершается немедленно. 
        
    6. Подсистема MAPI указывает каждому загруженному поставщику MAPI, что клиентский процесс MAPI завершает работу. Для тех поставщиков, которые реализовали интерфейс **IMAPIProviderShutdown: IUnknown** , подсистема MAPI вызывает соответствующий метод [IMAPIProviderShutdown::D офастшутдовн](imapiprovidershutdown-dofastshutdown.md) . На этом шаге эти поставщики MAPI должны проверить, что все необходимые действия, такие как сохранение данных и параметров, завершаются при подготовке клиента MAPI к немедленному отключению всех ссылок и выходе. 
    
## <a name="see-also"></a>См. также

- [Завершение работы клиента в MAPI](client-shutdown-in-mapi.md)
- [Параметры быстрого завершения работы пользователя](fast-shutdown-user-options.md)
- [Рекомендации по быстрому завершению работы](best-practices-for-fast-shutdown.md)

