---
title: IOlkApptRebaserEndRebaseAppointments
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: e47d5a8d-6a13-f430-fbfd-00df04b4a006
description: Waits for appointment rebasing to complete and retrieves the results.
ms.openlocfilehash: fd27021ce05b1d5b95fd258e0ee89b5bd4f2c7db
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19807877"
---
# <a name="iolkapptrebaserendrebaseappointments"></a><span data-ttu-id="79848-103">IOlkApptRebaser::EndRebaseAppointments</span><span class="sxs-lookup"><span data-stu-id="79848-103">IOlkApptRebaser::EndRebaseAppointments</span></span>

<span data-ttu-id="79848-104">Waits for appointment rebasing to complete and retrieves the results.</span><span class="sxs-lookup"><span data-stu-id="79848-104">Waits for appointment rebasing to complete and retrieves the results.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="79848-105">Краткие сведения</span><span class="sxs-lookup"><span data-stu-id="79848-105">Quick info</span></span>

<span data-ttu-id="79848-106">See [IOlkApptRebaser](iolkapptrebaser.md).</span><span class="sxs-lookup"><span data-stu-id="79848-106">See [IOlkApptRebaser](iolkapptrebaser.md).</span></span>
  
```cpp
HRESULT EndRebaseAppointments( 
    void *pContext, 
    HRESULT *phResult);
```

## <a name="parameters"></a><span data-ttu-id="79848-107">Parameters</span><span class="sxs-lookup"><span data-stu-id="79848-107">Parameters</span></span>

<span data-ttu-id="79848-108">_pContext_</span><span class="sxs-lookup"><span data-stu-id="79848-108">_pContext_</span></span>
  
> <span data-ttu-id="79848-p101">[in] Required. A pointer to the context obtained from a call to [IOlkApptRebaser::BeginRebaseAppointments](iolkapptrebaser-beginrebaseappointments.md).</span><span class="sxs-lookup"><span data-stu-id="79848-p101">[in] Required. A pointer to the context obtained from a call to [IOlkApptRebaser::BeginRebaseAppointments](iolkapptrebaser-beginrebaseappointments.md).</span></span>
    
<span data-ttu-id="79848-111">_phResult_</span><span class="sxs-lookup"><span data-stu-id="79848-111">_phResult_</span></span>
  
> <span data-ttu-id="79848-p102">[out] Required. A pointer to an **HRESULT** to retrieve the result of the rebasing operation.</span><span class="sxs-lookup"><span data-stu-id="79848-p102">[out] Required. A pointer to an **HRESULT** to retrieve the result of the rebasing operation.</span></span> 
    
## <a name="return-values"></a><span data-ttu-id="79848-114">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="79848-114">Return values</span></span>

<span data-ttu-id="79848-115">S_OK if the call succeeded; otherwise, an error code.</span><span class="sxs-lookup"><span data-stu-id="79848-115">S_OK if the call succeeded; otherwise, an error code.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="79848-116">См. также</span><span class="sxs-lookup"><span data-stu-id="79848-116">See also</span></span>

- [<span data-ttu-id="79848-117">About rebasing calendars programmatically for Daylight Saving Time</span><span class="sxs-lookup"><span data-stu-id="79848-117">About rebasing calendars programmatically for Daylight Saving Time</span></span>](about-rebasing-calendars-programmatically-for-daylight-saving-time.md)

