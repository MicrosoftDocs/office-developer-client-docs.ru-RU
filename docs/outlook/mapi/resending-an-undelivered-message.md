---
title: Повторная отправка недоставленного сообщения
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 71768db3-a107-47c6-8e6b-775e8d40ac36
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: ddd0c1419531b0822bb98df51f47e12e63dcf242
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328681"
---
# <a name="resending-an-undelivered-message"></a><span data-ttu-id="81c67-103">Повторная отправка недоставленного сообщения</span><span class="sxs-lookup"><span data-stu-id="81c67-103">Resending an undelivered message</span></span>
  
<span data-ttu-id="81c67-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="81c67-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="81c67-105">Поставщик транспорта отправляет отчет о недоставке, когда он не может успешно доставить отправленное вами сообщение.</span><span class="sxs-lookup"><span data-stu-id="81c67-105">A transport provider sends a non-delivery report (NDR) when it cannot successfully deliver a message that you have submitted.</span></span> <span data-ttu-id="81c67-106">Клиенты могут попытаться повторно отправить эти недоставленные сообщения.</span><span class="sxs-lookup"><span data-stu-id="81c67-106">It is up to the client whether or not users can attempt to resend these undelivered messages.</span></span> <span data-ttu-id="81c67-107">Если вы поддерживаете повторную отправку сообщений, вы можете использовать форму, предоставляемую MAPI, или внедрить собственные сообщения.</span><span class="sxs-lookup"><span data-stu-id="81c67-107">If you support resending messages, you can either use a form provided by MAPI or implement your own.</span></span> <span data-ttu-id="81c67-108">Форма MAPI отображает имена неудачных получателей и причину сбоя доставки, если это возможно, и включает кнопку, которая при выборе позволяет пользователю повторно отправить сообщение.</span><span class="sxs-lookup"><span data-stu-id="81c67-108">The MAPI form displays the names of the failed recipients and the reason for the delivery failure, if possible, and includes a button that, when selected, allows a user to resend the message.</span></span>
  
<span data-ttu-id="81c67-109">При получении отправленного сообщения оно должно выглядеть точно так же, как исходное сообщение.</span><span class="sxs-lookup"><span data-stu-id="81c67-109">When a resent message is received, it should look exactly like the original message.</span></span> <span data-ttu-id="81c67-110">Получатель не должен отличать сообщение, которое было доставлено при первой попытке передачи, или последующей попытке.</span><span class="sxs-lookup"><span data-stu-id="81c67-110">The recipient should be unable to differentiate between a message that was delivered on its first attempt at transmission or a subsequent attempt.</span></span> <span data-ttu-id="81c67-111">Ответы на это сообщение должны работать точно так же, как если бы сообщение было успешно отправлено в первый раз.</span><span class="sxs-lookup"><span data-stu-id="81c67-111">Replies on this message should work exactly as if the message had been sent successfully the first time.</span></span>
  
### <a name="to-resend-an-undelivered-message"></a><span data-ttu-id="81c67-112">Повторная отправка недоставленного сообщения</span><span class="sxs-lookup"><span data-stu-id="81c67-112">To resend an undelivered message</span></span>
  
1. <span data-ttu-id="81c67-113">Call [IMAPIFolder:: CreateMessage](imapifolder-createmessage.md) для создания нового сообщения.</span><span class="sxs-lookup"><span data-stu-id="81c67-113">Call [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) to create a new message.</span></span> 
    
