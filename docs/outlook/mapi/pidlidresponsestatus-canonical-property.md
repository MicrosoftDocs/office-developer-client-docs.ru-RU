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
ms.openlocfilehash: 8c8e284752c6fd47eb7a8f227e2dbfeceebea596
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32345761"
---
# <a name="pidlidresponsestatus-canonical-property"></a><span data-ttu-id="8ec9c-103">Каноническое свойство PidLidResponseStatus</span><span class="sxs-lookup"><span data-stu-id="8ec9c-103">PidLidResponseStatus Canonical Property</span></span>

  
  
<span data-ttu-id="8ec9c-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8ec9c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8ec9c-105">Указывает состояние отклика участника.</span><span class="sxs-lookup"><span data-stu-id="8ec9c-105">Specifies the response status of an attendee.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="8ec9c-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="8ec9c-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="8ec9c-107">диспидреспонсестатус</span><span class="sxs-lookup"><span data-stu-id="8ec9c-107">dispidResponseStatus</span></span>  <br/> |
|<span data-ttu-id="8ec9c-108">Набор свойств:</span><span class="sxs-lookup"><span data-stu-id="8ec9c-108">Property set:</span></span>  <br/> |<span data-ttu-id="8ec9c-109">PSETID_Appointment</span><span class="sxs-lookup"><span data-stu-id="8ec9c-109">PSETID_Appointment</span></span>  <br/> |
|<span data-ttu-id="8ec9c-110">Длинный идентификатор (крышка):</span><span class="sxs-lookup"><span data-stu-id="8ec9c-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="8ec9c-111">0x00008218</span><span class="sxs-lookup"><span data-stu-id="8ec9c-111">0x00008218</span></span>  <br/> |
|<span data-ttu-id="8ec9c-112">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="8ec9c-112">Data type:</span></span>  <br/> |<span data-ttu-id="8ec9c-113">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="8ec9c-113">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="8ec9c-114">Область:</span><span class="sxs-lookup"><span data-stu-id="8ec9c-114">Area:</span></span>  <br/> |<span data-ttu-id="8ec9c-115">Собрания</span><span class="sxs-lookup"><span data-stu-id="8ec9c-115">Meetings</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="8ec9c-116">Примечания</span><span class="sxs-lookup"><span data-stu-id="8ec9c-116">Remarks</span></span>

<span data-ttu-id="8ec9c-117">Состояние отклика должно быть одним из значений в приведенной ниже таблице.</span><span class="sxs-lookup"><span data-stu-id="8ec9c-117">The response status must be one of the values in the table below.</span></span>
  
