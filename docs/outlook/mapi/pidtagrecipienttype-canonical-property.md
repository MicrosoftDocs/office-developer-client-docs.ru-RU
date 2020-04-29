---
title: Каноническое свойство PidTagRecipientType
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagRecipientType
api_type:
- COM
ms.assetid: 67e31027-6bc2-4a40-9b00-d61baef4ab0f
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 9d74fdb3acb6db94078d6090f0def050fb564cd9
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32355260"
---
# <a name="pidtagrecipienttype-canonical-property"></a><span data-ttu-id="678f1-103">Каноническое свойство PidTagRecipientType</span><span class="sxs-lookup"><span data-stu-id="678f1-103">PidTagRecipientType Canonical Property</span></span>

  
  
<span data-ttu-id="678f1-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="678f1-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="678f1-105">Содержит тип получателя сообщения.</span><span class="sxs-lookup"><span data-stu-id="678f1-105">Contains the recipient type for a message recipient.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="678f1-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="678f1-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="678f1-107">PR_RECIPIENT_TYPE</span><span class="sxs-lookup"><span data-stu-id="678f1-107">PR_RECIPIENT_TYPE</span></span>  <br/> |
|<span data-ttu-id="678f1-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="678f1-108">Identifier:</span></span>  <br/> |<span data-ttu-id="678f1-109">0x0C15</span><span class="sxs-lookup"><span data-stu-id="678f1-109">0x0C15</span></span>  <br/> |
|<span data-ttu-id="678f1-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="678f1-110">Data type:</span></span>  <br/> |<span data-ttu-id="678f1-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="678f1-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="678f1-112">Область:</span><span class="sxs-lookup"><span data-stu-id="678f1-112">Area:</span></span>  <br/> |<span data-ttu-id="678f1-113">Получатель MAPI</span><span class="sxs-lookup"><span data-stu-id="678f1-113">MAPI recipient</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="678f1-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="678f1-114">Remarks</span></span>

<span data-ttu-id="678f1-115">Тип получателя, содержащийся в этом свойстве, состоит из одного обязательного значения и одного необязательного флага.</span><span class="sxs-lookup"><span data-stu-id="678f1-115">The recipient type contained in this property consists of one required value and one optional flag.</span></span>
  
<span data-ttu-id="678f1-116">Это свойство должно содержать только одно из следующих значений:</span><span class="sxs-lookup"><span data-stu-id="678f1-116">This property must contain exactly one of the following values:</span></span>
  
<span data-ttu-id="678f1-117">MAPI_TO</span><span class="sxs-lookup"><span data-stu-id="678f1-117">MAPI_TO</span></span> 
  
> <span data-ttu-id="678f1-118">Получатель является основным (to) получателем.</span><span class="sxs-lookup"><span data-stu-id="678f1-118">The recipient is a primary (To) recipient.</span></span> <span data-ttu-id="678f1-119">Для обработки основных получателей требуются клиенты.</span><span class="sxs-lookup"><span data-stu-id="678f1-119">Clients are required to handle primary recipients.</span></span> <span data-ttu-id="678f1-120">��� ��������� ���� �������� ���������������.</span><span class="sxs-lookup"><span data-stu-id="678f1-120">All other types are optional.</span></span>
    
<span data-ttu-id="678f1-121">MAPI_CC</span><span class="sxs-lookup"><span data-stu-id="678f1-121">MAPI_CC</span></span> 
  
> <span data-ttu-id="678f1-122">Получатель — это получатель копии (CC), а получатель, который получает сообщение в дополнение к основным получателям.</span><span class="sxs-lookup"><span data-stu-id="678f1-122">The recipient is a carbon copy (CC) recipient, a recipient that receives a message in addition to the primary recipients.</span></span>
    
<span data-ttu-id="678f1-123">MAPI_BCC</span><span class="sxs-lookup"><span data-stu-id="678f1-123">MAPI_BCC</span></span> 
  
> <span data-ttu-id="678f1-124">Получатель — это получатель скрытой копии (BCC).</span><span class="sxs-lookup"><span data-stu-id="678f1-124">The recipient is a blind carbon copy (BCC) recipient.</span></span> <span data-ttu-id="678f1-125">Основной получатель и получатель копии не знают о существовании получателей СКРЫТой копии.</span><span class="sxs-lookup"><span data-stu-id="678f1-125">Primary and carbon copy recipients are unaware of the existence of BCC recipients.</span></span> 
    
