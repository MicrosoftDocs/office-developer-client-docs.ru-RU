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
# <a name="saving-a-message-in-the-inbox"></a><span data-ttu-id="3610a-103">Сохранение сообщения в почтовом ящике</span><span class="sxs-lookup"><span data-stu-id="3610a-103">Saving a Message in the Inbox</span></span>

  
  
<span data-ttu-id="3610a-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3610a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
 <span data-ttu-id="3610a-105">**Хранение сообщения в почтовой ящике без получателей**</span><span class="sxs-lookup"><span data-stu-id="3610a-105">**To store a message in the Inbox without any recipients**</span></span>
  
1. <span data-ttu-id="3610a-106">Вызовите [IMsgStore::GetReceiveFolder,](imsgstore-getreceivefolder.md) чтобы получить идентификатор записи для входящих сообщений.</span><span class="sxs-lookup"><span data-stu-id="3610a-106">Call [IMsgStore::GetReceiveFolder](imsgstore-getreceivefolder.md) to retrieve the entry identifier of the Inbox.</span></span> 
    
2. <span data-ttu-id="3610a-107">Вызовите [IMsgStore::OpenEntry,](imsgstore-openentry.md) чтобы открыть "Входящие" и получить на него указатель.</span><span class="sxs-lookup"><span data-stu-id="3610a-107">Call [IMsgStore::OpenEntry](imsgstore-openentry.md) to open the Inbox and retrieve a pointer to it.</span></span> 
    
3. <span data-ttu-id="3610a-108">Вызовите метод [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) почтового ящика, чтобы создать сообщение.</span><span class="sxs-lookup"><span data-stu-id="3610a-108">Call the Inbox's [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) method to create the message.</span></span> 
    
4. <span data-ttu-id="3610a-109">Вызовите метод [IMAPIProp::SetProps](imapiprop-setprops.md) сообщения, чтобы добавить свойства **PR_BODY** ([PidTagBody),](pidtagbody-canonical-property.md) **PR_HTML** ([PidTagHtml)](pidtaghtml-canonical-property.md)или **PR_RTF_COMPRESSED** ([PidTagRtfCompressed)](pidtagrtfcompressed-canonical-property.md)и **PR_SUBJECT** ([PidTagSubject).](pidtagsubject-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="3610a-109">Call the message's [IMAPIProp::SetProps](imapiprop-setprops.md) method to add the **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)), **PR_HTML** ([PidTagHtml](pidtaghtml-canonical-property.md)), or **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) and **PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md)) properties.</span></span> 
    
5. <span data-ttu-id="3610a-110">Создайте каждое вложение, установите его свойства и сохраните его.</span><span class="sxs-lookup"><span data-stu-id="3610a-110">Create each attachment, set its properties, and save it.</span></span> <span data-ttu-id="3610a-111">Дополнительные сведения о добавлении вложений в сообщения см. в описании [создания вложения в сообщение.](creating-a-message-attachment.md)</span><span class="sxs-lookup"><span data-stu-id="3610a-111">For detailed information about adding attachments to messages, see [Creating a Message Attachment](creating-a-message-attachment.md).</span></span>
    
6. <span data-ttu-id="3610a-112">Вызовите **IMessage::SaveChanges,** чтобы сохранить сообщение.</span><span class="sxs-lookup"><span data-stu-id="3610a-112">Call **IMessage::SaveChanges** to save the message.</span></span> <span data-ttu-id="3610a-113">На этом этапе он появится в таблице содержимого в "Входящие".</span><span class="sxs-lookup"><span data-stu-id="3610a-113">At this point it will appear in the contents table of the Inbox.</span></span> 
    
<span data-ttu-id="3610a-114">Если вы хотите периодически сохранять сообщение, прежде чем оно появится в таблице содержимого папки "Входящие", создайте его в скрытой папке, например в корневой папке поддерева IPM, а затем переместите его в папку "Входящие".</span><span class="sxs-lookup"><span data-stu-id="3610a-114">If you want to save a message intermittantly before having it appear in the contents table of the Inbox, create it instead in a hidden folder such as the root folder of the IPM subtree and then move it to the Inbox.</span></span> 
  

