---
title: Навигация по папке "Входящие"
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 2ad1459f-d59a-4784-94ea-4cad194e6e50
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 87fcde5a28a30f08bc2fd5f28fb692a4b4251fbf
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19812516"
---
# <a name="traversing-the-inbox-folder"></a><span data-ttu-id="53d35-103">Навигация по папке "Входящие"</span><span class="sxs-lookup"><span data-stu-id="53d35-103">Traversing the Inbox Folder</span></span>

  
  
<span data-ttu-id="53d35-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="53d35-104">**Applies to**: Outlook</span></span> 
  
 <span data-ttu-id="53d35-105">**Чтобы просмотреть все сообщения в папке "Входящие"**</span><span class="sxs-lookup"><span data-stu-id="53d35-105">**To cycle through all of the messages in the Inbox**</span></span>
  
1. <span data-ttu-id="53d35-106">Вызовите [IMsgStore::GetReceiveFolder](imsgstore-getreceivefolder.md) , чтобы получить идентификатор записи из папки «Входящие».</span><span class="sxs-lookup"><span data-stu-id="53d35-106">Call [IMsgStore::GetReceiveFolder](imsgstore-getreceivefolder.md) to retrieve the entry identifier of the Inbox.</span></span> 
    
2. <span data-ttu-id="53d35-107">Вызовите **IMAPIFolder::OpenEntry** , чтобы открыть папку "Входящие".</span><span class="sxs-lookup"><span data-stu-id="53d35-107">Call **IMAPIFolder::OpenEntry** to open the Inbox.</span></span> 
    
3. <span data-ttu-id="53d35-108">Вызов метода [IMAPIContainer::GetContentsTable](imapicontainer-getcontentstable.md) папке "Входящие" для получения содержимого таблицы.</span><span class="sxs-lookup"><span data-stu-id="53d35-108">Call the Inbox's [IMAPIContainer::GetContentsTable](imapicontainer-getcontentstable.md) method to retrieve the contents table.</span></span> 
    
4. <span data-ttu-id="53d35-109">Вызовите метод [IMAPITable::SetColumns](imapitable-setcolumns.md) таблицы для ограничения столбец, задайте значение **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) и другие столбцы, которые требуется содержимое.</span><span class="sxs-lookup"><span data-stu-id="53d35-109">Call the contents table's [IMAPITable::SetColumns](imapitable-setcolumns.md) method to limit the column set to **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) and any other columns you require.</span></span> 
    
5. <span data-ttu-id="53d35-110">Вызов [IMAPITable::QueryRows](imapitable-queryrows.md) для извлечения группы строк.</span><span class="sxs-lookup"><span data-stu-id="53d35-110">Call [IMAPITable::QueryRows](imapitable-queryrows.md) to retrieve a group of rows.</span></span> 
    
6. <span data-ttu-id="53d35-111">Пока не больше не существует все строки в таблице содержимого:</span><span class="sxs-lookup"><span data-stu-id="53d35-111">Until there are no longer any rows in the contents table:</span></span>
    
1. <span data-ttu-id="53d35-112">Вызовите [IMsgStore::OpenEntry](imsgstore-openentry.md) , чтобы открыть сообщение, представленное идентификатор записи из каждой строки.</span><span class="sxs-lookup"><span data-stu-id="53d35-112">Call [IMsgStore::OpenEntry](imsgstore-openentry.md) to open the message represented by the entry identifier from each row.</span></span> 
    
2. <span data-ttu-id="53d35-113">Назначьте параметр _lppUnk_ локального указатель интерфейса **IMessage** .</span><span class="sxs-lookup"><span data-stu-id="53d35-113">Assign the  _lppUnk_ parameter to a local **IMessage** interface pointer.</span></span> 
    
3. <span data-ttu-id="53d35-114">Работа со свойствами сообщения.</span><span class="sxs-lookup"><span data-stu-id="53d35-114">Work with the properties of the message.</span></span>
    
4. <span data-ttu-id="53d35-115">Выпуск указатель, на который указывает параметр _lppUnk_ .</span><span class="sxs-lookup"><span data-stu-id="53d35-115">Release the pointer pointed to by the  _lppUnk_ parameter.</span></span> 
    
5. <span data-ttu-id="53d35-116">Вызов [IMAPITable::QueryRows](imapitable-queryrows.md) для получения следующей группы строк.</span><span class="sxs-lookup"><span data-stu-id="53d35-116">Call [IMAPITable::QueryRows](imapitable-queryrows.md) to retrieve the next group of rows.</span></span> 
    
7. <span data-ttu-id="53d35-117">Выпуск таблицу содержимого.</span><span class="sxs-lookup"><span data-stu-id="53d35-117">Release the contents table.</span></span>
    

