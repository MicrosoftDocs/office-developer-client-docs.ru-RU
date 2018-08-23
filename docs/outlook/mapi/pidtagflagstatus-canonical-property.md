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
ms.openlocfilehash: 8dba5906a00beb6d38e4f3e375a9c57db79d42f1
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22575961"
---
# <a name="pidtagflagstatus-canonical-property"></a><span data-ttu-id="fe30e-103">Каноническое свойство PidTagFlagStatus</span><span class="sxs-lookup"><span data-stu-id="fe30e-103">PidTagFlagStatus Canonical Property</span></span>

  
  
<span data-ttu-id="fe30e-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="fe30e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="fe30e-105">Указывает состояние флага объекта message.</span><span class="sxs-lookup"><span data-stu-id="fe30e-105">Specifies the flag state of the message object.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="fe30e-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="fe30e-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="fe30e-107">PR_FLAG_STATUS</span><span class="sxs-lookup"><span data-stu-id="fe30e-107">PR_FLAG_STATUS</span></span>  <br/> |
|<span data-ttu-id="fe30e-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="fe30e-108">Identifier:</span></span>  <br/> |<span data-ttu-id="fe30e-109">0x1090</span><span class="sxs-lookup"><span data-stu-id="fe30e-109">0x1090</span></span>  <br/> |
|<span data-ttu-id="fe30e-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="fe30e-110">Data type:</span></span>  <br/> |<span data-ttu-id="fe30e-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="fe30e-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="fe30e-112">Область:</span><span class="sxs-lookup"><span data-stu-id="fe30e-112">Area:</span></span>  <br/> |<span data-ttu-id="fe30e-113">Разное</span><span class="sxs-lookup"><span data-stu-id="fe30e-113">Miscellaneous</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="fe30e-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="fe30e-114">Remarks</span></span>

<span data-ttu-id="fe30e-115">Это свойство должно отсутствовать для объекта, связанные с собрания и не должно быть для объекта задачи.</span><span class="sxs-lookup"><span data-stu-id="fe30e-115">This property must not exist on a meeting-related object, and it should not exist on a task object.</span></span> <span data-ttu-id="fe30e-116">Если установлено на другие объекты сообщения, это свойство должно быть задано одно из следующих значений:</span><span class="sxs-lookup"><span data-stu-id="fe30e-116">When set on other message objects, this property must be set to one of the following values:</span></span>
  
|<span data-ttu-id="fe30e-117">**Числовое значение**</span><span class="sxs-lookup"><span data-stu-id="fe30e-117">**Numeric value**</span></span>|<span data-ttu-id="fe30e-118">**Имя**</span><span class="sxs-lookup"><span data-stu-id="fe30e-118">**Name**</span></span>|<span data-ttu-id="fe30e-119">**Описание**</span><span class="sxs-lookup"><span data-stu-id="fe30e-119">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="fe30e-120">Этот параметр не указан</span><span class="sxs-lookup"><span data-stu-id="fe30e-120">Not present</span></span>  <br/> |<span data-ttu-id="fe30e-121">Н/Д</span><span class="sxs-lookup"><span data-stu-id="fe30e-121">N/A</span></span>  <br/> |<span data-ttu-id="fe30e-122">Без отметки</span><span class="sxs-lookup"><span data-stu-id="fe30e-122">Unflagged</span></span>  <br/> |
|<span data-ttu-id="fe30e-123">0x00000001</span><span class="sxs-lookup"><span data-stu-id="fe30e-123">0x00000001</span></span>  <br/> |<span data-ttu-id="fe30e-124">followupComplete</span><span class="sxs-lookup"><span data-stu-id="fe30e-124">followupComplete</span></span>  <br/> |<span data-ttu-id="fe30e-125">Отмеченные завершена</span><span class="sxs-lookup"><span data-stu-id="fe30e-125">Flagged complete</span></span>  <br/> |
|<span data-ttu-id="fe30e-126">0x00000002</span><span class="sxs-lookup"><span data-stu-id="fe30e-126">0x00000002</span></span>  <br/> |<span data-ttu-id="fe30e-127">followupFlagged</span><span class="sxs-lookup"><span data-stu-id="fe30e-127">followupFlagged</span></span>  <br/> |<span data-ttu-id="fe30e-128">Отмеченные</span><span class="sxs-lookup"><span data-stu-id="fe30e-128">Flagged</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="fe30e-129">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="fe30e-129">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="fe30e-130">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="fe30e-130">Protocol specifications</span></span>

<span data-ttu-id="fe30e-131">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="fe30e-131">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="fe30e-132">Содержит ссылки на связанные спецификаций протокола Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="fe30e-132">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="fe30e-133">[[MS-OXOFLAG]](http://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="fe30e-133">[[MS-OXOFLAG]](http://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="fe30e-134">Задает свойства и операции, связанные с флагов.</span><span class="sxs-lookup"><span data-stu-id="fe30e-134">Specifies the properties and operations related to flagging.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="fe30e-135">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="fe30e-135">Header files</span></span>

<span data-ttu-id="fe30e-136">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="fe30e-136">Mapidefs.h</span></span>
  
> <span data-ttu-id="fe30e-137">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="fe30e-137">Provides data type definitions.</span></span>
    
<span data-ttu-id="fe30e-138">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="fe30e-138">Mapitags.h</span></span>
  
> <span data-ttu-id="fe30e-139">Содержит определения свойства в списке альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="fe30e-139">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="fe30e-140">См. также</span><span class="sxs-lookup"><span data-stu-id="fe30e-140">See also</span></span>



[<span data-ttu-id="fe30e-141">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="fe30e-141">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="fe30e-142">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="fe30e-142">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="fe30e-143">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="fe30e-143">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="fe30e-144">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="fe30e-144">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

