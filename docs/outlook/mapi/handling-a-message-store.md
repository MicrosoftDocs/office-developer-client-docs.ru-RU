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
ms.openlocfilehash: 0712407a7882c449c065cb6816694b4a1611036f
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22568471"
---
# <a name="handling-a-message-store"></a><span data-ttu-id="70447-103">Обработка хранилища сообщений</span><span class="sxs-lookup"><span data-stu-id="70447-103">Handling a message store</span></span>
  
<span data-ttu-id="70447-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="70447-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="70447-105">Обработка хранилища сообщений является важной частью любой клиент набор задач.</span><span class="sxs-lookup"><span data-stu-id="70447-105">Handling a message store is an important part of any client's set of tasks.</span></span> <span data-ttu-id="70447-106">Эти задачи включают открытие, копирование, перемещение, добавление и удаление папок и сообщений, отображение различных таблиц, установка свойств и управление уровнями доступа.</span><span class="sxs-lookup"><span data-stu-id="70447-106">These tasks include opening, copying, moving, adding, and deleting folders and messages, displaying various tables, setting properties, and controlling access levels.</span></span>

- <span data-ttu-id="70447-107">[Открытие хранилища сообщений](opening-a-message-store.md): Описание открытия одного или нескольких хранилищ сообщений во время сеанса.</span><span class="sxs-lookup"><span data-stu-id="70447-107">[Opening a Message Store](opening-a-message-store.md): Describes how to open one or more message stores during a session.</span></span>
    
- <span data-ttu-id="70447-108">[Открытие хранилище сообщений по умолчанию](opening-the-default-message-store.md): описывается, как открыть хранилище сообщений по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="70447-108">[Opening the Default Message Store](opening-the-default-message-store.md): Describes how to open the default message store.</span></span>
    
- <span data-ttu-id="70447-109">[Проверка и инициализации хранилища сообщений](validating-and-initializing-a-message-store.md): Описание способов инициализации и проверки хранилища сообщений.</span><span class="sxs-lookup"><span data-stu-id="70447-109">[Validating and Initializing a Message Store](validating-and-initializing-a-message-store.md): Describes how to initialize and validate a message store.</span></span>
    
- <span data-ttu-id="70447-110">[Поиск в хранилище сообщений](searching-a-message-store.md): описывается, как просмотреть одной или нескольких папок, поиск сообщений, которые соответствуют условиям поиска.</span><span class="sxs-lookup"><span data-stu-id="70447-110">[Searching a Message Store](searching-a-message-store.md): Describes how to look through one or more folders looking for messages that match search criteria.</span></span>
    
- <span data-ttu-id="70447-111">[При выборе папки получают](selecting-a-receive-folder.md): описываются шаги по созданию папки приема.</span><span class="sxs-lookup"><span data-stu-id="70447-111">[Selecting a Receive Folder](selecting-a-receive-folder.md): Describes the steps for creating a receive folder.</span></span>
    
- <span data-ttu-id="70447-112">[Открытие папки хранения сообщений](opening-a-message-store-folder.md): описывается, как открыть папку.</span><span class="sxs-lookup"><span data-stu-id="70447-112">[Opening a Message Store Folder](opening-a-message-store-folder.md): Describes how to open a folder.</span></span>
    
- <span data-ttu-id="70447-113">[Отображение Содержание папки](displaying-a-folder-contents-table.md): Описание способов отображения таблицы содержимое папки, которая содержит сводную информацию обо всех его сообщения.</span><span class="sxs-lookup"><span data-stu-id="70447-113">[Displaying a Folder Contents Table](displaying-a-folder-contents-table.md): Describes how to display the folder contents table that contains summary information about all of its messages.</span></span>
    
- <span data-ttu-id="70447-114">[Обход папки "Входящие"](traversing-the-inbox-folder.md): описывается, как выполнить переход по все сообщения в папке "Входящие".</span><span class="sxs-lookup"><span data-stu-id="70447-114">[Traversing the Inbox Folder](traversing-the-inbox-folder.md): Describes how to cycle through all the messages in the Inbox.</span></span>
    
- <span data-ttu-id="70447-115">[Копирование или перехода сообщение или папки](copying-or-moving-a-message-or-a-folder.md): описывается, как скопировать или переместить одно или несколько сообщений.</span><span class="sxs-lookup"><span data-stu-id="70447-115">[Copying or Moving a Message or a Folder](copying-or-moving-a-message-or-a-folder.md): Describes how to copy or move one or more messages.</span></span>
    
- <span data-ttu-id="70447-116">[Открытие сообщения](opening-a-message.md): описывается, как открыть сообщение.</span><span class="sxs-lookup"><span data-stu-id="70447-116">[Opening a Message](opening-a-message.md): Describes how to open a message.</span></span>
    
- <span data-ttu-id="70447-117">[Поиск значка для сообщения](finding-the-icon-for-a-message.md): описывается, как найти значок, который связан с сообщением.</span><span class="sxs-lookup"><span data-stu-id="70447-117">[Finding the Icon for a Message](finding-the-icon-for-a-message.md): Describes how to find an icon that is associated with a message.</span></span>
    
- <span data-ttu-id="70447-118">[Открытие представления дескриптора](opening-a-view-descriptor.md): описывается, как открыть дескриптор представления.</span><span class="sxs-lookup"><span data-stu-id="70447-118">[Opening a View Descriptor](opening-a-view-descriptor.md): Describes how to open a view descriptor.</span></span>
    
- <span data-ttu-id="70447-119">[Удаление сообщения](deleting-a-message.md): описывается, как удалить сообщение.</span><span class="sxs-lookup"><span data-stu-id="70447-119">[Deleting a Message](deleting-a-message.md): Describes how to delete a message.</span></span>
    
- <span data-ttu-id="70447-120">[Сохранение сообщения в папке "Входящие"](saving-a-message-in-the-inbox.md): описывается, как хранить сообщения в папке "Входящие".</span><span class="sxs-lookup"><span data-stu-id="70447-120">[Saving a Message in the Inbox](saving-a-message-in-the-inbox.md): Describes how to store a message in the Inbox.</span></span>
    
- <span data-ttu-id="70447-121">[Поиск отправленных или сохранения сообщений](finding-sent-or-saved-messages.md): описывается, как найти все исходящие сообщения, которые были сохранены или отправки.</span><span class="sxs-lookup"><span data-stu-id="70447-121">[Finding Sent or Saved Messages](finding-sent-or-saved-messages.md): Describes how to locate all outgoing messages that have been saved or sent.</span></span>
    
- <span data-ttu-id="70447-122">[Отслеживание бесед](tracking-conversations.md): Описание способов отслеживания бесед.</span><span class="sxs-lookup"><span data-stu-id="70447-122">[Tracking Conversations](tracking-conversations.md): Describes how to track conversations.</span></span>
    

