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
# <a name="pidlidappointmenttimezonedefinitionrecur-canonical-property"></a><span data-ttu-id="b7157-103">Каноническое свойство PidLidAppointmentTimeZoneDefinitionRecur</span><span class="sxs-lookup"><span data-stu-id="b7157-103">PidLidAppointmentTimeZoneDefinitionRecur Canonical Property</span></span>

  
  
<span data-ttu-id="b7157-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b7157-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b7157-105">Содержит поток, который сополагается с постоянным форматом структуры [TZDEFINITION,](https://msdn.microsoft.com/library/0ae21571-2299-6407-807c-428668bb6798%28Office.15%29.aspx) в котором хранится описание часового пояса, используемого при составлении повторяющейся встречи или запроса на собрание.</span><span class="sxs-lookup"><span data-stu-id="b7157-105">Contains a stream that maps to the persisted format of a [TZDEFINITION](https://msdn.microsoft.com/library/0ae21571-2299-6407-807c-428668bb6798%28Office.15%29.aspx) structure, which stores the description for the time zone that is used when a recurring appointment or meeting request is created.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="b7157-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="b7157-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="b7157-107">dispidApptTZDefRecur</span><span class="sxs-lookup"><span data-stu-id="b7157-107">dispidApptTZDefRecur</span></span>  <br/> |
|<span data-ttu-id="b7157-108">Набор свойств:</span><span class="sxs-lookup"><span data-stu-id="b7157-108">Property set:</span></span>  <br/> |<span data-ttu-id="b7157-109">PSETID_Appointment</span><span class="sxs-lookup"><span data-stu-id="b7157-109">PSETID_Appointment</span></span>  <br/> |
|<span data-ttu-id="b7157-110">Длинный ИД (КРЫШКА):</span><span class="sxs-lookup"><span data-stu-id="b7157-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="b7157-111">0x00008260</span><span class="sxs-lookup"><span data-stu-id="b7157-111">0x00008260</span></span>  <br/> |
|<span data-ttu-id="b7157-112">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="b7157-112">Data type:</span></span>  <br/> |<span data-ttu-id="b7157-113">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="b7157-113">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="b7157-114">Область:</span><span class="sxs-lookup"><span data-stu-id="b7157-114">Area:</span></span>  <br/> |<span data-ttu-id="b7157-115">Календарь</span><span class="sxs-lookup"><span data-stu-id="b7157-115">Calendar</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b7157-116">Примечания</span><span class="sxs-lookup"><span data-stu-id="b7157-116">Remarks</span></span>

<span data-ttu-id="b7157-117">Версии Microsoft Outlook с Microsoft Office Outlook 2007 г., а также решения на основе объектов данных совместной работы (CDO) 1.2.1, которые запускали средство обновления календаря Outlook или Exchange Server, используют свойства **dispidApptTZDefRecur** и **dispidTimeZoneStruct** [(PidLidTimeZoneStruct),](pidlidtimezonestruct-canonical-property.md)чтобы определить, следует ли корректировать повторяющееся собрание при изменении правил часового пояса.</span><span class="sxs-lookup"><span data-stu-id="b7157-117">Versions of Microsoft Outlook since Microsoft Office Outlook 2007, and solutions based on Collaboration Data Objects (CDO) 1.2.1 that have run the Outlook or Exchange Server calendar update tool use the **dispidApptTZDefRecur** and **dispidTimeZoneStruct** ([PidLidTimeZoneStruct](pidlidtimezonestruct-canonical-property.md)) properties to determine whether the recurring meeting should be adjusted if the rules of the time zone change.</span></span> <span data-ttu-id="b7157-118">Эти свойства необходимо синхронизировать, так как старые клиенты по-прежнему могут управлять **свойством dispidTimeZoneStruct.**</span><span class="sxs-lookup"><span data-stu-id="b7157-118">These properties must be synchronized, because older clients may still manipulate the **dispidTimeZoneStruct** property.</span></span> <span data-ttu-id="b7157-119">Чтобы определить, синхронизируются ли два свойства, член **wFlags** для правила, которое соответствует **dispidTimeZoneStruct,** должен иметь TZRULE_FLAG_RECUR_CURRENT_TZREG флага.</span><span class="sxs-lookup"><span data-stu-id="b7157-119">To detect whether the two properties are synchronized, the **wFlags** member for the rule that matches **dispidTimeZoneStruct** should have the TZRULE_FLAG_RECUR_CURRENT_TZREG flag set.</span></span> <span data-ttu-id="b7157-120">Если этот флаг не установлен или установлен, а правило в свойстве **dispidTimeZoneStruct** не соответствует помеченным правилу, следует отменить свойство **dispidApptTZDefRecur,** а вместо него использовать **dispidTimeZoneStruct.**</span><span class="sxs-lookup"><span data-stu-id="b7157-120">If this flag is not set, or it is set and the rule in the **dispidTimeZoneStruct** property does not match the marked rule, the **dispidApptTZDefRecur** property should be discarded and **dispidTimeZoneStruct** should be used instead.</span></span> 
  
<span data-ttu-id="b7157-121">При записи свойств **dispidApptTZDefRecur** и **dispidTimeZoneStruct** в новое повторяющееся собрание или при произвольном выборе использования свойства **dispidTimeZoneStruct** необходимо использовать текущее определение часового пояса (в соответствии с реестром Windows).</span><span class="sxs-lookup"><span data-stu-id="b7157-121">When you write both the **dispidApptTZDefRecur** and **dispidTimeZoneStruct** properties to a new recurring meeting, or, when you make an arbitrary choice to use the **dispidTimeZoneStruct** property, the current definition for the time zone (according to the Windows registry) should be used.</span></span> 
  
<span data-ttu-id="b7157-122">Разбор должен быть осторожным при считывате потоке, полученном от **dispidApptTZDefRecur,** или при сохраняемом **TZDEFINITION** в потоке для обязательства перед двоичным свойством, таким как **dispidApptTZDefRecur.**</span><span class="sxs-lookup"><span data-stu-id="b7157-122">A parser must be careful when it reads a stream that is obtained from **dispidApptTZDefRecur**, or when it persists **TZDEFINITION** to a stream for commitment to a binary property such as **dispidApptTZDefRecur**.</span></span> <span data-ttu-id="b7157-123">Дополнительные сведения см. в [разделах о том, как сохранить TZDEFINITION](https://msdn.microsoft.com/library/0dec535d-d48f-39a5-97d5-0bd109134b3b%28Office.15%29.aspx)в потоке для фиксации двоичного свойства.</span><span class="sxs-lookup"><span data-stu-id="b7157-123">For more information, see [About persisting TZDEFINITION to a stream to commit to a binary property](https://msdn.microsoft.com/library/0dec535d-d48f-39a5-97d5-0bd109134b3b%28Office.15%29.aspx).</span></span>
  
 <span data-ttu-id="b7157-124">**dispidApptTZDefRecur** указывает сведения о часовом поясе, который описывает преобразование даты и времени собрания в повторяющийся ряд в UTC и из него.</span><span class="sxs-lookup"><span data-stu-id="b7157-124">**dispidApptTZDefRecur** specifies time zone information that describes how to convert the meeting date and time on a recurring series to and from Coordinated Universal Time (UTC).</span></span> <span data-ttu-id="b7157-125">Если это свойство установлено, но имеет данные, несогласованные с данными, представленными **dispidTimeZoneStruct,** клиент должен использовать **dispidTimeZoneStruct** вместо **dispidApptTZDefRecur.**</span><span class="sxs-lookup"><span data-stu-id="b7157-125">If this property is set but it has data that is inconsistent with the data represented by **dispidTimeZoneStruct**, the client must use **dispidTimeZoneStruct** instead of **dispidApptTZDefRecur**.</span></span> <span data-ttu-id="b7157-126">Если **dispidApptTZDefRecur** не установлен, будет использоваться свойство **PidLidTimeZoneStruct.**</span><span class="sxs-lookup"><span data-stu-id="b7157-126">If **dispidApptTZDefRecur** is not set, the **PidLidTimeZoneStruct** property will be used instead.</span></span> <span data-ttu-id="b7157-127">Поля в этом BLOB-проекте кодируются в порядок с небольшими конечнымибами.</span><span class="sxs-lookup"><span data-stu-id="b7157-127">The fields in this BLOB are encoded in little-endian byte order.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="b7157-128">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="b7157-128">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="b7157-129">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="b7157-129">Protocol specifications</span></span>

<span data-ttu-id="b7157-130">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="b7157-130">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="b7157-131">Предоставляет определения набора свойств и ссылки на связанные Exchange Server спецификации протокола.</span><span class="sxs-lookup"><span data-stu-id="b7157-131">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="b7157-132">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="b7157-132">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="b7157-133">Указывает свойства и операции для встреч, запросов на собрание и ответных сообщений.</span><span class="sxs-lookup"><span data-stu-id="b7157-133">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="b7157-134">Файлы заголовок</span><span class="sxs-lookup"><span data-stu-id="b7157-134">Header files</span></span>

<span data-ttu-id="b7157-135">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="b7157-135">Mapidefs.h</span></span>
  
> <span data-ttu-id="b7157-136">Предоставляет определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="b7157-136">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="b7157-137">См. также</span><span class="sxs-lookup"><span data-stu-id="b7157-137">See also</span></span>



[<span data-ttu-id="b7157-138">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="b7157-138">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="b7157-139">Канонические свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="b7157-139">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="b7157-140">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="b7157-140">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="b7157-141">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="b7157-141">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

