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
ms.openlocfilehash: 75d390edd06aaf826f6b8c2d996e4e08bf6a7334
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360853"
---
# <a name="pidtagdepth-canonical-property"></a><span data-ttu-id="0fe4b-103">Каноническое свойство PidTagDepth</span><span class="sxs-lookup"><span data-stu-id="0fe4b-103">PidTagDepth Canonical Property</span></span>

  
  
<span data-ttu-id="0fe4b-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0fe4b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0fe4b-105">Содержит integer, которое представляет относительный уровень отступа или глубины объекта в таблице иерархии.</span><span class="sxs-lookup"><span data-stu-id="0fe4b-105">Contains an integer that represents the relative level of indentation, or depth, of an object in a hierarchy table.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="0fe4b-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="0fe4b-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="0fe4b-107">PR_DEPTH</span><span class="sxs-lookup"><span data-stu-id="0fe4b-107">PR_DEPTH</span></span>  <br/> |
|<span data-ttu-id="0fe4b-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="0fe4b-108">Identifier:</span></span>  <br/> |<span data-ttu-id="0fe4b-109">0x3005</span><span class="sxs-lookup"><span data-stu-id="0fe4b-109">0x3005</span></span>  <br/> |
|<span data-ttu-id="0fe4b-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="0fe4b-110">Data type:</span></span>  <br/> |<span data-ttu-id="0fe4b-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="0fe4b-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="0fe4b-112">Область:</span><span class="sxs-lookup"><span data-stu-id="0fe4b-112">Area:</span></span>  <br/> |<span data-ttu-id="0fe4b-113">Общие MAPI</span><span class="sxs-lookup"><span data-stu-id="0fe4b-113">MAPI common</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="0fe4b-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="0fe4b-114">Remarks</span></span>

<span data-ttu-id="0fe4b-115">Это свойство также может указывать уровень категоризации строки в таблице содержимого или глубину иерархии в таблице иерархии.</span><span class="sxs-lookup"><span data-stu-id="0fe4b-115">This property can also specify the categorization level of a row in a contents table or the hierarchy depth in a hierarchy table.</span></span> <span data-ttu-id="0fe4b-116">Глубина от нуля, где ноль представляет собой левую категорию.</span><span class="sxs-lookup"><span data-stu-id="0fe4b-116">The depth is zero-based, where zero represents the leftmost category.</span></span> <span data-ttu-id="0fe4b-117">Во всех случаях значение свойства представляет относительное значение, а не абсолютное значение.</span><span class="sxs-lookup"><span data-stu-id="0fe4b-117">In all cases, the property value represents a relative value rather than an absolute value.</span></span> <span data-ttu-id="0fe4b-118">Например, в таблице иерархии значение глубины относительно контейнера, из которого была извлечена таблица иерархии.</span><span class="sxs-lookup"><span data-stu-id="0fe4b-118">In the hierarchy table, for example, the depth value is relative to the container from which the hierarchy table was retrieved.</span></span> <span data-ttu-id="0fe4b-119">Глубина не представляет абсолютной глубины из корневого контейнера.</span><span class="sxs-lookup"><span data-stu-id="0fe4b-119">The depth does not represent an absolute depth from the root container.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="0fe4b-120">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="0fe4b-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="0fe4b-121">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="0fe4b-121">Protocol specifications</span></span>

<span data-ttu-id="0fe4b-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="0fe4b-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="0fe4b-123">Содержит ссылки на связанные Exchange Server протоколы.</span><span class="sxs-lookup"><span data-stu-id="0fe4b-123">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="0fe4b-124">[[MS-OXCTABL]](https://msdn.microsoft.com/library/d33612dc-36a8-4623-8a26-c156cf8aae4b%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="0fe4b-124">[[MS-OXCTABL]](https://msdn.microsoft.com/library/d33612dc-36a8-4623-8a26-c156cf8aae4b%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="0fe4b-125">Включает допустимые операции для основных объектов таблицы.</span><span class="sxs-lookup"><span data-stu-id="0fe4b-125">Includes permissible operations for the core table objects.</span></span>
    
<span data-ttu-id="0fe4b-126">[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="0fe4b-126">[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="0fe4b-127">Указывает свойства и операции для списков пользователей, контактов, групп и ресурсов.</span><span class="sxs-lookup"><span data-stu-id="0fe4b-127">Specifies the properties and operations for lists of users, contacts, groups, and resources.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="0fe4b-128">Файлы заголовок</span><span class="sxs-lookup"><span data-stu-id="0fe4b-128">Header files</span></span>

<span data-ttu-id="0fe4b-129">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="0fe4b-129">Mapidefs.h</span></span>
  
> <span data-ttu-id="0fe4b-130">Предоставляет определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="0fe4b-130">Provides data type definitions.</span></span>
    
<span data-ttu-id="0fe4b-131">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="0fe4b-131">Mapitags.h</span></span>
  
> <span data-ttu-id="0fe4b-132">Содержит определения свойств, перечисленных в качестве альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="0fe4b-132">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="0fe4b-133">См. также</span><span class="sxs-lookup"><span data-stu-id="0fe4b-133">See also</span></span>



[<span data-ttu-id="0fe4b-134">Каноническое свойство PidTagObjectType</span><span class="sxs-lookup"><span data-stu-id="0fe4b-134">PidTagObjectType Canonical Property</span></span>](pidtagobjecttype-canonical-property.md)
  
[<span data-ttu-id="0fe4b-135">Каноническое свойство PidTagSelectable</span><span class="sxs-lookup"><span data-stu-id="0fe4b-135">PidTagSelectable Canonical Property</span></span>](pidtagselectable-canonical-property.md)


[<span data-ttu-id="0fe4b-136">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="0fe4b-136">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="0fe4b-137">Канонические свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="0fe4b-137">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="0fe4b-138">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="0fe4b-138">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="0fe4b-139">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="0fe4b-139">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

