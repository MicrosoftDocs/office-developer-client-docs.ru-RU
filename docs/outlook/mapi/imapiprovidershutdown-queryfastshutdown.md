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
ms.openlocfilehash: 50b49761cf5923b11a450cbce7b7991f5ddd4d82
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418220"
---
# <a name="imapiprovidershutdownqueryfastshutdown"></a>IMAPIProviderShutdown::QueryFastShutdown

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Запрашивает поставщика MAPI для поддержки быстрого отключения. 
  
```cpp
HRESULT QueryFastShutdown ();
```

## <a name="return-value"></a>Возвращаемое значение

S_OK
  
> Поставщик MAPI поддерживает клиента MAPI для быстрого отключения.
    
MAPI_E_NO_SUPPORT
  
> Поставщик MAPI не поддерживает клиента MAPI для быстрого отключения.
    
## <a name="remarks"></a>Примечания

Поставщики MAPI, которые не нуждаются в поддержке быстрого отключения клиента, по-прежнему должны реализовать интерфейс [IMAPIProviderShutdown](imapiprovidershutdowniunknown.md) и иметь метод **IMAPIProviderShutdown::QueryFastShutdown** MAPI_E_NO_SUPPORT. Для Outlook клиента MAPI это Outlook ожидание выпуска всех внешних ссылок до его выхода. 
  
В зависимости от параметра Windows реестра для быстрого отключения, не реализация интерфейса **IMAPIProviderShutdown** не обязательно препятствует быстрому отключению клиента. 
  
## <a name="see-also"></a>См. также



[IMAPIProviderShutdown : IUnknown](imapiprovidershutdowniunknown.md)


[Завершение работы клиента в MAPI](client-shutdown-in-mapi.md)

