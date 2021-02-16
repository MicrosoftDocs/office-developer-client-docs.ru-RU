---
title: TZDEFINITION
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 0ae21571-2299-6407-807c-428668bb6798
description: Представляет весь часовой пояс, включая все исторические, текущие и будущие правила смены часового пояса для перехода на летнее время.
ms.openlocfilehash: 5f7000ecc1fa602b330670c2ee1c39f673a11a65
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33429343"
---
# <a name="tzdefinition"></a>TZDEFINITION

Представляет весь часовой пояс, включая все исторические, текущие и будущие правила смены часового пояса для перехода на летнее время.
  
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
  
> Указывает, что имя ключа, которое представляет часовой пояс в реестре Windows, является допустимым. Так как каждый часовой пояс всегда должен быть определен по имени ключа, этот элемент всегда должен иметь **значение** TZDEFINITION_FLAG_VALID_KEYNAME.
    
_pwszKeyName_
  
> Имя ключа для этого часового пояса в реестре Windows. Это имя не должно быть локализовано. Он имеет максимальный размер **MAX_PATH,** который определяется в файле загона windows.h комплекта средств разработки программного обеспечения для Windows (SDK). 
    
_cRules_
  
> Количество правил часового пояса для этого определения. Максимальное количество правил — **TZ_MAX_RULES.** 
    
_rgRules_
  
> Массив правил, которые описывают, когда происходят смены.
    
## <a name="remarks"></a>Примечания

В  *rgRules*  должно быть хотя бы одно правило. Первое правило  *в rgRules*  считается правилом, который будет применяться до начала второго правила, независимо от  *stStart*  для первого правила. 
  
Правила должны сортироваться от самых старых к новым. Между правилами не допускается накладывать друг на друга, поэтому считается, что предыдущее правило заканчивается, когда начинается новое правило.
  
## <a name="see-also"></a>См. также

- [Constants (Outlook exported APIs)](constants-outlook-exported-apis.md)
- [Сведения о программном переводе календарей на летнее время](about-rebasing-calendars-programmatically-for-daylight-saving-time.md)  
- [HrCreateApptRebaser](hrcreateapptrebaser.md)

