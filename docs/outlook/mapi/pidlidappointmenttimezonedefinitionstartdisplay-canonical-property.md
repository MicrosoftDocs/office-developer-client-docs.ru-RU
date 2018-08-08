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
ms.openlocfilehash: f6d0c7c6f6f34330c143781fbac976392ee1c9a1
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19810203"
---
# <a name="pidlidappointmenttimezonedefinitionstartdisplay-canonical-property"></a><span data-ttu-id="b1390-103">Каноническое свойство PidLidAppointmentTimeZoneDefinitionStartDisplay</span><span class="sxs-lookup"><span data-stu-id="b1390-103">PidLidAppointmentTimeZoneDefinitionStartDisplay Canonical Property</span></span>

  
  
<span data-ttu-id="b1390-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="b1390-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="b1390-105">Содержит поток, который соответствует сохраненного формата [TZDEFINITION](http://msdn.microsoft.com/library/0ae21571-2299-6407-807c-428668bb6798%28Office.15%29.aspx) структуры, который хранит описание часовой пояс, который используется при выборе время начала единичных встречи или приглашения на собрание.</span><span class="sxs-lookup"><span data-stu-id="b1390-105">Contains a stream that maps to the persisted format of a [TZDEFINITION](http://msdn.microsoft.com/library/0ae21571-2299-6407-807c-428668bb6798%28Office.15%29.aspx) structure, which stores the description for the time zone that is used when the start time of a single-instance appointment or meeting request is selected.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="b1390-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="b1390-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="b1390-107">dispidApptTZDefStartDisplay</span><span class="sxs-lookup"><span data-stu-id="b1390-107">dispidApptTZDefStartDisplay</span></span>  <br/> |
|<span data-ttu-id="b1390-108">Набор свойств:</span><span class="sxs-lookup"><span data-stu-id="b1390-108">Property set:</span></span>  <br/> |<span data-ttu-id="b1390-109">PSETID_Appointment</span><span class="sxs-lookup"><span data-stu-id="b1390-109">PSETID_Appointment</span></span>  <br/> |
|<span data-ttu-id="b1390-110">Длинный идентификатор (КРЫШКА):</span><span class="sxs-lookup"><span data-stu-id="b1390-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="b1390-111">0x0000825E</span><span class="sxs-lookup"><span data-stu-id="b1390-111">0x0000825E</span></span>  <br/> |
|<span data-ttu-id="b1390-112">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="b1390-112">Data type:</span></span>  <br/> |<span data-ttu-id="b1390-113">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="b1390-113">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="b1390-114">Область:</span><span class="sxs-lookup"><span data-stu-id="b1390-114">Area:</span></span>  <br/> |<span data-ttu-id="b1390-115">Календарь</span><span class="sxs-lookup"><span data-stu-id="b1390-115">Calendar</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b1390-116">Замечания</span><span class="sxs-lookup"><span data-stu-id="b1390-116">Remarks</span></span>

<span data-ttu-id="b1390-117">Время начала и время окончания экземпляра хранилища Microsoft Office Outlook 2003 или более ранних версий и решения, основанные на объекты совместной работы (CDO) 1.2.1 и, не запускайте средство обновления календаря Outlook или Microsoft Exchange Server встречи и приглашения на собрания в формате UTC.</span><span class="sxs-lookup"><span data-stu-id="b1390-117">Microsoft Office Outlook 2003 or earlier, and solutions that are based on Collaboration Data Objects (CDO) 1.2.1 and that have not run the calendar update tool for Outlook or Microsoft Exchange Server, store the start time and end time of single-instance appointments and meeting requests in Coordinated Universal Time (UTC).</span></span> <span data-ttu-id="b1390-118">Эти клиенты не следует хранить какие-либо сведения для часового пояса, в котором создается встречи или приглашения на собрание.</span><span class="sxs-lookup"><span data-stu-id="b1390-118">These clients do not store any information for the time zone in which the appointment or meeting request is created.</span></span>
  
<span data-ttu-id="b1390-119">Версии Outlook, так как Microsoft Office Outlook 2007 и решений на основании CDO 1.2.1 (en), ранее выполненные средство обновления календаря Outlook или Exchange Server это свойство используется для хранения часовой пояс для времени начала.</span><span class="sxs-lookup"><span data-stu-id="b1390-119">Versions of Outlook since Microsoft Office Outlook 2007, and solutions based on CDO 1.2.1 that have run the Outlook or Exchange Server calendar update tool use this property to store the time zone for the start time.</span></span> <span data-ttu-id="b1390-120">Свойство **dispidApptTZDefStartDisplay** показывает встречи или собрания в исходный часовой пояс, что было запланировано.</span><span class="sxs-lookup"><span data-stu-id="b1390-120">The **dispidApptTZDefStartDisplay** property shows the appointment or meeting in the original time zone that it was scheduled.</span></span> <span data-ttu-id="b1390-121">Определяет корректировки время начала изменения правила часового пояса.</span><span class="sxs-lookup"><span data-stu-id="b1390-121">It determines whether the start time should be adjusted if the rules of the time zone change.</span></span> <span data-ttu-id="b1390-122">Если данное свойство отсутствует, используется значение текущего часового пояса.</span><span class="sxs-lookup"><span data-stu-id="b1390-122">If this property is missing, the current local time zone is assumed.</span></span> <span data-ttu-id="b1390-123">Это свойство используется только для отображения и не используется в расширения повторения.</span><span class="sxs-lookup"><span data-stu-id="b1390-123">This property is used for display purposes only and is not used in recurrence expansion.</span></span> 
  
<span data-ttu-id="b1390-124">Средство синтаксического анализа необходимо следить за тем, при считывании потока, полученного из этого свойства или для сохранения **TZDEFINITION** поток для, направленных на двоичного свойства, такие как **dispidApptTZDefStartDisplay**.</span><span class="sxs-lookup"><span data-stu-id="b1390-124">A parser must be careful when it reads a stream obtained from this property, or when it persists **TZDEFINITION** to a stream for commitment to a binary property such as **dispidApptTZDefStartDisplay**.</span></span> <span data-ttu-id="b1390-125">Для получения дополнительных сведений см [Сохранение TZDEFINITION поток, чтобы зафиксировать двоичного свойства](http://msdn.microsoft.com/library/0dec535d-d48f-39a5-97d5-0bd109134b3b%28Office.15%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="b1390-125">For more information, see [About persisting TZDEFINITION to a stream to commit to a binary property](http://msdn.microsoft.com/library/0dec535d-d48f-39a5-97d5-0bd109134b3b%28Office.15%29.aspx).</span></span>
  
<span data-ttu-id="b1390-126">Это свойство определяет часовой пояс информацию для свойства **dispidApptStartWhole** ([PidLidAppointmentStartWhole](pidlidappointmentstartwhole-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="b1390-126">This property specifies time zone information for the **dispidApptStartWhole** ([PidLidAppointmentStartWhole](pidlidappointmentstartwhole-canonical-property.md)) property.</span></span> <span data-ttu-id="b1390-127">Значение **dispidApptTZDefStartDisplay** используется для преобразования даты начала и время в формате UTC в локальный часовой пояс для отображения.</span><span class="sxs-lookup"><span data-stu-id="b1390-127">The value of **dispidApptTZDefStartDisplay** is used to convert the start date and time from UTC to the local time zone for display purposes.</span></span> <span data-ttu-id="b1390-128">Для каждого **TZRULE** заданный этим свойством флаг TZRULE_FLAG_RECUR_CURRENT_TZREG не должно быть задано.</span><span class="sxs-lookup"><span data-stu-id="b1390-128">For each **TZRULE** specified by this property, the TZRULE_FLAG_RECUR_CURRENT_TZREG flag must not be set.</span></span> <span data-ttu-id="b1390-129">Например если **TZRULE** эффективных правило, значение поля, **TZRULE** должен быть «0x0002»; в противном случае он должен быть «0x0000».</span><span class="sxs-lookup"><span data-stu-id="b1390-129">For example, if the **TZRULE** is the effective rule, the value of the field, **TZRULE** must be "0x0002"; otherwise, it must be "0x0000".</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="b1390-130">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="b1390-130">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="b1390-131">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="b1390-131">Protocol specifications</span></span>

<span data-ttu-id="b1390-132">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="b1390-132">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="b1390-133">Содержит определения набора свойств и ссылки на связанные спецификаций протокола Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="b1390-133">Provides property set definitions and references to related Exchange Server protocol specifications..</span></span>
    
<span data-ttu-id="b1390-134">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="b1390-134">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="b1390-135">Задает свойства и операции для встречи, приглашения на собрание и ответы.</span><span class="sxs-lookup"><span data-stu-id="b1390-135">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="b1390-136">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="b1390-136">Header files</span></span>

<span data-ttu-id="b1390-137">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="b1390-137">Mapidefs.h</span></span>
  
> <span data-ttu-id="b1390-138">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="b1390-138">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="b1390-139">См. также</span><span class="sxs-lookup"><span data-stu-id="b1390-139">See also</span></span>



[<span data-ttu-id="b1390-140">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="b1390-140">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="b1390-141">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="b1390-141">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="b1390-142">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="b1390-142">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="b1390-143">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="b1390-143">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

