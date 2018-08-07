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
ms.openlocfilehash: cae4ef6e4d7634ca2b429eb946aa948f5d90cd92
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19812049"
---
# <a name="pidtagtodoitemflags-canonical-property"></a><span data-ttu-id="18d18-103">Каноническое свойство PidTagToDoItemFlags</span><span class="sxs-lookup"><span data-stu-id="18d18-103">PidTagToDoItemFlags Canonical Property</span></span>

  
  
<span data-ttu-id="18d18-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="18d18-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="18d18-105">Представляет условие отмеченного элемента списка дел.</span><span class="sxs-lookup"><span data-stu-id="18d18-105">Represents a To-Do item's flagged condition.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="18d18-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="18d18-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="18d18-107">PR_TODO_ITEM_FLAGS</span><span class="sxs-lookup"><span data-stu-id="18d18-107">PR_TODO_ITEM_FLAGS</span></span>  <br/> |
|<span data-ttu-id="18d18-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="18d18-108">Identifier:</span></span>  <br/> |<span data-ttu-id="18d18-109">0x0E2B</span><span class="sxs-lookup"><span data-stu-id="18d18-109">0x0E2B</span></span>  <br/> |
|<span data-ttu-id="18d18-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="18d18-110">Data type:</span></span>  <br/> |<span data-ttu-id="18d18-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="18d18-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="18d18-112">Область:</span><span class="sxs-lookup"><span data-stu-id="18d18-112">Area:</span></span>  <br/> |<span data-ttu-id="18d18-113">MAPI передаваемого</span><span class="sxs-lookup"><span data-stu-id="18d18-113">MAPI non-transmittable</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="18d18-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="18d18-114">Remarks</span></span>

<span data-ttu-id="18d18-115">Это свойство представляет битовое поле, в котором каждый бит необходимо задать значение 1 ситуациях связанного условие в следующей таблице, в противном случае — 0.</span><span class="sxs-lookup"><span data-stu-id="18d18-115">This property is a bit field in which each bit should be set to 1 if the associated condition in the following table applies, otherwise 0.</span></span>
  
||||
|:-----|:-----|:-----|
|<span data-ttu-id="18d18-116">Числовое значение</span><span class="sxs-lookup"><span data-stu-id="18d18-116">Numeric value</span></span>  <br/> |<span data-ttu-id="18d18-117">Имя</span><span class="sxs-lookup"><span data-stu-id="18d18-117">Name</span></span>  <br/> |<span data-ttu-id="18d18-118">Описание</span><span class="sxs-lookup"><span data-stu-id="18d18-118">Description</span></span>  <br/> |
|<span data-ttu-id="18d18-119">Этот параметр не указан</span><span class="sxs-lookup"><span data-stu-id="18d18-119">Not present</span></span>  <br/> |<span data-ttu-id="18d18-120">Нет</span><span class="sxs-lookup"><span data-stu-id="18d18-120">N/A</span></span>  <br/> |<span data-ttu-id="18d18-121">Без отметки</span><span class="sxs-lookup"><span data-stu-id="18d18-121">Unflagged</span></span>  <br/> |
|<span data-ttu-id="18d18-122">1</span><span class="sxs-lookup"><span data-stu-id="18d18-122">1</span></span>  <br/> |<span data-ttu-id="18d18-123">todoTimeFlagged</span><span class="sxs-lookup"><span data-stu-id="18d18-123">todoTimeFlagged</span></span>  <br/> |<span data-ttu-id="18d18-124">Объект является отметкой времени</span><span class="sxs-lookup"><span data-stu-id="18d18-124">Object is time flagged</span></span>  <br/> |
|<span data-ttu-id="18d18-125">8</span><span class="sxs-lookup"><span data-stu-id="18d18-125">8</span></span>  <br/> |<span data-ttu-id="18d18-126">todoRecipientFlagged</span><span class="sxs-lookup"><span data-stu-id="18d18-126">todoRecipientFlagged</span></span>  <br/> |<span data-ttu-id="18d18-127">Должны быть установлены только на объект черновика сообщения, а это означает, что объект имеет флаг для получателей.</span><span class="sxs-lookup"><span data-stu-id="18d18-127">Should only be set on a draft message object, and it means that the object is flagged for recipients.</span></span>  <br/> |
   
<span data-ttu-id="18d18-128">Зарезервированные все биты, не указанные в таблице.</span><span class="sxs-lookup"><span data-stu-id="18d18-128">All bits that are not specified in the table are reserved.</span></span> <span data-ttu-id="18d18-129">Они должны игнорироваться, но должны быть сохранены, если они определены.</span><span class="sxs-lookup"><span data-stu-id="18d18-129">They must be ignored, but should be preserved if they are set.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="18d18-130">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="18d18-130">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="18d18-131">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="18d18-131">Protocol specifications</span></span>

<span data-ttu-id="18d18-132">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="18d18-132">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="18d18-133">Содержит ссылки на связанные спецификаций протокола Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="18d18-133">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="18d18-134">[[MS-OXOFLAG]](http://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="18d18-134">[[MS-OXOFLAG]](http://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="18d18-135">Задает свойства и операции, связанные с флагов.</span><span class="sxs-lookup"><span data-stu-id="18d18-135">Specifies the properties and operations related to flagging.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="18d18-136">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="18d18-136">Header files</span></span>

<span data-ttu-id="18d18-137">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="18d18-137">Mapidefs.h</span></span>
  
> <span data-ttu-id="18d18-138">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="18d18-138">Provides data type definitions.</span></span>
    
<span data-ttu-id="18d18-139">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="18d18-139">Mapitags.h</span></span>
  
> <span data-ttu-id="18d18-140">Содержит определения свойства в списке альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="18d18-140">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="18d18-141">См. также</span><span class="sxs-lookup"><span data-stu-id="18d18-141">See also</span></span>



[<span data-ttu-id="18d18-142">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="18d18-142">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="18d18-143">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="18d18-143">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="18d18-144">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="18d18-144">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="18d18-145">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="18d18-145">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

