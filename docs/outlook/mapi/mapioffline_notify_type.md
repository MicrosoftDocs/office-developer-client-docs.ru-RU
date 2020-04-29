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
# <a name="mapioffline_notify_type"></a><span data-ttu-id="d6049-103">MAPIOFFLINE_NOTIFY_TYPE</span><span class="sxs-lookup"><span data-stu-id="d6049-103">MAPIOFFLINE_NOTIFY_TYPE</span></span>

  
  
<span data-ttu-id="d6049-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d6049-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d6049-105">MAPIOFFLINE_NOTIFY_TYPE уведомления определяет, будет ли выполняться изменение состояния подключения, выполняется или завершено.</span><span class="sxs-lookup"><span data-stu-id="d6049-105">The MAPIOFFLINE_NOTIFY_TYPE of a notification identifies if a change in the connection state is going to take place, is taking place, or has completed.</span></span> 
  
## <a name="quick-info"></a><span data-ttu-id="d6049-106">Краткие сведения</span><span class="sxs-lookup"><span data-stu-id="d6049-106">Quick info</span></span>

<span data-ttu-id="d6049-107">Обратитесь к разделу **[имапиоффлиненотифи](imapiofflinenotifyiunknown.md)**.</span><span class="sxs-lookup"><span data-stu-id="d6049-107">See **[IMAPIOfflineNotify](imapiofflinenotifyiunknown.md)**.</span></span> 
  
```cpp
typedef enum { 
    MAPIOFFLINE_NOTIFY_TYPE_STATECHANGE_START = 1,  
    MAPIOFFLINE_NOTIFY_TYPE_STATECHANGE = 2,  
    MAPIOFFLINE_NOTIFY_TYPE_STATECHANGE_DONE = 3  
} MAPIOFFLINE_NOTIFY_TYPE;
```

## <a name="see-also"></a><span data-ttu-id="d6049-108">См. также</span><span class="sxs-lookup"><span data-stu-id="d6049-108">See also</span></span>



[<span data-ttu-id="d6049-109">Об API автономного режима</span><span class="sxs-lookup"><span data-stu-id="d6049-109">About the Offline State API</span></span>](about-the-offline-state-api.md)
  
[<span data-ttu-id="d6049-110">��������� MAPI</span><span class="sxs-lookup"><span data-stu-id="d6049-110">MAPI Constants</span></span>](mapi-constants.md)
  
[<span data-ttu-id="d6049-111">MAPIOFFLINE_NOTIFY</span><span class="sxs-lookup"><span data-stu-id="d6049-111">MAPIOFFLINE_NOTIFY</span></span>](mapioffline_notify.md)

