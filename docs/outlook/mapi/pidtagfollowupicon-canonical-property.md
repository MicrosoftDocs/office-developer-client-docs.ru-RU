---
title: Каноническое свойство PidTagFollowupIcon
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagFollowupIcon
api_type:
- HeaderDef
ms.assetid: 374cef41-141a-491b-8dd1-eaf1a2044204
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 39840f27d67daca625daea08555ab89d5a362e63
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19811143"
---
# <a name="pidtagfollowupicon-canonical-property"></a><span data-ttu-id="a0546-103">Каноническое свойство PidTagFollowupIcon</span><span class="sxs-lookup"><span data-stu-id="a0546-103">PidTagFollowupIcon Canonical Property</span></span>

  
  
<span data-ttu-id="a0546-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="a0546-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="a0546-105">Указывает цвет объекта message.</span><span class="sxs-lookup"><span data-stu-id="a0546-105">Specifies the flag color of the message object.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="a0546-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="a0546-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="a0546-107">PR_FOLLOWUP_ICON</span><span class="sxs-lookup"><span data-stu-id="a0546-107">PR_FOLLOWUP_ICON</span></span>  <br/> |
|<span data-ttu-id="a0546-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="a0546-108">Identifier:</span></span>  <br/> |<span data-ttu-id="a0546-109">0x1095</span><span class="sxs-lookup"><span data-stu-id="a0546-109">0x1095</span></span>  <br/> |
|<span data-ttu-id="a0546-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="a0546-110">Data type:</span></span>  <br/> |<span data-ttu-id="a0546-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="a0546-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="a0546-112">Область:</span><span class="sxs-lookup"><span data-stu-id="a0546-112">Area:</span></span>  <br/> |<span data-ttu-id="a0546-113">Переименование папки сообщения</span><span class="sxs-lookup"><span data-stu-id="a0546-113">Rename message folder</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a0546-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="a0546-114">Remarks</span></span>

<span data-ttu-id="a0546-115">Это свойство не должна существовать, если значение свойства **PR_FLAG_STATUS** ([PidTagFlagStatus](pidtagflagstatus-canonical-property.md)) имеет значение «followupFlagged» или объект message — это объект, относящихся к собранию.</span><span class="sxs-lookup"><span data-stu-id="a0546-115">This property must not exist unless the value of the **PR_FLAG_STATUS** ([PidTagFlagStatus](pidtagflagstatus-canonical-property.md)) property is set to "followupFlagged", or the message object is a meeting-related object.</span></span> <span data-ttu-id="a0546-116">Это свойство не должна существовать для объекта задачи.</span><span class="sxs-lookup"><span data-stu-id="a0546-116">This property should not exist on a task object.</span></span> <span data-ttu-id="a0546-117">Если установлено на другие объекты сообщения, это свойство должно быть присвоено одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="a0546-117">When set on other message objects, this property must be set to one of the following values.</span></span>
  
