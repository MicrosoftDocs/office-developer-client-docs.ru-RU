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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32350752"
---
# <a name="posting-a-message"></a><span data-ttu-id="09e00-103">Публикация сообщения</span><span class="sxs-lookup"><span data-stu-id="09e00-103">Posting a message</span></span>

<span data-ttu-id="09e00-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="09e00-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="09e00-105">Отправка сообщения похожа на отправку сообщения.</span><span class="sxs-lookup"><span data-stu-id="09e00-105">Posting a message is similar to sending a message.</span></span> <span data-ttu-id="09e00-106">Основным различием является назначение.</span><span class="sxs-lookup"><span data-stu-id="09e00-106">The main difference is the destination.</span></span> <span data-ttu-id="09e00-107">Вместо того чтобы направляться одному или нескольким получателям в одной или нескольких системах обмена сообщениями, помещенное в папку сообщение остается в папке в текущем хранилище сообщений.</span><span class="sxs-lookup"><span data-stu-id="09e00-107">Rather than being directed to one or more recipients across one or more messaging systems, a posted message remains in a folder in the current message store.</span></span>
  
### <a name="to-post-a-message"></a><span data-ttu-id="09e00-108">Публикация сообщения</span><span class="sxs-lookup"><span data-stu-id="09e00-108">To post a message</span></span>
  
1. <span data-ttu-id="09e00-109">Откройте папку назначения, вызвав [IMsgStore:: OpenEntry](imsgstore-openentry.md).</span><span class="sxs-lookup"><span data-stu-id="09e00-109">Open the destination folder by calling [IMsgStore::OpenEntry](imsgstore-openentry.md).</span></span> <span data-ttu-id="09e00-110">Если конечная папка является папкой "Входящие", необходимо указать идентификатор записи для передачи в **OpenEntry** , вызвав [IMsgStore:: жетрецеивефолдер](imsgstore-getreceivefolder.md).</span><span class="sxs-lookup"><span data-stu-id="09e00-110">If the destination folder is the Inbox, locate the entry identifier to pass to **OpenEntry** by calling [IMsgStore::GetReceiveFolder](imsgstore-getreceivefolder.md).</span></span> 
    
2. <span data-ttu-id="09e00-111">Call [IMAPIFolder:: CreateMessage](imapifolder-createmessage.md) для создания сообщения.</span><span class="sxs-lookup"><span data-stu-id="09e00-111">Call [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) to create the message.</span></span> 
    
3. <span data-ttu-id="09e00-112">ВыЗовите метод сообщения [IMAPIProp:: SetProps](imapiprop-setprops.md) , чтобы задать:</span><span class="sxs-lookup"><span data-stu-id="09e00-112">Call the message's [IMAPIProp::SetProps](imapiprop-setprops.md) method to set:</span></span> 
    
   - <span data-ttu-id="09e00-113">Флаг МСГФЛАГ_РЕАД в свойстве **PidTagMessageFlags** ( [пр_мессаже_флагс](pidtagmessageflags-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="09e00-113">The MSGFLAG_READ flag in the **PidTagMessageFlags** ( [PR_MESSAGE_FLAGS](pidtagmessageflags-canonical-property.md)) property.</span></span>
    
   - <span data-ttu-id="09e00-114">Свойства **пр_сендер** .</span><span class="sxs-lookup"><span data-stu-id="09e00-114">The **PR_SENDER** properties.</span></span> 
    
   - <span data-ttu-id="09e00-115">Свойства **пр_сент_репресентинг** .</span><span class="sxs-lookup"><span data-stu-id="09e00-115">The **PR_SENT_REPRESENTING** properties.</span></span> 
    
   - <span data-ttu-id="09e00-116">Свойство **пр_рецеипт_тиме** ([PidTagReceiptTime](pidtagreceipttime-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="09e00-116">The **PR_RECEIPT_TIME** ([PidTagReceiptTime](pidtagreceipttime-canonical-property.md)) property.</span></span>
    
   - <span data-ttu-id="09e00-117">Свойство **пр_ртф_компрессед** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) или **пр_боди** ([PidTagBody](pidtagbody-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="09e00-117">The **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) or **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) property.</span></span>
    
   - <span data-ttu-id="09e00-118">Свойство **пр_субжект** ([PidTagSubject](pidtagsubject-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="09e00-118">The **PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md)) property.</span></span>
    
   - <span data-ttu-id="09e00-119">Свойство **пр_мессаже_класс** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="09e00-119">The **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)) property.</span></span>
    
   - <span data-ttu-id="09e00-120">Все свойства, необходимые для класса Message.</span><span class="sxs-lookup"><span data-stu-id="09e00-120">Any properties required by the message class.</span></span>
    
4. <span data-ttu-id="09e00-121">ВыЗовите метод [IMAPIProp:: SaveChanges](imapiprop-savechanges.md) сообщения для сохранения сообщения.</span><span class="sxs-lookup"><span data-stu-id="09e00-121">Call the message's [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method to save the message.</span></span> 
    
5. <span data-ttu-id="09e00-122">При необходимости создайте вложение, задайте его свойства и сохраните его.</span><span class="sxs-lookup"><span data-stu-id="09e00-122">If necessary, create an attachment, set its properties, and save it.</span></span> <span data-ttu-id="09e00-123">Дополнительные сведения о добавлении вложений в сообщения приведены в статье [Создание вложения сообщения](creating-a-message-attachment.md).</span><span class="sxs-lookup"><span data-stu-id="09e00-123">For more information about adding attachments to messages, see [Creating a Message Attachment](creating-a-message-attachment.md).</span></span>
    
6. <span data-ttu-id="09e00-124">Call **iMessage:: SaveChanges** для сохранения сообщения.</span><span class="sxs-lookup"><span data-stu-id="09e00-124">Call **IMessage::SaveChanges** to save the message.</span></span> <span data-ttu-id="09e00-125">На этом шаге он будет отображаться в таблице содержимого конечной папки.</span><span class="sxs-lookup"><span data-stu-id="09e00-125">At this point it will appear in the contents table of the destination folder.</span></span> 
    
<span data-ttu-id="09e00-126">Обратите внимание, что список получателей не создается.</span><span class="sxs-lookup"><span data-stu-id="09e00-126">Notice that you do not create a recipient list.</span></span> <span data-ttu-id="09e00-127">Вместо этого необходимо задать несколько свойств, которые обычно задаются поставщиком транспорта для отправленного сообщения.</span><span class="sxs-lookup"><span data-stu-id="09e00-127">Instead, you set several properties that are normally set by a transport provider for a sent message.</span></span> 
  
<span data-ttu-id="09e00-128">Если вы хотите, чтобы сообщение сохранялось периодически, прежде чем оно будет отображаться в таблице содержимого видимой папки, создайте его, а не в скрытой папке, такой как корневая папка поддерева IPM, а затем переместите его в целевую папку.</span><span class="sxs-lookup"><span data-stu-id="09e00-128">If you want to save a message intermittently before having it appear in the contents table of the visible folder, create it instead in a hidden folder such as the root folder of the IPM subtree and then move it to the target folder.</span></span> 
  

