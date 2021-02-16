---
title: Сведения о сохранении TZDEFINITION в потоке для помещения в двоичное свойство
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 0dec535d-d48f-39a5-97d5-0bd109134b3b
description: Свойства часового пояса PidLidAppointmentTimeZoneDefinitionEndDisplay, PidLidAppointmentTimeZoneDefinitionRecur и PidLidAppointmentTimeZoneDefinitionStartDisplay — это двоичные именуемые свойства, каждое из которых содержит поток, который сопостает сохраняемого формата структуры TZDEFINITION.
ms.openlocfilehash: f94b751a55aa852c962eebe5d46968e9e622e315
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316978"
---
# <a name="about-persisting-tzdefinition-to-a-stream-to-commit-to-a-binary-property"></a><span data-ttu-id="5f3c9-103">Сведения о сохранении TZDEFINITION в потоке для помещения в двоичное свойство</span><span class="sxs-lookup"><span data-stu-id="5f3c9-103">About persisting TZDEFINITION to a stream to commit to a binary property</span></span>

<span data-ttu-id="5f3c9-104">Свойства часового пояса [PidLidAppointmentTimeZoneDefinitionEndDisplay,](https://msdn.microsoft.com/library/7b6193cb-612b-408e-b9bc-285df313e2cc%28Office.15%29.aspx) [PidLidAppointmentTimeZoneDefinitionRecur](https://msdn.microsoft.com/library/52fd57a0-9e34-4452-9ecd-2acb454446c9%28Office.15%29.aspx)и [PidLidAppointmentTimeZoneDefinitionStartDisplay](https://msdn.microsoft.com/library/08239670-3211-420c-99d7-0056ed967cb8%28Office.15%29.aspx) — это двоичные именуемые свойства, каждое из которых содержит поток, который сопостает сохраняемого формата структуры [TZDEFINITION.](tzdefinition.md)</span><span class="sxs-lookup"><span data-stu-id="5f3c9-104">The time zone properties, [PidLidAppointmentTimeZoneDefinitionEndDisplay](https://msdn.microsoft.com/library/7b6193cb-612b-408e-b9bc-285df313e2cc%28Office.15%29.aspx), [PidLidAppointmentTimeZoneDefinitionRecur](https://msdn.microsoft.com/library/52fd57a0-9e34-4452-9ecd-2acb454446c9%28Office.15%29.aspx), and [PidLidAppointmentTimeZoneDefinitionStartDisplay](https://msdn.microsoft.com/library/08239670-3211-420c-99d7-0056ed967cb8%28Office.15%29.aspx) are binary named properties, each of which contains a stream that maps to the persisted format of a [TZDEFINITION](tzdefinition.md) structure.</span></span> 
  
<span data-ttu-id="5f3c9-105">В этом разделе описывается небольшой конечный формат, который можно использовать при сохраняемом **TZDEFINITION** в потоке для фиксации одного из трех двоичных свойств.</span><span class="sxs-lookup"><span data-stu-id="5f3c9-105">This topic describes a little endian format that can be used when persisting **TZDEFINITION** to a stream to commit to one of three binary properties.</span></span> <span data-ttu-id="5f3c9-106">Используйте тот же конечный формат в parser для интерпретации значения потока, полученного из одного из этих свойств.</span><span class="sxs-lookup"><span data-stu-id="5f3c9-106">Use the same endian format in a parser to interpret a stream value obtained from one of these properties.</span></span> 
  
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

<span data-ttu-id="5f3c9-107">Основной номер версии используется для внести серьезные изменения.</span><span class="sxs-lookup"><span data-stu-id="5f3c9-107">The major version number is used to make a breaking change.</span></span> <span data-ttu-id="5f3c9-108">Клиенты, которые не знакомы с основным номером версии, должны рассматривать свойство так, будто его там нет.</span><span class="sxs-lookup"><span data-stu-id="5f3c9-108">Clients that are unfamiliar with the major version number should treat the property as if it is not there.</span></span> <span data-ttu-id="5f3c9-109">Клиенты, записывавая структуру, должны **указывать константы TZ_BIN_VERSION_MAJOR.**</span><span class="sxs-lookup"><span data-stu-id="5f3c9-109">Clients writing the structure should specify the constant **TZ_BIN_VERSION_MAJOR**.</span></span> 
  
<span data-ttu-id="5f3c9-110">Номер второстепенной версии используется для большого числа вариантов.</span><span class="sxs-lookup"><span data-stu-id="5f3c9-110">The minor version number is used for extensibility.</span></span> <span data-ttu-id="5f3c9-111">Клиенты, которые не знакомы с номером второстепенной версии, должны прочитать данные, которые они понимают, и пропустить данные, которые могут быть примечены к каждому правилу или общему потоку.</span><span class="sxs-lookup"><span data-stu-id="5f3c9-111">Clients that are unfamiliar with the minor version number should read the data that they understand, and skip over the data that might be appended to each rule or to the overall stream.</span></span> <span data-ttu-id="5f3c9-112">Клиенты, записывавая структуру, должны **указывать константы TZ_BIN_VERSION_MINOR.**</span><span class="sxs-lookup"><span data-stu-id="5f3c9-112">Clients writing the structure should specify the constant **TZ_BIN_VERSION_MINOR**.</span></span> 
  
<span data-ttu-id="5f3c9-113">Если анализщик не понимает основной версии загона, он не должен читать остальную часть структуры и вести себя так, как если бы данные отсутствуют.</span><span class="sxs-lookup"><span data-stu-id="5f3c9-113">If a parser does not understand the major version of the header, it should not read the rest of the structure and behave as if the data is missing.</span></span> <span data-ttu-id="5f3c9-114">Если разбор не понимает дополнительные версии заголовок, он должен использовать **cbHeader,** чтобы игнорировать части, которые он не понимает, и заранее читать части потока, который он понимает.</span><span class="sxs-lookup"><span data-stu-id="5f3c9-114">If a parser does not understand the minor version of the header, it should use **cbHeader** to ignore the portions that it does not understand and advance to read the portions of the stream that it understands.</span></span> 
  
<span data-ttu-id="5f3c9-115">Значение **wFlags** всегда **TZDEFINITION_FLAG_VALID_KEYNAME.**</span><span class="sxs-lookup"><span data-stu-id="5f3c9-115">The value of **wFlags** is always **TZDEFINITION_FLAG_VALID_KEYNAME**.</span></span> <span data-ttu-id="5f3c9-116">Имя ключа имеет максимальный размер **MAX_PATH.**</span><span class="sxs-lookup"><span data-stu-id="5f3c9-116">The key name has a maximum size of **MAX_PATH**.</span></span> 
  
<span data-ttu-id="5f3c9-117">Если обсчетщик не распознает основной версии правила, клиент должен игнорировать правило и использовать **cbRule,** чтобы следующую версию правила.</span><span class="sxs-lookup"><span data-stu-id="5f3c9-117">If a parser does not recognize the major version of a rule, the client should ignore the rule, and use **cbRule** to advance to the next rule.</span></span> <span data-ttu-id="5f3c9-118">Если обсчетщик не распознает второстепенную версию правила, клиент должен только разобрать части правила, которые он понимает.</span><span class="sxs-lookup"><span data-stu-id="5f3c9-118">If a parser does not recognize the minor version of a rule, the client should only parse the parts of the rule that it understands.</span></span> 
  
<span data-ttu-id="5f3c9-119">При сохраняемой структуре **TZDEFINITION** в потоке, разберите не следует пытаться записать какие-либо сведения, которые он не понимает.</span><span class="sxs-lookup"><span data-stu-id="5f3c9-119">When persisting a **TZDEFINITION** structure to a stream, a parser should not try to write any information that it does not understand.</span></span> 
  
<span data-ttu-id="5f3c9-120">Максимальное число правил — 1024.</span><span class="sxs-lookup"><span data-stu-id="5f3c9-120">The maximum number of rules is 1024.</span></span>
  
<span data-ttu-id="5f3c9-121">Обратите внимание, что структура [TZREG](tzreg.md) сохраняется здесь иначе, чем когда она сохраняется отдельно, поэтому один и тот же код нельзя использовать для ее разметки.</span><span class="sxs-lookup"><span data-stu-id="5f3c9-121">Note that the [TZREG](tzreg.md) structure is persisted here differently than when persisted alone, so the same code cannot be used to parse it.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="5f3c9-122">См. также</span><span class="sxs-lookup"><span data-stu-id="5f3c9-122">See also</span></span>

- [<span data-ttu-id="5f3c9-123">Constants (Outlook exported APIs)</span><span class="sxs-lookup"><span data-stu-id="5f3c9-123">Constants (Outlook exported APIs)</span></span>](constants-outlook-exported-apis.md)
- [<span data-ttu-id="5f3c9-124">Анализ потока из двоичного свойства для считывания структуры TZDEFINITION</span><span class="sxs-lookup"><span data-stu-id="5f3c9-124">Parse a stream from a binary property to read the TZDEFINITION structure</span></span>](how-to-parse-stream-from-binary-property-to-read-tzdefinition-structure.md)
- [<span data-ttu-id="5f3c9-125">Считывание свойств часового пояса встречи</span><span class="sxs-lookup"><span data-stu-id="5f3c9-125">Read time zone properties from an appointment</span></span>](how-to-read-time-zone-properties-from-an-appointment.md)

