---
title: Обход папки "Входящие"
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 2ad1459f-d59a-4784-94ea-4cad194e6e50
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: e954cb2d8029a31e7f69daaa7e8ed55a7953ac02
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33406558"
---
# <a name="traversing-the-inbox-folder"></a><span data-ttu-id="fa3ea-103">Обход папки "Входящие"</span><span class="sxs-lookup"><span data-stu-id="fa3ea-103">Traversing the Inbox Folder</span></span>

  
  
<span data-ttu-id="fa3ea-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="fa3ea-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
 <span data-ttu-id="fa3ea-105">**Циклия всех сообщений в почтовой ящике**</span><span class="sxs-lookup"><span data-stu-id="fa3ea-105">**To cycle through all of the messages in the Inbox**</span></span>
  
1. <span data-ttu-id="fa3ea-106">Вызовите [IMsgStore::GetReceiveFolder,](imsgstore-getreceivefolder.md) чтобы получить идентификатор записи для входящих сообщений.</span><span class="sxs-lookup"><span data-stu-id="fa3ea-106">Call [IMsgStore::GetReceiveFolder](imsgstore-getreceivefolder.md) to retrieve the entry identifier of the Inbox.</span></span> 
    
2. <span data-ttu-id="fa3ea-107">Вызовите **IMAPIFolder::OpenEntry,** чтобы открыть "Входящие".</span><span class="sxs-lookup"><span data-stu-id="fa3ea-107">Call **IMAPIFolder::OpenEntry** to open the Inbox.</span></span> 
    
3. <span data-ttu-id="fa3ea-108">Вызовите метод [IMAPIContainer::GetContentsTable](imapicontainer-getcontentstable.md) для извлечения таблицы содержимого.</span><span class="sxs-lookup"><span data-stu-id="fa3ea-108">Call the Inbox's [IMAPIContainer::GetContentsTable](imapicontainer-getcontentstable.md) method to retrieve the contents table.</span></span> 
    
4. <span data-ttu-id="fa3ea-109">Вызовите метод [IMAPITable::SetColumns](imapitable-setcolumns.md) таблицы содержимого, чтобы ограничить набор столбцов PR_ENTRYID **(** [PidTagEntryId)](pidtagentryid-canonical-property.md)и любыми другими требуемыми столбцами.</span><span class="sxs-lookup"><span data-stu-id="fa3ea-109">Call the contents table's [IMAPITable::SetColumns](imapitable-setcolumns.md) method to limit the column set to **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) and any other columns you require.</span></span> 
    
5. <span data-ttu-id="fa3ea-110">Вызов [IMAPITable::QueryRows](imapitable-queryrows.md) для получения группы строк.</span><span class="sxs-lookup"><span data-stu-id="fa3ea-110">Call [IMAPITable::QueryRows](imapitable-queryrows.md) to retrieve a group of rows.</span></span> 
    
6. <span data-ttu-id="fa3ea-111">Пока в таблице содержимого больше нет строк:</span><span class="sxs-lookup"><span data-stu-id="fa3ea-111">Until there are no longer any rows in the contents table:</span></span>
    
1. <span data-ttu-id="fa3ea-112">Вызовите [IMsgStore::OpenEntry,](imsgstore-openentry.md) чтобы открыть сообщение, представленное идентификатором записи из каждой строки.</span><span class="sxs-lookup"><span data-stu-id="fa3ea-112">Call [IMsgStore::OpenEntry](imsgstore-openentry.md) to open the message represented by the entry identifier from each row.</span></span> 
    
2. <span data-ttu-id="fa3ea-113">_Назначьте параметр lppUnk_ локальному указателю интерфейса **IMessage.**</span><span class="sxs-lookup"><span data-stu-id="fa3ea-113">Assign the  _lppUnk_ parameter to a local **IMessage** interface pointer.</span></span> 
    
3. <span data-ttu-id="fa3ea-114">Работа со свойствами сообщения.</span><span class="sxs-lookup"><span data-stu-id="fa3ea-114">Work with the properties of the message.</span></span>
    
4. <span data-ttu-id="fa3ea-115">Отпустите указатель, на который указывает параметр _lppUnk._</span><span class="sxs-lookup"><span data-stu-id="fa3ea-115">Release the pointer pointed to by the  _lppUnk_ parameter.</span></span> 
    
5. <span data-ttu-id="fa3ea-116">Вызовите [IMAPITable::QueryRows,](imapitable-queryrows.md) чтобы получить следующую группу строк.</span><span class="sxs-lookup"><span data-stu-id="fa3ea-116">Call [IMAPITable::QueryRows](imapitable-queryrows.md) to retrieve the next group of rows.</span></span> 
    
7. <span data-ttu-id="fa3ea-117">Отпустите таблицу содержимого.</span><span class="sxs-lookup"><span data-stu-id="fa3ea-117">Release the contents table.</span></span>
    

