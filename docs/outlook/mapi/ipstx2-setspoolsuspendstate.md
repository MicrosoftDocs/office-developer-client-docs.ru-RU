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
ms.openlocfilehash: 30ec82788e46ca07c6529ce74872e0a0c7c012a1
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19809558"
---
# <a name="ipstx2setspoolsuspendstate"></a><span data-ttu-id="fd41f-103">IPSTX2::SetSpoolSuspendState</span><span class="sxs-lookup"><span data-stu-id="fd41f-103">IPSTX2::SetSpoolSuspendState</span></span>

  
  
<span data-ttu-id="fd41f-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="fd41f-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="fd41f-105">Задает приостановленном состоянии очереди.</span><span class="sxs-lookup"><span data-stu-id="fd41f-105">Sets the suspended state on the spooler.</span></span>
  
```cpp
void SetSpoolSuspendState( 
    ULONG ulState 
);
```

## <a name="parameters"></a><span data-ttu-id="fd41f-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="fd41f-106">Parameters</span></span>

 <span data-ttu-id="fd41f-107">_ulState_</span><span class="sxs-lookup"><span data-stu-id="fd41f-107">_ulState_</span></span>
  
> <span data-ttu-id="fd41f-108">[in] Состояние, значение очереди.</span><span class="sxs-lookup"><span data-stu-id="fd41f-108">[in] The state to set the spooler to.</span></span> <span data-ttu-id="fd41f-109">Оно должно быть одно из следующих значений:</span><span class="sxs-lookup"><span data-stu-id="fd41f-109">It must be one of the following values:</span></span>
    
 <span data-ttu-id="fd41f-110">**SS_ACTIVE**</span><span class="sxs-lookup"><span data-stu-id="fd41f-110">**SS_ACTIVE**</span></span>
  
> 
    
 <span data-ttu-id="fd41f-111">**SS_SUSPENDED**</span><span class="sxs-lookup"><span data-stu-id="fd41f-111">**SS_SUSPENDED**</span></span>
  
> 
    
## <a name="see-also"></a><span data-ttu-id="fd41f-112">См. также</span><span class="sxs-lookup"><span data-stu-id="fd41f-112">See also</span></span>



[<span data-ttu-id="fd41f-113">��������� MAPI</span><span class="sxs-lookup"><span data-stu-id="fd41f-113">MAPI Constants</span></span>](mapi-constants.md)

