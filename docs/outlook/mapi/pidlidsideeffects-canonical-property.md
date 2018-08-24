---
title: Каноническое свойство PidLidSideEffects
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidSideEffects
api_type:
- COM
ms.assetid: 90d601d9-5eeb-40b6-885d-ccd8a95ae322
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: fa29a55a5fc2ce89e125909d13a2c14a347ef831
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22594028"
---
# <a name="pidlidsideeffects-canonical-property"></a><span data-ttu-id="de6b5-103">Каноническое свойство PidLidSideEffects</span><span class="sxs-lookup"><span data-stu-id="de6b5-103">PidLidSideEffects Canonical Property</span></span>

  
  
<span data-ttu-id="de6b5-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="de6b5-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="de6b5-105">Позволяет определить способ обработки объекта message клиентом при работе на входные данные конечных пользователей.</span><span class="sxs-lookup"><span data-stu-id="de6b5-105">Controls how a message object is handled by the client when acting on end-user input.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="de6b5-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="de6b5-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="de6b5-107">dispidSideEffects</span><span class="sxs-lookup"><span data-stu-id="de6b5-107">dispidSideEffects</span></span>  <br/> |
|<span data-ttu-id="de6b5-108">Набор свойств:</span><span class="sxs-lookup"><span data-stu-id="de6b5-108">Property set:</span></span>  <br/> |<span data-ttu-id="de6b5-109">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="de6b5-109">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="de6b5-110">Длинный идентификатор (КРЫШКА):</span><span class="sxs-lookup"><span data-stu-id="de6b5-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="de6b5-111">0x00008510</span><span class="sxs-lookup"><span data-stu-id="de6b5-111">0x00008510</span></span>  <br/> |
|<span data-ttu-id="de6b5-112">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="de6b5-112">Data type:</span></span>  <br/> |<span data-ttu-id="de6b5-113">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="de6b5-113">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="de6b5-114">Область:</span><span class="sxs-lookup"><span data-stu-id="de6b5-114">Area:</span></span>  <br/> |<span data-ttu-id="de6b5-115">Конфигурация во время выполнения</span><span class="sxs-lookup"><span data-stu-id="de6b5-115">Run-time configuration</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="de6b5-116">Замечания</span><span class="sxs-lookup"><span data-stu-id="de6b5-116">Remarks</span></span>

<span data-ttu-id="de6b5-117">Необходимо установить значение битовую или ноль или несколько из следующих флагов.</span><span class="sxs-lookup"><span data-stu-id="de6b5-117">Must be set to a bitwise or zero or more of the following flags.</span></span>
  
