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
# <a name="pidlidappointmenttimezonedefinitionrecur-canonical-property"></a><span data-ttu-id="759b2-103">Каноническое свойство PidLidAppointmentTimeZoneDefinitionRecur</span><span class="sxs-lookup"><span data-stu-id="759b2-103">PidLidAppointmentTimeZoneDefinitionRecur Canonical Property</span></span>

  
  
<span data-ttu-id="759b2-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="759b2-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="759b2-105">Содержит поток, который сопоставляется с сохраненным форматом структуры [TZDEFINITION](https://msdn.microsoft.com/library/0ae21571-2299-6407-807c-428668bb6798%28Office.15%29.aspx) , в котором хранятся описания для часового пояса, используемого при создании повторяющейся встречи или приглашения на собрание.</span><span class="sxs-lookup"><span data-stu-id="759b2-105">Contains a stream that maps to the persisted format of a [TZDEFINITION](https://msdn.microsoft.com/library/0ae21571-2299-6407-807c-428668bb6798%28Office.15%29.aspx) structure, which stores the description for the time zone that is used when a recurring appointment or meeting request is created.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="759b2-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="759b2-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="759b2-107">Диспидаппттздефрекур</span><span class="sxs-lookup"><span data-stu-id="759b2-107">dispidApptTZDefRecur</span></span>  <br/> |
|<span data-ttu-id="759b2-108">Набор свойств:</span><span class="sxs-lookup"><span data-stu-id="759b2-108">Property set:</span></span>  <br/> |<span data-ttu-id="759b2-109">Псетид_аппоинтмент</span><span class="sxs-lookup"><span data-stu-id="759b2-109">PSETID_Appointment</span></span>  <br/> |
|<span data-ttu-id="759b2-110">Длинный идентификатор (крышка):</span><span class="sxs-lookup"><span data-stu-id="759b2-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="759b2-111">0x00008260</span><span class="sxs-lookup"><span data-stu-id="759b2-111">0x00008260</span></span>  <br/> |
|<span data-ttu-id="759b2-112">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="759b2-112">Data type:</span></span>  <br/> |<span data-ttu-id="759b2-113">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="759b2-113">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="759b2-114">Область:</span><span class="sxs-lookup"><span data-stu-id="759b2-114">Area:</span></span>  <br/> |<span data-ttu-id="759b2-115">Календарь</span><span class="sxs-lookup"><span data-stu-id="759b2-115">Calendar</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="759b2-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="759b2-116">Remarks</span></span>

<span data-ttu-id="759b2-117">Версии Microsoft Outlook с Microsoft Office Outlook 2007 и решения на основе объектов данных совместной работы (CDO) 1.2.1, на которых запущено средство обновления календаря Outlook или Exchange Server, используйте **диспидаппттздефрекур** и \*\* свойства Диспидтимезонеструкт\*\* ([PidLidTimeZoneStruct](pidlidtimezonestruct-canonical-property.md)), чтобы определить, следует ли корректировать повторяющееся собрание при изменении правил часового пояса.</span><span class="sxs-lookup"><span data-stu-id="759b2-117">Versions of Microsoft Outlook since Microsoft Office Outlook 2007, and solutions based on Collaboration Data Objects (CDO) 1.2.1 that have run the Outlook or Exchange Server calendar update tool use the **dispidApptTZDefRecur** and **dispidTimeZoneStruct** ([PidLidTimeZoneStruct](pidlidtimezonestruct-canonical-property.md)) properties to determine whether the recurring meeting should be adjusted if the rules of the time zone change.</span></span> <span data-ttu-id="759b2-118">Эти свойства должны быть синхронизированы, так как старые клиенты все еще могут управлять свойством **диспидтимезонеструкт** .</span><span class="sxs-lookup"><span data-stu-id="759b2-118">These properties must be synchronized, because older clients may still manipulate the **dispidTimeZoneStruct** property.</span></span> <span data-ttu-id="759b2-119">Чтобы определить, синхронизированы ли два свойства, элемент **вфлагс** для правила, который соответствует **диспидтимезонеструкт** , должен иметь установленный флаг тзруле_флаг_рекур_куррент_тзрег.</span><span class="sxs-lookup"><span data-stu-id="759b2-119">To detect whether the two properties are synchronized, the **wFlags** member for the rule that matches **dispidTimeZoneStruct** should have the TZRULE_FLAG_RECUR_CURRENT_TZREG flag set.</span></span> <span data-ttu-id="759b2-120">Если этот флаг не задан или задано, а правило в свойстве **диспидтимезонеструкт** не отвечает отмеченному правилу, свойство **диспидаппттздефрекур** должно быть удалено, а вместо этого должно использоваться **диспидтимезонеструкт** .</span><span class="sxs-lookup"><span data-stu-id="759b2-120">If this flag is not set, or it is set and the rule in the **dispidTimeZoneStruct** property does not match the marked rule, the **dispidApptTZDefRecur** property should be discarded and **dispidTimeZoneStruct** should be used instead.</span></span> 
  
<span data-ttu-id="759b2-121">Когда вы записываете свойства **диспидаппттздефрекур** и **диспидтимезонеструкт** в новое повторяющееся собрание или при произвольном выборе для использования свойства **диспидтимезонеструкт** текущее определение для часового пояса ( в соответствии с реестром Windows) следует использовать.</span><span class="sxs-lookup"><span data-stu-id="759b2-121">When you write both the **dispidApptTZDefRecur** and **dispidTimeZoneStruct** properties to a new recurring meeting, or, when you make an arbitrary choice to use the **dispidTimeZoneStruct** property, the current definition for the time zone (according to the Windows registry) should be used.</span></span> 
  
<span data-ttu-id="759b2-122">Синтаксический анализатор должен быть внимательным при чтении потока, полученного из **диспидаппттздефрекур**, или при сохранении **TZDEFINITION** в потоке для фиксации в двоичном свойстве, например **диспидаппттздефрекур**.</span><span class="sxs-lookup"><span data-stu-id="759b2-122">A parser must be careful when it reads a stream that is obtained from **dispidApptTZDefRecur**, or when it persists **TZDEFINITION** to a stream for commitment to a binary property such as **dispidApptTZDefRecur**.</span></span> <span data-ttu-id="759b2-123">Дополнительные сведения [о СОХРАНЕНИИ TZDEFINITION в потоке для фиксации в двоичном свойстве](https://msdn.microsoft.com/library/0dec535d-d48f-39a5-97d5-0bd109134b3b%28Office.15%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="759b2-123">For more information, see [About persisting TZDEFINITION to a stream to commit to a binary property](https://msdn.microsoft.com/library/0dec535d-d48f-39a5-97d5-0bd109134b3b%28Office.15%29.aspx).</span></span>
  
 <span data-ttu-id="759b2-124">**диспидаппттздефрекур** указывает сведения о часовом поясе, которые описывают, как преобразовать дату и время собрания в серию, а также из времени в формате UTC.</span><span class="sxs-lookup"><span data-stu-id="759b2-124">**dispidApptTZDefRecur** specifies time zone information that describes how to convert the meeting date and time on a recurring series to and from Coordinated Universal Time (UTC).</span></span> <span data-ttu-id="759b2-125">Если это свойство задано, но содержит данные, несовместимые с данными, представленными в **диспидтимезонеструкт**, клиент должен использовать **диспидтимезонеструкт** вместо **диспидаппттздефрекур**.</span><span class="sxs-lookup"><span data-stu-id="759b2-125">If this property is set but it has data that is inconsistent with the data represented by **dispidTimeZoneStruct**, the client must use **dispidTimeZoneStruct** instead of **dispidApptTZDefRecur**.</span></span> <span data-ttu-id="759b2-126">Если **диспидаппттздефрекур** не задано, вместо него будет использоваться свойство **PidLidTimeZoneStruct** .</span><span class="sxs-lookup"><span data-stu-id="759b2-126">If **dispidApptTZDefRecur** is not set, the **PidLidTimeZoneStruct** property will be used instead.</span></span> <span data-ttu-id="759b2-127">Поля в этом большом ДВОИЧНОМ ОБЪЕКТЕ кодируются с помощью порядка байтов с прямым порядком байтов.</span><span class="sxs-lookup"><span data-stu-id="759b2-127">The fields in this BLOB are encoded in little-endian byte order.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="759b2-128">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="759b2-128">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="759b2-129">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="759b2-129">Protocol specifications</span></span>

<span data-ttu-id="759b2-130">[[MS — ОКСПРОПС]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="759b2-130">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="759b2-131">Содержит определения свойств и ссылки на связанные спецификации протокола Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="759b2-131">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="759b2-132">[[MS — ОКСОКАЛ]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="759b2-132">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="759b2-133">Задает свойства и операции для встречи, приглашения на собрание и ответных сообщений.</span><span class="sxs-lookup"><span data-stu-id="759b2-133">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="759b2-134">Файлы заГоловков</span><span class="sxs-lookup"><span data-stu-id="759b2-134">Header files</span></span>

<span data-ttu-id="759b2-135">MAPIDEFS. h</span><span class="sxs-lookup"><span data-stu-id="759b2-135">Mapidefs.h</span></span>
  
> <span data-ttu-id="759b2-136">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="759b2-136">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="759b2-137">См. также</span><span class="sxs-lookup"><span data-stu-id="759b2-137">See also</span></span>



[<span data-ttu-id="759b2-138">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="759b2-138">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="759b2-139">Каноническое свойство MAPI</span><span class="sxs-lookup"><span data-stu-id="759b2-139">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="759b2-140">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="759b2-140">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="759b2-141">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="759b2-141">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

