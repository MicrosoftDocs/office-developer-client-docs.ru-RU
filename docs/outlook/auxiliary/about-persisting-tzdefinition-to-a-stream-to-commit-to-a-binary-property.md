---
title: Сведения о сохранении TZDEFINITION в потоке для помещения в двоичное свойство
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 0dec535d-d48f-39a5-97d5-0bd109134b3b
description: Свойства часового пояса, PidLidAppointmentTimeZoneDefinitionEndDisplay, PidLidAppointmentTimeZoneDefinitionRecur и PidLidAppointmentTimeZoneDefinitionStartDisplay являются двоичными именованными свойствами, каждый из которых содержит поток, сопоставляемый с постоянном форматом структуры TZDEFINITION.
ms.openlocfilehash: f94b751a55aa852c962eebe5d46968e9e622e315
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316978"
---
# <a name="about-persisting-tzdefinition-to-a-stream-to-commit-to-a-binary-property"></a>Сведения о сохранении TZDEFINITION в потоке для помещения в двоичное свойство

Свойства часового пояса, [PidLidAppointmentTimeZoneDefinitionEndDisplay](https://msdn.microsoft.com/library/7b6193cb-612b-408e-b9bc-285df313e2cc%28Office.15%29.aspx), [PidLidAppointmentTimeZoneDefinitionRecur](https://msdn.microsoft.com/library/52fd57a0-9e34-4452-9ecd-2acb454446c9%28Office.15%29.aspx)и [PidLidAppointmentTimeZoneDefinitionStartDisplay](https://msdn.microsoft.com/library/08239670-3211-420c-99d7-0056ed967cb8%28Office.15%29.aspx) являются двоичными именованными свойствами, каждый из которых содержит поток, сопоставляемый с постоянном форматом структуры [TZDEFINITION](tzdefinition.md) . 
  
В этом разделе описывается прямой формат с обратным порядком байтов, который можно использовать при сохранении **TZDEFINITION** в потоке для фиксации в одном из трех двоичных свойств. Используйте один и тот же формат endian в средстве синтаксического анализа для интерпретации значения потока, полученного из одного из этих свойств. 
  
```cpp
BYTE  bMajorVersion;    // breaking change
BYTE  bMinorVersion;    // extensibility
WORD  cbHeader;         // size of following data until TZREG sub structure
WORD  wFlags;
if (TZDEFINITION_FLAG_VALID_GUID)
   GUID  guid;                // guid
if (TZDEFINITION_FLAG_VALID_KEYNAME)     
    WORD   cchKeyName;        // does not include null char
    WCHAR  rgchKeyName;       // not null terminated
    WORD  cRules;             // number of rules
// for each rule
   BYTE        bMajorVersion;         // breaking change
   BYTE        bMinorVersion;         // extensibility
   WORD        cbRule;                // size of following data
   WORD        wFlags;                // flags
   SYSTEMTIME  stStart;               // GMT when this rule starts
// Following are the fields of the TZREG sub structure
   long        lBias;                // offset from GMT
   long        lStandardBias;        // offset from bias during standard time
   long        lDaylightBias;        // offset from bias during daylight time
   SYSTEMTIME  stStandardDate;       // time to switch to standard time
   SYSTEMTIME  stDaylightDate;       // time to switch to daylight time
```

Основной номер версии используется для внесения критических изменений. Клиенты, не знакомые с номером основной версии, должны считать это свойство, как если бы оно не было указано. Клиенты, пишущие структуру, должны указать константу **TZ_BIN_VERSION_MAJOR**. 
  
Дополнительный номер версии используется для расширения. Клиенты, не знакомые с номером дополнительной версии, должны считать данные, которые они понимают, и пропустить данные, которые могут быть добавлены к каждому правилу или к общему потоку. Клиенты, пишущие структуру, должны указать константу **TZ_BIN_VERSION_MINOR**. 
  
Если средство синтаксического анализа не понимает основную версию заголовка, оно не должно считывать оставшуюся часть структуры и вести себя так, как если бы данные отсутствовали. Если дополнительный номер версии заголовка не распознается синтаксическим анализатором, он должен использовать **кбхеадер** для игнорирования частей, которые он не понимает, и для чтения частей потока, который он понимает. 
  
Значение **вфлагс** всегда **TZDEFINITION_FLAG_VALID_KEYNAME**. Имя ключа имеет максимальный размер **MAX_PATH**. 
  
Если средство синтаксического анализа не распознает основную версию правила, клиент должен игнорировать это правило и использовать **кбруле** для перехода к следующему правилу. Если дополнительный номер версии правила не распознается средством синтаксического анализа, клиент должен проанализировать только те части правила, которые он понимает. 
  
При сохранении структуры **TZDEFINITION** в потоке средство синтаксического анализа не должно пытаться записать какую бы то ни было непонятную информацию. 
  
Максимальное число правил — 1024.
  
Обратите внимание, что структура [TZREG](tzreg.md) хранится не так, как при сохранении, поэтому один и тот же код невозможно использовать для синтаксического анализа. 
  
## <a name="see-also"></a>См. также

- [Constants (Outlook exported APIs)](constants-outlook-exported-apis.md)
- [Анализ потока из двоичного свойства для считывания структуры TZDEFINITION](how-to-parse-stream-from-binary-property-to-read-tzdefinition-structure.md)
- [Считывание свойств часового пояса встречи](how-to-read-time-zone-properties-from-an-appointment.md)

