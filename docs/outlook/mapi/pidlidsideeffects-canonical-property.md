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
# <a name="pidlidsideeffects-canonical-property"></a><span data-ttu-id="10ad6-103">Каноническое свойство PidLidSideEffects</span><span class="sxs-lookup"><span data-stu-id="10ad6-103">PidLidSideEffects Canonical Property</span></span>

  
  
<span data-ttu-id="10ad6-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="10ad6-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="10ad6-105">Управляет тем, как клиент обрабатывает объект Message при работе с пользовательским вводом.</span><span class="sxs-lookup"><span data-stu-id="10ad6-105">Controls how a message object is handled by the client when acting on end-user input.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="10ad6-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="10ad6-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="10ad6-107">диспидсидиффектс</span><span class="sxs-lookup"><span data-stu-id="10ad6-107">dispidSideEffects</span></span>  <br/> |
|<span data-ttu-id="10ad6-108">Набор свойств:</span><span class="sxs-lookup"><span data-stu-id="10ad6-108">Property set:</span></span>  <br/> |<span data-ttu-id="10ad6-109">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="10ad6-109">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="10ad6-110">Длинный идентификатор (крышка):</span><span class="sxs-lookup"><span data-stu-id="10ad6-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="10ad6-111">0x00008510</span><span class="sxs-lookup"><span data-stu-id="10ad6-111">0x00008510</span></span>  <br/> |
|<span data-ttu-id="10ad6-112">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="10ad6-112">Data type:</span></span>  <br/> |<span data-ttu-id="10ad6-113">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="10ad6-113">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="10ad6-114">Область:</span><span class="sxs-lookup"><span data-stu-id="10ad6-114">Area:</span></span>  <br/> |<span data-ttu-id="10ad6-115">Настройка времени выполнения</span><span class="sxs-lookup"><span data-stu-id="10ad6-115">Run-time configuration</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="10ad6-116">Примечания</span><span class="sxs-lookup"><span data-stu-id="10ad6-116">Remarks</span></span>

<span data-ttu-id="10ad6-117">Должно быть задано побитовое или ноль или более из следующих флагов.</span><span class="sxs-lookup"><span data-stu-id="10ad6-117">Must be set to a bitwise or zero or more of the following flags.</span></span>
  