<span data-ttu-id="678f1-126">MAPI_P1</span><span class="sxs-lookup"><span data-stu-id="678f1-126">MAPI_P1</span></span> 
  
> <span data-ttu-id="678f1-127">Получателю не удалось получить сообщение о предыдущей попытке.</span><span class="sxs-lookup"><span data-stu-id="678f1-127">The recipient did not successfully receive the message on the previous attempt.</span></span> <span data-ttu-id="678f1-128">Это повторная отправка более ранней передачи.</span><span class="sxs-lookup"><span data-stu-id="678f1-128">This is a resend of an earlier transmission.</span></span>
    
<span data-ttu-id="678f1-129">Кроме того, можно задать следующий флаг:</span><span class="sxs-lookup"><span data-stu-id="678f1-129">In addition, the following flag can be set:</span></span>
  
<span data-ttu-id="678f1-130">MAPI_SUBMITTED</span><span class="sxs-lookup"><span data-stu-id="678f1-130">MAPI_SUBMITTED</span></span> 
  
> <span data-ttu-id="678f1-131">Получатель уже получил сообщение и не требует его повторного получения.</span><span class="sxs-lookup"><span data-stu-id="678f1-131">The recipient has already received the message and does not need to receive it again.</span></span> <span data-ttu-id="678f1-132">Это повторная отправка более ранней передачи.</span><span class="sxs-lookup"><span data-stu-id="678f1-132">This is a resend of an earlier transmission.</span></span> <span data-ttu-id="678f1-133">Этот флаг задается в сочетании со значениями **MAPI_TO**, **MAPI_CC**и **MAPI_BCC** .</span><span class="sxs-lookup"><span data-stu-id="678f1-133">This flag is set in conjunction with the **MAPI_TO**, **MAPI_CC**, and **MAPI_BCC** values.</span></span> 
    
<span data-ttu-id="678f1-134">Значение MAPI_P1 и флаг **MAPI_SUBMITTED** используются, когда сообщение передается в связи с доставкой одного или нескольких указанных получателей.</span><span class="sxs-lookup"><span data-stu-id="678f1-134">The MAPI_P1 value and the **MAPI_SUBMITTED** flag are used when a message is being retransmitted due to nondelivery to one or more of the intended recipients.</span></span> <span data-ttu-id="678f1-135">Для такой повторной передачи клиент устанавливает **MAPI_SUBMITTED** для каждого получателя, который не требует повторного сообщения, но должен отображаться в списке получателей.</span><span class="sxs-lookup"><span data-stu-id="678f1-135">For this retransmission, the client sets **MAPI_SUBMITTED** on every recipient that does not need the message again but should be displayed in the recipient list.</span></span> <span data-ttu-id="678f1-136">Для каждого получателя, который не получал сообщение ранее, клиент сохраняет исходный получатель со своим **PR_RECIPIENT_TYPEным** значением без изменений, но дополнительно отправляет копию получателя с MAPI_P1 вместо исходного значения.</span><span class="sxs-lookup"><span data-stu-id="678f1-136">For every recipient that did not receive the message previously, the client retains the original recipient with its **PR_RECIPIENT_TYPE** value unchanged, but additionally submits a copy of the recipient with MAPI_P1 in place of the original value.</span></span> <span data-ttu-id="678f1-137">Эта копия, которая отбрасывается до фактической доставки, приводит получателя к конверту P1 и гарантирует физическую повторную передачу для этого получателя.</span><span class="sxs-lookup"><span data-stu-id="678f1-137">This copy, which is discarded before actual delivery, forces the recipient into the P1 envelope and guarantees physical retransmission to that recipient.</span></span> <span data-ttu-id="678f1-138">Для свойства **PR_RESPONSIBILITY** ([PidTagResponsibility](pidtagresponsibility-canonical-property.md)) для MAPI_P1 получателей задано значение "false".</span><span class="sxs-lookup"><span data-stu-id="678f1-138">The **PR_RESPONSIBILITY** ([PidTagResponsibility](pidtagresponsibility-canonical-property.md)) property is set to FALSE for MAPI_P1 recipients.</span></span>
  
