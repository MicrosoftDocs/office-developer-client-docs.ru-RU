---
title: Каноническое свойство PidTagRecipientFlags
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagRecipientFlags
api_type:
- COM
ms.assetid: 9fbe537f-b5fe-48a2-803c-653c50c82efd
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 7b791d75c2a76ea1a504c0d8862dd20f5365b475
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32356702"
---
# <a name="pidtagrecipientflags-canonical-property"></a><span data-ttu-id="c758c-103">Каноническое свойство PidTagRecipientFlags</span><span class="sxs-lookup"><span data-stu-id="c758c-103">PidTagRecipientFlags Canonical Property</span></span>

  
  
<span data-ttu-id="c758c-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c758c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c758c-105">Указывает немного поле, которое описывает состояние получателя.</span><span class="sxs-lookup"><span data-stu-id="c758c-105">Specifies a bit field that describes the recipient status.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="c758c-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="c758c-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="c758c-107">PR_RECIPIENT_FLAGS</span><span class="sxs-lookup"><span data-stu-id="c758c-107">PR_RECIPIENT_FLAGS</span></span>  <br/> |
|<span data-ttu-id="c758c-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="c758c-108">Identifier:</span></span>  <br/> |<span data-ttu-id="c758c-109">0x5FFD</span><span class="sxs-lookup"><span data-stu-id="c758c-109">0x5FFD</span></span>  <br/> |
|<span data-ttu-id="c758c-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="c758c-110">Data type:</span></span>  <br/> |<span data-ttu-id="c758c-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="c758c-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="c758c-112">Область:</span><span class="sxs-lookup"><span data-stu-id="c758c-112">Area:</span></span>  <br/> |<span data-ttu-id="c758c-113">Получатель транспорта</span><span class="sxs-lookup"><span data-stu-id="c758c-113">Transport recipient</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c758c-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="c758c-114">Remarks</span></span>

<span data-ttu-id="c758c-115">Это свойство не требуется.</span><span class="sxs-lookup"><span data-stu-id="c758c-115">This property is not required.</span></span> <span data-ttu-id="c758c-116">Ниже приводится отдельный флажок, который можно установить.</span><span class="sxs-lookup"><span data-stu-id="c758c-116">The following are the individual flags that can be set.</span></span>
  
