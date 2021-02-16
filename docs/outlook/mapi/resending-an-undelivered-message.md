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
# <a name="resending-an-undelivered-message"></a><span data-ttu-id="5b45b-103">Повторная отправка недоставленного сообщения</span><span class="sxs-lookup"><span data-stu-id="5b45b-103">Resending an undelivered message</span></span>
  
<span data-ttu-id="5b45b-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5b45b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5b45b-105">Если поставщик транспорта не удается доставить отправленное сообщение, поставщик транспорта отправляет отчет о невыдаваемой доставке.</span><span class="sxs-lookup"><span data-stu-id="5b45b-105">A transport provider sends a non-delivery report (NDR) when it cannot successfully deliver a message that you have submitted.</span></span> <span data-ttu-id="5b45b-106">Клиент может ли пользователи пытаться повторно отправить эти недосвеченные сообщения.</span><span class="sxs-lookup"><span data-stu-id="5b45b-106">It is up to the client whether or not users can attempt to resend these undelivered messages.</span></span> <span data-ttu-id="5b45b-107">Если вы поддерживаете повторное отправлять сообщения, вы можете использовать форму, предоставленную MAPI, или реализовать собственную.</span><span class="sxs-lookup"><span data-stu-id="5b45b-107">If you support resending messages, you can either use a form provided by MAPI or implement your own.</span></span> <span data-ttu-id="5b45b-108">В форме MAPI отображаются имена неудачных получателей и причина сбоя доставки, если это возможно, а также кнопка, которая при выборе позволяет пользователю повторно отправить сообщение.</span><span class="sxs-lookup"><span data-stu-id="5b45b-108">The MAPI form displays the names of the failed recipients and the reason for the delivery failure, if possible, and includes a button that, when selected, allows a user to resend the message.</span></span>
  
<span data-ttu-id="5b45b-109">При получении повторного сообщения оно должно выглядеть точно так же, как исходное сообщение.</span><span class="sxs-lookup"><span data-stu-id="5b45b-109">When a resent message is received, it should look exactly like the original message.</span></span> <span data-ttu-id="5b45b-110">Получатель не должен различать сообщение, доставленное при первой попытке передачи, или последующие попытки.</span><span class="sxs-lookup"><span data-stu-id="5b45b-110">The recipient should be unable to differentiate between a message that was delivered on its first attempt at transmission or a subsequent attempt.</span></span> <span data-ttu-id="5b45b-111">Ответы на это сообщение должны работать точно так же, как если бы сообщение было успешно отправлено в первый раз.</span><span class="sxs-lookup"><span data-stu-id="5b45b-111">Replies on this message should work exactly as if the message had been sent successfully the first time.</span></span>
  
### <a name="to-resend-an-undelivered-message"></a><span data-ttu-id="5b45b-112">Чтобы повторно отправить недосвеченное сообщение</span><span class="sxs-lookup"><span data-stu-id="5b45b-112">To resend an undelivered message</span></span>
  
1. <span data-ttu-id="5b45b-113">Вызов [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) для создания нового сообщения.</span><span class="sxs-lookup"><span data-stu-id="5b45b-113">Call [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) to create a new message.</span></span> 
    
