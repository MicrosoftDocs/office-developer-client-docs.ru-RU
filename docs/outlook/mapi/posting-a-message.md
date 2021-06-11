---
title: Публикация сообщения
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: cc3e1546-e58b-413f-82d7-4efeb86b0000
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 2c174d48a19e23de725e1d5a1533130175f2ab00
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33429770"
---
# <a name="posting-a-message"></a><span data-ttu-id="f23c6-103">Публикация сообщения</span><span class="sxs-lookup"><span data-stu-id="f23c6-103">Posting a message</span></span>

<span data-ttu-id="f23c6-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f23c6-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f23c6-105">Публикация сообщения похожа на отправку сообщения.</span><span class="sxs-lookup"><span data-stu-id="f23c6-105">Posting a message is similar to sending a message.</span></span> <span data-ttu-id="f23c6-106">Основное отличие — назначение.</span><span class="sxs-lookup"><span data-stu-id="f23c6-106">The main difference is the destination.</span></span> <span data-ttu-id="f23c6-107">Вместо того, чтобы отправляться одному или более получателям через одну или несколько систем обмена сообщениями, размещенное сообщение остается в папке в текущем хранилище сообщений.</span><span class="sxs-lookup"><span data-stu-id="f23c6-107">Rather than being directed to one or more recipients across one or more messaging systems, a posted message remains in a folder in the current message store.</span></span>
  
### <a name="to-post-a-message"></a><span data-ttu-id="f23c6-108">Публикация сообщения</span><span class="sxs-lookup"><span data-stu-id="f23c6-108">To post a message</span></span>
  
1. <span data-ttu-id="f23c6-109">Откройте папку назначения, позвонив [в IMsgStore::OpenEntry.](imsgstore-openentry.md)</span><span class="sxs-lookup"><span data-stu-id="f23c6-109">Open the destination folder by calling [IMsgStore::OpenEntry](imsgstore-openentry.md).</span></span> <span data-ttu-id="f23c6-110">Если папка назначения — папка "Входящие", найдите идентификатор записи для передачи **в OpenEntry,** позвонив [в IMsgStore::GetReceiveFolder](imsgstore-getreceivefolder.md).</span><span class="sxs-lookup"><span data-stu-id="f23c6-110">If the destination folder is the Inbox, locate the entry identifier to pass to **OpenEntry** by calling [IMsgStore::GetReceiveFolder](imsgstore-getreceivefolder.md).</span></span> 
    
2. <span data-ttu-id="f23c6-111">Вызов [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) для создания сообщения.</span><span class="sxs-lookup"><span data-stu-id="f23c6-111">Call [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) to create the message.</span></span> 
    
3. <span data-ttu-id="f23c6-112">Вызовите метод [IMAPIProp::SetProps,](imapiprop-setprops.md) чтобы установить:</span><span class="sxs-lookup"><span data-stu-id="f23c6-112">Call the message's [IMAPIProp::SetProps](imapiprop-setprops.md) method to set:</span></span> 
    
   - <span data-ttu-id="f23c6-113">Флаг MSGFLAG_READ в **свойстве PidTagMessageFlags** [(PR_MESSAGE_FLAGS).](pidtagmessageflags-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="f23c6-113">The MSGFLAG_READ flag in the **PidTagMessageFlags** ( [PR_MESSAGE_FLAGS](pidtagmessageflags-canonical-property.md)) property.</span></span>
    
   - <span data-ttu-id="f23c6-114">Свойства **PR_SENDER.**</span><span class="sxs-lookup"><span data-stu-id="f23c6-114">The **PR_SENDER** properties.</span></span> 
    
   - <span data-ttu-id="f23c6-115">Свойства **PR_SENT_REPRESENTING.**</span><span class="sxs-lookup"><span data-stu-id="f23c6-115">The **PR_SENT_REPRESENTING** properties.</span></span> 
    
   - <span data-ttu-id="f23c6-116">Свойство **PR_RECEIPT_TIME** [(PidTagReceiptTime).](pidtagreceipttime-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="f23c6-116">The **PR_RECEIPT_TIME** ([PidTagReceiptTime](pidtagreceipttime-canonical-property.md)) property.</span></span>
    
   - <span data-ttu-id="f23c6-117">Свойство **PR_RTF_COMPRESSED** [(PidTagRtfCompressed)](pidtagrtfcompressed-canonical-property.md)или **PR_BODY** [(PidTagBody).](pidtagbody-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="f23c6-117">The **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) or **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) property.</span></span>
    
   - <span data-ttu-id="f23c6-118">Свойство **PR_SUBJECT** [(PidTagSubject).](pidtagsubject-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="f23c6-118">The **PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md)) property.</span></span>
    
   - <span data-ttu-id="f23c6-119">Свойство **PR_MESSAGE_CLASS** [(PidTagMessageClass).](pidtagmessageclass-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="f23c6-119">The **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)) property.</span></span>
    
   - <span data-ttu-id="f23c6-120">Любые свойства, необходимые классу сообщений.</span><span class="sxs-lookup"><span data-stu-id="f23c6-120">Any properties required by the message class.</span></span>
    
4. <span data-ttu-id="f23c6-121">Чтобы сохранить сообщение, позвоните по методу [IMAPIProp::SaveChanges.](imapiprop-savechanges.md)</span><span class="sxs-lookup"><span data-stu-id="f23c6-121">Call the message's [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method to save the message.</span></span> 
    
5. <span data-ttu-id="f23c6-122">При необходимости создайте вложение, установите его свойства и сохраните.</span><span class="sxs-lookup"><span data-stu-id="f23c6-122">If necessary, create an attachment, set its properties, and save it.</span></span> <span data-ttu-id="f23c6-123">Дополнительные сведения о добавлении вложений в сообщения см. в [приложении Creating a Message Attachment.](creating-a-message-attachment.md)</span><span class="sxs-lookup"><span data-stu-id="f23c6-123">For more information about adding attachments to messages, see [Creating a Message Attachment](creating-a-message-attachment.md).</span></span>
    
6. <span data-ttu-id="f23c6-124">Вызов **IMessage::SaveChanges,** чтобы сохранить сообщение.</span><span class="sxs-lookup"><span data-stu-id="f23c6-124">Call **IMessage::SaveChanges** to save the message.</span></span> <span data-ttu-id="f23c6-125">На этом этапе он появится в таблице содержимого папки назначения.</span><span class="sxs-lookup"><span data-stu-id="f23c6-125">At this point it will appear in the contents table of the destination folder.</span></span> 
    
<span data-ttu-id="f23c6-126">Обратите внимание, что список получателей не создается.</span><span class="sxs-lookup"><span data-stu-id="f23c6-126">Notice that you do not create a recipient list.</span></span> <span data-ttu-id="f23c6-127">Вместо этого вы установите несколько свойств, которые обычно устанавливаются поставщиком транспорта для отправленного сообщения.</span><span class="sxs-lookup"><span data-stu-id="f23c6-127">Instead, you set several properties that are normally set by a transport provider for a sent message.</span></span> 
  
<span data-ttu-id="f23c6-128">Если вы хотите сохранить сообщение с перерывами, прежде чем оно появится в таблице содержимого видимой папки, создайте его в скрытой папке, например корневой папке подтриба IPM, а затем переместите его в целевую папку.</span><span class="sxs-lookup"><span data-stu-id="f23c6-128">If you want to save a message intermittently before having it appear in the contents table of the visible folder, create it instead in a hidden folder such as the root folder of the IPM subtree and then move it to the target folder.</span></span> 
  

