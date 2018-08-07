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
ms.openlocfilehash: 0218ff558e9dfca2f73bbad2dc42cdb7bd7121fc
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19811694"
---
# <a name="pidtagrecipienttype-canonical-property"></a><span data-ttu-id="d9a37-103">Каноническое свойство PidTagRecipientType</span><span class="sxs-lookup"><span data-stu-id="d9a37-103">PidTagRecipientType Canonical Property</span></span>

  
  
<span data-ttu-id="d9a37-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="d9a37-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="d9a37-105">Содержит тип получателя для получателя сообщения.</span><span class="sxs-lookup"><span data-stu-id="d9a37-105">Contains the recipient type for a message recipient.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="d9a37-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="d9a37-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="d9a37-107">PR_RECIPIENT_TYPE</span><span class="sxs-lookup"><span data-stu-id="d9a37-107">PR_RECIPIENT_TYPE</span></span>  <br/> |
|<span data-ttu-id="d9a37-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="d9a37-108">Identifier:</span></span>  <br/> |<span data-ttu-id="d9a37-109">0x0C15</span><span class="sxs-lookup"><span data-stu-id="d9a37-109">0x0C15</span></span>  <br/> |
|<span data-ttu-id="d9a37-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="d9a37-110">Data type:</span></span>  <br/> |<span data-ttu-id="d9a37-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="d9a37-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="d9a37-112">Область:</span><span class="sxs-lookup"><span data-stu-id="d9a37-112">Area:</span></span>  <br/> |<span data-ttu-id="d9a37-113">Получатель MAPI</span><span class="sxs-lookup"><span data-stu-id="d9a37-113">MAPI recipient</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d9a37-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="d9a37-114">Remarks</span></span>

<span data-ttu-id="d9a37-115">Тип получателя, содержащиеся в этом свойстве состоит из одного необходимые значения и один необязательный флаг.</span><span class="sxs-lookup"><span data-stu-id="d9a37-115">The recipient type contained in this property consists of one required value and one optional flag.</span></span>
  
<span data-ttu-id="d9a37-116">Это свойство должно содержать только один из следующих значений:</span><span class="sxs-lookup"><span data-stu-id="d9a37-116">This property must contain exactly one of the following values:</span></span>
  
<span data-ttu-id="d9a37-117">MAPI_TO</span><span class="sxs-lookup"><span data-stu-id="d9a37-117">MAPI_TO</span></span> 
  
> <span data-ttu-id="d9a37-118">Получатель является основным (получателю).</span><span class="sxs-lookup"><span data-stu-id="d9a37-118">The recipient is a primary (To) recipient.</span></span> <span data-ttu-id="d9a37-119">Клиентам требуется обрабатывать получателей.</span><span class="sxs-lookup"><span data-stu-id="d9a37-119">Clients are required to handle primary recipients.</span></span> <span data-ttu-id="d9a37-120">��� ��������� ���� �������� ���������������.</span><span class="sxs-lookup"><span data-stu-id="d9a37-120">All other types are optional.</span></span>
    
<span data-ttu-id="d9a37-121">MAPI_CC</span><span class="sxs-lookup"><span data-stu-id="d9a37-121">MAPI_CC</span></span> 
  
> <span data-ttu-id="d9a37-122">Получатель является получателей скрытой копии (CC), получателя, который получает сообщение в дополнение к получателей.</span><span class="sxs-lookup"><span data-stu-id="d9a37-122">The recipient is a carbon copy (CC) recipient, a recipient that receives a message in addition to the primary recipients.</span></span>
    
<span data-ttu-id="d9a37-123">MAPI_BCC</span><span class="sxs-lookup"><span data-stu-id="d9a37-123">MAPI_BCC</span></span> 
  
> <span data-ttu-id="d9a37-124">Получатель является получателей скрытой копии (СК).</span><span class="sxs-lookup"><span data-stu-id="d9a37-124">The recipient is a blind carbon copy (BCC) recipient.</span></span> <span data-ttu-id="d9a37-125">Основная база данных и копии получатели не знают о наличии получателей скрытой копии.</span><span class="sxs-lookup"><span data-stu-id="d9a37-125">Primary and carbon copy recipients are unaware of the existence of BCC recipients.</span></span> 
    
