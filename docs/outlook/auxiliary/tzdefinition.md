---
title: TZDEFINITION
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 0ae21571-2299-6407-807c-428668bb6798
description: Представляет весь часовой пояс, включая все правила сдвига в прошлом, текущих и будущих часовых поясов для летнего времени.
ms.openlocfilehash: 5f7000ecc1fa602b330670c2ee1c39f673a11a65
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33429343"
---
# <a name="tzdefinition"></a><span data-ttu-id="a9e6f-103">TZDEFINITION</span><span class="sxs-lookup"><span data-stu-id="a9e6f-103">TZDEFINITION</span></span>

<span data-ttu-id="a9e6f-104">Представляет весь часовой пояс, включая все правила сдвига в прошлом, текущих и будущих часовых поясов для летнего времени.</span><span class="sxs-lookup"><span data-stu-id="a9e6f-104">Represents an entire time zone including all historical, current, and future time zone shift rules for daylight saving time.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="a9e6f-105">Краткие сведения</span><span class="sxs-lookup"><span data-stu-id="a9e6f-105">Quick info</span></span>

```cpp
typedef struct { 
    WORD     wFlags;  
    LPWSTR   pwszKeyName; 
    WORD     cRules; 
    TZRULE*  rgRules; 
} TZDEFINITION;
```

## <a name="members"></a><span data-ttu-id="a9e6f-106">Элементы</span><span class="sxs-lookup"><span data-stu-id="a9e6f-106">Members</span></span>

<span data-ttu-id="a9e6f-107">_Вфлагс_</span><span class="sxs-lookup"><span data-stu-id="a9e6f-107">_wFlags_</span></span>
  
> <span data-ttu-id="a9e6f-108">Указывает, что имя ключа, представляющее часовой пояс в реестре Windows, является допустимым.</span><span class="sxs-lookup"><span data-stu-id="a9e6f-108">Indicates that the key name that represents the time zone in the Windows registry is valid.</span></span> <span data-ttu-id="a9e6f-109">Так как каждый часовой пояс должен всегда определяться именем ключа, этот член всегда должен иметь значение **тздефинитион_флаг_валид_кэйнаме**.</span><span class="sxs-lookup"><span data-stu-id="a9e6f-109">Because each time zone should always be identified by a key name, this member should always have the value **TZDEFINITION_FLAG_VALID_KEYNAME**.</span></span>
    
<span data-ttu-id="a9e6f-110">_Пвсзкэйнаме_</span><span class="sxs-lookup"><span data-stu-id="a9e6f-110">_pwszKeyName_</span></span>
  
> <span data-ttu-id="a9e6f-111">Имя ключа для этого часового пояса в реестре Windows.</span><span class="sxs-lookup"><span data-stu-id="a9e6f-111">The name of the key for this time zone in the Windows registry.</span></span> <span data-ttu-id="a9e6f-112">Это имя не должно быть локализовано.</span><span class="sxs-lookup"><span data-stu-id="a9e6f-112">This name must not be localized.</span></span> <span data-ttu-id="a9e6f-113">Максимальный размер составляет значение **MAX_PATH**, которое определено в файле заголовка пакета средств разработки программного обеспечения (SDK) для Windows. h.</span><span class="sxs-lookup"><span data-stu-id="a9e6f-113">It has a maximum size of **MAX_PATH**, which is defined in the Windows Software Development Kit (SDK) header file windows.h.</span></span> 
    
<span data-ttu-id="a9e6f-114">_Крулес_</span><span class="sxs-lookup"><span data-stu-id="a9e6f-114">_cRules_</span></span>
  
> <span data-ttu-id="a9e6f-115">Количество правил для часовых поясов для этого определения.</span><span class="sxs-lookup"><span data-stu-id="a9e6f-115">The number of time zone rules for this definition.</span></span> <span data-ttu-id="a9e6f-116">Максимальное число правил — **тз_макс_рулес**.</span><span class="sxs-lookup"><span data-stu-id="a9e6f-116">The maximum number of rules is **TZ_MAX_RULES**.</span></span> 
    
<span data-ttu-id="a9e6f-117">_Ргрулес_</span><span class="sxs-lookup"><span data-stu-id="a9e6f-117">_rgRules_</span></span>
  
> <span data-ttu-id="a9e6f-118">Массив правил, описывающих, когда происходят сдвиги.</span><span class="sxs-lookup"><span data-stu-id="a9e6f-118">An array of rules that describe when shifts occur.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="a9e6f-119">Примечания</span><span class="sxs-lookup"><span data-stu-id="a9e6f-119">Remarks</span></span>

<span data-ttu-id="a9e6f-120">В *ргрулес* должно быть по крайней мере одно правило.</span><span class="sxs-lookup"><span data-stu-id="a9e6f-120">There must be at least one rule in  *rgRules*  .</span></span> <span data-ttu-id="a9e6f-121">Первое правило в *ргрулес* считается используемым правилом, пока не будет запущено второе правило, независимо от того, какой *стстарт* в первом правиле.</span><span class="sxs-lookup"><span data-stu-id="a9e6f-121">The first rule in  *rgRules*  is considered to be the rule to use until the second rule starts, regardless of the  *stStart*  on the first rule.</span></span> 
  
<span data-ttu-id="a9e6f-122">Правила следует отсортировать от старых к новым.</span><span class="sxs-lookup"><span data-stu-id="a9e6f-122">The rules should be sorted from oldest to newest.</span></span> <span data-ttu-id="a9e6f-123">Между правилами не существует перекрытия, поэтому при запуске нового правила предыдущее правило считается завершенным.</span><span class="sxs-lookup"><span data-stu-id="a9e6f-123">There is no overlap allowed between rules, so a prior rule is deemed to end when a new rule starts.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="a9e6f-124">См. также</span><span class="sxs-lookup"><span data-stu-id="a9e6f-124">See also</span></span>

- [<span data-ttu-id="a9e6f-125">Constants (Outlook exported APIs)</span><span class="sxs-lookup"><span data-stu-id="a9e6f-125">Constants (Outlook exported APIs)</span></span>](constants-outlook-exported-apis.md)
- [<span data-ttu-id="a9e6f-126">About rebasing calendars programmatically for Daylight Saving Time</span><span class="sxs-lookup"><span data-stu-id="a9e6f-126">About rebasing calendars programmatically for Daylight Saving Time</span></span>](about-rebasing-calendars-programmatically-for-daylight-saving-time.md)  
- [<span data-ttu-id="a9e6f-127">HrCreateApptRebaser</span><span class="sxs-lookup"><span data-stu-id="a9e6f-127">HrCreateApptRebaser</span></span>](hrcreateapptrebaser.md)

