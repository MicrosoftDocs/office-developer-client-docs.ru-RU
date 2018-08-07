---
title: Каноническое свойство PidTagScheduleInfoFreeBusyTentative
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagScheduleInfoFreeBusyTentative
api_type:
- COM
ms.assetid: 28453d29-30c5-405b-84d2-5bb5f281756c
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: a00505b765abdcb7b8fe9d68052774b30bbdf692
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19811857"
---
# <a name="pidtagscheduleinfofreebusytentative-canonical-property"></a><span data-ttu-id="31d9c-103">Каноническое свойство PidTagScheduleInfoFreeBusyTentative</span><span class="sxs-lookup"><span data-stu-id="31d9c-103">PidTagScheduleInfoFreeBusyTentative Canonical Property</span></span>

  
  
<span data-ttu-id="31d9c-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="31d9c-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="31d9c-105">Содержит блоки времени, для которых состояние доступности под вопросом.</span><span class="sxs-lookup"><span data-stu-id="31d9c-105">Contains the blocks of times for which the free/busy status is tentative.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="31d9c-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="31d9c-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="31d9c-107">PR_SCHDINFO_FREEBUSY_TENTATIVE</span><span class="sxs-lookup"><span data-stu-id="31d9c-107">PR_SCHDINFO_FREEBUSY_TENTATIVE</span></span>  <br/> |
|<span data-ttu-id="31d9c-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="31d9c-108">Identifier:</span></span>  <br/> |<span data-ttu-id="31d9c-109">0x6852</span><span class="sxs-lookup"><span data-stu-id="31d9c-109">0x6852</span></span>  <br/> |
|<span data-ttu-id="31d9c-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="31d9c-110">Data type:</span></span>  <br/> |<span data-ttu-id="31d9c-111">PT_MV_BINARY</span><span class="sxs-lookup"><span data-stu-id="31d9c-111">PT_MV_BINARY</span></span>  <br/> |
|<span data-ttu-id="31d9c-112">Область:</span><span class="sxs-lookup"><span data-stu-id="31d9c-112">Area:</span></span>  <br/> |<span data-ttu-id="31d9c-113">Обмен сведениями о доступности</span><span class="sxs-lookup"><span data-stu-id="31d9c-113">Free/Busy</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="31d9c-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="31d9c-114">Remarks</span></span>