<span data-ttu-id="678f1-139">Когда клиент отображает форму повторной отправки, отображаются только получатели MAPI_P1.</span><span class="sxs-lookup"><span data-stu-id="678f1-139">When a client displays a resend form, only the MAPI_P1 recipients are visible.</span></span> <span data-ttu-id="678f1-140">Если пользователь не введет дополнительных получателей, то при доставке сообщения список получателей отображается точно так же, как при первом отправке сообщения.</span><span class="sxs-lookup"><span data-stu-id="678f1-140">Unless the user enters additional recipients, when the message is delivered, the recipient list appears exactly as it did when the message was sent for the first time.</span></span> 
  
<span data-ttu-id="678f1-141">Свойства **PR_DISPLAY_TO** ([PidTagDisplayTo](pidtagdisplayto-canonical-property.md)), **PR_DISPLAY_CC** ([PidTagDisplayCc](pidtagdisplaycc-canonical-property.md)) и **PR_DISPLAY_BCC** ([PidTagDisplayBcc](pidtagdisplaybcc-canonical-property.md)) относятся к типу получателя.</span><span class="sxs-lookup"><span data-stu-id="678f1-141">The **PR_DISPLAY_TO** ([PidTagDisplayTo](pidtagdisplayto-canonical-property.md)), **PR_DISPLAY_CC** ([PidTagDisplayCc](pidtagdisplaycc-canonical-property.md)) and **PR_DISPLAY_BCC** ([PidTagDisplayBcc](pidtagdisplaybcc-canonical-property.md)) properties are related to recipient type.</span></span> <span data-ttu-id="678f1-142">Когда клиент вызывает **IMAPIProp сообщения:: SaveChanges** и есть по крайней мере один получатель в списке получателей, поставщик хранилища сообщений задает эти свойства следующим образом:</span><span class="sxs-lookup"><span data-stu-id="678f1-142">When a client calls a message's **IMAPIProp::SaveChanges** and there is at least one recipient in the recipient list, the message store provider sets these properties as follows:</span></span> 
  
|<span data-ttu-id="678f1-143">**Свойство**</span><span class="sxs-lookup"><span data-stu-id="678f1-143">**Property**</span></span>|<span data-ttu-id="678f1-144">**Описание**</span><span class="sxs-lookup"><span data-stu-id="678f1-144">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="678f1-145">PR_DISPLAY_TO</span><span class="sxs-lookup"><span data-stu-id="678f1-145">PR_DISPLAY_TO</span></span>  <br/> |<span data-ttu-id="678f1-146">Задайте значение TRUE, если один или несколько получателей **MAPI_TO** получателей.</span><span class="sxs-lookup"><span data-stu-id="678f1-146">Set to TRUE if one or more of the recipients are **MAPI_TO** recipients.</span></span>  <br/> |
|<span data-ttu-id="678f1-147">PR_DISPLAY_CC</span><span class="sxs-lookup"><span data-stu-id="678f1-147">PR_DISPLAY_CC</span></span>  <br/> |<span data-ttu-id="678f1-148">Задайте значение TRUE, если один или несколько получателей **MAPI_CC** получателей.</span><span class="sxs-lookup"><span data-stu-id="678f1-148">Set to TRUE if one or more of the recipients are **MAPI_CC** recipients.</span></span>  <br/> |
| <span data-ttu-id="678f1-149">PR_DISPLAY_BCC</span><span class="sxs-lookup"><span data-stu-id="678f1-149">PR_DISPLAY_BCC</span></span>  <br/> |<span data-ttu-id="678f1-150">Задайте значение TRUE, если один или несколько получателей **MAPI_BCC** получателей.</span><span class="sxs-lookup"><span data-stu-id="678f1-150">Set to TRUE if one or more of the recipients are **MAPI_BCC** recipients.</span></span>  <br/> |
   
