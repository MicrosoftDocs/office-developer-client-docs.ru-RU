---
title: IMAPIClientShutdownQueryFastShutdown
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIClientShutdown.QueryFastShutdown
api_type:
- COM
ms.assetid: b743b5b6-4a7c-46b8-99eb-afd13ee947db
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 6a76488f56f9d1eb1b344c01de2615627dd5d3ec
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418150"
---
# <a name="imapiclientshutdownqueryfastshutdown"></a>IMAPIClientShutdown::QueryFastShutdown

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Запрашивает подсистему MAPI для поддержки быстрого отключения, предоставляемую загруженными поставщиками MAPI.
  
```cpp
HRESULT QueryFastShutdown ();
```

## <a name="return-value"></a>Возвращаемое значение

S_OK
  
> Подсистема MAPI поддерживает клиента MAPI для быстрого отключения.
    
MAPI_E_NO_SUPPORT
  
> Поставщик MAPI не поддерживает клиента MAPI для быстрого отключения.
    
## <a name="remarks"></a>Примечания

Поддерживает ли подсистема MAPI клиента MAPI для быстрого отключения, зависит от параметра реестра Windows пользователя или поведения клиента MAPI по умолчанию для быстрого отключения. Это также зависит от способности загруженных поставщиков MAPI поддерживать быстрое отключение. Дополнительные сведения см. в [меню Fast Shutdown User Options.](fast-shutdown-user-options.md)
  
## <a name="see-also"></a>См. также



[IMAPIClientShutdown : IUnknown](imapiclientshutdowniunknown.md)


[Завершение работы клиента в MAPI](client-shutdown-in-mapi.md)

