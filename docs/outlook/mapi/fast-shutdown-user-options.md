---
title: Пользовательские параметры быстрого завершения работы
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
api_type:
- COM
ms.assetid: 220aeab5-20f6-4520-96c9-8aaa0e8ea15b
description: 'Дата последнего изменения: 26 июня 2012 года'
localization_priority: Priority
ms.openlocfilehash: 3c60862733c6b38e60650ae9daba9bba578fcd58
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28716371"
---
# <a name="fast-shutdown-user-options"></a>Пользовательские параметры быстрого завершения работы

**Область применения**: Outlook 2013 | Outlook 2016 
  
В этой статье описаны три параметра реестра Windows, доступные начиная с Microsoft Outlook 2010, включая Microsoft Outlook 2013, для быстрого завершения работы клиентов MAPI пользователя. Администраторы могут использовать эти параметры реестра, чтобы указать предпочитаемое поведение при завершении работы клиента в зависимости от поддержки поставщиками MAPI быстрого завершения работы клиента. Параметр администратора, в свою очередь, определяет реакцию подсистемы MAPI на вызов клиентом MAPI метода [IMAPIClientShutdown::QueryFastShutdown](imapiclientshutdown-queryfastshutdown.md) с учетом наличия поддержки быстрого завершения работы. 
  
Хотя параметр реестра отражает предпочтения администратора на уровне пользователя по быстрому завершению работы для всех клиентов MAPI, разработчик клиента MAPI может решить, поддерживает ли клиент быстрое завершение работы независимо от других клиентов MAPI и параметра реестра администратора. Тем не менее, для успешности быстрого завершения работы у пользователя должен быть настроен необходимый параметр реестра, клиент MAPI должен начать быстрое завершение работы с помощью интерфейса [IMAPIClientShutdown: IUnknown](imapiclientshutdowniunknown.md), а поставщики MAPI, работающие с клиентом, должны реализовать интерфейс [IMAPIProviderShutdown: IUnknown](imapiprovidershutdowniunknown.md) для поддержки быстрого завершения работы клиента. 
  
В приведенном ниже списке описаны три варианта на уровне пользователя.
  
### <a name="option-1-the-mapi-subsystem-enables-fast-shutdown-unless-mapi-providers-explicitly-opt-out"></a>Вариант 1. Подсистема MAPI позволяет быстро завершить работу, если поставщики MAPI не отказались от этого явным образом 
    
Начиная с Outlook 2010, это поведение по умолчанию, если Outlook является клиентом MAPI. Это необязательно является поведением по умолчанию в других клиентах MAPI. Чтобы явным образом указать этот вариант для Outlook, администраторы могут настроить указанный ниже раздел реестра и значение.
    
Раздел реестра:
  
>  `[HKEY_CURRENT_USER\Software\Policies\Microsoft\Office\14.0\Outlook\Options\Shutdown]`
    
Значение:
  
>  `"FastShutdownBehavior"=dword:00000000`
    
Когда клиент MAPI запускает быстрое завершение работы и вызывает метод **IMAPIClientShutdown::QueryFastShutdown** для запроса поддержки быстрого завершения работы, подсистема MAPI в ответ на запрос возвращает значение S\_OK, если никакой поставщик MAPI с активным сеансом MAPI у клиента MAPI явным образом не отказался от поддержки быстрого завершения работы. 

Поставщик MAPI отказывается от быстрого завершения работы путем возвращения ошибки при реализации метода [IMAPIProviderShutdown::QueryFastShutdown](imapiprovidershutdown-queryfastshutdown.md) (MAPI\_E\_NO\_SUPPORT). Если один или несколько поставщиков MAPI возвращают ошибку в методе **IMAPIProviderShutdown::QueryFastShutdown**, подсистема MAPI возвращает значение MAPI_\E_\NO\_SUPPORT в метод **IMAPIClientShutdown::QueryFastShutdown**. 

Если поставщик MAPI не оказался от применения, подсистема MAPI возвращает значение S\_OK, даже если один или несколько поставщиков не реализовали интерфейс **IMAPIProviderShutdown : IUnknown**. 
    
### <a name="option-2-the-mapi-subsystem-enables-fast-shutdown-only-if-every-mapi-provider-explicitly-opts-in"></a>Вариант 2. Подсистема MAPI позволяет быстро завершить работу, если все поставщики MAPI согласились на это явным образом 
    
Администраторы должны явным образом настроить указанный ниже раздел реестра и значение, чтобы указать предпочтение для быстрого завершения работы клиента.
    
Раздел реестра:
  
>  `[HKEY_CURRENT_USER\Software\Policies\Microsoft\Office\14.0\Outlook\Options\Shutdown]`
    
Значение:
  
>  `"FastShutdownBehavior"=dword:00000001`
    
Когда клиент MAPI запускает быстрое завершение работы и вызывает метод **IMAPIClientShutdown::QueryFastShutdown** для запроса поддержки быстрого завершения работы, подсистема MAPI в ответ на запрос возвращает значение S\_OK, если все поставщики MAPI с активными сеансами с клиентами MAPI поддерживают быстрое завершение работы. Поставщик MAPI демонстрирует свою поддержку путем возвращения кода отсутствия ошибки при реализации метода **IMAPIProviderShutdown::QueryFastShutdown** (S\_ОК). 

Если один или несколько таких поставщиков MAPI возвращают значение MAPI\_E\_NO\_SUPPORT или не реализуют метод **IMAPIProviderShutdown::QueryFastShutdown**, подсистема MAPI возвращает код ошибки в метод **IMAPIClientShutdown::QueryFastShutdown**.
    
### <a name="option-3-an-administrator-disables-support-for-client-fast-shutdown"></a>Вариант 3. Администратор отключает поддержку быстрого завершения работы клиента
    
Администраторы должны явным образом настроить указанный ниже раздел реестра и значение, чтобы отключить поддержку быстрого завершения работы клиента.
    
Раздел реестра:
  
>  `[HKEY_CURRENT_USER\Software\Policies\Microsoft\Office\14.0\Outlook\Options\Shutdown]`
    
Значение:
  
>  `"FastShutdownBehavior"=dword:00000002`
    
Когда клиент MAPI запускает быстрое завершение работы и вызывает метод **IMAPIClientShutdown::QueryFastShutdown** для запроса поддержки быстрого завершения работы, подсистема MAPI в ответ на запрос возвращает значение MAPI_E_NO_SUPPORT независимо от поддержки каким-либо поставщиком MAPI быстрого завершения работы. При этом параметре реестра подсистема MAPI никогда не вызывает метод **IMAPIProviderShutdown::QueryFastShutdown** или [IMAPIProviderShutdown::DoFastShutdown](imapiprovidershutdown-dofastshutdown.md) поставщиков. 
    
## <a name="see-also"></a>См. также

- [Завершение работы клиента в MAPI](client-shutdown-in-mapi.md)
- [Обзор быстрого завершения работы](fast-shutdown-overview.md)
- [Рекомендации по быстрому завершению работы](best-practices-for-fast-shutdown.md)