<span data-ttu-id="678f1-151">В X. 400 конверт P1 или Delivery является сведениями, необходимыми для доставки сообщения, включая свойства адреса получателя и флаги, управляющие доставкой и ответами.</span><span class="sxs-lookup"><span data-stu-id="678f1-151">In X.400, the P1 or delivery envelope is the information needed to deliver a message, including the recipient's address properties and any option flags controlling delivery and replies.</span></span> <span data-ttu-id="678f1-152">В качестве конверта P2 или Display отображаются сведения, которые обычно отображаются для каждого получателя, кроме самого текста сообщения.</span><span class="sxs-lookup"><span data-stu-id="678f1-152">The P2 or display envelope is the information usually displayed to each recipient other than the message text itself.</span></span> <span data-ttu-id="678f1-153">Обычно она включает тему, важность, приоритет, чувствительность и время отправки, а также имя основного и скопированного получателей.</span><span class="sxs-lookup"><span data-stu-id="678f1-153">It typically includes the subject, importance, priority, sensitivity, and submission time, as well as the primary and copied recipient names.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="678f1-154">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="678f1-154">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="678f1-155">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="678f1-155">Protocol specifications</span></span>

<span data-ttu-id="678f1-156">[[MS — ОКСПРОПС]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="678f1-156">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="678f1-157">Содержит ссылки на соответствующие спецификации протоколов Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="678f1-157">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="678f1-158">[[MS — ОКСКМСГ]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="678f1-158">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="678f1-159">Обрабатывает объекты сообщений и вложений.</span><span class="sxs-lookup"><span data-stu-id="678f1-159">Handles message and attachment objects.</span></span>
    
<span data-ttu-id="678f1-160">[[MS — ОКСОМСГ]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="678f1-160">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="678f1-161">Задает свойства и операции, допустимые для объектов сообщений электронной почты.</span><span class="sxs-lookup"><span data-stu-id="678f1-161">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
<span data-ttu-id="678f1-162">[[MS — ОКСОКАЛ]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="678f1-162">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="678f1-163">Задает свойства и операции для встречи, приглашения на собрание и ответных сообщений.</span><span class="sxs-lookup"><span data-stu-id="678f1-163">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="678f1-164">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="678f1-164">Header files</span></span>

<span data-ttu-id="678f1-165">MAPIDEFS. h</span><span class="sxs-lookup"><span data-stu-id="678f1-165">Mapidefs.h</span></span>
  
> <span data-ttu-id="678f1-166">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="678f1-166">Provides data type definitions.</span></span>
    
<span data-ttu-id="678f1-167">Мапитагс. h</span><span class="sxs-lookup"><span data-stu-id="678f1-167">Mapitags.h</span></span>
  
> <span data-ttu-id="678f1-168">Содержит определения свойств, перечисленных как альтернативные имена.</span><span class="sxs-lookup"><span data-stu-id="678f1-168">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="678f1-169">См. также</span><span class="sxs-lookup"><span data-stu-id="678f1-169">See also</span></span>



[<span data-ttu-id="678f1-170">Каноническое свойство PidTagRecipientStatus</span><span class="sxs-lookup"><span data-stu-id="678f1-170">PidTagRecipientStatus Canonical Property</span></span>](pidtagrecipientstatus-canonical-property.md)
  
[<span data-ttu-id="678f1-171">Каноническое свойство PidTagDisplayTo</span><span class="sxs-lookup"><span data-stu-id="678f1-171">PidTagDisplayTo Canonical Property</span></span>](pidtagdisplayto-canonical-property.md)
  
[<span data-ttu-id="678f1-172">Каноническое свойство PidTagDisplayBcc</span><span class="sxs-lookup"><span data-stu-id="678f1-172">PidTagDisplayBcc Canonical Property</span></span>](pidtagdisplaybcc-canonical-property.md)
  
[<span data-ttu-id="678f1-173">Каноническое свойство PidTagDisplayCc</span><span class="sxs-lookup"><span data-stu-id="678f1-173">PidTagDisplayCc Canonical Property</span></span>](pidtagdisplaycc-canonical-property.md)


[<span data-ttu-id="678f1-174">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="678f1-174">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="678f1-175">Каноническое свойство MAPI</span><span class="sxs-lookup"><span data-stu-id="678f1-175">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="678f1-176">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="678f1-176">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="678f1-177">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="678f1-177">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

