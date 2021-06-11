---
title: IPSTX2SetSpoolSuspendState
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IPSTX2.SetSpoolSuspendState
api_type:
- COM
ms.assetid: 396db029-1d4a-203d-2256-3353d03c6767
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: e988114e8e71ad1f80d20ab0d5a30c37425f5952
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407517"
---
# <a name="ipstx2setspoolsuspendstate"></a><span data-ttu-id="9dc5f-103">IPSTX2::SetSpoolSuspendState</span><span class="sxs-lookup"><span data-stu-id="9dc5f-103">IPSTX2::SetSpoolSuspendState</span></span>

  
  
<span data-ttu-id="9dc5f-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9dc5f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9dc5f-105">Задает приостановку состояния на шпалере.</span><span class="sxs-lookup"><span data-stu-id="9dc5f-105">Sets the suspended state on the spooler.</span></span>
  
```cpp
void SetSpoolSuspendState( 
    ULONG ulState 
);
```

## <a name="parameters"></a><span data-ttu-id="9dc5f-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="9dc5f-106">Parameters</span></span>

 <span data-ttu-id="9dc5f-107">_ulState_</span><span class="sxs-lookup"><span data-stu-id="9dc5f-107">_ulState_</span></span>
  
> <span data-ttu-id="9dc5f-108">[in] Состояние, на который должен устанавливаться шпалер.</span><span class="sxs-lookup"><span data-stu-id="9dc5f-108">[in] The state to set the spooler to.</span></span> <span data-ttu-id="9dc5f-109">Это должно быть одно из следующих значений:</span><span class="sxs-lookup"><span data-stu-id="9dc5f-109">It must be one of the following values:</span></span>
    
 <span data-ttu-id="9dc5f-110">**SS_ACTIVE**</span><span class="sxs-lookup"><span data-stu-id="9dc5f-110">**SS_ACTIVE**</span></span>
  
> 
    
 <span data-ttu-id="9dc5f-111">**SS_SUSPENDED**</span><span class="sxs-lookup"><span data-stu-id="9dc5f-111">**SS_SUSPENDED**</span></span>
  
> 
    
## <a name="see-also"></a><span data-ttu-id="9dc5f-112">См. также</span><span class="sxs-lookup"><span data-stu-id="9dc5f-112">See also</span></span>



[<span data-ttu-id="9dc5f-113">Константы MAPI</span><span class="sxs-lookup"><span data-stu-id="9dc5f-113">MAPI Constants</span></span>](mapi-constants.md)

