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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316284"
---
# <a name="pidtagfollowupicon-canonical-property"></a><span data-ttu-id="1f875-103">Каноническое свойство PidTagFollowupIcon</span><span class="sxs-lookup"><span data-stu-id="1f875-103">PidTagFollowupIcon Canonical Property</span></span>

  
  
<span data-ttu-id="1f875-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1f875-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1f875-105">Задает цвет флажка для объекта Message.</span><span class="sxs-lookup"><span data-stu-id="1f875-105">Specifies the flag color of the message object.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="1f875-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="1f875-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="1f875-107">ПР_ФОЛЛОВУП_ИКОН</span><span class="sxs-lookup"><span data-stu-id="1f875-107">PR_FOLLOWUP_ICON</span></span>  <br/> |
|<span data-ttu-id="1f875-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="1f875-108">Identifier:</span></span>  <br/> |<span data-ttu-id="1f875-109">0x1095</span><span class="sxs-lookup"><span data-stu-id="1f875-109">0x1095</span></span>  <br/> |
|<span data-ttu-id="1f875-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="1f875-110">Data type:</span></span>  <br/> |<span data-ttu-id="1f875-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="1f875-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="1f875-112">Область:</span><span class="sxs-lookup"><span data-stu-id="1f875-112">Area:</span></span>  <br/> |<span data-ttu-id="1f875-113">ПереИменование папки сообщений</span><span class="sxs-lookup"><span data-stu-id="1f875-113">Rename message folder</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="1f875-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="1f875-114">Remarks</span></span>

<span data-ttu-id="1f875-115">Это свойство не должно существовать, если для свойства **пр_флаг_статус** ([PidTagFlagStatus](pidtagflagstatus-canonical-property.md)) не задано значение "фолловупфлагжед", или объект Message является объектом, связанным с собранием.</span><span class="sxs-lookup"><span data-stu-id="1f875-115">This property must not exist unless the value of the **PR_FLAG_STATUS** ([PidTagFlagStatus](pidtagflagstatus-canonical-property.md)) property is set to "followupFlagged", or the message object is a meeting-related object.</span></span> <span data-ttu-id="1f875-116">Это свойство не должно существовать для объекта Task.</span><span class="sxs-lookup"><span data-stu-id="1f875-116">This property should not exist on a task object.</span></span> <span data-ttu-id="1f875-117">Если задано для других объектов Message, этому свойству необходимо присвоить одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="1f875-117">When set on other message objects, this property must be set to one of the following values.</span></span>
  
