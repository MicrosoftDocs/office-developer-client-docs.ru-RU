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
ms.openlocfilehash: 074bcf7c051b78bc32caf66502747e7fb1ab6b79
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25389892"
---
# <a name="pidtagrecipienttrackstatus-canonical-property"></a><span data-ttu-id="7cf5a-103">Каноническое свойство PidTagRecipientTrackStatus</span><span class="sxs-lookup"><span data-stu-id="7cf5a-103">PidTagRecipientTrackStatus Canonical Property</span></span>

  
  
<span data-ttu-id="7cf5a-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7cf5a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7cf5a-105">Указывает состояние ответ, возвращенный участником.</span><span class="sxs-lookup"><span data-stu-id="7cf5a-105">Indicates the response status returned by the attendee.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="7cf5a-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="7cf5a-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="7cf5a-107">PR_RECIPIENT_TRACKSTATUS</span><span class="sxs-lookup"><span data-stu-id="7cf5a-107">PR_RECIPIENT_TRACKSTATUS</span></span>  <br/> |
|<span data-ttu-id="7cf5a-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="7cf5a-108">Identifier:</span></span>  <br/> |<span data-ttu-id="7cf5a-109">0x5FFF</span><span class="sxs-lookup"><span data-stu-id="7cf5a-109">0x5FFF</span></span>  <br/> |
|<span data-ttu-id="7cf5a-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="7cf5a-110">Data type:</span></span>  <br/> |<span data-ttu-id="7cf5a-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="7cf5a-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="7cf5a-112">Область:</span><span class="sxs-lookup"><span data-stu-id="7cf5a-112">Area:</span></span>  <br/> |<span data-ttu-id="7cf5a-113">Получатель транспорта</span><span class="sxs-lookup"><span data-stu-id="7cf5a-113">Transport recipient</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="7cf5a-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="7cf5a-114">Remarks</span></span>

<span data-ttu-id="7cf5a-115">Если это значение не задано, то должен быть предполагается respNone.</span><span class="sxs-lookup"><span data-stu-id="7cf5a-115">If this value is not set, it must be assumed to be respNone.</span></span> <span data-ttu-id="7cf5a-116">В противном случае оно должно быть одно из следующих:</span><span class="sxs-lookup"><span data-stu-id="7cf5a-116">Otherwise, it must be one of the following:</span></span>
  
|<span data-ttu-id="7cf5a-117">**Состояние ответа**</span><span class="sxs-lookup"><span data-stu-id="7cf5a-117">**Response status**</span></span>|<span data-ttu-id="7cf5a-118">**Значение**</span><span class="sxs-lookup"><span data-stu-id="7cf5a-118">**Value**</span></span>|<span data-ttu-id="7cf5a-119">**Описание**</span><span class="sxs-lookup"><span data-stu-id="7cf5a-119">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="7cf5a-120">respNone</span><span class="sxs-lookup"><span data-stu-id="7cf5a-120">respNone</span></span>  <br/> |<span data-ttu-id="7cf5a-121">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7cf5a-121">0x00000000</span></span>  <br/> |<span data-ttu-id="7cf5a-122">Нет ответа необходим для этого объекта.</span><span class="sxs-lookup"><span data-stu-id="7cf5a-122">No response is required for this object.</span></span> <span data-ttu-id="7cf5a-123">Это обоснование для объектов встречи и собрания объекты ответа.</span><span class="sxs-lookup"><span data-stu-id="7cf5a-123">This is the case for appointment objects and meeting response objects.</span></span>  <br/> |
|<span data-ttu-id="7cf5a-124">respTentative</span><span class="sxs-lookup"><span data-stu-id="7cf5a-124">respTentative</span></span>  <br/> |<span data-ttu-id="7cf5a-125">0x00000002</span><span class="sxs-lookup"><span data-stu-id="7cf5a-125">0x00000002</span></span>  <br/> |<span data-ttu-id="7cf5a-126">Это значение в объект участника собрания указывает, что участником условно принял приглашение на собрание объекта запроса.</span><span class="sxs-lookup"><span data-stu-id="7cf5a-126">This value on the attendee's meeting object indicates that the attendee has tentatively accepted the meeting request object.</span></span>  <br/> |
|<span data-ttu-id="7cf5a-127">respAccepted</span><span class="sxs-lookup"><span data-stu-id="7cf5a-127">respAccepted</span></span>  <br/> |<span data-ttu-id="7cf5a-128">0x00000003</span><span class="sxs-lookup"><span data-stu-id="7cf5a-128">0x00000003</span></span>  <br/> |<span data-ttu-id="7cf5a-129">Это значение в объект участника собрания указывает, что участник принял приглашение на собрание объекта запроса.</span><span class="sxs-lookup"><span data-stu-id="7cf5a-129">This value on the attendee's meeting object indicates that the attendee has accepted the meeting request object.</span></span>  <br/> |
|<span data-ttu-id="7cf5a-130">respDeclined</span><span class="sxs-lookup"><span data-stu-id="7cf5a-130">respDeclined</span></span>  <br/> |<span data-ttu-id="7cf5a-131">0x00000004</span><span class="sxs-lookup"><span data-stu-id="7cf5a-131">0x00000004</span></span>  <br/> |<span data-ttu-id="7cf5a-132">Это значение в объект участника собрания указывает, что участник отклонил собрания объекта запроса.</span><span class="sxs-lookup"><span data-stu-id="7cf5a-132">This value on the attendee's meeting object indicates that the attendee has declined the meeting request object.</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="7cf5a-133">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="7cf5a-133">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="7cf5a-134">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="7cf5a-134">Protocol specifications</span></span>

<span data-ttu-id="7cf5a-135">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="7cf5a-135">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="7cf5a-136">Содержит ссылки на связанные спецификаций протокола Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="7cf5a-136">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="7cf5a-137">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="7cf5a-137">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="7cf5a-138">Задает свойства и операции для встречи, приглашения на собрание и ответы.</span><span class="sxs-lookup"><span data-stu-id="7cf5a-138">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
<span data-ttu-id="7cf5a-139">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="7cf5a-139">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="7cf5a-140">Обрабатывает объекты сообщения и вложения.</span><span class="sxs-lookup"><span data-stu-id="7cf5a-140">Handles message and attachment objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="7cf5a-141">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="7cf5a-141">Header files</span></span>

<span data-ttu-id="7cf5a-142">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="7cf5a-142">Mapidefs.h</span></span>
  
> <span data-ttu-id="7cf5a-143">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="7cf5a-143">Provides data type definitions.</span></span>
    
<span data-ttu-id="7cf5a-144">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="7cf5a-144">Mapitags.h</span></span>
  
> <span data-ttu-id="7cf5a-145">Содержит определения свойства в списке альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="7cf5a-145">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="7cf5a-146">См. также</span><span class="sxs-lookup"><span data-stu-id="7cf5a-146">See also</span></span>



[<span data-ttu-id="7cf5a-147">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="7cf5a-147">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="7cf5a-148">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="7cf5a-148">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="7cf5a-149">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="7cf5a-149">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="7cf5a-150">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="7cf5a-150">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

