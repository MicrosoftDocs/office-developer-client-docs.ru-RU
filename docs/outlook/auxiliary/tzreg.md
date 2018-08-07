---
title: TZREG
manager: soliver
ms.date: 12/07/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: a353e1a3-0187-20af-b9ba-43438f6024d5
description: Определяет при запуске летнего времени, когда происходит возврат стандартного времени и сколько часов — это летнего shift.
ms.openlocfilehash: 85812ab053d77c07f9360b6bf3a1faaf72cae573
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19807971"
---
# <a name="tzreg"></a><span data-ttu-id="0bde2-103">TZREG</span><span class="sxs-lookup"><span data-stu-id="0bde2-103">TZREG</span></span>

<span data-ttu-id="0bde2-104">Определяет при запуске летнего времени, когда происходит возврат стандартного времени и сколько часов — это летнего shift.</span><span class="sxs-lookup"><span data-stu-id="0bde2-104">Defines when daylight saving time starts, when the return to standard time occurs, and how many hours the daylight saving shift is.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="0bde2-105">Краткие сведения</span><span class="sxs-lookup"><span data-stu-id="0bde2-105">Quick info</span></span>

```cpp
typedef struct RenTimeZone { 
    long        lBias;  
    long        lStandardBias; 
    long        lDaylightBias; 
    SYSTEMTIME  stStandardDate; 
    SYSTEMTIME  stDaylightDate; 
} TZREG; 

```

## <a name="members"></a><span data-ttu-id="0bde2-106">Members</span><span class="sxs-lookup"><span data-stu-id="0bde2-106">Members</span></span>

<span data-ttu-id="0bde2-107">_lBias_</span><span class="sxs-lookup"><span data-stu-id="0bde2-107">_lBias_</span></span>
  
> <span data-ttu-id="0bde2-108">Смещение от среднего времени по Гринвичу (GMT).</span><span class="sxs-lookup"><span data-stu-id="0bde2-108">The offset from Greenwich Mean Time (GMT).</span></span>
    
<span data-ttu-id="0bde2-109">_lStandardBias_</span><span class="sxs-lookup"><span data-stu-id="0bde2-109">_lStandardBias_</span></span>
  
> <span data-ttu-id="0bde2-110">Смещение от bias во время (зима).</span><span class="sxs-lookup"><span data-stu-id="0bde2-110">The offset from bias during standard time.</span></span>
    
<span data-ttu-id="0bde2-111">_lDaylightBias_</span><span class="sxs-lookup"><span data-stu-id="0bde2-111">_lDaylightBias_</span></span>
  
> <span data-ttu-id="0bde2-112">Смещение от bias во время перехода на летнее время.</span><span class="sxs-lookup"><span data-stu-id="0bde2-112">The offset from bias during daylight saving time.</span></span>
    
<span data-ttu-id="0bde2-113">_stStandardDate_</span><span class="sxs-lookup"><span data-stu-id="0bde2-113">_stStandardDate_</span></span>
  
> <span data-ttu-id="0bde2-114">Время, чтобы переключиться на стандартное время.</span><span class="sxs-lookup"><span data-stu-id="0bde2-114">The time to switch to standard time.</span></span>
    
<span data-ttu-id="0bde2-115">_stDaylightDate_</span><span class="sxs-lookup"><span data-stu-id="0bde2-115">_stDaylightDate_</span></span>
  
> <span data-ttu-id="0bde2-116">Время для перехода на летнее время.</span><span class="sxs-lookup"><span data-stu-id="0bde2-116">The time to switch to daylight saving time.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="0bde2-117">Замечания</span><span class="sxs-lookup"><span data-stu-id="0bde2-117">Remarks</span></span>

<span data-ttu-id="0bde2-118">Эта структура аналогична **TIME_ZONE_INFORMATION**.</span><span class="sxs-lookup"><span data-stu-id="0bde2-118">This structure is similar to **TIME_ZONE_INFORMATION**.</span></span> <span data-ttu-id="0bde2-119">Это структуры, используемый в устаревших клиентов для хранения сведений о часовом поясе для повторяющихся собраний.</span><span class="sxs-lookup"><span data-stu-id="0bde2-119">This is the structure used by legacy clients to store time zone information for recurring meetings.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="0bde2-120">См. также</span><span class="sxs-lookup"><span data-stu-id="0bde2-120">See also</span></span>

- [<span data-ttu-id="0bde2-121">About rebasing calendars programmatically for Daylight Saving Time</span><span class="sxs-lookup"><span data-stu-id="0bde2-121">About rebasing calendars programmatically for Daylight Saving Time</span></span>](about-rebasing-calendars-programmatically-for-daylight-saving-time.md)  
- [<span data-ttu-id="0bde2-122">HrCreateApptRebaser</span><span class="sxs-lookup"><span data-stu-id="0bde2-122">HrCreateApptRebaser</span></span>](hrcreateapptrebaser.md)  
- [<span data-ttu-id="0bde2-123">TZRULE</span><span class="sxs-lookup"><span data-stu-id="0bde2-123">TZRULE</span></span>](tzrule.md)

