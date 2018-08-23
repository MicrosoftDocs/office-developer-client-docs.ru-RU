---
title: Отображение таблицу содержимого папки
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 14a4c123-776d-4a32-9688-8a4402dd1f53
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 51c88e8c062a409db305e893b82f43d8c8ac7094
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22580798"
---
# <a name="displaying-a-folder-contents-table"></a><span data-ttu-id="71500-103">Отображение таблицу содержимого папки</span><span class="sxs-lookup"><span data-stu-id="71500-103">Displaying a folder contents table</span></span>

<span data-ttu-id="71500-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="71500-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="71500-105">В таблице содержимое папки содержит сводную информацию обо всех его сообщения.</span><span class="sxs-lookup"><span data-stu-id="71500-105">The contents table of a folder contains summary information about all of its messages.</span></span> <span data-ttu-id="71500-106">В таблице содержимое папки получения для класса сообщения отображается сводная информация о новых входящих сообщений.</span><span class="sxs-lookup"><span data-stu-id="71500-106">Summary information about new incoming messages appears in the contents table of the receive folder for the message class.</span></span> <span data-ttu-id="71500-107">Чтобы сделать эту информацию для пользователей, получения таблицы и отображения столбцов и строк соответствующим образом.</span><span class="sxs-lookup"><span data-stu-id="71500-107">To make this information available to users, retrieve the table and display the columns and rows as appropriate.</span></span>
  
<span data-ttu-id="71500-108">**Для отображения содержимого папки**</span><span class="sxs-lookup"><span data-stu-id="71500-108">**To display a folder contents table**</span></span>
  
1. <span data-ttu-id="71500-109">Вызовите [IMsgStore::OpenEntry](imsgstore-openentry.md), передав идентификатор записи папки, содержащей таблицу.</span><span class="sxs-lookup"><span data-stu-id="71500-109">Call [IMsgStore::OpenEntry](imsgstore-openentry.md), passing the entry identifier of the folder containing the table.</span></span>
    
2. <span data-ttu-id="71500-110">Вызовите метод [IMAPIContainer::GetContentsTable](imapicontainer-getcontentstable.md) папки, чтобы открыть его содержимое в таблице.</span><span class="sxs-lookup"><span data-stu-id="71500-110">Call the folder's [IMAPIContainer::GetContentsTable](imapicontainer-getcontentstable.md) method to open its contents table.</span></span> 
    
3. <span data-ttu-id="71500-111">Ограничьте Просмотр содержимого таблицы при желании путем вызова метода [IMAPITable::SetColumns](imapitable-setcolumns.md) таблицы для указания определенных столбцов.</span><span class="sxs-lookup"><span data-stu-id="71500-111">Limit your view of the contents table if desired by calling the table's [IMAPITable::SetColumns](imapitable-setcolumns.md) method to specify particular columns.</span></span> 
    
4. <span data-ttu-id="71500-112">Ограничьте Просмотр содержимого таблицы при желании путем вызова метода [IMAPITable::Restrict](imapitable-restrict.md) таблицы для фильтрации конкретной строки.</span><span class="sxs-lookup"><span data-stu-id="71500-112">Limit your view of the contents table if desired by calling the table's [IMAPITable::Restrict](imapitable-restrict.md) method to filter particular rows.</span></span> <span data-ttu-id="71500-113">Если, например требуется показать только сообщения с определенным классом сообщения, для которых еще не требуется прочитать:</span><span class="sxs-lookup"><span data-stu-id="71500-113">If, for example, you want to show only messages with a specific message class that have yet to be read:</span></span> 
    
    1. <span data-ttu-id="71500-114">Создайте ограничение свойства в структуре [SPropertyRestriction](spropertyrestriction.md) , соответствующее свойство **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)) с помощью класса сообщений.</span><span class="sxs-lookup"><span data-stu-id="71500-114">Create a property restriction in an [SPropertyRestriction](spropertyrestriction.md) structure that matches the **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)) property with the desired message class.</span></span> 
        
    2. <span data-ttu-id="71500-115">Создайте ограничение битовой маски в структуре [SBitMaskRestriction](sbitmaskrestriction.md) , использующий **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) в качестве тега свойства и значения MSGFLAG_UNREAD как маски.</span><span class="sxs-lookup"><span data-stu-id="71500-115">Create a bitmask restriction in an [SBitMaskRestriction](sbitmaskrestriction.md) structure that uses **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) as the property tag and the MSGFLAG_UNREAD value as the mask.</span></span>
        
    3. <span data-ttu-id="71500-116">Создания ограничения в структуре [SAndRestriction](sandrestriction.md) , объединяющий ограничения свойств и битовую маску.</span><span class="sxs-lookup"><span data-stu-id="71500-116">Create a restriction in an [SAndRestriction](sandrestriction.md) structure that joins the property and bitmask restrictions.</span></span> 
    
5. <span data-ttu-id="71500-117">Сортировка в таблице содержимое при желании путем вызова метода [IMAPITable::SortTable](imapitable-sorttable.md) таблицы.</span><span class="sxs-lookup"><span data-stu-id="71500-117">Sort the contents table if desired by calling the table's [IMAPITable::SortTable](imapitable-sorttable.md) method.</span></span> 
    
6. <span data-ttu-id="71500-118">Вызовите [IMAPITable::QueryRows](imapitable-queryrows.md) , чтобы получить все строки из таблицы содержимого для обработки.</span><span class="sxs-lookup"><span data-stu-id="71500-118">Call [IMAPITable::QueryRows](imapitable-queryrows.md) to retrieve all of the rows from the contents table for processing.</span></span> 
    

