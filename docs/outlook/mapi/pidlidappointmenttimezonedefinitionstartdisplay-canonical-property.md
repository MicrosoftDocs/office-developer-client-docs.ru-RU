---
title: Каноническое свойство PidLidAppointmentTimeZoneDefinitionStartDisplay
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidAppointmentTimeZoneDefinitionStartDispl
api_type:
- COM
ms.assetid: 08239670-3211-420c-99d7-0056ed967cb8
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 504dc4b1cecb9798590e4a15968acc3aa98fe4a6
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32345019"
---
# <a name="pidlidappointmenttimezonedefinitionstartdisplay-canonical-property"></a><span data-ttu-id="95730-103">Каноническое свойство PidLidAppointmentTimeZoneDefinitionStartDisplay</span><span class="sxs-lookup"><span data-stu-id="95730-103">PidLidAppointmentTimeZoneDefinitionStartDisplay Canonical Property</span></span>

  
  
<span data-ttu-id="95730-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="95730-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="95730-105">Содержит поток, который сопополагает с упорным форматом структуры [TZDEFINITION,](https://msdn.microsoft.com/library/0ae21571-2299-6407-807c-428668bb6798%28Office.15%29.aspx) в котором хранится описание часового пояса, используемого при выборе времени начала встречи или собрания одного экземпляра.</span><span class="sxs-lookup"><span data-stu-id="95730-105">Contains a stream that maps to the persisted format of a [TZDEFINITION](https://msdn.microsoft.com/library/0ae21571-2299-6407-807c-428668bb6798%28Office.15%29.aspx) structure, which stores the description for the time zone that is used when the start time of a single-instance appointment or meeting request is selected.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="95730-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="95730-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="95730-107">dispidApptTZDefStartDisplay</span><span class="sxs-lookup"><span data-stu-id="95730-107">dispidApptTZDefStartDisplay</span></span>  <br/> |
|<span data-ttu-id="95730-108">Набор свойств:</span><span class="sxs-lookup"><span data-stu-id="95730-108">Property set:</span></span>  <br/> |<span data-ttu-id="95730-109">PSETID_Appointment</span><span class="sxs-lookup"><span data-stu-id="95730-109">PSETID_Appointment</span></span>  <br/> |
|<span data-ttu-id="95730-110">Long ID (LID):</span><span class="sxs-lookup"><span data-stu-id="95730-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="95730-111">0x0000825E</span><span class="sxs-lookup"><span data-stu-id="95730-111">0x0000825E</span></span>  <br/> |
|<span data-ttu-id="95730-112">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="95730-112">Data type:</span></span>  <br/> |<span data-ttu-id="95730-113">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="95730-113">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="95730-114">Область:</span><span class="sxs-lookup"><span data-stu-id="95730-114">Area:</span></span>  <br/> |<span data-ttu-id="95730-115">Календарь</span><span class="sxs-lookup"><span data-stu-id="95730-115">Calendar</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="95730-116">Примечания</span><span class="sxs-lookup"><span data-stu-id="95730-116">Remarks</span></span>

<span data-ttu-id="95730-117">Microsoft Office Outlook 2003 или более ранних лет и решения, основанные на объектах данных совместной работы (CDO) 1.2.1 и не запускаемом средстве обновления календаря для Outlook или Microsoft Exchange Server, сохраняют время начала и окончания встреч и запросов на собрания в координирующем универсальном времени (UTC).</span><span class="sxs-lookup"><span data-stu-id="95730-117">Microsoft Office Outlook 2003 or earlier, and solutions that are based on Collaboration Data Objects (CDO) 1.2.1 and that have not run the calendar update tool for Outlook or Microsoft Exchange Server, store the start time and end time of single-instance appointments and meeting requests in Coordinated Universal Time (UTC).</span></span> <span data-ttu-id="95730-118">Эти клиенты не хранят сведения о часовом поясе, в котором создается запрос на встречу или собрание.</span><span class="sxs-lookup"><span data-stu-id="95730-118">These clients do not store any information for the time zone in which the appointment or meeting request is created.</span></span>
  
<span data-ttu-id="95730-119">Версии Outlook с Microsoft Office Outlook 2007 г. и решения на основе CDO 1.2.1, которые запускали средство обновления Outlook или Exchange Server календаря, используют это свойство для хранения часового пояса для начала.</span><span class="sxs-lookup"><span data-stu-id="95730-119">Versions of Outlook since Microsoft Office Outlook 2007, and solutions based on CDO 1.2.1 that have run the Outlook or Exchange Server calendar update tool use this property to store the time zone for the start time.</span></span> <span data-ttu-id="95730-120">Свойство **dispidApptTZDefStartDisplay** показывает встречу или встречу в исходном часовом поясе, которое было запланировано.</span><span class="sxs-lookup"><span data-stu-id="95730-120">The **dispidApptTZDefStartDisplay** property shows the appointment or meeting in the original time zone that it was scheduled.</span></span> <span data-ttu-id="95730-121">Он определяет, следует ли корректировать время начала при изменении правил часового пояса.</span><span class="sxs-lookup"><span data-stu-id="95730-121">It determines whether the start time should be adjusted if the rules of the time zone change.</span></span> <span data-ttu-id="95730-122">Если этого свойства не хватает, предполагается текущий локальный часовой пояс.</span><span class="sxs-lookup"><span data-stu-id="95730-122">If this property is missing, the current local time zone is assumed.</span></span> <span data-ttu-id="95730-123">Это свойство используется только для отображения и не используется в расширении повторяемости.</span><span class="sxs-lookup"><span data-stu-id="95730-123">This property is used for display purposes only and is not used in recurrence expansion.</span></span> 
  
<span data-ttu-id="95730-124">Разборщик должен быть осторожным, когда он читает поток, полученный из этого свойства, или когда он **сохраняется TZDEFINITION** в поток для приверженности двоичному свойству, такому как **dispidApptTZDefStartDisplay**.</span><span class="sxs-lookup"><span data-stu-id="95730-124">A parser must be careful when it reads a stream obtained from this property, or when it persists **TZDEFINITION** to a stream for commitment to a binary property such as **dispidApptTZDefStartDisplay**.</span></span> <span data-ttu-id="95730-125">Дополнительные сведения см. в разделах О сохраняющихся [TZDEFINITION](https://msdn.microsoft.com/library/0dec535d-d48f-39a5-97d5-0bd109134b3b%28Office.15%29.aspx)в потоке для фиксации двоичного свойства.</span><span class="sxs-lookup"><span data-stu-id="95730-125">For more information, see [About persisting TZDEFINITION to a stream to commit to a binary property](https://msdn.microsoft.com/library/0dec535d-d48f-39a5-97d5-0bd109134b3b%28Office.15%29.aspx).</span></span>
  
<span data-ttu-id="95730-126">Это свойство указывает сведения о часовом поясе для свойства **dispidApptStartWhole** [(PidLidAppointmentStartWhole).](pidlidappointmentstartwhole-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="95730-126">This property specifies time zone information for the **dispidApptStartWhole** ([PidLidAppointmentStartWhole](pidlidappointmentstartwhole-canonical-property.md)) property.</span></span> <span data-ttu-id="95730-127">Значение **dispidApptTZDefStartDisplay** используется для преобразования даты начала и времени из UTC в локальный часовой пояс для отображения.</span><span class="sxs-lookup"><span data-stu-id="95730-127">The value of **dispidApptTZDefStartDisplay** is used to convert the start date and time from UTC to the local time zone for display purposes.</span></span> <span data-ttu-id="95730-128">Для каждого **TZRULE,** указанного этим свойством, флаг TZRULE_FLAG_RECUR_CURRENT_TZREG не должен быть задан.</span><span class="sxs-lookup"><span data-stu-id="95730-128">For each **TZRULE** specified by this property, the TZRULE_FLAG_RECUR_CURRENT_TZREG flag must not be set.</span></span> <span data-ttu-id="95730-129">Например, если **TZRULE** является эффективным правилом, значение **поля, TZRULE** должно быть "0x0002"; в противном случае он должен быть "0x0000".</span><span class="sxs-lookup"><span data-stu-id="95730-129">For example, if the **TZRULE** is the effective rule, the value of the field, **TZRULE** must be "0x0002"; otherwise, it must be "0x0000".</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="95730-130">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="95730-130">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="95730-131">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="95730-131">Protocol specifications</span></span>

<span data-ttu-id="95730-132">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="95730-132">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="95730-133">Предоставляет определения набора свойств и ссылки на связанные Exchange Server протоколы..</span><span class="sxs-lookup"><span data-stu-id="95730-133">Provides property set definitions and references to related Exchange Server protocol specifications..</span></span>
    
<span data-ttu-id="95730-134">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="95730-134">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="95730-135">Указывает свойства и операции для встреч, запросов на собрания и ответных сообщений.</span><span class="sxs-lookup"><span data-stu-id="95730-135">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="95730-136">Файлы заголовки</span><span class="sxs-lookup"><span data-stu-id="95730-136">Header files</span></span>

<span data-ttu-id="95730-137">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="95730-137">Mapidefs.h</span></span>
  
> <span data-ttu-id="95730-138">Предоставляет определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="95730-138">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="95730-139">См. также</span><span class="sxs-lookup"><span data-stu-id="95730-139">See also</span></span>



[<span data-ttu-id="95730-140">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="95730-140">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="95730-141">Канонические свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="95730-141">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="95730-142">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="95730-142">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="95730-143">Сопоставление имен MAPI с каноническими именами свойств</span><span class="sxs-lookup"><span data-stu-id="95730-143">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

