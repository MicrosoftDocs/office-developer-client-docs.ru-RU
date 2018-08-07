---
title: Поиск хранилища сообщений
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 9e8d4639-7507-4d98-b56f-a65be369dc40
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 90ed7da43d7f9e5e8b5f3024f1eee99a2d7a2b5c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19812225"
---
# <a name="searching-a-message-store"></a><span data-ttu-id="9fac5-103">Поиск хранилища сообщений</span><span class="sxs-lookup"><span data-stu-id="9fac5-103">Searching a message store</span></span>

<span data-ttu-id="9fac5-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="9fac5-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="9fac5-105">Клиентские приложения могут выполнять поиск по одной или нескольких папок, поиск сообщений, которые соответствуют условиям поиска.</span><span class="sxs-lookup"><span data-stu-id="9fac5-105">Client applications can search through one or more folders looking for messages that match search criteria.</span></span> <span data-ttu-id="9fac5-106">Самый простой способ поиска включает применение ограничения для определения условий и помещает результаты в папку результатов поиска, созданные явным образом для поиска или для предыдущего поиска.</span><span class="sxs-lookup"><span data-stu-id="9fac5-106">The most straightforward search technique involves applying a restriction to define criteria and placing the results into a search-results folder, created explicitly for this search or for a prior search.</span></span> <span data-ttu-id="9fac5-107">Не все хранилища сообщений поддерживает этот метод.</span><span class="sxs-lookup"><span data-stu-id="9fac5-107">Not all message stores support this technique.</span></span> 

<span data-ttu-id="9fac5-108">Для определения того, является ли хранилище сообщений используется поддерживает использование результатов поиска папок, вызвать его метод [IMAPIProp::GetProps](imapiprop-getprops.md) для получения **связей с Общественностью\_STORE_SUPPORT_MASK** свойство ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="9fac5-108">To determine whether or not the message store you are using supports using search-results folders, call its [IMAPIProp::GetProps](imapiprop-getprops.md) method to retrieve the **PR\_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) property.</span></span> <span data-ttu-id="9fac5-109">Если установлен флаг STORE_SEARCH_OK, поддерживается поиск.</span><span class="sxs-lookup"><span data-stu-id="9fac5-109">If the STORE_SEARCH_OK flag is set, searching is supported.</span></span> <span data-ttu-id="9fac5-110">Если не задано, то необходимо альтернативный подход, такие как вручную проверкой целевые папки.</span><span class="sxs-lookup"><span data-stu-id="9fac5-110">If it is not set, you'll need an alternate approach such as manually inspecting the target folders.</span></span>
  
### <a name="to-search-one-or-more-folders-in-a-message-store"></a><span data-ttu-id="9fac5-111">Для поиска одного или нескольких папок в хранилище сообщений</span><span class="sxs-lookup"><span data-stu-id="9fac5-111">To search one or more folders in a message store</span></span>
  
1. <span data-ttu-id="9fac5-112">Если у вас есть папка результатов поиска из предыдущего поиска, перейдите к шагу 2.</span><span class="sxs-lookup"><span data-stu-id="9fac5-112">If you have a search-results folder from a previous search, skip to step 2.</span></span> <span data-ttu-id="9fac5-113">В противном случае — создание папки результатов поиска:</span><span class="sxs-lookup"><span data-stu-id="9fac5-113">Otherwise, to create a search-results folder:</span></span>
    
    1. <span data-ttu-id="9fac5-114">Получите идентификатор записи на корневую папку результатов поиска путем вызова метода [IMAPIProp::GetProps](imapiprop-getprops.md) хранилища сообщений и разрешения на запрос **PR_FINDER_ENTRYID** ([PidTagFinderEntryId](pidtagfinderentryid-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="9fac5-114">Retrieve the entry identifier for the search-results root folder by calling the message store's [IMAPIProp::GetProps](imapiprop-getprops.md) method and requesting **PR_FINDER_ENTRYID** ([PidTagFinderEntryId](pidtagfinderentryid-canonical-property.md)).</span></span>
        
    2. <span data-ttu-id="9fac5-115">Вызовите [IMsgStore::OpenEntry](imsgstore-openentry.md) , чтобы открыть папку, представленного PR_FINDER_ENTRYID.</span><span class="sxs-lookup"><span data-stu-id="9fac5-115">Call [IMsgStore::OpenEntry](imsgstore-openentry.md) to open the folder represented by PR_FINDER_ENTRYID.</span></span> 
        
    3. <span data-ttu-id="9fac5-116">Вызов метода [IMAPIFolder::CreateFolder](imapifolder-createfolder.md) папки для создания папки результатов поиска с установленным флагом FOLDER_SEARCH.</span><span class="sxs-lookup"><span data-stu-id="9fac5-116">Call the folder's [IMAPIFolder::CreateFolder](imapifolder-createfolder.md) method to create a search-results folder with the FOLDER_SEARCH flag set.</span></span> 
    
2. <span data-ttu-id="9fac5-117">Создание ограничения для хранения условиям поиска.</span><span class="sxs-lookup"><span data-stu-id="9fac5-117">Build a restriction to hold your search criteria.</span></span> 
    
3. <span data-ttu-id="9fac5-118">Создайте массив идентификаторов записи, представляющие папки для поиска.</span><span class="sxs-lookup"><span data-stu-id="9fac5-118">Create an array of entry identifiers that represent the folders to search.</span></span> <span data-ttu-id="9fac5-119">Этот шаг можно пропустить, если раньше папка результатов поиска, и вы хотите найти те же папки.</span><span class="sxs-lookup"><span data-stu-id="9fac5-119">This step is unnecessary if the search-results folder has been used before and you want to search the same folders.</span></span>
    
4. <span data-ttu-id="9fac5-120">Вызовите метод [IMAPIContainer::SetSearchCriteria](imapicontainer-setsearchcriteria.md) папка результатов поиска, с указанием _lpContainerList_ запись идентификатор массива и _lpRestriction_ ограничения.</span><span class="sxs-lookup"><span data-stu-id="9fac5-120">Call the search-results folder's [IMAPIContainer::SetSearchCriteria](imapicontainer-setsearchcriteria.md) method, pointing  _lpContainerList_ to the entry identifier array and  _lpRestriction_ to the restriction.</span></span> 
    
5. <span data-ttu-id="9fac5-121">Если вы зарегистрировали уведомлений завершения поиска с хранилища сообщений, ожидание уведомления поступления.</span><span class="sxs-lookup"><span data-stu-id="9fac5-121">If you have registered for search complete notifications with the message store, wait for the notification to arrive.</span></span>
    
6. <span data-ttu-id="9fac5-122">Просмотр результатов поиска путем вызова метода [IMAPIContainer::GetContentsTable](imapicontainer-getcontentstable.md) папки для доступа к его содержимое в таблице результатов поиска.</span><span class="sxs-lookup"><span data-stu-id="9fac5-122">View the results of the search by calling the search-results folder's [IMAPIContainer::GetContentsTable](imapicontainer-getcontentstable.md) method to access its contents table.</span></span> 
    
7. <span data-ttu-id="9fac5-123">Метод содержимое таблицы [IMAPITable::QueryRows](imapitable-queryrows.md) для получения сообщений, соответствующих критериям поиска.</span><span class="sxs-lookup"><span data-stu-id="9fac5-123">Call the contents table's [IMAPITable::QueryRows](imapitable-queryrows.md) method to retrieve the messages that satisfy the search criteria.</span></span> 
    

