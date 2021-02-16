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
# <a name="tzreg"></a>TZREG

Определяет время начала перехода на летнее время, время возврата к стандартному времени и время перехода на летнее время.
  
## <a name="quick-info"></a>Краткие сведения

```cpp
typedef struct RenTimeZone { 
    long        lBias;  
    long        lStandardBias; 
    long        lDaylightBias; 
    SYSTEMTIME  stStandardDate; 
    SYSTEMTIME  stDaylightDate; 
} TZREG; 

```

## <a name="members"></a>Элементы

_lBias_
  
> Смещение по гринвичскому времени (GMT).
    
_lStandardBias_
  
> Смещение смещения в стандартное время.
    
_lDaylightBias_
  
> Смещение смещения в летнее время.
    
_stStandardDate_
  
> Время перехода на стандартное время.
    
_stDaylightDate_
  
> Время перехода на летнее время.
    
## <a name="remarks"></a>Примечания

Эта структура аналогична **TIME_ZONE_INFORMATION.** Это структура, используемая устаревшими клиентами для хранения сведений о часовом поясе для повторяющихся собраний.
  
## <a name="see-also"></a>См. также

- [Сведения о программном переводе календарей на летнее время](about-rebasing-calendars-programmatically-for-daylight-saving-time.md)  
- [HrCreateApptRebaser](hrcreateapptrebaser.md)  
- [TZRULE](tzrule.md)

