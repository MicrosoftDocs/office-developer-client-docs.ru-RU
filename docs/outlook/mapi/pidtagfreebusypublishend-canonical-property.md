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
ms.openlocfilehash: 1f7f439b211b60f7acad3a9dd19c50a21923c1cc
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19811163"
---
# <a name="pidtagfreebusypublishend-canonical-property"></a><span data-ttu-id="7e667-103">Каноническое свойство PidTagFreeBusyPublishEnd</span><span class="sxs-lookup"><span data-stu-id="7e667-103">PidTagFreeBusyPublishEnd Canonical Property</span></span>

  
  
<span data-ttu-id="7e667-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="7e667-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="7e667-105">Содержит время окончания публикации диапазона.</span><span class="sxs-lookup"><span data-stu-id="7e667-105">Contains the end time of the publishing range.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="7e667-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="7e667-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="7e667-107">PR_FREEBUSY_PUBLISH_END</span><span class="sxs-lookup"><span data-stu-id="7e667-107">PR_FREEBUSY_PUBLISH_END</span></span>  <br/> |
|<span data-ttu-id="7e667-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="7e667-108">Identifier:</span></span>  <br/> |<span data-ttu-id="7e667-109">0x6848</span><span class="sxs-lookup"><span data-stu-id="7e667-109">0x6848</span></span>  <br/> |
|<span data-ttu-id="7e667-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="7e667-110">Data type:</span></span>  <br/> |<span data-ttu-id="7e667-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="7e667-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="7e667-112">Область:</span><span class="sxs-lookup"><span data-stu-id="7e667-112">Area:</span></span>  <br/> |<span data-ttu-id="7e667-113">Обмен сведениями о доступности</span><span class="sxs-lookup"><span data-stu-id="7e667-113">Free/Busy</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="7e667-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="7e667-114">Remarks</span></span>

<span data-ttu-id="7e667-115">Значение для этого свойства вычисляется путем добавления значение **PR_FREEBUSY_COUNT_MONTHS** ([PidTagFreeBusyCountMonths](pidtagfreebusycountmonths-canonical-property.md)) на дату начала публикации диапазона.</span><span class="sxs-lookup"><span data-stu-id="7e667-115">The value for this property is computed by adding the value of **PR_FREEBUSY_COUNT_MONTHS** ([PidTagFreeBusyCountMonths](pidtagfreebusycountmonths-canonical-property.md)) to the start date of the publishing range.</span></span> <span data-ttu-id="7e667-116">Это значение выражается как число минут после полуночи, 1 января 1601 в формате UTC.</span><span class="sxs-lookup"><span data-stu-id="7e667-116">This value is expressed as the number of minutes since midnight, January 1, 1601 in Coordinated Universal Time (UTC).</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="7e667-117">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="7e667-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="7e667-118">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="7e667-118">Protocol specifications</span></span>

<span data-ttu-id="7e667-119">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="7e667-119">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="7e667-120">Содержит ссылки на связанные спецификаций протокола Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="7e667-120">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="7e667-121">[[MS-OXOPFFB]](http://msdn.microsoft.com/library/1a527299-7211-4d27-a74c-b69bd0746320%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="7e667-121">[[MS-OXOPFFB]](http://msdn.microsoft.com/library/1a527299-7211-4d27-a74c-b69bd0746320%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="7e667-122">Публикует доступности пользователя или ресурса.</span><span class="sxs-lookup"><span data-stu-id="7e667-122">Publishes the availability of a user or resource.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="7e667-123">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="7e667-123">Header files</span></span>

<span data-ttu-id="7e667-124">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="7e667-124">Mapidefs.h</span></span>
  
> <span data-ttu-id="7e667-125">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="7e667-125">Provides data type definitions.</span></span>
    
<span data-ttu-id="7e667-126">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="7e667-126">Mapitags.h</span></span>
  
> <span data-ttu-id="7e667-127">Содержит определения свойства в списке альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="7e667-127">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="7e667-128">См. также</span><span class="sxs-lookup"><span data-stu-id="7e667-128">See also</span></span>



[<span data-ttu-id="7e667-129">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="7e667-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="7e667-130">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="7e667-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="7e667-131">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="7e667-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="7e667-132">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="7e667-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

