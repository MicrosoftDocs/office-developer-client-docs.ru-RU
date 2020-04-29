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
# <a name="pidlidappointmenttimezonedefinitionenddisplay-canonical-property"></a><span data-ttu-id="9d18e-103">Каноническое свойство PidLidAppointmentTimeZoneDefinitionEndDisplay</span><span class="sxs-lookup"><span data-stu-id="9d18e-103">PidLidAppointmentTimeZoneDefinitionEndDisplay Canonical Property</span></span>

  
  
<span data-ttu-id="9d18e-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9d18e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9d18e-105">Содержит поток, который сопоставляется с сохраненным форматом структуры [TZDEFINITION](https://msdn.microsoft.com/library/0ae21571-2299-6407-807c-428668bb6798%28Office.15%29.aspx) , в котором хранится описание для часового пояса, используемого при выборе времени окончания встречи с одним экземпляром или приглашения на собрание.</span><span class="sxs-lookup"><span data-stu-id="9d18e-105">Contains a stream that maps to the persisted format of a [TZDEFINITION](https://msdn.microsoft.com/library/0ae21571-2299-6407-807c-428668bb6798%28Office.15%29.aspx) structure, which stores the description for the time zone that is used when the end time of a single-instance appointment or meeting request is selected.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="9d18e-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="9d18e-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="9d18e-107">диспидаппттздефенддисплай</span><span class="sxs-lookup"><span data-stu-id="9d18e-107">dispidApptTZDefEndDisplay</span></span>  <br/> |
|<span data-ttu-id="9d18e-108">Набор свойств:</span><span class="sxs-lookup"><span data-stu-id="9d18e-108">Property set:</span></span>  <br/> |<span data-ttu-id="9d18e-109">PSETID_Appointment</span><span class="sxs-lookup"><span data-stu-id="9d18e-109">PSETID_Appointment</span></span>  <br/> |
|<span data-ttu-id="9d18e-110">Длинный идентификатор (крышка):</span><span class="sxs-lookup"><span data-stu-id="9d18e-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="9d18e-111">0x0000825F</span><span class="sxs-lookup"><span data-stu-id="9d18e-111">0x0000825F</span></span>  <br/> |
|<span data-ttu-id="9d18e-112">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="9d18e-112">Data type:</span></span>  <br/> |<span data-ttu-id="9d18e-113">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="9d18e-113">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="9d18e-114">Область:</span><span class="sxs-lookup"><span data-stu-id="9d18e-114">Area:</span></span>  <br/> |<span data-ttu-id="9d18e-115">Календарь</span><span class="sxs-lookup"><span data-stu-id="9d18e-115">Calendar</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="9d18e-116">Примечания</span><span class="sxs-lookup"><span data-stu-id="9d18e-116">Remarks</span></span>

<span data-ttu-id="9d18e-117">Microsoft Office Outlook 2003 или более ранней версии, а также решения, основанные на объектах данных совместной работы (CDO) 1.2.1 и не запускают средство обновления календаря для Outlook или Microsoft Exchange Server, сохраняют время начала и окончания встреч и приглашений на собрание в формате UTC.</span><span class="sxs-lookup"><span data-stu-id="9d18e-117">Microsoft Office Outlook 2003 or earlier, and solutions that are based on Collaboration Data Objects (CDO) 1.2.1 and that have not run the calendar update tool for Outlook or Microsoft Exchange Server, store the start time and end time of single-instance appointments and meeting requests in Coordinated Universal Time (UTC).</span></span> <span data-ttu-id="9d18e-118">Эти клиенты не хранят никакие сведения о часовом поясе, в котором создается приглашение на встречу или собрание.</span><span class="sxs-lookup"><span data-stu-id="9d18e-118">These clients do not store any information for the time zone where the appointment or meeting request is created.</span></span>
  
<span data-ttu-id="9d18e-119">Версии Microsoft Outlook с Microsoft Office Outlook 2007 и решения, основанные на CDO 1.2.1, на которых запущено средство обновления календаря Outlook или Exchange Server, используют **диспидаппттздефенддисплай** для хранения часового пояса времени окончания.</span><span class="sxs-lookup"><span data-stu-id="9d18e-119">Versions of Microsoft Outlook since Microsoft Office Outlook 2007, and solutions based on CDO 1.2.1 that have run the Outlook or Exchange Server calendar update tool use **dispidApptTZDefEndDisplay** to store the time zone for the end time.</span></span> <span data-ttu-id="9d18e-120">**диспидаппттздефенддисплай** показывает встречу или собрание в исходном часовом поясе, которое было запланировано, и определяет, следует ли корректировать время окончания при изменении правил в часовом поясе.</span><span class="sxs-lookup"><span data-stu-id="9d18e-120">**dispidApptTZDefEndDisplay** shows the appointment or meeting in the original time zone that it was scheduled, and determines whether the end time should be adjusted if the rules of the time zone change.</span></span> <span data-ttu-id="9d18e-121">Если это свойство отсутствует, используется часовой пояс, заданный свойством **диспидаппттздефстартдисплай** ([PidLidAppointmentTimeZoneDefinitionStartDisplay](pidlidappointmenttimezonedefinitionstartdisplay-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="9d18e-121">If this property is missing, the time zone specified by the **dispidApptTZDefStartDisplay** ([PidLidAppointmentTimeZoneDefinitionStartDisplay](pidlidappointmenttimezonedefinitionstartdisplay-canonical-property.md)) property is used.</span></span> <span data-ttu-id="9d18e-122">Если **диспидаппттздефстартдисплай** отсутствует или не является допустимым, подразумевается текущий местный часовой пояс.</span><span class="sxs-lookup"><span data-stu-id="9d18e-122">If **dispidApptTZDefStartDisplay** is missing or invalid, the current local time zone is assumed.</span></span> <span data-ttu-id="9d18e-123">**диспидаппттздефенддисплай** используется только для отображения и не используется в развертывании повторений.</span><span class="sxs-lookup"><span data-stu-id="9d18e-123">**dispidApptTZDefEndDisplay** is used for display purposes only and is not used in recurrence expansion.</span></span> 
  
<span data-ttu-id="9d18e-124">Синтаксический анализатор должен быть внимательным при чтении потока, полученного из **диспидаппттздефенддисплай**, или при сохранении **TZDEFINITION** в потоке для фиксации в двоичном свойстве, например **диспидаппттздефенддисплай**.</span><span class="sxs-lookup"><span data-stu-id="9d18e-124">A parser must be careful when it reads a stream obtained from **dispidApptTZDefEndDisplay**, or when it persists **TZDEFINITION** to a stream for commitment to a binary property such as **dispidApptTZDefEndDisplay**.</span></span> <span data-ttu-id="9d18e-125">Дополнительные сведения [о СОХРАНЕНИИ TZDEFINITION в потоке для фиксации в двоичном свойстве](https://msdn.microsoft.com/library/0dec535d-d48f-39a5-97d5-0bd109134b3b%28Office.15%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="9d18e-125">For more information, see [About persisting TZDEFINITION to a stream to commit to a binary property](https://msdn.microsoft.com/library/0dec535d-d48f-39a5-97d5-0bd109134b3b%28Office.15%29.aspx).</span></span>
  
 <span data-ttu-id="9d18e-126">**диспидаппттздефенддисплай** определяет сведения о часовом поясе для свойства **диспидапптендвхоле** ([PidLidAppointmentEndWhole](pidlidappointmentendwhole-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="9d18e-126">**dispidApptTZDefEndDisplay** specifies time zone information for the **dispidApptEndWhole** ([PidLidAppointmentEndWhole](pidlidappointmentendwhole-canonical-property.md)) property.</span></span> <span data-ttu-id="9d18e-127">Формат, ограничения и вычисление **диспидаппттздефенддисплай** совпадают с указанными в свойстве **диспидаппттздефстартдисплай** .</span><span class="sxs-lookup"><span data-stu-id="9d18e-127">The format, constraints, and computation of **dispidApptTZDefEndDisplay** are the same as specified in the **dispidApptTZDefStartDisplay** property.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="9d18e-128">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="9d18e-128">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="9d18e-129">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="9d18e-129">Protocol specifications</span></span>

<span data-ttu-id="9d18e-130">[[MS — ОКСПРОПС]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="9d18e-130">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="9d18e-131">Содержит определения свойств и ссылки на связанные спецификации протокола Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="9d18e-131">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="9d18e-132">[[MS — ОКСОКАЛ]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="9d18e-132">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="9d18e-133">Задает свойства и операции для встречи, приглашения на собрание и ответных сообщений.</span><span class="sxs-lookup"><span data-stu-id="9d18e-133">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="9d18e-134">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="9d18e-134">Header files</span></span>

<span data-ttu-id="9d18e-135">MAPIDEFS. h</span><span class="sxs-lookup"><span data-stu-id="9d18e-135">Mapidefs.h</span></span>
  
> <span data-ttu-id="9d18e-136">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="9d18e-136">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="9d18e-137">См. также</span><span class="sxs-lookup"><span data-stu-id="9d18e-137">See also</span></span>



[<span data-ttu-id="9d18e-138">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="9d18e-138">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="9d18e-139">Каноническое свойство MAPI</span><span class="sxs-lookup"><span data-stu-id="9d18e-139">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="9d18e-140">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="9d18e-140">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="9d18e-141">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="9d18e-141">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

