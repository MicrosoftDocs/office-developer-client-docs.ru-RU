---
title: Каноническое свойство PidTagFlagStatus
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagFlagStatus
api_type:
- HeaderDef
ms.assetid: b5117360-0939-4535-83fe-3b4a240b5217
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: bca8fccaa43bb3157b3d4e2af7d6aafa64972b41
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316298"
---
# <a name="pidtagflagstatus-canonical-property"></a><span data-ttu-id="ef138-103">Каноническое свойство PidTagFlagStatus</span><span class="sxs-lookup"><span data-stu-id="ef138-103">PidTagFlagStatus Canonical Property</span></span>

  
  
<span data-ttu-id="ef138-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ef138-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ef138-105">Указывает состояние флага объекта Message.</span><span class="sxs-lookup"><span data-stu-id="ef138-105">Specifies the flag state of the message object.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="ef138-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="ef138-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="ef138-107">ПР_ФЛАГ_СТАТУС</span><span class="sxs-lookup"><span data-stu-id="ef138-107">PR_FLAG_STATUS</span></span>  <br/> |
|<span data-ttu-id="ef138-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="ef138-108">Identifier:</span></span>  <br/> |<span data-ttu-id="ef138-109">0x1090</span><span class="sxs-lookup"><span data-stu-id="ef138-109">0x1090</span></span>  <br/> |
|<span data-ttu-id="ef138-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="ef138-110">Data type:</span></span>  <br/> |<span data-ttu-id="ef138-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="ef138-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="ef138-112">Область:</span><span class="sxs-lookup"><span data-stu-id="ef138-112">Area:</span></span>  <br/> |<span data-ttu-id="ef138-113">Разное</span><span class="sxs-lookup"><span data-stu-id="ef138-113">Miscellaneous</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ef138-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="ef138-114">Remarks</span></span>

<span data-ttu-id="ef138-115">Это свойство не должно существовать в объекте, связанном с собранием, и не должно существовать в объекте Task.</span><span class="sxs-lookup"><span data-stu-id="ef138-115">This property must not exist on a meeting-related object, and it should not exist on a task object.</span></span> <span data-ttu-id="ef138-116">Если задано для других объектов Message, этому свойству необходимо присвоить одно из следующих значений:</span><span class="sxs-lookup"><span data-stu-id="ef138-116">When set on other message objects, this property must be set to one of the following values:</span></span>
  
|<span data-ttu-id="ef138-117">**Числовое значение**</span><span class="sxs-lookup"><span data-stu-id="ef138-117">**Numeric value**</span></span>|<span data-ttu-id="ef138-118">**Имя**</span><span class="sxs-lookup"><span data-stu-id="ef138-118">**Name**</span></span>|<span data-ttu-id="ef138-119">**Описание**</span><span class="sxs-lookup"><span data-stu-id="ef138-119">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="ef138-120">Отсутствует</span><span class="sxs-lookup"><span data-stu-id="ef138-120">Not present</span></span>  <br/> |<span data-ttu-id="ef138-121">Недоступно</span><span class="sxs-lookup"><span data-stu-id="ef138-121">N/A</span></span>  <br/> |<span data-ttu-id="ef138-122">Без отметки</span><span class="sxs-lookup"><span data-stu-id="ef138-122">Unflagged</span></span>  <br/> |
|<span data-ttu-id="ef138-123">0x00000001</span><span class="sxs-lookup"><span data-stu-id="ef138-123">0x00000001</span></span>  <br/> |<span data-ttu-id="ef138-124">Фолловупкомплете</span><span class="sxs-lookup"><span data-stu-id="ef138-124">followupComplete</span></span>  <br/> |<span data-ttu-id="ef138-125">Помеченные как завершенные</span><span class="sxs-lookup"><span data-stu-id="ef138-125">Flagged complete</span></span>  <br/> |
|<span data-ttu-id="ef138-126">0x00000002</span><span class="sxs-lookup"><span data-stu-id="ef138-126">0x00000002</span></span>  <br/> |<span data-ttu-id="ef138-127">Фолловупфлагжед</span><span class="sxs-lookup"><span data-stu-id="ef138-127">followupFlagged</span></span>  <br/> |<span data-ttu-id="ef138-128">Отмеченные</span><span class="sxs-lookup"><span data-stu-id="ef138-128">Flagged</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="ef138-129">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="ef138-129">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="ef138-130">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="ef138-130">Protocol specifications</span></span>

<span data-ttu-id="ef138-131">[[MS — ОКСПРОПС]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="ef138-131">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="ef138-132">Содержит ссылки на соответствующие спецификации протоколов Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="ef138-132">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="ef138-133">[[MS — ОКСОФЛАГ]](https://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="ef138-133">[[MS-OXOFLAG]](https://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="ef138-134">Задает свойства и операции, связанные с пометкой.</span><span class="sxs-lookup"><span data-stu-id="ef138-134">Specifies the properties and operations related to flagging.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="ef138-135">Файлы заГоловков</span><span class="sxs-lookup"><span data-stu-id="ef138-135">Header files</span></span>

<span data-ttu-id="ef138-136">MAPIDEFS. h</span><span class="sxs-lookup"><span data-stu-id="ef138-136">Mapidefs.h</span></span>
  
> <span data-ttu-id="ef138-137">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="ef138-137">Provides data type definitions.</span></span>
    
<span data-ttu-id="ef138-138">Мапитагс. h</span><span class="sxs-lookup"><span data-stu-id="ef138-138">Mapitags.h</span></span>
  
> <span data-ttu-id="ef138-139">Содержит определения свойств, перечисленных как альтернативные имена.</span><span class="sxs-lookup"><span data-stu-id="ef138-139">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="ef138-140">См. также</span><span class="sxs-lookup"><span data-stu-id="ef138-140">See also</span></span>



[<span data-ttu-id="ef138-141">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="ef138-141">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="ef138-142">Каноническое свойство MAPI</span><span class="sxs-lookup"><span data-stu-id="ef138-142">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="ef138-143">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="ef138-143">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="ef138-144">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="ef138-144">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

