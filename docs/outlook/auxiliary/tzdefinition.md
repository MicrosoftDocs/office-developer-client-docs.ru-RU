---
title: TZDEFINITION
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 0ae21571-2299-6407-807c-428668bb6798
description: Представляет весь часовой пояс, включая все исторические, текущие и будущие правила смены часового пояса для летнего времени.
ms.openlocfilehash: 5f7000ecc1fa602b330670c2ee1c39f673a11a65
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33429343"
---
# <a name="tzdefinition"></a><span data-ttu-id="36e83-103">TZDEFINITION</span><span class="sxs-lookup"><span data-stu-id="36e83-103">TZDEFINITION</span></span>

<span data-ttu-id="36e83-104">Представляет весь часовой пояс, включая все исторические, текущие и будущие правила смены часового пояса для летнего времени.</span><span class="sxs-lookup"><span data-stu-id="36e83-104">Represents an entire time zone including all historical, current, and future time zone shift rules for daylight saving time.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="36e83-105">Краткие сведения</span><span class="sxs-lookup"><span data-stu-id="36e83-105">Quick info</span></span>

```cpp
typedef struct { 
    WORD     wFlags;  
    LPWSTR   pwszKeyName; 
    WORD     cRules; 
    TZRULE*  rgRules; 
} TZDEFINITION;
```

## <a name="members"></a><span data-ttu-id="36e83-106">Элементы</span><span class="sxs-lookup"><span data-stu-id="36e83-106">Members</span></span>

<span data-ttu-id="36e83-107">_wFlags_</span><span class="sxs-lookup"><span data-stu-id="36e83-107">_wFlags_</span></span>
  
> <span data-ttu-id="36e83-108">Указывает, что ключевое имя, которое представляет часовой пояс в Windows реестра, является допустимым.</span><span class="sxs-lookup"><span data-stu-id="36e83-108">Indicates that the key name that represents the time zone in the Windows registry is valid.</span></span> <span data-ttu-id="36e83-109">Так как каждый часовой пояс всегда должен быть определен ключевым именем, этот член должен всегда иметь **значение TZDEFINITION_FLAG_VALID_KEYNAME**.</span><span class="sxs-lookup"><span data-stu-id="36e83-109">Because each time zone should always be identified by a key name, this member should always have the value **TZDEFINITION_FLAG_VALID_KEYNAME**.</span></span>
    
<span data-ttu-id="36e83-110">_pwszKeyName_</span><span class="sxs-lookup"><span data-stu-id="36e83-110">_pwszKeyName_</span></span>
  
> <span data-ttu-id="36e83-111">Имя ключа для этого часового пояса в Windows реестре.</span><span class="sxs-lookup"><span data-stu-id="36e83-111">The name of the key for this time zone in the Windows registry.</span></span> <span data-ttu-id="36e83-112">Это имя не должно быть локализовано.</span><span class="sxs-lookup"><span data-stu-id="36e83-112">This name must not be localized.</span></span> <span data-ttu-id="36e83-113">Он имеет максимальный размер **MAX_PATH,** который определяется в файле windows.h Windows программного обеспечения (SDK).</span><span class="sxs-lookup"><span data-stu-id="36e83-113">It has a maximum size of **MAX_PATH**, which is defined in the Windows Software Development Kit (SDK) header file windows.h.</span></span> 
    
<span data-ttu-id="36e83-114">_cRules_</span><span class="sxs-lookup"><span data-stu-id="36e83-114">_cRules_</span></span>
  
> <span data-ttu-id="36e83-115">Количество правил часового пояса для этого определения.</span><span class="sxs-lookup"><span data-stu-id="36e83-115">The number of time zone rules for this definition.</span></span> <span data-ttu-id="36e83-116">Максимальное количество правил **TZ_MAX_RULES**.</span><span class="sxs-lookup"><span data-stu-id="36e83-116">The maximum number of rules is **TZ_MAX_RULES**.</span></span> 
    
<span data-ttu-id="36e83-117">_rgRules_</span><span class="sxs-lookup"><span data-stu-id="36e83-117">_rgRules_</span></span>
  
> <span data-ttu-id="36e83-118">Массив правил, описывая, когда происходят сдвиги.</span><span class="sxs-lookup"><span data-stu-id="36e83-118">An array of rules that describe when shifts occur.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="36e83-119">Примечания</span><span class="sxs-lookup"><span data-stu-id="36e83-119">Remarks</span></span>

<span data-ttu-id="36e83-120">В  *rgRules*  должно быть по крайней мере одно правило.</span><span class="sxs-lookup"><span data-stu-id="36e83-120">There must be at least one rule in  *rgRules*  .</span></span> <span data-ttu-id="36e83-121">Первое правило  *в rgRules*  считается правилом, используемого до начала второго правила, независимо от  *stStart*  на первом правиле.</span><span class="sxs-lookup"><span data-stu-id="36e83-121">The first rule in  *rgRules*  is considered to be the rule to use until the second rule starts, regardless of the  *stStart*  on the first rule.</span></span> 
  
<span data-ttu-id="36e83-122">Правила следует сортировать от самых старых к новым.</span><span class="sxs-lookup"><span data-stu-id="36e83-122">The rules should be sorted from oldest to newest.</span></span> <span data-ttu-id="36e83-123">Между правилами не допускается совпадение, поэтому предварительное правило считается конечным при начале нового правила.</span><span class="sxs-lookup"><span data-stu-id="36e83-123">There is no overlap allowed between rules, so a prior rule is deemed to end when a new rule starts.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="36e83-124">См. также</span><span class="sxs-lookup"><span data-stu-id="36e83-124">See also</span></span>

- [<span data-ttu-id="36e83-125">Constants (Outlook exported APIs)</span><span class="sxs-lookup"><span data-stu-id="36e83-125">Constants (Outlook exported APIs)</span></span>](constants-outlook-exported-apis.md)
- [<span data-ttu-id="36e83-126">Сведения о программном переводе календарей на летнее время</span><span class="sxs-lookup"><span data-stu-id="36e83-126">About rebasing calendars programmatically for Daylight Saving Time</span></span>](about-rebasing-calendars-programmatically-for-daylight-saving-time.md)  
- [<span data-ttu-id="36e83-127">HrCreateApptRebaser</span><span class="sxs-lookup"><span data-stu-id="36e83-127">HrCreateApptRebaser</span></span>](hrcreateapptrebaser.md)

