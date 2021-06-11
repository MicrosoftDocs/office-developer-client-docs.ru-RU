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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33432669"
---
# <a name="resending-an-undelivered-message"></a><span data-ttu-id="8ea43-103">Повторная отправка недоставленного сообщения</span><span class="sxs-lookup"><span data-stu-id="8ea43-103">Resending an undelivered message</span></span>
  
<span data-ttu-id="8ea43-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8ea43-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8ea43-105">Поставщик транспорта отправляет отчет о невывозе (NDR), если он не может успешно доставить отправленное сообщение.</span><span class="sxs-lookup"><span data-stu-id="8ea43-105">A transport provider sends a non-delivery report (NDR) when it cannot successfully deliver a message that you have submitted.</span></span> <span data-ttu-id="8ea43-106">Клиент должен определить, могут ли пользователи пытаться повторно отправлять эти неизданные сообщения.</span><span class="sxs-lookup"><span data-stu-id="8ea43-106">It is up to the client whether or not users can attempt to resend these undelivered messages.</span></span> <span data-ttu-id="8ea43-107">Если вы поддерживаете повторное сообщение, вы можете использовать форму, предоставленную MAPI, или реализовать свою собственную.</span><span class="sxs-lookup"><span data-stu-id="8ea43-107">If you support resending messages, you can either use a form provided by MAPI or implement your own.</span></span> <span data-ttu-id="8ea43-108">В форме MAPI отображаются имена сбоя получателей и причина сбоя доставки, если это возможно, и включает кнопку, которая при выборе позволяет пользователю повторно отправлять сообщение.</span><span class="sxs-lookup"><span data-stu-id="8ea43-108">The MAPI form displays the names of the failed recipients and the reason for the delivery failure, if possible, and includes a button that, when selected, allows a user to resend the message.</span></span>
  
<span data-ttu-id="8ea43-109">При получении обиленного сообщения оно должно выглядеть точно так же, как исходное.</span><span class="sxs-lookup"><span data-stu-id="8ea43-109">When a resent message is received, it should look exactly like the original message.</span></span> <span data-ttu-id="8ea43-110">Получатель должен быть не в состоянии различать сообщение, доставленное с первой попытки передачи, или последующая попытка.</span><span class="sxs-lookup"><span data-stu-id="8ea43-110">The recipient should be unable to differentiate between a message that was delivered on its first attempt at transmission or a subsequent attempt.</span></span> <span data-ttu-id="8ea43-111">Ответы на это сообщение должны работать так же, как если бы сообщение было отправлено успешно в первый раз.</span><span class="sxs-lookup"><span data-stu-id="8ea43-111">Replies on this message should work exactly as if the message had been sent successfully the first time.</span></span>
  
### <a name="to-resend-an-undelivered-message"></a><span data-ttu-id="8ea43-112">Повторное повторное сообщение, не отображенное</span><span class="sxs-lookup"><span data-stu-id="8ea43-112">To resend an undelivered message</span></span>
  
1. <span data-ttu-id="8ea43-113">Вызов [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) для создания нового сообщения.</span><span class="sxs-lookup"><span data-stu-id="8ea43-113">Call [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) to create a new message.</span></span> 
    
