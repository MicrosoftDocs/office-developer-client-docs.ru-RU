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
# <a name="pidtagfollowupicon-canonical-property"></a><span data-ttu-id="0e5bf-103">Каноническое свойство PidTagFollowupIcon</span><span class="sxs-lookup"><span data-stu-id="0e5bf-103">PidTagFollowupIcon Canonical Property</span></span>

  
  
<span data-ttu-id="0e5bf-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0e5bf-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0e5bf-105">Указывает цвет флага объекта сообщения.</span><span class="sxs-lookup"><span data-stu-id="0e5bf-105">Specifies the flag color of the message object.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="0e5bf-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="0e5bf-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="0e5bf-107">PR_FOLLOWUP_ICON</span><span class="sxs-lookup"><span data-stu-id="0e5bf-107">PR_FOLLOWUP_ICON</span></span>  <br/> |
|<span data-ttu-id="0e5bf-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="0e5bf-108">Identifier:</span></span>  <br/> |<span data-ttu-id="0e5bf-109">0x1095</span><span class="sxs-lookup"><span data-stu-id="0e5bf-109">0x1095</span></span>  <br/> |
|<span data-ttu-id="0e5bf-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="0e5bf-110">Data type:</span></span>  <br/> |<span data-ttu-id="0e5bf-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="0e5bf-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="0e5bf-112">Область:</span><span class="sxs-lookup"><span data-stu-id="0e5bf-112">Area:</span></span>  <br/> |<span data-ttu-id="0e5bf-113">Переименование папки сообщений</span><span class="sxs-lookup"><span data-stu-id="0e5bf-113">Rename message folder</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="0e5bf-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="0e5bf-114">Remarks</span></span>

<span data-ttu-id="0e5bf-115">Это свойство не должно существовать, если значение свойства **PR_FLAG_STATUS** ([PidTagFlagStatus)](pidtagflagstatus-canonical-property.md)не имеет значения "followupFlagged" или объект сообщения является объектом, связанным с собранием.</span><span class="sxs-lookup"><span data-stu-id="0e5bf-115">This property must not exist unless the value of the **PR_FLAG_STATUS** ([PidTagFlagStatus](pidtagflagstatus-canonical-property.md)) property is set to "followupFlagged", or the message object is a meeting-related object.</span></span> <span data-ttu-id="0e5bf-116">Это свойство не должно существовать в объекте задачи.</span><span class="sxs-lookup"><span data-stu-id="0e5bf-116">This property should not exist on a task object.</span></span> <span data-ttu-id="0e5bf-117">Если этот объект за установлен для других объектов сообщений, этому свойству необходимо установить одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="0e5bf-117">When set on other message objects, this property must be set to one of the following values.</span></span>
  
