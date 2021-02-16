---
title: Обработка хранилища сообщений
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 7eca0e1f-a855-4ef7-b892-0bddee59de5e
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 933dbd95a4b2f82d78e6e8035936eb2be4ba09ec
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407545"
---
# <a name="handling-a-message-store"></a><span data-ttu-id="ee169-103">Обработка хранилища сообщений</span><span class="sxs-lookup"><span data-stu-id="ee169-103">Handling a message store</span></span>
  
<span data-ttu-id="ee169-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ee169-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ee169-105">Обработка хранения сообщений является важной частью набора задач любого клиента.</span><span class="sxs-lookup"><span data-stu-id="ee169-105">Handling a message store is an important part of any client's set of tasks.</span></span> <span data-ttu-id="ee169-106">К этим задачам относятся открытие, копирование, перемещение, добавление и удаление папок и сообщений, отображение различных таблиц, настройка свойств и управление уровнями доступа.</span><span class="sxs-lookup"><span data-stu-id="ee169-106">These tasks include opening, copying, moving, adding, and deleting folders and messages, displaying various tables, setting properties, and controlling access levels.</span></span>

- <span data-ttu-id="ee169-107">[Открытие хранилища сообщений](opening-a-message-store.md): описывается, как открыть одно или несколько хранилищ сообщений во время сеанса.</span><span class="sxs-lookup"><span data-stu-id="ee169-107">[Opening a Message Store](opening-a-message-store.md): Describes how to open one or more message stores during a session.</span></span>
    
- <span data-ttu-id="ee169-108">[Открытие магазина сообщений по умолчанию](opening-the-default-message-store.md): описывается, как открыть хранилище сообщений по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="ee169-108">[Opening the Default Message Store](opening-the-default-message-store.md): Describes how to open the default message store.</span></span>
    
- <span data-ttu-id="ee169-109">[Проверка и инициализация хранилище сообщений](validating-and-initializing-a-message-store.md): описывается, как инициализировать и проверить хранилище сообщений.</span><span class="sxs-lookup"><span data-stu-id="ee169-109">[Validating and Initializing a Message Store](validating-and-initializing-a-message-store.md): Describes how to initialize and validate a message store.</span></span>
    
- <span data-ttu-id="ee169-110">[Поиск в хранилище сообщений:](searching-a-message-store.md)описание того, как искать сообщения, которые соответствуют условиям поиска, в одной или более папках.</span><span class="sxs-lookup"><span data-stu-id="ee169-110">[Searching a Message Store](searching-a-message-store.md): Describes how to look through one or more folders looking for messages that match search criteria.</span></span>
    
- <span data-ttu-id="ee169-111">[Выбор папки получения](selecting-a-receive-folder.md): описывает действия по созданию папки получения.</span><span class="sxs-lookup"><span data-stu-id="ee169-111">[Selecting a Receive Folder](selecting-a-receive-folder.md): Describes the steps for creating a receive folder.</span></span>
    
- <span data-ttu-id="ee169-112">[Открытие папки в хранилище сообщений](opening-a-message-store-folder.md): описывается, как открыть папку.</span><span class="sxs-lookup"><span data-stu-id="ee169-112">[Opening a Message Store Folder](opening-a-message-store-folder.md): Describes how to open a folder.</span></span>
    
- <span data-ttu-id="ee169-113">[Displaying a Folder Contents Table](displaying-a-folder-contents-table.md): Describes how to display the folder contents table that contains summary information about all of its messages.</span><span class="sxs-lookup"><span data-stu-id="ee169-113">[Displaying a Folder Contents Table](displaying-a-folder-contents-table.md): Describes how to display the folder contents table that contains summary information about all of its messages.</span></span>
    
- <span data-ttu-id="ee169-114">[Просмотр папки "Входящие":](traversing-the-inbox-folder.md)описывает циклику всех сообщений в папке "Входящие".</span><span class="sxs-lookup"><span data-stu-id="ee169-114">[Traversing the Inbox Folder](traversing-the-inbox-folder.md): Describes how to cycle through all the messages in the Inbox.</span></span>
    
- <span data-ttu-id="ee169-115">[Копирование или перемещение сообщения или](copying-or-moving-a-message-or-a-folder.md)папки : описывает копирование или перемещение одного или более сообщений.</span><span class="sxs-lookup"><span data-stu-id="ee169-115">[Copying or Moving a Message or a Folder](copying-or-moving-a-message-or-a-folder.md): Describes how to copy or move one or more messages.</span></span>
    
- <span data-ttu-id="ee169-116">[Открытие сообщения](opening-a-message.md): описывает, как открыть сообщение.</span><span class="sxs-lookup"><span data-stu-id="ee169-116">[Opening a Message](opening-a-message.md): Describes how to open a message.</span></span>
    
- <span data-ttu-id="ee169-117">[Поиск значка сообщения:](finding-the-icon-for-a-message.md)описание поиска значка, связанного с сообщением.</span><span class="sxs-lookup"><span data-stu-id="ee169-117">[Finding the Icon for a Message](finding-the-icon-for-a-message.md): Describes how to find an icon that is associated with a message.</span></span>
    
- <span data-ttu-id="ee169-118">[Открытие дескриптора представления](opening-a-view-descriptor.md): описывает, как открыть дескриптор представления.</span><span class="sxs-lookup"><span data-stu-id="ee169-118">[Opening a View Descriptor](opening-a-view-descriptor.md): Describes how to open a view descriptor.</span></span>
    
- <span data-ttu-id="ee169-119">[Удаление сообщения:](deleting-a-message.md)описывается, как удалить сообщение.</span><span class="sxs-lookup"><span data-stu-id="ee169-119">[Deleting a Message](deleting-a-message.md): Describes how to delete a message.</span></span>
    
- <span data-ttu-id="ee169-120">[Saving a Message in the Inbox](saving-a-message-in-the-inbox.md): Describes how to store a message in the Inbox.</span><span class="sxs-lookup"><span data-stu-id="ee169-120">[Saving a Message in the Inbox](saving-a-message-in-the-inbox.md): Describes how to store a message in the Inbox.</span></span>
    
- <span data-ttu-id="ee169-121">[Поиск отправленных или сохраненных](finding-sent-or-saved-messages.md)сообщений : описывается, как найти все исходяющие сообщения, которые были сохранены или отправлены.</span><span class="sxs-lookup"><span data-stu-id="ee169-121">[Finding Sent or Saved Messages](finding-sent-or-saved-messages.md): Describes how to locate all outgoing messages that have been saved or sent.</span></span>
    
- <span data-ttu-id="ee169-122">[Отслеживание бесед](tracking-conversations.md): описывается, как отслеживать беседы.</span><span class="sxs-lookup"><span data-stu-id="ee169-122">[Tracking Conversations](tracking-conversations.md): Describes how to track conversations.</span></span>
    

