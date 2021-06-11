---
title: MAPIOFFLINE_NOTIFY_TYPE
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: a111d7b7-6e87-4958-8f9b-0f2adbeb8b63
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 65ed848907e196c315e8ddb61c4afd2fe03faa18
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33413432"
---
# <a name="mapioffline_notify_type"></a>MAPIOFFLINE_NOTIFY_TYPE

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
В MAPIOFFLINE_NOTIFY_TYPE уведомления указывается, происходит или завершено изменение состояния подключения. 
  
## <a name="quick-info"></a>Краткие сведения

См. **[IMAPIOfflineNotify](imapiofflinenotifyiunknown.md)**. 
  
```cpp
typedef enum { 
    MAPIOFFLINE_NOTIFY_TYPE_STATECHANGE_START = 1,  
    MAPIOFFLINE_NOTIFY_TYPE_STATECHANGE = 2,  
    MAPIOFFLINE_NOTIFY_TYPE_STATECHANGE_DONE = 3  
} MAPIOFFLINE_NOTIFY_TYPE;
```

## <a name="see-also"></a>См. также



[Об API автономного режима](about-the-offline-state-api.md)
  
[��������� MAPI](mapi-constants.md)
  
[MAPIOFFLINE_NOTIFY](mapioffline_notify.md)

