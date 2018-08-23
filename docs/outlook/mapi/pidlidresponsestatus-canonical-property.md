---
title: Каноническое свойство PidLidResponseStatus
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidResponseStatus
api_type:
- COM
ms.assetid: e56142fd-204b-497e-83b9-59f9acda6cb4
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 2e6aa8407459fef5fd9657e9d2887f0ae78ff9c9
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22585467"
---
# <a name="pidlidresponsestatus-canonical-property"></a><span data-ttu-id="1a968-103">Каноническое свойство PidLidResponseStatus</span><span class="sxs-lookup"><span data-stu-id="1a968-103">PidLidResponseStatus Canonical Property</span></span>

  
  
<span data-ttu-id="1a968-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1a968-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1a968-105">Указывает состояние ответа для участника.</span><span class="sxs-lookup"><span data-stu-id="1a968-105">Specifies the response status of an attendee.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="1a968-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="1a968-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="1a968-107">dispidResponseStatus</span><span class="sxs-lookup"><span data-stu-id="1a968-107">dispidResponseStatus</span></span>  <br/> |
|<span data-ttu-id="1a968-108">Набор свойств:</span><span class="sxs-lookup"><span data-stu-id="1a968-108">Property set:</span></span>  <br/> |<span data-ttu-id="1a968-109">PSETID_Appointment</span><span class="sxs-lookup"><span data-stu-id="1a968-109">PSETID_Appointment</span></span>  <br/> |
|<span data-ttu-id="1a968-110">Длинный идентификатор (КРЫШКА):</span><span class="sxs-lookup"><span data-stu-id="1a968-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="1a968-111">0x00008218</span><span class="sxs-lookup"><span data-stu-id="1a968-111">0x00008218</span></span>  <br/> |
|<span data-ttu-id="1a968-112">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="1a968-112">Data type:</span></span>  <br/> |<span data-ttu-id="1a968-113">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="1a968-113">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="1a968-114">Область:</span><span class="sxs-lookup"><span data-stu-id="1a968-114">Area:</span></span>  <br/> |<span data-ttu-id="1a968-115">Meetings (собрания);</span><span class="sxs-lookup"><span data-stu-id="1a968-115">Meetings</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="1a968-116">Замечания</span><span class="sxs-lookup"><span data-stu-id="1a968-116">Remarks</span></span>

<span data-ttu-id="1a968-117">Состояние ответа должно быть одно из значений в таблице ниже.</span><span class="sxs-lookup"><span data-stu-id="1a968-117">The response status must be one of the values in the table below.</span></span>
  