2. <span data-ttu-id="8ea43-114">Скопируйте все свойства из исходного сообщения, за исключением свойства \*\* PR_MESSAGE_RECIPIENTS \*\*[(PidTagMessageRecipients),](pidtagmessagerecipients-canonical-property.md)а также свойств PR_SENDER **и PR_SENT_REPRESENTING.** </span><span class="sxs-lookup"><span data-stu-id="8ea43-114">Copy all of the properties from the original message, excluding the \*\* PR_MESSAGE_RECIPIENTS \*\* ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md)) property, and the **PR_SENDER** and **PR_SENT_REPRESENTING** properties.</span></span> <span data-ttu-id="8ea43-115">Внести следующие изменения свойств:</span><span class="sxs-lookup"><span data-stu-id="8ea43-115">Make the following property modifications:</span></span> 
    
   - <span data-ttu-id="8ea43-116">Установите **PR_MESSAGE_CLASS** [(PidTagMessageClass)](pidtagmessageclass-canonical-property.md)для свойства \*\*PR_ORIG_MESSAGE_CLASS \*\*[(PidTagOriginalMessageClass).](pidtagoriginalmessageclass-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="8ea43-116">Set **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)) to the report's \*\*PR_ORIG_MESSAGE_CLASS \*\* ([PidTagOriginalMessageClass](pidtagoriginalmessageclass-canonical-property.md)) property.</span></span>
    
   - <span data-ttu-id="8ea43-117">Установите флаг MSGFLAG_RESEND в **свойстве PR_MESSAGE_FLAGS** [(PidTagMessageFlags).](pidtagmessageflags-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="8ea43-117">Set the MSGFLAG_RESEND flag in the **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) property.</span></span>
    
   - <span data-ttu-id="8ea43-118">Установите **PR_ORIGINAL_ENTRYID** [(PidTagOriginalEntryId)](pidtagoriginalentryid-canonical-property.md)для свойства PR_ENTRYID  [(PidTagEntryId).](pidtagentryid-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="8ea43-118">Set **PR_ORIGINAL_ENTRYID** ([PidTagOriginalEntryId](pidtagoriginalentryid-canonical-property.md)) to the original message's **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) property.</span></span>
    
   - <span data-ttu-id="8ea43-119">Для каждого получателя установите MAPI_SUBMITTED в **свойстве PR_RECIPIENT_TYPE** [(PidTagRecipientType).](pidtagrecipienttype-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="8ea43-119">For each recipient, set MAPI_SUBMITTED in the **PR_RECIPIENT_TYPE** ([PidTagRecipientType](pidtagrecipienttype-canonical-property.md)) property.</span></span> 
    
   - <span data-ttu-id="8ea43-120">Дублировать каждого сбойного получателя.</span><span class="sxs-lookup"><span data-stu-id="8ea43-120">Duplicate each failed recipient.</span></span> <span data-ttu-id="8ea43-121">Измените **свойство PR_RECIPIENT_TYPE** для дубликатного получателя на MAPI_P1.</span><span class="sxs-lookup"><span data-stu-id="8ea43-121">Change the **PR_RECIPIENT_TYPE** property for the duplicated recipient to MAPI_P1.</span></span> <span data-ttu-id="8ea43-122">Поэтому для каждого неудатного получателя в таблице получателей  теперь есть две записи: одна  с PR_RECIPIENT_TYPE установлена к исходному значению, а другая с PR_RECIPIENT_TYPE для MAPI_P1.</span><span class="sxs-lookup"><span data-stu-id="8ea43-122">Therefore, for each failed recipient there are now two entries in the recipient table: one with **PR_RECIPIENT_TYPE** set to its original value and the other with **PR_RECIPIENT_TYPE** set to MAPI_P1.</span></span> 
    
3. <span data-ttu-id="8ea43-123">Вызов [ScCreateConversationIndex,](sccreateconversationindex.md) чтобы при желании настроить отслеживание разговоров.</span><span class="sxs-lookup"><span data-stu-id="8ea43-123">Call [ScCreateConversationIndex](sccreateconversationindex.md) to set up conversation tracking if desired.</span></span> 
    
4. <span data-ttu-id="8ea43-124">Чтобы обновить список получателей, позвоните по методу [IMessage::ModifyRecipients](imessage-modifyrecipients.md) нового сообщения.</span><span class="sxs-lookup"><span data-stu-id="8ea43-124">Call the new message's [IMessage::ModifyRecipients](imessage-modifyrecipients.md) method to update the recipient list.</span></span> 
    
5. <span data-ttu-id="8ea43-125">Вызов [IMessage::SubmitMessage](imessage-submitmessage.md) для сохранения и отправки нового сообщения.</span><span class="sxs-lookup"><span data-stu-id="8ea43-125">Call [IMessage::SubmitMessage](imessage-submitmessage.md) to save and send the new message.</span></span> 
    

