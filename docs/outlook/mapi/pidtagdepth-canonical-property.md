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
# <a name="pidtagdepth-canonical-property"></a><span data-ttu-id="cdc10-103">Каноническое свойство PidTagDepth</span><span class="sxs-lookup"><span data-stu-id="cdc10-103">PidTagDepth Canonical Property</span></span>

  
  
<span data-ttu-id="cdc10-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="cdc10-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="cdc10-105">Содержит целое число, представляющее относительный уровень отступа или глубины объекта в таблице иерархий.</span><span class="sxs-lookup"><span data-stu-id="cdc10-105">Contains an integer that represents the relative level of indentation, or depth, of an object in a hierarchy table.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="cdc10-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="cdc10-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="cdc10-107">PR_DEPTH</span><span class="sxs-lookup"><span data-stu-id="cdc10-107">PR_DEPTH</span></span>  <br/> |
|<span data-ttu-id="cdc10-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="cdc10-108">Identifier:</span></span>  <br/> |<span data-ttu-id="cdc10-109">0x3005</span><span class="sxs-lookup"><span data-stu-id="cdc10-109">0x3005</span></span>  <br/> |
|<span data-ttu-id="cdc10-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="cdc10-110">Data type:</span></span>  <br/> |<span data-ttu-id="cdc10-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="cdc10-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="cdc10-112">Область:</span><span class="sxs-lookup"><span data-stu-id="cdc10-112">Area:</span></span>  <br/> |<span data-ttu-id="cdc10-113">Общие протоколы MAPI</span><span class="sxs-lookup"><span data-stu-id="cdc10-113">MAPI common</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="cdc10-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="cdc10-114">Remarks</span></span>

<span data-ttu-id="cdc10-115">В этом свойстве также можно указать уровень классификации строки в таблице содержимого или глубину иерархии в таблице иерархий.</span><span class="sxs-lookup"><span data-stu-id="cdc10-115">This property can also specify the categorization level of a row in a contents table or the hierarchy depth in a hierarchy table.</span></span> <span data-ttu-id="cdc10-116">Глубина отсчета от нуля, где ноль соответствует самой левой категории.</span><span class="sxs-lookup"><span data-stu-id="cdc10-116">The depth is zero-based, where zero represents the leftmost category.</span></span> <span data-ttu-id="cdc10-117">Во всех случаях значение свойства представляет относительное значение, а не абсолютное значение.</span><span class="sxs-lookup"><span data-stu-id="cdc10-117">In all cases, the property value represents a relative value rather than an absolute value.</span></span> <span data-ttu-id="cdc10-118">Например, в таблице иерархий значение глубины задается относительно контейнера, из которого была получена таблица иерархии.</span><span class="sxs-lookup"><span data-stu-id="cdc10-118">In the hierarchy table, for example, the depth value is relative to the container from which the hierarchy table was retrieved.</span></span> <span data-ttu-id="cdc10-119">Глубина не представляет абсолютную глубину из корневого контейнера.</span><span class="sxs-lookup"><span data-stu-id="cdc10-119">The depth does not represent an absolute depth from the root container.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="cdc10-120">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="cdc10-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="cdc10-121">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="cdc10-121">Protocol specifications</span></span>

<span data-ttu-id="cdc10-122">[[MS — ОКСПРОПС]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="cdc10-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="cdc10-123">Содержит ссылки на соответствующие спецификации протоколов Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="cdc10-123">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="cdc10-124">[[MS — ОКСКТАБЛ]](https://msdn.microsoft.com/library/d33612dc-36a8-4623-8a26-c156cf8aae4b%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="cdc10-124">[[MS-OXCTABL]](https://msdn.microsoft.com/library/d33612dc-36a8-4623-8a26-c156cf8aae4b%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="cdc10-125">Включает в себя допустимые операции для основных объектов Table.</span><span class="sxs-lookup"><span data-stu-id="cdc10-125">Includes permissible operations for the core table objects.</span></span>
    
<span data-ttu-id="cdc10-126">[[MS — ОКСОАБК]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="cdc10-126">[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="cdc10-127">Задает свойства и операции для списков пользователей, контактов, групп и ресурсов.</span><span class="sxs-lookup"><span data-stu-id="cdc10-127">Specifies the properties and operations for lists of users, contacts, groups, and resources.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="cdc10-128">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="cdc10-128">Header files</span></span>

<span data-ttu-id="cdc10-129">MAPIDEFS. h</span><span class="sxs-lookup"><span data-stu-id="cdc10-129">Mapidefs.h</span></span>
  
> <span data-ttu-id="cdc10-130">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="cdc10-130">Provides data type definitions.</span></span>
    
<span data-ttu-id="cdc10-131">Мапитагс. h</span><span class="sxs-lookup"><span data-stu-id="cdc10-131">Mapitags.h</span></span>
  
> <span data-ttu-id="cdc10-132">Содержит определения свойств, перечисленных как альтернативные имена.</span><span class="sxs-lookup"><span data-stu-id="cdc10-132">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="cdc10-133">См. также</span><span class="sxs-lookup"><span data-stu-id="cdc10-133">See also</span></span>



[<span data-ttu-id="cdc10-134">Каноническое свойство PidTagObjectType</span><span class="sxs-lookup"><span data-stu-id="cdc10-134">PidTagObjectType Canonical Property</span></span>](pidtagobjecttype-canonical-property.md)
  
[<span data-ttu-id="cdc10-135">Каноническое свойство PidTagSelectable</span><span class="sxs-lookup"><span data-stu-id="cdc10-135">PidTagSelectable Canonical Property</span></span>](pidtagselectable-canonical-property.md)


[<span data-ttu-id="cdc10-136">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="cdc10-136">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="cdc10-137">Каноническое свойство MAPI</span><span class="sxs-lookup"><span data-stu-id="cdc10-137">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="cdc10-138">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="cdc10-138">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="cdc10-139">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="cdc10-139">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

