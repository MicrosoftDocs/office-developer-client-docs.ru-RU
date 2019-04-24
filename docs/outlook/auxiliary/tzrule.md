---
title: TZRULE
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 75ed353c-7d3e-e148-4057-715e82a0f32c
description: Задает сведения о том, когда начинается летнее время, а также год вступления в силу правила с часовым поясом.
ms.openlocfilehash: 71ede7c0061a058c2dd85c7b9b36c42583a6bb84
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328618"
---
# <a name="tzrule"></a>TZRULE

Задает сведения о том, когда начинается летнее время, а также год вступления в силу правила с часовым поясом. 
  
## <a name="quick-info"></a>Краткие сведения

```cpp
typedef struct { 
    WORD        wFlags;  
    SYSTEMTIME  stStart; 
    TZREG       TZReg; 
} TZRULE;
```

## <a name="members"></a>Элементы

_Вфлагс_
  
> Флаги, заданные для этого элемента, определяют конкретные сведения для этого правила часового пояса. Ниже приведены возможные флаги.
    
   - **Тзруле_флаг_еффективе_тзрег** — определяет правило, которое должно использоваться в данный момент. Только одно правило может быть помечено как действующее правило. Все остальные правила предназначены только для сравнения. 
    
   - **Тзруле_флаг_рекур_куррент_тзрег** — для повторяющихся собраний — определяет правило, совпадающее с правилом в [PidLidTimeZoneStruct](https://msdn.microsoft.com/library/2acf0036-2f3e-4f90-8614-7aa667860f74%28Office.15%29.aspx). Это можно использовать для обнаружения того, был ли **PidLidTimeZoneStruct** изменен устаревшим клиентом, что в противном случае не будет знать о новом свойстве Complete. 
    
_Стстарт_
  
> Время, в течение которого было запущено правило часового пояса, в формате UTC.
    
_TZReg_
  
> Сведения о часовом поясе для правила часового пояса.
    
## <a name="remarks"></a>Комментарии

Эта структура дополняет [TZREG](tzreg.md) , предоставляя дополнительные сведения о том, когда правила часовых поясов вступают в силу. 
  
## <a name="see-also"></a>См. также

- [About rebasing calendars programmatically for Daylight Saving Time](about-rebasing-calendars-programmatically-for-daylight-saving-time.md) 
- [Constants (Outlook exported APIs)](constants-outlook-exported-apis.md)
- [HrCreateApptRebaser](hrcreateapptrebaser.md)
- [TZDEFINITION](tzdefinition.md)

