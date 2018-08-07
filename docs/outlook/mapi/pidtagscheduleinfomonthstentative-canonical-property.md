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
ms.openlocfilehash: 20620a5835e627eb7543a03037f9be75db6739ac
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19811854"
---
# <a name="pidtagscheduleinfomonthstentative-canonical-property"></a><span data-ttu-id="73582-103">Каноническое свойство PidTagScheduleInfoMonthsTentative</span><span class="sxs-lookup"><span data-stu-id="73582-103">PidTagScheduleInfoMonthsTentative Canonical Property</span></span>

  
  
<span data-ttu-id="73582-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="73582-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="73582-105">Содержит месяцев, помеченные под вопросом в сообщении о доступности.</span><span class="sxs-lookup"><span data-stu-id="73582-105">Contains the months marked tentative in the free/busy message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="73582-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="73582-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="73582-107">PR_SCHDINFO_MONTHS_TENTATIVE</span><span class="sxs-lookup"><span data-stu-id="73582-107">PR_SCHDINFO_MONTHS_TENTATIVE</span></span>  <br/> |
|<span data-ttu-id="73582-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="73582-108">Identifier:</span></span>  <br/> |<span data-ttu-id="73582-109">0x6851</span><span class="sxs-lookup"><span data-stu-id="73582-109">0x6851</span></span>  <br/> |
|<span data-ttu-id="73582-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="73582-110">Data type:</span></span>  <br/> |<span data-ttu-id="73582-111">PT_MV_LONG</span><span class="sxs-lookup"><span data-stu-id="73582-111">PT_MV_LONG</span></span>  <br/> |
|<span data-ttu-id="73582-112">Область:</span><span class="sxs-lookup"><span data-stu-id="73582-112">Area:</span></span>  <br/> |<span data-ttu-id="73582-113">Обмен сведениями о доступности</span><span class="sxs-lookup"><span data-stu-id="73582-113">Free/Busy</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="73582-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="73582-114">Remarks</span></span>

<span data-ttu-id="73582-115">Число значений в это свойство должно быть между 0 и число месяцев, к которому применяется публикации интервал, заданный период между **PR_FREEBUSY_PUBLISH_START** ([PidTagFreeBusyPublishStart](pidtagfreebusypublishstart-canonical-property.md)) и **PR_FREEBUSY_PUBLISH_END **Свойства ([PidTagFreeBusyPublishEnd](pidtagfreebusypublishend-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="73582-115">The number of values in this property must be between zero and the number of months covered by the publishing range, which is the period between the **PR_FREEBUSY_PUBLISH_START** ([PidTagFreeBusyPublishStart](pidtagfreebusypublishstart-canonical-property.md)) and **PR_FREEBUSY_PUBLISH_END** ([PidTagFreeBusyPublishEnd](pidtagfreebusypublishend-canonical-property.md)) properties.</span></span>
  
<span data-ttu-id="73582-116">Каждое значение этого свойства имеет месяц и год, закодированный в нем.</span><span class="sxs-lookup"><span data-stu-id="73582-116">Each value in this property, has a month and year encoded in it.</span></span> <span data-ttu-id="73582-117">Это именно рассчитывается, используя выражение «году × 16 + месяц» где года, месяца на основе григорианский календарь.</span><span class="sxs-lookup"><span data-stu-id="73582-117">This is calculated by using the expression "year × 16 + month" where year and month are based on the Gregorian calendar.</span></span> <span data-ttu-id="73582-118">Значения сортируются в порядке возрастания и кодируются в формате с прямым.</span><span class="sxs-lookup"><span data-stu-id="73582-118">The values are sorted in ascending order and are encoded in little-endian format.</span></span> <span data-ttu-id="73582-119">Если событие распространено на несколько месяцев или нескольких лет должно быть одно значение для каждого месяца, которые лежат в диапазоне от публикации.</span><span class="sxs-lookup"><span data-stu-id="73582-119">If an event is spread across multiple months, or multiple years, there must be one value for each of the months that fall in the publishing range.</span></span> <span data-ttu-id="73582-120">Если нет под вопросом событий в диапазоне публикации, затем это свойство и **PR_SCHDINFO_FREEBUSY_TENTATIVE** ([PidTagScheduleInfoFreeBusyTentative](pidtagscheduleinfofreebusytentative-canonical-property.md)) не должен быть установлен или должен быть удален, если они существуют.</span><span class="sxs-lookup"><span data-stu-id="73582-120">If there are no tentative events in the publishing range, then this property and **PR_SCHDINFO_FREEBUSY_TENTATIVE** ([PidTagScheduleInfoFreeBusyTentative](pidtagscheduleinfofreebusytentative-canonical-property.md)) must not be set or must be deleted if they already exist.</span></span> <span data-ttu-id="73582-121">В противном случае необходимо установить это свойство.</span><span class="sxs-lookup"><span data-stu-id="73582-121">Otherwise, this property must be set.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="73582-122">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="73582-122">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="73582-123">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="73582-123">Protocol specifications</span></span>

<span data-ttu-id="73582-124">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="73582-124">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="73582-125">Содержит ссылки на связанные спецификаций протокола Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="73582-125">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="73582-126">[[MS-OXOPFFB]](http://msdn.microsoft.com/library/1a527299-7211-4d27-a74c-b69bd0746320%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="73582-126">[[MS-OXOPFFB]](http://msdn.microsoft.com/library/1a527299-7211-4d27-a74c-b69bd0746320%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="73582-127">Публикует доступности пользователя или ресурса.</span><span class="sxs-lookup"><span data-stu-id="73582-127">Publishes the availability of a user or resource.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="73582-128">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="73582-128">Header files</span></span>

<span data-ttu-id="73582-129">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="73582-129">Mapidefs.h</span></span>
  
> <span data-ttu-id="73582-130">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="73582-130">Provides data type definitions.</span></span>
    
<span data-ttu-id="73582-131">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="73582-131">Mapitags.h</span></span>
  
> <span data-ttu-id="73582-132">Содержит определения свойства в списке альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="73582-132">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="73582-133">См. также</span><span class="sxs-lookup"><span data-stu-id="73582-133">See also</span></span>



[<span data-ttu-id="73582-134">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="73582-134">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="73582-135">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="73582-135">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="73582-136">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="73582-136">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="73582-137">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="73582-137">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

