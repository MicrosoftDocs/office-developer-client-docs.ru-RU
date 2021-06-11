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
ms.openlocfilehash: e5e9b06178a1517fc1c8652b0d667faf1afc77cc
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32345355"
---
# <a name="pidlidappointmenttimezonedefinitionrecur-canonical-property"></a><span data-ttu-id="d13bf-103">Каноническое свойство PidLidAppointmentTimeZoneDefinitionRecur</span><span class="sxs-lookup"><span data-stu-id="d13bf-103">PidLidAppointmentTimeZoneDefinitionRecur Canonical Property</span></span>

  
  
<span data-ttu-id="d13bf-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d13bf-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d13bf-105">Содержит поток, который совмещая сохраняемого формата структуры [TZDEFINITION,](https://msdn.microsoft.com/library/0ae21571-2299-6407-807c-428668bb6798%28Office.15%29.aspx) в котором хранится описание часового пояса, используемого при повторном назначении или запросе на собрание.</span><span class="sxs-lookup"><span data-stu-id="d13bf-105">Contains a stream that maps to the persisted format of a [TZDEFINITION](https://msdn.microsoft.com/library/0ae21571-2299-6407-807c-428668bb6798%28Office.15%29.aspx) structure, which stores the description for the time zone that is used when a recurring appointment or meeting request is created.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="d13bf-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="d13bf-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="d13bf-107">dispidApptTZDefRecur</span><span class="sxs-lookup"><span data-stu-id="d13bf-107">dispidApptTZDefRecur</span></span>  <br/> |
|<span data-ttu-id="d13bf-108">Набор свойств:</span><span class="sxs-lookup"><span data-stu-id="d13bf-108">Property set:</span></span>  <br/> |<span data-ttu-id="d13bf-109">PSETID_Appointment</span><span class="sxs-lookup"><span data-stu-id="d13bf-109">PSETID_Appointment</span></span>  <br/> |
|<span data-ttu-id="d13bf-110">Long ID (LID):</span><span class="sxs-lookup"><span data-stu-id="d13bf-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="d13bf-111">0x00008260</span><span class="sxs-lookup"><span data-stu-id="d13bf-111">0x00008260</span></span>  <br/> |
|<span data-ttu-id="d13bf-112">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="d13bf-112">Data type:</span></span>  <br/> |<span data-ttu-id="d13bf-113">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="d13bf-113">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="d13bf-114">Область:</span><span class="sxs-lookup"><span data-stu-id="d13bf-114">Area:</span></span>  <br/> |<span data-ttu-id="d13bf-115">Календарь</span><span class="sxs-lookup"><span data-stu-id="d13bf-115">Calendar</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d13bf-116">Примечания</span><span class="sxs-lookup"><span data-stu-id="d13bf-116">Remarks</span></span>

<span data-ttu-id="d13bf-117">Версии Microsoft Outlook с Microsoft Office Outlook 2007 г. и решения на основе объектов данных совместной работы (CDO) 1.2.1, которые запускали средство обновления Outlook или Exchange Server календаря, используют **dispidApptTZDefRecur** и **dispidTimeZoneStruct** [(PidLidTimeZoneStruct),](pidlidtimezonestruct-canonical-property.md)чтобы определить, следует ли корректировать повторяющиеся собрания, если правила часового пояса изменятся.</span><span class="sxs-lookup"><span data-stu-id="d13bf-117">Versions of Microsoft Outlook since Microsoft Office Outlook 2007, and solutions based on Collaboration Data Objects (CDO) 1.2.1 that have run the Outlook or Exchange Server calendar update tool use the **dispidApptTZDefRecur** and **dispidTimeZoneStruct** ([PidLidTimeZoneStruct](pidlidtimezonestruct-canonical-property.md)) properties to determine whether the recurring meeting should be adjusted if the rules of the time zone change.</span></span> <span data-ttu-id="d13bf-118">Эти свойства необходимо синхронизировать, так как более старые клиенты по-прежнему могут манипулировать **свойством dispidTimeZoneStruct.**</span><span class="sxs-lookup"><span data-stu-id="d13bf-118">These properties must be synchronized, because older clients may still manipulate the **dispidTimeZoneStruct** property.</span></span> <span data-ttu-id="d13bf-119">Чтобы определить, синхронизированы ли эти два свойства, участник **wFlags** для правила, которое совпадает с **dispidTimeZoneStruct,** должен иметь TZRULE_FLAG_RECUR_CURRENT_TZREG флага.</span><span class="sxs-lookup"><span data-stu-id="d13bf-119">To detect whether the two properties are synchronized, the **wFlags** member for the rule that matches **dispidTimeZoneStruct** should have the TZRULE_FLAG_RECUR_CURRENT_TZREG flag set.</span></span> <span data-ttu-id="d13bf-120">Если этот флаг не установлен или установлен, а правило в свойстве dispidTimeZoneStruct не совпадает с отмеченным правилом, свойство **dispidApptTZDefRecur** должно быть отброшено и вместо него следует использовать **dispidTimeZoneStruct.** </span><span class="sxs-lookup"><span data-stu-id="d13bf-120">If this flag is not set, or it is set and the rule in the **dispidTimeZoneStruct** property does not match the marked rule, the **dispidApptTZDefRecur** property should be discarded and **dispidTimeZoneStruct** should be used instead.</span></span> 
  
<span data-ttu-id="d13bf-121">При записи свойств **dispidApptTZDefRecur** и **dispidTimeZoneStruct** на новое повторяющееся собрание или при произвольном выборе использования свойства **dispidTimeZoneStruct** необходимо использовать текущее определение часового пояса (согласно реестру Windows).</span><span class="sxs-lookup"><span data-stu-id="d13bf-121">When you write both the **dispidApptTZDefRecur** and **dispidTimeZoneStruct** properties to a new recurring meeting, or, when you make an arbitrary choice to use the **dispidTimeZoneStruct** property, the current definition for the time zone (according to the Windows registry) should be used.</span></span> 
  
<span data-ttu-id="d13bf-122">Разборщик должен быть осторожным, когда он читает поток, полученный из **dispidApptTZDefRecur**, или когда он **сохраняется TZDEFINITION** в поток для обязательств к двоичному свойству, например **dispidApptTZDefRecur**.</span><span class="sxs-lookup"><span data-stu-id="d13bf-122">A parser must be careful when it reads a stream that is obtained from **dispidApptTZDefRecur**, or when it persists **TZDEFINITION** to a stream for commitment to a binary property such as **dispidApptTZDefRecur**.</span></span> <span data-ttu-id="d13bf-123">Дополнительные сведения см. в разделах О сохраняющихся [TZDEFINITION](https://msdn.microsoft.com/library/0dec535d-d48f-39a5-97d5-0bd109134b3b%28Office.15%29.aspx)в потоке для фиксации двоичного свойства.</span><span class="sxs-lookup"><span data-stu-id="d13bf-123">For more information, see [About persisting TZDEFINITION to a stream to commit to a binary property](https://msdn.microsoft.com/library/0dec535d-d48f-39a5-97d5-0bd109134b3b%28Office.15%29.aspx).</span></span>
  
 <span data-ttu-id="d13bf-124">**dispidApptTZDefRecur** указывает сведения часового пояса, описывающие, как преобразовать дату и время собрания в повторяющейся серии в скоординированное универсальное время (UTC) и из него.</span><span class="sxs-lookup"><span data-stu-id="d13bf-124">**dispidApptTZDefRecur** specifies time zone information that describes how to convert the meeting date and time on a recurring series to and from Coordinated Universal Time (UTC).</span></span> <span data-ttu-id="d13bf-125">Если это свойство заданной, но оно имеет данные, несовместимые с данными, представленными **dispidTimeZoneStruct,** клиент должен использовать **dispidTimeZoneStruct** вместо **dispidApptTZDefRecur**.</span><span class="sxs-lookup"><span data-stu-id="d13bf-125">If this property is set but it has data that is inconsistent with the data represented by **dispidTimeZoneStruct**, the client must use **dispidTimeZoneStruct** instead of **dispidApptTZDefRecur**.</span></span> <span data-ttu-id="d13bf-126">Если **не установлено dispidApptTZDefRecur,** вместо этого будет использоваться свойство **PidLidTimeZoneStruct.**</span><span class="sxs-lookup"><span data-stu-id="d13bf-126">If **dispidApptTZDefRecur** is not set, the **PidLidTimeZoneStruct** property will be used instead.</span></span> <span data-ttu-id="d13bf-127">Поля в этом BLOB закодированы в порядке мало-endian byte.</span><span class="sxs-lookup"><span data-stu-id="d13bf-127">The fields in this BLOB are encoded in little-endian byte order.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="d13bf-128">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="d13bf-128">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="d13bf-129">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="d13bf-129">Protocol specifications</span></span>

<span data-ttu-id="d13bf-130">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="d13bf-130">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="d13bf-131">Предоставляет определения набора свойств и ссылки на связанные Exchange Server протоколы.</span><span class="sxs-lookup"><span data-stu-id="d13bf-131">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="d13bf-132">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="d13bf-132">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="d13bf-133">Указывает свойства и операции для встреч, запросов на собрания и ответных сообщений.</span><span class="sxs-lookup"><span data-stu-id="d13bf-133">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="d13bf-134">Файлы заголовки</span><span class="sxs-lookup"><span data-stu-id="d13bf-134">Header files</span></span>

<span data-ttu-id="d13bf-135">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="d13bf-135">Mapidefs.h</span></span>
  
> <span data-ttu-id="d13bf-136">Предоставляет определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="d13bf-136">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="d13bf-137">См. также</span><span class="sxs-lookup"><span data-stu-id="d13bf-137">See also</span></span>



[<span data-ttu-id="d13bf-138">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="d13bf-138">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="d13bf-139">Канонические свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="d13bf-139">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="d13bf-140">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="d13bf-140">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="d13bf-141">Сопоставление имен MAPI с каноническими именами свойств</span><span class="sxs-lookup"><span data-stu-id="d13bf-141">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

