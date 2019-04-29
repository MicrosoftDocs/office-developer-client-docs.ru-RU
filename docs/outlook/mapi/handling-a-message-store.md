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
# <a name="handling-a-message-store"></a><span data-ttu-id="9992b-103">Обработка хранилища сообщений</span><span class="sxs-lookup"><span data-stu-id="9992b-103">Handling a message store</span></span>
  
<span data-ttu-id="9992b-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9992b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9992b-105">Обработка хранилища сообщений является важной частью любого набора задач клиента.</span><span class="sxs-lookup"><span data-stu-id="9992b-105">Handling a message store is an important part of any client's set of tasks.</span></span> <span data-ttu-id="9992b-106">К этим задачам относятся открытие, копирование, перемещение, Добавление и удаление папок и сообщений, отображение различных таблиц, установка свойств и управление уровнями доступа.</span><span class="sxs-lookup"><span data-stu-id="9992b-106">These tasks include opening, copying, moving, adding, and deleting folders and messages, displaying various tables, setting properties, and controlling access levels.</span></span>

- <span data-ttu-id="9992b-107">[Открытие хранилища сообщений](opening-a-message-store.md): в этой статье описывается открытие одного или нескольких хранилищ сообщений во время сеанса.</span><span class="sxs-lookup"><span data-stu-id="9992b-107">[Opening a Message Store](opening-a-message-store.md): Describes how to open one or more message stores during a session.</span></span>
    
- <span data-ttu-id="9992b-108">[Открытие хранилища сообщений по умолчанию](opening-the-default-message-store.md): инструкции по открытию хранилища сообщений по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="9992b-108">[Opening the Default Message Store](opening-the-default-message-store.md): Describes how to open the default message store.</span></span>
    
- <span data-ttu-id="9992b-109">[Проверка и инициализация хранилища сообщений](validating-and-initializing-a-message-store.md): описание инициализации и проверки хранилища сообщений.</span><span class="sxs-lookup"><span data-stu-id="9992b-109">[Validating and Initializing a Message Store](validating-and-initializing-a-message-store.md): Describes how to initialize and validate a message store.</span></span>
    
- <span data-ttu-id="9992b-110">[Поиск в хранилище сообщений](searching-a-message-store.md): в этой статье описывается, как просматривать одну или несколько папок для поиска сообщений, которые отвечают условиям поиска.</span><span class="sxs-lookup"><span data-stu-id="9992b-110">[Searching a Message Store](searching-a-message-store.md): Describes how to look through one or more folders looking for messages that match search criteria.</span></span>
    
- <span data-ttu-id="9992b-111">[Выбор папки получения](selecting-a-receive-folder.md): описание действий по созданию папки получения.</span><span class="sxs-lookup"><span data-stu-id="9992b-111">[Selecting a Receive Folder](selecting-a-receive-folder.md): Describes the steps for creating a receive folder.</span></span>
    
- <span data-ttu-id="9992b-112">[Открытие папки хранилища сообщений](opening-a-message-store-folder.md): инструкции по открытию папки.</span><span class="sxs-lookup"><span data-stu-id="9992b-112">[Opening a Message Store Folder](opening-a-message-store-folder.md): Describes how to open a folder.</span></span>
    
- <span data-ttu-id="9992b-113">[Отображение таблицы содержимого папки](displaying-a-folder-contents-table.md): в этой статье описывается, как отобразить таблицу содержимого папки, в которой содержатся сводные сведения обо всех сообщениях.</span><span class="sxs-lookup"><span data-stu-id="9992b-113">[Displaying a Folder Contents Table](displaying-a-folder-contents-table.md): Describes how to display the folder contents table that contains summary information about all of its messages.</span></span>
    
- <span data-ttu-id="9992b-114">[Обзор папки "Входящие"](traversing-the-inbox-folder.md): в этой статье описывается цикл по всем сообщениям в папке "Входящие".</span><span class="sxs-lookup"><span data-stu-id="9992b-114">[Traversing the Inbox Folder](traversing-the-inbox-folder.md): Describes how to cycle through all the messages in the Inbox.</span></span>
    
- <span data-ttu-id="9992b-115">[Копирование или перемещение сообщения или папки](copying-or-moving-a-message-or-a-folder.md): инструкции по копированию или перемещению одного или нескольких сообщений.</span><span class="sxs-lookup"><span data-stu-id="9992b-115">[Copying or Moving a Message or a Folder](copying-or-moving-a-message-or-a-folder.md): Describes how to copy or move one or more messages.</span></span>
    
- <span data-ttu-id="9992b-116">[Открытие сообщения](opening-a-message.md): в этой статье описывается, как открыть сообщение.</span><span class="sxs-lookup"><span data-stu-id="9992b-116">[Opening a Message](opening-a-message.md): Describes how to open a message.</span></span>
    
- <span data-ttu-id="9992b-117">[Поиск значка сообщения](finding-the-icon-for-a-message.md): сведения о том, как найти значок, связанный с сообщением.</span><span class="sxs-lookup"><span data-stu-id="9992b-117">[Finding the Icon for a Message](finding-the-icon-for-a-message.md): Describes how to find an icon that is associated with a message.</span></span>
    
- <span data-ttu-id="9992b-118">[Открытие дескриптора представления](opening-a-view-descriptor.md): в этой статье описывается, как открыть дескриптор представления.</span><span class="sxs-lookup"><span data-stu-id="9992b-118">[Opening a View Descriptor](opening-a-view-descriptor.md): Describes how to open a view descriptor.</span></span>
    
- <span data-ttu-id="9992b-119">[Удаление сообщения](deleting-a-message.md): в этой статье описано, как удалить сообщение.</span><span class="sxs-lookup"><span data-stu-id="9992b-119">[Deleting a Message](deleting-a-message.md): Describes how to delete a message.</span></span>
    
- <span data-ttu-id="9992b-120">[Сохранение сообщения в папке "Входящие"](saving-a-message-in-the-inbox.md): сведения о том, как хранить сообщение в папке "Входящие".</span><span class="sxs-lookup"><span data-stu-id="9992b-120">[Saving a Message in the Inbox](saving-a-message-in-the-inbox.md): Describes how to store a message in the Inbox.</span></span>
    
- <span data-ttu-id="9992b-121">[Поиск отправленных или сохраненНых сообщений](finding-sent-or-saved-messages.md): сведения о поиске всех сохраненных или отправленных исходящих сообщений.</span><span class="sxs-lookup"><span data-stu-id="9992b-121">[Finding Sent or Saved Messages](finding-sent-or-saved-messages.md): Describes how to locate all outgoing messages that have been saved or sent.</span></span>
    
- <span data-ttu-id="9992b-122">[Отслеживание бесед](tracking-conversations.md): сведения о том, как отслеживать беседы.</span><span class="sxs-lookup"><span data-stu-id="9992b-122">[Tracking Conversations](tracking-conversations.md): Describes how to track conversations.</span></span>
    

