---
title: Сохранение сообщения в папке "Входящие"
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 3df04d4e-7e80-4232-aadc-c05c99ab59cb
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 3c48ded73d924a400632a94feab65f7afca6e526
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19812168"
---
# <a name="saving-a-message-in-the-inbox"></a><span data-ttu-id="67494-103">Сохранение сообщения в папке "Входящие"</span><span class="sxs-lookup"><span data-stu-id="67494-103">Saving a Message in the Inbox</span></span>

  
  
<span data-ttu-id="67494-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="67494-104">**Applies to**: Outlook</span></span> 
  
 <span data-ttu-id="67494-105">**Для хранения сообщения в папке "Входящие" без получателей**</span><span class="sxs-lookup"><span data-stu-id="67494-105">**To store a message in the Inbox without any recipients**</span></span>
  
1. <span data-ttu-id="67494-106">Вызовите [IMsgStore::GetReceiveFolder](imsgstore-getreceivefolder.md) , чтобы получить идентификатор записи из папки «Входящие».</span><span class="sxs-lookup"><span data-stu-id="67494-106">Call [IMsgStore::GetReceiveFolder](imsgstore-getreceivefolder.md) to retrieve the entry identifier of the Inbox.</span></span> 
    
2. <span data-ttu-id="67494-107">Вызов [IMsgStore::OpenEntry](imsgstore-openentry.md) для открытия папки «Входящие» и получить указатель на него.</span><span class="sxs-lookup"><span data-stu-id="67494-107">Call [IMsgStore::OpenEntry](imsgstore-openentry.md) to open the Inbox and retrieve a pointer to it.</span></span> 
    
3. <span data-ttu-id="67494-108">Вызов метода [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) папке "Входящие" для создания сообщения.</span><span class="sxs-lookup"><span data-stu-id="67494-108">Call the Inbox's [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) method to create the message.</span></span> 
    
4. <span data-ttu-id="67494-109">Вызовите метод [IMAPIProp::SetProps](imapiprop-setprops.md) сообщения, чтобы добавить **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)), **PR_HTML** ([PidTagHtml](pidtaghtml-canonical-property.md)) или **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) и **PR_SUBJECT** ([ PidTagSubject](pidtagsubject-canonical-property.md)) свойства.</span><span class="sxs-lookup"><span data-stu-id="67494-109">Call the message's [IMAPIProp::SetProps](imapiprop-setprops.md) method to add the **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)), **PR_HTML** ([PidTagHtml](pidtaghtml-canonical-property.md)), or **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) and **PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md)) properties.</span></span> 
    
5. <span data-ttu-id="67494-110">Создание каждого вложения, задайте его свойства и сохраните его.</span><span class="sxs-lookup"><span data-stu-id="67494-110">Create each attachment, set its properties, and save it.</span></span> <span data-ttu-id="67494-111">Подробные сведения о добавлении вложений в сообщения [Вложения сообщения](creating-a-message-attachment.md)см.</span><span class="sxs-lookup"><span data-stu-id="67494-111">For detailed information about adding attachments to messages, see [Creating a Message Attachment](creating-a-message-attachment.md).</span></span>
    
6. <span data-ttu-id="67494-112">Вызовите **IMessage::SaveChanges** , чтобы сохранить сообщение.</span><span class="sxs-lookup"><span data-stu-id="67494-112">Call **IMessage::SaveChanges** to save the message.</span></span> <span data-ttu-id="67494-113">На этом этапе оно будет отображаться в таблице содержимое из папки «Входящие».</span><span class="sxs-lookup"><span data-stu-id="67494-113">At this point it will appear in the contents table of the Inbox.</span></span> 
    
<span data-ttu-id="67494-114">Если вы хотите сохранить intermittantly сообщение перед его отображаются в таблице содержимое из папки «Входящие», вместо этого создать в скрытой папке, например в корневую папку поддерева IPM и затем перетащить его в папке "Входящие".</span><span class="sxs-lookup"><span data-stu-id="67494-114">If you want to save a message intermittantly before having it appear in the contents table of the Inbox, create it instead in a hidden folder such as the root folder of the IPM subtree and then move it to the Inbox.</span></span> 
  

