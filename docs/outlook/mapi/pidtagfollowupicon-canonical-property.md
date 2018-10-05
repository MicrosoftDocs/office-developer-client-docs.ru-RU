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
ms.openlocfilehash: 205b6ddc2b65297d69a2223aab7b745b223ee553
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25383522"
---
# <a name="pidtagfollowupicon-canonical-property"></a><span data-ttu-id="64ca4-103">Каноническое свойство PidTagFollowupIcon</span><span class="sxs-lookup"><span data-stu-id="64ca4-103">PidTagFollowupIcon Canonical Property</span></span>

  
  
<span data-ttu-id="64ca4-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="64ca4-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="64ca4-105">Указывает цвет объекта message.</span><span class="sxs-lookup"><span data-stu-id="64ca4-105">Specifies the flag color of the message object.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="64ca4-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="64ca4-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="64ca4-107">PR_FOLLOWUP_ICON</span><span class="sxs-lookup"><span data-stu-id="64ca4-107">PR_FOLLOWUP_ICON</span></span>  <br/> |
|<span data-ttu-id="64ca4-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="64ca4-108">Identifier:</span></span>  <br/> |<span data-ttu-id="64ca4-109">0x1095</span><span class="sxs-lookup"><span data-stu-id="64ca4-109">0x1095</span></span>  <br/> |
|<span data-ttu-id="64ca4-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="64ca4-110">Data type:</span></span>  <br/> |<span data-ttu-id="64ca4-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="64ca4-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="64ca4-112">Область:</span><span class="sxs-lookup"><span data-stu-id="64ca4-112">Area:</span></span>  <br/> |<span data-ttu-id="64ca4-113">Переименование папки сообщения</span><span class="sxs-lookup"><span data-stu-id="64ca4-113">Rename message folder</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="64ca4-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="64ca4-114">Remarks</span></span>

<span data-ttu-id="64ca4-115">Это свойство не должна существовать, если значение свойства **PR_FLAG_STATUS** ([PidTagFlagStatus](pidtagflagstatus-canonical-property.md)) имеет значение «followupFlagged» или объект message — это объект, относящихся к собранию.</span><span class="sxs-lookup"><span data-stu-id="64ca4-115">This property must not exist unless the value of the **PR_FLAG_STATUS** ([PidTagFlagStatus](pidtagflagstatus-canonical-property.md)) property is set to "followupFlagged", or the message object is a meeting-related object.</span></span> <span data-ttu-id="64ca4-116">Это свойство не должна существовать для объекта задачи.</span><span class="sxs-lookup"><span data-stu-id="64ca4-116">This property should not exist on a task object.</span></span> <span data-ttu-id="64ca4-117">Если установлено на другие объекты сообщения, это свойство должно быть присвоено одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="64ca4-117">When set on other message objects, this property must be set to one of the following values.</span></span>
  
