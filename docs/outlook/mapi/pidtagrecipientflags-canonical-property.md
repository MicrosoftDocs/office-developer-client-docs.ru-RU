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
# <a name="pidtagrecipientflags-canonical-property"></a><span data-ttu-id="267e8-103">Каноническое свойство PidTagRecipientFlags</span><span class="sxs-lookup"><span data-stu-id="267e8-103">PidTagRecipientFlags Canonical Property</span></span>

  
  
<span data-ttu-id="267e8-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="267e8-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="267e8-105">Задает битовое поле, описывающее состояние получателя.</span><span class="sxs-lookup"><span data-stu-id="267e8-105">Specifies a bit field that describes the recipient status.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="267e8-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="267e8-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="267e8-107">ПР_РЕЦИПИЕНТ_ФЛАГС</span><span class="sxs-lookup"><span data-stu-id="267e8-107">PR_RECIPIENT_FLAGS</span></span>  <br/> |
|<span data-ttu-id="267e8-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="267e8-108">Identifier:</span></span>  <br/> |<span data-ttu-id="267e8-109">0x5FFD</span><span class="sxs-lookup"><span data-stu-id="267e8-109">0x5FFD</span></span>  <br/> |
|<span data-ttu-id="267e8-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="267e8-110">Data type:</span></span>  <br/> |<span data-ttu-id="267e8-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="267e8-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="267e8-112">Область:</span><span class="sxs-lookup"><span data-stu-id="267e8-112">Area:</span></span>  <br/> |<span data-ttu-id="267e8-113">Получатель транспорта</span><span class="sxs-lookup"><span data-stu-id="267e8-113">Transport recipient</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="267e8-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="267e8-114">Remarks</span></span>

<span data-ttu-id="267e8-115">Это свойство не является обязательным.</span><span class="sxs-lookup"><span data-stu-id="267e8-115">This property is not required.</span></span> <span data-ttu-id="267e8-116">Ниже приведены отдельные флаги, которые можно задать.</span><span class="sxs-lookup"><span data-stu-id="267e8-116">The following are the individual flags that can be set.</span></span>
  
