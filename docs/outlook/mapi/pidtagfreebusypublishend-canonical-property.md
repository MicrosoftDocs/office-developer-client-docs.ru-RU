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
# <a name="pidtagfreebusypublishend-canonical-property"></a><span data-ttu-id="6218a-103">Каноническое свойство PidTagFreeBusyPublishEnd</span><span class="sxs-lookup"><span data-stu-id="6218a-103">PidTagFreeBusyPublishEnd Canonical Property</span></span>

  
  
<span data-ttu-id="6218a-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6218a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6218a-105">Содержит время окончания диапазона публикации.</span><span class="sxs-lookup"><span data-stu-id="6218a-105">Contains the end time of the publishing range.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="6218a-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="6218a-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="6218a-107">ПР_ФРИБУСИ_ПУБЛИШ_ЕНД</span><span class="sxs-lookup"><span data-stu-id="6218a-107">PR_FREEBUSY_PUBLISH_END</span></span>  <br/> |
|<span data-ttu-id="6218a-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="6218a-108">Identifier:</span></span>  <br/> |<span data-ttu-id="6218a-109">0x6848</span><span class="sxs-lookup"><span data-stu-id="6218a-109">0x6848</span></span>  <br/> |
|<span data-ttu-id="6218a-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="6218a-110">Data type:</span></span>  <br/> |<span data-ttu-id="6218a-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="6218a-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="6218a-112">Область:</span><span class="sxs-lookup"><span data-stu-id="6218a-112">Area:</span></span>  <br/> |<span data-ttu-id="6218a-113">Сведения о доступности</span><span class="sxs-lookup"><span data-stu-id="6218a-113">Free/Busy</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="6218a-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="6218a-114">Remarks</span></span>

<span data-ttu-id="6218a-115">Значение этого свойства вычисляется путем добавления значения **пр_фрибуси_каунт_монсс** ([PidTagFreeBusyCountMonths](pidtagfreebusycountmonths-canonical-property.md)) к дате начала диапазона публикации.</span><span class="sxs-lookup"><span data-stu-id="6218a-115">The value for this property is computed by adding the value of **PR_FREEBUSY_COUNT_MONTHS** ([PidTagFreeBusyCountMonths](pidtagfreebusycountmonths-canonical-property.md)) to the start date of the publishing range.</span></span> <span data-ttu-id="6218a-116">Это значение выражается в виде числа минут, начиная с полуночи 1 января 1601 г. в формате UTC.</span><span class="sxs-lookup"><span data-stu-id="6218a-116">This value is expressed as the number of minutes since midnight, January 1, 1601 in Coordinated Universal Time (UTC).</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="6218a-117">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="6218a-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="6218a-118">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="6218a-118">Protocol specifications</span></span>

<span data-ttu-id="6218a-119">[[MS — ОКСПРОПС]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="6218a-119">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="6218a-120">Содержит ссылки на соответствующие спецификации протоколов Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="6218a-120">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="6218a-121">[[MS — ОКСОПФФБ]](https://msdn.microsoft.com/library/1a527299-7211-4d27-a74c-b69bd0746320%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="6218a-121">[[MS-OXOPFFB]](https://msdn.microsoft.com/library/1a527299-7211-4d27-a74c-b69bd0746320%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="6218a-122">Публикует доступность пользователя или ресурса.</span><span class="sxs-lookup"><span data-stu-id="6218a-122">Publishes the availability of a user or resource.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="6218a-123">Файлы заГоловков</span><span class="sxs-lookup"><span data-stu-id="6218a-123">Header files</span></span>

<span data-ttu-id="6218a-124">MAPIDEFS. h</span><span class="sxs-lookup"><span data-stu-id="6218a-124">Mapidefs.h</span></span>
  
> <span data-ttu-id="6218a-125">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="6218a-125">Provides data type definitions.</span></span>
    
<span data-ttu-id="6218a-126">Мапитагс. h</span><span class="sxs-lookup"><span data-stu-id="6218a-126">Mapitags.h</span></span>
  
> <span data-ttu-id="6218a-127">Содержит определения свойств, перечисленных как альтернативные имена.</span><span class="sxs-lookup"><span data-stu-id="6218a-127">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="6218a-128">См. также</span><span class="sxs-lookup"><span data-stu-id="6218a-128">See also</span></span>



[<span data-ttu-id="6218a-129">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="6218a-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="6218a-130">Каноническое свойство MAPI</span><span class="sxs-lookup"><span data-stu-id="6218a-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="6218a-131">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="6218a-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="6218a-132">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="6218a-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

