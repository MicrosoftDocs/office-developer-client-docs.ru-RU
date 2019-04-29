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
# <a name="searching-a-message-store"></a><span data-ttu-id="d8aaa-103">Поиск в хранилище сообщений</span><span class="sxs-lookup"><span data-stu-id="d8aaa-103">Searching a message store</span></span>

<span data-ttu-id="d8aaa-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d8aaa-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d8aaa-105">Клиентские приложения могут выполнять поиск в одной или нескольких папках, в которых выполняется поиск сообщений, которые отвечают условиям поиска.</span><span class="sxs-lookup"><span data-stu-id="d8aaa-105">Client applications can search through one or more folders looking for messages that match search criteria.</span></span> <span data-ttu-id="d8aaa-106">Наиболее простая методика поиска включает в себя применение ограничения для определения критериев и размещения результатов в папке результатов поиска, созданной явным образом для этого поиска или для предыдущего поиска.</span><span class="sxs-lookup"><span data-stu-id="d8aaa-106">The most straightforward search technique involves applying a restriction to define criteria and placing the results into a search-results folder, created explicitly for this search or for a prior search.</span></span> <span data-ttu-id="d8aaa-107">Эту методику поддерживает не все хранилища сообщений.</span><span class="sxs-lookup"><span data-stu-id="d8aaa-107">Not all message stores support this technique.</span></span> 

<span data-ttu-id="d8aaa-108">Чтобы определить, поддерживает ли используемое хранилище сообщений использование папок результатов поиска, вызовите его метод [IMAPIProp::](imapiprop-getprops.md) -Props, чтобы получить значение свойства **\_PR сторе_суппорт_маск** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="d8aaa-108">To determine whether or not the message store you are using supports using search-results folders, call its [IMAPIProp::GetProps](imapiprop-getprops.md) method to retrieve the **PR\_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) property.</span></span> <span data-ttu-id="d8aaa-109">Если установлен флаг СТОРЕ_СЕАРЧ_ОК, Поиск поддерживается.</span><span class="sxs-lookup"><span data-stu-id="d8aaa-109">If the STORE_SEARCH_OK flag is set, searching is supported.</span></span> <span data-ttu-id="d8aaa-110">Если он не задан, потребуется альтернативный способ проверки целевых папок вручную.</span><span class="sxs-lookup"><span data-stu-id="d8aaa-110">If it is not set, you'll need an alternate approach such as manually inspecting the target folders.</span></span>
  
### <a name="to-search-one-or-more-folders-in-a-message-store"></a><span data-ttu-id="d8aaa-111">Поиск в одной или нескольких папках в хранилище сообщений</span><span class="sxs-lookup"><span data-stu-id="d8aaa-111">To search one or more folders in a message store</span></span>
  
1. <span data-ttu-id="d8aaa-112">Если у вас есть папка результатов поиска из предыдущего поиска, перейдите к шагу 2.</span><span class="sxs-lookup"><span data-stu-id="d8aaa-112">If you have a search-results folder from a previous search, skip to step 2.</span></span> <span data-ttu-id="d8aaa-113">В противном случае для создания папки результатов поиска выполните следующие действия:</span><span class="sxs-lookup"><span data-stu-id="d8aaa-113">Otherwise, to create a search-results folder:</span></span>
    
    1. <span data-ttu-id="d8aaa-114">Получите идентификатор записи для корневой папки результатов поиска, вызвав метод [IMAPIProp::](imapiprop-getprops.md) -PROPS хранилища сообщений и запрашивая **пр_финдер_ентрид** ([PidTagFinderEntryId](pidtagfinderentryid-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="d8aaa-114">Retrieve the entry identifier for the search-results root folder by calling the message store's [IMAPIProp::GetProps](imapiprop-getprops.md) method and requesting **PR_FINDER_ENTRYID** ([PidTagFinderEntryId](pidtagfinderentryid-canonical-property.md)).</span></span>
        
    2. <span data-ttu-id="d8aaa-115">Call [IMsgStore:: OpenEntry](imsgstore-openentry.md) для открытия папки, представленной с помощью пр_финдер_ентрид.</span><span class="sxs-lookup"><span data-stu-id="d8aaa-115">Call [IMsgStore::OpenEntry](imsgstore-openentry.md) to open the folder represented by PR_FINDER_ENTRYID.</span></span> 
        
    3. <span data-ttu-id="d8aaa-116">ВыЗовите метод [IMAPIFolder:: CreateFolder](imapifolder-createfolder.md) для создания папки результатов поиска с установленным флагом фолдер_сеарч.</span><span class="sxs-lookup"><span data-stu-id="d8aaa-116">Call the folder's [IMAPIFolder::CreateFolder](imapifolder-createfolder.md) method to create a search-results folder with the FOLDER_SEARCH flag set.</span></span> 
    
2. <span data-ttu-id="d8aaa-117">Создание ограничения для хранения критериев поиска.</span><span class="sxs-lookup"><span data-stu-id="d8aaa-117">Build a restriction to hold your search criteria.</span></span> 
    
3. <span data-ttu-id="d8aaa-118">Создайте массив идентификаторов записей, представляющих папки для поиска.</span><span class="sxs-lookup"><span data-stu-id="d8aaa-118">Create an array of entry identifiers that represent the folders to search.</span></span> <span data-ttu-id="d8aaa-119">Этот шаг не требуется, если ранее использовалась папка результатов поиска, и вы хотите выполнить поиск в тех же папках.</span><span class="sxs-lookup"><span data-stu-id="d8aaa-119">This step is unnecessary if the search-results folder has been used before and you want to search the same folders.</span></span>
    
4. <span data-ttu-id="d8aaa-120">ВыЗовите метод [IMAPIContainer:: сетсеарчкритериа](imapicontainer-setsearchcriteria.md) папки результатов поиска, указав _лпконтаинерлист_ в массиве идентификаторов записей и _лпрестриктион_ к ограничению.</span><span class="sxs-lookup"><span data-stu-id="d8aaa-120">Call the search-results folder's [IMAPIContainer::SetSearchCriteria](imapicontainer-setsearchcriteria.md) method, pointing  _lpContainerList_ to the entry identifier array and  _lpRestriction_ to the restriction.</span></span> 
    
5. <span data-ttu-id="d8aaa-121">Если вы зарегистрировались для получения уведомлений о завершении поиска с хранилищем сообщений, дождитесь поступления уведомления.</span><span class="sxs-lookup"><span data-stu-id="d8aaa-121">If you have registered for search complete notifications with the message store, wait for the notification to arrive.</span></span>
    
6. <span data-ttu-id="d8aaa-122">Просмотрите результаты поиска, вызвав метод [IMAPIContainer:: жетконтентстабле](imapicontainer-getcontentstable.md) папки результатов поиска, чтобы получить доступ к его таблице содержимого.</span><span class="sxs-lookup"><span data-stu-id="d8aaa-122">View the results of the search by calling the search-results folder's [IMAPIContainer::GetContentsTable](imapicontainer-getcontentstable.md) method to access its contents table.</span></span> 
    
7. <span data-ttu-id="d8aaa-123">ВыЗовите таблицу содержимого: метод [IMAPITable:: QueryRows](imapitable-queryrows.md) для получения сообщений, удовлетворяющих условиям поиска.</span><span class="sxs-lookup"><span data-stu-id="d8aaa-123">Call the contents table's [IMAPITable::QueryRows](imapitable-queryrows.md) method to retrieve the messages that satisfy the search criteria.</span></span> 
    

