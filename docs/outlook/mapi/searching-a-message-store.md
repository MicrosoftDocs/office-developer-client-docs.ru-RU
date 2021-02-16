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
# <a name="searching-a-message-store"></a><span data-ttu-id="4d3b1-103">Поиск в хранилище сообщений</span><span class="sxs-lookup"><span data-stu-id="4d3b1-103">Searching a message store</span></span>

<span data-ttu-id="4d3b1-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4d3b1-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4d3b1-105">Клиентские приложения могут искать сообщения, которые соответствуют условиям поиска, в одной или более папках.</span><span class="sxs-lookup"><span data-stu-id="4d3b1-105">Client applications can search through one or more folders looking for messages that match search criteria.</span></span> <span data-ttu-id="4d3b1-106">Самый простой способ поиска включает применение ограничения для определения критериев и помещение результатов в папку результатов поиска, созданную явно для этого поиска или для предыдущего поиска.</span><span class="sxs-lookup"><span data-stu-id="4d3b1-106">The most straightforward search technique involves applying a restriction to define criteria and placing the results into a search-results folder, created explicitly for this search or for a prior search.</span></span> <span data-ttu-id="4d3b1-107">Не все хранилища сообщений поддерживают этот метод.</span><span class="sxs-lookup"><span data-stu-id="4d3b1-107">Not all message stores support this technique.</span></span> 

<span data-ttu-id="4d3b1-108">Чтобы определить, поддерживает ли используемное хранилище сообщений использование папок результатов поиска, вызовите его метод [IMAPIProp::GetProps,](imapiprop-getprops.md) чтобы получить **свойство PR \_ STORE_SUPPORT_MASK** ([PidTagStoreSupportMask).](pidtagstoresupportmask-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="4d3b1-108">To determine whether or not the message store you are using supports using search-results folders, call its [IMAPIProp::GetProps](imapiprop-getprops.md) method to retrieve the **PR\_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) property.</span></span> <span data-ttu-id="4d3b1-109">Если установлен STORE_SEARCH_OK флага, поиск поддерживается.</span><span class="sxs-lookup"><span data-stu-id="4d3b1-109">If the STORE_SEARCH_OK flag is set, searching is supported.</span></span> <span data-ttu-id="4d3b1-110">Если он не установлен, вам потребуется альтернативный подход, например проверка целевых папок вручную.</span><span class="sxs-lookup"><span data-stu-id="4d3b1-110">If it is not set, you'll need an alternate approach such as manually inspecting the target folders.</span></span>
  
### <a name="to-search-one-or-more-folders-in-a-message-store"></a><span data-ttu-id="4d3b1-111">Поиск в одной или более папках в хранилище сообщений</span><span class="sxs-lookup"><span data-stu-id="4d3b1-111">To search one or more folders in a message store</span></span>
  
1. <span data-ttu-id="4d3b1-112">Если у вас есть папка результатов поиска из предыдущего поиска, переперейти к шагу 2.</span><span class="sxs-lookup"><span data-stu-id="4d3b1-112">If you have a search-results folder from a previous search, skip to step 2.</span></span> <span data-ttu-id="4d3b1-113">В противном случае создайте папку результатов поиска:</span><span class="sxs-lookup"><span data-stu-id="4d3b1-113">Otherwise, to create a search-results folder:</span></span>
    
    1. <span data-ttu-id="4d3b1-114">Получите идентификатор записи для корневой папки результатов поиска, вызывая метод [IMAPIProp::GetProps](imapiprop-getprops.md) в хранилище сообщений и запрашивая **PR_FINDER_ENTRYID** ([PidTagFinderEntryId).](pidtagfinderentryid-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="4d3b1-114">Retrieve the entry identifier for the search-results root folder by calling the message store's [IMAPIProp::GetProps](imapiprop-getprops.md) method and requesting **PR_FINDER_ENTRYID** ([PidTagFinderEntryId](pidtagfinderentryid-canonical-property.md)).</span></span>
        
    2. <span data-ttu-id="4d3b1-115">Вызовите [IMsgStore::OpenEntry,](imsgstore-openentry.md) чтобы открыть папку, представленную PR_FINDER_ENTRYID.</span><span class="sxs-lookup"><span data-stu-id="4d3b1-115">Call [IMsgStore::OpenEntry](imsgstore-openentry.md) to open the folder represented by PR_FINDER_ENTRYID.</span></span> 
        
    3. <span data-ttu-id="4d3b1-116">Вызовите метод [IMAPIFolder::CreateFolder](imapifolder-createfolder.md) папки результатов поиска с установленным FOLDER_SEARCH флагом.</span><span class="sxs-lookup"><span data-stu-id="4d3b1-116">Call the folder's [IMAPIFolder::CreateFolder](imapifolder-createfolder.md) method to create a search-results folder with the FOLDER_SEARCH flag set.</span></span> 
    
2. <span data-ttu-id="4d3b1-117">Создайте ограничение для удержания критериев поиска.</span><span class="sxs-lookup"><span data-stu-id="4d3b1-117">Build a restriction to hold your search criteria.</span></span> 
    
3. <span data-ttu-id="4d3b1-118">Создайте массив идентификаторов записей, которые представляют папки для поиска.</span><span class="sxs-lookup"><span data-stu-id="4d3b1-118">Create an array of entry identifiers that represent the folders to search.</span></span> <span data-ttu-id="4d3b1-119">Этот шаг не является необходимым, если папка результатов поиска использовалась ранее и вы хотите искать в этих же папках.</span><span class="sxs-lookup"><span data-stu-id="4d3b1-119">This step is unnecessary if the search-results folder has been used before and you want to search the same folders.</span></span>
    
4. <span data-ttu-id="4d3b1-120">Вызовите метод [IMAPIContainer::SetSearchCriteria](imapicontainer-setsearchcriteria.md) папки результатов поиска, указав  _lpContainerList_ на массив идентификаторов записей, а  _lpRestriction_ — на ограничение.</span><span class="sxs-lookup"><span data-stu-id="4d3b1-120">Call the search-results folder's [IMAPIContainer::SetSearchCriteria](imapicontainer-setsearchcriteria.md) method, pointing  _lpContainerList_ to the entry identifier array and  _lpRestriction_ to the restriction.</span></span> 
    
5. <span data-ttu-id="4d3b1-121">Если вы зарегистрировали полные уведомления о поиске в хранилище сообщений, дождись их поступления.</span><span class="sxs-lookup"><span data-stu-id="4d3b1-121">If you have registered for search complete notifications with the message store, wait for the notification to arrive.</span></span>
    
6. <span data-ttu-id="4d3b1-122">Чтобы просмотреть результаты поиска, вы можете вызывать метод [IMAPIContainer::GetContentsTable](imapicontainer-getcontentstable.md) папки результатов поиска для доступа к таблице содержимого.</span><span class="sxs-lookup"><span data-stu-id="4d3b1-122">View the results of the search by calling the search-results folder's [IMAPIContainer::GetContentsTable](imapicontainer-getcontentstable.md) method to access its contents table.</span></span> 
    
7. <span data-ttu-id="4d3b1-123">Вызовите метод [IMAPITable::QueryRows](imapitable-queryrows.md) таблицы содержимого, чтобы получить сообщения, удовлетворяющие условиям поиска.</span><span class="sxs-lookup"><span data-stu-id="4d3b1-123">Call the contents table's [IMAPITable::QueryRows](imapitable-queryrows.md) method to retrieve the messages that satisfy the search criteria.</span></span> 
    

