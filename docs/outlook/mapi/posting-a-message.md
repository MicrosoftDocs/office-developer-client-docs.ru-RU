---
title: Отправка сообщения
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: cc3e1546-e58b-413f-82d7-4efeb86b0000
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 33bf6780979ee25739abf93d89744e1517363c63
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19812069"
---
# <a name="posting-a-message"></a><span data-ttu-id="38c0d-103">Отправка сообщения</span><span class="sxs-lookup"><span data-stu-id="38c0d-103">Posting a message</span></span>

<span data-ttu-id="38c0d-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="38c0d-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="38c0d-105">Учет сообщение аналогичен отправки сообщения.</span><span class="sxs-lookup"><span data-stu-id="38c0d-105">Posting a message is similar to sending a message.</span></span> <span data-ttu-id="38c0d-106">Основное различие — конечным файлом.</span><span class="sxs-lookup"><span data-stu-id="38c0d-106">The main difference is the destination.</span></span> <span data-ttu-id="38c0d-107">Вместо проходить для одного или нескольких получателей через один или несколько систем обмена сообщениями, отправленное сообщение остается в папке в хранилище текущего сообщения.</span><span class="sxs-lookup"><span data-stu-id="38c0d-107">Rather than being directed to one or more recipients across one or more messaging systems, a posted message remains in a folder in the current message store.</span></span>
  
### <a name="to-post-a-message"></a><span data-ttu-id="38c0d-108">Чтобы отправить сообщение</span><span class="sxs-lookup"><span data-stu-id="38c0d-108">To post a message</span></span>
  
1. <span data-ttu-id="38c0d-109">Откройте папку назначения путем вызова [IMsgStore::OpenEntry](imsgstore-openentry.md).</span><span class="sxs-lookup"><span data-stu-id="38c0d-109">Open the destination folder by calling [IMsgStore::OpenEntry](imsgstore-openentry.md).</span></span> <span data-ttu-id="38c0d-110">Если конечной папки "Входящие", найдите идентификатор записи для передачи **OpenEntry** путем вызова [IMsgStore::GetReceiveFolder](imsgstore-getreceivefolder.md).</span><span class="sxs-lookup"><span data-stu-id="38c0d-110">If the destination folder is the Inbox, locate the entry identifier to pass to **OpenEntry** by calling [IMsgStore::GetReceiveFolder](imsgstore-getreceivefolder.md).</span></span> 
    
2. <span data-ttu-id="38c0d-111">Вызов [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) для создания сообщения.</span><span class="sxs-lookup"><span data-stu-id="38c0d-111">Call [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) to create the message.</span></span> 
    
3. <span data-ttu-id="38c0d-112">Вызовите метод [IMAPIProp::SetProps](imapiprop-setprops.md) сообщение для установки:</span><span class="sxs-lookup"><span data-stu-id="38c0d-112">Call the message's [IMAPIProp::SetProps](imapiprop-setprops.md) method to set:</span></span> 
    
   - <span data-ttu-id="38c0d-113">Флаг MSGFLAG_READ в свойстве **PidTagMessageFlags** ( [PR_MESSAGE_FLAGS](pidtagmessageflags-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="38c0d-113">The MSGFLAG_READ flag in the **PidTagMessageFlags** ( [PR_MESSAGE_FLAGS](pidtagmessageflags-canonical-property.md)) property.</span></span>
    
   - <span data-ttu-id="38c0d-114">Свойства **PR_SENDER** .</span><span class="sxs-lookup"><span data-stu-id="38c0d-114">The **PR_SENDER** properties.</span></span> 
    
   - <span data-ttu-id="38c0d-115">Свойства **PR_SENT_REPRESENTING** .</span><span class="sxs-lookup"><span data-stu-id="38c0d-115">The **PR_SENT_REPRESENTING** properties.</span></span> 
    
   - <span data-ttu-id="38c0d-116">Свойство **PR_RECEIPT_TIME** ([PidTagReceiptTime](pidtagreceipttime-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="38c0d-116">The **PR_RECEIPT_TIME** ([PidTagReceiptTime](pidtagreceipttime-canonical-property.md)) property.</span></span>
    
   - <span data-ttu-id="38c0d-117">**PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) или свойство **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="38c0d-117">The **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) or **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) property.</span></span>
    
   - <span data-ttu-id="38c0d-118">Свойство **PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="38c0d-118">The **PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md)) property.</span></span>
    
   - <span data-ttu-id="38c0d-119">Свойство **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="38c0d-119">The **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)) property.</span></span>
    
   - <span data-ttu-id="38c0d-120">Любые свойства, необходимые для класса сообщения.</span><span class="sxs-lookup"><span data-stu-id="38c0d-120">Any properties required by the message class.</span></span>
    
4. <span data-ttu-id="38c0d-121">Вызовите метод [IMAPIProp::SaveChanges](imapiprop-savechanges.md) сообщения, чтобы сохранить сообщение.</span><span class="sxs-lookup"><span data-stu-id="38c0d-121">Call the message's [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method to save the message.</span></span> 
    
5. <span data-ttu-id="38c0d-122">При необходимости создайте вложения, задайте его свойства и сохраните его.</span><span class="sxs-lookup"><span data-stu-id="38c0d-122">If necessary, create an attachment, set its properties, and save it.</span></span> <span data-ttu-id="38c0d-123">Дополнительные сведения о добавлении вложений в сообщения [Вложения сообщения](creating-a-message-attachment.md)см.</span><span class="sxs-lookup"><span data-stu-id="38c0d-123">For more information about adding attachments to messages, see [Creating a Message Attachment](creating-a-message-attachment.md).</span></span>
    
6. <span data-ttu-id="38c0d-124">Вызовите **IMessage::SaveChanges** , чтобы сохранить сообщение.</span><span class="sxs-lookup"><span data-stu-id="38c0d-124">Call **IMessage::SaveChanges** to save the message.</span></span> <span data-ttu-id="38c0d-125">На этом этапе оно будет отображаться в таблице содержимое папки назначения.</span><span class="sxs-lookup"><span data-stu-id="38c0d-125">At this point it will appear in the contents table of the destination folder.</span></span> 
    
<span data-ttu-id="38c0d-126">Обратите внимание на то, что не создает список получателей.</span><span class="sxs-lookup"><span data-stu-id="38c0d-126">Notice that you do not create a recipient list.</span></span> <span data-ttu-id="38c0d-127">Вместо этого можно задать несколько свойств, которые обычно задаются с помощью поставщика транспорта для отправки сообщения.</span><span class="sxs-lookup"><span data-stu-id="38c0d-127">Instead, you set several properties that are normally set by a transport provider for a sent message.</span></span> 
  
<span data-ttu-id="38c0d-128">Если вы хотите сохранить периодически перед его отображаются в таблице содержимое папки, отображается сообщение, создайте вместо этого в скрытой папке, например в корневую папку поддерева IPM и затем перетащить его в целевой папке.</span><span class="sxs-lookup"><span data-stu-id="38c0d-128">If you want to save a message intermittently before having it appear in the contents table of the visible folder, create it instead in a hidden folder such as the root folder of the IPM subtree and then move it to the target folder.</span></span> 
  

