---
title: Иолкапптребасербегинребасеаппоинтментс
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: ed50422e-9edf-4b73-1789-340b70532621
description: Begins a task for appointment rebasing given a list of appointments, usually obtained from IOlkApptRebaser::EndEnumerateAppointments.
ms.openlocfilehash: f0f2377f30de7688aaa4196e3a046c664c2128aa
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32321912"
---
# <a name="iolkapptrebaserbeginrebaseappointments"></a><span data-ttu-id="e0ef4-103">IOlkApptRebaser::BeginRebaseAppointments</span><span class="sxs-lookup"><span data-stu-id="e0ef4-103">IOlkApptRebaser::BeginRebaseAppointments</span></span>

<span data-ttu-id="e0ef4-104">Begins a task for appointment rebasing given a list of appointments, usually obtained from [IOlkApptRebaser::EndEnumerateAppointments](iolkapptrebaser-endenumerateappointments.md).</span><span class="sxs-lookup"><span data-stu-id="e0ef4-104">Begins a task for appointment rebasing given a list of appointments, usually obtained from [IOlkApptRebaser::EndEnumerateAppointments](iolkapptrebaser-endenumerateappointments.md).</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="e0ef4-105">Краткие сведения</span><span class="sxs-lookup"><span data-stu-id="e0ef4-105">Quick info</span></span>

<span data-ttu-id="e0ef4-106">See [IOlkApptRebaser](iolkapptrebaser.md).</span><span class="sxs-lookup"><span data-stu-id="e0ef4-106">See [IOlkApptRebaser](iolkapptrebaser.md).</span></span>
  
```cpp
HRESULT BeginRebaseAppointments( 
    const SRowSet *pRows, 
    PFNREBASETASKPROGRESS pfnProgress, 
    PFNREBASETASKCOMPLETE pfnComplete, 
    void **ppContext);
```

## <a name="parameters"></a><span data-ttu-id="e0ef4-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="e0ef4-107">Parameters</span></span>

<span data-ttu-id="e0ef4-108">_Провс_</span><span class="sxs-lookup"><span data-stu-id="e0ef4-108">_pRows_</span></span>
  
> <span data-ttu-id="e0ef4-p101">[in] Required. A pointer to an [SRowSet](https://msdn.microsoft.com/library/7e3761be-afd6-46cb-9a08-25e9016c1241%28Office.15%29.aspx) structure that describes the appointments that need rebasing. This structure is usually obtained from a prior call to [IOlkApptRebaser::EndEnumerateAppointments](iolkapptrebaser-endenumerateappointments.md).</span><span class="sxs-lookup"><span data-stu-id="e0ef4-p101">[in] Required. A pointer to an [SRowSet](https://msdn.microsoft.com/library/7e3761be-afd6-46cb-9a08-25e9016c1241%28Office.15%29.aspx) structure that describes the appointments that need rebasing. This structure is usually obtained from a prior call to [IOlkApptRebaser::EndEnumerateAppointments](iolkapptrebaser-endenumerateappointments.md).</span></span>
    
<span data-ttu-id="e0ef4-112">_Пфнпрогресс_</span><span class="sxs-lookup"><span data-stu-id="e0ef4-112">_pfnProgress_</span></span>
  
> <span data-ttu-id="e0ef4-p102">[in] Optional. A pointer to a rebase task progress function to receive progress. **PFNREBASETASKPROGRESS** is defined in tzmovelib.h.</span><span class="sxs-lookup"><span data-stu-id="e0ef4-p102">[in] Optional. A pointer to a rebase task progress function to receive progress. **PFNREBASETASKPROGRESS** is defined in tzmovelib.h.</span></span> 
    
<span data-ttu-id="e0ef4-116">_Пфнкомплете_</span><span class="sxs-lookup"><span data-stu-id="e0ef4-116">_pfnComplete_</span></span>
  
> <span data-ttu-id="e0ef4-p103">[out] Optional. A pointer to a rebase task completion function to receive notification of rebase completion. **PFNREBASETASKCOMPLETE** is defined in tzmovelib.h.</span><span class="sxs-lookup"><span data-stu-id="e0ef4-p103">[out] Optional. A pointer to a rebase task completion function to receive notification of rebase completion. **PFNREBASETASKCOMPLETE** is defined in tzmovelib.h.</span></span> 
    
<span data-ttu-id="e0ef4-120">_Ппконтекст_</span><span class="sxs-lookup"><span data-stu-id="e0ef4-120">_ppContext_</span></span>
  
> <span data-ttu-id="e0ef4-p104">[out] Required. A pointer to a pointer to the returned context. This context will usually be passed to [IOlkApptRebaser::EndRebaseAppointments](iolkapptrebaser-endrebaseappointments.md).</span><span class="sxs-lookup"><span data-stu-id="e0ef4-p104">[out] Required. A pointer to a pointer to the returned context. This context will usually be passed to [IOlkApptRebaser::EndRebaseAppointments](iolkapptrebaser-endrebaseappointments.md).</span></span>
    
## <a name="return-values"></a><span data-ttu-id="e0ef4-124">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="e0ef4-124">Return values</span></span>

<span data-ttu-id="e0ef4-125">S_OK if the call succeeded; otherwise, an error code.</span><span class="sxs-lookup"><span data-stu-id="e0ef4-125">S_OK if the call succeeded; otherwise, an error code.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="e0ef4-126">Замечания</span><span class="sxs-lookup"><span data-stu-id="e0ef4-126">Remarks</span></span>

<span data-ttu-id="e0ef4-127">This task runs on a new thread.</span><span class="sxs-lookup"><span data-stu-id="e0ef4-127">This task runs on a new thread.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="e0ef4-128">См. также</span><span class="sxs-lookup"><span data-stu-id="e0ef4-128">See also</span></span>

- [<span data-ttu-id="e0ef4-129">About rebasing calendars programmatically for Daylight Saving Time</span><span class="sxs-lookup"><span data-stu-id="e0ef4-129">About rebasing calendars programmatically for Daylight Saving Time</span></span>](about-rebasing-calendars-programmatically-for-daylight-saving-time.md)

