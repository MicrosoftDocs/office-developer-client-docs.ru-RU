---
title: Каноническое свойство PidTagDepth
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagDepth
api_type:
- HeaderDef
ms.assetid: 04d444a5-e97f-48e6-89a5-8a6cb2136408
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 25af87004ef5616a6c6fc575c647fdd1794d710f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19811054"
---
# <a name="pidtagdepth-canonical-property"></a><span data-ttu-id="3c5ad-103">Каноническое свойство PidTagDepth</span><span class="sxs-lookup"><span data-stu-id="3c5ad-103">PidTagDepth Canonical Property</span></span>

  
  
<span data-ttu-id="3c5ad-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="3c5ad-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="3c5ad-105">Содержит целое число, представляющее относительный уровень отступа или глубину объекта в таблице иерархии.</span><span class="sxs-lookup"><span data-stu-id="3c5ad-105">Contains an integer that represents the relative level of indentation, or depth, of an object in a hierarchy table.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="3c5ad-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="3c5ad-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="3c5ad-107">PR_DEPTH</span><span class="sxs-lookup"><span data-stu-id="3c5ad-107">PR_DEPTH</span></span>  <br/> |
|<span data-ttu-id="3c5ad-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="3c5ad-108">Identifier:</span></span>  <br/> |<span data-ttu-id="3c5ad-109">0x3005</span><span class="sxs-lookup"><span data-stu-id="3c5ad-109">0x3005</span></span>  <br/> |
|<span data-ttu-id="3c5ad-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="3c5ad-110">Data type:</span></span>  <br/> |<span data-ttu-id="3c5ad-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="3c5ad-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="3c5ad-112">Область:</span><span class="sxs-lookup"><span data-stu-id="3c5ad-112">Area:</span></span>  <br/> |<span data-ttu-id="3c5ad-113">Распространенные MAPI</span><span class="sxs-lookup"><span data-stu-id="3c5ad-113">MAPI common</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="3c5ad-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="3c5ad-114">Remarks</span></span>

<span data-ttu-id="3c5ad-115">Это свойство можно также задать уровень категоризации строки в таблицу содержимого или число уровней в иерархии в таблице иерархии.</span><span class="sxs-lookup"><span data-stu-id="3c5ad-115">This property can also specify the categorization level of a row in a contents table or the hierarchy depth in a hierarchy table.</span></span> <span data-ttu-id="3c5ad-116">Глубина с отсчетом от нуля, где нулевой представляет самые левые категории.</span><span class="sxs-lookup"><span data-stu-id="3c5ad-116">The depth is zero-based, where zero represents the leftmost category.</span></span> <span data-ttu-id="3c5ad-117">Во всех случаях относительное значение, а не абсолютное значение представляет значение свойства.</span><span class="sxs-lookup"><span data-stu-id="3c5ad-117">In all cases, the property value represents a relative value rather than an absolute value.</span></span> <span data-ttu-id="3c5ad-118">В таблице иерархии, например значение глубины — относительно контейнера, из которого извлекается таблицы иерархии.</span><span class="sxs-lookup"><span data-stu-id="3c5ad-118">In the hierarchy table, for example, the depth value is relative to the container from which the hierarchy table was retrieved.</span></span> <span data-ttu-id="3c5ad-119">Глубина не представляет абсолютный глубины из корневого контейнера.</span><span class="sxs-lookup"><span data-stu-id="3c5ad-119">The depth does not represent an absolute depth from the root container.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="3c5ad-120">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="3c5ad-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="3c5ad-121">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="3c5ad-121">Protocol specifications</span></span>

<span data-ttu-id="3c5ad-122">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="3c5ad-122">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="3c5ad-123">Содержит ссылки на связанные спецификаций протокола Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="3c5ad-123">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="3c5ad-124">[[MS-OXCTABL]](http://msdn.microsoft.com/library/d33612dc-36a8-4623-8a26-c156cf8aae4b%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="3c5ad-124">[[MS-OXCTABL]](http://msdn.microsoft.com/library/d33612dc-36a8-4623-8a26-c156cf8aae4b%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="3c5ad-125">Включает в себя разрешенных операций для базовых объектов в таблице.</span><span class="sxs-lookup"><span data-stu-id="3c5ad-125">Includes permissible operations for the core table objects.</span></span>
    
<span data-ttu-id="3c5ad-126">[[MS-OXOABK]](http://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="3c5ad-126">[[MS-OXOABK]](http://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="3c5ad-127">Задает свойства и операции для списков пользователей, контактов, групп и ресурсов.</span><span class="sxs-lookup"><span data-stu-id="3c5ad-127">Specifies the properties and operations for lists of users, contacts, groups, and resources.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="3c5ad-128">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="3c5ad-128">Header files</span></span>

<span data-ttu-id="3c5ad-129">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="3c5ad-129">Mapidefs.h</span></span>
  
> <span data-ttu-id="3c5ad-130">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="3c5ad-130">Provides data type definitions.</span></span>
    
<span data-ttu-id="3c5ad-131">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="3c5ad-131">Mapitags.h</span></span>
  
> <span data-ttu-id="3c5ad-132">Содержит определения свойства в списке альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="3c5ad-132">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="3c5ad-133">См. также</span><span class="sxs-lookup"><span data-stu-id="3c5ad-133">See also</span></span>



[<span data-ttu-id="3c5ad-134">Каноническое свойство PidTagObjectType</span><span class="sxs-lookup"><span data-stu-id="3c5ad-134">PidTagObjectType Canonical Property</span></span>](pidtagobjecttype-canonical-property.md)
  
[<span data-ttu-id="3c5ad-135">Каноническое свойство PidTagSelectable</span><span class="sxs-lookup"><span data-stu-id="3c5ad-135">PidTagSelectable Canonical Property</span></span>](pidtagselectable-canonical-property.md)


[<span data-ttu-id="3c5ad-136">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="3c5ad-136">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="3c5ad-137">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="3c5ad-137">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="3c5ad-138">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="3c5ad-138">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="3c5ad-139">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="3c5ad-139">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

