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
# <a name="tzreg"></a>TZREG

Определяет, когда начинается летнее время, когда происходит возврат к стандартному времени, и сколько часов составляет переход на летнее время.
  
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
  
> Смещение от гринвичского времени (GMT).
    
_lStandardBias_
  
> Смещение от смещения в стандартное время.
    
_lDaylightBias_
  
> Смещение от смещения во время летнего времени.
    
_stStandardDate_
  
> Время перехода на стандартное время.
    
_stDaylightDate_
  
> Время перехода на летнее время.
    
## <a name="remarks"></a>Примечания

Эта структура похожа на **TIME_ZONE_INFORMATION**. Это структура, используемая устаревшими клиентами для хранения данных часовых поясов для повторяющихся собраний.
  
## <a name="see-also"></a>См. также

- [Сведения о программном переводе календарей на летнее время](about-rebasing-calendars-programmatically-for-daylight-saving-time.md)  
- [HrCreateApptRebaser](hrcreateapptrebaser.md)  
- [TZRULE](tzrule.md)