<span data-ttu-id="d9a37-126">MAPI_P1</span><span class="sxs-lookup"><span data-stu-id="d9a37-126">MAPI_P1</span></span> 
  
> <span data-ttu-id="d9a37-127">Получатель не получил сообщение на Предыдущая попытка успешно.</span><span class="sxs-lookup"><span data-stu-id="d9a37-127">The recipient did not successfully receive the message on the previous attempt.</span></span> <span data-ttu-id="d9a37-128">Это отправить более ранних передачи.</span><span class="sxs-lookup"><span data-stu-id="d9a37-128">This is a resend of an earlier transmission.</span></span>
    
<span data-ttu-id="d9a37-129">Кроме того можно задать следующий флаг:</span><span class="sxs-lookup"><span data-stu-id="d9a37-129">In addition, the following flag can be set:</span></span>
  
<span data-ttu-id="d9a37-130">MAPI_SUBMITTED</span><span class="sxs-lookup"><span data-stu-id="d9a37-130">MAPI_SUBMITTED</span></span> 
  
> <span data-ttu-id="d9a37-131">Получатель уже получил сообщение и не требуется получать еще раз.</span><span class="sxs-lookup"><span data-stu-id="d9a37-131">The recipient has already received the message and does not need to receive it again.</span></span> <span data-ttu-id="d9a37-132">Это отправить более ранних передачи.</span><span class="sxs-lookup"><span data-stu-id="d9a37-132">This is a resend of an earlier transmission.</span></span> <span data-ttu-id="d9a37-133">Этот флаг устанавливается вместе с **MAPI_TO**, **MAPI_CC**и **MAPI_BCC** значения.</span><span class="sxs-lookup"><span data-stu-id="d9a37-133">This flag is set in conjunction with the **MAPI_TO**, **MAPI_CC**, and **MAPI_BCC** values.</span></span> 
    
<span data-ttu-id="d9a37-134">Значение MAPI_P1 и флаг **MAPI_SUBMITTED** используются повторно отправлено сообщение из-за недоставке к одному или нескольким указанным получателям.</span><span class="sxs-lookup"><span data-stu-id="d9a37-134">The MAPI_P1 value and the **MAPI_SUBMITTED** flag are used when a message is being retransmitted due to nondelivery to one or more of the intended recipients.</span></span> <span data-ttu-id="d9a37-135">Для этой повторной передачи клиента задает **MAPI_SUBMITTED** для каждого получателя, который не обязательно сообщение еще раз, но должно отображаться в списке получателей.</span><span class="sxs-lookup"><span data-stu-id="d9a37-135">For this retransmission, the client sets **MAPI_SUBMITTED** on every recipient that does not need the message again but should be displayed in the recipient list.</span></span> <span data-ttu-id="d9a37-136">Для каждого получателя, который ранее не получил сообщение клиент сохраняет исходный получатель на **PR_RECIPIENT_TYPE** значение без изменений, но кроме того отправляет копию получателя с MAPI_P1 вместо исходное значение.</span><span class="sxs-lookup"><span data-stu-id="d9a37-136">For every recipient that did not receive the message previously, the client retains the original recipient with its **PR_RECIPIENT_TYPE** value unchanged, but additionally submits a copy of the recipient with MAPI_P1 in place of the original value.</span></span> <span data-ttu-id="d9a37-137">Эта копия, удаляется перед доставкой фактический принудительно получателя в конверте P1 и гарантирует физических повторной передачи получателя.</span><span class="sxs-lookup"><span data-stu-id="d9a37-137">This copy, which is discarded before actual delivery, forces the recipient into the P1 envelope and guarantees physical retransmission to that recipient.</span></span> <span data-ttu-id="d9a37-138">Свойство **PR_RESPONSIBILITY** ([PidTagResponsibility](pidtagresponsibility-canonical-property.md)) задано значение FALSE для MAPI_P1 получателей.</span><span class="sxs-lookup"><span data-stu-id="d9a37-138">The **PR_RESPONSIBILITY** ([PidTagResponsibility](pidtagresponsibility-canonical-property.md)) property is set to FALSE for MAPI_P1 recipients.</span></span>
  