|<span data-ttu-id="8ec9c-118">**Состояние ответа**</span><span class="sxs-lookup"><span data-stu-id="8ec9c-118">**Response status**</span></span>|<span data-ttu-id="8ec9c-119">**Значение**</span><span class="sxs-lookup"><span data-stu-id="8ec9c-119">**Value**</span></span>|<span data-ttu-id="8ec9c-120">**Описание**</span><span class="sxs-lookup"><span data-stu-id="8ec9c-120">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="8ec9c-121">респноне</span><span class="sxs-lookup"><span data-stu-id="8ec9c-121">respNone</span></span>  <br/> |<span data-ttu-id="8ec9c-122">0x00000000</span><span class="sxs-lookup"><span data-stu-id="8ec9c-122">0x00000000</span></span>  <br/> |<span data-ttu-id="8ec9c-123">Для этого объекта ответ не нужен.</span><span class="sxs-lookup"><span data-stu-id="8ec9c-123">No response is required for this object.</span></span> <span data-ttu-id="8ec9c-124">Это относится к объектам встреч и объектам ответа на собрания.</span><span class="sxs-lookup"><span data-stu-id="8ec9c-124">This is the case for appointment objects and meeting response objects.</span></span>  <br/> |
|<span data-ttu-id="8ec9c-125">респорганизед</span><span class="sxs-lookup"><span data-stu-id="8ec9c-125">respOrganized</span></span>  <br/> |<span data-ttu-id="8ec9c-126">0x00000001</span><span class="sxs-lookup"><span data-stu-id="8ec9c-126">0x00000001</span></span>  <br/> |<span data-ttu-id="8ec9c-127">Это собрание принадлежит организатору.</span><span class="sxs-lookup"><span data-stu-id="8ec9c-127">This meeting belongs to the organizer.</span></span>  <br/> |
|<span data-ttu-id="8ec9c-128">респтентативе</span><span class="sxs-lookup"><span data-stu-id="8ec9c-128">respTentative</span></span>  <br/> |<span data-ttu-id="8ec9c-129">0x00000002</span><span class="sxs-lookup"><span data-stu-id="8ec9c-129">0x00000002</span></span>  <br/> |<span data-ttu-id="8ec9c-130">Это значение на собрании участника указывает на то, что участник принял приглашение на собрание под вопросом.</span><span class="sxs-lookup"><span data-stu-id="8ec9c-130">This value on the attendee's meeting indicates that the attendee has tentatively accepted the meeting request.</span></span>  <br/> |
|<span data-ttu-id="8ec9c-131">респакцептед</span><span class="sxs-lookup"><span data-stu-id="8ec9c-131">respAccepted</span></span>  <br/> |<span data-ttu-id="8ec9c-132">0x00000003</span><span class="sxs-lookup"><span data-stu-id="8ec9c-132">0x00000003</span></span>  <br/> |<span data-ttu-id="8ec9c-133">Это значение на совещании "т" пользователя указывает на то, что участник принял приглашение на собрание.</span><span class="sxs-lookup"><span data-stu-id="8ec9c-133">This value on the attendee's meeting t indicates that the attendee has accepted the meeting request.</span></span>  <br/> |
|<span data-ttu-id="8ec9c-134">респдеклинед</span><span class="sxs-lookup"><span data-stu-id="8ec9c-134">respDeclined</span></span>  <br/> |<span data-ttu-id="8ec9c-135">0x00000004</span><span class="sxs-lookup"><span data-stu-id="8ec9c-135">0x00000004</span></span>  <br/> |<span data-ttu-id="8ec9c-136">Это значение на собрании участника указывает на то, что участник отклонил приглашение на собрание.</span><span class="sxs-lookup"><span data-stu-id="8ec9c-136">This value on the attendee's meeting indicates that the attendee has declined the meeting request.</span></span>  <br/> |
|<span data-ttu-id="8ec9c-137">респнотреспондед</span><span class="sxs-lookup"><span data-stu-id="8ec9c-137">respNotResponded</span></span>  <br/> |<span data-ttu-id="8ec9c-138">0x00000005</span><span class="sxs-lookup"><span data-stu-id="8ec9c-138">0x00000005</span></span>  <br/> |<span data-ttu-id="8ec9c-139">Это значение на собрании участника указывает на то, что участника еще не ответил.</span><span class="sxs-lookup"><span data-stu-id="8ec9c-139">This value on the attendee's meeting indicates the attendee has not yet responded.</span></span> <span data-ttu-id="8ec9c-140">Это значение находится в приглашении на собрание, обновлении собрания и отмене собрания.</span><span class="sxs-lookup"><span data-stu-id="8ec9c-140">This value is on the meeting request, meeting update, and meeting cancelation.</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="8ec9c-141">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="8ec9c-141">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="8ec9c-142">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="8ec9c-142">Protocol specifications</span></span>

<span data-ttu-id="8ec9c-143">[[MS — ОКСПРОПС]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="8ec9c-143">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="8ec9c-144">Содержит определения свойств и ссылки на связанные спецификации протокола Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="8ec9c-144">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="8ec9c-145">[[MS — ОКСОКАЛ]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="8ec9c-145">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="8ec9c-146">Задает свойства и операции для встречи, приглашения на собрание и ответных сообщений.</span><span class="sxs-lookup"><span data-stu-id="8ec9c-146">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="8ec9c-147">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="8ec9c-147">Header files</span></span>

<span data-ttu-id="8ec9c-148">MAPIDEFS. h</span><span class="sxs-lookup"><span data-stu-id="8ec9c-148">Mapidefs.h</span></span>
  
> <span data-ttu-id="8ec9c-149">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="8ec9c-149">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="8ec9c-150">См. также</span><span class="sxs-lookup"><span data-stu-id="8ec9c-150">See also</span></span>



[<span data-ttu-id="8ec9c-151">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="8ec9c-151">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="8ec9c-152">Каноническое свойство MAPI</span><span class="sxs-lookup"><span data-stu-id="8ec9c-152">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="8ec9c-153">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="8ec9c-153">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="8ec9c-154">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="8ec9c-154">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

