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
ms.openlocfilehash: 2d57e6a195036ead9eb42666876e91a72f65eb8b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32331299"
---
# <a name="pidlidsideeffects-canonical-property"></a><span data-ttu-id="9184f-103">Каноническое свойство PidLidSideEffects</span><span class="sxs-lookup"><span data-stu-id="9184f-103">PidLidSideEffects Canonical Property</span></span>

  
  
<span data-ttu-id="9184f-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9184f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9184f-105">Управление обработкой объекта сообщения клиентом при вводимом пользователем вводе.</span><span class="sxs-lookup"><span data-stu-id="9184f-105">Controls how a message object is handled by the client when acting on end-user input.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="9184f-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="9184f-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="9184f-107">dispidSideEffects</span><span class="sxs-lookup"><span data-stu-id="9184f-107">dispidSideEffects</span></span>  <br/> |
|<span data-ttu-id="9184f-108">Набор свойств:</span><span class="sxs-lookup"><span data-stu-id="9184f-108">Property set:</span></span>  <br/> |<span data-ttu-id="9184f-109">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="9184f-109">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="9184f-110">Long ID (LID):</span><span class="sxs-lookup"><span data-stu-id="9184f-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="9184f-111">0x00008510</span><span class="sxs-lookup"><span data-stu-id="9184f-111">0x00008510</span></span>  <br/> |
|<span data-ttu-id="9184f-112">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="9184f-112">Data type:</span></span>  <br/> |<span data-ttu-id="9184f-113">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="9184f-113">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="9184f-114">Область:</span><span class="sxs-lookup"><span data-stu-id="9184f-114">Area:</span></span>  <br/> |<span data-ttu-id="9184f-115">Конфигурация времени запуска</span><span class="sxs-lookup"><span data-stu-id="9184f-115">Run-time configuration</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="9184f-116">Примечания</span><span class="sxs-lookup"><span data-stu-id="9184f-116">Remarks</span></span>

<span data-ttu-id="9184f-117">Должно быть установлено немного или ноль или более из следующих флагов.</span><span class="sxs-lookup"><span data-stu-id="9184f-117">Must be set to a bitwise or zero or more of the following flags.</span></span>
  
