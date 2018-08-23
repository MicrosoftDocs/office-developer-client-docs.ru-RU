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
ms.openlocfilehash: b539de9793c45e4b393452c264d72dda6fa58c4e
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22568800"
---
# <a name="pidtagfreebusypublishend-canonical-property"></a><span data-ttu-id="47711-103">Каноническое свойство PidTagFreeBusyPublishEnd</span><span class="sxs-lookup"><span data-stu-id="47711-103">PidTagFreeBusyPublishEnd Canonical Property</span></span>

  
  
<span data-ttu-id="47711-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="47711-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="47711-105">Содержит время окончания публикации диапазона.</span><span class="sxs-lookup"><span data-stu-id="47711-105">Contains the end time of the publishing range.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="47711-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="47711-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="47711-107">PR_FREEBUSY_PUBLISH_END</span><span class="sxs-lookup"><span data-stu-id="47711-107">PR_FREEBUSY_PUBLISH_END</span></span>  <br/> |
|<span data-ttu-id="47711-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="47711-108">Identifier:</span></span>  <br/> |<span data-ttu-id="47711-109">0x6848</span><span class="sxs-lookup"><span data-stu-id="47711-109">0x6848</span></span>  <br/> |
|<span data-ttu-id="47711-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="47711-110">Data type:</span></span>  <br/> |<span data-ttu-id="47711-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="47711-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="47711-112">Область:</span><span class="sxs-lookup"><span data-stu-id="47711-112">Area:</span></span>  <br/> |<span data-ttu-id="47711-113">Обмен сведениями о доступности</span><span class="sxs-lookup"><span data-stu-id="47711-113">Free/Busy</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="47711-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="47711-114">Remarks</span></span>

<span data-ttu-id="47711-115">Значение для этого свойства вычисляется путем добавления значение **PR_FREEBUSY_COUNT_MONTHS** ([PidTagFreeBusyCountMonths](pidtagfreebusycountmonths-canonical-property.md)) на дату начала публикации диапазона.</span><span class="sxs-lookup"><span data-stu-id="47711-115">The value for this property is computed by adding the value of **PR_FREEBUSY_COUNT_MONTHS** ([PidTagFreeBusyCountMonths](pidtagfreebusycountmonths-canonical-property.md)) to the start date of the publishing range.</span></span> <span data-ttu-id="47711-116">Это значение выражается как число минут после полуночи, 1 января 1601 в формате UTC.</span><span class="sxs-lookup"><span data-stu-id="47711-116">This value is expressed as the number of minutes since midnight, January 1, 1601 in Coordinated Universal Time (UTC).</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="47711-117">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="47711-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="47711-118">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="47711-118">Protocol specifications</span></span>

<span data-ttu-id="47711-119">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="47711-119">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="47711-120">Содержит ссылки на связанные спецификаций протокола Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="47711-120">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="47711-121">[[MS-OXOPFFB]](http://msdn.microsoft.com/library/1a527299-7211-4d27-a74c-b69bd0746320%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="47711-121">[[MS-OXOPFFB]](http://msdn.microsoft.com/library/1a527299-7211-4d27-a74c-b69bd0746320%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="47711-122">Публикует доступности пользователя или ресурса.</span><span class="sxs-lookup"><span data-stu-id="47711-122">Publishes the availability of a user or resource.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="47711-123">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="47711-123">Header files</span></span>

<span data-ttu-id="47711-124">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="47711-124">Mapidefs.h</span></span>
  
> <span data-ttu-id="47711-125">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="47711-125">Provides data type definitions.</span></span>
    
<span data-ttu-id="47711-126">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="47711-126">Mapitags.h</span></span>
  
> <span data-ttu-id="47711-127">Содержит определения свойства в списке альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="47711-127">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="47711-128">См. также</span><span class="sxs-lookup"><span data-stu-id="47711-128">See also</span></span>



[<span data-ttu-id="47711-129">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="47711-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="47711-130">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="47711-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="47711-131">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="47711-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="47711-132">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="47711-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