|<span data-ttu-id="64ca4-118">**Числовое значение**</span><span class="sxs-lookup"><span data-stu-id="64ca4-118">**Numeric value**</span></span>|<span data-ttu-id="64ca4-119">**Имя**</span><span class="sxs-lookup"><span data-stu-id="64ca4-119">**Name**</span></span>|<span data-ttu-id="64ca4-120">**Описание**</span><span class="sxs-lookup"><span data-stu-id="64ca4-120">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="64ca4-121">Этот параметр не указан</span><span class="sxs-lookup"><span data-stu-id="64ca4-121">Not present</span></span>  <br/> |<span data-ttu-id="64ca4-122">Н/Д</span><span class="sxs-lookup"><span data-stu-id="64ca4-122">N/A</span></span>  <br/> |<span data-ttu-id="64ca4-123">Без цвета</span><span class="sxs-lookup"><span data-stu-id="64ca4-123">No color</span></span>  <br/> |
|<span data-ttu-id="64ca4-124">1</span><span class="sxs-lookup"><span data-stu-id="64ca4-124">1</span></span>  <br/> |<span data-ttu-id="64ca4-125">followupIcon1</span><span class="sxs-lookup"><span data-stu-id="64ca4-125">followupIcon1</span></span>  <br/> |<span data-ttu-id="64ca4-126">Лиловый флажок</span><span class="sxs-lookup"><span data-stu-id="64ca4-126">Purple flag</span></span>  <br/> |
|<span data-ttu-id="64ca4-127">2</span><span class="sxs-lookup"><span data-stu-id="64ca4-127">2</span></span>  <br/> |<span data-ttu-id="64ca4-128">followupIcon2</span><span class="sxs-lookup"><span data-stu-id="64ca4-128">followupIcon2</span></span>  <br/> |<span data-ttu-id="64ca4-129">Оранжевый флажок</span><span class="sxs-lookup"><span data-stu-id="64ca4-129">Orange flag</span></span>  <br/> |
|<span data-ttu-id="64ca4-130">3</span><span class="sxs-lookup"><span data-stu-id="64ca4-130">3</span></span>  <br/> |<span data-ttu-id="64ca4-131">followupIcon3</span><span class="sxs-lookup"><span data-stu-id="64ca4-131">followupIcon3</span></span>  <br/> |<span data-ttu-id="64ca4-132">Зеленый флажок</span><span class="sxs-lookup"><span data-stu-id="64ca4-132">Green flag</span></span>  <br/> |
|<span data-ttu-id="64ca4-133">4</span><span class="sxs-lookup"><span data-stu-id="64ca4-133">4</span></span>  <br/> |<span data-ttu-id="64ca4-134">followupIcon4</span><span class="sxs-lookup"><span data-stu-id="64ca4-134">followupIcon4</span></span>  <br/> |<span data-ttu-id="64ca4-135">Желтый флажок</span><span class="sxs-lookup"><span data-stu-id="64ca4-135">Yellow flag</span></span>  <br/> |
|<span data-ttu-id="64ca4-136">5</span><span class="sxs-lookup"><span data-stu-id="64ca4-136">5</span></span>  <br/> |<span data-ttu-id="64ca4-137">followupIcon5</span><span class="sxs-lookup"><span data-stu-id="64ca4-137">followupIcon5</span></span>  <br/> |<span data-ttu-id="64ca4-138">Синий флажок</span><span class="sxs-lookup"><span data-stu-id="64ca4-138">Blue flag</span></span>  <br/> |
|<span data-ttu-id="64ca4-139">6</span><span class="sxs-lookup"><span data-stu-id="64ca4-139">6</span></span>  <br/> |<span data-ttu-id="64ca4-140">followupIcon6</span><span class="sxs-lookup"><span data-stu-id="64ca4-140">followupIcon6</span></span>  <br/> |<span data-ttu-id="64ca4-141">Красный флажок</span><span class="sxs-lookup"><span data-stu-id="64ca4-141">Red flag</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="64ca4-142">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="64ca4-142">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="64ca4-143">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="64ca4-143">Protocol specifications</span></span>

<span data-ttu-id="64ca4-144">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="64ca4-144">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="64ca4-145">Содержит ссылки на связанные спецификаций протокола Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="64ca4-145">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="64ca4-146">[[MS-OXOFLAG]](https://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="64ca4-146">[[MS-OXOFLAG]](https://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="64ca4-147">Задает свойства и операции, связанные с флагов.</span><span class="sxs-lookup"><span data-stu-id="64ca4-147">Specifies the properties and operations related to flagging.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="64ca4-148">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="64ca4-148">Header files</span></span>

<span data-ttu-id="64ca4-149">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="64ca4-149">Mapidefs.h</span></span>
  
> <span data-ttu-id="64ca4-150">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="64ca4-150">Provides data type definitions.</span></span>
    
<span data-ttu-id="64ca4-151">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="64ca4-151">Mapitags.h</span></span>
  
> <span data-ttu-id="64ca4-152">Содержит определения свойства в списке альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="64ca4-152">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="64ca4-153">См. также</span><span class="sxs-lookup"><span data-stu-id="64ca4-153">See also</span></span>



[<span data-ttu-id="64ca4-154">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="64ca4-154">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="64ca4-155">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="64ca4-155">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="64ca4-156">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="64ca4-156">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="64ca4-157">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="64ca4-157">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

