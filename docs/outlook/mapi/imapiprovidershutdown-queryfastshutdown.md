---
title: IMAPIProviderShutdownQueryFastShutdown
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIProviderShutdown.QueryFastShutdown
api_type:
- COM
ms.assetid: 12069912-4b87-4945-9123-51106e0d2d54
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 4301fb504439cf0ebd70b5ece589c812cb74844e
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22585299"
---
# <a name="imapiprovidershutdownqueryfastshutdown"></a>IMAPIProviderShutdown::QueryFastShutdown

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Запросы, которые поддерживают поставщика MAPI для быстрое завершение работы. 
  
```cpp
HRESULT QueryFastShutdown ();
```

## <a name="return-value"></a>Возвращаемое значение

S_OK
  
> Поставщик MAPI поддерживает быстрое завершение работы клиента MAPI.
    
MAPI_E_NO_SUPPORT
  
> Поставщик MAPI не поддерживает быстрое завершение работы клиента MAPI.
    
## <a name="remarks"></a>Замечания

Поставщики MAPI, которые не должны поддерживать быстрое завершение работы клиента следует по-прежнему реализовать интерфейс [IMAPIProviderShutdown](imapiprovidershutdowniunknown.md) и метод **IMAPIProviderShutdown::QueryFastShutdown** возвращает MAPI_E_NO_SUPPORT. Для Outlook как клиент MAPI в результате Outlook вынуждены ждать освобождения всех внешних ссылок освободить до его завершения. 
  
В зависимости от реестра Windows пользователя политика для быстрое завершение работы не реализация интерфейса **IMAPIProviderShutdown** не обязательно быстрое завершение работы клиента. 
  
## <a name="see-also"></a>См. также



[IMAPIProviderShutdown : IUnknown](imapiprovidershutdowniunknown.md)


[Завершение работы клиента в MAPI](client-shutdown-in-mapi.md)

