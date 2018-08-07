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
ms.openlocfilehash: a93e5a44768cd99512189f800bf98ab6e30b575d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19811648"
---
# <a name="pidtagrecipientflags-canonical-property"></a><span data-ttu-id="9dc87-103">Каноническое свойство PidTagRecipientFlags</span><span class="sxs-lookup"><span data-stu-id="9dc87-103">PidTagRecipientFlags Canonical Property</span></span>

  
  
<span data-ttu-id="9dc87-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="9dc87-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="9dc87-105">Задает битовое поле, которое описывает состояние получателя.</span><span class="sxs-lookup"><span data-stu-id="9dc87-105">Specifies a bit field that describes the recipient status.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="9dc87-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="9dc87-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="9dc87-107">PR_RECIPIENT_FLAGS</span><span class="sxs-lookup"><span data-stu-id="9dc87-107">PR_RECIPIENT_FLAGS</span></span>  <br/> |
|<span data-ttu-id="9dc87-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="9dc87-108">Identifier:</span></span>  <br/> |<span data-ttu-id="9dc87-109">0x5FFD</span><span class="sxs-lookup"><span data-stu-id="9dc87-109">0x5FFD</span></span>  <br/> |
|<span data-ttu-id="9dc87-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="9dc87-110">Data type:</span></span>  <br/> |<span data-ttu-id="9dc87-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="9dc87-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="9dc87-112">Область:</span><span class="sxs-lookup"><span data-stu-id="9dc87-112">Area:</span></span>  <br/> |<span data-ttu-id="9dc87-113">Получатель транспорта</span><span class="sxs-lookup"><span data-stu-id="9dc87-113">Transport recipient</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="9dc87-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="9dc87-114">Remarks</span></span>

<span data-ttu-id="9dc87-115">Это свойство не требуется.</span><span class="sxs-lookup"><span data-stu-id="9dc87-115">This property is not required.</span></span> <span data-ttu-id="9dc87-116">Ниже приведены отдельные флаги, которые можно задать.</span><span class="sxs-lookup"><span data-stu-id="9dc87-116">The following are the individual flags that can be set.</span></span>
  
