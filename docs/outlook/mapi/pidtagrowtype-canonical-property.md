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
ms.openlocfilehash: 6e856cc8dc131c1b6266181a954a8da9cfb1d1ea
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22566105"
---
# <a name="pidtagrowtype-canonical-property"></a><span data-ttu-id="d9409-103">Каноническое свойство PidTagRowType</span><span class="sxs-lookup"><span data-stu-id="d9409-103">PidTagRowType Canonical Property</span></span>

  
  
<span data-ttu-id="d9409-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d9409-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d9409-105">Содержит значение, которое указывает тип строки в таблице.</span><span class="sxs-lookup"><span data-stu-id="d9409-105">Contains a value that indicates the type of a row in a table.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="d9409-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="d9409-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="d9409-107">PR_ROW_TYPE</span><span class="sxs-lookup"><span data-stu-id="d9409-107">PR_ROW_TYPE</span></span>  <br/> |
|<span data-ttu-id="d9409-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="d9409-108">Identifier:</span></span>  <br/> |<span data-ttu-id="d9409-109">0x0FF5</span><span class="sxs-lookup"><span data-stu-id="d9409-109">0x0FF5</span></span>  <br/> |
|<span data-ttu-id="d9409-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="d9409-110">Data type:</span></span>  <br/> |<span data-ttu-id="d9409-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="d9409-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="d9409-112">Область:</span><span class="sxs-lookup"><span data-stu-id="d9409-112">Area:</span></span>  <br/> |<span data-ttu-id="d9409-113">MAPI передаваемого</span><span class="sxs-lookup"><span data-stu-id="d9409-113">MAPI non-transmittable</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d9409-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="d9409-114">Remarks</span></span>

<span data-ttu-id="d9409-115">Это свойство отображается только на содержимое таблиц.</span><span class="sxs-lookup"><span data-stu-id="d9409-115">This property appears only on contents tables.</span></span> <span data-ttu-id="d9409-116">Категории существует только в том случае, если он имеет элементов.</span><span class="sxs-lookup"><span data-stu-id="d9409-116">A category only exists when it has items.</span></span>
  
<span data-ttu-id="d9409-117">Это свойство может иметь только один из следующих значений:</span><span class="sxs-lookup"><span data-stu-id="d9409-117">This property can have exactly one of the following values:</span></span>
  
<span data-ttu-id="d9409-118">TBL_LEAF_ROW</span><span class="sxs-lookup"><span data-stu-id="d9409-118">TBL_LEAF_ROW</span></span> 
  
> <span data-ttu-id="d9409-119">Представляет фактические данные, а не строкой категории.</span><span class="sxs-lookup"><span data-stu-id="d9409-119">Represents actual data, rather than a category row.</span></span>
    
<span data-ttu-id="d9409-120">TBL_EMPTY_CATEGORY</span><span class="sxs-lookup"><span data-stu-id="d9409-120">TBL_EMPTY_CATEGORY</span></span> 
  
> <span data-ttu-id="d9409-121">В настоящее время не используется.</span><span class="sxs-lookup"><span data-stu-id="d9409-121">Not currently used.</span></span>
    
<span data-ttu-id="d9409-122">TBL_EXPANDED_CATEGORY</span><span class="sxs-lookup"><span data-stu-id="d9409-122">TBL_EXPANDED_CATEGORY</span></span> 
  
> <span data-ttu-id="d9409-123">Категории развернут; в пользовательском интерфейсе это обычно отображается со знаком минус (-) рядом с ним.</span><span class="sxs-lookup"><span data-stu-id="d9409-123">The category is expanded; the user interface usually displays this with the minus sign ( - ) next to it.</span></span>
    
<span data-ttu-id="d9409-124">TBL_COLLAPSED_CATEGORY</span><span class="sxs-lookup"><span data-stu-id="d9409-124">TBL_COLLAPSED_CATEGORY</span></span> 
  
> <span data-ttu-id="d9409-125">Категории свернута; в пользовательском интерфейсе это обычно отображается с значок "плюс" (+) рядом с ним.</span><span class="sxs-lookup"><span data-stu-id="d9409-125">The category is collapsed; the user interface usually displays this with the plus sign (+) next to it.</span></span>
    
## <a name="related-resources"></a><span data-ttu-id="d9409-126">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="d9409-126">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="d9409-127">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="d9409-127">Protocol specifications</span></span>

<span data-ttu-id="d9409-128">[[MS-OXCTABL]](http://msdn.microsoft.com/library/d33612dc-36a8-4623-8a26-c156cf8aae4b%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="d9409-128">[[MS-OXCTABL]](http://msdn.microsoft.com/library/d33612dc-36a8-4623-8a26-c156cf8aae4b%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="d9409-129">Включает в себя разрешенных операций для базовых объектов в таблице.</span><span class="sxs-lookup"><span data-stu-id="d9409-129">Includes permissible operations for the core table objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="d9409-130">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="d9409-130">Header files</span></span>

<span data-ttu-id="d9409-131">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="d9409-131">Mapidefs.h</span></span>
  
> <span data-ttu-id="d9409-132">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="d9409-132">Provides data type definitions.</span></span>
    
<span data-ttu-id="d9409-133">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="d9409-133">Mapitags.h</span></span>
  
> <span data-ttu-id="d9409-134">Содержит определения свойства в списке альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="d9409-134">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="d9409-135">См. также</span><span class="sxs-lookup"><span data-stu-id="d9409-135">See also</span></span>



[<span data-ttu-id="d9409-136">Каноническое свойство PidTagRowid</span><span class="sxs-lookup"><span data-stu-id="d9409-136">PidTagRowid Canonical Property</span></span>](pidtagrowid-canonical-property.md)


[<span data-ttu-id="d9409-137">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="d9409-137">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="d9409-138">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="d9409-138">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="d9409-139">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="d9409-139">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="d9409-140">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="d9409-140">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

