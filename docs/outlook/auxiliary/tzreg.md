---
title: TZREG
manager: soliver
ms.date: 12/07/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: a353e1a3-0187-20af-b9ba-43438f6024d5
description: Определяет, когда начинается летнее время, когда происходит возврат к стандартному времени, и сколько часов составляет переход на летнее время.
ms.openlocfilehash: 136ff6ad0c1a9bc2ad61ef7ba698d66d645165d8
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33419368"
---
# <a name="tzreg"></a><span data-ttu-id="18125-103">TZREG</span><span class="sxs-lookup"><span data-stu-id="18125-103">TZREG</span></span>

<span data-ttu-id="18125-104">Определяет, когда начинается летнее время, когда происходит возврат к стандартному времени, и сколько часов составляет переход на летнее время.</span><span class="sxs-lookup"><span data-stu-id="18125-104">Defines when daylight saving time starts, when the return to standard time occurs, and how many hours the daylight saving shift is.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="18125-105">Краткие сведения</span><span class="sxs-lookup"><span data-stu-id="18125-105">Quick info</span></span>

```cpp
typedef struct RenTimeZone { 
    long        lBias;  
    long        lStandardBias; 
    long        lDaylightBias; 
    SYSTEMTIME  stStandardDate; 
    SYSTEMTIME  stDaylightDate; 
} TZREG; 

```

## <a name="members"></a><span data-ttu-id="18125-106">Элементы</span><span class="sxs-lookup"><span data-stu-id="18125-106">Members</span></span>

<span data-ttu-id="18125-107">_lBias_</span><span class="sxs-lookup"><span data-stu-id="18125-107">_lBias_</span></span>
  
> <span data-ttu-id="18125-108">Смещение от гринвичского времени (GMT).</span><span class="sxs-lookup"><span data-stu-id="18125-108">The offset from Greenwich Mean Time (GMT).</span></span>
    
<span data-ttu-id="18125-109">_lStandardBias_</span><span class="sxs-lookup"><span data-stu-id="18125-109">_lStandardBias_</span></span>
  
> <span data-ttu-id="18125-110">Смещение от смещения в стандартное время.</span><span class="sxs-lookup"><span data-stu-id="18125-110">The offset from bias during standard time.</span></span>
    
<span data-ttu-id="18125-111">_lDaylightBias_</span><span class="sxs-lookup"><span data-stu-id="18125-111">_lDaylightBias_</span></span>
  
> <span data-ttu-id="18125-112">Смещение от смещения во время летнего времени.</span><span class="sxs-lookup"><span data-stu-id="18125-112">The offset from bias during daylight saving time.</span></span>
    
<span data-ttu-id="18125-113">_stStandardDate_</span><span class="sxs-lookup"><span data-stu-id="18125-113">_stStandardDate_</span></span>
  
> <span data-ttu-id="18125-114">Время перехода на стандартное время.</span><span class="sxs-lookup"><span data-stu-id="18125-114">The time to switch to standard time.</span></span>
    
<span data-ttu-id="18125-115">_stDaylightDate_</span><span class="sxs-lookup"><span data-stu-id="18125-115">_stDaylightDate_</span></span>
  
> <span data-ttu-id="18125-116">Время перехода на летнее время.</span><span class="sxs-lookup"><span data-stu-id="18125-116">The time to switch to daylight saving time.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="18125-117">Примечания</span><span class="sxs-lookup"><span data-stu-id="18125-117">Remarks</span></span>

<span data-ttu-id="18125-118">Эта структура похожа на **TIME_ZONE_INFORMATION**.</span><span class="sxs-lookup"><span data-stu-id="18125-118">This structure is similar to **TIME_ZONE_INFORMATION**.</span></span> <span data-ttu-id="18125-119">Это структура, используемая устаревшими клиентами для хранения данных часовых поясов для повторяющихся собраний.</span><span class="sxs-lookup"><span data-stu-id="18125-119">This is the structure used by legacy clients to store time zone information for recurring meetings.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="18125-120">См. также</span><span class="sxs-lookup"><span data-stu-id="18125-120">See also</span></span>

- [<span data-ttu-id="18125-121">Сведения о программном переводе календарей на летнее время</span><span class="sxs-lookup"><span data-stu-id="18125-121">About rebasing calendars programmatically for Daylight Saving Time</span></span>](about-rebasing-calendars-programmatically-for-daylight-saving-time.md)  
- [<span data-ttu-id="18125-122">HrCreateApptRebaser</span><span class="sxs-lookup"><span data-stu-id="18125-122">HrCreateApptRebaser</span></span>](hrcreateapptrebaser.md)  
- [<span data-ttu-id="18125-123">TZRULE</span><span class="sxs-lookup"><span data-stu-id="18125-123">TZRULE</span></span>](tzrule.md)

