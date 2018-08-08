---
title: Сведения о сохранении TZDEFINITION в потоке для помещения в двоичное свойство
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 0dec535d-d48f-39a5-97d5-0bd109134b3b
description: Свойства часового пояса, PidLidAppointmentTimeZoneDefinitionEndDisplay, PidLidAppointmentTimeZoneDefinitionRecur и PidLidAppointmentTimeZoneDefinitionStartDisplay двоичные свойства, каждая из которых содержит поток, который сопоставляется с именем постоянные формат TZDEFINITION структуры.
ms.openlocfilehash: 8e00c7203e2a0adfdf9ff3e6dadff6485c8b5111
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19807671"
---
# <a name="about-persisting-tzdefinition-to-a-stream-to-commit-to-a-binary-property"></a><span data-ttu-id="38112-103">Сведения о сохранении TZDEFINITION в потоке для помещения в двоичное свойство</span><span class="sxs-lookup"><span data-stu-id="38112-103">About persisting TZDEFINITION to a stream to commit to a binary property</span></span>

<span data-ttu-id="38112-104">Свойства часового пояса, [PidLidAppointmentTimeZoneDefinitionEndDisplay](http://msdn.microsoft.com/library/7b6193cb-612b-408e-b9bc-285df313e2cc%28Office.15%29.aspx), [PidLidAppointmentTimeZoneDefinitionRecur](http://msdn.microsoft.com/library/52fd57a0-9e34-4452-9ecd-2acb454446c9%28Office.15%29.aspx)и [PidLidAppointmentTimeZoneDefinitionStartDisplay](http://msdn.microsoft.com/library/08239670-3211-420c-99d7-0056ed967cb8%28Office.15%29.aspx) двоичные с именем свойства, каждая из которых содержит поток, который соответствует сохраненного формата [TZDEFINITION](tzdefinition.md) структуры.</span><span class="sxs-lookup"><span data-stu-id="38112-104">The time zone properties, [PidLidAppointmentTimeZoneDefinitionEndDisplay](http://msdn.microsoft.com/library/7b6193cb-612b-408e-b9bc-285df313e2cc%28Office.15%29.aspx), [PidLidAppointmentTimeZoneDefinitionRecur](http://msdn.microsoft.com/library/52fd57a0-9e34-4452-9ecd-2acb454446c9%28Office.15%29.aspx), and [PidLidAppointmentTimeZoneDefinitionStartDisplay](http://msdn.microsoft.com/library/08239670-3211-420c-99d7-0056ed967cb8%28Office.15%29.aspx) are binary named properties, each of which contains a stream that maps to the persisted format of a [TZDEFINITION](tzdefinition.md) structure.</span></span> 
  
<span data-ttu-id="38112-105">В этом разделе описываются прямой порядок байтов, который можно использовать при сохранении **TZDEFINITION** к потоку для применения к одной из трех свойства двоичных файлов.</span><span class="sxs-lookup"><span data-stu-id="38112-105">This topic describes a little endian format that can be used when persisting **TZDEFINITION** to a stream to commit to one of three binary properties.</span></span> <span data-ttu-id="38112-106">Используйте тот же формат порядком в средства синтаксического анализа для интерпретации значения потока, полученный от одного из этих свойств.</span><span class="sxs-lookup"><span data-stu-id="38112-106">Use the same endian format in a parser to interpret a stream value obtained from one of these properties.</span></span> 
  
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

<span data-ttu-id="38112-107">Чтобы сделать разбиение на изменение используется основной номер версии.</span><span class="sxs-lookup"><span data-stu-id="38112-107">The major version number is used to make a breaking change.</span></span> <span data-ttu-id="38112-108">Клиенты, которые не знакомы с основной номер версии следует считать свойства не существует.</span><span class="sxs-lookup"><span data-stu-id="38112-108">Clients that are unfamiliar with the major version number should treat the property as if it is not there.</span></span> <span data-ttu-id="38112-109">Клиенты, записи структуры следует указать константу **TZ_BIN_VERSION_MAJOR**.</span><span class="sxs-lookup"><span data-stu-id="38112-109">Clients writing the structure should specify the constant **TZ_BIN_VERSION_MAJOR**.</span></span> 
  
<span data-ttu-id="38112-110">Дополнительный номер версии используется для расширения.</span><span class="sxs-lookup"><span data-stu-id="38112-110">The minor version number is used for extensibility.</span></span> <span data-ttu-id="38112-111">Клиенты, которые не знакомы с дополнительный номер версии адресованы данные, которые они понять и пропустить данных, который может быть добавлен в каждом правиле или общий поток.</span><span class="sxs-lookup"><span data-stu-id="38112-111">Clients that are unfamiliar with the minor version number should read the data that they understand, and skip over the data that might be appended to each rule or to the overall stream.</span></span> <span data-ttu-id="38112-112">Клиенты, записи структуры следует указать константу **TZ_BIN_VERSION_MINOR**.</span><span class="sxs-lookup"><span data-stu-id="38112-112">Clients writing the structure should specify the constant **TZ_BIN_VERSION_MINOR**.</span></span> 
  
<span data-ttu-id="38112-113">Если средство синтаксического анализа не понимает основной номер версии заголовка, его не следует чтение rest структуры и будут рассматриваться как, если отсутствуют данные.</span><span class="sxs-lookup"><span data-stu-id="38112-113">If a parser does not understand the major version of the header, it should not read the rest of the structure and behave as if the data is missing.</span></span> <span data-ttu-id="38112-114">Если средство синтаксического анализа не распознает дополнительный номер версии заголовка, его следует использовать **cbHeader** игнорировать частей, которые он не понимает и перейти на чтение части потока, который он понимает.</span><span class="sxs-lookup"><span data-stu-id="38112-114">If a parser does not understand the minor version of the header, it should use **cbHeader** to ignore the portions that it does not understand and advance to read the portions of the stream that it understands.</span></span> 
  
<span data-ttu-id="38112-115">**WFlags** значение всегда **TZDEFINITION_FLAG_VALID_KEYNAME**.</span><span class="sxs-lookup"><span data-stu-id="38112-115">The value of **wFlags** is always **TZDEFINITION_FLAG_VALID_KEYNAME**.</span></span> <span data-ttu-id="38112-116">Имя ключа имеет максимальный размер **MAX_PATH**.</span><span class="sxs-lookup"><span data-stu-id="38112-116">The key name has a maximum size of **MAX_PATH**.</span></span> 
  
<span data-ttu-id="38112-117">Если средство синтаксического анализа не распознает основной номер версии правила, клиент должен игнорировать правила и использовать **cbRule** для перехода на следующее правило.</span><span class="sxs-lookup"><span data-stu-id="38112-117">If a parser does not recognize the major version of a rule, the client should ignore the rule, and use **cbRule** to advance to the next rule.</span></span> <span data-ttu-id="38112-118">Если средство синтаксического анализа не распознает дополнительный номер версии правила, клиент только следует выполнить синтаксический анализ частей правило, она понимает.</span><span class="sxs-lookup"><span data-stu-id="38112-118">If a parser does not recognize the minor version of a rule, the client should only parse the parts of the rule that it understands.</span></span> 
  
<span data-ttu-id="38112-119">При сохранении структура **TZDEFINITION** к потоку средства синтаксического анализа не рекомендуется создавать какие-либо сведения, не поддерживающий.</span><span class="sxs-lookup"><span data-stu-id="38112-119">When persisting a **TZDEFINITION** structure to a stream, a parser should not try to write any information that it does not understand.</span></span> 
  
<span data-ttu-id="38112-120">Максимальное число правил составляет 1024.</span><span class="sxs-lookup"><span data-stu-id="38112-120">The maximum number of rules is 1024.</span></span>
  
<span data-ttu-id="38112-121">Обратите внимание, что структура [TZREG](tzreg.md) сохраняется здесь иначе, чем при сохранении отдельно, так и тот же код не может использоваться для его обработки.</span><span class="sxs-lookup"><span data-stu-id="38112-121">Note that the [TZREG](tzreg.md) structure is persisted here differently than when persisted alone, so the same code cannot be used to parse it.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="38112-122">См. также</span><span class="sxs-lookup"><span data-stu-id="38112-122">See also</span></span>

- [<span data-ttu-id="38112-123">Constants (Outlook exported APIs)</span><span class="sxs-lookup"><span data-stu-id="38112-123">Constants (Outlook exported APIs)</span></span>](constants-outlook-exported-apis.md)
- [<span data-ttu-id="38112-124">Анализ потока из двоичного свойства для считывания структуры TZDEFINITION</span><span class="sxs-lookup"><span data-stu-id="38112-124">Parse a stream from a binary property to read the TZDEFINITION structure</span></span>](how-to-parse-stream-from-binary-property-to-read-tzdefinition-structure.md)
- [<span data-ttu-id="38112-125">Считывание свойств часового пояса встречи</span><span class="sxs-lookup"><span data-stu-id="38112-125">Read time zone properties from an appointment</span></span>](how-to-read-time-zone-properties-from-an-appointment.md)

