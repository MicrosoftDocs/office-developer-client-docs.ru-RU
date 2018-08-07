---
title: Повторная отправка недоставленных сообщений
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 71768db3-a107-47c6-8e6b-775e8d40ac36
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 4fd0bf5a542e006ec743dbb7fe03d3331875c6d2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19812131"
---
# <a name="resending-an-undelivered-message"></a><span data-ttu-id="4e784-103">Повторная отправка недоставленных сообщений</span><span class="sxs-lookup"><span data-stu-id="4e784-103">Resending an undelivered message</span></span>
  
<span data-ttu-id="4e784-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="4e784-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="4e784-105">При успешной доставки сообщения, которое вы отправили, поставщика транспорта отправляет отчет о недоставке (NDR).</span><span class="sxs-lookup"><span data-stu-id="4e784-105">A transport provider sends a non-delivery report (NDR) when it cannot successfully deliver a message that you have submitted.</span></span> <span data-ttu-id="4e784-106">Это клиенту ли пользователи могут пытаться переслать этих недоставленных сообщений.</span><span class="sxs-lookup"><span data-stu-id="4e784-106">It is up to the client whether or not users can attempt to resend these undelivered messages.</span></span> <span data-ttu-id="4e784-107">Если вы поддерживаете повторная отправка сообщений, можно использовать форму, предоставленные MAPI или реализации собственного.</span><span class="sxs-lookup"><span data-stu-id="4e784-107">If you support resending messages, you can either use a form provided by MAPI or implement your own.</span></span> <span data-ttu-id="4e784-108">Отображает имена неудачных получателей и причину сбоя доставки, если это возможно формы MAPI и отображается кнопка, при выборе позволяет пользователям отправить сообщение.</span><span class="sxs-lookup"><span data-stu-id="4e784-108">The MAPI form displays the names of the failed recipients and the reason for the delivery failure, if possible, and includes a button that, when selected, allows a user to resend the message.</span></span>
  
<span data-ttu-id="4e784-109">При получении повторно отправленная сообщения, он должен выглядеть так же, как исходное сообщение.</span><span class="sxs-lookup"><span data-stu-id="4e784-109">When a resent message is received, it should look exactly like the original message.</span></span> <span data-ttu-id="4e784-110">Получатель не должны иметь возможности для различения сообщение, которое было доставлено на его первая попытка передачи или последующие попытки.</span><span class="sxs-lookup"><span data-stu-id="4e784-110">The recipient should be unable to differentiate between a message that was delivered on its first attempt at transmission or a subsequent attempt.</span></span> <span data-ttu-id="4e784-111">Ответы на это сообщение должны работать точно так же, как если сообщение успешно отправлено первый раз.</span><span class="sxs-lookup"><span data-stu-id="4e784-111">Replies on this message should work exactly as if the message had been sent successfully the first time.</span></span>
  
### <a name="to-resend-an-undelivered-message"></a><span data-ttu-id="4e784-112">Для повторной отправки недоставленных сообщений</span><span class="sxs-lookup"><span data-stu-id="4e784-112">To resend an undelivered message</span></span>
  
1. <span data-ttu-id="4e784-113">Вызов [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) для создания нового сообщения.</span><span class="sxs-lookup"><span data-stu-id="4e784-113">Call [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) to create a new message.</span></span> 
    
2. <span data-ttu-id="4e784-114">Скопируйте все свойства из исходного сообщения, за исключением ** PR_MESSAGE_RECIPIENTS ** свойства **PR_SENDER** и **PR_SENT_REPRESENTING** и свойство ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="4e784-114">Copy all of the properties from the original message, excluding the ** PR_MESSAGE_RECIPIENTS ** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md)) property, and the **PR_SENDER** and **PR_SENT_REPRESENTING** properties.</span></span> <span data-ttu-id="4e784-115">Внесите следующие изменения свойств:</span><span class="sxs-lookup"><span data-stu-id="4e784-115">Make the following property modifications:</span></span> 
    
   - <span data-ttu-id="4e784-116">Установка **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)) к отчету ** PR_ORIG_MESSAGE_CLASS ** свойство ([PidTagOriginalMessageClass](pidtagoriginalmessageclass-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="4e784-116">Set **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)) to the report's **PR_ORIG_MESSAGE_CLASS ** ([PidTagOriginalMessageClass](pidtagoriginalmessageclass-canonical-property.md)) property.</span></span>
    
   - <span data-ttu-id="4e784-117">Установите флаг MSGFLAG_RESEND в свойстве **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="4e784-117">Set the MSGFLAG_RESEND flag in the **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) property.</span></span>
    
   - <span data-ttu-id="4e784-118">Значение свойства **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) исходное сообщение **PR_ORIGINAL_ENTRYID** ([PidTagOriginalEntryId](pidtagoriginalentryid-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="4e784-118">Set **PR_ORIGINAL_ENTRYID** ([PidTagOriginalEntryId](pidtagoriginalentryid-canonical-property.md)) to the original message's **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) property.</span></span>
    
   - <span data-ttu-id="4e784-119">Для каждого получателя задайте MAPI_SUBMITTED в свойстве **PR_RECIPIENT_TYPE** ([PidTagRecipientType](pidtagrecipienttype-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="4e784-119">For each recipient, set MAPI_SUBMITTED in the **PR_RECIPIENT_TYPE** ([PidTagRecipientType](pidtagrecipienttype-canonical-property.md)) property.</span></span> 
    
   - <span data-ttu-id="4e784-120">Дублирующиеся каждого получателя, сбоя.</span><span class="sxs-lookup"><span data-stu-id="4e784-120">Duplicate each failed recipient.</span></span> <span data-ttu-id="4e784-121">Измените свойство **PR_RECIPIENT_TYPE** для повторяющихся получателя на MAPI_P1.</span><span class="sxs-lookup"><span data-stu-id="4e784-121">Change the **PR_RECIPIENT_TYPE** property for the duplicated recipient to MAPI_P1.</span></span> <span data-ttu-id="4e784-122">Таким образом, для каждого получателя, неудачных имеется теперь две записи в таблице получателей: одно с **PR_RECIPIENT_TYPE** значение исходное значение а другое с **PR_RECIPIENT_TYPE** MAPI_P1.</span><span class="sxs-lookup"><span data-stu-id="4e784-122">Therefore, for each failed recipient there are now two entries in the recipient table: one with **PR_RECIPIENT_TYPE** set to its original value and the other with **PR_RECIPIENT_TYPE** set to MAPI_P1.</span></span> 
    
3. <span data-ttu-id="4e784-123">Вызов [ScCreateConversationIndex](sccreateconversationindex.md) для настройки отслеживания при желании беседы.</span><span class="sxs-lookup"><span data-stu-id="4e784-123">Call [ScCreateConversationIndex](sccreateconversationindex.md) to set up conversation tracking if desired.</span></span> 
    
4. <span data-ttu-id="4e784-124">Вызов метода [IMessage::ModifyRecipients](imessage-modifyrecipients.md) новое сообщение для обновления списка получателей.</span><span class="sxs-lookup"><span data-stu-id="4e784-124">Call the new message's [IMessage::ModifyRecipients](imessage-modifyrecipients.md) method to update the recipient list.</span></span> 
    
5. <span data-ttu-id="4e784-125">Вызовите [IMessage::SubmitMessage](imessage-submitmessage.md) , чтобы сохранить и отправить новое сообщение.</span><span class="sxs-lookup"><span data-stu-id="4e784-125">Call [IMessage::SubmitMessage](imessage-submitmessage.md) to save and send the new message.</span></span> 
    

