---
title: Каноническое свойство PidLidAppointmentTimeZoneDefinitionRecur
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidAppointmentTimeZoneDefinitionRecur
api_type:
- COM
ms.assetid: 52fd57a0-9e34-4452-9ecd-2acb454446c9
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 5cff6ec7b39c26eec098d250688d98bf1e4799ea
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19810214"
---
# <a name="pidlidappointmenttimezonedefinitionrecur-canonical-property"></a><span data-ttu-id="c0c03-103">Каноническое свойство PidLidAppointmentTimeZoneDefinitionRecur</span><span class="sxs-lookup"><span data-stu-id="c0c03-103">PidLidAppointmentTimeZoneDefinitionRecur Canonical Property</span></span>

  
  
<span data-ttu-id="c0c03-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="c0c03-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="c0c03-105">Содержит поток, который соответствует сохраненного формата [TZDEFINITION](http://msdn.microsoft.com/library/0ae21571-2299-6407-807c-428668bb6798%28Office.15%29.aspx) структуры, который хранит описание часовой пояс, который используется при создании повторяющейся встречи или приглашения на собрание.</span><span class="sxs-lookup"><span data-stu-id="c0c03-105">Contains a stream that maps to the persisted format of a [TZDEFINITION](http://msdn.microsoft.com/library/0ae21571-2299-6407-807c-428668bb6798%28Office.15%29.aspx) structure, which stores the description for the time zone that is used when a recurring appointment or meeting request is created.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="c0c03-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="c0c03-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="c0c03-107">dispidApptTZDefRecur</span><span class="sxs-lookup"><span data-stu-id="c0c03-107">dispidApptTZDefRecur</span></span>  <br/> |
|<span data-ttu-id="c0c03-108">Набор свойств:</span><span class="sxs-lookup"><span data-stu-id="c0c03-108">Property set:</span></span>  <br/> |<span data-ttu-id="c0c03-109">PSETID_Appointment</span><span class="sxs-lookup"><span data-stu-id="c0c03-109">PSETID_Appointment</span></span>  <br/> |
|<span data-ttu-id="c0c03-110">Длинный идентификатор (КРЫШКА):</span><span class="sxs-lookup"><span data-stu-id="c0c03-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="c0c03-111">0x00008260</span><span class="sxs-lookup"><span data-stu-id="c0c03-111">0x00008260</span></span>  <br/> |
|<span data-ttu-id="c0c03-112">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="c0c03-112">Data type:</span></span>  <br/> |<span data-ttu-id="c0c03-113">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="c0c03-113">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="c0c03-114">Область:</span><span class="sxs-lookup"><span data-stu-id="c0c03-114">Area:</span></span>  <br/> |<span data-ttu-id="c0c03-115">Календарь</span><span class="sxs-lookup"><span data-stu-id="c0c03-115">Calendar</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c0c03-116">Замечания</span><span class="sxs-lookup"><span data-stu-id="c0c03-116">Remarks</span></span>

<span data-ttu-id="c0c03-117">Используйте средство **dispidApptTZDefRecur** и **обновление для систем Microsoft Outlook, начиная с Microsoft Office Outlook 2007 и решения, основанные на объекты совместной работы (CDO) 1.2.1 (en), ранее выполненные календаря Outlook или Exchange Server dispidTimeZoneStruct** ([PidLidTimeZoneStruct](pidlidtimezonestruct-canonical-property.md)) свойства, чтобы определить, должны быть настроены повторяющееся собрание, при изменении правила часового пояса.</span><span class="sxs-lookup"><span data-stu-id="c0c03-117">Versions of Microsoft Outlook since Microsoft Office Outlook 2007, and solutions based on Collaboration Data Objects (CDO) 1.2.1 that have run the Outlook or Exchange Server calendar update tool use the **dispidApptTZDefRecur** and **dispidTimeZoneStruct** ([PidLidTimeZoneStruct](pidlidtimezonestruct-canonical-property.md)) properties to determine whether the recurring meeting should be adjusted if the rules of the time zone change.</span></span> <span data-ttu-id="c0c03-118">Эти свойства должны быть синхронизированы, так как старых клиентов по-прежнему могут изменить значение свойства **dispidTimeZoneStruct** .</span><span class="sxs-lookup"><span data-stu-id="c0c03-118">These properties must be synchronized, because older clients may still manipulate the **dispidTimeZoneStruct** property.</span></span> <span data-ttu-id="c0c03-119">Для обнаружения синхронизированных два свойства члена **wFlags** для правила, которая соответствует **dispidTimeZoneStruct** наличие флаг TZRULE_FLAG_RECUR_CURRENT_TZREG.</span><span class="sxs-lookup"><span data-stu-id="c0c03-119">To detect whether the two properties are synchronized, the **wFlags** member for the rule that matches **dispidTimeZoneStruct** should have the TZRULE_FLAG_RECUR_CURRENT_TZREG flag set.</span></span> <span data-ttu-id="c0c03-120">Если этот флаг не установлен, или оно установлено и правила в свойстве **dispidTimeZoneStruct** не соответствует помеченные правило, не следует использовать свойство **dispidApptTZDefRecur** и **dispidTimeZoneStruct** следует использовать вместо этого.</span><span class="sxs-lookup"><span data-stu-id="c0c03-120">If this flag is not set, or it is set and the rule in the **dispidTimeZoneStruct** property does not match the marked rule, the **dispidApptTZDefRecur** property should be discarded and **dispidTimeZoneStruct** should be used instead.</span></span> 
  
<span data-ttu-id="c0c03-121">При создании свойства **dispidApptTZDefRecur** и **dispidTimeZoneStruct** новое повторяющееся собрание, или, если сделать произвольный выбор с помощью свойства **dispidTimeZoneStruct** текущего определения часового пояса ( в соответствии с реестра Windows) следует использовать.</span><span class="sxs-lookup"><span data-stu-id="c0c03-121">When you write both the **dispidApptTZDefRecur** and **dispidTimeZoneStruct** properties to a new recurring meeting, or, when you make an arbitrary choice to use the **dispidTimeZoneStruct** property, the current definition for the time zone (according to the Windows registry) should be used.</span></span> 
  
<span data-ttu-id="c0c03-122">Средство синтаксического анализа необходимо следить за тем, при считывании поток, полученную из **dispidApptTZDefRecur**или для сохранения **TZDEFINITION** поток для, направленных на двоичного свойства, такие как **dispidApptTZDefRecur**.</span><span class="sxs-lookup"><span data-stu-id="c0c03-122">A parser must be careful when it reads a stream that is obtained from **dispidApptTZDefRecur**, or when it persists **TZDEFINITION** to a stream for commitment to a binary property such as **dispidApptTZDefRecur**.</span></span> <span data-ttu-id="c0c03-123">Для получения дополнительных сведений см [Сохранение TZDEFINITION поток, чтобы зафиксировать двоичного свойства](http://msdn.microsoft.com/library/0dec535d-d48f-39a5-97d5-0bd109134b3b%28Office.15%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="c0c03-123">For more information, see [About persisting TZDEFINITION to a stream to commit to a binary property](http://msdn.microsoft.com/library/0dec535d-d48f-39a5-97d5-0bd109134b3b%28Office.15%29.aspx).</span></span>
  
 <span data-ttu-id="c0c03-124">**dispidApptTZDefRecur** указывает сведения часового пояса, описывающая способ преобразования собрания даты и времени на серии повторяющихся и в формате UTC.</span><span class="sxs-lookup"><span data-stu-id="c0c03-124">**dispidApptTZDefRecur** specifies time zone information that describes how to convert the meeting date and time on a recurring series to and from Coordinated Universal Time (UTC).</span></span> <span data-ttu-id="c0c03-125">Если задано это свойство, но он содержит данные, не соответствует данных, представленному **dispidTimeZoneStruct**, клиент должен использовать **dispidTimeZoneStruct** вместо **dispidApptTZDefRecur**.</span><span class="sxs-lookup"><span data-stu-id="c0c03-125">If this property is set but it has data that is inconsistent with the data represented by **dispidTimeZoneStruct**, the client must use **dispidTimeZoneStruct** instead of **dispidApptTZDefRecur**.</span></span> <span data-ttu-id="c0c03-126">Если **dispidApptTZDefRecur** не задано, будет использоваться свойство **PidLidTimeZoneStruct** .</span><span class="sxs-lookup"><span data-stu-id="c0c03-126">If **dispidApptTZDefRecur** is not set, the **PidLidTimeZoneStruct** property will be used instead.</span></span> <span data-ttu-id="c0c03-127">Поля в этом больших двоичных ОБЪЕКТОВ, помеченные в байтовом формате с прямым.</span><span class="sxs-lookup"><span data-stu-id="c0c03-127">The fields in this BLOB are encoded in little-endian byte order.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="c0c03-128">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="c0c03-128">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="c0c03-129">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="c0c03-129">Protocol specifications</span></span>

<span data-ttu-id="c0c03-130">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c0c03-130">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c0c03-131">Содержит определения набора свойств и ссылки на связанные спецификаций протокола Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="c0c03-131">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="c0c03-132">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c0c03-132">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c0c03-133">Задает свойства и операции для встречи, приглашения на собрание и ответы.</span><span class="sxs-lookup"><span data-stu-id="c0c03-133">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="c0c03-134">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="c0c03-134">Header files</span></span>

<span data-ttu-id="c0c03-135">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="c0c03-135">Mapidefs.h</span></span>
  
> <span data-ttu-id="c0c03-136">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="c0c03-136">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="c0c03-137">См. также</span><span class="sxs-lookup"><span data-stu-id="c0c03-137">See also</span></span>



[<span data-ttu-id="c0c03-138">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="c0c03-138">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="c0c03-139">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="c0c03-139">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="c0c03-140">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="c0c03-140">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="c0c03-141">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="c0c03-141">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

