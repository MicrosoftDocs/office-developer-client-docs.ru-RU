---
title: Быстрое завершение работы пользовательских параметров
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 220aeab5-20f6-4520-96c9-8aaa0e8ea15b
description: 'Последнее изменение: 26 июня 2012 г.'
ms.openlocfilehash: a58f8b98ab2f5a5c1028440676a561427272d028
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19808408"
---
# <a name="fast-shutdown-user-options"></a>Быстрое завершение работы пользовательских параметров

**Относится к**: Outlook 
  
В этом разделе описываются три параметров реестра Windows, которые доступны, начиная с Microsoft Outlook 2010 и теперь включая Microsoft Outlook 2013 для быстрое завершение работы клиентов MAPI пользователя. Администраторы могут использовать эти параметры реестра для указания режима завершения работы предпочитаемого клиентского в зависимости от те поставщики MAPI поддержка быстрое завершение работы клиента. Установка администратора, в свою очередь, определяет реакцию подсистемы MAPI на клиента MAPI вызов [IMAPIClientShutdown::QueryFastShutdown](imapiclientshutdown-queryfastshutdown.md) с точки зрения поддержки доступно быстрое завершение работы. 
  
Несмотря на то, что параметр реестра отражает предпочтений администратора на уровне пользователя, для быстрого завершения работы для всех клиентов MAPI, разработчик клиента MAPI можно определить, поддерживает ли клиент быстрое завершение работы независимо от других клиентов MAPI и параметр реестра администратора. Тем не менее, для быстрого завершения работы вступили в силу успешно, пользователь должен иметь значение реестра, необходимых, клиент MAPI должен инициировать быстрое завершение работы с помощью [IMAPIClientShutdown: IUnknown](imapiclientshutdowniunknown.md) интерфейса и поставщики MAPI, которые работают с Клиент должен реализовывать [IMAPIProviderShutdown: IUnknown](imapiprovidershutdowniunknown.md) интерфейс для поддержки быстрое завершение работы клиента. 
  
В следующем списке описываются три варианта уровня пользователя.
  
### <a name="option-1-the-mapi-subsystem-enables-fast-shutdown-unless-mapi-providers-explicitly-opt-out"></a>Вариант 1: Подсистемы MAPI позволяет быстрое завершение работы, если не поставщики MAPI явным образом отключить 
    
Начиная с Outlook 2010, это поведение по умолчанию при Outlook — это клиент MAPI; она не обязательно поведение по умолчанию для других клиентов MAPI. Чтобы явно задать этот параметр для Outlook, Администраторы имеют возможность задать следующий раздел реестра и значение.
    
Раздел реестра:
  
>  `[HKEY_CURRENT_USER\Software\Policies\Microsoft\Office\14.0\Outlook\Options\Shutdown]`
    
Значение:
  
>  `"FastShutdownBehavior"=dword:00000000`
    
Если клиент MAPI инициирует быстрое завершение работы и вызывает **IMAPIClientShutdown::QueryFastShutdown** для запроса для поддержки быстрое завершение работы, подсистемы MAPI отвечает на запрос, возвращая S\_OK в течение без поставщика MAPI, имеющей active MAPI сеанс с помощью клиентского интерфейса MAPI выбрал явно не поддерживается быстрое завершение работы. 

Отключает поставщика MAPI из него быстрое завершение работы с помощью метода [IMAPIProviderShutdown::QueryFastShutdown](imapiprovidershutdown-queryfastshutdown.md) возвращает ошибку (MAPI\_E\_NO\_поддержки). Если один или несколько поставщики MAPI возвращает ошибку в **IMAPIProviderShutdown::QueryFastShutdown**, подсистемы MAPI возвращает MAPI_\E_\NO\_поддержки **IMAPIClientShutdown::QueryFastShutdown**. 

Если не отключает поставщика MAPI, возвращает подсистемы MAPI S\_OK, даже в том случае, если один или несколько поставщиков не реализованы **IMAPIProviderShutdown: IUnknown** интерфейса. 
    
### <a name="option-2-the-mapi-subsystem-enables-fast-shutdown-only-if-every-mapi-provider-explicitly-opts-in"></a>Вариант 2: Подсистемы MAPI позволяет быстрое завершение работы, только в том случае, если в явно отключает все поставщики MAPI 
    
Администраторам необходимо явно задать следующий раздел реестра и значение, чтобы указать этот параметр для быстрое завершение работы клиента.
    
Раздел реестра:
  
>  `[HKEY_CURRENT_USER\Software\Policies\Microsoft\Office\14.0\Outlook\Options\Shutdown]`
    
Значение:
  
>  `"FastShutdownBehavior"=dword:00000001`
    
Если клиент MAPI инициирует быстрое завершение работы и вызывает **IMAPIClientShutdown::QueryFastShutdown** для запроса для поддержки быстрое завершение работы, подсистемы MAPI отвечает на запрос, возвращая S\_OK, если все поставщики MAPI, у которых активных сеансов с MAPI поддержки быстрое завершение работы клиента. Поставщика MAPI демонстрируется поддержки, реализовав **IMAPIProviderShutdown::QueryFastShutdown** для возврата кода об отсутствии ошибок (S\_ОК). 

Если один или несколько таких поставщики MAPI возврата MAPI\_E\_NO\_поддержки, или не внедрять **IMAPIProviderShutdown::QueryFastShutdown**подсистемы MAPI возвращает код ошибки для **IMAPIClientShutdown::QueryFastShutdown** .
    
### <a name="option-3-an-administrator-disables-support-for-client-fast-shutdown"></a>Вариант 3: Администратор отключает поддержку быстрое завершение работы клиента
    
Администраторам необходимо явно задать следующий раздел реестра и значение для отключения поддержки быстрое завершение работы клиента.
    
Раздел реестра:
  
>  `[HKEY_CURRENT_USER\Software\Policies\Microsoft\Office\14.0\Outlook\Options\Shutdown]`
    
Значение:
  
>  `"FastShutdownBehavior"=dword:00000002`
    
Если клиент MAPI инициирует быстрое завершение работы и вызывает **IMAPIClientShutdown::QueryFastShutdown** для запроса для поддержки быстрое завершение работы, подсистемы MAPI отвечает на запрос, возвращая MAPI_E_NO_SUPPORT, независимо от того, требуется ли любого поставщика MAPI поддерживает быстрое завершение работы. В разделе этот параметр реестра в подсистеме MAPI никогда не вызывает метод **IMAPIProviderShutdown::QueryFastShutdown** или [IMAPIProviderShutdown::DoFastShutdown](imapiprovidershutdown-dofastshutdown.md) любого поставщика. 
    
## <a name="see-also"></a>См. также

- [Завершение работы клиента в MAPI](client-shutdown-in-mapi.md)
- [Обзор быстрого завершения работы](fast-shutdown-overview.md)
- [Рекомендации по быстрому завершению работы](best-practices-for-fast-shutdown.md)