|<span data-ttu-id="10ad6-118">**Name**</span><span class="sxs-lookup"><span data-stu-id="10ad6-118">**Name**</span></span>|<span data-ttu-id="10ad6-119">**Value**</span><span class="sxs-lookup"><span data-stu-id="10ad6-119">**Value**</span></span>|<span data-ttu-id="10ad6-120">**Описание**</span><span class="sxs-lookup"><span data-stu-id="10ad6-120">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="10ad6-121">сеопентоделете</span><span class="sxs-lookup"><span data-stu-id="10ad6-121">seOpenToDelete</span></span>  <br/> |<span data-ttu-id="10ad6-122">0x0001</span><span class="sxs-lookup"><span data-stu-id="10ad6-122">0x0001</span></span>  <br/> |<span data-ttu-id="10ad6-123">При удалении объекта Message необходимо выполнить дополнительную обработку объекта Message.</span><span class="sxs-lookup"><span data-stu-id="10ad6-123">Additional processing is required on the message object when deleting.</span></span>  <br/> |
|<span data-ttu-id="10ad6-124">сенофраме</span><span class="sxs-lookup"><span data-stu-id="10ad6-124">seNoFrame</span></span>  <br/> |<span data-ttu-id="10ad6-125">0x0008</span><span class="sxs-lookup"><span data-stu-id="10ad6-125">0x0008</span></span>  <br/> |<span data-ttu-id="10ad6-126">С объектом Message не связан пользовательский интерфейс.</span><span class="sxs-lookup"><span data-stu-id="10ad6-126">No UI is associated with the message object.</span></span>  <br/> |
|<span data-ttu-id="10ad6-127">секоерцетоинбокс</span><span class="sxs-lookup"><span data-stu-id="10ad6-127">seCoerceToInbox</span></span>  <br/> |<span data-ttu-id="10ad6-128">0x0010</span><span class="sxs-lookup"><span data-stu-id="10ad6-128">0x0010</span></span>  <br/> |<span data-ttu-id="10ad6-129">Для объекта Message требуется дополнительная обработка при перемещении или копировании в объект Folder с помощью свойства **PR_CONTAINER_CLASS** ([PIDTAGCONTAINERCLASS](pidtagcontainerclass-canonical-property.md)) "IPF. Note (Примечание).</span><span class="sxs-lookup"><span data-stu-id="10ad6-129">Additional processing is required on the message object when moving or copying to a folder object with a **PR_CONTAINER_CLASS** ([PidTagContainerClass](pidtagcontainerclass-canonical-property.md)) property of "IPF.Note".</span></span>  <br/> |
|<span data-ttu-id="10ad6-130">сеопентокопи</span><span class="sxs-lookup"><span data-stu-id="10ad6-130">seOpenTocopy</span></span>  <br/> |<span data-ttu-id="10ad6-131">0x0020</span><span class="sxs-lookup"><span data-stu-id="10ad6-131">0x0020</span></span>  <br/> |<span data-ttu-id="10ad6-132">При копировании в другую папку требуется дополнительная обработка объекта Message.</span><span class="sxs-lookup"><span data-stu-id="10ad6-132">Additional processing is required on the message object when copying to another folder.</span></span>  <br/> |
|<span data-ttu-id="10ad6-133">сеопентомове</span><span class="sxs-lookup"><span data-stu-id="10ad6-133">seOpenToMove</span></span>  <br/> |<span data-ttu-id="10ad6-134">0x0040</span><span class="sxs-lookup"><span data-stu-id="10ad6-134">0x0040</span></span>  <br/> |<span data-ttu-id="10ad6-135">При перемещении в другую папку требуется дополнительная обработка объекта Message.</span><span class="sxs-lookup"><span data-stu-id="10ad6-135">Additional processing is required on the message object when moving to another folder.</span></span>  <br/> |
|<span data-ttu-id="10ad6-136">сеопенфорктксмену</span><span class="sxs-lookup"><span data-stu-id="10ad6-136">seOpenForCtxMenu</span></span>  <br/> |<span data-ttu-id="10ad6-137">0x0100</span><span class="sxs-lookup"><span data-stu-id="10ad6-137">0x0100</span></span>  <br/> |<span data-ttu-id="10ad6-138">При отображении команд для конечного пользователя требуется дополнительная обработка объекта Message.</span><span class="sxs-lookup"><span data-stu-id="10ad6-138">Additional processing is required on the message object when displaying verbs to the end-user.</span></span>  <br/> |
|<span data-ttu-id="10ad6-139">секаннотундоделете</span><span class="sxs-lookup"><span data-stu-id="10ad6-139">seCannotUndoDelete</span></span>  <br/> |<span data-ttu-id="10ad6-140">0x0400</span><span class="sxs-lookup"><span data-stu-id="10ad6-140">0x0400</span></span>  <br/> |<span data-ttu-id="10ad6-141">Невозможно отменить операцию удаления, если не задано значение "Сеопентоделете".</span><span class="sxs-lookup"><span data-stu-id="10ad6-141">Cannot undo delete operation, must not be set unless "seOpenToDelete" is set.</span></span>  <br/> |
|<span data-ttu-id="10ad6-142">секаннотундокопи</span><span class="sxs-lookup"><span data-stu-id="10ad6-142">seCannotUndoCopy</span></span>  <br/> |<span data-ttu-id="10ad6-143">0x0800</span><span class="sxs-lookup"><span data-stu-id="10ad6-143">0x0800</span></span>  <br/> |<span data-ttu-id="10ad6-144">Невозможно отменить операцию копирования, если не задано значение "Сеопентокопи".</span><span class="sxs-lookup"><span data-stu-id="10ad6-144">Cannot undo copy operation, must not be set unless "seOpenTocopy" is set.</span></span>  <br/> |
|<span data-ttu-id="10ad6-145">секаннотундомове</span><span class="sxs-lookup"><span data-stu-id="10ad6-145">seCannotUndoMove</span></span>  <br/> |<span data-ttu-id="10ad6-146">0x1000</span><span class="sxs-lookup"><span data-stu-id="10ad6-146">0x1000</span></span>  <br/> |<span data-ttu-id="10ad6-147">Невозможно отменить операцию перемещения, если не задано значение "Сеопентомове".</span><span class="sxs-lookup"><span data-stu-id="10ad6-147">Cannot undo move operation, must not be set unless "seOpenToMove" is set.</span></span>  <br/> |
|<span data-ttu-id="10ad6-148">сехасскрипт</span><span class="sxs-lookup"><span data-stu-id="10ad6-148">seHasScript</span></span>  <br/> |<span data-ttu-id="10ad6-149">0x2000</span><span class="sxs-lookup"><span data-stu-id="10ad6-149">0x2000</span></span>  <br/> |<span data-ttu-id="10ad6-150">Объект Message содержит скрипт конечного пользователя.</span><span class="sxs-lookup"><span data-stu-id="10ad6-150">The message object contains end-user script.</span></span>  <br/> |
|<span data-ttu-id="10ad6-151">сеопентопермделете</span><span class="sxs-lookup"><span data-stu-id="10ad6-151">seOpenToPermDelete</span></span>  <br/> |<span data-ttu-id="10ad6-152">0x4000</span><span class="sxs-lookup"><span data-stu-id="10ad6-152">0x4000</span></span>  <br/> |<span data-ttu-id="10ad6-153">Для окончательного удаления объекта Message требуется дополнительная обработка.</span><span class="sxs-lookup"><span data-stu-id="10ad6-153">Additional processing is required to permanently delete the message object.</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="10ad6-154">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="10ad6-154">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="10ad6-155">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="10ad6-155">Protocol specifications</span></span>

<span data-ttu-id="10ad6-156">[[MS — ОКСПРОПС]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="10ad6-156">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="10ad6-157">Предоставляет определение набора свойств и ссылки на соответствующие спецификации протокола Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="10ad6-157">Provides property set definition and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="10ad6-158">[[MS — ОКСКМСГ]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="10ad6-158">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="10ad6-159">Обрабатывает объекты сообщений и вложений.</span><span class="sxs-lookup"><span data-stu-id="10ad6-159">Handles message and attachment objects.</span></span>
    
<span data-ttu-id="10ad6-160">[[MS — ОКСОКАЛ]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="10ad6-160">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="10ad6-161">Задает свойства и операции для встречи, приглашения на собрание и ответных сообщений.</span><span class="sxs-lookup"><span data-stu-id="10ad6-161">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="10ad6-162">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="10ad6-162">Header files</span></span>

<span data-ttu-id="10ad6-163">MAPIDEFS. h</span><span class="sxs-lookup"><span data-stu-id="10ad6-163">Mapidefs.h</span></span>
  
> <span data-ttu-id="10ad6-164">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="10ad6-164">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="10ad6-165">См. также</span><span class="sxs-lookup"><span data-stu-id="10ad6-165">See also</span></span>



[<span data-ttu-id="10ad6-166">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="10ad6-166">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="10ad6-167">Каноническое свойство MAPI</span><span class="sxs-lookup"><span data-stu-id="10ad6-167">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="10ad6-168">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="10ad6-168">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="10ad6-169">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="10ad6-169">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