<span data-ttu-id="d9a37-139">При клиента отображается форма отправить, отображаются только MAPI_P1 получателей.</span><span class="sxs-lookup"><span data-stu-id="d9a37-139">When a client displays a resend form, only the MAPI_P1 recipients are visible.</span></span> <span data-ttu-id="d9a37-140">Если пользователь вводит дополнительных получателей при доставке сообщения, список получателей отображается точно так же, как и когда сообщение было отправлено в первый раз.</span><span class="sxs-lookup"><span data-stu-id="d9a37-140">Unless the user enters additional recipients, when the message is delivered, the recipient list appears exactly as it did when the message was sent for the first time.</span></span> 
  
<span data-ttu-id="d9a37-141">**PR_DISPLAY_TO** ([PidTagDisplayTo](pidtagdisplayto-canonical-property.md)), **PR_DISPLAY_CC** ([PidTagDisplayCc](pidtagdisplaycc-canonical-property.md)) и **PR_DISPLAY_BCC** ([PidTagDisplayBcc](pidtagdisplaybcc-canonical-property.md)) свойства связаны с тип получателя.</span><span class="sxs-lookup"><span data-stu-id="d9a37-141">The **PR_DISPLAY_TO** ([PidTagDisplayTo](pidtagdisplayto-canonical-property.md)), **PR_DISPLAY_CC** ([PidTagDisplayCc](pidtagdisplaycc-canonical-property.md)) and **PR_DISPLAY_BCC** ([PidTagDisplayBcc](pidtagdisplaybcc-canonical-property.md)) properties are related to recipient type.</span></span> <span data-ttu-id="d9a37-142">Если клиент вызывает сообщение **IMAPIProp::SaveChanges** и имеется хотя бы одного получателя в список получателей, поставщик хранения сообщений задает эти свойства следующим образом:</span><span class="sxs-lookup"><span data-stu-id="d9a37-142">When a client calls a message's **IMAPIProp::SaveChanges** and there is at least one recipient in the recipient list, the message store provider sets these properties as follows:</span></span> 
  
|<span data-ttu-id="d9a37-143">**Свойство**</span><span class="sxs-lookup"><span data-stu-id="d9a37-143">**Property**</span></span>|<span data-ttu-id="d9a37-144">**Описание**</span><span class="sxs-lookup"><span data-stu-id="d9a37-144">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="d9a37-145">PR_DISPLAY_TO</span><span class="sxs-lookup"><span data-stu-id="d9a37-145">PR_DISPLAY_TO</span></span>  <br/> |<span data-ttu-id="d9a37-146">Задайте значение TRUE, если один или несколько получателей, **MAPI_TO** получателей.</span><span class="sxs-lookup"><span data-stu-id="d9a37-146">Set to TRUE if one or more of the recipients are **MAPI_TO** recipients.</span></span>  <br/> |
|<span data-ttu-id="d9a37-147">PR_DISPLAY_CC</span><span class="sxs-lookup"><span data-stu-id="d9a37-147">PR_DISPLAY_CC</span></span>  <br/> |<span data-ttu-id="d9a37-148">Задайте значение TRUE, если один или несколько получателей, **MAPI_CC** получателей.</span><span class="sxs-lookup"><span data-stu-id="d9a37-148">Set to TRUE if one or more of the recipients are **MAPI_CC** recipients.</span></span>  <br/> |
| <span data-ttu-id="d9a37-149">PR_DISPLAY_BCC</span><span class="sxs-lookup"><span data-stu-id="d9a37-149">PR_DISPLAY_BCC</span></span>  <br/> |<span data-ttu-id="d9a37-150">Задайте значение TRUE, если один или несколько получателей, **MAPI_BCC** получателей.</span><span class="sxs-lookup"><span data-stu-id="d9a37-150">Set to TRUE if one or more of the recipients are **MAPI_BCC** recipients.</span></span>  <br/> |
   
