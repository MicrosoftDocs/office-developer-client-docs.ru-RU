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
# <a name="pidtagflagstatus-canonical-property"></a><span data-ttu-id="33561-103">Каноническое свойство PidTagFlagStatus</span><span class="sxs-lookup"><span data-stu-id="33561-103">PidTagFlagStatus Canonical Property</span></span>

  
  
<span data-ttu-id="33561-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="33561-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="33561-105">Указывает состояние флага объекта message.</span><span class="sxs-lookup"><span data-stu-id="33561-105">Specifies the flag state of the message object.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="33561-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="33561-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="33561-107">PR_FLAG_STATUS</span><span class="sxs-lookup"><span data-stu-id="33561-107">PR_FLAG_STATUS</span></span>  <br/> |
|<span data-ttu-id="33561-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="33561-108">Identifier:</span></span>  <br/> |<span data-ttu-id="33561-109">0x1090</span><span class="sxs-lookup"><span data-stu-id="33561-109">0x1090</span></span>  <br/> |
|<span data-ttu-id="33561-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="33561-110">Data type:</span></span>  <br/> |<span data-ttu-id="33561-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="33561-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="33561-112">Область:</span><span class="sxs-lookup"><span data-stu-id="33561-112">Area:</span></span>  <br/> |<span data-ttu-id="33561-113">Разное</span><span class="sxs-lookup"><span data-stu-id="33561-113">Miscellaneous</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="33561-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="33561-114">Remarks</span></span>

<span data-ttu-id="33561-115">Это свойство не должно существовать в объекте, связанном с собранием, и не должно существовать в объекте задачи.</span><span class="sxs-lookup"><span data-stu-id="33561-115">This property must not exist on a meeting-related object, and it should not exist on a task object.</span></span> <span data-ttu-id="33561-116">Если этот объект за установлен для других объектов сообщений, этому свойству необходимо установить одно из следующих значений:</span><span class="sxs-lookup"><span data-stu-id="33561-116">When set on other message objects, this property must be set to one of the following values:</span></span>
  
|<span data-ttu-id="33561-117">**Числовая величина**</span><span class="sxs-lookup"><span data-stu-id="33561-117">**Numeric value**</span></span>|<span data-ttu-id="33561-118">**Название**</span><span class="sxs-lookup"><span data-stu-id="33561-118">**Name**</span></span>|<span data-ttu-id="33561-119">**Описание**</span><span class="sxs-lookup"><span data-stu-id="33561-119">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="33561-120">Нет</span><span class="sxs-lookup"><span data-stu-id="33561-120">Not present</span></span>  <br/> |<span data-ttu-id="33561-121">Недоступно</span><span class="sxs-lookup"><span data-stu-id="33561-121">N/A</span></span>  <br/> |<span data-ttu-id="33561-122">Unflagged</span><span class="sxs-lookup"><span data-stu-id="33561-122">Unflagged</span></span>  <br/> |
|<span data-ttu-id="33561-123">0x00000001</span><span class="sxs-lookup"><span data-stu-id="33561-123">0x00000001</span></span>  <br/> |<span data-ttu-id="33561-124">followupComplete</span><span class="sxs-lookup"><span data-stu-id="33561-124">followupComplete</span></span>  <br/> |<span data-ttu-id="33561-125">Помечено как завершенное</span><span class="sxs-lookup"><span data-stu-id="33561-125">Flagged complete</span></span>  <br/> |
|<span data-ttu-id="33561-126">0x00000002</span><span class="sxs-lookup"><span data-stu-id="33561-126">0x00000002</span></span>  <br/> |<span data-ttu-id="33561-127">followupFlagged</span><span class="sxs-lookup"><span data-stu-id="33561-127">followupFlagged</span></span>  <br/> |<span data-ttu-id="33561-128">Flagged</span><span class="sxs-lookup"><span data-stu-id="33561-128">Flagged</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="33561-129">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="33561-129">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="33561-130">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="33561-130">Protocol specifications</span></span>

<span data-ttu-id="33561-131">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="33561-131">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="33561-132">Содержит ссылки на связанные Exchange Server протоколы.</span><span class="sxs-lookup"><span data-stu-id="33561-132">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="33561-133">[[MS-OXOFLAG]](https://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="33561-133">[[MS-OXOFLAG]](https://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="33561-134">Указывает свойства и операции, связанные с помезданием.</span><span class="sxs-lookup"><span data-stu-id="33561-134">Specifies the properties and operations related to flagging.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="33561-135">Файлы заголовок</span><span class="sxs-lookup"><span data-stu-id="33561-135">Header files</span></span>

<span data-ttu-id="33561-136">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="33561-136">Mapidefs.h</span></span>
  
> <span data-ttu-id="33561-137">Предоставляет определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="33561-137">Provides data type definitions.</span></span>
    
<span data-ttu-id="33561-138">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="33561-138">Mapitags.h</span></span>
  
> <span data-ttu-id="33561-139">Содержит определения свойств, перечисленных в качестве альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="33561-139">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="33561-140">См. также</span><span class="sxs-lookup"><span data-stu-id="33561-140">See also</span></span>



[<span data-ttu-id="33561-141">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="33561-141">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="33561-142">Канонические свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="33561-142">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="33561-143">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="33561-143">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="33561-144">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="33561-144">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

