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
ms.openlocfilehash: 119cd7edc5b9b615a39cea6aa1c405c396ce2afa
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19810190"
---
# <a name="pidlidappointmenttimezonedefinitionenddisplay-canonical-property"></a><span data-ttu-id="d88b2-103">Каноническое свойство PidLidAppointmentTimeZoneDefinitionEndDisplay</span><span class="sxs-lookup"><span data-stu-id="d88b2-103">PidLidAppointmentTimeZoneDefinitionEndDisplay Canonical Property</span></span>

  
  
<span data-ttu-id="d88b2-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="d88b2-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="d88b2-105">Содержит поток, который соответствует сохраненного формата [TZDEFINITION](http://msdn.microsoft.com/library/0ae21571-2299-6407-807c-428668bb6798%28Office.15%29.aspx) структуры, который хранит описание часовой пояс, который используется при выборе время окончания встречи экземпляра или приглашения на собрание.</span><span class="sxs-lookup"><span data-stu-id="d88b2-105">Contains a stream that maps to the persisted format of a [TZDEFINITION](http://msdn.microsoft.com/library/0ae21571-2299-6407-807c-428668bb6798%28Office.15%29.aspx) structure, which stores the description for the time zone that is used when the end time of a single-instance appointment or meeting request is selected.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="d88b2-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="d88b2-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="d88b2-107">dispidApptTZDefEndDisplay</span><span class="sxs-lookup"><span data-stu-id="d88b2-107">dispidApptTZDefEndDisplay</span></span>  <br/> |
|<span data-ttu-id="d88b2-108">Набор свойств:</span><span class="sxs-lookup"><span data-stu-id="d88b2-108">Property set:</span></span>  <br/> |<span data-ttu-id="d88b2-109">PSETID_Appointment</span><span class="sxs-lookup"><span data-stu-id="d88b2-109">PSETID_Appointment</span></span>  <br/> |
|<span data-ttu-id="d88b2-110">Длинный идентификатор (КРЫШКА):</span><span class="sxs-lookup"><span data-stu-id="d88b2-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="d88b2-111">0x0000825F</span><span class="sxs-lookup"><span data-stu-id="d88b2-111">0x0000825F</span></span>  <br/> |
|<span data-ttu-id="d88b2-112">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="d88b2-112">Data type:</span></span>  <br/> |<span data-ttu-id="d88b2-113">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="d88b2-113">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="d88b2-114">Область:</span><span class="sxs-lookup"><span data-stu-id="d88b2-114">Area:</span></span>  <br/> |<span data-ttu-id="d88b2-115">Календарь</span><span class="sxs-lookup"><span data-stu-id="d88b2-115">Calendar</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d88b2-116">Замечания</span><span class="sxs-lookup"><span data-stu-id="d88b2-116">Remarks</span></span>

<span data-ttu-id="d88b2-117">Время начала и время окончания экземпляра хранилища Microsoft Office Outlook 2003 или более ранних версий и решения, основанные на объекты совместной работы (CDO) 1.2.1 и, не запускайте средство обновления календаря Outlook или Microsoft Exchange Server встречи и приглашения на собрания в формате UTC.</span><span class="sxs-lookup"><span data-stu-id="d88b2-117">Microsoft Office Outlook 2003 or earlier, and solutions that are based on Collaboration Data Objects (CDO) 1.2.1 and that have not run the calendar update tool for Outlook or Microsoft Exchange Server, store the start time and end time of single-instance appointments and meeting requests in Coordinated Universal Time (UTC).</span></span> <span data-ttu-id="d88b2-118">Эти клиенты не следует хранить какие-либо сведения для часового пояса, в котором создается встречи или приглашения на собрание.</span><span class="sxs-lookup"><span data-stu-id="d88b2-118">These clients do not store any information for the time zone where the appointment or meeting request is created.</span></span>
  
<span data-ttu-id="d88b2-119">Версии Microsoft Outlook, начиная с Microsoft Office Outlook 2007 и решения, основанные на CDO 1.2.1 (en), ранее выполненные календаря Outlook или Exchange Server обновление использования средства **dispidApptTZDefEndDisplay** для хранения часовой пояс времени окончания.</span><span class="sxs-lookup"><span data-stu-id="d88b2-119">Versions of Microsoft Outlook since Microsoft Office Outlook 2007, and solutions based on CDO 1.2.1 that have run the Outlook or Exchange Server calendar update tool use **dispidApptTZDefEndDisplay** to store the time zone for the end time.</span></span> <span data-ttu-id="d88b2-120">**dispidApptTZDefEndDisplay** показывает встречи или собрания в исходный часовой пояс, оно было запланировано и определяет корректировки время окончания при изменении правила часового пояса.</span><span class="sxs-lookup"><span data-stu-id="d88b2-120">**dispidApptTZDefEndDisplay** shows the appointment or meeting in the original time zone that it was scheduled, and determines whether the end time should be adjusted if the rules of the time zone change.</span></span> <span data-ttu-id="d88b2-121">Если это свойство не найден, используется часовой пояс, указанного в свойстве **dispidApptTZDefStartDisplay** ([PidLidAppointmentTimeZoneDefinitionStartDisplay](pidlidappointmenttimezonedefinitionstartdisplay-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="d88b2-121">If this property is missing, the time zone specified by the **dispidApptTZDefStartDisplay** ([PidLidAppointmentTimeZoneDefinitionStartDisplay](pidlidappointmenttimezonedefinitionstartdisplay-canonical-property.md)) property is used.</span></span> <span data-ttu-id="d88b2-122">Если **dispidApptTZDefStartDisplay** отсутствует или является недопустимым, используется значение текущего часового пояса.</span><span class="sxs-lookup"><span data-stu-id="d88b2-122">If **dispidApptTZDefStartDisplay** is missing or invalid, the current local time zone is assumed.</span></span> <span data-ttu-id="d88b2-123">**dispidApptTZDefEndDisplay** используется только для отображения и не используется в расширения повторения.</span><span class="sxs-lookup"><span data-stu-id="d88b2-123">**dispidApptTZDefEndDisplay** is used for display purposes only and is not used in recurrence expansion.</span></span> 
  
<span data-ttu-id="d88b2-124">Средство синтаксического анализа необходимо следить за тем, при считывании потока, полученный из **dispidApptTZDefEndDisplay**или для сохранения **TZDEFINITION** поток для, направленных на двоичного свойства, такие как **dispidApptTZDefEndDisplay**.</span><span class="sxs-lookup"><span data-stu-id="d88b2-124">A parser must be careful when it reads a stream obtained from **dispidApptTZDefEndDisplay**, or when it persists **TZDEFINITION** to a stream for commitment to a binary property such as **dispidApptTZDefEndDisplay**.</span></span> <span data-ttu-id="d88b2-125">Для получения дополнительных сведений см [Сохранение TZDEFINITION поток, чтобы зафиксировать двоичного свойства](http://msdn.microsoft.com/library/0dec535d-d48f-39a5-97d5-0bd109134b3b%28Office.15%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="d88b2-125">For more information, see [About persisting TZDEFINITION to a stream to commit to a binary property](http://msdn.microsoft.com/library/0dec535d-d48f-39a5-97d5-0bd109134b3b%28Office.15%29.aspx).</span></span>
  
 <span data-ttu-id="d88b2-126">**dispidApptTZDefEndDisplay** указывает часовой пояс информацию для свойства **dispidApptEndWhole** ([PidLidAppointmentEndWhole](pidlidappointmentendwhole-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="d88b2-126">**dispidApptTZDefEndDisplay** specifies time zone information for the **dispidApptEndWhole** ([PidLidAppointmentEndWhole](pidlidappointmentendwhole-canonical-property.md)) property.</span></span> <span data-ttu-id="d88b2-127">Формат, ограничений и вычисление **dispidApptTZDefEndDisplay** совпадают, указанный в свойстве **dispidApptTZDefStartDisplay** .</span><span class="sxs-lookup"><span data-stu-id="d88b2-127">The format, constraints, and computation of **dispidApptTZDefEndDisplay** are the same as specified in the **dispidApptTZDefStartDisplay** property.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="d88b2-128">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="d88b2-128">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="d88b2-129">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="d88b2-129">Protocol specifications</span></span>

<span data-ttu-id="d88b2-130">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="d88b2-130">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="d88b2-131">Содержит определения набора свойств и ссылки на связанные спецификаций протокола Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="d88b2-131">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="d88b2-132">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="d88b2-132">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="d88b2-133">Задает свойства и операции для встречи, приглашения на собрание и ответы.</span><span class="sxs-lookup"><span data-stu-id="d88b2-133">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="d88b2-134">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="d88b2-134">Header files</span></span>

<span data-ttu-id="d88b2-135">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="d88b2-135">Mapidefs.h</span></span>
  
> <span data-ttu-id="d88b2-136">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="d88b2-136">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="d88b2-137">См. также</span><span class="sxs-lookup"><span data-stu-id="d88b2-137">See also</span></span>



[<span data-ttu-id="d88b2-138">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="d88b2-138">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="d88b2-139">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="d88b2-139">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="d88b2-140">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="d88b2-140">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="d88b2-141">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="d88b2-141">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