<span data-ttu-id="d9a37-151">В X.400 конверт P1 или доставки — это сведения, необходимые для доставки сообщений, включая свойства адрес получателя и любые флаги управления доставки и ответов.</span><span class="sxs-lookup"><span data-stu-id="d9a37-151">In X.400, the P1 or delivery envelope is the information needed to deliver a message, including the recipient's address properties and any option flags controlling delivery and replies.</span></span> <span data-ttu-id="d9a37-152">Конверт P2 или отображения, сведения, обычно отображается для каждого получателя, отличный от самого текста сообщения.</span><span class="sxs-lookup"><span data-stu-id="d9a37-152">The P2 or display envelope is the information usually displayed to each recipient other than the message text itself.</span></span> <span data-ttu-id="d9a37-153">Как правило, включает тему, важность, приоритет, уровень конфиденциальности сообщения и время отправки, а также основной и скопированной получателей.</span><span class="sxs-lookup"><span data-stu-id="d9a37-153">It typically includes the subject, importance, priority, sensitivity, and submission time, as well as the primary and copied recipient names.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="d9a37-154">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="d9a37-154">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="d9a37-155">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="d9a37-155">Protocol specifications</span></span>

<span data-ttu-id="d9a37-156">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="d9a37-156">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="d9a37-157">Содержит ссылки на связанные спецификаций протокола Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="d9a37-157">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="d9a37-158">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="d9a37-158">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="d9a37-159">Обрабатывает объекты сообщения и вложения.</span><span class="sxs-lookup"><span data-stu-id="d9a37-159">Handles message and attachment objects.</span></span>
    
<span data-ttu-id="d9a37-160">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="d9a37-160">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="d9a37-161">Задает свойства и операции, допустимые для объектов сообщения электронной почты.</span><span class="sxs-lookup"><span data-stu-id="d9a37-161">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
<span data-ttu-id="d9a37-162">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="d9a37-162">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="d9a37-163">Задает свойства и операции для встречи, приглашения на собрание и ответы.</span><span class="sxs-lookup"><span data-stu-id="d9a37-163">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="d9a37-164">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="d9a37-164">Header files</span></span>

<span data-ttu-id="d9a37-165">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="d9a37-165">Mapidefs.h</span></span>
  
> <span data-ttu-id="d9a37-166">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="d9a37-166">Provides data type definitions.</span></span>
    
<span data-ttu-id="d9a37-167">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="d9a37-167">Mapitags.h</span></span>
  
> <span data-ttu-id="d9a37-168">Содержит определения свойства в списке альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="d9a37-168">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="d9a37-169">См. также</span><span class="sxs-lookup"><span data-stu-id="d9a37-169">See also</span></span>



[<span data-ttu-id="d9a37-170">Каноническое свойство PidTagRecipientStatus</span><span class="sxs-lookup"><span data-stu-id="d9a37-170">PidTagRecipientStatus Canonical Property</span></span>](pidtagrecipientstatus-canonical-property.md)
  
[<span data-ttu-id="d9a37-171">Каноническое свойство PidTagDisplayTo</span><span class="sxs-lookup"><span data-stu-id="d9a37-171">PidTagDisplayTo Canonical Property</span></span>](pidtagdisplayto-canonical-property.md)
  
[<span data-ttu-id="d9a37-172">Каноническое свойство PidTagDisplayBcc</span><span class="sxs-lookup"><span data-stu-id="d9a37-172">PidTagDisplayBcc Canonical Property</span></span>](pidtagdisplaybcc-canonical-property.md)
  
[<span data-ttu-id="d9a37-173">Каноническое свойство PidTagDisplayCc</span><span class="sxs-lookup"><span data-stu-id="d9a37-173">PidTagDisplayCc Canonical Property</span></span>](pidtagdisplaycc-canonical-property.md)


[<span data-ttu-id="d9a37-174">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="d9a37-174">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="d9a37-175">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="d9a37-175">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="d9a37-176">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="d9a37-176">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="d9a37-177">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="d9a37-177">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

