---
title: TZRULE
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 75ed353c-7d3e-e148-4057-715e82a0f32c
description: Указывает сведения для правила часового пояса о том, когда начинается летнее время и в какой год это правило вступает в силу.
ms.openlocfilehash: 71ede7c0061a058c2dd85c7b9b36c42583a6bb84
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328618"
---
# <a name="tzrule"></a>TZRULE

Указывает сведения для правила часового пояса о том, когда начинается летнее время и в какой год это правило вступает в силу. 
  
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
  
> Флаги, установленные для этого члена, определяют конкретные сведения для этого правила часовой пояс. Возможные флаги:
    
   - **TZRULE_FLAG_EFFECTIVE_TZREG** — определяет правило как правило, которое должно использоваться в настоящее время. В качестве эффективного правила можно пометить только одно правило. Все остальные правила только для сравнения. 
    
   - **TZRULE_FLAG_RECUR_CURRENT_TZREG** — в повторяющихся собраниях определяет правило как совпадает с правилом в [PidLidTimeZoneStruct.](https://msdn.microsoft.com/library/2acf0036-2f3e-4f90-8614-7aa667860f74%28Office.15%29.aspx) Это можно использовать для определения того, был ли **pidLidTimeZoneStruct** значительно изменен устаревшим клиентом, который в противном случае не знает о новом, более полном свойстве. 
    
_stStart_
  
> Время начала работы правила часовой пояса в UTC.
    
_TZReg_
  
> Сведения о часовом поясе для правила часовой пояс.
    
## <a name="remarks"></a>Примечания

Эта структура дополняет [TZREG](tzreg.md) за счет предоставления дополнительных сведений, указывающих, когда правила часовых поясов вступает в силу. 
  
## <a name="see-also"></a>См. также

- [Сведения о программном переводе календарей на летнее время](about-rebasing-calendars-programmatically-for-daylight-saving-time.md) 
- [Constants (Outlook exported APIs)](constants-outlook-exported-apis.md)
- [HrCreateApptRebaser](hrcreateapptrebaser.md)
- [TZDEFINITION](tzdefinition.md)

