---
title: TZRULE
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 75ed353c-7d3e-e148-4057-715e82a0f32c
description: Задает сведения о при запуске летнее время и года, в котором это правило часового пояса сначала вступает в силу для часового пояса.
ms.openlocfilehash: 77d56d238d959992bfadd2d8c143391ca6fa4d5b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19807969"
---
# <a name="tzrule"></a><span data-ttu-id="76235-103">TZRULE</span><span class="sxs-lookup"><span data-stu-id="76235-103">TZRULE</span></span>

<span data-ttu-id="76235-104">Задает сведения о при запуске летнее время и года, в котором это правило часового пояса сначала вступает в силу для часового пояса.</span><span class="sxs-lookup"><span data-stu-id="76235-104">Specifies information for a time zone rule about when daylight saving time starts, and the year in which that time zone rule first takes effect.</span></span> 
  
## <a name="quick-info"></a><span data-ttu-id="76235-105">Краткие сведения</span><span class="sxs-lookup"><span data-stu-id="76235-105">Quick info</span></span>

```cpp
typedef struct { 
    WORD        wFlags;  
    SYSTEMTIME  stStart; 
    TZREG       TZReg; 
} TZRULE;
```

## <a name="members"></a><span data-ttu-id="76235-106">Members</span><span class="sxs-lookup"><span data-stu-id="76235-106">Members</span></span>

<span data-ttu-id="76235-107">_wFlags_</span><span class="sxs-lookup"><span data-stu-id="76235-107">_wFlags_</span></span>
  
> <span data-ttu-id="76235-108">Флаги для этого элемента укажите подробные сведения для этого правила часового пояса.</span><span class="sxs-lookup"><span data-stu-id="76235-108">The flags set for this member identify specific details for this time zone rule.</span></span> <span data-ttu-id="76235-109">Флаги, как показано ниже:</span><span class="sxs-lookup"><span data-stu-id="76235-109">The possible flags are as follows:</span></span>
    
   - <span data-ttu-id="76235-110">**TZRULE_FLAG_EFFECTIVE_TZREG** — определяет правило, что следует использовать в настоящее время.</span><span class="sxs-lookup"><span data-stu-id="76235-110">**TZRULE_FLAG_EFFECTIVE_TZREG** —Identifies the rule as the one that should be used currently.</span></span> <span data-ttu-id="76235-111">Только одно правило может быть помечен как действующие правила.</span><span class="sxs-lookup"><span data-stu-id="76235-111">Only one rule can be marked as the effective rule.</span></span> <span data-ttu-id="76235-112">Все другие правила используются только в целях сравнения.</span><span class="sxs-lookup"><span data-stu-id="76235-112">All other rules are for comparison purposes only.</span></span> 
    
   - <span data-ttu-id="76235-113">**TZRULE_FLAG_RECUR_CURRENT_TZREG** — повторяющихся собраний определяет правило, как правило, в [PidLidTimeZoneStruct](http://msdn.microsoft.com/library/2acf0036-2f3e-4f90-8614-7aa667860f74%28Office.15%29.aspx)сопоставления.</span><span class="sxs-lookup"><span data-stu-id="76235-113">**TZRULE_FLAG_RECUR_CURRENT_TZREG** —On recurring meetings, identifies the rule as matching the rule in [PidLidTimeZoneStruct](http://msdn.microsoft.com/library/2acf0036-2f3e-4f90-8614-7aa667860f74%28Office.15%29.aspx).</span></span> <span data-ttu-id="76235-114">Это можно использовать для определения, были ли изменены **PidLidTimeZoneStruct** значительно при использовании устаревшего клиента, что было бы в противном случае — новый, более полную свойства.</span><span class="sxs-lookup"><span data-stu-id="76235-114">This can be used to detect whether **PidLidTimeZoneStruct** has been modified significantly by a legacy client, which would be otherwise unaware of the new, more complete property.</span></span> 
    
<span data-ttu-id="76235-115">_stStart_</span><span class="sxs-lookup"><span data-stu-id="76235-115">_stStart_</span></span>
  
> <span data-ttu-id="76235-116">Время в формате UTC (UTC) начала часового пояса.</span><span class="sxs-lookup"><span data-stu-id="76235-116">The time in Coordinated Universal Time (UTC) that the time zone rule started.</span></span>
    
<span data-ttu-id="76235-117">_TZReg_</span><span class="sxs-lookup"><span data-stu-id="76235-117">_TZReg_</span></span>
  
> <span data-ttu-id="76235-118">Сведения о часового пояса для часового пояса.</span><span class="sxs-lookup"><span data-stu-id="76235-118">The time zone information for the time zone rule.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="76235-119">Замечания</span><span class="sxs-lookup"><span data-stu-id="76235-119">Remarks</span></span>

<span data-ttu-id="76235-120">Эта структура дополняет [TZREG](tzreg.md) содержат дополнительные сведения, указывающий, когда правила часового пояса вступили в силу.</span><span class="sxs-lookup"><span data-stu-id="76235-120">This structure augments [TZREG](tzreg.md) by providing additional information indicating when time zone rules take effect.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="76235-121">См. также</span><span class="sxs-lookup"><span data-stu-id="76235-121">See also</span></span>

- [<span data-ttu-id="76235-122">About rebasing calendars programmatically for Daylight Saving Time</span><span class="sxs-lookup"><span data-stu-id="76235-122">About rebasing calendars programmatically for Daylight Saving Time</span></span>](about-rebasing-calendars-programmatically-for-daylight-saving-time.md) 
- [<span data-ttu-id="76235-123">Constants (Outlook exported APIs)</span><span class="sxs-lookup"><span data-stu-id="76235-123">Constants (Outlook exported APIs)</span></span>](constants-outlook-exported-apis.md)
- [<span data-ttu-id="76235-124">HrCreateApptRebaser</span><span class="sxs-lookup"><span data-stu-id="76235-124">HrCreateApptRebaser</span></span>](hrcreateapptrebaser.md)
- [<span data-ttu-id="76235-125">TZDEFINITION</span><span class="sxs-lookup"><span data-stu-id="76235-125">TZDEFINITION</span></span>](tzdefinition.md)