|<span data-ttu-id="c758c-117">**Значение**</span><span class="sxs-lookup"><span data-stu-id="c758c-117">**Value**</span></span>|<span data-ttu-id="c758c-118">**Описание**</span><span class="sxs-lookup"><span data-stu-id="c758c-118">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="c758c-119">S (recipSendable, 0x00000001)</span><span class="sxs-lookup"><span data-stu-id="c758c-119">S (recipSendable, 0x00000001)</span></span>  <br/> |<span data-ttu-id="c758c-120">Получатель — **отправимый участник.**</span><span class="sxs-lookup"><span data-stu-id="c758c-120">The recipient is a **Sendable** Attendee.</span></span> <span data-ttu-id="c758c-121">Этот флаг используется только в **свойстве dispidApptUnsendableRecips** [(PidLidAppointmentUnsendableRecipients).](pidlidappointmentunsendablerecipients-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="c758c-121">This flag is only used in the **dispidApptUnsendableRecips** ([PidLidAppointmentUnsendableRecipients](pidlidappointmentunsendablerecipients-canonical-property.md)) property.</span></span>  <br/> |
|<span data-ttu-id="c758c-122">O (recipOrganizer, 0x0000002)</span><span class="sxs-lookup"><span data-stu-id="c758c-122">O (recipOrganizer, 0x0000002)</span></span>  <br/> |<span data-ttu-id="c758c-123">**RecipientRow,** на котором установлен этот флаг, представляет организатор собрания.</span><span class="sxs-lookup"><span data-stu-id="c758c-123">The **RecipientRow** on which this flag is set represents the meeting Organizer.</span></span>  <br/> |
|<span data-ttu-id="c758c-124">ER (recipExceptionalResponse, 0x00000010)</span><span class="sxs-lookup"><span data-stu-id="c758c-124">ER (recipExceptionalResponse, 0x00000010)</span></span>  <br/> |<span data-ttu-id="c758c-125">Указывает, что участник дал ответ на исключение, на котором находится **этот RecipientRow.**</span><span class="sxs-lookup"><span data-stu-id="c758c-125">Indicates that the attendee gave a response for the exception on which this **RecipientRow** resides.</span></span> <span data-ttu-id="c758c-126">Этот флаг используется только в **объекте RecipientRow** встроенного объекта сообщения исключения объекта собрания организатора.</span><span class="sxs-lookup"><span data-stu-id="c758c-126">This flag is only used in a **RecipientRow** of an exception embedded message object of the organizer's meeting object.</span></span>  <br/> |
|<span data-ttu-id="c758c-127">ED (recipExceptionalDeleted, 0x00000020)</span><span class="sxs-lookup"><span data-stu-id="c758c-127">ED (recipExceptionalDeleted, 0x00000020)</span></span>  <br/> |<span data-ttu-id="c758c-128">Указывает, что, хотя **RecipientRow существует,** его следует рассматривать как если бы соответствующий получатель этого не сделал.</span><span class="sxs-lookup"><span data-stu-id="c758c-128">Indicates that although the **RecipientRow** exists, it should be treated as if the corresponding recipient does not.</span></span> <span data-ttu-id="c758c-129">Этот флаг используется только в **объекте RecipientRow** встроенного объекта сообщения исключения объекта собрания организатора.</span><span class="sxs-lookup"><span data-stu-id="c758c-129">This flag is only used in a **RecipientRow** of an exception embedded message object of the organizer's meeting object.</span></span>  <br/> |
|<span data-ttu-id="c758c-130">X (зарезервировано, 0x00000040)</span><span class="sxs-lookup"><span data-stu-id="c758c-130">X (reserved, 0x00000040)</span></span>  <br/> |<span data-ttu-id="c758c-131">Не следует устанавливать.</span><span class="sxs-lookup"><span data-stu-id="c758c-131">Must not be set.</span></span>  <br/> |
|<span data-ttu-id="c758c-132">X (зарезервировано, 0x00000080)</span><span class="sxs-lookup"><span data-stu-id="c758c-132">X (reserved, 0x00000080)</span></span>  <br/> |<span data-ttu-id="c758c-133">Не следует устанавливать.</span><span class="sxs-lookup"><span data-stu-id="c758c-133">Must not be set.</span></span>  <br/> |
|<span data-ttu-id="c758c-134">G (recipOriginal, 0x00000100)</span><span class="sxs-lookup"><span data-stu-id="c758c-134">G (recipOriginal, 0x00000100)</span></span>  <br/> |<span data-ttu-id="c758c-135">Указывает, что получатель — это первоначальный участник.</span><span class="sxs-lookup"><span data-stu-id="c758c-135">Indicates the recipient is an original attendee.</span></span> <span data-ttu-id="c758c-136">Этот флаг используется только в **свойстве dispidApptUnsendableRecips.**</span><span class="sxs-lookup"><span data-stu-id="c758c-136">This flag is only used in the **dispidApptUnsendableRecips** property.</span></span>  <br/> |
|<span data-ttu-id="c758c-137">X (зарезервировано, 0x00000200)</span><span class="sxs-lookup"><span data-stu-id="c758c-137">X (reserved, 0x00000200)</span></span>  <br/> |<span data-ttu-id="c758c-138">Зарезервировано.</span><span class="sxs-lookup"><span data-stu-id="c758c-138">Reserved.</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="c758c-139">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="c758c-139">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="c758c-140">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="c758c-140">Protocol specifications</span></span>

<span data-ttu-id="c758c-141">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c758c-141">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c758c-142">Содержит ссылки на связанные Exchange Server протоколы.</span><span class="sxs-lookup"><span data-stu-id="c758c-142">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="c758c-143">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c758c-143">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c758c-144">Указывает свойства и операции для встреч, запросов на собрания и ответных сообщений.</span><span class="sxs-lookup"><span data-stu-id="c758c-144">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="c758c-145">Файлы заголовки</span><span class="sxs-lookup"><span data-stu-id="c758c-145">Header files</span></span>

<span data-ttu-id="c758c-146">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="c758c-146">Mapidefs.h</span></span>
  
> <span data-ttu-id="c758c-147">Предоставляет определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="c758c-147">Provides data type definitions.</span></span>
    
<span data-ttu-id="c758c-148">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="c758c-148">Mapitags.h</span></span>
  
> <span data-ttu-id="c758c-149">Содержит определения свойств, перечисленных в качестве альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="c758c-149">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="c758c-150">См. также</span><span class="sxs-lookup"><span data-stu-id="c758c-150">See also</span></span>



[<span data-ttu-id="c758c-151">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="c758c-151">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="c758c-152">Канонические свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="c758c-152">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="c758c-153">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="c758c-153">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="c758c-154">Сопоставление имен MAPI с каноническими именами свойств</span><span class="sxs-lookup"><span data-stu-id="c758c-154">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

