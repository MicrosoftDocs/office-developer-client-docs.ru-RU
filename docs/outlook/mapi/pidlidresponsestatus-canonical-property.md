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
description: '���� ���������� ���������: 9 ����� 2015 �.'
ms.openlocfilehash: 0bfa3a01613c49b122e92e4ac281e5b20b5f07ae
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19810516"
---
# <a name="pidlidresponsestatus-canonical-property"></a><span data-ttu-id="25ee4-103">Каноническое свойство PidLidResponseStatus</span><span class="sxs-lookup"><span data-stu-id="25ee4-103">PidLidResponseStatus Canonical Property</span></span>

  
  
<span data-ttu-id="25ee4-104">**Применимо к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="25ee4-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="25ee4-105">Указывает состояние ответа для участника.</span><span class="sxs-lookup"><span data-stu-id="25ee4-105">Specifies the response status of an attendee.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="25ee4-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="25ee4-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="25ee4-107">dispidResponseStatus</span><span class="sxs-lookup"><span data-stu-id="25ee4-107">dispidResponseStatus</span></span>  <br/> |
|<span data-ttu-id="25ee4-108">Набор свойств:</span><span class="sxs-lookup"><span data-stu-id="25ee4-108">Property set:</span></span>  <br/> |<span data-ttu-id="25ee4-109">PSETID_Appointment</span><span class="sxs-lookup"><span data-stu-id="25ee4-109">PSETID_Appointment</span></span>  <br/> |
|<span data-ttu-id="25ee4-110">Длинный идентификатор (КРЫШКА):</span><span class="sxs-lookup"><span data-stu-id="25ee4-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="25ee4-111">0x00008218</span><span class="sxs-lookup"><span data-stu-id="25ee4-111">0x00008218</span></span>  <br/> |
|<span data-ttu-id="25ee4-112">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="25ee4-112">Data type:</span></span>  <br/> |<span data-ttu-id="25ee4-113">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="25ee4-113">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="25ee4-114">Области:</span><span class="sxs-lookup"><span data-stu-id="25ee4-114">Area:</span></span>  <br/> |<span data-ttu-id="25ee4-115">Meetings (собрания);</span><span class="sxs-lookup"><span data-stu-id="25ee4-115">Meetings</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="25ee4-116">Замечания</span><span class="sxs-lookup"><span data-stu-id="25ee4-116">Remarks</span></span>

<span data-ttu-id="25ee4-117">Состояние ответа должно быть одно из значений в таблице ниже.</span><span class="sxs-lookup"><span data-stu-id="25ee4-117">The response status must be one of the values in the table below.</span></span>
  
