---
title: Имапипровидершутдовндофастшутдовн
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIProviderShutdown.DoFastShutdown
api_type:
- COM
ms.assetid: d2b66a8e-2e28-4c32-af95-38d345c7bbd7
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 4ff93ed9353d58ef6b68823bebf8b5b27a0df6e8
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428846"
---
# <a name="imapiprovidershutdowndofastshutdown"></a>IMAPIProviderShutdown::DoFastShutdown

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Указывает поставщику MAPI, что клиент MAPI немедленно завершает работу, поэтому поставщик MAPI сохранит изменения, чтобы предотвратить потерю данных.
  
```cpp
HRESULT DoFastShutdown ();
```

## <a name="return-value"></a>Возвращаемое значение

S_OK
  
> Поставщик MAPI готов к немедленному завершению работы клиента MAPI. 
    
## <a name="see-also"></a>См. также



[IMAPIProviderShutdown : IUnknown](imapiprovidershutdowniunknown.md)


[Завершение работы клиента в MAPI](client-shutdown-in-mapi.md)

