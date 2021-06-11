---
title: Каноническое свойство PidLidAppointmentTimeZoneDefinitionEndDisplay
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidAppointmentTimeZoneDefinitionEndDisplay
api_type:
- COM
ms.assetid: 7b6193cb-612b-408e-b9bc-285df313e2cc
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 24ccd25a1d799f3146bd230e5156be0051104f47
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32345383"
---
# <a name="pidlidappointmenttimezonedefinitionenddisplay-canonical-property"></a><span data-ttu-id="cd261-103">Каноническое свойство PidLidAppointmentTimeZoneDefinitionEndDisplay</span><span class="sxs-lookup"><span data-stu-id="cd261-103">PidLidAppointmentTimeZoneDefinitionEndDisplay Canonical Property</span></span>

  
  
<span data-ttu-id="cd261-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="cd261-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="cd261-105">Содержит поток, который сопополагает с упорным форматом структуры [TZDEFINITION,](https://msdn.microsoft.com/library/0ae21571-2299-6407-807c-428668bb6798%28Office.15%29.aspx) в котором хранится описание часового пояса, используемого при выборе конечного времени назначения или собрания одного экземпляра.</span><span class="sxs-lookup"><span data-stu-id="cd261-105">Contains a stream that maps to the persisted format of a [TZDEFINITION](https://msdn.microsoft.com/library/0ae21571-2299-6407-807c-428668bb6798%28Office.15%29.aspx) structure, which stores the description for the time zone that is used when the end time of a single-instance appointment or meeting request is selected.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="cd261-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="cd261-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="cd261-107">dispidApptTZDefEndDisplay</span><span class="sxs-lookup"><span data-stu-id="cd261-107">dispidApptTZDefEndDisplay</span></span>  <br/> |
|<span data-ttu-id="cd261-108">Набор свойств:</span><span class="sxs-lookup"><span data-stu-id="cd261-108">Property set:</span></span>  <br/> |<span data-ttu-id="cd261-109">PSETID_Appointment</span><span class="sxs-lookup"><span data-stu-id="cd261-109">PSETID_Appointment</span></span>  <br/> |
|<span data-ttu-id="cd261-110">Long ID (LID):</span><span class="sxs-lookup"><span data-stu-id="cd261-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="cd261-111">0x0000825F</span><span class="sxs-lookup"><span data-stu-id="cd261-111">0x0000825F</span></span>  <br/> |
|<span data-ttu-id="cd261-112">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="cd261-112">Data type:</span></span>  <br/> |<span data-ttu-id="cd261-113">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="cd261-113">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="cd261-114">Область:</span><span class="sxs-lookup"><span data-stu-id="cd261-114">Area:</span></span>  <br/> |<span data-ttu-id="cd261-115">Календарь</span><span class="sxs-lookup"><span data-stu-id="cd261-115">Calendar</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="cd261-116">Примечания</span><span class="sxs-lookup"><span data-stu-id="cd261-116">Remarks</span></span>

<span data-ttu-id="cd261-117">Microsoft Office Outlook 2003 или более ранних лет и решения, основанные на объектах данных совместной работы (CDO) 1.2.1 и не запускаемом средстве обновления календаря для Outlook или Microsoft Exchange Server, сохраняют время начала и окончания встреч и запросов на собрания в координирующем универсальном времени (UTC).</span><span class="sxs-lookup"><span data-stu-id="cd261-117">Microsoft Office Outlook 2003 or earlier, and solutions that are based on Collaboration Data Objects (CDO) 1.2.1 and that have not run the calendar update tool for Outlook or Microsoft Exchange Server, store the start time and end time of single-instance appointments and meeting requests in Coordinated Universal Time (UTC).</span></span> <span data-ttu-id="cd261-118">Эти клиенты не хранят информацию о часовом поясе, в котором создается запрос на встречу или встречу.</span><span class="sxs-lookup"><span data-stu-id="cd261-118">These clients do not store any information for the time zone where the appointment or meeting request is created.</span></span>
  
<span data-ttu-id="cd261-119">Версии Microsoft Outlook с Microsoft Office Outlook 2007 г., а решения на основе CDO 1.2.1, которые запускали средство обновления Outlook или Exchange Server календаря, используют **dispidApptTZDefEndDisplay** для хранения часового пояса в течение конечного времени.</span><span class="sxs-lookup"><span data-stu-id="cd261-119">Versions of Microsoft Outlook since Microsoft Office Outlook 2007, and solutions based on CDO 1.2.1 that have run the Outlook or Exchange Server calendar update tool use **dispidApptTZDefEndDisplay** to store the time zone for the end time.</span></span> <span data-ttu-id="cd261-120">**dispidApptTZDefEndDisplay** показывает встречу или собрание в исходном часовом поясе, которое было запланировано, и определяет, следует ли корректировать конечное время при изменении правил часового пояса.</span><span class="sxs-lookup"><span data-stu-id="cd261-120">**dispidApptTZDefEndDisplay** shows the appointment or meeting in the original time zone that it was scheduled, and determines whether the end time should be adjusted if the rules of the time zone change.</span></span> <span data-ttu-id="cd261-121">Если этого свойства не хватает, используется часовой пояс, указанный **свойством dispidApptTZDefStartDisplay** [(PidLidAppointmentTimeZoneDefinitionStartDisplay).](pidlidappointmenttimezonedefinitionstartdisplay-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="cd261-121">If this property is missing, the time zone specified by the **dispidApptTZDefStartDisplay** ([PidLidAppointmentTimeZoneDefinitionStartDisplay](pidlidappointmenttimezonedefinitionstartdisplay-canonical-property.md)) property is used.</span></span> <span data-ttu-id="cd261-122">Если **dispidApptTZDefStartDisplay** отсутствует или недействительна, предполагается текущий локальный часовой пояс.</span><span class="sxs-lookup"><span data-stu-id="cd261-122">If **dispidApptTZDefStartDisplay** is missing or invalid, the current local time zone is assumed.</span></span> <span data-ttu-id="cd261-123">**dispidApptTZDefEndDisplay** используется только для отображения и не используется при расширении повторяемости.</span><span class="sxs-lookup"><span data-stu-id="cd261-123">**dispidApptTZDefEndDisplay** is used for display purposes only and is not used in recurrence expansion.</span></span> 
  
<span data-ttu-id="cd261-124">Разборщик должен быть осторожным, когда он читает поток, полученный из **dispidApptTZDefEndDisplay**, или когда он **сохраняется TZDEFINITION** в поток для приверженности двоичному свойству, такому как **dispidApptTZDefEndDisplay**.</span><span class="sxs-lookup"><span data-stu-id="cd261-124">A parser must be careful when it reads a stream obtained from **dispidApptTZDefEndDisplay**, or when it persists **TZDEFINITION** to a stream for commitment to a binary property such as **dispidApptTZDefEndDisplay**.</span></span> <span data-ttu-id="cd261-125">Дополнительные сведения см. в разделах О сохраняющихся [TZDEFINITION](https://msdn.microsoft.com/library/0dec535d-d48f-39a5-97d5-0bd109134b3b%28Office.15%29.aspx)в потоке для фиксации двоичного свойства.</span><span class="sxs-lookup"><span data-stu-id="cd261-125">For more information, see [About persisting TZDEFINITION to a stream to commit to a binary property](https://msdn.microsoft.com/library/0dec535d-d48f-39a5-97d5-0bd109134b3b%28Office.15%29.aspx).</span></span>
  
 <span data-ttu-id="cd261-126">**dispidApptTZDefEndDisplay** указывает сведения о часовом поясе для свойства **dispidApptEndWhole** [(PidLidAppointmentEndWhole).](pidlidappointmentendwhole-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="cd261-126">**dispidApptTZDefEndDisplay** specifies time zone information for the **dispidApptEndWhole** ([PidLidAppointmentEndWhole](pidlidappointmentendwhole-canonical-property.md)) property.</span></span> <span data-ttu-id="cd261-127">Формат, ограничения и вычисления **dispidApptTZDefEndDisplay** те же, что и в свойстве **dispidApptTZDefStartDisplay.**</span><span class="sxs-lookup"><span data-stu-id="cd261-127">The format, constraints, and computation of **dispidApptTZDefEndDisplay** are the same as specified in the **dispidApptTZDefStartDisplay** property.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="cd261-128">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="cd261-128">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="cd261-129">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="cd261-129">Protocol specifications</span></span>

<span data-ttu-id="cd261-130">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="cd261-130">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="cd261-131">Предоставляет определения набора свойств и ссылки на связанные Exchange Server протоколы.</span><span class="sxs-lookup"><span data-stu-id="cd261-131">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="cd261-132">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="cd261-132">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="cd261-133">Указывает свойства и операции для встреч, запросов на собрания и ответных сообщений.</span><span class="sxs-lookup"><span data-stu-id="cd261-133">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="cd261-134">Файлы заголовки</span><span class="sxs-lookup"><span data-stu-id="cd261-134">Header files</span></span>

<span data-ttu-id="cd261-135">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="cd261-135">Mapidefs.h</span></span>
  
> <span data-ttu-id="cd261-136">Предоставляет определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="cd261-136">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="cd261-137">См. также</span><span class="sxs-lookup"><span data-stu-id="cd261-137">See also</span></span>



[<span data-ttu-id="cd261-138">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="cd261-138">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="cd261-139">Канонические свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="cd261-139">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="cd261-140">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="cd261-140">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="cd261-141">Сопоставление имен MAPI с каноническими именами свойств</span><span class="sxs-lookup"><span data-stu-id="cd261-141">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

