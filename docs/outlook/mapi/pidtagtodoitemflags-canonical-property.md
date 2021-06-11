---
title: Каноническое свойство PidTagToDoItemFlags
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagToDoItemFlags
api_type:
- COM
ms.assetid: bb7ccb45-ce08-4d22-9259-db15cd267e34
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 6ddc7231afef0a224b92be7fe86216e56200ab70
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32284485"
---
# <a name="pidtagtodoitemflags-canonical-property"></a><span data-ttu-id="87b89-103">Каноническое свойство PidTagToDoItemFlags</span><span class="sxs-lookup"><span data-stu-id="87b89-103">PidTagToDoItemFlags Canonical Property</span></span>

  
  
<span data-ttu-id="87b89-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="87b89-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="87b89-105">Представляет состояние To-Do помеченного элемента.</span><span class="sxs-lookup"><span data-stu-id="87b89-105">Represents a To-Do item's flagged condition.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="87b89-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="87b89-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="87b89-107">PR_TODO_ITEM_FLAGS</span><span class="sxs-lookup"><span data-stu-id="87b89-107">PR_TODO_ITEM_FLAGS</span></span>  <br/> |
|<span data-ttu-id="87b89-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="87b89-108">Identifier:</span></span>  <br/> |<span data-ttu-id="87b89-109">0x0E2B</span><span class="sxs-lookup"><span data-stu-id="87b89-109">0x0E2B</span></span>  <br/> |
|<span data-ttu-id="87b89-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="87b89-110">Data type:</span></span>  <br/> |<span data-ttu-id="87b89-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="87b89-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="87b89-112">Область:</span><span class="sxs-lookup"><span data-stu-id="87b89-112">Area:</span></span>  <br/> |<span data-ttu-id="87b89-113">MAPI, не передаваемая</span><span class="sxs-lookup"><span data-stu-id="87b89-113">MAPI non-transmittable</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="87b89-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="87b89-114">Remarks</span></span>

<span data-ttu-id="87b89-115">Это свойство является битным полем, в котором каждый бит должен быть установлен до 1, если применяется связанное условие в следующей таблице, в противном случае 0.</span><span class="sxs-lookup"><span data-stu-id="87b89-115">This property is a bit field in which each bit should be set to 1 if the associated condition in the following table applies, otherwise 0.</span></span>
  
||||
|:-----|:-----|:-----|
|<span data-ttu-id="87b89-116">Числовая величина</span><span class="sxs-lookup"><span data-stu-id="87b89-116">Numeric value</span></span>  <br/> |<span data-ttu-id="87b89-117">Имя</span><span class="sxs-lookup"><span data-stu-id="87b89-117">Name</span></span>  <br/> |<span data-ttu-id="87b89-118">Описание</span><span class="sxs-lookup"><span data-stu-id="87b89-118">Description</span></span>  <br/> |
|<span data-ttu-id="87b89-119">Не присутствует</span><span class="sxs-lookup"><span data-stu-id="87b89-119">Not present</span></span>  <br/> |<span data-ttu-id="87b89-120">Н/Д</span><span class="sxs-lookup"><span data-stu-id="87b89-120">N/A</span></span>  <br/> |<span data-ttu-id="87b89-121">Unflagged</span><span class="sxs-lookup"><span data-stu-id="87b89-121">Unflagged</span></span>  <br/> |
|<span data-ttu-id="87b89-122">1</span><span class="sxs-lookup"><span data-stu-id="87b89-122">1</span></span>  <br/> |<span data-ttu-id="87b89-123">todoTimeFlagged</span><span class="sxs-lookup"><span data-stu-id="87b89-123">todoTimeFlagged</span></span>  <br/> |<span data-ttu-id="87b89-124">Объект помечен временем</span><span class="sxs-lookup"><span data-stu-id="87b89-124">Object is time flagged</span></span>  <br/> |
|<span data-ttu-id="87b89-125">8 </span><span class="sxs-lookup"><span data-stu-id="87b89-125">8</span></span>  <br/> |<span data-ttu-id="87b89-126">todoRecipientFlagged</span><span class="sxs-lookup"><span data-stu-id="87b89-126">todoRecipientFlagged</span></span>  <br/> |<span data-ttu-id="87b89-127">Следует установить только объект черновика сообщения, а это означает, что объект помечен для получателей.</span><span class="sxs-lookup"><span data-stu-id="87b89-127">Should only be set on a draft message object, and it means that the object is flagged for recipients.</span></span>  <br/> |
   
<span data-ttu-id="87b89-128">Все биты, не указанные в таблице, зарезервированы.</span><span class="sxs-lookup"><span data-stu-id="87b89-128">All bits that are not specified in the table are reserved.</span></span> <span data-ttu-id="87b89-129">Они должны быть проигнорированы, но должны быть сохранены, если они установлены.</span><span class="sxs-lookup"><span data-stu-id="87b89-129">They must be ignored, but should be preserved if they are set.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="87b89-130">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="87b89-130">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="87b89-131">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="87b89-131">Protocol specifications</span></span>

<span data-ttu-id="87b89-132">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="87b89-132">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="87b89-133">Содержит ссылки на связанные Exchange Server протоколы.</span><span class="sxs-lookup"><span data-stu-id="87b89-133">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="87b89-134">[[MS-OXOFLAG]](https://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="87b89-134">[[MS-OXOFLAG]](https://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="87b89-135">Указывает свойства и операции, связанные с маркировкой.</span><span class="sxs-lookup"><span data-stu-id="87b89-135">Specifies the properties and operations related to flagging.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="87b89-136">Файлы заголовки</span><span class="sxs-lookup"><span data-stu-id="87b89-136">Header files</span></span>

<span data-ttu-id="87b89-137">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="87b89-137">Mapidefs.h</span></span>
  
> <span data-ttu-id="87b89-138">Предоставляет определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="87b89-138">Provides data type definitions.</span></span>
    
<span data-ttu-id="87b89-139">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="87b89-139">Mapitags.h</span></span>
  
> <span data-ttu-id="87b89-140">Содержит определения свойств, перечисленных в качестве альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="87b89-140">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="87b89-141">См. также</span><span class="sxs-lookup"><span data-stu-id="87b89-141">See also</span></span>



[<span data-ttu-id="87b89-142">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="87b89-142">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="87b89-143">Канонические свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="87b89-143">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="87b89-144">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="87b89-144">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="87b89-145">Сопоставление имен MAPI с каноническими именами свойств</span><span class="sxs-lookup"><span data-stu-id="87b89-145">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

