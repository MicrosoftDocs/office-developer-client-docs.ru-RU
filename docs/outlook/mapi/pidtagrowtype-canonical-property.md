---
title: Каноническое свойство PidTagRowType
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagRowType
api_type:
- COM
ms.assetid: d57ce5c8-1f60-4709-b86a-4468c4208dfe
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 962e8c92ae61e8b60862a3ae26a7cdfbf5034e89
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359516"
---
# <a name="pidtagrowtype-canonical-property"></a><span data-ttu-id="3843d-103">Каноническое свойство PidTagRowType</span><span class="sxs-lookup"><span data-stu-id="3843d-103">PidTagRowType Canonical Property</span></span>

  
  
<span data-ttu-id="3843d-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3843d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3843d-105">Содержит значение, которое указывает тип строки в таблице.</span><span class="sxs-lookup"><span data-stu-id="3843d-105">Contains a value that indicates the type of a row in a table.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="3843d-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="3843d-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="3843d-107">PR_ROW_TYPE</span><span class="sxs-lookup"><span data-stu-id="3843d-107">PR_ROW_TYPE</span></span>  <br/> |
|<span data-ttu-id="3843d-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="3843d-108">Identifier:</span></span>  <br/> |<span data-ttu-id="3843d-109">0x0FF5</span><span class="sxs-lookup"><span data-stu-id="3843d-109">0x0FF5</span></span>  <br/> |
|<span data-ttu-id="3843d-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="3843d-110">Data type:</span></span>  <br/> |<span data-ttu-id="3843d-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="3843d-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="3843d-112">Область:</span><span class="sxs-lookup"><span data-stu-id="3843d-112">Area:</span></span>  <br/> |<span data-ttu-id="3843d-113">MAPI, не передаваемая</span><span class="sxs-lookup"><span data-stu-id="3843d-113">MAPI non-transmittable</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="3843d-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="3843d-114">Remarks</span></span>

<span data-ttu-id="3843d-115">Это свойство отображается только в таблицах контента.</span><span class="sxs-lookup"><span data-stu-id="3843d-115">This property appears only on contents tables.</span></span> <span data-ttu-id="3843d-116">Категория существует только при найме элементов.</span><span class="sxs-lookup"><span data-stu-id="3843d-116">A category only exists when it has items.</span></span>
  
<span data-ttu-id="3843d-117">Это свойство может иметь одно из следующих значений:</span><span class="sxs-lookup"><span data-stu-id="3843d-117">This property can have exactly one of the following values:</span></span>
  
<span data-ttu-id="3843d-118">TBL_LEAF_ROW</span><span class="sxs-lookup"><span data-stu-id="3843d-118">TBL_LEAF_ROW</span></span> 
  
> <span data-ttu-id="3843d-119">Представляет фактические данные, а не строку категории.</span><span class="sxs-lookup"><span data-stu-id="3843d-119">Represents actual data, rather than a category row.</span></span>
    
<span data-ttu-id="3843d-120">TBL_EMPTY_CATEGORY</span><span class="sxs-lookup"><span data-stu-id="3843d-120">TBL_EMPTY_CATEGORY</span></span> 
  
> <span data-ttu-id="3843d-121">В настоящее время не используется.</span><span class="sxs-lookup"><span data-stu-id="3843d-121">Not currently used.</span></span>
    
<span data-ttu-id="3843d-122">TBL_EXPANDED_CATEGORY</span><span class="sxs-lookup"><span data-stu-id="3843d-122">TBL_EXPANDED_CATEGORY</span></span> 
  
> <span data-ttu-id="3843d-123">Категория расширена; пользовательский интерфейс обычно отображает это со знаком минус ( - ) рядом с ним.</span><span class="sxs-lookup"><span data-stu-id="3843d-123">The category is expanded; the user interface usually displays this with the minus sign ( - ) next to it.</span></span>
    
<span data-ttu-id="3843d-124">TBL_COLLAPSED_CATEGORY</span><span class="sxs-lookup"><span data-stu-id="3843d-124">TBL_COLLAPSED_CATEGORY</span></span> 
  
> <span data-ttu-id="3843d-125">Категория свернута; пользовательский интерфейс обычно отображает это со знаком плюс (+) рядом с ним.</span><span class="sxs-lookup"><span data-stu-id="3843d-125">The category is collapsed; the user interface usually displays this with the plus sign (+) next to it.</span></span>
    
## <a name="related-resources"></a><span data-ttu-id="3843d-126">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="3843d-126">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="3843d-127">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="3843d-127">Protocol specifications</span></span>

<span data-ttu-id="3843d-128">[[MS-OXCTABL]](https://msdn.microsoft.com/library/d33612dc-36a8-4623-8a26-c156cf8aae4b%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="3843d-128">[[MS-OXCTABL]](https://msdn.microsoft.com/library/d33612dc-36a8-4623-8a26-c156cf8aae4b%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="3843d-129">Включает допустимые операции для основных объектов таблицы.</span><span class="sxs-lookup"><span data-stu-id="3843d-129">Includes permissible operations for the core table objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="3843d-130">Файлы заголовки</span><span class="sxs-lookup"><span data-stu-id="3843d-130">Header files</span></span>

<span data-ttu-id="3843d-131">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="3843d-131">Mapidefs.h</span></span>
  
> <span data-ttu-id="3843d-132">Предоставляет определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="3843d-132">Provides data type definitions.</span></span>
    
<span data-ttu-id="3843d-133">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="3843d-133">Mapitags.h</span></span>
  
> <span data-ttu-id="3843d-134">Содержит определения свойств, перечисленных в качестве альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="3843d-134">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="3843d-135">См. также</span><span class="sxs-lookup"><span data-stu-id="3843d-135">See also</span></span>



[<span data-ttu-id="3843d-136">Каноническое свойство PidTagRowid</span><span class="sxs-lookup"><span data-stu-id="3843d-136">PidTagRowid Canonical Property</span></span>](pidtagrowid-canonical-property.md)


[<span data-ttu-id="3843d-137">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="3843d-137">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="3843d-138">Канонические свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="3843d-138">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="3843d-139">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="3843d-139">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="3843d-140">Сопоставление имен MAPI с каноническими именами свойств</span><span class="sxs-lookup"><span data-stu-id="3843d-140">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