|<span data-ttu-id="25ee4-118">**Состояние ответа**</span><span class="sxs-lookup"><span data-stu-id="25ee4-118">**Response status**</span></span>|<span data-ttu-id="25ee4-119">**Значение**</span><span class="sxs-lookup"><span data-stu-id="25ee4-119">**Value**</span></span>|<span data-ttu-id="25ee4-120">**Описание**</span><span class="sxs-lookup"><span data-stu-id="25ee4-120">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="25ee4-121">respNone</span><span class="sxs-lookup"><span data-stu-id="25ee4-121">respNone</span></span>  <br/> |<span data-ttu-id="25ee4-122">0x00000000</span><span class="sxs-lookup"><span data-stu-id="25ee4-122">0x00000000</span></span>  <br/> |<span data-ttu-id="25ee4-123">Нет ответа необходим для этого объекта.</span><span class="sxs-lookup"><span data-stu-id="25ee4-123">No response is required for this object.</span></span> <span data-ttu-id="25ee4-124">Это обоснование для объектов встречи и собрания объекты ответа.</span><span class="sxs-lookup"><span data-stu-id="25ee4-124">This is the case for appointment objects and meeting response objects.</span></span>  <br/> |
|<span data-ttu-id="25ee4-125">respOrganized</span><span class="sxs-lookup"><span data-stu-id="25ee4-125">respOrganized</span></span>  <br/> |<span data-ttu-id="25ee4-126">0x00000001</span><span class="sxs-lookup"><span data-stu-id="25ee4-126">0x00000001</span></span>  <br/> |<span data-ttu-id="25ee4-127">Приглашение на собрание принадлежит организатора.</span><span class="sxs-lookup"><span data-stu-id="25ee4-127">This meeting belongs to the organizer.</span></span>  <br/> |
|<span data-ttu-id="25ee4-128">respTentative</span><span class="sxs-lookup"><span data-stu-id="25ee4-128">respTentative</span></span>  <br/> |<span data-ttu-id="25ee4-129">0x00000002</span><span class="sxs-lookup"><span data-stu-id="25ee4-129">0x00000002</span></span>  <br/> |<span data-ttu-id="25ee4-130">Это значение на участника собрания указывает, что участник условно принял приглашение на собрание.</span><span class="sxs-lookup"><span data-stu-id="25ee4-130">This value on the attendee's meeting indicates that the attendee has tentatively accepted the meeting request.</span></span>  <br/> |
|<span data-ttu-id="25ee4-131">respAccepted</span><span class="sxs-lookup"><span data-stu-id="25ee4-131">respAccepted</span></span>  <br/> |<span data-ttu-id="25ee4-132">0x00000003</span><span class="sxs-lookup"><span data-stu-id="25ee4-132">0x00000003</span></span>  <br/> |<span data-ttu-id="25ee4-133">Это значение на участника собрания t указывает, что участник принял запрос на собрание.</span><span class="sxs-lookup"><span data-stu-id="25ee4-133">This value on the attendee's meeting t indicates that the attendee has accepted the meeting request.</span></span>  <br/> |
|<span data-ttu-id="25ee4-134">respDeclined</span><span class="sxs-lookup"><span data-stu-id="25ee4-134">respDeclined</span></span>  <br/> |<span data-ttu-id="25ee4-135">0x00000004</span><span class="sxs-lookup"><span data-stu-id="25ee4-135">0x00000004</span></span>  <br/> |<span data-ttu-id="25ee4-136">Это значение на участника собрания указывает, что участник отклонил запрос на собрание.</span><span class="sxs-lookup"><span data-stu-id="25ee4-136">This value on the attendee's meeting indicates that the attendee has declined the meeting request.</span></span>  <br/> |
|<span data-ttu-id="25ee4-137">respNotResponded</span><span class="sxs-lookup"><span data-stu-id="25ee4-137">respNotResponded</span></span>  <br/> |<span data-ttu-id="25ee4-138">0x00000005</span><span class="sxs-lookup"><span data-stu-id="25ee4-138">0x00000005</span></span>  <br/> |<span data-ttu-id="25ee4-139">Это значение на участника собрания указывает, что участник собрания еще не ответил.</span><span class="sxs-lookup"><span data-stu-id="25ee4-139">This value on the attendee's meeting indicates the attendee has not yet responded.</span></span> <span data-ttu-id="25ee4-140">Это значение — на приглашения на собрание, обновление собрания и Отмена собрания.</span><span class="sxs-lookup"><span data-stu-id="25ee4-140">This value is on the meeting request, meeting update, and meeting cancelation.</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="25ee4-141">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="25ee4-141">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="25ee4-142">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="25ee4-142">Protocol specifications</span></span>

<span data-ttu-id="25ee4-143">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="25ee4-143">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="25ee4-144">Содержит определения набора свойств и ссылки на связанные спецификаций протокола Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="25ee4-144">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="25ee4-145">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="25ee4-145">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="25ee4-146">Задает свойства и операции для встречи, приглашения на собрание и ответы.</span><span class="sxs-lookup"><span data-stu-id="25ee4-146">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="25ee4-147">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="25ee4-147">Header files</span></span>

<span data-ttu-id="25ee4-148">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="25ee4-148">Mapidefs.h</span></span>
  
> <span data-ttu-id="25ee4-149">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="25ee4-149">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="25ee4-150">См. также</span><span class="sxs-lookup"><span data-stu-id="25ee4-150">See also</span></span>



[<span data-ttu-id="25ee4-151">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="25ee4-151">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="25ee4-152">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="25ee4-152">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="25ee4-153">Каноническое свойство имена сопоставляемых именам MAPI</span><span class="sxs-lookup"><span data-stu-id="25ee4-153">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="25ee4-154">Сопоставление имен MAPI имена каноническое свойств</span><span class="sxs-lookup"><span data-stu-id="25ee4-154">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