2. <span data-ttu-id="81c67-114">Скопируйте все свойства из исходного сообщения, исключая свойство \* \* ПР_МЕССАЖЕ_РЕЦИПИЕНТС \* \* ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md)), и свойства **пр_сендер** и **пр_сент_репресентинг** .</span><span class="sxs-lookup"><span data-stu-id="81c67-114">Copy all of the properties from the original message, excluding the \*\* PR_MESSAGE_RECIPIENTS \*\* ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md)) property, and the **PR_SENDER** and **PR_SENT_REPRESENTING** properties.</span></span> <span data-ttu-id="81c67-115">Внесите следующие изменения свойств:</span><span class="sxs-lookup"><span data-stu-id="81c67-115">Make the following property modifications:</span></span> 
    
   - <span data-ttu-id="81c67-116">Задайте для **пр_мессаже_класс** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)) свойство отчета \* \* Пр_ориг_мессаже_класс \* \* ([PidTagOriginalMessageClass](pidtagoriginalmessageclass-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="81c67-116">Set **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)) to the report's \*\*PR_ORIG_MESSAGE_CLASS \*\* ([PidTagOriginalMessageClass](pidtagoriginalmessageclass-canonical-property.md)) property.</span></span>
    
   - <span data-ttu-id="81c67-117">Установите флаг МСГФЛАГ_РЕСЕНД в свойстве \*\*пр_мессаже_флагс\*\* ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="81c67-117">Set the MSGFLAG_RESEND flag in the **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) property.</span></span>
    
   - <span data-ttu-id="81c67-118">Задайте **пр_оригинал_ентрид** ([PidTagOriginalEntryId](pidtagoriginalentryid-canonical-property.md)) в качестве значения свойства **пр_ентрид** исходного сообщения ([PidTagEntryId](pidtagentryid-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="81c67-118">Set **PR_ORIGINAL_ENTRYID** ([PidTagOriginalEntryId](pidtagoriginalentryid-canonical-property.md)) to the original message's **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) property.</span></span>
    
   - <span data-ttu-id="81c67-119">Для каждого получателя установите МАПИ_СУБМИТТЕД в свойстве \*\*пр_реЦипиент_типе\*\* ([PidTagRecipientType](pidtagrecipienttype-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="81c67-119">For each recipient, set MAPI_SUBMITTED in the **PR_RECIPIENT_TYPE** ([PidTagRecipientType](pidtagrecipienttype-canonical-property.md)) property.</span></span> 
    
   - <span data-ttu-id="81c67-120">Дублировать каждого неудачного получателя.</span><span class="sxs-lookup"><span data-stu-id="81c67-120">Duplicate each failed recipient.</span></span> <span data-ttu-id="81c67-121">Измените свойство **пр_реЦипиент_типе** для повторяющегося получателя на MAPI_P1.</span><span class="sxs-lookup"><span data-stu-id="81c67-121">Change the **PR_RECIPIENT_TYPE** property for the duplicated recipient to MAPI_P1.</span></span> <span data-ttu-id="81c67-122">Таким образом, для каждого неудачного получателя в таблице получателей теперь имеется две записи: одна с **пр_реЦипиент_типе** имеет исходное значение, а другая с **пр_реЦипиент_типе** значением MAPI_P1.</span><span class="sxs-lookup"><span data-stu-id="81c67-122">Therefore, for each failed recipient there are now two entries in the recipient table: one with **PR_RECIPIENT_TYPE** set to its original value and the other with **PR_RECIPIENT_TYPE** set to MAPI_P1.</span></span> 
    
3. <span data-ttu-id="81c67-123">ВыЗовите [сккреатеконверсатиониндекс](sccreateconversationindex.md) , чтобы настроить отслеживание бесед, если это необходимо.</span><span class="sxs-lookup"><span data-stu-id="81c67-123">Call [ScCreateConversationIndex](sccreateconversationindex.md) to set up conversation tracking if desired.</span></span> 
    
4. <span data-ttu-id="81c67-124">ВыЗовите метод [iMessage:: модифиреЦипиентс](imessage-modifyrecipients.md) нового сообщения, чтобы обновить список получателей.</span><span class="sxs-lookup"><span data-stu-id="81c67-124">Call the new message's [IMessage::ModifyRecipients](imessage-modifyrecipients.md) method to update the recipient list.</span></span> 
    
5. <span data-ttu-id="81c67-125">Call [iMessage:: субмитмессаже](imessage-submitmessage.md) , чтобы сохранить и отправить новое сообщение.</span><span class="sxs-lookup"><span data-stu-id="81c67-125">Call [IMessage::SubmitMessage](imessage-submitmessage.md) to save and send the new message.</span></span> 
    

