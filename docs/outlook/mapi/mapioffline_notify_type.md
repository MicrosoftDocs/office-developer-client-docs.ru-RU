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
ms.openlocfilehash: e7120b843eae8df70cb2c4f9cbf581dcf0e09c11
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22566889"
---
# <a name="mapiofflinenotifytype"></a><span data-ttu-id="27b3c-103">MAPIOFFLINE_NOTIFY_TYPE</span><span class="sxs-lookup"><span data-stu-id="27b3c-103">MAPIOFFLINE_NOTIFY_TYPE</span></span>

  
  
<span data-ttu-id="27b3c-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="27b3c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="27b3c-105">При изменении состояния подключения необходимо предпринять месте, с удалением или завершения — определяет MAPIOFFLINE_NOTIFY_TYPE уведомление.</span><span class="sxs-lookup"><span data-stu-id="27b3c-105">The MAPIOFFLINE_NOTIFY_TYPE of a notification identifies if a change in the connection state is going to take place, is taking place, or has completed.</span></span> 
  
## <a name="quick-info"></a><span data-ttu-id="27b3c-106">Краткие сведения</span><span class="sxs-lookup"><span data-stu-id="27b3c-106">Quick info</span></span>

<span data-ttu-id="27b3c-107">В разделе **[IMAPIOfflineNotify](imapiofflinenotifyiunknown.md)**.</span><span class="sxs-lookup"><span data-stu-id="27b3c-107">See **[IMAPIOfflineNotify](imapiofflinenotifyiunknown.md)**.</span></span> 
  
```cpp
typedef enum { 
    MAPIOFFLINE_NOTIFY_TYPE_STATECHANGE_START = 1,  
    MAPIOFFLINE_NOTIFY_TYPE_STATECHANGE = 2,  
    MAPIOFFLINE_NOTIFY_TYPE_STATECHANGE_DONE = 3  
} MAPIOFFLINE_NOTIFY_TYPE;
```

## <a name="see-also"></a><span data-ttu-id="27b3c-108">См. также</span><span class="sxs-lookup"><span data-stu-id="27b3c-108">See also</span></span>



[<span data-ttu-id="27b3c-109">Сведения об API автономного состояния</span><span class="sxs-lookup"><span data-stu-id="27b3c-109">About the Offline State API</span></span>](about-the-offline-state-api.md)
  
[<span data-ttu-id="27b3c-110">��������� MAPI</span><span class="sxs-lookup"><span data-stu-id="27b3c-110">MAPI Constants</span></span>](mapi-constants.md)
  
[<span data-ttu-id="27b3c-111">MAPIOFFLINE_NOTIFY</span><span class="sxs-lookup"><span data-stu-id="27b3c-111">MAPIOFFLINE_NOTIFY</span></span>](mapioffline_notify.md)

