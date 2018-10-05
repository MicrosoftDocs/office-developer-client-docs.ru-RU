---
title: Сведения о сохранении TZDEFINITION в потоке для помещения в двоичное свойство
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 0dec535d-d48f-39a5-97d5-0bd109134b3b
description: Свойства часового пояса, PidLidAppointmentTimeZoneDefinitionEndDisplay, PidLidAppointmentTimeZoneDefinitionRecur и PidLidAppointmentTimeZoneDefinitionStartDisplay двоичные свойства, каждая из которых содержит поток, который сопоставляется с именем постоянные формат TZDEFINITION структуры.
ms.openlocfilehash: f94b751a55aa852c962eebe5d46968e9e622e315
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25398621"
---
# <a name="about-persisting-tzdefinition-to-a-stream-to-commit-to-a-binary-property"></a>Сведения о сохранении TZDEFINITION в потоке для помещения в двоичное свойство

Свойства часового пояса, [PidLidAppointmentTimeZoneDefinitionEndDisplay](https://msdn.microsoft.com/library/7b6193cb-612b-408e-b9bc-285df313e2cc%28Office.15%29.aspx), [PidLidAppointmentTimeZoneDefinitionRecur](https://msdn.microsoft.com/library/52fd57a0-9e34-4452-9ecd-2acb454446c9%28Office.15%29.aspx)и [PidLidAppointmentTimeZoneDefinitionStartDisplay](https://msdn.microsoft.com/library/08239670-3211-420c-99d7-0056ed967cb8%28Office.15%29.aspx) двоичные с именем свойства, каждая из которых содержит поток, который соответствует сохраненного формата [TZDEFINITION](tzdefinition.md) структуры. 
  
В этом разделе описываются прямой порядок байтов, который можно использовать при сохранении **TZDEFINITION** к потоку для применения к одной из трех свойства двоичных файлов. Используйте тот же формат порядком в средства синтаксического анализа для интерпретации значения потока, полученный от одного из этих свойств. 
  
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

Чтобы сделать разбиение на изменение используется основной номер версии. Клиенты, которые не знакомы с основной номер версии следует считать свойства не существует. Клиенты, записи структуры следует указать константу **TZ_BIN_VERSION_MAJOR**. 
  
Дополнительный номер версии используется для расширения. Клиенты, которые не знакомы с дополнительный номер версии адресованы данные, которые они понять и пропустить данных, который может быть добавлен в каждом правиле или общий поток. Клиенты, записи структуры следует указать константу **TZ_BIN_VERSION_MINOR**. 
  
Если средство синтаксического анализа не понимает основной номер версии заголовка, его не следует чтение rest структуры и будут рассматриваться как, если отсутствуют данные. Если средство синтаксического анализа не распознает дополнительный номер версии заголовка, его следует использовать **cbHeader** игнорировать частей, которые он не понимает и перейти на чтение части потока, который он понимает. 
  
**WFlags** значение всегда **TZDEFINITION_FLAG_VALID_KEYNAME**. Имя ключа имеет максимальный размер **MAX_PATH**. 
  
Если средство синтаксического анализа не распознает основной номер версии правила, клиент должен игнорировать правила и использовать **cbRule** для перехода на следующее правило. Если средство синтаксического анализа не распознает дополнительный номер версии правила, клиент только следует выполнить синтаксический анализ частей правило, она понимает. 
  
При сохранении структура **TZDEFINITION** к потоку средства синтаксического анализа не рекомендуется создавать какие-либо сведения, не поддерживающий. 
  
Максимальное число правил составляет 1024.
  
Обратите внимание, что структура [TZREG](tzreg.md) сохраняется здесь иначе, чем при сохранении отдельно, так и тот же код не может использоваться для его обработки. 
  
## <a name="see-also"></a>См. также

- [Constants (Outlook exported APIs)](constants-outlook-exported-apis.md)
- [Анализ потока из двоичного свойства для считывания структуры TZDEFINITION](how-to-parse-stream-from-binary-property-to-read-tzdefinition-structure.md)
- [Считывание свойств часового пояса встречи](how-to-read-time-zone-properties-from-an-appointment.md)

