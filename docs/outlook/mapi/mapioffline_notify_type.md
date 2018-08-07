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
ms.openlocfilehash: 468dfd634c4aaf18b019d06975ec9066c9d5f7a6
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19809889"
---
# <a name="mapiofflinenotifytype"></a>MAPIOFFLINE_NOTIFY_TYPE

  
  
**Относится к**: Outlook 
  
При изменении состояния подключения необходимо предпринять месте, с удалением или завершения — определяет MAPIOFFLINE_NOTIFY_TYPE уведомление. 
  
## <a name="quick-info"></a>Краткие сведения

В разделе **[IMAPIOfflineNotify](imapiofflinenotifyiunknown.md)**. 
  
```cpp
typedef enum { 
    MAPIOFFLINE_NOTIFY_TYPE_STATECHANGE_START = 1,  
    MAPIOFFLINE_NOTIFY_TYPE_STATECHANGE = 2,  
    MAPIOFFLINE_NOTIFY_TYPE_STATECHANGE_DONE = 3  
} MAPIOFFLINE_NOTIFY_TYPE;
```

## <a name="see-also"></a>См. также



[Сведения об API автономного состояния](about-the-offline-state-api.md)
  
[��������� MAPI](mapi-constants.md)
  
[MAPIOFFLINE_NOTIFY](mapioffline_notify.md)

