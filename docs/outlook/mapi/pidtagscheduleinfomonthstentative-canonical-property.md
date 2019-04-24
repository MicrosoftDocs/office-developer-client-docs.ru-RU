---
title: Каноническое свойство PidTagScheduleInfoMonthsTentative
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagScheduleInfoMonthsTentative
api_type:
- COM
ms.assetid: 3179442c-6499-464a-93af-eb0a7a5b0d30
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 6fa0579dcd98a0d819e58e62d8a42cb2972a9d1e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359761"
---
# <a name="pidtagscheduleinfomonthstentative-canonical-property"></a><span data-ttu-id="e5b85-103">Каноническое свойство PidTagScheduleInfoMonthsTentative</span><span class="sxs-lookup"><span data-stu-id="e5b85-103">PidTagScheduleInfoMonthsTentative Canonical Property</span></span>

  
  
<span data-ttu-id="e5b85-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e5b85-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e5b85-105">Содержит месяцы, помеченные под вопросом в сообщении о занятости.</span><span class="sxs-lookup"><span data-stu-id="e5b85-105">Contains the months marked tentative in the free/busy message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="e5b85-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="e5b85-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="e5b85-107">ПР_СЧДИНФО_МОНСС_ТЕНТАТИВЕ</span><span class="sxs-lookup"><span data-stu-id="e5b85-107">PR_SCHDINFO_MONTHS_TENTATIVE</span></span>  <br/> |
|<span data-ttu-id="e5b85-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="e5b85-108">Identifier:</span></span>  <br/> |<span data-ttu-id="e5b85-109">0x6851</span><span class="sxs-lookup"><span data-stu-id="e5b85-109">0x6851</span></span>  <br/> |
|<span data-ttu-id="e5b85-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="e5b85-110">Data type:</span></span>  <br/> |<span data-ttu-id="e5b85-111">ПТ_МВ_ЛОНГ</span><span class="sxs-lookup"><span data-stu-id="e5b85-111">PT_MV_LONG</span></span>  <br/> |
|<span data-ttu-id="e5b85-112">Область:</span><span class="sxs-lookup"><span data-stu-id="e5b85-112">Area:</span></span>  <br/> |<span data-ttu-id="e5b85-113">Сведения о доступности</span><span class="sxs-lookup"><span data-stu-id="e5b85-113">Free/Busy</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e5b85-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="e5b85-114">Remarks</span></span>

<span data-ttu-id="e5b85-115">Число значений в этом свойстве должно быть между нулем и числом месяцев, охваченных диапазоном публикации, который является периодом между **пр_фрибуси_публиш_старт** ([PidTagFreeBusyPublishStart](pidtagfreebusypublishstart-canonical-property.md)) и \*\*пр_фрибуси_публиш_енд \*\*Свойства ([PidTagFreeBusyPublishEnd](pidtagfreebusypublishend-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="e5b85-115">The number of values in this property must be between zero and the number of months covered by the publishing range, which is the period between the **PR_FREEBUSY_PUBLISH_START** ([PidTagFreeBusyPublishStart](pidtagfreebusypublishstart-canonical-property.md)) and **PR_FREEBUSY_PUBLISH_END** ([PidTagFreeBusyPublishEnd](pidtagfreebusypublishend-canonical-property.md)) properties.</span></span>
  
<span data-ttu-id="e5b85-116">Каждое значение этого свойства содержит месяц и год, закодированный в нем.</span><span class="sxs-lookup"><span data-stu-id="e5b85-116">Each value in this property, has a month and year encoded in it.</span></span> <span data-ttu-id="e5b85-117">Он вычисляется с помощью выражения "Year × 16 + month", где год и месяц основываются на григорианском календаре.</span><span class="sxs-lookup"><span data-stu-id="e5b85-117">This is calculated by using the expression "year × 16 + month" where year and month are based on the Gregorian calendar.</span></span> <span data-ttu-id="e5b85-118">Значения сортируются в возрастающем порядке и кодируются в формате с прямым порядком байтов.</span><span class="sxs-lookup"><span data-stu-id="e5b85-118">The values are sorted in ascending order and are encoded in little-endian format.</span></span> <span data-ttu-id="e5b85-119">Если событие распространяется в течение нескольких месяцев или несколько лет, для каждого из месяцев, которые попадают в диапазон публикации, должно быть по одному значению.</span><span class="sxs-lookup"><span data-stu-id="e5b85-119">If an event is spread across multiple months, or multiple years, there must be one value for each of the months that fall in the publishing range.</span></span> <span data-ttu-id="e5b85-120">Если в диапазоне публикации нет предварительных событий, то это свойство и **пр_счдинфо_фрибуси_тентативе** ([PidTagScheduleInfoFreeBusyTentative](pidtagscheduleinfofreebusytentative-canonical-property.md)) не должны быть заданы или должны быть удалены, если они уже существуют.</span><span class="sxs-lookup"><span data-stu-id="e5b85-120">If there are no tentative events in the publishing range, then this property and **PR_SCHDINFO_FREEBUSY_TENTATIVE** ([PidTagScheduleInfoFreeBusyTentative](pidtagscheduleinfofreebusytentative-canonical-property.md)) must not be set or must be deleted if they already exist.</span></span> <span data-ttu-id="e5b85-121">В противном случае необходимо задать значение этого свойства.</span><span class="sxs-lookup"><span data-stu-id="e5b85-121">Otherwise, this property must be set.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="e5b85-122">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="e5b85-122">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="e5b85-123">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="e5b85-123">Protocol specifications</span></span>

<span data-ttu-id="e5b85-124">[[MS — ОКСПРОПС]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e5b85-124">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e5b85-125">Содержит ссылки на соответствующие спецификации протоколов Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="e5b85-125">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="e5b85-126">[[MS — ОКСОПФФБ]](https://msdn.microsoft.com/library/1a527299-7211-4d27-a74c-b69bd0746320%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e5b85-126">[[MS-OXOPFFB]](https://msdn.microsoft.com/library/1a527299-7211-4d27-a74c-b69bd0746320%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e5b85-127">Публикует доступность пользователя или ресурса.</span><span class="sxs-lookup"><span data-stu-id="e5b85-127">Publishes the availability of a user or resource.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="e5b85-128">Файлы заГоловков</span><span class="sxs-lookup"><span data-stu-id="e5b85-128">Header files</span></span>

<span data-ttu-id="e5b85-129">MAPIDEFS. h</span><span class="sxs-lookup"><span data-stu-id="e5b85-129">Mapidefs.h</span></span>
  
> <span data-ttu-id="e5b85-130">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="e5b85-130">Provides data type definitions.</span></span>
    
<span data-ttu-id="e5b85-131">Мапитагс. h</span><span class="sxs-lookup"><span data-stu-id="e5b85-131">Mapitags.h</span></span>
  
> <span data-ttu-id="e5b85-132">Содержит определения свойств, перечисленных как альтернативные имена.</span><span class="sxs-lookup"><span data-stu-id="e5b85-132">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="e5b85-133">См. также</span><span class="sxs-lookup"><span data-stu-id="e5b85-133">See also</span></span>



[<span data-ttu-id="e5b85-134">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="e5b85-134">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="e5b85-135">Каноническое свойство MAPI</span><span class="sxs-lookup"><span data-stu-id="e5b85-135">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="e5b85-136">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="e5b85-136">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="e5b85-137">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="e5b85-137">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

