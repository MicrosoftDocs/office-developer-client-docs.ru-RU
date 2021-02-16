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
# <a name="pidtagfreebusypublishend-canonical-property"></a><span data-ttu-id="7a9a1-103">Каноническое свойство PidTagFreeBusyPublishEnd</span><span class="sxs-lookup"><span data-stu-id="7a9a1-103">PidTagFreeBusyPublishEnd Canonical Property</span></span>

  
  
<span data-ttu-id="7a9a1-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7a9a1-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7a9a1-105">Содержит время окончания диапазона публикации.</span><span class="sxs-lookup"><span data-stu-id="7a9a1-105">Contains the end time of the publishing range.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="7a9a1-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="7a9a1-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="7a9a1-107">PR_FREEBUSY_PUBLISH_END</span><span class="sxs-lookup"><span data-stu-id="7a9a1-107">PR_FREEBUSY_PUBLISH_END</span></span>  <br/> |
|<span data-ttu-id="7a9a1-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="7a9a1-108">Identifier:</span></span>  <br/> |<span data-ttu-id="7a9a1-109">0x6848</span><span class="sxs-lookup"><span data-stu-id="7a9a1-109">0x6848</span></span>  <br/> |
|<span data-ttu-id="7a9a1-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="7a9a1-110">Data type:</span></span>  <br/> |<span data-ttu-id="7a9a1-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="7a9a1-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="7a9a1-112">Область:</span><span class="sxs-lookup"><span data-stu-id="7a9a1-112">Area:</span></span>  <br/> |<span data-ttu-id="7a9a1-113">Free/Busy</span><span class="sxs-lookup"><span data-stu-id="7a9a1-113">Free/Busy</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="7a9a1-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="7a9a1-114">Remarks</span></span>

<span data-ttu-id="7a9a1-115">Значение этого свойства вычисляется путем добавления значения **PR_FREEBUSY_COUNT_MONTHS** ([PidTagFreeBusyCountMonths)](pidtagfreebusycountmonths-canonical-property.md)в дату начала диапазона публикации.</span><span class="sxs-lookup"><span data-stu-id="7a9a1-115">The value for this property is computed by adding the value of **PR_FREEBUSY_COUNT_MONTHS** ([PidTagFreeBusyCountMonths](pidtagfreebusycountmonths-canonical-property.md)) to the start date of the publishing range.</span></span> <span data-ttu-id="7a9a1-116">Это значение выражается в количестве минут с полуночи 1 января 1601 г. по времени в универсальном координируется (UTC).</span><span class="sxs-lookup"><span data-stu-id="7a9a1-116">This value is expressed as the number of minutes since midnight, January 1, 1601 in Coordinated Universal Time (UTC).</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="7a9a1-117">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="7a9a1-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="7a9a1-118">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="7a9a1-118">Protocol specifications</span></span>

<span data-ttu-id="7a9a1-119">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="7a9a1-119">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="7a9a1-120">Содержит ссылки на связанные Exchange Server протоколы.</span><span class="sxs-lookup"><span data-stu-id="7a9a1-120">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="7a9a1-121">[[MS-OXOPFFB]](https://msdn.microsoft.com/library/1a527299-7211-4d27-a74c-b69bd0746320%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="7a9a1-121">[[MS-OXOPFFB]](https://msdn.microsoft.com/library/1a527299-7211-4d27-a74c-b69bd0746320%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="7a9a1-122">Публикует доступность пользователя или ресурса.</span><span class="sxs-lookup"><span data-stu-id="7a9a1-122">Publishes the availability of a user or resource.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="7a9a1-123">Файлы заголовок</span><span class="sxs-lookup"><span data-stu-id="7a9a1-123">Header files</span></span>

<span data-ttu-id="7a9a1-124">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="7a9a1-124">Mapidefs.h</span></span>
  
> <span data-ttu-id="7a9a1-125">Предоставляет определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="7a9a1-125">Provides data type definitions.</span></span>
    
<span data-ttu-id="7a9a1-126">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="7a9a1-126">Mapitags.h</span></span>
  
> <span data-ttu-id="7a9a1-127">Содержит определения свойств, перечисленных в качестве альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="7a9a1-127">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="7a9a1-128">См. также</span><span class="sxs-lookup"><span data-stu-id="7a9a1-128">See also</span></span>



[<span data-ttu-id="7a9a1-129">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="7a9a1-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="7a9a1-130">Канонические свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="7a9a1-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="7a9a1-131">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="7a9a1-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="7a9a1-132">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="7a9a1-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

