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
# <a name="pidtagflagstatus-canonical-property"></a><span data-ttu-id="3b5a7-103">Каноническое свойство PidTagFlagStatus</span><span class="sxs-lookup"><span data-stu-id="3b5a7-103">PidTagFlagStatus Canonical Property</span></span>

  
  
<span data-ttu-id="3b5a7-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3b5a7-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3b5a7-105">Указывает состояние флага объекта сообщения.</span><span class="sxs-lookup"><span data-stu-id="3b5a7-105">Specifies the flag state of the message object.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="3b5a7-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="3b5a7-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="3b5a7-107">PR_FLAG_STATUS</span><span class="sxs-lookup"><span data-stu-id="3b5a7-107">PR_FLAG_STATUS</span></span>  <br/> |
|<span data-ttu-id="3b5a7-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="3b5a7-108">Identifier:</span></span>  <br/> |<span data-ttu-id="3b5a7-109">0x1090</span><span class="sxs-lookup"><span data-stu-id="3b5a7-109">0x1090</span></span>  <br/> |
|<span data-ttu-id="3b5a7-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="3b5a7-110">Data type:</span></span>  <br/> |<span data-ttu-id="3b5a7-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="3b5a7-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="3b5a7-112">Область:</span><span class="sxs-lookup"><span data-stu-id="3b5a7-112">Area:</span></span>  <br/> |<span data-ttu-id="3b5a7-113">Разное</span><span class="sxs-lookup"><span data-stu-id="3b5a7-113">Miscellaneous</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="3b5a7-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="3b5a7-114">Remarks</span></span>

<span data-ttu-id="3b5a7-115">Это свойство не должно существовать на объекте, связанном с собранием, и не должно существовать на объекте задачи.</span><span class="sxs-lookup"><span data-stu-id="3b5a7-115">This property must not exist on a meeting-related object, and it should not exist on a task object.</span></span> <span data-ttu-id="3b5a7-116">При заданной на других объектах сообщений это свойство должно быть заданной для одного из следующих значений:</span><span class="sxs-lookup"><span data-stu-id="3b5a7-116">When set on other message objects, this property must be set to one of the following values:</span></span>
  
|<span data-ttu-id="3b5a7-117">**Числовая величина**</span><span class="sxs-lookup"><span data-stu-id="3b5a7-117">**Numeric value**</span></span>|<span data-ttu-id="3b5a7-118">**Имя**</span><span class="sxs-lookup"><span data-stu-id="3b5a7-118">**Name**</span></span>|<span data-ttu-id="3b5a7-119">**Описание**</span><span class="sxs-lookup"><span data-stu-id="3b5a7-119">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="3b5a7-120">Не присутствует</span><span class="sxs-lookup"><span data-stu-id="3b5a7-120">Not present</span></span>  <br/> |<span data-ttu-id="3b5a7-121">Н/Д</span><span class="sxs-lookup"><span data-stu-id="3b5a7-121">N/A</span></span>  <br/> |<span data-ttu-id="3b5a7-122">Unflagged</span><span class="sxs-lookup"><span data-stu-id="3b5a7-122">Unflagged</span></span>  <br/> |
|<span data-ttu-id="3b5a7-123">0x00000001</span><span class="sxs-lookup"><span data-stu-id="3b5a7-123">0x00000001</span></span>  <br/> |<span data-ttu-id="3b5a7-124">followupComplete</span><span class="sxs-lookup"><span data-stu-id="3b5a7-124">followupComplete</span></span>  <br/> |<span data-ttu-id="3b5a7-125">Пометка завершена</span><span class="sxs-lookup"><span data-stu-id="3b5a7-125">Flagged complete</span></span>  <br/> |
|<span data-ttu-id="3b5a7-126">0x00000002</span><span class="sxs-lookup"><span data-stu-id="3b5a7-126">0x00000002</span></span>  <br/> |<span data-ttu-id="3b5a7-127">followupFlagged</span><span class="sxs-lookup"><span data-stu-id="3b5a7-127">followupFlagged</span></span>  <br/> |<span data-ttu-id="3b5a7-128">Помечено</span><span class="sxs-lookup"><span data-stu-id="3b5a7-128">Flagged</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="3b5a7-129">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="3b5a7-129">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="3b5a7-130">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="3b5a7-130">Protocol specifications</span></span>

<span data-ttu-id="3b5a7-131">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="3b5a7-131">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="3b5a7-132">Содержит ссылки на связанные Exchange Server протоколы.</span><span class="sxs-lookup"><span data-stu-id="3b5a7-132">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="3b5a7-133">[[MS-OXOFLAG]](https://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="3b5a7-133">[[MS-OXOFLAG]](https://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="3b5a7-134">Указывает свойства и операции, связанные с маркировкой.</span><span class="sxs-lookup"><span data-stu-id="3b5a7-134">Specifies the properties and operations related to flagging.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="3b5a7-135">Файлы заголовки</span><span class="sxs-lookup"><span data-stu-id="3b5a7-135">Header files</span></span>

<span data-ttu-id="3b5a7-136">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="3b5a7-136">Mapidefs.h</span></span>
  
> <span data-ttu-id="3b5a7-137">Предоставляет определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="3b5a7-137">Provides data type definitions.</span></span>
    
<span data-ttu-id="3b5a7-138">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="3b5a7-138">Mapitags.h</span></span>
  
> <span data-ttu-id="3b5a7-139">Содержит определения свойств, перечисленных в качестве альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="3b5a7-139">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="3b5a7-140">См. также</span><span class="sxs-lookup"><span data-stu-id="3b5a7-140">See also</span></span>



[<span data-ttu-id="3b5a7-141">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="3b5a7-141">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="3b5a7-142">Канонические свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="3b5a7-142">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="3b5a7-143">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="3b5a7-143">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="3b5a7-144">Сопоставление имен MAPI с каноническими именами свойств</span><span class="sxs-lookup"><span data-stu-id="3b5a7-144">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

