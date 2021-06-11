---
title: Отображение таблицы содержимого папки
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 14a4c123-776d-4a32-9688-8a4402dd1f53
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 56847283afaf41c1d45cdb875ddf49eaa5881175
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412396"
---
# <a name="displaying-a-folder-contents-table"></a><span data-ttu-id="a4203-103">Отображение таблицы содержимого папки</span><span class="sxs-lookup"><span data-stu-id="a4203-103">Displaying a folder contents table</span></span>

<span data-ttu-id="a4203-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a4203-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a4203-105">В таблице содержимого папки содержатся сводные сведения обо всех ее сообщениях.</span><span class="sxs-lookup"><span data-stu-id="a4203-105">The contents table of a folder contains summary information about all of its messages.</span></span> <span data-ttu-id="a4203-106">Сводная информация о новых входящих сообщениях отображается в таблице содержимого папки получения для класса сообщений.</span><span class="sxs-lookup"><span data-stu-id="a4203-106">Summary information about new incoming messages appears in the contents table of the receive folder for the message class.</span></span> <span data-ttu-id="a4203-107">Чтобы сделать эти сведения доступными для пользователей, извлекаем таблицу и отображаем столбцы и строки по мере необходимости.</span><span class="sxs-lookup"><span data-stu-id="a4203-107">To make this information available to users, retrieve the table and display the columns and rows as appropriate.</span></span>
  
<span data-ttu-id="a4203-108">**Отображение таблицы содержимого папки**</span><span class="sxs-lookup"><span data-stu-id="a4203-108">**To display a folder contents table**</span></span>
  
1. <span data-ttu-id="a4203-109">Позвоните [в IMsgStore::OpenEntry,](imsgstore-openentry.md)передав идентификатор записи папки, содержащей таблицу.</span><span class="sxs-lookup"><span data-stu-id="a4203-109">Call [IMsgStore::OpenEntry](imsgstore-openentry.md), passing the entry identifier of the folder containing the table.</span></span>
    
2. <span data-ttu-id="a4203-110">Чтобы открыть таблицу содержимого, вызовите метод [IMAPIContainer::GetContentsTable.](imapicontainer-getcontentstable.md)</span><span class="sxs-lookup"><span data-stu-id="a4203-110">Call the folder's [IMAPIContainer::GetContentsTable](imapicontainer-getcontentstable.md) method to open its contents table.</span></span> 
    
3. <span data-ttu-id="a4203-111">Ограничить представление таблицы содержимого при желании, назвав метод [IMAPITable::SetColumns](imapitable-setcolumns.md) для указания определенных столбцов.</span><span class="sxs-lookup"><span data-stu-id="a4203-111">Limit your view of the contents table if desired by calling the table's [IMAPITable::SetColumns](imapitable-setcolumns.md) method to specify particular columns.</span></span> 
    
4. <span data-ttu-id="a4203-112">Ограничите представление таблицы содержимого при желании, назвав метод [IMAPITable:::Limit](imapitable-restrict.md) для фильтрации определенных строк.</span><span class="sxs-lookup"><span data-stu-id="a4203-112">Limit your view of the contents table if desired by calling the table's [IMAPITable::Restrict](imapitable-restrict.md) method to filter particular rows.</span></span> <span data-ttu-id="a4203-113">Если, например, необходимо показывать только сообщения с определенным классом сообщений, которые еще не прочитано:</span><span class="sxs-lookup"><span data-stu-id="a4203-113">If, for example, you want to show only messages with a specific message class that have yet to be read:</span></span> 
    
    1. <span data-ttu-id="a4203-114">Создайте ограничение свойств в структуре [SPropertyRestriction,](spropertyrestriction.md) которое соответствует **свойству PR_MESSAGE_CLASS** [(PidTagMessageClass)](pidtagmessageclass-canonical-property.md)с нужным классом сообщений.</span><span class="sxs-lookup"><span data-stu-id="a4203-114">Create a property restriction in an [SPropertyRestriction](spropertyrestriction.md) structure that matches the **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)) property with the desired message class.</span></span> 
        
    2. <span data-ttu-id="a4203-115">Создайте ограничение битмаски в структуре [SBitMaskRestriction,](sbitmaskrestriction.md) которая использует **PR_MESSAGE_FLAGS** [(PidTagMessageFlags)](pidtagmessageflags-canonical-property.md)в качестве тега свойства и MSGFLAG_UNREAD в качестве маски.</span><span class="sxs-lookup"><span data-stu-id="a4203-115">Create a bitmask restriction in an [SBitMaskRestriction](sbitmaskrestriction.md) structure that uses **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) as the property tag and the MSGFLAG_UNREAD value as the mask.</span></span>
        
    3. <span data-ttu-id="a4203-116">Создайте ограничение в [структуре SAndRestriction,](sandrestriction.md) которая присоединяется к ограничениям свойства и bitmask.</span><span class="sxs-lookup"><span data-stu-id="a4203-116">Create a restriction in an [SAndRestriction](sandrestriction.md) structure that joins the property and bitmask restrictions.</span></span> 
    
5. <span data-ttu-id="a4203-117">Сортировка таблицы содержимого при желании путем вызова метода [IMAPITable::SortTable таблицы.](imapitable-sorttable.md)</span><span class="sxs-lookup"><span data-stu-id="a4203-117">Sort the contents table if desired by calling the table's [IMAPITable::SortTable](imapitable-sorttable.md) method.</span></span> 
    
6. <span data-ttu-id="a4203-118">Вызов [IMAPITable::QueryRows](imapitable-queryrows.md) для получения всех строк из таблицы содержимого для обработки.</span><span class="sxs-lookup"><span data-stu-id="a4203-118">Call [IMAPITable::QueryRows](imapitable-queryrows.md) to retrieve all of the rows from the contents table for processing.</span></span> 
    

