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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32307842"
---
# <a name="tzreg"></a>TZREG

Определяет, когда происходит переход на летнее время, когда происходит возврат к стандартному времени и сколько часов сдвига на летнее время.
  
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

_Лбиас_
  
> Смещение относительно среднего времени по Гринвичу (GMT).
    
_Лстандардбиас_
  
> Смещение от смещения в зимнее время.
    
_Лдайлигхтбиас_
  
> Смещение от смещения во время летнего времени.
    
_Стстандарддате_
  
> Время переключения на стандартное время.
    
_Стдайлигхтдате_
  
> Время переключения на летнее время.
    
## <a name="remarks"></a>Замечания

Эта структура аналогична **тиме_зоне_информатион**. Это структура, используемая устаревшими клиентами для хранения сведений о часовых поясах для повторяющихся собраний.
  
## <a name="see-also"></a>См. также

- [About rebasing calendars programmatically for Daylight Saving Time](about-rebasing-calendars-programmatically-for-daylight-saving-time.md)  
- [HrCreateApptRebaser](hrcreateapptrebaser.md)  
- [TZRULE](tzrule.md)

