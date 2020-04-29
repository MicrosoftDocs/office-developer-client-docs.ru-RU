---
title: иолкапптребасербегиненумератеаппоинтментс
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 8946703a-aaa8-6b3f-aa68-931365db620d
description: Begins a task for appointment enumeration in a calendar folder to find the appointments that need rebasing.
ms.openlocfilehash: cc89b3510f09bb98fd6720cb6d5ab3edeb13eac8
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407272"
---
# <a name="iolkapptrebaserbeginenumerateappointments"></a><span data-ttu-id="63cc0-103">IOlkApptRebaser::BeginEnumerateAppointments</span><span class="sxs-lookup"><span data-stu-id="63cc0-103">IOlkApptRebaser::BeginEnumerateAppointments</span></span>

<span data-ttu-id="63cc0-104">Begins a task for appointment enumeration in a calendar folder to find the appointments that need rebasing.</span><span class="sxs-lookup"><span data-stu-id="63cc0-104">Begins a task for appointment enumeration in a calendar folder to find the appointments that need rebasing.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="63cc0-105">Краткие сведения</span><span class="sxs-lookup"><span data-stu-id="63cc0-105">Quick info</span></span>

<span data-ttu-id="63cc0-106">See [IOlkApptRebaser](iolkapptrebaser.md).</span><span class="sxs-lookup"><span data-stu-id="63cc0-106">See [IOlkApptRebaser](iolkapptrebaser.md).</span></span>
  
```cpp
HRESULT BeginEnumerateAppointments( 
    PFNREBASETASKPROGRESS pfnProgress, 
    void **ppContext);
```

## <a name="parameters"></a><span data-ttu-id="63cc0-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="63cc0-107">Parameters</span></span>

<span data-ttu-id="63cc0-108">_пфнпрогресс_</span><span class="sxs-lookup"><span data-stu-id="63cc0-108">_pfnProgress_</span></span>
  
> <span data-ttu-id="63cc0-p101">[in] Optional. A pointer to a rebase task progress function to receive progress. **PFNREBASETASKPROGRESS** is defined in tzmovelib.h.</span><span class="sxs-lookup"><span data-stu-id="63cc0-p101">[in] Optional. A pointer to a rebase task progress function to receive progress. **PFNREBASETASKPROGRESS** is defined in tzmovelib.h.</span></span> 
    
<span data-ttu-id="63cc0-112">_ппконтекст_</span><span class="sxs-lookup"><span data-stu-id="63cc0-112">_ppContext_</span></span>
  
> <span data-ttu-id="63cc0-p102">[out] Required. A pointer to a pointer to the returned context. This context will be passed to [IOlkApptRebaser::EndEnumerateAppointments](iolkapptrebaser-endenumerateappointments.md).</span><span class="sxs-lookup"><span data-stu-id="63cc0-p102">[out] Required. A pointer to a pointer to the returned context. This context will be passed to [IOlkApptRebaser::EndEnumerateAppointments](iolkapptrebaser-endenumerateappointments.md).</span></span>
    
## <a name="return-values"></a><span data-ttu-id="63cc0-116">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="63cc0-116">Return values</span></span>

<span data-ttu-id="63cc0-117">S_OK if the call succeeded; otherwise, an error code.</span><span class="sxs-lookup"><span data-stu-id="63cc0-117">S_OK if the call succeeded; otherwise, an error code.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="63cc0-118">Примечания</span><span class="sxs-lookup"><span data-stu-id="63cc0-118">Remarks</span></span>

<span data-ttu-id="63cc0-119">This task runs on a new thread.</span><span class="sxs-lookup"><span data-stu-id="63cc0-119">This task runs on a new thread.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="63cc0-120">См. также</span><span class="sxs-lookup"><span data-stu-id="63cc0-120">See also</span></span>

- [<span data-ttu-id="63cc0-121">About rebasing calendars programmatically for Daylight Saving Time</span><span class="sxs-lookup"><span data-stu-id="63cc0-121">About rebasing calendars programmatically for Daylight Saving Time</span></span>](about-rebasing-calendars-programmatically-for-daylight-saving-time.md)

