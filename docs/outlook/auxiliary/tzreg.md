---
title: TZREG
manager: soliver
ms.date: 12/07/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: a353e1a3-0187-20af-b9ba-43438f6024d5
description: Определяет время начала перехода на летнее время, время возврата к стандартному времени и время перехода на летнее время.
ms.openlocfilehash: 136ff6ad0c1a9bc2ad61ef7ba698d66d645165d8
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33419368"
---
# <a name="tzreg"></a><span data-ttu-id="64910-103">TZREG</span><span class="sxs-lookup"><span data-stu-id="64910-103">TZREG</span></span>

<span data-ttu-id="64910-104">Определяет время начала перехода на летнее время, время возврата к стандартному времени и время перехода на летнее время.</span><span class="sxs-lookup"><span data-stu-id="64910-104">Defines when daylight saving time starts, when the return to standard time occurs, and how many hours the daylight saving shift is.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="64910-105">Краткие сведения</span><span class="sxs-lookup"><span data-stu-id="64910-105">Quick info</span></span>

```cpp
typedef struct RenTimeZone { 
    long        lBias;  
    long        lStandardBias; 
    long        lDaylightBias; 
    SYSTEMTIME  stStandardDate; 
    SYSTEMTIME  stDaylightDate; 
} TZREG; 

```

## <a name="members"></a><span data-ttu-id="64910-106">Элементы</span><span class="sxs-lookup"><span data-stu-id="64910-106">Members</span></span>

<span data-ttu-id="64910-107">_lBias_</span><span class="sxs-lookup"><span data-stu-id="64910-107">_lBias_</span></span>
  
> <span data-ttu-id="64910-108">Смещение по гринвичскому времени (GMT).</span><span class="sxs-lookup"><span data-stu-id="64910-108">The offset from Greenwich Mean Time (GMT).</span></span>
    
<span data-ttu-id="64910-109">_lStandardBias_</span><span class="sxs-lookup"><span data-stu-id="64910-109">_lStandardBias_</span></span>
  
> <span data-ttu-id="64910-110">Смещение смещения в стандартное время.</span><span class="sxs-lookup"><span data-stu-id="64910-110">The offset from bias during standard time.</span></span>
    
<span data-ttu-id="64910-111">_lDaylightBias_</span><span class="sxs-lookup"><span data-stu-id="64910-111">_lDaylightBias_</span></span>
  
> <span data-ttu-id="64910-112">Смещение смещения в летнее время.</span><span class="sxs-lookup"><span data-stu-id="64910-112">The offset from bias during daylight saving time.</span></span>
    
<span data-ttu-id="64910-113">_stStandardDate_</span><span class="sxs-lookup"><span data-stu-id="64910-113">_stStandardDate_</span></span>
  
> <span data-ttu-id="64910-114">Время перехода на стандартное время.</span><span class="sxs-lookup"><span data-stu-id="64910-114">The time to switch to standard time.</span></span>
    
<span data-ttu-id="64910-115">_stDaylightDate_</span><span class="sxs-lookup"><span data-stu-id="64910-115">_stDaylightDate_</span></span>
  
> <span data-ttu-id="64910-116">Время перехода на летнее время.</span><span class="sxs-lookup"><span data-stu-id="64910-116">The time to switch to daylight saving time.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="64910-117">Примечания</span><span class="sxs-lookup"><span data-stu-id="64910-117">Remarks</span></span>

<span data-ttu-id="64910-118">Эта структура аналогична **TIME_ZONE_INFORMATION.**</span><span class="sxs-lookup"><span data-stu-id="64910-118">This structure is similar to **TIME_ZONE_INFORMATION**.</span></span> <span data-ttu-id="64910-119">Это структура, используемая устаревшими клиентами для хранения сведений о часовом поясе для повторяющихся собраний.</span><span class="sxs-lookup"><span data-stu-id="64910-119">This is the structure used by legacy clients to store time zone information for recurring meetings.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="64910-120">См. также</span><span class="sxs-lookup"><span data-stu-id="64910-120">See also</span></span>

- [<span data-ttu-id="64910-121">Сведения о программном переводе календарей на летнее время</span><span class="sxs-lookup"><span data-stu-id="64910-121">About rebasing calendars programmatically for Daylight Saving Time</span></span>](about-rebasing-calendars-programmatically-for-daylight-saving-time.md)  
- [<span data-ttu-id="64910-122">HrCreateApptRebaser</span><span class="sxs-lookup"><span data-stu-id="64910-122">HrCreateApptRebaser</span></span>](hrcreateapptrebaser.md)  
- [<span data-ttu-id="64910-123">TZRULE</span><span class="sxs-lookup"><span data-stu-id="64910-123">TZRULE</span></span>](tzrule.md)

