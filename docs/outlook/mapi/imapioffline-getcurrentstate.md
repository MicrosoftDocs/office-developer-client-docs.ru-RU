---
title: Имапиоффлинежеткуррентстате
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
ms.openlocfilehash: f5170ceb443dcde075440bf84d29000afe4680c7
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32321275"
---
# <a name="imapiofflinegetcurrentstate"></a><span data-ttu-id="dfbca-103">IMAPIOffline::GetCurrentState</span><span class="sxs-lookup"><span data-stu-id="dfbca-103">IMAPIOffline::GetCurrentState</span></span>

  
  
<span data-ttu-id="dfbca-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="dfbca-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="dfbca-105">Возвращает текущее или автономное состояние автономного объекта.</span><span class="sxs-lookup"><span data-stu-id="dfbca-105">Gets the current online or offline state of an offline object.</span></span>
  
```cpp
HRESULT GetCurrentState( 
    ULONG* pulState 
);
```

## <a name="parameters"></a><span data-ttu-id="dfbca-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="dfbca-106">Parameters</span></span>

 <span data-ttu-id="dfbca-107">_Пулстате_</span><span class="sxs-lookup"><span data-stu-id="dfbca-107">_pulState_</span></span>
  
> <span data-ttu-id="dfbca-108">вышли Текущее оперативное или автономное состояние автономного объекта.</span><span class="sxs-lookup"><span data-stu-id="dfbca-108">[out] The current online or offline state of an offline object.</span></span> <span data-ttu-id="dfbca-109">Оно должно быть одним из следующих двух значений:</span><span class="sxs-lookup"><span data-stu-id="dfbca-109">It must be one of these two values:</span></span>
    
<span data-ttu-id="dfbca-110">MAPIOFFLINE_STATE_ONLINE</span><span class="sxs-lookup"><span data-stu-id="dfbca-110">MAPIOFFLINE_STATE_ONLINE</span></span>
  
> 
    
<span data-ttu-id="dfbca-111">MAPIOFFLINE_STATE_OFFLINE</span><span class="sxs-lookup"><span data-stu-id="dfbca-111">MAPIOFFLINE_STATE_OFFLINE</span></span>
  
> 
    
## <a name="see-also"></a><span data-ttu-id="dfbca-112">См. также</span><span class="sxs-lookup"><span data-stu-id="dfbca-112">See also</span></span>



[<span data-ttu-id="dfbca-113">IMAPIOffline::GetCapabilities</span><span class="sxs-lookup"><span data-stu-id="dfbca-113">IMAPIOffline::GetCapabilities</span></span>](imapioffline-getcapabilities.md)
  
[<span data-ttu-id="dfbca-114">IMAPIOffline::SetCurrentState</span><span class="sxs-lookup"><span data-stu-id="dfbca-114">IMAPIOffline::SetCurrentState</span></span>](imapioffline-setcurrentstate.md)


[<span data-ttu-id="dfbca-115">Константы MAPI</span><span class="sxs-lookup"><span data-stu-id="dfbca-115">MAPI Constants</span></span>](mapi-constants.md)

