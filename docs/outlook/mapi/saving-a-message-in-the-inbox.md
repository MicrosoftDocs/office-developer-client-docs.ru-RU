---
title: Сохранение сообщения в почтовом ящике
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 3df04d4e-7e80-4232-aadc-c05c99ab59cb
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 672a9df55ce711b88451a517a2813c9ad8c599ce
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407895"
---
# <a name="saving-a-message-in-the-inbox"></a><span data-ttu-id="da61f-103">Сохранение сообщения в почтовом ящике</span><span class="sxs-lookup"><span data-stu-id="da61f-103">Saving a Message in the Inbox</span></span>

  
  
<span data-ttu-id="da61f-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="da61f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
 <span data-ttu-id="da61f-105">**Хранение сообщения в почтовом ящике без получателей**</span><span class="sxs-lookup"><span data-stu-id="da61f-105">**To store a message in the Inbox without any recipients**</span></span>
  
1. <span data-ttu-id="da61f-106">Позвоните [в IMsgStore::GetReceiveFolder,](imsgstore-getreceivefolder.md) чтобы получить идентификатор входа в почтовый ящик.</span><span class="sxs-lookup"><span data-stu-id="da61f-106">Call [IMsgStore::GetReceiveFolder](imsgstore-getreceivefolder.md) to retrieve the entry identifier of the Inbox.</span></span> 
    
2. <span data-ttu-id="da61f-107">Позвоните [в IMsgStore::OpenEntry,](imsgstore-openentry.md) чтобы открыть почтовый ящик и получить указатель на него.</span><span class="sxs-lookup"><span data-stu-id="da61f-107">Call [IMsgStore::OpenEntry](imsgstore-openentry.md) to open the Inbox and retrieve a pointer to it.</span></span> 
    
3. <span data-ttu-id="da61f-108">Чтобы создать сообщение, позвоните по методу [IMAPIFolder::CreateMessage.](imapifolder-createmessage.md)</span><span class="sxs-lookup"><span data-stu-id="da61f-108">Call the Inbox's [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) method to create the message.</span></span> 
    
4. <span data-ttu-id="da61f-109">Позвоните по методу [IMAPIProp::SetProps,](imapiprop-setprops.md) чтобы добавить свойства **PR_BODY** [(PidTagBody),](pidtagbody-canonical-property.md) **PR_HTML** [(PidTagHtml),](pidtaghtml-canonical-property.md) **или PR_RTF_COMPRESSED** [(PidTagRtfCompressed)](pidtagrtfcompressed-canonical-property.md)и **PR_SUBJECT** [(PidTagSubject).](pidtagsubject-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="da61f-109">Call the message's [IMAPIProp::SetProps](imapiprop-setprops.md) method to add the **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)), **PR_HTML** ([PidTagHtml](pidtaghtml-canonical-property.md)), or **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) and **PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md)) properties.</span></span> 
    
5. <span data-ttu-id="da61f-110">Создайте каждое вложение, установите его свойства и сохраните.</span><span class="sxs-lookup"><span data-stu-id="da61f-110">Create each attachment, set its properties, and save it.</span></span> <span data-ttu-id="da61f-111">Подробные сведения о добавлении вложений в сообщения см. в [приложении Creating a Message Attachment](creating-a-message-attachment.md).</span><span class="sxs-lookup"><span data-stu-id="da61f-111">For detailed information about adding attachments to messages, see [Creating a Message Attachment](creating-a-message-attachment.md).</span></span>
    
6. <span data-ttu-id="da61f-112">Вызов **IMessage::SaveChanges,** чтобы сохранить сообщение.</span><span class="sxs-lookup"><span data-stu-id="da61f-112">Call **IMessage::SaveChanges** to save the message.</span></span> <span data-ttu-id="da61f-113">На этом этапе он появится в таблице содержимого почтового ящика.</span><span class="sxs-lookup"><span data-stu-id="da61f-113">At this point it will appear in the contents table of the Inbox.</span></span> 
    
<span data-ttu-id="da61f-114">Если необходимо сохранить сообщение с перерывами, прежде чем оно появится в таблице содержимого папки "Входящие", создайте его в скрытой папке, например корневой папке подтриба IPM, а затем переместите его в папку "Входящие".</span><span class="sxs-lookup"><span data-stu-id="da61f-114">If you want to save a message intermittantly before having it appear in the contents table of the Inbox, create it instead in a hidden folder such as the root folder of the IPM subtree and then move it to the Inbox.</span></span> 
  