|<span data-ttu-id="a0546-118">**Числовое значение**</span><span class="sxs-lookup"><span data-stu-id="a0546-118">**Numeric value**</span></span>|<span data-ttu-id="a0546-119">**Имя**</span><span class="sxs-lookup"><span data-stu-id="a0546-119">**Name**</span></span>|<span data-ttu-id="a0546-120">**Описание**</span><span class="sxs-lookup"><span data-stu-id="a0546-120">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="a0546-121">Этот параметр не указан</span><span class="sxs-lookup"><span data-stu-id="a0546-121">Not present</span></span>  <br/> |<span data-ttu-id="a0546-122">Нет</span><span class="sxs-lookup"><span data-stu-id="a0546-122">N/A</span></span>  <br/> |<span data-ttu-id="a0546-123">Без цвета</span><span class="sxs-lookup"><span data-stu-id="a0546-123">No color</span></span>  <br/> |
|<span data-ttu-id="a0546-124">1</span><span class="sxs-lookup"><span data-stu-id="a0546-124">1</span></span>  <br/> |<span data-ttu-id="a0546-125">followupIcon1</span><span class="sxs-lookup"><span data-stu-id="a0546-125">followupIcon1</span></span>  <br/> |<span data-ttu-id="a0546-126">Лиловый флажок</span><span class="sxs-lookup"><span data-stu-id="a0546-126">Purple flag</span></span>  <br/> |
|<span data-ttu-id="a0546-127">2</span><span class="sxs-lookup"><span data-stu-id="a0546-127">2</span></span>  <br/> |<span data-ttu-id="a0546-128">followupIcon2</span><span class="sxs-lookup"><span data-stu-id="a0546-128">followupIcon2</span></span>  <br/> |<span data-ttu-id="a0546-129">Оранжевый флажок</span><span class="sxs-lookup"><span data-stu-id="a0546-129">Orange flag</span></span>  <br/> |
|<span data-ttu-id="a0546-130">3</span><span class="sxs-lookup"><span data-stu-id="a0546-130">3</span></span>  <br/> |<span data-ttu-id="a0546-131">followupIcon3</span><span class="sxs-lookup"><span data-stu-id="a0546-131">followupIcon3</span></span>  <br/> |<span data-ttu-id="a0546-132">Зеленый флажок</span><span class="sxs-lookup"><span data-stu-id="a0546-132">Green flag</span></span>  <br/> |
|<span data-ttu-id="a0546-133">4</span><span class="sxs-lookup"><span data-stu-id="a0546-133">4</span></span>  <br/> |<span data-ttu-id="a0546-134">followupIcon4</span><span class="sxs-lookup"><span data-stu-id="a0546-134">followupIcon4</span></span>  <br/> |<span data-ttu-id="a0546-135">Желтый флажок</span><span class="sxs-lookup"><span data-stu-id="a0546-135">Yellow flag</span></span>  <br/> |
|<span data-ttu-id="a0546-136">5</span><span class="sxs-lookup"><span data-stu-id="a0546-136">5</span></span>  <br/> |<span data-ttu-id="a0546-137">followupIcon5</span><span class="sxs-lookup"><span data-stu-id="a0546-137">followupIcon5</span></span>  <br/> |<span data-ttu-id="a0546-138">Синий флажок</span><span class="sxs-lookup"><span data-stu-id="a0546-138">Blue flag</span></span>  <br/> |
|<span data-ttu-id="a0546-139">6</span><span class="sxs-lookup"><span data-stu-id="a0546-139">6</span></span>  <br/> |<span data-ttu-id="a0546-140">followupIcon6</span><span class="sxs-lookup"><span data-stu-id="a0546-140">followupIcon6</span></span>  <br/> |<span data-ttu-id="a0546-141">Красный флажок</span><span class="sxs-lookup"><span data-stu-id="a0546-141">Red flag</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="a0546-142">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="a0546-142">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="a0546-143">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="a0546-143">Protocol specifications</span></span>

<span data-ttu-id="a0546-144">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="a0546-144">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="a0546-145">Содержит ссылки на связанные спецификаций протокола Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="a0546-145">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="a0546-146">[[MS-OXOFLAG]](http://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="a0546-146">[[MS-OXOFLAG]](http://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="a0546-147">Задает свойства и операции, связанные с флагов.</span><span class="sxs-lookup"><span data-stu-id="a0546-147">Specifies the properties and operations related to flagging.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="a0546-148">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="a0546-148">Header files</span></span>

<span data-ttu-id="a0546-149">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="a0546-149">Mapidefs.h</span></span>
  
> <span data-ttu-id="a0546-150">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="a0546-150">Provides data type definitions.</span></span>
    
<span data-ttu-id="a0546-151">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="a0546-151">Mapitags.h</span></span>
  
> <span data-ttu-id="a0546-152">Содержит определения свойства в списке альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="a0546-152">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="a0546-153">См. также</span><span class="sxs-lookup"><span data-stu-id="a0546-153">See also</span></span>



[<span data-ttu-id="a0546-154">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="a0546-154">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="a0546-155">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="a0546-155">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="a0546-156">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="a0546-156">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="a0546-157">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="a0546-157">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

