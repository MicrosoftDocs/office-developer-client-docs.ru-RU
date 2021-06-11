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
# <a name="handling-a-message-store"></a><span data-ttu-id="639d8-103">Обработка хранилища сообщений</span><span class="sxs-lookup"><span data-stu-id="639d8-103">Handling a message store</span></span>
  
<span data-ttu-id="639d8-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="639d8-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="639d8-105">Обработка магазина сообщений является важной частью набора задач любого клиента.</span><span class="sxs-lookup"><span data-stu-id="639d8-105">Handling a message store is an important part of any client's set of tasks.</span></span> <span data-ttu-id="639d8-106">Эти задачи включают открытие, копирование, перемещение, добавление и удаление папок и сообщений, отображение различных таблиц, параметры свойств и управление уровнями доступа.</span><span class="sxs-lookup"><span data-stu-id="639d8-106">These tasks include opening, copying, moving, adding, and deleting folders and messages, displaying various tables, setting properties, and controlling access levels.</span></span>

- <span data-ttu-id="639d8-107">[Открытие хранилища сообщений](opening-a-message-store.md). Описывает, как открыть один или несколько магазинов сообщений во время сеанса.</span><span class="sxs-lookup"><span data-stu-id="639d8-107">[Opening a Message Store](opening-a-message-store.md): Describes how to open one or more message stores during a session.</span></span>
    
- <span data-ttu-id="639d8-108">[Открытие магазина сообщений по умолчанию.](opening-the-default-message-store.md)Описывается, как открыть хранилище сообщений по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="639d8-108">[Opening the Default Message Store](opening-the-default-message-store.md): Describes how to open the default message store.</span></span>
    
- <span data-ttu-id="639d8-109">[Проверка и инициализация](validating-and-initializing-a-message-store.md)магазина сообщений. Описывается, как инициализировать и проверить хранилище сообщений.</span><span class="sxs-lookup"><span data-stu-id="639d8-109">[Validating and Initializing a Message Store](validating-and-initializing-a-message-store.md): Describes how to initialize and validate a message store.</span></span>
    
- <span data-ttu-id="639d8-110">[Поиск в хранилище сообщений](searching-a-message-store.md). Описывает, как искать одну или несколько папок, ища сообщения, которые соответствуют критериям поиска.</span><span class="sxs-lookup"><span data-stu-id="639d8-110">[Searching a Message Store](searching-a-message-store.md): Describes how to look through one or more folders looking for messages that match search criteria.</span></span>
    
- <span data-ttu-id="639d8-111">[Выбор папки "Получение".](selecting-a-receive-folder.md)Описывает действия по созданию папки получения.</span><span class="sxs-lookup"><span data-stu-id="639d8-111">[Selecting a Receive Folder](selecting-a-receive-folder.md): Describes the steps for creating a receive folder.</span></span>
    
- <span data-ttu-id="639d8-112">[Открытие папки магазина сообщений.](opening-a-message-store-folder.md)Описывается, как открыть папку.</span><span class="sxs-lookup"><span data-stu-id="639d8-112">[Opening a Message Store Folder](opening-a-message-store-folder.md): Describes how to open a folder.</span></span>
    
- <span data-ttu-id="639d8-113">[Отображение таблицы содержимого](displaying-a-folder-contents-table.md)папки . Описывает, как отображать таблицу содержимого папки, содержаную сводную информацию обо всех ее сообщениях.</span><span class="sxs-lookup"><span data-stu-id="639d8-113">[Displaying a Folder Contents Table](displaying-a-folder-contents-table.md): Describes how to display the folder contents table that contains summary information about all of its messages.</span></span>
    
- <span data-ttu-id="639d8-114">[Обход папки "Папка входящие".](traversing-the-inbox-folder.md)Описывает, как циклить все сообщения в папке "Входящие".</span><span class="sxs-lookup"><span data-stu-id="639d8-114">[Traversing the Inbox Folder](traversing-the-inbox-folder.md): Describes how to cycle through all the messages in the Inbox.</span></span>
    
- <span data-ttu-id="639d8-115">[Копирование или перемещение сообщения или](copying-or-moving-a-message-or-a-folder.md)папки : Описывает, как скопировать или переместить одно или несколько сообщений.</span><span class="sxs-lookup"><span data-stu-id="639d8-115">[Copying or Moving a Message or a Folder](copying-or-moving-a-message-or-a-folder.md): Describes how to copy or move one or more messages.</span></span>
    
- <span data-ttu-id="639d8-116">[Открытие сообщения.](opening-a-message.md)Описывает, как открыть сообщение.</span><span class="sxs-lookup"><span data-stu-id="639d8-116">[Opening a Message](opening-a-message.md): Describes how to open a message.</span></span>
    
- <span data-ttu-id="639d8-117">[Поиск значка для сообщения](finding-the-icon-for-a-message.md). Описывает, как найти значок, связанный с сообщением.</span><span class="sxs-lookup"><span data-stu-id="639d8-117">[Finding the Icon for a Message](finding-the-icon-for-a-message.md): Describes how to find an icon that is associated with a message.</span></span>
    
- <span data-ttu-id="639d8-118">[Открытие дескриптора](opening-a-view-descriptor.md)представления : Описывает, как открыть дескриптор представления.</span><span class="sxs-lookup"><span data-stu-id="639d8-118">[Opening a View Descriptor](opening-a-view-descriptor.md): Describes how to open a view descriptor.</span></span>
    
- <span data-ttu-id="639d8-119">[Удаление сообщения](deleting-a-message.md). Описывает, как удалить сообщение.</span><span class="sxs-lookup"><span data-stu-id="639d8-119">[Deleting a Message](deleting-a-message.md): Describes how to delete a message.</span></span>
    
- <span data-ttu-id="639d8-120">[Сохранение сообщения в почтовом ящике](saving-a-message-in-the-inbox.md). Описывает, как хранить сообщение в почтовом ящике.</span><span class="sxs-lookup"><span data-stu-id="639d8-120">[Saving a Message in the Inbox](saving-a-message-in-the-inbox.md): Describes how to store a message in the Inbox.</span></span>
    
- <span data-ttu-id="639d8-121">[Поиск отправленных или сохраненных](finding-sent-or-saved-messages.md)сообщений. Описывает, как найти все исходяющие сообщения, которые были сохранены или отправлены.</span><span class="sxs-lookup"><span data-stu-id="639d8-121">[Finding Sent or Saved Messages](finding-sent-or-saved-messages.md): Describes how to locate all outgoing messages that have been saved or sent.</span></span>
    
- <span data-ttu-id="639d8-122">[Отслеживание разговоров](tracking-conversations.md). Описывает, как отслеживать беседы.</span><span class="sxs-lookup"><span data-stu-id="639d8-122">[Tracking Conversations](tracking-conversations.md): Describes how to track conversations.</span></span>
    