|<span data-ttu-id="9184f-118">**Name**</span><span class="sxs-lookup"><span data-stu-id="9184f-118">**Name**</span></span>|<span data-ttu-id="9184f-119">**Value**</span><span class="sxs-lookup"><span data-stu-id="9184f-119">**Value**</span></span>|<span data-ttu-id="9184f-120">**Описание**</span><span class="sxs-lookup"><span data-stu-id="9184f-120">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="9184f-121">seOpenToDelete</span><span class="sxs-lookup"><span data-stu-id="9184f-121">seOpenToDelete</span></span>  <br/> |<span data-ttu-id="9184f-122">0x0001</span><span class="sxs-lookup"><span data-stu-id="9184f-122">0x0001</span></span>  <br/> |<span data-ttu-id="9184f-123">При удалении объекта сообщения требуется дополнительная обработка.</span><span class="sxs-lookup"><span data-stu-id="9184f-123">Additional processing is required on the message object when deleting.</span></span>  <br/> |
|<span data-ttu-id="9184f-124">seNoFrame</span><span class="sxs-lookup"><span data-stu-id="9184f-124">seNoFrame</span></span>  <br/> |<span data-ttu-id="9184f-125">0x0008</span><span class="sxs-lookup"><span data-stu-id="9184f-125">0x0008</span></span>  <br/> |<span data-ttu-id="9184f-126">С объектом сообщения не связан пользовательский интерфейс.</span><span class="sxs-lookup"><span data-stu-id="9184f-126">No UI is associated with the message object.</span></span>  <br/> |
|<span data-ttu-id="9184f-127">seCoerceToInbox</span><span class="sxs-lookup"><span data-stu-id="9184f-127">seCoerceToInbox</span></span>  <br/> |<span data-ttu-id="9184f-128">0x0010</span><span class="sxs-lookup"><span data-stu-id="9184f-128">0x0010</span></span>  <br/> |<span data-ttu-id="9184f-129">Дополнительная обработка требуется на объекте сообщения при перемещении или копировании в объект папки с свойством **PR_CONTAINER_CLASS** [(PidTagContainerClass)](pidtagcontainerclass-canonical-property.md)свойства "IPF. Примечание".</span><span class="sxs-lookup"><span data-stu-id="9184f-129">Additional processing is required on the message object when moving or copying to a folder object with a **PR_CONTAINER_CLASS** ([PidTagContainerClass](pidtagcontainerclass-canonical-property.md)) property of "IPF.Note".</span></span>  <br/> |
|<span data-ttu-id="9184f-130">seOpenTocopy</span><span class="sxs-lookup"><span data-stu-id="9184f-130">seOpenTocopy</span></span>  <br/> |<span data-ttu-id="9184f-131">0x0020</span><span class="sxs-lookup"><span data-stu-id="9184f-131">0x0020</span></span>  <br/> |<span data-ttu-id="9184f-132">Дополнительная обработка требуется на объекте сообщения при копировании в другую папку.</span><span class="sxs-lookup"><span data-stu-id="9184f-132">Additional processing is required on the message object when copying to another folder.</span></span>  <br/> |
|<span data-ttu-id="9184f-133">seOpenToMove</span><span class="sxs-lookup"><span data-stu-id="9184f-133">seOpenToMove</span></span>  <br/> |<span data-ttu-id="9184f-134">0x0040</span><span class="sxs-lookup"><span data-stu-id="9184f-134">0x0040</span></span>  <br/> |<span data-ttu-id="9184f-135">Дополнительная обработка требуется на объекте сообщения при перемещении в другую папку.</span><span class="sxs-lookup"><span data-stu-id="9184f-135">Additional processing is required on the message object when moving to another folder.</span></span>  <br/> |
|<span data-ttu-id="9184f-136">seOpenForCtxMenu</span><span class="sxs-lookup"><span data-stu-id="9184f-136">seOpenForCtxMenu</span></span>  <br/> |<span data-ttu-id="9184f-137">0x0100</span><span class="sxs-lookup"><span data-stu-id="9184f-137">0x0100</span></span>  <br/> |<span data-ttu-id="9184f-138">Для отображения глаголов конечному пользователю требуется дополнительная обработка на объекте сообщения.</span><span class="sxs-lookup"><span data-stu-id="9184f-138">Additional processing is required on the message object when displaying verbs to the end-user.</span></span>  <br/> |
|<span data-ttu-id="9184f-139">seCannotUndoDelete</span><span class="sxs-lookup"><span data-stu-id="9184f-139">seCannotUndoDelete</span></span>  <br/> |<span data-ttu-id="9184f-140">0x0400</span><span class="sxs-lookup"><span data-stu-id="9184f-140">0x0400</span></span>  <br/> |<span data-ttu-id="9184f-141">Не удается отменить операцию удаления, ее нельзя задать, если не установлено "seOpenToDelete".</span><span class="sxs-lookup"><span data-stu-id="9184f-141">Cannot undo delete operation, must not be set unless "seOpenToDelete" is set.</span></span>  <br/> |
|<span data-ttu-id="9184f-142">seCannotUndoCopy</span><span class="sxs-lookup"><span data-stu-id="9184f-142">seCannotUndoCopy</span></span>  <br/> |<span data-ttu-id="9184f-143">0x0800</span><span class="sxs-lookup"><span data-stu-id="9184f-143">0x0800</span></span>  <br/> |<span data-ttu-id="9184f-144">Не удается отменить операцию копирования, ее нельзя задать, если не установлена "seOpenTocopy".</span><span class="sxs-lookup"><span data-stu-id="9184f-144">Cannot undo copy operation, must not be set unless "seOpenTocopy" is set.</span></span>  <br/> |
|<span data-ttu-id="9184f-145">seCannotUndoMove</span><span class="sxs-lookup"><span data-stu-id="9184f-145">seCannotUndoMove</span></span>  <br/> |<span data-ttu-id="9184f-146">0x1000</span><span class="sxs-lookup"><span data-stu-id="9184f-146">0x1000</span></span>  <br/> |<span data-ttu-id="9184f-147">Не удается отменить операцию перемещения, ее нельзя задать, если не установлено "seOpenToMove".</span><span class="sxs-lookup"><span data-stu-id="9184f-147">Cannot undo move operation, must not be set unless "seOpenToMove" is set.</span></span>  <br/> |
|<span data-ttu-id="9184f-148">seHasScript</span><span class="sxs-lookup"><span data-stu-id="9184f-148">seHasScript</span></span>  <br/> |<span data-ttu-id="9184f-149">0x2000</span><span class="sxs-lookup"><span data-stu-id="9184f-149">0x2000</span></span>  <br/> |<span data-ttu-id="9184f-150">Объект сообщения содержит сценарий конечных пользователей.</span><span class="sxs-lookup"><span data-stu-id="9184f-150">The message object contains end-user script.</span></span>  <br/> |
|<span data-ttu-id="9184f-151">seOpenToPermDelete</span><span class="sxs-lookup"><span data-stu-id="9184f-151">seOpenToPermDelete</span></span>  <br/> |<span data-ttu-id="9184f-152">0x4000</span><span class="sxs-lookup"><span data-stu-id="9184f-152">0x4000</span></span>  <br/> |<span data-ttu-id="9184f-153">Для удаления объекта сообщения требуется дополнительная обработка.</span><span class="sxs-lookup"><span data-stu-id="9184f-153">Additional processing is required to permanently delete the message object.</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="9184f-154">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="9184f-154">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="9184f-155">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="9184f-155">Protocol specifications</span></span>

<span data-ttu-id="9184f-156">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="9184f-156">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="9184f-157">Предоставляет определение набора свойств и ссылки на связанные Exchange Server протоколы.</span><span class="sxs-lookup"><span data-stu-id="9184f-157">Provides property set definition and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="9184f-158">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="9184f-158">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="9184f-159">Обрабатывает объекты сообщений и вложений.</span><span class="sxs-lookup"><span data-stu-id="9184f-159">Handles message and attachment objects.</span></span>
    
<span data-ttu-id="9184f-160">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="9184f-160">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="9184f-161">Указывает свойства и операции для встреч, запросов на собрания и ответных сообщений.</span><span class="sxs-lookup"><span data-stu-id="9184f-161">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="9184f-162">Файлы заголовки</span><span class="sxs-lookup"><span data-stu-id="9184f-162">Header files</span></span>

<span data-ttu-id="9184f-163">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="9184f-163">Mapidefs.h</span></span>
  
> <span data-ttu-id="9184f-164">Предоставляет определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="9184f-164">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="9184f-165">См. также</span><span class="sxs-lookup"><span data-stu-id="9184f-165">See also</span></span>



[<span data-ttu-id="9184f-166">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="9184f-166">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="9184f-167">Канонические свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="9184f-167">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="9184f-168">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="9184f-168">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="9184f-169">Сопоставление имен MAPI с каноническими именами свойств</span><span class="sxs-lookup"><span data-stu-id="9184f-169">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

