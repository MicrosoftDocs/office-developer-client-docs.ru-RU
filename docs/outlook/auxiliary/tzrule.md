---
title: TZRULE
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 75ed353c-7d3e-e148-4057-715e82a0f32c
description: Задает сведения о том, когда начинается летнее время, а также год вступления в силу правила с часовым поясом.
ms.openlocfilehash: 71ede7c0061a058c2dd85c7b9b36c42583a6bb84
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328618"
---
# <a name="tzrule"></a><span data-ttu-id="8c2c2-103">TZRULE</span><span class="sxs-lookup"><span data-stu-id="8c2c2-103">TZRULE</span></span>

<span data-ttu-id="8c2c2-104">Задает сведения о том, когда начинается летнее время, а также год вступления в силу правила с часовым поясом.</span><span class="sxs-lookup"><span data-stu-id="8c2c2-104">Specifies information for a time zone rule about when daylight saving time starts, and the year in which that time zone rule first takes effect.</span></span> 
  
## <a name="quick-info"></a><span data-ttu-id="8c2c2-105">Краткие сведения</span><span class="sxs-lookup"><span data-stu-id="8c2c2-105">Quick info</span></span>

```cpp
typedef struct { 
    WORD        wFlags;  
    SYSTEMTIME  stStart; 
    TZREG       TZReg; 
} TZRULE;
```

## <a name="members"></a><span data-ttu-id="8c2c2-106">Элементы</span><span class="sxs-lookup"><span data-stu-id="8c2c2-106">Members</span></span>

<span data-ttu-id="8c2c2-107">_Вфлагс_</span><span class="sxs-lookup"><span data-stu-id="8c2c2-107">_wFlags_</span></span>
  
> <span data-ttu-id="8c2c2-108">Флаги, заданные для этого элемента, определяют конкретные сведения для этого правила часового пояса.</span><span class="sxs-lookup"><span data-stu-id="8c2c2-108">The flags set for this member identify specific details for this time zone rule.</span></span> <span data-ttu-id="8c2c2-109">Ниже приведены возможные флаги.</span><span class="sxs-lookup"><span data-stu-id="8c2c2-109">The possible flags are as follows:</span></span>
    
   - <span data-ttu-id="8c2c2-110">**Тзруле_флаг_еффективе_тзрег** — определяет правило, которое должно использоваться в данный момент.</span><span class="sxs-lookup"><span data-stu-id="8c2c2-110">**TZRULE_FLAG_EFFECTIVE_TZREG** —Identifies the rule as the one that should be used currently.</span></span> <span data-ttu-id="8c2c2-111">Только одно правило может быть помечено как действующее правило.</span><span class="sxs-lookup"><span data-stu-id="8c2c2-111">Only one rule can be marked as the effective rule.</span></span> <span data-ttu-id="8c2c2-112">Все остальные правила предназначены только для сравнения.</span><span class="sxs-lookup"><span data-stu-id="8c2c2-112">All other rules are for comparison purposes only.</span></span> 
    
   - <span data-ttu-id="8c2c2-113">**Тзруле_флаг_рекур_куррент_тзрег** — для повторяющихся собраний — определяет правило, совпадающее с правилом в [PidLidTimeZoneStruct](https://msdn.microsoft.com/library/2acf0036-2f3e-4f90-8614-7aa667860f74%28Office.15%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="8c2c2-113">**TZRULE_FLAG_RECUR_CURRENT_TZREG** —On recurring meetings, identifies the rule as matching the rule in [PidLidTimeZoneStruct](https://msdn.microsoft.com/library/2acf0036-2f3e-4f90-8614-7aa667860f74%28Office.15%29.aspx).</span></span> <span data-ttu-id="8c2c2-114">Это можно использовать для обнаружения того, был ли **PidLidTimeZoneStruct** изменен устаревшим клиентом, что в противном случае не будет знать о новом свойстве Complete.</span><span class="sxs-lookup"><span data-stu-id="8c2c2-114">This can be used to detect whether **PidLidTimeZoneStruct** has been modified significantly by a legacy client, which would be otherwise unaware of the new, more complete property.</span></span> 
    
<span data-ttu-id="8c2c2-115">_Стстарт_</span><span class="sxs-lookup"><span data-stu-id="8c2c2-115">_stStart_</span></span>
  
> <span data-ttu-id="8c2c2-116">Время, в течение которого было запущено правило часового пояса, в формате UTC.</span><span class="sxs-lookup"><span data-stu-id="8c2c2-116">The time in Coordinated Universal Time (UTC) that the time zone rule started.</span></span>
    
<span data-ttu-id="8c2c2-117">_TZReg_</span><span class="sxs-lookup"><span data-stu-id="8c2c2-117">_TZReg_</span></span>
  
> <span data-ttu-id="8c2c2-118">Сведения о часовом поясе для правила часового пояса.</span><span class="sxs-lookup"><span data-stu-id="8c2c2-118">The time zone information for the time zone rule.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="8c2c2-119">Комментарии</span><span class="sxs-lookup"><span data-stu-id="8c2c2-119">Remarks</span></span>

<span data-ttu-id="8c2c2-120">Эта структура дополняет [TZREG](tzreg.md) , предоставляя дополнительные сведения о том, когда правила часовых поясов вступают в силу.</span><span class="sxs-lookup"><span data-stu-id="8c2c2-120">This structure augments [TZREG](tzreg.md) by providing additional information indicating when time zone rules take effect.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="8c2c2-121">См. также</span><span class="sxs-lookup"><span data-stu-id="8c2c2-121">See also</span></span>

- [<span data-ttu-id="8c2c2-122">About rebasing calendars programmatically for Daylight Saving Time</span><span class="sxs-lookup"><span data-stu-id="8c2c2-122">About rebasing calendars programmatically for Daylight Saving Time</span></span>](about-rebasing-calendars-programmatically-for-daylight-saving-time.md) 
- [<span data-ttu-id="8c2c2-123">Constants (Outlook exported APIs)</span><span class="sxs-lookup"><span data-stu-id="8c2c2-123">Constants (Outlook exported APIs)</span></span>](constants-outlook-exported-apis.md)
- [<span data-ttu-id="8c2c2-124">HrCreateApptRebaser</span><span class="sxs-lookup"><span data-stu-id="8c2c2-124">HrCreateApptRebaser</span></span>](hrcreateapptrebaser.md)
- [<span data-ttu-id="8c2c2-125">TZDEFINITION</span><span class="sxs-lookup"><span data-stu-id="8c2c2-125">TZDEFINITION</span></span>](tzdefinition.md)