|<span data-ttu-id="de6b5-118">**Имя**</span><span class="sxs-lookup"><span data-stu-id="de6b5-118">**Name**</span></span>|<span data-ttu-id="de6b5-119">**Значение**</span><span class="sxs-lookup"><span data-stu-id="de6b5-119">**Value**</span></span>|<span data-ttu-id="de6b5-120">**Описание**</span><span class="sxs-lookup"><span data-stu-id="de6b5-120">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="de6b5-121">seOpenToDelete</span><span class="sxs-lookup"><span data-stu-id="de6b5-121">seOpenToDelete</span></span>  <br/> |<span data-ttu-id="de6b5-122">0x0001</span><span class="sxs-lookup"><span data-stu-id="de6b5-122">0x0001</span></span>  <br/> |<span data-ttu-id="de6b5-123">При удалении на объект message требуется дополнительной обработки.</span><span class="sxs-lookup"><span data-stu-id="de6b5-123">Additional processing is required on the message object when deleting.</span></span>  <br/> |
|<span data-ttu-id="de6b5-124">seNoFrame</span><span class="sxs-lookup"><span data-stu-id="de6b5-124">seNoFrame</span></span>  <br/> |<span data-ttu-id="de6b5-125">0x0008</span><span class="sxs-lookup"><span data-stu-id="de6b5-125">0x0008</span></span>  <br/> |<span data-ttu-id="de6b5-126">Пользовательского интерфейса не связан с объектом сообщения.</span><span class="sxs-lookup"><span data-stu-id="de6b5-126">No UI is associated with the message object.</span></span>  <br/> |
|<span data-ttu-id="de6b5-127">seCoerceToInbox</span><span class="sxs-lookup"><span data-stu-id="de6b5-127">seCoerceToInbox</span></span>  <br/> |<span data-ttu-id="de6b5-128">0x0010</span><span class="sxs-lookup"><span data-stu-id="de6b5-128">0x0010</span></span>  <br/> |<span data-ttu-id="de6b5-129">Требуется дополнительной обработки на объект сообщения, когда перемещение и копирование объект folder со свойством **PR_CONTAINER_CLASS** ([PidTagContainerClass](pidtagcontainerclass-canonical-property.md)) «IPF. Обратите внимание на то».</span><span class="sxs-lookup"><span data-stu-id="de6b5-129">Additional processing is required on the message object when moving or copying to a folder object with a **PR_CONTAINER_CLASS** ([PidTagContainerClass](pidtagcontainerclass-canonical-property.md)) property of "IPF.Note".</span></span>  <br/> |
|<span data-ttu-id="de6b5-130">seOpenTocopy</span><span class="sxs-lookup"><span data-stu-id="de6b5-130">seOpenTocopy</span></span>  <br/> |<span data-ttu-id="de6b5-131">0x0020</span><span class="sxs-lookup"><span data-stu-id="de6b5-131">0x0020</span></span>  <br/> |<span data-ttu-id="de6b5-132">При копировании в другую папку на объект message требуется дополнительной обработки.</span><span class="sxs-lookup"><span data-stu-id="de6b5-132">Additional processing is required on the message object when copying to another folder.</span></span>  <br/> |
|<span data-ttu-id="de6b5-133">seOpenToMove</span><span class="sxs-lookup"><span data-stu-id="de6b5-133">seOpenToMove</span></span>  <br/> |<span data-ttu-id="de6b5-134">0x0040</span><span class="sxs-lookup"><span data-stu-id="de6b5-134">0x0040</span></span>  <br/> |<span data-ttu-id="de6b5-135">При переходе на другую папку на объект message требуется дополнительной обработки.</span><span class="sxs-lookup"><span data-stu-id="de6b5-135">Additional processing is required on the message object when moving to another folder.</span></span>  <br/> |
|<span data-ttu-id="de6b5-136">seOpenForCtxMenu</span><span class="sxs-lookup"><span data-stu-id="de6b5-136">seOpenForCtxMenu</span></span>  <br/> |<span data-ttu-id="de6b5-137">0x0100</span><span class="sxs-lookup"><span data-stu-id="de6b5-137">0x0100</span></span>  <br/> |<span data-ttu-id="de6b5-138">При отображении команд для конечных пользователей на объект message требуется дополнительной обработки.</span><span class="sxs-lookup"><span data-stu-id="de6b5-138">Additional processing is required on the message object when displaying verbs to the end-user.</span></span>  <br/> |
|<span data-ttu-id="de6b5-139">seCannotUndoDelete</span><span class="sxs-lookup"><span data-stu-id="de6b5-139">seCannotUndoDelete</span></span>  <br/> |<span data-ttu-id="de6b5-140">0x0400</span><span class="sxs-lookup"><span data-stu-id="de6b5-140">0x0400</span></span>  <br/> |<span data-ttu-id="de6b5-141">Не удается отменить операцию удаления, не должен быть установлен, если не имеет значение «seOpenToDelete».</span><span class="sxs-lookup"><span data-stu-id="de6b5-141">Cannot undo delete operation, must not be set unless "seOpenToDelete" is set.</span></span>  <br/> |
|<span data-ttu-id="de6b5-142">seCannotUndoCopy</span><span class="sxs-lookup"><span data-stu-id="de6b5-142">seCannotUndoCopy</span></span>  <br/> |<span data-ttu-id="de6b5-143">0x0800</span><span class="sxs-lookup"><span data-stu-id="de6b5-143">0x0800</span></span>  <br/> |<span data-ttu-id="de6b5-144">Не удается отменить операцию копирования, не должен быть установлен, если не имеет значение «seOpenTocopy».</span><span class="sxs-lookup"><span data-stu-id="de6b5-144">Cannot undo copy operation, must not be set unless "seOpenTocopy" is set.</span></span>  <br/> |
|<span data-ttu-id="de6b5-145">seCannotUndoMove</span><span class="sxs-lookup"><span data-stu-id="de6b5-145">seCannotUndoMove</span></span>  <br/> |<span data-ttu-id="de6b5-146">0x1000</span><span class="sxs-lookup"><span data-stu-id="de6b5-146">0x1000</span></span>  <br/> |<span data-ttu-id="de6b5-147">Не удается отменить операцию перемещения, не должен быть установлен, если не имеет значение «seOpenToMove».</span><span class="sxs-lookup"><span data-stu-id="de6b5-147">Cannot undo move operation, must not be set unless "seOpenToMove" is set.</span></span>  <br/> |
|<span data-ttu-id="de6b5-148">seHasScript</span><span class="sxs-lookup"><span data-stu-id="de6b5-148">seHasScript</span></span>  <br/> |<span data-ttu-id="de6b5-149">0x2000</span><span class="sxs-lookup"><span data-stu-id="de6b5-149">0x2000</span></span>  <br/> |<span data-ttu-id="de6b5-150">Объект сообщения содержит скрипт конечных пользователей.</span><span class="sxs-lookup"><span data-stu-id="de6b5-150">The message object contains end-user script.</span></span>  <br/> |
|<span data-ttu-id="de6b5-151">seOpenToPermDelete</span><span class="sxs-lookup"><span data-stu-id="de6b5-151">seOpenToPermDelete</span></span>  <br/> |<span data-ttu-id="de6b5-152">0x4000</span><span class="sxs-lookup"><span data-stu-id="de6b5-152">0x4000</span></span>  <br/> |<span data-ttu-id="de6b5-153">Чтобы окончательно удалить объект message требуется дополнительной обработки.</span><span class="sxs-lookup"><span data-stu-id="de6b5-153">Additional processing is required to permanently delete the message object.</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="de6b5-154">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="de6b5-154">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="de6b5-155">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="de6b5-155">Protocol specifications</span></span>

<span data-ttu-id="de6b5-156">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="de6b5-156">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="de6b5-157">Содержит определение набора свойств и ссылки на связанные спецификаций протокола Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="de6b5-157">Provides property set definition and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="de6b5-158">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="de6b5-158">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="de6b5-159">Обрабатывает объекты сообщения и вложения.</span><span class="sxs-lookup"><span data-stu-id="de6b5-159">Handles message and attachment objects.</span></span>
    
<span data-ttu-id="de6b5-160">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="de6b5-160">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="de6b5-161">Задает свойства и операции для встречи, приглашения на собрание и ответы.</span><span class="sxs-lookup"><span data-stu-id="de6b5-161">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="de6b5-162">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="de6b5-162">Header files</span></span>

<span data-ttu-id="de6b5-163">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="de6b5-163">Mapidefs.h</span></span>
  
> <span data-ttu-id="de6b5-164">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="de6b5-164">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="de6b5-165">См. также</span><span class="sxs-lookup"><span data-stu-id="de6b5-165">See also</span></span>



[<span data-ttu-id="de6b5-166">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="de6b5-166">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="de6b5-167">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="de6b5-167">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="de6b5-168">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="de6b5-168">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="de6b5-169">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="de6b5-169">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