|<span data-ttu-id="0e5bf-118">**Числовая величина**</span><span class="sxs-lookup"><span data-stu-id="0e5bf-118">**Numeric value**</span></span>|<span data-ttu-id="0e5bf-119">**Название**</span><span class="sxs-lookup"><span data-stu-id="0e5bf-119">**Name**</span></span>|<span data-ttu-id="0e5bf-120">**Описание**</span><span class="sxs-lookup"><span data-stu-id="0e5bf-120">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="0e5bf-121">Нет</span><span class="sxs-lookup"><span data-stu-id="0e5bf-121">Not present</span></span>  <br/> |<span data-ttu-id="0e5bf-122">Недоступно</span><span class="sxs-lookup"><span data-stu-id="0e5bf-122">N/A</span></span>  <br/> |<span data-ttu-id="0e5bf-123">Без цвета</span><span class="sxs-lookup"><span data-stu-id="0e5bf-123">No color</span></span>  <br/> |
|<span data-ttu-id="0e5bf-124">1 </span><span class="sxs-lookup"><span data-stu-id="0e5bf-124">1</span></span>  <br/> |<span data-ttu-id="0e5bf-125">followupIcon1</span><span class="sxs-lookup"><span data-stu-id="0e5bf-125">followupIcon1</span></span>  <br/> |<span data-ttu-id="0e5bf-126">Сиреневый флаг</span><span class="sxs-lookup"><span data-stu-id="0e5bf-126">Purple flag</span></span>  <br/> |
|<span data-ttu-id="0e5bf-127">2 </span><span class="sxs-lookup"><span data-stu-id="0e5bf-127">2</span></span>  <br/> |<span data-ttu-id="0e5bf-128">followupIcon2</span><span class="sxs-lookup"><span data-stu-id="0e5bf-128">followupIcon2</span></span>  <br/> |<span data-ttu-id="0e5bf-129">Оранжевый флаг</span><span class="sxs-lookup"><span data-stu-id="0e5bf-129">Orange flag</span></span>  <br/> |
|<span data-ttu-id="0e5bf-130">3 </span><span class="sxs-lookup"><span data-stu-id="0e5bf-130">3</span></span>  <br/> |<span data-ttu-id="0e5bf-131">followupIcon3</span><span class="sxs-lookup"><span data-stu-id="0e5bf-131">followupIcon3</span></span>  <br/> |<span data-ttu-id="0e5bf-132">Зеленый флаг</span><span class="sxs-lookup"><span data-stu-id="0e5bf-132">Green flag</span></span>  <br/> |
|<span data-ttu-id="0e5bf-133">4 </span><span class="sxs-lookup"><span data-stu-id="0e5bf-133">4</span></span>  <br/> |<span data-ttu-id="0e5bf-134">followupIcon4</span><span class="sxs-lookup"><span data-stu-id="0e5bf-134">followupIcon4</span></span>  <br/> |<span data-ttu-id="0e5bf-135">Желтый флаг</span><span class="sxs-lookup"><span data-stu-id="0e5bf-135">Yellow flag</span></span>  <br/> |
|<span data-ttu-id="0e5bf-136">5 </span><span class="sxs-lookup"><span data-stu-id="0e5bf-136">5</span></span>  <br/> |<span data-ttu-id="0e5bf-137">followupIcon5</span><span class="sxs-lookup"><span data-stu-id="0e5bf-137">followupIcon5</span></span>  <br/> |<span data-ttu-id="0e5bf-138">Синий флаг</span><span class="sxs-lookup"><span data-stu-id="0e5bf-138">Blue flag</span></span>  <br/> |
|<span data-ttu-id="0e5bf-139">6 </span><span class="sxs-lookup"><span data-stu-id="0e5bf-139">6</span></span>  <br/> |<span data-ttu-id="0e5bf-140">followupIcon6</span><span class="sxs-lookup"><span data-stu-id="0e5bf-140">followupIcon6</span></span>  <br/> |<span data-ttu-id="0e5bf-141">Красный флаг</span><span class="sxs-lookup"><span data-stu-id="0e5bf-141">Red flag</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="0e5bf-142">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="0e5bf-142">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="0e5bf-143">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="0e5bf-143">Protocol specifications</span></span>

<span data-ttu-id="0e5bf-144">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="0e5bf-144">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="0e5bf-145">Содержит ссылки на связанные Exchange Server протоколы.</span><span class="sxs-lookup"><span data-stu-id="0e5bf-145">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="0e5bf-146">[[MS-OXOFLAG]](https://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="0e5bf-146">[[MS-OXOFLAG]](https://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="0e5bf-147">Указывает свойства и операции, связанные с помезданием.</span><span class="sxs-lookup"><span data-stu-id="0e5bf-147">Specifies the properties and operations related to flagging.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="0e5bf-148">Файлы заголовок</span><span class="sxs-lookup"><span data-stu-id="0e5bf-148">Header files</span></span>

<span data-ttu-id="0e5bf-149">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="0e5bf-149">Mapidefs.h</span></span>
  
> <span data-ttu-id="0e5bf-150">Предоставляет определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="0e5bf-150">Provides data type definitions.</span></span>
    
<span data-ttu-id="0e5bf-151">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="0e5bf-151">Mapitags.h</span></span>
  
> <span data-ttu-id="0e5bf-152">Содержит определения свойств, перечисленных в качестве альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="0e5bf-152">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="0e5bf-153">См. также</span><span class="sxs-lookup"><span data-stu-id="0e5bf-153">See also</span></span>



[<span data-ttu-id="0e5bf-154">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="0e5bf-154">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="0e5bf-155">Канонические свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="0e5bf-155">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="0e5bf-156">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="0e5bf-156">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="0e5bf-157">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="0e5bf-157">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

