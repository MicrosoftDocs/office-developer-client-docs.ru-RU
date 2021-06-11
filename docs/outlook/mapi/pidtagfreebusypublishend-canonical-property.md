---
title: Каноническое свойство PidTagFreeBusyPublishEnd
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagFreeBusyPublishEnd
api_type:
- HeaderDef
ms.assetid: df239741-6a63-4cd4-9bbb-42c0f5c668a5
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 3b4a8cb7136eee914dc697d24e0374ccb4b6f8b1
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316186"
---
# <a name="pidtagfreebusypublishend-canonical-property"></a><span data-ttu-id="e588d-103">Каноническое свойство PidTagFreeBusyPublishEnd</span><span class="sxs-lookup"><span data-stu-id="e588d-103">PidTagFreeBusyPublishEnd Canonical Property</span></span>

  
  
<span data-ttu-id="e588d-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e588d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e588d-105">Содержит конечное время диапазона публикации.</span><span class="sxs-lookup"><span data-stu-id="e588d-105">Contains the end time of the publishing range.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="e588d-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="e588d-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="e588d-107">PR_FREEBUSY_PUBLISH_END</span><span class="sxs-lookup"><span data-stu-id="e588d-107">PR_FREEBUSY_PUBLISH_END</span></span>  <br/> |
|<span data-ttu-id="e588d-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="e588d-108">Identifier:</span></span>  <br/> |<span data-ttu-id="e588d-109">0x6848</span><span class="sxs-lookup"><span data-stu-id="e588d-109">0x6848</span></span>  <br/> |
|<span data-ttu-id="e588d-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="e588d-110">Data type:</span></span>  <br/> |<span data-ttu-id="e588d-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="e588d-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="e588d-112">Область:</span><span class="sxs-lookup"><span data-stu-id="e588d-112">Area:</span></span>  <br/> |<span data-ttu-id="e588d-113">Бесплатный/занятый</span><span class="sxs-lookup"><span data-stu-id="e588d-113">Free/Busy</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e588d-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="e588d-114">Remarks</span></span>

<span data-ttu-id="e588d-115">Значение для этого свойства вычисляется путем добавления **значения PR_FREEBUSY_COUNT_MONTHS** [(PidTagFreeBusyCountMonths)](pidtagfreebusycountmonths-canonical-property.md)к дате начала диапазона публикации.</span><span class="sxs-lookup"><span data-stu-id="e588d-115">The value for this property is computed by adding the value of **PR_FREEBUSY_COUNT_MONTHS** ([PidTagFreeBusyCountMonths](pidtagfreebusycountmonths-canonical-property.md)) to the start date of the publishing range.</span></span> <span data-ttu-id="e588d-116">Это значение выражается как количество минут с полуночи, 1 января 1601 г. в Координируется универсальное время (UTC).</span><span class="sxs-lookup"><span data-stu-id="e588d-116">This value is expressed as the number of minutes since midnight, January 1, 1601 in Coordinated Universal Time (UTC).</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="e588d-117">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="e588d-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="e588d-118">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="e588d-118">Protocol specifications</span></span>

<span data-ttu-id="e588d-119">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e588d-119">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e588d-120">Содержит ссылки на связанные Exchange Server протоколы.</span><span class="sxs-lookup"><span data-stu-id="e588d-120">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="e588d-121">[[MS-OXOPFFB]](https://msdn.microsoft.com/library/1a527299-7211-4d27-a74c-b69bd0746320%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e588d-121">[[MS-OXOPFFB]](https://msdn.microsoft.com/library/1a527299-7211-4d27-a74c-b69bd0746320%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e588d-122">Публикует доступность пользователя или ресурса.</span><span class="sxs-lookup"><span data-stu-id="e588d-122">Publishes the availability of a user or resource.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="e588d-123">Файлы заголовки</span><span class="sxs-lookup"><span data-stu-id="e588d-123">Header files</span></span>

<span data-ttu-id="e588d-124">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="e588d-124">Mapidefs.h</span></span>
  
> <span data-ttu-id="e588d-125">Предоставляет определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="e588d-125">Provides data type definitions.</span></span>
    
<span data-ttu-id="e588d-126">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="e588d-126">Mapitags.h</span></span>
  
> <span data-ttu-id="e588d-127">Содержит определения свойств, перечисленных в качестве альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="e588d-127">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="e588d-128">См. также</span><span class="sxs-lookup"><span data-stu-id="e588d-128">See also</span></span>



[<span data-ttu-id="e588d-129">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="e588d-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="e588d-130">Канонические свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="e588d-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="e588d-131">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="e588d-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="e588d-132">Сопоставление имен MAPI с каноническими именами свойств</span><span class="sxs-lookup"><span data-stu-id="e588d-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