|<span data-ttu-id="9dc87-117">**Значение**</span><span class="sxs-lookup"><span data-stu-id="9dc87-117">**Value**</span></span>|<span data-ttu-id="9dc87-118">**Описание**</span><span class="sxs-lookup"><span data-stu-id="9dc87-118">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="9dc87-119">S (recipSendable, 0x00000001)</span><span class="sxs-lookup"><span data-stu-id="9dc87-119">S (recipSendable, 0x00000001)</span></span>  <br/> |<span data-ttu-id="9dc87-120">Получатель является **Sendable** Attendee.</span><span class="sxs-lookup"><span data-stu-id="9dc87-120">The recipient is a **Sendable** Attendee.</span></span> <span data-ttu-id="9dc87-121">Этот флаг используется только в свойстве **dispidApptUnsendableRecips** ([PidLidAppointmentUnsendableRecipients](pidlidappointmentunsendablerecipients-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="9dc87-121">This flag is only used in the **dispidApptUnsendableRecips** ([PidLidAppointmentUnsendableRecipients](pidlidappointmentunsendablerecipients-canonical-property.md)) property.</span></span>  <br/> |
|<span data-ttu-id="9dc87-122">O (recipOrganizer, 0x0000002)</span><span class="sxs-lookup"><span data-stu-id="9dc87-122">O (recipOrganizer, 0x0000002)</span></span>  <br/> |<span data-ttu-id="9dc87-123">**RecipientRow** , на котором установлен этот флаг представляет организатора собрания.</span><span class="sxs-lookup"><span data-stu-id="9dc87-123">The **RecipientRow** on which this flag is set represents the meeting Organizer.</span></span>  <br/> |
|<span data-ttu-id="9dc87-124">Аварийного восстановления (recipExceptionalResponse 0x00000010)</span><span class="sxs-lookup"><span data-stu-id="9dc87-124">ER (recipExceptionalResponse, 0x00000010)</span></span>  <br/> |<span data-ttu-id="9dc87-125">Указывает, что участник предоставили ответа для исключения, на котором находится в этом **RecipientRow** .</span><span class="sxs-lookup"><span data-stu-id="9dc87-125">Indicates that the attendee gave a response for the exception on which this **RecipientRow** resides.</span></span> <span data-ttu-id="9dc87-126">Этот флаг используется только в **RecipientRow** объекта внедренных сообщений исключения объекта организатора собрания.</span><span class="sxs-lookup"><span data-stu-id="9dc87-126">This flag is only used in a **RecipientRow** of an exception embedded message object of the organizer's meeting object.</span></span>  <br/> |
|<span data-ttu-id="9dc87-127">ED (recipExceptionalDeleted 0x00000020)</span><span class="sxs-lookup"><span data-stu-id="9dc87-127">ED (recipExceptionalDeleted, 0x00000020)</span></span>  <br/> |<span data-ttu-id="9dc87-128">Указывает, что несмотря на то, что существует **RecipientRow** , его следует рассматривать как, если соответствующий получателя не поддерживает.</span><span class="sxs-lookup"><span data-stu-id="9dc87-128">Indicates that although the **RecipientRow** exists, it should be treated as if the corresponding recipient does not.</span></span> <span data-ttu-id="9dc87-129">Этот флаг используется только в **RecipientRow** объекта внедренных сообщений исключения объекта организатора собрания.</span><span class="sxs-lookup"><span data-stu-id="9dc87-129">This flag is only used in a **RecipientRow** of an exception embedded message object of the organizer's meeting object.</span></span>  <br/> |
|<span data-ttu-id="9dc87-130">X (зарезервирован, 0x00000040)</span><span class="sxs-lookup"><span data-stu-id="9dc87-130">X (reserved, 0x00000040)</span></span>  <br/> |<span data-ttu-id="9dc87-131">Не должно быть задано.</span><span class="sxs-lookup"><span data-stu-id="9dc87-131">Must not be set.</span></span>  <br/> |
|<span data-ttu-id="9dc87-132">X (зарезервирован, 0x00000080)</span><span class="sxs-lookup"><span data-stu-id="9dc87-132">X (reserved, 0x00000080)</span></span>  <br/> |<span data-ttu-id="9dc87-133">Не должно быть задано.</span><span class="sxs-lookup"><span data-stu-id="9dc87-133">Must not be set.</span></span>  <br/> |
|<span data-ttu-id="9dc87-134">G (recipOriginal, 0x00000100)</span><span class="sxs-lookup"><span data-stu-id="9dc87-134">G (recipOriginal, 0x00000100)</span></span>  <br/> |<span data-ttu-id="9dc87-135">Указывает, что получатель является исходного участника.</span><span class="sxs-lookup"><span data-stu-id="9dc87-135">Indicates the recipient is an original attendee.</span></span> <span data-ttu-id="9dc87-136">Этот флаг используется только в свойстве **dispidApptUnsendableRecips** .</span><span class="sxs-lookup"><span data-stu-id="9dc87-136">This flag is only used in the **dispidApptUnsendableRecips** property.</span></span>  <br/> |
|<span data-ttu-id="9dc87-137">X (зарезервирован, 0x00000200)</span><span class="sxs-lookup"><span data-stu-id="9dc87-137">X (reserved, 0x00000200)</span></span>  <br/> |<span data-ttu-id="9dc87-138">Зарезервировано.</span><span class="sxs-lookup"><span data-stu-id="9dc87-138">Reserved.</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="9dc87-139">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="9dc87-139">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="9dc87-140">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="9dc87-140">Protocol specifications</span></span>

<span data-ttu-id="9dc87-141">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="9dc87-141">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="9dc87-142">Содержит ссылки на связанные спецификаций протокола Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="9dc87-142">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="9dc87-143">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="9dc87-143">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="9dc87-144">Задает свойства и операции для встречи, приглашения на собрание и ответы.</span><span class="sxs-lookup"><span data-stu-id="9dc87-144">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="9dc87-145">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="9dc87-145">Header files</span></span>

<span data-ttu-id="9dc87-146">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="9dc87-146">Mapidefs.h</span></span>
  
> <span data-ttu-id="9dc87-147">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="9dc87-147">Provides data type definitions.</span></span>
    
<span data-ttu-id="9dc87-148">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="9dc87-148">Mapitags.h</span></span>
  
> <span data-ttu-id="9dc87-149">Содержит определения свойства в списке альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="9dc87-149">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="9dc87-150">См. также</span><span class="sxs-lookup"><span data-stu-id="9dc87-150">See also</span></span>



[<span data-ttu-id="9dc87-151">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="9dc87-151">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="9dc87-152">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="9dc87-152">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="9dc87-153">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="9dc87-153">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="9dc87-154">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="9dc87-154">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

