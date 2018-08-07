---
title: Каноническое свойство PidTagRecipientTrackStatus
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagRecipientTrackStatus
api_type:
- COM
ms.assetid: d619b5e7-2867-44fc-9b42-123bb1bf7bde
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: cbc934eec5331a0302ba222108ee92a0dc696b1f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19811684"
---
# <a name="pidtagrecipienttrackstatus-canonical-property"></a><span data-ttu-id="5ff01-103">Каноническое свойство PidTagRecipientTrackStatus</span><span class="sxs-lookup"><span data-stu-id="5ff01-103">PidTagRecipientTrackStatus Canonical Property</span></span>

  
  
<span data-ttu-id="5ff01-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="5ff01-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="5ff01-105">Указывает состояние ответ, возвращенный участником.</span><span class="sxs-lookup"><span data-stu-id="5ff01-105">Indicates the response status returned by the attendee.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="5ff01-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="5ff01-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="5ff01-107">PR_RECIPIENT_TRACKSTATUS</span><span class="sxs-lookup"><span data-stu-id="5ff01-107">PR_RECIPIENT_TRACKSTATUS</span></span>  <br/> |
|<span data-ttu-id="5ff01-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="5ff01-108">Identifier:</span></span>  <br/> |<span data-ttu-id="5ff01-109">0x5FFF</span><span class="sxs-lookup"><span data-stu-id="5ff01-109">0x5FFF</span></span>  <br/> |
|<span data-ttu-id="5ff01-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="5ff01-110">Data type:</span></span>  <br/> |<span data-ttu-id="5ff01-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="5ff01-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="5ff01-112">Область:</span><span class="sxs-lookup"><span data-stu-id="5ff01-112">Area:</span></span>  <br/> |<span data-ttu-id="5ff01-113">Получатель транспорта</span><span class="sxs-lookup"><span data-stu-id="5ff01-113">Transport recipient</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="5ff01-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="5ff01-114">Remarks</span></span>

<span data-ttu-id="5ff01-115">Если это значение не задано, то должен быть предполагается respNone.</span><span class="sxs-lookup"><span data-stu-id="5ff01-115">If this value is not set, it must be assumed to be respNone.</span></span> <span data-ttu-id="5ff01-116">В противном случае оно должно быть одно из следующих:</span><span class="sxs-lookup"><span data-stu-id="5ff01-116">Otherwise, it must be one of the following:</span></span>
  
|<span data-ttu-id="5ff01-117">**Состояние ответа**</span><span class="sxs-lookup"><span data-stu-id="5ff01-117">**Response status**</span></span>|<span data-ttu-id="5ff01-118">**Значение**</span><span class="sxs-lookup"><span data-stu-id="5ff01-118">**Value**</span></span>|<span data-ttu-id="5ff01-119">**Описание**</span><span class="sxs-lookup"><span data-stu-id="5ff01-119">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="5ff01-120">respNone</span><span class="sxs-lookup"><span data-stu-id="5ff01-120">respNone</span></span>  <br/> |<span data-ttu-id="5ff01-121">0x00000000</span><span class="sxs-lookup"><span data-stu-id="5ff01-121">0x00000000</span></span>  <br/> |<span data-ttu-id="5ff01-122">Нет ответа необходим для этого объекта.</span><span class="sxs-lookup"><span data-stu-id="5ff01-122">No response is required for this object.</span></span> <span data-ttu-id="5ff01-123">Это обоснование для объектов встречи и собрания объекты ответа.</span><span class="sxs-lookup"><span data-stu-id="5ff01-123">This is the case for appointment objects and meeting response objects.</span></span>  <br/> |
|<span data-ttu-id="5ff01-124">respTentative</span><span class="sxs-lookup"><span data-stu-id="5ff01-124">respTentative</span></span>  <br/> |<span data-ttu-id="5ff01-125">0x00000002</span><span class="sxs-lookup"><span data-stu-id="5ff01-125">0x00000002</span></span>  <br/> |<span data-ttu-id="5ff01-126">Это значение в объект участника собрания указывает, что участником условно принял приглашение на собрание объекта запроса.</span><span class="sxs-lookup"><span data-stu-id="5ff01-126">This value on the attendee's meeting object indicates that the attendee has tentatively accepted the meeting request object.</span></span>  <br/> |
|<span data-ttu-id="5ff01-127">respAccepted</span><span class="sxs-lookup"><span data-stu-id="5ff01-127">respAccepted</span></span>  <br/> |<span data-ttu-id="5ff01-128">0x00000003</span><span class="sxs-lookup"><span data-stu-id="5ff01-128">0x00000003</span></span>  <br/> |<span data-ttu-id="5ff01-129">Это значение в объект участника собрания указывает, что участник принял приглашение на собрание объекта запроса.</span><span class="sxs-lookup"><span data-stu-id="5ff01-129">This value on the attendee's meeting object indicates that the attendee has accepted the meeting request object.</span></span>  <br/> |
|<span data-ttu-id="5ff01-130">respDeclined</span><span class="sxs-lookup"><span data-stu-id="5ff01-130">respDeclined</span></span>  <br/> |<span data-ttu-id="5ff01-131">0x00000004</span><span class="sxs-lookup"><span data-stu-id="5ff01-131">0x00000004</span></span>  <br/> |<span data-ttu-id="5ff01-132">Это значение в объект участника собрания указывает, что участник отклонил собрания объекта запроса.</span><span class="sxs-lookup"><span data-stu-id="5ff01-132">This value on the attendee's meeting object indicates that the attendee has declined the meeting request object.</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="5ff01-133">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="5ff01-133">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="5ff01-134">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="5ff01-134">Protocol specifications</span></span>

<span data-ttu-id="5ff01-135">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="5ff01-135">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="5ff01-136">Содержит ссылки на связанные спецификаций протокола Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="5ff01-136">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="5ff01-137">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="5ff01-137">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="5ff01-138">Задает свойства и операции для встречи, приглашения на собрание и ответы.</span><span class="sxs-lookup"><span data-stu-id="5ff01-138">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
<span data-ttu-id="5ff01-139">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="5ff01-139">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="5ff01-140">Обрабатывает объекты сообщения и вложения.</span><span class="sxs-lookup"><span data-stu-id="5ff01-140">Handles message and attachment objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="5ff01-141">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="5ff01-141">Header files</span></span>

<span data-ttu-id="5ff01-142">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="5ff01-142">Mapidefs.h</span></span>
  
> <span data-ttu-id="5ff01-143">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="5ff01-143">Provides data type definitions.</span></span>
    
<span data-ttu-id="5ff01-144">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="5ff01-144">Mapitags.h</span></span>
  
> <span data-ttu-id="5ff01-145">Содержит определения свойства в списке альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="5ff01-145">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="5ff01-146">См. также</span><span class="sxs-lookup"><span data-stu-id="5ff01-146">See also</span></span>



[<span data-ttu-id="5ff01-147">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="5ff01-147">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="5ff01-148">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="5ff01-148">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="5ff01-149">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="5ff01-149">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="5ff01-150">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="5ff01-150">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

