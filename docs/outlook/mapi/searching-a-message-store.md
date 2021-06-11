---
title: Поиск в хранилище сообщений
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 9e8d4639-7507-4d98-b56f-a65be369dc40
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 7240f49a15fdaea4d1f30dae578d25c3f2c1c0f3
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33426039"
---
# <a name="searching-a-message-store"></a><span data-ttu-id="cf335-103">Поиск в хранилище сообщений</span><span class="sxs-lookup"><span data-stu-id="cf335-103">Searching a message store</span></span>

<span data-ttu-id="cf335-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="cf335-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="cf335-105">Клиентские приложения могут искать сообщения в одной или несколько папок, которые соответствуют критериям поиска.</span><span class="sxs-lookup"><span data-stu-id="cf335-105">Client applications can search through one or more folders looking for messages that match search criteria.</span></span> <span data-ttu-id="cf335-106">Самый простой метод поиска предполагает применение ограничения для определения критериев и размещение результатов в папку результатов поиска, созданную явно для этого поиска или для предварительного поиска.</span><span class="sxs-lookup"><span data-stu-id="cf335-106">The most straightforward search technique involves applying a restriction to define criteria and placing the results into a search-results folder, created explicitly for this search or for a prior search.</span></span> <span data-ttu-id="cf335-107">Не все хранилища сообщений поддерживают этот метод.</span><span class="sxs-lookup"><span data-stu-id="cf335-107">Not all message stores support this technique.</span></span> 

<span data-ttu-id="cf335-108">Чтобы определить, используется ли хранилище сообщений с помощью папок результатов поиска, позвоните по методу [IMAPIProp::GetProps](imapiprop-getprops.md) для получения свойства PR **\_ STORE_SUPPORT_MASK** [(PidTagStoreSupportMask).](pidtagstoresupportmask-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="cf335-108">To determine whether or not the message store you are using supports using search-results folders, call its [IMAPIProp::GetProps](imapiprop-getprops.md) method to retrieve the **PR\_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) property.</span></span> <span data-ttu-id="cf335-109">Если установлен STORE_SEARCH_OK флаг, поиск поддерживается.</span><span class="sxs-lookup"><span data-stu-id="cf335-109">If the STORE_SEARCH_OK flag is set, searching is supported.</span></span> <span data-ttu-id="cf335-110">Если она не установлена, вам потребуется альтернативный подход, например ручная проверка целевых папок.</span><span class="sxs-lookup"><span data-stu-id="cf335-110">If it is not set, you'll need an alternate approach such as manually inspecting the target folders.</span></span>
  
### <a name="to-search-one-or-more-folders-in-a-message-store"></a><span data-ttu-id="cf335-111">Поиск одной или более папок в хранилище сообщений</span><span class="sxs-lookup"><span data-stu-id="cf335-111">To search one or more folders in a message store</span></span>
  
1. <span data-ttu-id="cf335-112">Если у вас есть папка результатов поиска из предыдущего поиска, пропустите шаг 2.</span><span class="sxs-lookup"><span data-stu-id="cf335-112">If you have a search-results folder from a previous search, skip to step 2.</span></span> <span data-ttu-id="cf335-113">В противном случае для создания папки результатов поиска:</span><span class="sxs-lookup"><span data-stu-id="cf335-113">Otherwise, to create a search-results folder:</span></span>
    
    1. <span data-ttu-id="cf335-114">Извлечение идентификатора записи для корневой папки результатов поиска путем вызова метода [IMAPIProp::GetProps](imapiprop-getprops.md) магазина сообщений и запроса PR_FINDER_ENTRYID[(PidTagFinderEntryId).](pidtagfinderentryid-canonical-property.md) </span><span class="sxs-lookup"><span data-stu-id="cf335-114">Retrieve the entry identifier for the search-results root folder by calling the message store's [IMAPIProp::GetProps](imapiprop-getprops.md) method and requesting **PR_FINDER_ENTRYID** ([PidTagFinderEntryId](pidtagfinderentryid-canonical-property.md)).</span></span>
        
    2. <span data-ttu-id="cf335-115">Позвоните [в IMsgStore::OpenEntry,](imsgstore-openentry.md) чтобы открыть папку, представленную PR_FINDER_ENTRYID.</span><span class="sxs-lookup"><span data-stu-id="cf335-115">Call [IMsgStore::OpenEntry](imsgstore-openentry.md) to open the folder represented by PR_FINDER_ENTRYID.</span></span> 
        
    3. <span data-ttu-id="cf335-116">Вызов метода [IMAPIFolder::CreateFolder](imapifolder-createfolder.md) для создания папки результатов поиска с FOLDER_SEARCH флагом.</span><span class="sxs-lookup"><span data-stu-id="cf335-116">Call the folder's [IMAPIFolder::CreateFolder](imapifolder-createfolder.md) method to create a search-results folder with the FOLDER_SEARCH flag set.</span></span> 
    
2. <span data-ttu-id="cf335-117">Создайте ограничение для удержания критериев поиска.</span><span class="sxs-lookup"><span data-stu-id="cf335-117">Build a restriction to hold your search criteria.</span></span> 
    
3. <span data-ttu-id="cf335-118">Создайте массив идентификаторов записей, которые представляют папки для поиска.</span><span class="sxs-lookup"><span data-stu-id="cf335-118">Create an array of entry identifiers that represent the folders to search.</span></span> <span data-ttu-id="cf335-119">Этот шаг не является необходимым, если папка результатов поиска была использована ранее, и вы хотите искать те же папки.</span><span class="sxs-lookup"><span data-stu-id="cf335-119">This step is unnecessary if the search-results folder has been used before and you want to search the same folders.</span></span>
    
4. <span data-ttu-id="cf335-120">Вызовите метод [IMAPIContainer::SetSearchCriteria,](imapicontainer-setsearchcriteria.md) указав  _lpContainerList_ на массив идентификатора входа и  _lpRestriction_ к ограничению.</span><span class="sxs-lookup"><span data-stu-id="cf335-120">Call the search-results folder's [IMAPIContainer::SetSearchCriteria](imapicontainer-setsearchcriteria.md) method, pointing  _lpContainerList_ to the entry identifier array and  _lpRestriction_ to the restriction.</span></span> 
    
5. <span data-ttu-id="cf335-121">Если вы зарегистрировались для поиска полных уведомлений в хранилище сообщений, дождись прибытия уведомления.</span><span class="sxs-lookup"><span data-stu-id="cf335-121">If you have registered for search complete notifications with the message store, wait for the notification to arrive.</span></span>
    
6. <span data-ttu-id="cf335-122">Просмотр результатов поиска с помощью метода [IMAPIContainer::GetContentsTable](imapicontainer-getcontentstable.md) для доступа к его таблице содержимого.</span><span class="sxs-lookup"><span data-stu-id="cf335-122">View the results of the search by calling the search-results folder's [IMAPIContainer::GetContentsTable](imapicontainer-getcontentstable.md) method to access its contents table.</span></span> 
    
7. <span data-ttu-id="cf335-123">Для получения сообщений, удовлетворяющих критериям поиска, вызовите метод [IMAPITable::QueryRows](imapitable-queryrows.md) таблицы содержимого.</span><span class="sxs-lookup"><span data-stu-id="cf335-123">Call the contents table's [IMAPITable::QueryRows](imapitable-queryrows.md) method to retrieve the messages that satisfy the search criteria.</span></span> 
    

