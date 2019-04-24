---
title: Поддерево IPM
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: b5fc6084-722d-44e8-8637-f4160a4fb19b
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 92c7a09d9d608ac31920d49b20f78bedd26f5fcd
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32317110"
---
# <a name="ipm-subtree"></a><span data-ttu-id="a9c20-103">Поддерево IPM</span><span class="sxs-lookup"><span data-stu-id="a9c20-103">IPM Subtree</span></span>

  
  
<span data-ttu-id="a9c20-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a9c20-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a9c20-105">MAPI создает дерево папок под корневой папкой хранилища сообщений для всех клиентов, которые отправляют и получают сообщения от человека, а не компьютера, получателя.</span><span class="sxs-lookup"><span data-stu-id="a9c20-105">MAPI creates a tree of folders beneath the root folder of a message store for all clients that send messages to and receive messages from human, rather than computer, recipients.</span></span> <span data-ttu-id="a9c20-106">Сообщения, которыми обмениваются получатели людей, называются взаимосвязанными сообщениями, а это дерево называется межпользовательским сообщением или IPM, поддеревом.</span><span class="sxs-lookup"><span data-stu-id="a9c20-106">Messages exchanged between human recipients are known as interpersonal messages, and this tree is known as the interpersonal message, or IPM, subtree.</span></span> 
  
<span data-ttu-id="a9c20-107">Поддерево IPM для хранилища доставки состоит из по крайней мере следующих папок:</span><span class="sxs-lookup"><span data-stu-id="a9c20-107">An IPM subtree for a delivery store consists of at least the following folders:</span></span>
  
- <span data-ttu-id="a9c20-108">Inbox;</span><span class="sxs-lookup"><span data-stu-id="a9c20-108">Inbox</span></span>
    
- <span data-ttu-id="a9c20-109">Исходящие</span><span class="sxs-lookup"><span data-stu-id="a9c20-109">Outbox</span></span>
    
- <span data-ttu-id="a9c20-110">Отправленные</span><span class="sxs-lookup"><span data-stu-id="a9c20-110">Sent Items</span></span>
    
- <span data-ttu-id="a9c20-111">Удаленные</span><span class="sxs-lookup"><span data-stu-id="a9c20-111">Deleted Items</span></span>
    
<span data-ttu-id="a9c20-112">Это имена и роли по умолчанию для каждой из этих папок; Клиент может указать собственные имена, если имена по умолчанию не подходят.</span><span class="sxs-lookup"><span data-stu-id="a9c20-112">These are the default names and roles for each of these folders; a client can specify its own names if the default names are not appropriate.</span></span> <span data-ttu-id="a9c20-113">MAPI назначает имена по умолчанию и сопоставления для этих папок, чтобы предотвратить непреднамеренное исчезновение сообщений, если клиент не устанавливает получение папок для сообщений.</span><span class="sxs-lookup"><span data-stu-id="a9c20-113">MAPI assigns default names and associations for these folders to keep messages from inadvertently disappearing if a client neglects to establish receiving folders for messages.</span></span> 
  
<span data-ttu-id="a9c20-114">В контексте Microsoft Office Outlook поддерево IPM состоит из дополнительных папок по умолчанию для календаря, контактов, задач, заМеток и журнала.</span><span class="sxs-lookup"><span data-stu-id="a9c20-114">In a Microsoft Office Outlook context, an IPM subtree consists of additional default folders for Calendar, Contacts, Tasks, Notes, and Journal.</span></span>
  
<span data-ttu-id="a9c20-115">Обычно в папке "Входящие" хранятся входящие сообщения, а в папке "исХодящие" находятся исходящие сообщения (то есть сообщения, ожидающие отправки).</span><span class="sxs-lookup"><span data-stu-id="a9c20-115">The Inbox typically holds incoming messages, and the Outbox holds outgoing messages (that is, messages waiting to be sent).</span></span> <span data-ttu-id="a9c20-116">Папка "Отправленные" содержит копию каждого отправленного сообщения, если клиент установил для свойства **пр_сентмаил_ентрид** ([PidTagSentMailEntryId](pidtagsentmailentryid-canonical-property.md)) идентификатор записи этой папки.</span><span class="sxs-lookup"><span data-stu-id="a9c20-116">The Sent Items folder holds a copy of each sent message if the client has set the **PR_SENTMAIL_ENTRYID** ([PidTagSentMailEntryId](pidtagsentmailentryid-canonical-property.md)) property to the entry identifier of this folder.</span></span> <span data-ttu-id="a9c20-117">Папка "Удаленные" содержит сообщения, помеченные для удаления.</span><span class="sxs-lookup"><span data-stu-id="a9c20-117">The Deleted Items folder contains messages marked for removal.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="a9c20-118">См. также</span><span class="sxs-lookup"><span data-stu-id="a9c20-118">See also</span></span>



[<span data-ttu-id="a9c20-119">����� MAPI</span><span class="sxs-lookup"><span data-stu-id="a9c20-119">MAPI Folders</span></span>](mapi-folders.md)