|<span data-ttu-id="1a968-118">**Состояние ответа**</span><span class="sxs-lookup"><span data-stu-id="1a968-118">**Response status**</span></span>|<span data-ttu-id="1a968-119">**Значение**</span><span class="sxs-lookup"><span data-stu-id="1a968-119">**Value**</span></span>|<span data-ttu-id="1a968-120">**Описание**</span><span class="sxs-lookup"><span data-stu-id="1a968-120">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="1a968-121">respNone</span><span class="sxs-lookup"><span data-stu-id="1a968-121">respNone</span></span>  <br/> |<span data-ttu-id="1a968-122">0x00000000</span><span class="sxs-lookup"><span data-stu-id="1a968-122">0x00000000</span></span>  <br/> |<span data-ttu-id="1a968-123">Нет ответа необходим для этого объекта.</span><span class="sxs-lookup"><span data-stu-id="1a968-123">No response is required for this object.</span></span> <span data-ttu-id="1a968-124">Это обоснование для объектов встречи и собрания объекты ответа.</span><span class="sxs-lookup"><span data-stu-id="1a968-124">This is the case for appointment objects and meeting response objects.</span></span>  <br/> |
|<span data-ttu-id="1a968-125">respOrganized</span><span class="sxs-lookup"><span data-stu-id="1a968-125">respOrganized</span></span>  <br/> |<span data-ttu-id="1a968-126">0x00000001</span><span class="sxs-lookup"><span data-stu-id="1a968-126">0x00000001</span></span>  <br/> |<span data-ttu-id="1a968-127">Приглашение на собрание принадлежит организатора.</span><span class="sxs-lookup"><span data-stu-id="1a968-127">This meeting belongs to the organizer.</span></span>  <br/> |
|<span data-ttu-id="1a968-128">respTentative</span><span class="sxs-lookup"><span data-stu-id="1a968-128">respTentative</span></span>  <br/> |<span data-ttu-id="1a968-129">0x00000002</span><span class="sxs-lookup"><span data-stu-id="1a968-129">0x00000002</span></span>  <br/> |<span data-ttu-id="1a968-130">Это значение на участника собрания указывает, что участник условно принял приглашение на собрание.</span><span class="sxs-lookup"><span data-stu-id="1a968-130">This value on the attendee's meeting indicates that the attendee has tentatively accepted the meeting request.</span></span>  <br/> |
|<span data-ttu-id="1a968-131">respAccepted</span><span class="sxs-lookup"><span data-stu-id="1a968-131">respAccepted</span></span>  <br/> |<span data-ttu-id="1a968-132">0x00000003</span><span class="sxs-lookup"><span data-stu-id="1a968-132">0x00000003</span></span>  <br/> |<span data-ttu-id="1a968-133">Это значение на участника собрания t указывает, что участник принял запрос на собрание.</span><span class="sxs-lookup"><span data-stu-id="1a968-133">This value on the attendee's meeting t indicates that the attendee has accepted the meeting request.</span></span>  <br/> |
|<span data-ttu-id="1a968-134">respDeclined</span><span class="sxs-lookup"><span data-stu-id="1a968-134">respDeclined</span></span>  <br/> |<span data-ttu-id="1a968-135">0x00000004</span><span class="sxs-lookup"><span data-stu-id="1a968-135">0x00000004</span></span>  <br/> |<span data-ttu-id="1a968-136">Это значение на участника собрания указывает, что участник отклонил запрос на собрание.</span><span class="sxs-lookup"><span data-stu-id="1a968-136">This value on the attendee's meeting indicates that the attendee has declined the meeting request.</span></span>  <br/> |
|<span data-ttu-id="1a968-137">respNotResponded</span><span class="sxs-lookup"><span data-stu-id="1a968-137">respNotResponded</span></span>  <br/> |<span data-ttu-id="1a968-138">0x00000005</span><span class="sxs-lookup"><span data-stu-id="1a968-138">0x00000005</span></span>  <br/> |<span data-ttu-id="1a968-139">Это значение на участника собрания указывает, что участник собрания еще не ответил.</span><span class="sxs-lookup"><span data-stu-id="1a968-139">This value on the attendee's meeting indicates the attendee has not yet responded.</span></span> <span data-ttu-id="1a968-140">Это значение — на приглашения на собрание, обновление собрания и Отмена собрания.</span><span class="sxs-lookup"><span data-stu-id="1a968-140">This value is on the meeting request, meeting update, and meeting cancelation.</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="1a968-141">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="1a968-141">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="1a968-142">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="1a968-142">Protocol specifications</span></span>

<span data-ttu-id="1a968-143">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="1a968-143">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="1a968-144">Содержит определения набора свойств и ссылки на связанные спецификаций протокола Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="1a968-144">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="1a968-145">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="1a968-145">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="1a968-146">Задает свойства и операции для встречи, приглашения на собрание и ответы.</span><span class="sxs-lookup"><span data-stu-id="1a968-146">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="1a968-147">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="1a968-147">Header files</span></span>

<span data-ttu-id="1a968-148">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="1a968-148">Mapidefs.h</span></span>
  
> <span data-ttu-id="1a968-149">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="1a968-149">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="1a968-150">См. также</span><span class="sxs-lookup"><span data-stu-id="1a968-150">See also</span></span>



[<span data-ttu-id="1a968-151">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="1a968-151">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="1a968-152">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="1a968-152">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="1a968-153">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="1a968-153">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="1a968-154">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="1a968-154">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

