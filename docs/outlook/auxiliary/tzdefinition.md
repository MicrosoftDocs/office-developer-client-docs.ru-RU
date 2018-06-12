---
title: TZDEFINITION
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 0ae21571-2299-6407-807c-428668bb6798
description: Представляет всей часового пояса, включая все правила shift журналу, текущие и будущие часового пояса на летнее время.
ms.openlocfilehash: f436216f5da882ea8ac144e6bd384e51e31abb8e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19807981"
---
# <a name="tzdefinition"></a><span data-ttu-id="660d2-103">TZDEFINITION</span><span class="sxs-lookup"><span data-stu-id="660d2-103">TZDEFINITION</span></span>

<span data-ttu-id="660d2-104">Представляет всей часового пояса, включая все правила shift журналу, текущие и будущие часового пояса на летнее время.</span><span class="sxs-lookup"><span data-stu-id="660d2-104">Represents an entire time zone including all historical, current, and future time zone shift rules for daylight saving time.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="660d2-105">Краткие сведения</span><span class="sxs-lookup"><span data-stu-id="660d2-105">Quick info</span></span>

```cpp
typedef struct { 
    WORD     wFlags;  
    LPWSTR   pwszKeyName; 
    WORD     cRules; 
    TZRULE*  rgRules; 
} TZDEFINITION;
```

## <a name="members"></a><span data-ttu-id="660d2-106">Элементы</span><span class="sxs-lookup"><span data-stu-id="660d2-106">Members</span></span>

<span data-ttu-id="660d2-107">_wFlags_</span><span class="sxs-lookup"><span data-stu-id="660d2-107">_wFlags_</span></span>
  
> <span data-ttu-id="660d2-108">Указывает допустимое имя раздела, который представляет часового пояса в реестре Windows.</span><span class="sxs-lookup"><span data-stu-id="660d2-108">Indicates that the key name that represents the time zone in the Windows registry is valid.</span></span> <span data-ttu-id="660d2-109">Поскольку каждый часовой пояс всегда должны идентифицироваться по имени ключа, этот член всегда должен иметь значение **TZDEFINITION_FLAG_VALID_KEYNAME**.</span><span class="sxs-lookup"><span data-stu-id="660d2-109">Because each time zone should always be identified by a key name, this member should always have the value **TZDEFINITION_FLAG_VALID_KEYNAME**.</span></span>
    
<span data-ttu-id="660d2-110">_pwszKeyName_</span><span class="sxs-lookup"><span data-stu-id="660d2-110">_pwszKeyName_</span></span>
  
> <span data-ttu-id="660d2-111">Имя ключа для данного часового пояса в реестре Windows.</span><span class="sxs-lookup"><span data-stu-id="660d2-111">The name of the key for this time zone in the Windows registry.</span></span> <span data-ttu-id="660d2-112">Это имя не должны быть переведены.</span><span class="sxs-lookup"><span data-stu-id="660d2-112">This name must not be localized.</span></span> <span data-ttu-id="660d2-113">Она имеет максимальный размер **MAX_PATH**, которое определяется в файле windows.h заголовка Windows Software Development Kit (SDK).</span><span class="sxs-lookup"><span data-stu-id="660d2-113">It has a maximum size of **MAX_PATH**, which is defined in the Windows Software Development Kit (SDK) header file windows.h.</span></span> 
    
<span data-ttu-id="660d2-114">_cRules_</span><span class="sxs-lookup"><span data-stu-id="660d2-114">_cRules_</span></span>
  
> <span data-ttu-id="660d2-115">Число правил часовой пояс для этого определения.</span><span class="sxs-lookup"><span data-stu-id="660d2-115">The number of time zone rules for this definition.</span></span> <span data-ttu-id="660d2-116">Максимальное число правил — **TZ_MAX_RULES**.</span><span class="sxs-lookup"><span data-stu-id="660d2-116">The maximum number of rules is **TZ_MAX_RULES**.</span></span> 
    
<span data-ttu-id="660d2-117">_rgRules_</span><span class="sxs-lookup"><span data-stu-id="660d2-117">_rgRules_</span></span>
  
> <span data-ttu-id="660d2-118">Массив правил, определяющих при возникновении смены.</span><span class="sxs-lookup"><span data-stu-id="660d2-118">An array of rules that describe when shifts occur.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="660d2-119">Замечания</span><span class="sxs-lookup"><span data-stu-id="660d2-119">Remarks</span></span>

<span data-ttu-id="660d2-120">*RgRules* должен быть по крайней мере одно правило.</span><span class="sxs-lookup"><span data-stu-id="660d2-120">There must be at least one rule in  *rgRules*  .</span></span> <span data-ttu-id="660d2-121">Первое правило в *rgRules* считаются правила для использования до начала второе правило, вне зависимости от *stStart* на первое правило.</span><span class="sxs-lookup"><span data-stu-id="660d2-121">The first rule in  *rgRules*  is considered to be the rule to use until the second rule starts, regardless of the  *stStart*  on the first rule.</span></span> 
  
<span data-ttu-id="660d2-122">Правила будут сортироваться от более ранних к более поздним.</span><span class="sxs-lookup"><span data-stu-id="660d2-122">The rules should be sorted from oldest to newest.</span></span> <span data-ttu-id="660d2-123">Нет без перекрытия между правилами, поэтому предыдущего правила считается окончания при запуске новое правило.</span><span class="sxs-lookup"><span data-stu-id="660d2-123">There is no overlap allowed between rules, so a prior rule is deemed to end when a new rule starts.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="660d2-124">См. также</span><span class="sxs-lookup"><span data-stu-id="660d2-124">See also</span></span>

- [<span data-ttu-id="660d2-125">Constants (Outlook exported APIs)</span><span class="sxs-lookup"><span data-stu-id="660d2-125">Constants (Outlook exported APIs)</span></span>](constants-outlook-exported-apis.md)
- [<span data-ttu-id="660d2-126">About rebasing calendars programmatically for Daylight Saving Time</span><span class="sxs-lookup"><span data-stu-id="660d2-126">About rebasing calendars programmatically for Daylight Saving Time</span></span>](about-rebasing-calendars-programmatically-for-daylight-saving-time.md)  
- [<span data-ttu-id="660d2-127">HrCreateApptRebaser</span><span class="sxs-lookup"><span data-stu-id="660d2-127">HrCreateApptRebaser</span></span>](hrcreateapptrebaser.md)

