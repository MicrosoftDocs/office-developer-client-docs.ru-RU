---
title: Иолкапптребасерендребасеаппоинтментс
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: e47d5a8d-6a13-f430-fbfd-00df04b4a006
description: Waits for appointment rebasing to complete and retrieves the results.
ms.openlocfilehash: a6e62cff9efea1fc7079d04bc9b032b5637f8847
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32321891"
---
# <a name="iolkapptrebaserendrebaseappointments"></a><span data-ttu-id="a9f5b-103">IOlkApptRebaser::EndRebaseAppointments</span><span class="sxs-lookup"><span data-stu-id="a9f5b-103">IOlkApptRebaser::EndRebaseAppointments</span></span>

<span data-ttu-id="a9f5b-104">Waits for appointment rebasing to complete and retrieves the results.</span><span class="sxs-lookup"><span data-stu-id="a9f5b-104">Waits for appointment rebasing to complete and retrieves the results.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="a9f5b-105">Краткие сведения</span><span class="sxs-lookup"><span data-stu-id="a9f5b-105">Quick info</span></span>

<span data-ttu-id="a9f5b-106">See [IOlkApptRebaser](iolkapptrebaser.md).</span><span class="sxs-lookup"><span data-stu-id="a9f5b-106">See [IOlkApptRebaser](iolkapptrebaser.md).</span></span>
  
```cpp
HRESULT EndRebaseAppointments( 
    void *pContext, 
    HRESULT *phResult);
```

## <a name="parameters"></a><span data-ttu-id="a9f5b-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="a9f5b-107">Parameters</span></span>

<span data-ttu-id="a9f5b-108">_Пконтекст_</span><span class="sxs-lookup"><span data-stu-id="a9f5b-108">_pContext_</span></span>
  
> <span data-ttu-id="a9f5b-p101">[in] Required. A pointer to the context obtained from a call to [IOlkApptRebaser::BeginRebaseAppointments](iolkapptrebaser-beginrebaseappointments.md).</span><span class="sxs-lookup"><span data-stu-id="a9f5b-p101">[in] Required. A pointer to the context obtained from a call to [IOlkApptRebaser::BeginRebaseAppointments](iolkapptrebaser-beginrebaseappointments.md).</span></span>
    
<span data-ttu-id="a9f5b-111">_Фресулт_</span><span class="sxs-lookup"><span data-stu-id="a9f5b-111">_phResult_</span></span>
  
> <span data-ttu-id="a9f5b-p102">[out] Required. A pointer to an **HRESULT** to retrieve the result of the rebasing operation.</span><span class="sxs-lookup"><span data-stu-id="a9f5b-p102">[out] Required. A pointer to an **HRESULT** to retrieve the result of the rebasing operation.</span></span> 
    
## <a name="return-values"></a><span data-ttu-id="a9f5b-114">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="a9f5b-114">Return values</span></span>

<span data-ttu-id="a9f5b-115">S_OK if the call succeeded; otherwise, an error code.</span><span class="sxs-lookup"><span data-stu-id="a9f5b-115">S_OK if the call succeeded; otherwise, an error code.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="a9f5b-116">См. также</span><span class="sxs-lookup"><span data-stu-id="a9f5b-116">See also</span></span>

- [<span data-ttu-id="a9f5b-117">About rebasing calendars programmatically for Daylight Saving Time</span><span class="sxs-lookup"><span data-stu-id="a9f5b-117">About rebasing calendars programmatically for Daylight Saving Time</span></span>](about-rebasing-calendars-programmatically-for-daylight-saving-time.md)

