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
ms.openlocfilehash: 6fe642d10a50d25874aee170441a07c184b46575
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22591095"
---
# <a name="ipm-subtree"></a><span data-ttu-id="dc7b1-103">Поддерево IPM</span><span class="sxs-lookup"><span data-stu-id="dc7b1-103">IPM Subtree</span></span>

  
  
<span data-ttu-id="dc7b1-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="dc7b1-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="dc7b1-105">MAPI создает дерево папок в корневой папке хранилищем сообщений для всех клиентов, сообщения, чтобы отправлять и принимать сообщения от человека, а не на компьютер, получателей.</span><span class="sxs-lookup"><span data-stu-id="dc7b1-105">MAPI creates a tree of folders beneath the root folder of a message store for all clients that send messages to and receive messages from human, rather than computer, recipients.</span></span> <span data-ttu-id="dc7b1-106">Сообщений, отправленных в между человеческого получателей, известных как сообщения электронной почты — это и известные это дерево как сообщения электронной почты — это или IPM поддерева.</span><span class="sxs-lookup"><span data-stu-id="dc7b1-106">Messages exchanged between human recipients are known as interpersonal messages, and this tree is known as the interpersonal message, or IPM, subtree.</span></span> 
  
<span data-ttu-id="dc7b1-107">Поддерева IPM в хранилище доставки состоит из по крайней мере следующие папки:</span><span class="sxs-lookup"><span data-stu-id="dc7b1-107">An IPM subtree for a delivery store consists of at least the following folders:</span></span>
  
- <span data-ttu-id="dc7b1-108">Inbox</span><span class="sxs-lookup"><span data-stu-id="dc7b1-108">Inbox</span></span>
    
- <span data-ttu-id="dc7b1-109">Исходящие</span><span class="sxs-lookup"><span data-stu-id="dc7b1-109">Outbox</span></span>
    
- <span data-ttu-id="dc7b1-110">Отправленные элементы</span><span class="sxs-lookup"><span data-stu-id="dc7b1-110">Sent Items</span></span>
    
- <span data-ttu-id="dc7b1-111">"Удаленные"</span><span class="sxs-lookup"><span data-stu-id="dc7b1-111">Deleted Items</span></span>
    
<span data-ttu-id="dc7b1-112">Ниже приведены имена по умолчанию и ролей для каждого из этих папок; Клиент может указывать собственные имена, если имена по умолчанию не подходят.</span><span class="sxs-lookup"><span data-stu-id="dc7b1-112">These are the default names and roles for each of these folders; a client can specify its own names if the default names are not appropriate.</span></span> <span data-ttu-id="dc7b1-113">MAPI назначает имена по умолчанию и связей для этих папок, которые следует хранить сообщения из случайно исчезновением Если клиент отказывается установления получение папок для сообщения.</span><span class="sxs-lookup"><span data-stu-id="dc7b1-113">MAPI assigns default names and associations for these folders to keep messages from inadvertently disappearing if a client neglects to establish receiving folders for messages.</span></span> 
  
<span data-ttu-id="dc7b1-114">В контексте Microsoft Office Outlook поддерева IPM состоит из папок дополнительные по умолчанию для календаря, контакты, задачи, заметки и журнал.</span><span class="sxs-lookup"><span data-stu-id="dc7b1-114">In a Microsoft Office Outlook context, an IPM subtree consists of additional default folders for Calendar, Contacts, Tasks, Notes, and Journal.</span></span>
  
<span data-ttu-id="dc7b1-115">Папки «Входящие» обычно содержит входящих сообщений и исходящие — исходящие сообщения (то есть сообщения, ожидающие отправки).</span><span class="sxs-lookup"><span data-stu-id="dc7b1-115">The Inbox typically holds incoming messages, and the Outbox holds outgoing messages (that is, messages waiting to be sent).</span></span> <span data-ttu-id="dc7b1-116">Папка «Отправленные» содержит копию всех отправленных сообщений, если клиент значение свойства **PR_SENTMAIL_ENTRYID** ([PidTagSentMailEntryId](pidtagsentmailentryid-canonical-property.md)) идентификатор записи из этой папки.</span><span class="sxs-lookup"><span data-stu-id="dc7b1-116">The Sent Items folder holds a copy of each sent message if the client has set the **PR_SENTMAIL_ENTRYID** ([PidTagSentMailEntryId](pidtagsentmailentryid-canonical-property.md)) property to the entry identifier of this folder.</span></span> <span data-ttu-id="dc7b1-117">Папки «Удаленные» содержит сообщения, помеченные для удаления.</span><span class="sxs-lookup"><span data-stu-id="dc7b1-117">The Deleted Items folder contains messages marked for removal.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="dc7b1-118">См. также</span><span class="sxs-lookup"><span data-stu-id="dc7b1-118">See also</span></span>



[<span data-ttu-id="dc7b1-119">����� MAPI</span><span class="sxs-lookup"><span data-stu-id="dc7b1-119">MAPI Folders</span></span>](mapi-folders.md)