|<span data-ttu-id="1f875-118">**Числовое значение**</span><span class="sxs-lookup"><span data-stu-id="1f875-118">**Numeric value**</span></span>|<span data-ttu-id="1f875-119">**Имя**</span><span class="sxs-lookup"><span data-stu-id="1f875-119">**Name**</span></span>|<span data-ttu-id="1f875-120">**Описание**</span><span class="sxs-lookup"><span data-stu-id="1f875-120">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="1f875-121">Отсутствует</span><span class="sxs-lookup"><span data-stu-id="1f875-121">Not present</span></span>  <br/> |<span data-ttu-id="1f875-122">Недоступно</span><span class="sxs-lookup"><span data-stu-id="1f875-122">N/A</span></span>  <br/> |<span data-ttu-id="1f875-123">Нет цвета</span><span class="sxs-lookup"><span data-stu-id="1f875-123">No color</span></span>  <br/> |
|<span data-ttu-id="1f875-124">1,1</span><span class="sxs-lookup"><span data-stu-id="1f875-124">1</span></span>  <br/> |<span data-ttu-id="1f875-125">followupIcon1</span><span class="sxs-lookup"><span data-stu-id="1f875-125">followupIcon1</span></span>  <br/> |<span data-ttu-id="1f875-126">Лиловый флаг</span><span class="sxs-lookup"><span data-stu-id="1f875-126">Purple flag</span></span>  <br/> |
|<span data-ttu-id="1f875-127">2</span><span class="sxs-lookup"><span data-stu-id="1f875-127">2</span></span>  <br/> |<span data-ttu-id="1f875-128">followupIcon2</span><span class="sxs-lookup"><span data-stu-id="1f875-128">followupIcon2</span></span>  <br/> |<span data-ttu-id="1f875-129">Оранжевый флаг</span><span class="sxs-lookup"><span data-stu-id="1f875-129">Orange flag</span></span>  <br/> |
|<span data-ttu-id="1f875-130">4</span><span class="sxs-lookup"><span data-stu-id="1f875-130">3</span></span>  <br/> |<span data-ttu-id="1f875-131">followupIcon3</span><span class="sxs-lookup"><span data-stu-id="1f875-131">followupIcon3</span></span>  <br/> |<span data-ttu-id="1f875-132">Зеленый флаг</span><span class="sxs-lookup"><span data-stu-id="1f875-132">Green flag</span></span>  <br/> |
|<span data-ttu-id="1f875-133">SP4</span><span class="sxs-lookup"><span data-stu-id="1f875-133">4</span></span>  <br/> |<span data-ttu-id="1f875-134">followupIcon4</span><span class="sxs-lookup"><span data-stu-id="1f875-134">followupIcon4</span></span>  <br/> |<span data-ttu-id="1f875-135">Желтый флаг</span><span class="sxs-lookup"><span data-stu-id="1f875-135">Yellow flag</span></span>  <br/> |
|<span data-ttu-id="1f875-136">17:00</span><span class="sxs-lookup"><span data-stu-id="1f875-136">5</span></span>  <br/> |<span data-ttu-id="1f875-137">followupIcon5</span><span class="sxs-lookup"><span data-stu-id="1f875-137">followupIcon5</span></span>  <br/> |<span data-ttu-id="1f875-138">Синий флажок</span><span class="sxs-lookup"><span data-stu-id="1f875-138">Blue flag</span></span>  <br/> |
|<span data-ttu-id="1f875-139">ICMPv6</span><span class="sxs-lookup"><span data-stu-id="1f875-139">6</span></span>  <br/> |<span data-ttu-id="1f875-140">followupIcon6</span><span class="sxs-lookup"><span data-stu-id="1f875-140">followupIcon6</span></span>  <br/> |<span data-ttu-id="1f875-141">Красный флаг</span><span class="sxs-lookup"><span data-stu-id="1f875-141">Red flag</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="1f875-142">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="1f875-142">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="1f875-143">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="1f875-143">Protocol specifications</span></span>

<span data-ttu-id="1f875-144">[[MS — ОКСПРОПС]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="1f875-144">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="1f875-145">Содержит ссылки на соответствующие спецификации протоколов Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="1f875-145">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="1f875-146">[[MS — ОКСОФЛАГ]](https://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="1f875-146">[[MS-OXOFLAG]](https://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="1f875-147">Задает свойства и операции, связанные с пометкой.</span><span class="sxs-lookup"><span data-stu-id="1f875-147">Specifies the properties and operations related to flagging.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="1f875-148">Файлы заГоловков</span><span class="sxs-lookup"><span data-stu-id="1f875-148">Header files</span></span>

<span data-ttu-id="1f875-149">MAPIDEFS. h</span><span class="sxs-lookup"><span data-stu-id="1f875-149">Mapidefs.h</span></span>
  
> <span data-ttu-id="1f875-150">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="1f875-150">Provides data type definitions.</span></span>
    
<span data-ttu-id="1f875-151">Мапитагс. h</span><span class="sxs-lookup"><span data-stu-id="1f875-151">Mapitags.h</span></span>
  
> <span data-ttu-id="1f875-152">Содержит определения свойств, перечисленных как альтернативные имена.</span><span class="sxs-lookup"><span data-stu-id="1f875-152">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="1f875-153">См. также</span><span class="sxs-lookup"><span data-stu-id="1f875-153">See also</span></span>



[<span data-ttu-id="1f875-154">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="1f875-154">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="1f875-155">Каноническое свойство MAPI</span><span class="sxs-lookup"><span data-stu-id="1f875-155">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="1f875-156">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="1f875-156">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="1f875-157">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="1f875-157">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

