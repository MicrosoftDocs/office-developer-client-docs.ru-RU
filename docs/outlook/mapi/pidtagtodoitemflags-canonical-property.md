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
ms.openlocfilehash: 79f6c90d1ebd2257cc428e88dfce3d9ee9dfeccf
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22573469"
---
# <a name="pidtagtodoitemflags-canonical-property"></a><span data-ttu-id="9e878-103">Каноническое свойство PidTagToDoItemFlags</span><span class="sxs-lookup"><span data-stu-id="9e878-103">PidTagToDoItemFlags Canonical Property</span></span>

  
  
<span data-ttu-id="9e878-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9e878-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9e878-105">Представляет условие отмеченного элемента списка дел.</span><span class="sxs-lookup"><span data-stu-id="9e878-105">Represents a To-Do item's flagged condition.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="9e878-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="9e878-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="9e878-107">PR_TODO_ITEM_FLAGS</span><span class="sxs-lookup"><span data-stu-id="9e878-107">PR_TODO_ITEM_FLAGS</span></span>  <br/> |
|<span data-ttu-id="9e878-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="9e878-108">Identifier:</span></span>  <br/> |<span data-ttu-id="9e878-109">0x0E2B</span><span class="sxs-lookup"><span data-stu-id="9e878-109">0x0E2B</span></span>  <br/> |
|<span data-ttu-id="9e878-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="9e878-110">Data type:</span></span>  <br/> |<span data-ttu-id="9e878-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="9e878-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="9e878-112">Область:</span><span class="sxs-lookup"><span data-stu-id="9e878-112">Area:</span></span>  <br/> |<span data-ttu-id="9e878-113">MAPI передаваемого</span><span class="sxs-lookup"><span data-stu-id="9e878-113">MAPI non-transmittable</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="9e878-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="9e878-114">Remarks</span></span>

<span data-ttu-id="9e878-115">Это свойство представляет битовое поле, в котором каждый бит необходимо задать значение 1 ситуациях связанного условие в следующей таблице, в противном случае — 0.</span><span class="sxs-lookup"><span data-stu-id="9e878-115">This property is a bit field in which each bit should be set to 1 if the associated condition in the following table applies, otherwise 0.</span></span>
  
||||
|:-----|:-----|:-----|
|<span data-ttu-id="9e878-116">Числовое значение</span><span class="sxs-lookup"><span data-stu-id="9e878-116">Numeric value</span></span>  <br/> |<span data-ttu-id="9e878-117">Имя</span><span class="sxs-lookup"><span data-stu-id="9e878-117">Name</span></span>  <br/> |<span data-ttu-id="9e878-118">Описание</span><span class="sxs-lookup"><span data-stu-id="9e878-118">Description</span></span>  <br/> |
|<span data-ttu-id="9e878-119">Этот параметр не указан</span><span class="sxs-lookup"><span data-stu-id="9e878-119">Not present</span></span>  <br/> |<span data-ttu-id="9e878-120">Н/Д</span><span class="sxs-lookup"><span data-stu-id="9e878-120">N/A</span></span>  <br/> |<span data-ttu-id="9e878-121">Без отметки</span><span class="sxs-lookup"><span data-stu-id="9e878-121">Unflagged</span></span>  <br/> |
|<span data-ttu-id="9e878-122">1</span><span class="sxs-lookup"><span data-stu-id="9e878-122">1</span></span>  <br/> |<span data-ttu-id="9e878-123">todoTimeFlagged</span><span class="sxs-lookup"><span data-stu-id="9e878-123">todoTimeFlagged</span></span>  <br/> |<span data-ttu-id="9e878-124">Объект является отметкой времени</span><span class="sxs-lookup"><span data-stu-id="9e878-124">Object is time flagged</span></span>  <br/> |
|<span data-ttu-id="9e878-125">8</span><span class="sxs-lookup"><span data-stu-id="9e878-125">8</span></span>  <br/> |<span data-ttu-id="9e878-126">todoRecipientFlagged</span><span class="sxs-lookup"><span data-stu-id="9e878-126">todoRecipientFlagged</span></span>  <br/> |<span data-ttu-id="9e878-127">Должны быть установлены только на объект черновика сообщения, а это означает, что объект имеет флаг для получателей.</span><span class="sxs-lookup"><span data-stu-id="9e878-127">Should only be set on a draft message object, and it means that the object is flagged for recipients.</span></span>  <br/> |
   
<span data-ttu-id="9e878-128">Зарезервированные все биты, не указанные в таблице.</span><span class="sxs-lookup"><span data-stu-id="9e878-128">All bits that are not specified in the table are reserved.</span></span> <span data-ttu-id="9e878-129">Они должны игнорироваться, но должны быть сохранены, если они определены.</span><span class="sxs-lookup"><span data-stu-id="9e878-129">They must be ignored, but should be preserved if they are set.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="9e878-130">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="9e878-130">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="9e878-131">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="9e878-131">Protocol specifications</span></span>

<span data-ttu-id="9e878-132">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="9e878-132">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="9e878-133">Содержит ссылки на связанные спецификаций протокола Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="9e878-133">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="9e878-134">[[MS-OXOFLAG]](http://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="9e878-134">[[MS-OXOFLAG]](http://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="9e878-135">Задает свойства и операции, связанные с флагов.</span><span class="sxs-lookup"><span data-stu-id="9e878-135">Specifies the properties and operations related to flagging.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="9e878-136">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="9e878-136">Header files</span></span>

<span data-ttu-id="9e878-137">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="9e878-137">Mapidefs.h</span></span>
  
> <span data-ttu-id="9e878-138">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="9e878-138">Provides data type definitions.</span></span>
    
<span data-ttu-id="9e878-139">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="9e878-139">Mapitags.h</span></span>
  
> <span data-ttu-id="9e878-140">Содержит определения свойства в списке альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="9e878-140">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="9e878-141">См. также</span><span class="sxs-lookup"><span data-stu-id="9e878-141">See also</span></span>



[<span data-ttu-id="9e878-142">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="9e878-142">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="9e878-143">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="9e878-143">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="9e878-144">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="9e878-144">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="9e878-145">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="9e878-145">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

