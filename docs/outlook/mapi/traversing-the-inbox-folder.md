---
title: Просмотр папки "Входящие"
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 2ad1459f-d59a-4784-94ea-4cad194e6e50
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: e954cb2d8029a31e7f69daaa7e8ed55a7953ac02
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32356583"
---
# <a name="traversing-the-inbox-folder"></a><span data-ttu-id="9ca5c-103">Просмотр папки "Входящие"</span><span class="sxs-lookup"><span data-stu-id="9ca5c-103">Traversing the Inbox Folder</span></span>

  
  
<span data-ttu-id="9ca5c-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9ca5c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
 <span data-ttu-id="9ca5c-105">**Циклическое переключение между всеми сообщениями в папке "Входящие"**</span><span class="sxs-lookup"><span data-stu-id="9ca5c-105">**To cycle through all of the messages in the Inbox**</span></span>
  
1. <span data-ttu-id="9ca5c-106">Call [IMsgStore:: жетрецеивефолдер](imsgstore-getreceivefolder.md) для получения идентификатора записи папки "Входящие".</span><span class="sxs-lookup"><span data-stu-id="9ca5c-106">Call [IMsgStore::GetReceiveFolder](imsgstore-getreceivefolder.md) to retrieve the entry identifier of the Inbox.</span></span> 
    
2. <span data-ttu-id="9ca5c-107">Call **IMAPIFolder:: OpenEntry** для открытия папки "Входящие".</span><span class="sxs-lookup"><span data-stu-id="9ca5c-107">Call **IMAPIFolder::OpenEntry** to open the Inbox.</span></span> 
    
3. <span data-ttu-id="9ca5c-108">ВыЗовите метод [IMAPIContainer:: жетконтентстабле](imapicontainer-getcontentstable.md) из папки "Входящие" для получения таблицы содержимого.</span><span class="sxs-lookup"><span data-stu-id="9ca5c-108">Call the Inbox's [IMAPIContainer::GetContentsTable](imapicontainer-getcontentstable.md) method to retrieve the contents table.</span></span> 
    
4. <span data-ttu-id="9ca5c-109">ВыЗовите таблицу содержимого, выЗовите метод [IMAPITable:: метода SetColumns](imapitable-setcolumns.md) , чтобы ограничить набор столбцов значением **пр_ентрид** ([PidTagEntryId](pidtagentryid-canonical-property.md)) и любыми другими нужными столбцами.</span><span class="sxs-lookup"><span data-stu-id="9ca5c-109">Call the contents table's [IMAPITable::SetColumns](imapitable-setcolumns.md) method to limit the column set to **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) and any other columns you require.</span></span> 
    
5. <span data-ttu-id="9ca5c-110">Call [IMAPITable:: QueryRows](imapitable-queryrows.md) , чтобы получить группу строк.</span><span class="sxs-lookup"><span data-stu-id="9ca5c-110">Call [IMAPITable::QueryRows](imapitable-queryrows.md) to retrieve a group of rows.</span></span> 
    
6. <span data-ttu-id="9ca5c-111">Пока в таблице содержимого больше нет строк:</span><span class="sxs-lookup"><span data-stu-id="9ca5c-111">Until there are no longer any rows in the contents table:</span></span>
    
1. <span data-ttu-id="9ca5c-112">Call [IMsgStore:: OpenEntry](imsgstore-openentry.md) , чтобы открыть сообщение, представленное идентификатором записи, из каждой строки.</span><span class="sxs-lookup"><span data-stu-id="9ca5c-112">Call [IMsgStore::OpenEntry](imsgstore-openentry.md) to open the message represented by the entry identifier from each row.</span></span> 
    
2. <span data-ttu-id="9ca5c-113">Назначьте параметр _лппунк_ указателю на локальный интерфейс **iMessage** .</span><span class="sxs-lookup"><span data-stu-id="9ca5c-113">Assign the  _lppUnk_ parameter to a local **IMessage** interface pointer.</span></span> 
    
3. <span data-ttu-id="9ca5c-114">Работать со свойствами сообщения.</span><span class="sxs-lookup"><span data-stu-id="9ca5c-114">Work with the properties of the message.</span></span>
    
4. <span data-ttu-id="9ca5c-115">ОтПустите указатель, на который указывает параметр _лппунк_ .</span><span class="sxs-lookup"><span data-stu-id="9ca5c-115">Release the pointer pointed to by the  _lppUnk_ parameter.</span></span> 
    
5. <span data-ttu-id="9ca5c-116">Call [IMAPITable:: QueryRows](imapitable-queryrows.md) для получения следующей группы строк.</span><span class="sxs-lookup"><span data-stu-id="9ca5c-116">Call [IMAPITable::QueryRows](imapitable-queryrows.md) to retrieve the next group of rows.</span></span> 
    
7. <span data-ttu-id="9ca5c-117">Освободите таблицу содержимого.</span><span class="sxs-lookup"><span data-stu-id="9ca5c-117">Release the contents table.</span></span>
    

