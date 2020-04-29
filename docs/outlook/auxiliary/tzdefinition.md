---
title: TZDEFINITION
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 0ae21571-2299-6407-807c-428668bb6798
description: Представляет весь часовой пояс, включая все правила сдвига в прошлом, текущих и будущих часовых поясов для летнего времени.
ms.openlocfilehash: 5f7000ecc1fa602b330670c2ee1c39f673a11a65
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33429343"
---
# <a name="tzdefinition"></a>TZDEFINITION

Представляет весь часовой пояс, включая все правила сдвига в прошлом, текущих и будущих часовых поясов для летнего времени.
  
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

_вфлагс_
  
> Указывает, что имя ключа, представляющее часовой пояс в реестре Windows, является допустимым. Так как каждый часовой пояс должен всегда быть идентифицирован с помощью имени ключа, этому элементу всегда должно быть присвоено значение **TZDEFINITION_FLAG_VALID_KEYNAME**.
    
_пвсзкэйнаме_
  
> Имя ключа для этого часового пояса в реестре Windows. Это имя не должно быть локализовано. Он имеет максимальный размер **MAX_PATH**, который определен в файле заголовка пакета средств разработки программного обеспечения (SDK) Windows. h. 
    
_крулес_
  
> Количество правил для часовых поясов для этого определения. **TZ_MAX_RULES**максимальное число правил. 
    
_ргрулес_
  
> Массив правил, описывающих, когда происходят сдвиги.
    
## <a name="remarks"></a>Примечания

В *ргрулес* должно быть по крайней мере одно правило. Первое правило в *ргрулес* считается используемым правилом, пока не будет запущено второе правило, независимо от того, какой *стстарт* в первом правиле. 
  
Правила следует отсортировать от старых к новым. Между правилами не существует перекрытия, поэтому при запуске нового правила предыдущее правило считается завершенным.
  
## <a name="see-also"></a>См. также

- [Constants (Outlook exported APIs)](constants-outlook-exported-apis.md)
- [Сведения о программном переводе календарей на летнее время](about-rebasing-calendars-programmatically-for-daylight-saving-time.md)  
- [HrCreateApptRebaser](hrcreateapptrebaser.md)

