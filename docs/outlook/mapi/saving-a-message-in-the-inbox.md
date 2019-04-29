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
ms.openlocfilehash: 672a9df55ce711b88451a517a2813c9ad8c599ce
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407895"
---
# <a name="saving-a-message-in-the-inbox"></a><span data-ttu-id="e250c-103">Сохранение сообщения в папке "Входящие"</span><span class="sxs-lookup"><span data-stu-id="e250c-103">Saving a Message in the Inbox</span></span>

  
  
<span data-ttu-id="e250c-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e250c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
 <span data-ttu-id="e250c-105">**Сохранение сообщения в папке "Входящие" без получателей**</span><span class="sxs-lookup"><span data-stu-id="e250c-105">**To store a message in the Inbox without any recipients**</span></span>
  
1. <span data-ttu-id="e250c-106">Call [IMsgStore:: жетрецеивефолдер](imsgstore-getreceivefolder.md) для получения идентификатора записи папки "Входящие".</span><span class="sxs-lookup"><span data-stu-id="e250c-106">Call [IMsgStore::GetReceiveFolder](imsgstore-getreceivefolder.md) to retrieve the entry identifier of the Inbox.</span></span> 
    
2. <span data-ttu-id="e250c-107">Call [IMsgStore:: OpenEntry](imsgstore-openentry.md) , чтобы открыть папку "Входящие" и получить указатель на него.</span><span class="sxs-lookup"><span data-stu-id="e250c-107">Call [IMsgStore::OpenEntry](imsgstore-openentry.md) to open the Inbox and retrieve a pointer to it.</span></span> 
    
3. <span data-ttu-id="e250c-108">ВыЗовите метод [IMAPIFolder:: CreateMessage](imapifolder-createmessage.md) для создания сообщения.</span><span class="sxs-lookup"><span data-stu-id="e250c-108">Call the Inbox's [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) method to create the message.</span></span> 
    
4. <span data-ttu-id="e250c-109">ВыЗовите метод [IMAPIProp:: SetProps](imapiprop-setprops.md) , чтобы добавить **пр_боди** ([PidTagBody](pidtagbody-canonical-property.md)), **пр_хтмл** ([PidTagHtml](pidtaghtml-canonical-property.md)) или **пр_ртф_компрессед** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) и **пр_субжект** ([ Свойства PidTagSubject](pidtagsubject-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="e250c-109">Call the message's [IMAPIProp::SetProps](imapiprop-setprops.md) method to add the **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)), **PR_HTML** ([PidTagHtml](pidtaghtml-canonical-property.md)), or **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) and **PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md)) properties.</span></span> 
    
5. <span data-ttu-id="e250c-110">Создайте каждое вложение, задайте его свойства и сохраните.</span><span class="sxs-lookup"><span data-stu-id="e250c-110">Create each attachment, set its properties, and save it.</span></span> <span data-ttu-id="e250c-111">Более подробную информацию о добавлении вложений в сообщения можно узнать в статье [Создание вложения сообщения](creating-a-message-attachment.md).</span><span class="sxs-lookup"><span data-stu-id="e250c-111">For detailed information about adding attachments to messages, see [Creating a Message Attachment](creating-a-message-attachment.md).</span></span>
    
6. <span data-ttu-id="e250c-112">Call **iMessage:: SaveChanges** для сохранения сообщения.</span><span class="sxs-lookup"><span data-stu-id="e250c-112">Call **IMessage::SaveChanges** to save the message.</span></span> <span data-ttu-id="e250c-113">На этом шаге он будет отображаться в таблице содержимое папки "Входящие".</span><span class="sxs-lookup"><span data-stu-id="e250c-113">At this point it will appear in the contents table of the Inbox.</span></span> 
    
<span data-ttu-id="e250c-114">Если вы хотите сохранить сообщение интермиттантли, прежде чем оно будет отображаться в таблице содержимого папки "Входящие", создайте его, а не в скрытой папке, такой как корневая папка поддерева IPM, а затем переместите его в папку "Входящие".</span><span class="sxs-lookup"><span data-stu-id="e250c-114">If you want to save a message intermittantly before having it appear in the contents table of the Inbox, create it instead in a hidden folder such as the root folder of the IPM subtree and then move it to the Inbox.</span></span> 
  

