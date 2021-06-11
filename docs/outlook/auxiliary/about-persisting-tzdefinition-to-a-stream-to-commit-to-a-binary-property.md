---
title: Сведения о сохранении TZDEFINITION в потоке для помещения в двоичное свойство
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 0dec535d-d48f-39a5-97d5-0bd109134b3b
description: Свойства часового пояса PidLidAppointmentTimeZoneDefinitionEndDisplay, PidLidAppointmentTimeDefinitionRecur и PidLidAppointmentTimeZoneDefinitionStartDisplay являются двоичными свойствами, каждое из которых содержит поток, который содержит поток, который совмещает сохраняемого формата структуры TZDEFINITION.
ms.openlocfilehash: f94b751a55aa852c962eebe5d46968e9e622e315
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316978"
---
# <a name="about-persisting-tzdefinition-to-a-stream-to-commit-to-a-binary-property"></a>Сведения о сохранении TZDEFINITION в потоке для помещения в двоичное свойство

Свойства часового пояса [PidLidAppointmentTimeZoneDefinitionEndDisplay,](https://msdn.microsoft.com/library/7b6193cb-612b-408e-b9bc-285df313e2cc%28Office.15%29.aspx) [PidLidAppointmentTimeZoneDefinitionRecur](https://msdn.microsoft.com/library/52fd57a0-9e34-4452-9ecd-2acb454446c9%28Office.15%29.aspx)и [PidLidAppointmentTimeZoneDefinitionStartDisplay](https://msdn.microsoft.com/library/08239670-3211-420c-99d7-0056ed967cb8%28Office.15%29.aspx) являются двоичными свойствами, каждое из которых содержит поток, который содержит поток, который совмещает сохраняемого формата структуры [TZDEFINITION.](tzdefinition.md) 
  
В этом разделе описывается небольшой конечный формат, который можно использовать при упорядочии **TZDEFINITION** в потоке для фиксации одного из трех двоичных свойств. Используйте тот же конечный формат в области parser для интерпретации значения потока, полученного из одного из этих свойств. 
  
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

Основной номер версии используется для внося изменения. Клиенты, не знакомые с основным номером версии, должны относиться к свойству так, будто его нет. Клиенты, написав структуру, должны указать **TZ_BIN_VERSION_MAJOR.** 
  
Небольшой номер версии используется для раздвивемости. Клиенты, не знакомые с незначительным номером версии, должны прочитать данные, которые они понимают, и пропустить данные, которые могут быть примечены к каждому правилу или общему потоку. Клиенты, написав структуру, должны указать **TZ_BIN_VERSION_MINOR.** 
  
Если анализер не понимает главную версию загона, он не должен читать остальную структуру и вести себя так, как будто данные отсутствуют. Если разборщик не понимает незначительную версию заголовок, он должен использовать **cbHeader,** чтобы игнорировать те части, которые он не понимает, и продвигать чтение частей потока, который он понимает. 
  
Значение **wFlags** всегда **TZDEFINITION_FLAG_VALID_KEYNAME**. Имя ключа имеет максимальный размер **MAX_PATH**. 
  
Если размерщик не распознает главную версию правила, клиент должен игнорировать правило и использовать **cbRule** для продвижения к следующему правилу. Если разберегатель не распознает второстепенную версию правила, клиент должен только разберегать части правила, которые он понимает. 
  
При сохраняющихся **структурах TZDEFINITION** в потоке не следует пытаться записывать какие-либо сведения, которые он не понимает. 
  
Максимальное число правил — 1024.
  
Обратите внимание, что структура [TZREG](tzreg.md) сохраняется здесь по-другому, чем когда она сохраняется в одиночку, поэтому один и тот же код нельзя использовать для ее разметки. 
  
## <a name="see-also"></a>См. также

- [Constants (Outlook exported APIs)](constants-outlook-exported-apis.md)
- [Анализ потока из двоичного свойства для считывания структуры TZDEFINITION](how-to-parse-stream-from-binary-property-to-read-tzdefinition-structure.md)
- [Считывание свойств часового пояса встречи](how-to-read-time-zone-properties-from-an-appointment.md)