2. <span data-ttu-id="5b45b-114">Скопируйте все свойства из исходного сообщения, за исключением свойства \*\* PR_MESSAGE_RECIPIENTS \*\* ([PidTagMessageRecipients),](pidtagmessagerecipients-canonical-property.md)а также свойств PR_SENDER и **PR_SENT_REPRESENTING.** </span><span class="sxs-lookup"><span data-stu-id="5b45b-114">Copy all of the properties from the original message, excluding the \*\* PR_MESSAGE_RECIPIENTS \*\* ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md)) property, and the **PR_SENDER** and **PR_SENT_REPRESENTING** properties.</span></span> <span data-ttu-id="5b45b-115">Внести следующие изменения в свойства:</span><span class="sxs-lookup"><span data-stu-id="5b45b-115">Make the following property modifications:</span></span> 
    
   - <span data-ttu-id="5b45b-116">Установите **PR_MESSAGE_CLASS** ([PidTagMessageClass)](pidtagmessageclass-canonical-property.md)для свойства \*\*PR_ORIG_MESSAGE_CLASS \*\* отчета ([PidTagOriginalMessageClass).](pidtagoriginalmessageclass-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="5b45b-116">Set **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)) to the report's \*\*PR_ORIG_MESSAGE_CLASS \*\* ([PidTagOriginalMessageClass](pidtagoriginalmessageclass-canonical-property.md)) property.</span></span>
    
   - <span data-ttu-id="5b45b-117">Установите флаг MSGFLAG_RESEND в **свойстве PR_MESSAGE_FLAGS** ([PidTagMessageFlags).](pidtagmessageflags-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="5b45b-117">Set the MSGFLAG_RESEND flag in the **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) property.</span></span>
    
   - <span data-ttu-id="5b45b-118">Установите **PR_ORIGINAL_ENTRYID** ([PidTagOriginalEntryId)](pidtagoriginalentryid-canonical-property.md)свойству PR_ENTRYID **исходного** сообщения ([PidTagEntryId).](pidtagentryid-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="5b45b-118">Set **PR_ORIGINAL_ENTRYID** ([PidTagOriginalEntryId](pidtagoriginalentryid-canonical-property.md)) to the original message's **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) property.</span></span>
    
   - <span data-ttu-id="5b45b-119">Для каждого получателя MAPI_SUBMITTED в **свойстве PR_RECIPIENT_TYPE** ([PidTagRecipientType).](pidtagrecipienttype-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="5b45b-119">For each recipient, set MAPI_SUBMITTED in the **PR_RECIPIENT_TYPE** ([PidTagRecipientType](pidtagrecipienttype-canonical-property.md)) property.</span></span> 
    
   - <span data-ttu-id="5b45b-120">Дублируйте каждого сбойного получателя.</span><span class="sxs-lookup"><span data-stu-id="5b45b-120">Duplicate each failed recipient.</span></span> <span data-ttu-id="5b45b-121">Измените **PR_RECIPIENT_TYPE** для дубликата получателя на MAPI_P1.</span><span class="sxs-lookup"><span data-stu-id="5b45b-121">Change the **PR_RECIPIENT_TYPE** property for the duplicated recipient to MAPI_P1.</span></span> <span data-ttu-id="5b45b-122">Таким образом, для каждого получателя сбой теперь есть две записи в таблице получателей: одна  с **PR_RECIPIENT_TYPE** имеет исходное значение, а другая PR_RECIPIENT_TYPE имеет значение MAPI_P1.</span><span class="sxs-lookup"><span data-stu-id="5b45b-122">Therefore, for each failed recipient there are now two entries in the recipient table: one with **PR_RECIPIENT_TYPE** set to its original value and the other with **PR_RECIPIENT_TYPE** set to MAPI_P1.</span></span> 
    
3. <span data-ttu-id="5b45b-123">Вызовите [ScCreateConversationIndex,](sccreateconversationindex.md) чтобы при желании настроить отслеживание бесед.</span><span class="sxs-lookup"><span data-stu-id="5b45b-123">Call [ScCreateConversationIndex](sccreateconversationindex.md) to set up conversation tracking if desired.</span></span> 
    
4. <span data-ttu-id="5b45b-124">Вызовите метод [IMessage::ModifyRecipients](imessage-modifyrecipients.md) нового сообщения, чтобы обновить список получателей.</span><span class="sxs-lookup"><span data-stu-id="5b45b-124">Call the new message's [IMessage::ModifyRecipients](imessage-modifyrecipients.md) method to update the recipient list.</span></span> 
    
5. <span data-ttu-id="5b45b-125">Вызовите [IMessage::SubmitMessage,](imessage-submitmessage.md) чтобы сохранить и отправить новое сообщение.</span><span class="sxs-lookup"><span data-stu-id="5b45b-125">Call [IMessage::SubmitMessage](imessage-submitmessage.md) to save and send the new message.</span></span> 
    