<span data-ttu-id="31d9c-115">Это свойство имеет любое количество значений количество значений в **PR_SCHDINFO_MONTHS_TENTATIVE** ([PidTagScheduleInfoMonthsTentative](pidtagscheduleinfomonthstentative-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="31d9c-115">This property has as many values as the number of values in **PR_SCHDINFO_MONTHS_TENTATIVE** ([PidTagScheduleInfoMonthsTentative](pidtagscheduleinfomonthstentative-canonical-property.md)).</span></span> <span data-ttu-id="31d9c-116">Каждый двоичное значение представляет месяц и соответствует значению с таким же индексом в **PR_SCHDINFO_MONTHS_TENTATIVE**.</span><span class="sxs-lookup"><span data-stu-id="31d9c-116">Each binary value represents a month and corresponds to the value at the same index in **PR_SCHDINFO_MONTHS_TENTATIVE**.</span></span> <span data-ttu-id="31d9c-117">Двоичные значения сортируются в том же порядке, как значение в **PR_SCHDINFO_MONTHS_TENTATIVE**.</span><span class="sxs-lookup"><span data-stu-id="31d9c-117">The binary values are sorted in the same order as the values in **PR_SCHDINFO_MONTHS_TENTATIVE**.</span></span>
  
<span data-ttu-id="31d9c-118">Каждый двоичное значение имеет один или несколько блоков 4-БАЙТНЫХ и каждый из них содержит время начала в первых двух байтах и время окончания в второй два байта в формате с прямым.</span><span class="sxs-lookup"><span data-stu-id="31d9c-118">Each binary value has one or more 4-BYTE blocks and each of them contains the start time in the first two bytes and end time in the second two bytes in little-endian format.</span></span> <span data-ttu-id="31d9c-119">Время начала — число минут между полночь по Гринвичу (UTC) первого дня недели, месяца и время начала события в формате UTC.</span><span class="sxs-lookup"><span data-stu-id="31d9c-119">The start time is the number of minutes between midnight Coordinated Universal Time (UTC) of the first day of the month and the start time of the event in UTC.</span></span> <span data-ttu-id="31d9c-120">Время окончания — это число минут между полночь по Гринвичу первого дня недели, месяца и время окончания события в формате UTC.</span><span class="sxs-lookup"><span data-stu-id="31d9c-120">The end time is the number of minutes between midnight UTC of the first day of the month and the end time of the event in UTC.</span></span> <span data-ttu-id="31d9c-121">4-БАЙТНЫХ блоки сортируются в порядке возрастания.</span><span class="sxs-lookup"><span data-stu-id="31d9c-121">The 4-BYTE blocks are sorted in ascending order.</span></span>
  
<span data-ttu-id="31d9c-122">Последовательные или перекрывающиеся блоки времени объединяются в один блок с время начала время начала первого блока и время окончания как время окончания последнего блока.</span><span class="sxs-lookup"><span data-stu-id="31d9c-122">Consecutive or overlapping blocks of time are merged into one block with start time as the start time of the first block and end time as the end time of the last block.</span></span> <span data-ttu-id="31d9c-123">Если событие распределить по несколько месяцев или лет, событие делится на несколько блоков, другая — для каждого месяца.</span><span class="sxs-lookup"><span data-stu-id="31d9c-123">If an event is spread across multiple months or years, the event is split into multiple blocks, one for each month.</span></span> <span data-ttu-id="31d9c-124">Если нет под вопросом событий в диапазоне публикации, затем это свойство и **PR_SCHDINFO_MONTHS_TENTATIVE** не должен быть установлен или должен быть удален, если они существуют.</span><span class="sxs-lookup"><span data-stu-id="31d9c-124">If there are no tentative events in the publishing range, then this property and **PR_SCHDINFO_MONTHS_TENTATIVE** must not be set or must be deleted if they already exist.</span></span> <span data-ttu-id="31d9c-125">В противном случае необходимо установить это свойство.</span><span class="sxs-lookup"><span data-stu-id="31d9c-125">Otherwise, this property must be set.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="31d9c-126">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="31d9c-126">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="31d9c-127">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="31d9c-127">Protocol specifications</span></span>

<span data-ttu-id="31d9c-128">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="31d9c-128">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="31d9c-129">Содержит ссылки на связанные спецификаций протокола Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="31d9c-129">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="31d9c-130">[[MS-OXOPFFB]](http://msdn.microsoft.com/library/1a527299-7211-4d27-a74c-b69bd0746320%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="31d9c-130">[[MS-OXOPFFB]](http://msdn.microsoft.com/library/1a527299-7211-4d27-a74c-b69bd0746320%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="31d9c-131">Публикует доступности пользователя или ресурса.</span><span class="sxs-lookup"><span data-stu-id="31d9c-131">Publishes the availability of a user or resource.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="31d9c-132">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="31d9c-132">Header files</span></span>

<span data-ttu-id="31d9c-133">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="31d9c-133">Mapidefs.h</span></span>
  
> <span data-ttu-id="31d9c-134">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="31d9c-134">Provides data type definitions.</span></span>
    
<span data-ttu-id="31d9c-135">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="31d9c-135">Mapitags.h</span></span>
  
> <span data-ttu-id="31d9c-136">Содержит определения свойства в списке альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="31d9c-136">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="31d9c-137">См. также</span><span class="sxs-lookup"><span data-stu-id="31d9c-137">See also</span></span>



[<span data-ttu-id="31d9c-138">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="31d9c-138">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="31d9c-139">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="31d9c-139">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="31d9c-140">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="31d9c-140">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="31d9c-141">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="31d9c-141">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