|<span data-ttu-id="267e8-117">**Value**</span><span class="sxs-lookup"><span data-stu-id="267e8-117">**Value**</span></span>|<span data-ttu-id="267e8-118">**Описание**</span><span class="sxs-lookup"><span data-stu-id="267e8-118">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="267e8-119">S (РеЦипсендабле, 0x00000001)</span><span class="sxs-lookup"><span data-stu-id="267e8-119">S (recipSendable, 0x00000001)</span></span>  <br/> |<span data-ttu-id="267e8-120">Получатель — это доступный для **отправки** участник.</span><span class="sxs-lookup"><span data-stu-id="267e8-120">The recipient is a **Sendable** Attendee.</span></span> <span data-ttu-id="267e8-121">Этот флаг используется только в свойстве **диспидапптунсендаблереЦипс** ([PidLidAppointmentUnsendableRecipients](pidlidappointmentunsendablerecipients-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="267e8-121">This flag is only used in the **dispidApptUnsendableRecips** ([PidLidAppointmentUnsendableRecipients](pidlidappointmentunsendablerecipients-canonical-property.md)) property.</span></span>  <br/> |
|<span data-ttu-id="267e8-122">O (РеЦипорганизер, 0x0000002)</span><span class="sxs-lookup"><span data-stu-id="267e8-122">O (recipOrganizer, 0x0000002)</span></span>  <br/> |<span data-ttu-id="267e8-123">**РеЦипиентров** , на котором установлен этот флаг, представляет организатор собрания.</span><span class="sxs-lookup"><span data-stu-id="267e8-123">The **RecipientRow** on which this flag is set represents the meeting Organizer.</span></span>  <br/> |
|<span data-ttu-id="267e8-124">ER (РеЦипексцептионалреспонсе, 0x00000010)</span><span class="sxs-lookup"><span data-stu-id="267e8-124">ER (recipExceptionalResponse, 0x00000010)</span></span>  <br/> |<span data-ttu-id="267e8-125">Указывает, что участник предоставил ответ на исключение, в котором находится этот **реЦипиентров** .</span><span class="sxs-lookup"><span data-stu-id="267e8-125">Indicates that the attendee gave a response for the exception on which this **RecipientRow** resides.</span></span> <span data-ttu-id="267e8-126">Этот флаг используется только в **реЦипиентров** исключения внедренного объекта Message объекта собрания организатора.</span><span class="sxs-lookup"><span data-stu-id="267e8-126">This flag is only used in a **RecipientRow** of an exception embedded message object of the organizer's meeting object.</span></span>  <br/> |
|<span data-ttu-id="267e8-127">ED (РеЦипексцептионалделетед, 0x00000020)</span><span class="sxs-lookup"><span data-stu-id="267e8-127">ED (recipExceptionalDeleted, 0x00000020)</span></span>  <br/> |<span data-ttu-id="267e8-128">Указывает, что несмотря на то что **реЦипиентров** существует, он должен рассматриваться так, как если бы соответствующий получатель не был.</span><span class="sxs-lookup"><span data-stu-id="267e8-128">Indicates that although the **RecipientRow** exists, it should be treated as if the corresponding recipient does not.</span></span> <span data-ttu-id="267e8-129">Этот флаг используется только в **реЦипиентров** исключения внедренного объекта Message объекта собрания организатора.</span><span class="sxs-lookup"><span data-stu-id="267e8-129">This flag is only used in a **RecipientRow** of an exception embedded message object of the organizer's meeting object.</span></span>  <br/> |
|<span data-ttu-id="267e8-130">X (зарезервировано, 0x00000040)</span><span class="sxs-lookup"><span data-stu-id="267e8-130">X (reserved, 0x00000040)</span></span>  <br/> |<span data-ttu-id="267e8-131">Не должно быть задано.</span><span class="sxs-lookup"><span data-stu-id="267e8-131">Must not be set.</span></span>  <br/> |
|<span data-ttu-id="267e8-132">X (зарезервировано, 0x00000080)</span><span class="sxs-lookup"><span data-stu-id="267e8-132">X (reserved, 0x00000080)</span></span>  <br/> |<span data-ttu-id="267e8-133">Не должно быть задано.</span><span class="sxs-lookup"><span data-stu-id="267e8-133">Must not be set.</span></span>  <br/> |
|<span data-ttu-id="267e8-134">G (РеЦипоригинал, 0x00000100)</span><span class="sxs-lookup"><span data-stu-id="267e8-134">G (recipOriginal, 0x00000100)</span></span>  <br/> |<span data-ttu-id="267e8-135">Указывает, что получатель является исходным участником.</span><span class="sxs-lookup"><span data-stu-id="267e8-135">Indicates the recipient is an original attendee.</span></span> <span data-ttu-id="267e8-136">Этот флаг используется только в свойстве **диспидапптунсендаблереЦипс** .</span><span class="sxs-lookup"><span data-stu-id="267e8-136">This flag is only used in the **dispidApptUnsendableRecips** property.</span></span>  <br/> |
|<span data-ttu-id="267e8-137">X (зарезервировано, 0x00000200)</span><span class="sxs-lookup"><span data-stu-id="267e8-137">X (reserved, 0x00000200)</span></span>  <br/> |<span data-ttu-id="267e8-138">Резервирования.</span><span class="sxs-lookup"><span data-stu-id="267e8-138">Reserved.</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="267e8-139">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="267e8-139">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="267e8-140">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="267e8-140">Protocol specifications</span></span>

<span data-ttu-id="267e8-141">[[MS — ОКСПРОПС]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="267e8-141">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="267e8-142">Содержит ссылки на соответствующие спецификации протоколов Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="267e8-142">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="267e8-143">[[MS — ОКСОКАЛ]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="267e8-143">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="267e8-144">Задает свойства и операции для встречи, приглашения на собрание и ответных сообщений.</span><span class="sxs-lookup"><span data-stu-id="267e8-144">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="267e8-145">Файлы заГоловков</span><span class="sxs-lookup"><span data-stu-id="267e8-145">Header files</span></span>

<span data-ttu-id="267e8-146">MAPIDEFS. h</span><span class="sxs-lookup"><span data-stu-id="267e8-146">Mapidefs.h</span></span>
  
> <span data-ttu-id="267e8-147">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="267e8-147">Provides data type definitions.</span></span>
    
<span data-ttu-id="267e8-148">Мапитагс. h</span><span class="sxs-lookup"><span data-stu-id="267e8-148">Mapitags.h</span></span>
  
> <span data-ttu-id="267e8-149">Содержит определения свойств, перечисленных как альтернативные имена.</span><span class="sxs-lookup"><span data-stu-id="267e8-149">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="267e8-150">См. также</span><span class="sxs-lookup"><span data-stu-id="267e8-150">See also</span></span>



[<span data-ttu-id="267e8-151">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="267e8-151">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="267e8-152">Каноническое свойство MAPI</span><span class="sxs-lookup"><span data-stu-id="267e8-152">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="267e8-153">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="267e8-153">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="267e8-154">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="267e8-154">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

