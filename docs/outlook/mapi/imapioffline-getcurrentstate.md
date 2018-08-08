---
title: IMAPIOfflineGetCurrentState
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIOffline.GetCurrentState
api_type:
- COM
ms.assetid: f3769e83-d678-1087-fc0f-b4f156386333
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 3cf8ad3966c44add3fd85b9f1adf677039bfce15
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19808996"
---
# <a name="imapiofflinegetcurrentstate"></a><span data-ttu-id="1a7c9-103">IMAPIOffline::GetCurrentState</span><span class="sxs-lookup"><span data-stu-id="1a7c9-103">IMAPIOffline::GetCurrentState</span></span>

  
  
<span data-ttu-id="1a7c9-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="1a7c9-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="1a7c9-105">Возвращает текущее состояние сетевым и автономным автономного объекта.</span><span class="sxs-lookup"><span data-stu-id="1a7c9-105">Gets the current online or offline state of an offline object.</span></span>
  
```cpp
HRESULT GetCurrentState( 
    ULONG* pulState 
);
```

## <a name="parameters"></a><span data-ttu-id="1a7c9-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="1a7c9-106">Parameters</span></span>

 <span data-ttu-id="1a7c9-107">_pulState_</span><span class="sxs-lookup"><span data-stu-id="1a7c9-107">_pulState_</span></span>
  
> <span data-ttu-id="1a7c9-108">[out] Текущее сетевым и автономным состояние автономной объекта.</span><span class="sxs-lookup"><span data-stu-id="1a7c9-108">[out] The current online or offline state of an offline object.</span></span> <span data-ttu-id="1a7c9-109">Оно должно быть одно из следующих двух значений:</span><span class="sxs-lookup"><span data-stu-id="1a7c9-109">It must be one of these two values:</span></span>
    
<span data-ttu-id="1a7c9-110">MAPIOFFLINE_STATE_ONLINE</span><span class="sxs-lookup"><span data-stu-id="1a7c9-110">MAPIOFFLINE_STATE_ONLINE</span></span>
  
> 
    
<span data-ttu-id="1a7c9-111">MAPIOFFLINE_STATE_OFFLINE</span><span class="sxs-lookup"><span data-stu-id="1a7c9-111">MAPIOFFLINE_STATE_OFFLINE</span></span>
  
> 
    
## <a name="see-also"></a><span data-ttu-id="1a7c9-112">См. также</span><span class="sxs-lookup"><span data-stu-id="1a7c9-112">See also</span></span>



[<span data-ttu-id="1a7c9-113">IMAPIOffline::GetCapabilities</span><span class="sxs-lookup"><span data-stu-id="1a7c9-113">IMAPIOffline::GetCapabilities</span></span>](imapioffline-getcapabilities.md)
  
[<span data-ttu-id="1a7c9-114">IMAPIOffline::SetCurrentState</span><span class="sxs-lookup"><span data-stu-id="1a7c9-114">IMAPIOffline::SetCurrentState</span></span>](imapioffline-setcurrentstate.md)


[<span data-ttu-id="1a7c9-115">��������� MAPI</span><span class="sxs-lookup"><span data-stu-id="1a7c9-115">MAPI Constants</span></span>](mapi-constants.md)

