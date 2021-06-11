---
title: PidTagScheduleInfoMonthsTentative Canonical Property
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
# <a name="pidtagscheduleinfomonthstentative-canonical-property"></a><span data-ttu-id="281a9-103">PidTagScheduleInfoMonthsTentative Canonical Property</span><span class="sxs-lookup"><span data-stu-id="281a9-103">PidTagScheduleInfoMonthsTentative Canonical Property</span></span>

  
  
<span data-ttu-id="281a9-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="281a9-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="281a9-105">Содержит месяцы, отмеченные предварительно в свободном/загруженном сообщении.</span><span class="sxs-lookup"><span data-stu-id="281a9-105">Contains the months marked tentative in the free/busy message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="281a9-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="281a9-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="281a9-107">PR_SCHDINFO_MONTHS_TENTATIVE</span><span class="sxs-lookup"><span data-stu-id="281a9-107">PR_SCHDINFO_MONTHS_TENTATIVE</span></span>  <br/> |
|<span data-ttu-id="281a9-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="281a9-108">Identifier:</span></span>  <br/> |<span data-ttu-id="281a9-109">0x6851</span><span class="sxs-lookup"><span data-stu-id="281a9-109">0x6851</span></span>  <br/> |
|<span data-ttu-id="281a9-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="281a9-110">Data type:</span></span>  <br/> |<span data-ttu-id="281a9-111">PT_MV_LONG</span><span class="sxs-lookup"><span data-stu-id="281a9-111">PT_MV_LONG</span></span>  <br/> |
|<span data-ttu-id="281a9-112">Область:</span><span class="sxs-lookup"><span data-stu-id="281a9-112">Area:</span></span>  <br/> |<span data-ttu-id="281a9-113">Бесплатный/занятый</span><span class="sxs-lookup"><span data-stu-id="281a9-113">Free/Busy</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="281a9-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="281a9-114">Remarks</span></span>

<span data-ttu-id="281a9-115">Количество значений в этом свойстве должно быть от нуля до количества месяцев, охватываемых диапазоном публикации, который является периодом между свойствами **PR_FREEBUSY_PUBLISH_START** [(PidTagFreeBusyPublishStart)](pidtagfreebusypublishstart-canonical-property.md)и **PR_FREEBUSY_PUBLISH_END** [(PidTagFreeBusyPublishEnd).](pidtagfreebusypublishend-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="281a9-115">The number of values in this property must be between zero and the number of months covered by the publishing range, which is the period between the **PR_FREEBUSY_PUBLISH_START** ([PidTagFreeBusyPublishStart](pidtagfreebusypublishstart-canonical-property.md)) and **PR_FREEBUSY_PUBLISH_END** ([PidTagFreeBusyPublishEnd](pidtagfreebusypublishend-canonical-property.md)) properties.</span></span>
  
<span data-ttu-id="281a9-116">Каждое значение в этом свойстве кодирует месяц и год.</span><span class="sxs-lookup"><span data-stu-id="281a9-116">Each value in this property, has a month and year encoded in it.</span></span> <span data-ttu-id="281a9-117">Это рассчитывается с помощью выражения "год × 16 + месяц", в котором год и месяц основаны на григорианском календаре.</span><span class="sxs-lookup"><span data-stu-id="281a9-117">This is calculated by using the expression "year × 16 + month" where year and month are based on the Gregorian calendar.</span></span> <span data-ttu-id="281a9-118">Значения сортируются в порядке восходящей и закодируются в формате little-endian.</span><span class="sxs-lookup"><span data-stu-id="281a9-118">The values are sorted in ascending order and are encoded in little-endian format.</span></span> <span data-ttu-id="281a9-119">Если событие распространяется на несколько месяцев или несколько лет, для каждого из месяцев, которые попадают в диапазон публикации, должно быть одно значение.</span><span class="sxs-lookup"><span data-stu-id="281a9-119">If an event is spread across multiple months, or multiple years, there must be one value for each of the months that fall in the publishing range.</span></span> <span data-ttu-id="281a9-120">Если в диапазоне публикаций нет предварительных **событий,** то это свойство и PR_SCHDINFO_FREEBUSY_TENTATIVE [(PidTagScheduleInfoFreeBusyTentative)](pidtagscheduleinfofreebusytentative-canonical-property.md)не должны быть заданы или должны быть удалены, если они уже существуют.</span><span class="sxs-lookup"><span data-stu-id="281a9-120">If there are no tentative events in the publishing range, then this property and **PR_SCHDINFO_FREEBUSY_TENTATIVE** ([PidTagScheduleInfoFreeBusyTentative](pidtagscheduleinfofreebusytentative-canonical-property.md)) must not be set or must be deleted if they already exist.</span></span> <span data-ttu-id="281a9-121">В противном случае необходимо установить это свойство.</span><span class="sxs-lookup"><span data-stu-id="281a9-121">Otherwise, this property must be set.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="281a9-122">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="281a9-122">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="281a9-123">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="281a9-123">Protocol specifications</span></span>

<span data-ttu-id="281a9-124">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="281a9-124">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="281a9-125">Содержит ссылки на связанные Exchange Server протоколы.</span><span class="sxs-lookup"><span data-stu-id="281a9-125">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="281a9-126">[[MS-OXOPFFB]](https://msdn.microsoft.com/library/1a527299-7211-4d27-a74c-b69bd0746320%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="281a9-126">[[MS-OXOPFFB]](https://msdn.microsoft.com/library/1a527299-7211-4d27-a74c-b69bd0746320%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="281a9-127">Публикует доступность пользователя или ресурса.</span><span class="sxs-lookup"><span data-stu-id="281a9-127">Publishes the availability of a user or resource.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="281a9-128">Файлы заголовки</span><span class="sxs-lookup"><span data-stu-id="281a9-128">Header files</span></span>

<span data-ttu-id="281a9-129">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="281a9-129">Mapidefs.h</span></span>
  
> <span data-ttu-id="281a9-130">Предоставляет определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="281a9-130">Provides data type definitions.</span></span>
    
<span data-ttu-id="281a9-131">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="281a9-131">Mapitags.h</span></span>
  
> <span data-ttu-id="281a9-132">Содержит определения свойств, перечисленных в качестве альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="281a9-132">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="281a9-133">См. также</span><span class="sxs-lookup"><span data-stu-id="281a9-133">See also</span></span>



[<span data-ttu-id="281a9-134">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="281a9-134">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="281a9-135">Канонические свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="281a9-135">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="281a9-136">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="281a9-136">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="281a9-137">Сопоставление имен MAPI с каноническими именами свойств</span><span class="sxs-lookup"><span data-stu-id="281a9-137">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

