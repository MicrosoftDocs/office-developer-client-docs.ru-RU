---
title: TZDEFINITION
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 0ae21571-2299-6407-807c-428668bb6798
description: Представляет всей часового пояса, включая все правила shift журналу, текущие и будущие часового пояса на летнее время.
ms.openlocfilehash: f436216f5da882ea8ac144e6bd384e51e31abb8e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19807981"
---
# <a name="tzdefinition"></a>TZDEFINITION

Представляет всей часового пояса, включая все правила shift журналу, текущие и будущие часового пояса на летнее время.
  
## <a name="quick-info"></a>Краткие сведения

```cpp
typedef struct { 
    WORD     wFlags;  
    LPWSTR   pwszKeyName; 
    WORD     cRules; 
    TZRULE*  rgRules; 
} TZDEFINITION;
```

## <a name="members"></a>Элементы

_wFlags_
  
> Указывает допустимое имя раздела, который представляет часового пояса в реестре Windows. Поскольку каждый часовой пояс всегда должны идентифицироваться по имени ключа, этот член всегда должен иметь значение **TZDEFINITION_FLAG_VALID_KEYNAME**.
    
_pwszKeyName_
  
> Имя ключа для данного часового пояса в реестре Windows. Это имя не должны быть переведены. Она имеет максимальный размер **MAX_PATH**, которое определяется в файле windows.h заголовка Windows Software Development Kit (SDK). 
    
_cRules_
  
> Число правил часовой пояс для этого определения. Максимальное число правил — **TZ_MAX_RULES**. 
    
_rgRules_
  
> Массив правил, определяющих при возникновении смены.
    
## <a name="remarks"></a>Замечания

*RgRules* должен быть по крайней мере одно правило. Первое правило в *rgRules* считаются правила для использования до начала второе правило, вне зависимости от *stStart* на первое правило. 
  
Правила будут сортироваться от более ранних к более поздним. Нет без перекрытия между правилами, поэтому предыдущего правила считается окончания при запуске новое правило.
  
## <a name="see-also"></a>См. также

- [Constants (Outlook exported APIs)](constants-outlook-exported-apis.md)
- [About rebasing calendars programmatically for Daylight Saving Time](about-rebasing-calendars-programmatically-for-daylight-saving-time.md)  
- [HrCreateApptRebaser](hrcreateapptrebaser.md)

