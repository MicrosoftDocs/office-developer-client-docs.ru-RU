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
# <a name="tzreg"></a>TZREG

Определяет при запуске летнего времени, когда происходит возврат стандартного времени и сколько часов — это летнего shift.
  
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

## <a name="members"></a>Members

_lBias_
  
> Смещение от среднего времени по Гринвичу (GMT).
    
_lStandardBias_
  
> Смещение от bias во время (зима).
    
_lDaylightBias_
  
> Смещение от bias во время перехода на летнее время.
    
_stStandardDate_
  
> Время, чтобы переключиться на стандартное время.
    
_stDaylightDate_
  
> Время для перехода на летнее время.
    
## <a name="remarks"></a>Замечания

Эта структура аналогична **TIME_ZONE_INFORMATION**. Это структуры, используемый в устаревших клиентов для хранения сведений о часовом поясе для повторяющихся собраний.
  
## <a name="see-also"></a>См. также

- [About rebasing calendars programmatically for Daylight Saving Time](about-rebasing-calendars-programmatically-for-daylight-saving-time.md)  
- [HrCreateApptRebaser](hrcreateapptrebaser.md)  
- [TZRULE](tzrule.md)

