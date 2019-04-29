---
title: TZREG
manager: soliver
ms.date: 12/07/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: a353e1a3-0187-20af-b9ba-43438f6024d5
description: Определяет, когда происходит переход на летнее время, когда происходит возврат к стандартному времени и сколько часов сдвига на летнее время.
ms.openlocfilehash: 136ff6ad0c1a9bc2ad61ef7ba698d66d645165d8
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33419368"
---
# <a name="tzreg"></a><span data-ttu-id="44bff-103">TZREG</span><span class="sxs-lookup"><span data-stu-id="44bff-103">TZREG</span></span>

<span data-ttu-id="44bff-104">Определяет, когда происходит переход на летнее время, когда происходит возврат к стандартному времени и сколько часов сдвига на летнее время.</span><span class="sxs-lookup"><span data-stu-id="44bff-104">Defines when daylight saving time starts, when the return to standard time occurs, and how many hours the daylight saving shift is.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="44bff-105">Краткие сведения</span><span class="sxs-lookup"><span data-stu-id="44bff-105">Quick info</span></span>

```cpp
typedef struct RenTimeZone { 
    long        lBias;  
    long        lStandardBias; 
    long        lDaylightBias; 
    SYSTEMTIME  stStandardDate; 
    SYSTEMTIME  stDaylightDate; 
} TZREG; 

```

## <a name="members"></a><span data-ttu-id="44bff-106">Элементы</span><span class="sxs-lookup"><span data-stu-id="44bff-106">Members</span></span>

<span data-ttu-id="44bff-107">_Лбиас_</span><span class="sxs-lookup"><span data-stu-id="44bff-107">_lBias_</span></span>
  
> <span data-ttu-id="44bff-108">Смещение относительно среднего времени по Гринвичу (GMT).</span><span class="sxs-lookup"><span data-stu-id="44bff-108">The offset from Greenwich Mean Time (GMT).</span></span>
    
<span data-ttu-id="44bff-109">_Лстандардбиас_</span><span class="sxs-lookup"><span data-stu-id="44bff-109">_lStandardBias_</span></span>
  
> <span data-ttu-id="44bff-110">Смещение от смещения в зимнее время.</span><span class="sxs-lookup"><span data-stu-id="44bff-110">The offset from bias during standard time.</span></span>
    
<span data-ttu-id="44bff-111">_Лдайлигхтбиас_</span><span class="sxs-lookup"><span data-stu-id="44bff-111">_lDaylightBias_</span></span>
  
> <span data-ttu-id="44bff-112">Смещение от смещения во время летнего времени.</span><span class="sxs-lookup"><span data-stu-id="44bff-112">The offset from bias during daylight saving time.</span></span>
    
<span data-ttu-id="44bff-113">_Стстандарддате_</span><span class="sxs-lookup"><span data-stu-id="44bff-113">_stStandardDate_</span></span>
  
> <span data-ttu-id="44bff-114">Время переключения на стандартное время.</span><span class="sxs-lookup"><span data-stu-id="44bff-114">The time to switch to standard time.</span></span>
    
<span data-ttu-id="44bff-115">_Стдайлигхтдате_</span><span class="sxs-lookup"><span data-stu-id="44bff-115">_stDaylightDate_</span></span>
  
> <span data-ttu-id="44bff-116">Время переключения на летнее время.</span><span class="sxs-lookup"><span data-stu-id="44bff-116">The time to switch to daylight saving time.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="44bff-117">Примечания</span><span class="sxs-lookup"><span data-stu-id="44bff-117">Remarks</span></span>

<span data-ttu-id="44bff-118">Эта структура аналогична **тиме_зоне_информатион**.</span><span class="sxs-lookup"><span data-stu-id="44bff-118">This structure is similar to **TIME_ZONE_INFORMATION**.</span></span> <span data-ttu-id="44bff-119">Это структура, используемая устаревшими клиентами для хранения сведений о часовых поясах для повторяющихся собраний.</span><span class="sxs-lookup"><span data-stu-id="44bff-119">This is the structure used by legacy clients to store time zone information for recurring meetings.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="44bff-120">См. также</span><span class="sxs-lookup"><span data-stu-id="44bff-120">See also</span></span>

- [<span data-ttu-id="44bff-121">About rebasing calendars programmatically for Daylight Saving Time</span><span class="sxs-lookup"><span data-stu-id="44bff-121">About rebasing calendars programmatically for Daylight Saving Time</span></span>](about-rebasing-calendars-programmatically-for-daylight-saving-time.md)  
- [<span data-ttu-id="44bff-122">HrCreateApptRebaser</span><span class="sxs-lookup"><span data-stu-id="44bff-122">HrCreateApptRebaser</span></span>](hrcreateapptrebaser.md)  
- [<span data-ttu-id="44bff-123">TZRULE</span><span class="sxs-lookup"><span data-stu-id="44bff-123">TZRULE</span></span>](tzrule.md)

