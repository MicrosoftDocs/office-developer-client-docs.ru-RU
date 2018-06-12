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
# <a name="tzrule"></a>TZRULE

Задает сведения о при запуске летнее время и года, в котором это правило часового пояса сначала вступает в силу для часового пояса. 
  
## <a name="quick-info"></a>Краткие сведения

```cpp
typedef struct { 
    WORD        wFlags;  
    SYSTEMTIME  stStart; 
    TZREG       TZReg; 
} TZRULE;
```

## <a name="members"></a>Элементы

_wFlags_
  
> Флаги для этого элемента укажите подробные сведения для этого правила часового пояса. Флаги, как показано ниже:
    
   - **TZRULE_FLAG_EFFECTIVE_TZREG** — определяет правило, что следует использовать в настоящее время. Только одно правило может быть помечен как действующие правила. Все другие правила используются только в целях сравнения. 
    
   - **TZRULE_FLAG_RECUR_CURRENT_TZREG** — повторяющихся собраний определяет правило, как правило, в [PidLidTimeZoneStruct](http://msdn.microsoft.com/library/2acf0036-2f3e-4f90-8614-7aa667860f74%28Office.15%29.aspx)сопоставления. Это можно использовать для определения, были ли изменены **PidLidTimeZoneStruct** значительно при использовании устаревшего клиента, что было бы в противном случае — новый, более полную свойства. 
    
_stStart_
  
> Время в формате UTC (UTC) начала часового пояса.
    
_TZReg_
  
> Сведения о часового пояса для часового пояса.
    
## <a name="remarks"></a>Замечания

Эта структура дополняет [TZREG](tzreg.md) содержат дополнительные сведения, указывающий, когда правила часового пояса вступили в силу. 
  
## <a name="see-also"></a>См. также

- [About rebasing calendars programmatically for Daylight Saving Time](about-rebasing-calendars-programmatically-for-daylight-saving-time.md) 
- [Constants (Outlook exported APIs)](constants-outlook-exported-apis.md)
- [HrCreateApptRebaser](hrcreateapptrebaser.md)
- [TZDEFINITION](tzdefinition.md)

