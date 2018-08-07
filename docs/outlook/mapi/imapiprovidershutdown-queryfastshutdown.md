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
ms.openlocfilehash: d9f08c13f68c7d3d9f41b9a67ac1888d6c507c34
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19809078"
---
# <a name="imapiprovidershutdownqueryfastshutdown"></a>IMAPIProviderShutdown::QueryFastShutdown

  
  
**Относится к**: Outlook 
  
Запросы, которые поддерживают поставщика MAPI для быстрое завершение работы. 
  
```cpp
HRESULT QueryFastShutdown ();
```

## <a name="return-value"></a>������������ ��������

ЗНАЧЕНИЕ S_OK
  
> Поставщик MAPI поддерживает быстрое завершение работы клиента MAPI.
    
MAPI_E_NO_SUPPORT
  
> Поставщик MAPI не поддерживает быстрое завершение работы клиента MAPI.
    
## <a name="remarks"></a>Замечания

Поставщики MAPI, которые не должны поддерживать быстрое завершение работы клиента следует по-прежнему реализовать интерфейс [IMAPIProviderShutdown](imapiprovidershutdowniunknown.md) и метод **IMAPIProviderShutdown::QueryFastShutdown** возвращает MAPI_E_NO_SUPPORT. Для Outlook как клиент MAPI в результате Outlook вынуждены ждать освобождения всех внешних ссылок освободить до его завершения. 
  
В зависимости от реестра Windows пользователя политика для быстрое завершение работы не реализация интерфейса **IMAPIProviderShutdown** не обязательно быстрое завершение работы клиента. 
  
## <a name="see-also"></a>См. также



[IMAPIProviderShutdown : IUnknown](imapiprovidershutdowniunknown.md)


[Завершение работы клиента в MAPI](client-shutdown-in-mapi.md)

