---
title: Сведения об API хранилищ
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 166a8e60-e09d-7473-b61b-35d78a863192
description: '���� ���������� ���������: 25 ���� 2012 �.'
ms.openlocfilehash: d72df30eab5fde4288b5feba1d7045da05117bde
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22579377"
---
# <a name="about-the-store-api"></a><span data-ttu-id="47a7d-103">Сведения об API хранилищ</span><span class="sxs-lookup"><span data-stu-id="47a7d-103">About the Store API</span></span>

  
  
<span data-ttu-id="47a7d-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="47a7d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="47a7d-105">API-Интерфейс хранения предоставляет функциональные возможности прочие хранилища для хранения поставщиков.</span><span class="sxs-lookup"><span data-stu-id="47a7d-105">The Store API provides miscellaneous store functionality to store providers.</span></span> <span data-ttu-id="47a7d-106">Она предоставляет файлов определения, типы данных, свойств и интерфейсы.</span><span class="sxs-lookup"><span data-stu-id="47a7d-106">It provides the following defintions, data types, properties, and interfaces.</span></span>
  
<span data-ttu-id="47a7d-107">Определения:</span><span class="sxs-lookup"><span data-stu-id="47a7d-107">Definitions:</span></span>
  
- [<span data-ttu-id="47a7d-108">Константы для магазина API</span><span class="sxs-lookup"><span data-stu-id="47a7d-108">Constants for the Store API</span></span>](mapi-constants.md)
    
<span data-ttu-id="47a7d-109">Типы данных:</span><span class="sxs-lookup"><span data-stu-id="47a7d-109">Data types:</span></span>
  
- <span data-ttu-id="47a7d-110">**[INDEX_SEARCH_PUSHER_PROCESS](index_search_pusher_process.md)**</span><span class="sxs-lookup"><span data-stu-id="47a7d-110">**[INDEX_SEARCH_PUSHER_PROCESS](index_search_pusher_process.md)**</span></span>
    
- <span data-ttu-id="47a7d-111">**[MSCAP_SELECTOR](mscap_selector.md)**</span><span class="sxs-lookup"><span data-stu-id="47a7d-111">**[MSCAP_SELECTOR](mscap_selector.md)**</span></span>
    
<span data-ttu-id="47a7d-112">Именованные свойства:</span><span class="sxs-lookup"><span data-stu-id="47a7d-112">Named Properties:</span></span>
  
- <span data-ttu-id="47a7d-113">**[ArchiveSourceSupportMask](archivesourcesupportmask.md)**</span><span class="sxs-lookup"><span data-stu-id="47a7d-113">**[ArchiveSourceSupportMask](archivesourcesupportmask.md)**</span></span>
    
- <span data-ttu-id="47a7d-114">**[CrawlSourceSupportMask](crawlsourcesupportmask.md)**</span><span class="sxs-lookup"><span data-stu-id="47a7d-114">**[CrawlSourceSupportMask](crawlsourcesupportmask.md)**</span></span>
    
- <span data-ttu-id="47a7d-115">**[Вывести размер папки сервера](display-server-folder-sizes-property.md)**</span><span class="sxs-lookup"><span data-stu-id="47a7d-115">**[Display Server Folder Sizes](display-server-folder-sizes-property.md)**</span></span>
    
- <span data-ttu-id="47a7d-116">**[Скрытие параметра обновления собрания](hide-meeting-update-option-property.md)**</span><span class="sxs-lookup"><span data-stu-id="47a7d-116">**[Hide Meeting Update Option](hide-meeting-update-option-property.md)**</span></span>
    
- <span data-ttu-id="47a7d-117">**[Создание хранилища типа Private](make-store-type-private-property.md)**</span><span class="sxs-lookup"><span data-stu-id="47a7d-117">**[Make Store Type Private](make-store-type-private-property.md)**</span></span>
    
- <span data-ttu-id="47a7d-118">**[NoFolderScan](nofolderscan.md)**</span><span class="sxs-lookup"><span data-stu-id="47a7d-118">**[NoFolderScan](nofolderscan.md)**</span></span>
    
> [!NOTE]
> <span data-ttu-id="47a7d-119">Поставщики хранилища, не требуются функциональные возможности, предоставляемые эти именованные свойства можно игнорировать их и не реализации поддержки в интерфейсе **IMAPIProp** .</span><span class="sxs-lookup"><span data-stu-id="47a7d-119">Store providers that do not require any of the functionality offered by these named properties can simply ignore them and not implement support in the **IMAPIProp** interface.</span></span> <span data-ttu-id="47a7d-120">Так как эти свойства предоставляются начиная с Microsoft Outlook 2003 с пакетом обновления 1, добавляя их в хранилище в более ранней версии Microsoft Outlook не оказывает влияния.</span><span class="sxs-lookup"><span data-stu-id="47a7d-120">Because these properties are provided starting in Microsoft Outlook 2003 Service Pack 1, adding them to a store in an earlier version of Microsoft Outlook has no effect.</span></span> <span data-ttu-id="47a7d-121">Они игнорируются, если они не существуют или если их значение равно **false**.</span><span class="sxs-lookup"><span data-stu-id="47a7d-121">They are ignored if they do not exist or if their value is **false**.</span></span> 
  
<span data-ttu-id="47a7d-122">Свойства:</span><span class="sxs-lookup"><span data-stu-id="47a7d-122">Properties:</span></span>
  
- <span data-ttu-id="47a7d-123">**[PR_ADDITIONAL_REN_ENTRYIDS](pidtagadditionalrenentryids-canonical-property.md)**</span><span class="sxs-lookup"><span data-stu-id="47a7d-123">**[PR_ADDITIONAL_REN_ENTRYIDS](pidtagadditionalrenentryids-canonical-property.md)**</span></span>
    
- <span data-ttu-id="47a7d-124">**[PR_PROVIDER_ITEMID](pidtagprovideritemid-canonical-property.md)**</span><span class="sxs-lookup"><span data-stu-id="47a7d-124">**[PR_PROVIDER_ITEMID](pidtagprovideritemid-canonical-property.md)**</span></span>
    
- <span data-ttu-id="47a7d-125">**[PR_PROVIDER_PARENT_ITEMID](pidtagproviderparentitemid-canonical-property.md)**</span><span class="sxs-lookup"><span data-stu-id="47a7d-125">**[PR_PROVIDER_PARENT_ITEMID](pidtagproviderparentitemid-canonical-property.md)**</span></span>
    
- <span data-ttu-id="47a7d-126">**[PR_SEARCH_OWNER_ID](pidtagsearchownerid-canonical-property.md)**</span><span class="sxs-lookup"><span data-stu-id="47a7d-126">**[PR_SEARCH_OWNER_ID](pidtagsearchownerid-canonical-property.md)**</span></span>
    
<span data-ttu-id="47a7d-127">Интерфейсы:</span><span class="sxs-lookup"><span data-stu-id="47a7d-127">Interfaces:</span></span>
  
- <span data-ttu-id="47a7d-128">**[IFolderSupport](ifoldersupportiunknown.md)**</span><span class="sxs-lookup"><span data-stu-id="47a7d-128">**[IFolderSupport](ifoldersupportiunknown.md)**</span></span>
    
- <span data-ttu-id="47a7d-129">**[IMSCapabilities](imscapabilitiesiunknown.md)**</span><span class="sxs-lookup"><span data-stu-id="47a7d-129">**[IMSCapabilities](imscapabilitiesiunknown.md)**</span></span>
    
- <span data-ttu-id="47a7d-130">**[IProxyStoreObject](iproxystoreobject.md)**</span><span class="sxs-lookup"><span data-stu-id="47a7d-130">**[IProxyStoreObject](iproxystoreobject.md)**</span></span>
    
## <a name="registering-stores-for-indexing"></a><span data-ttu-id="47a7d-131">Регистрация хранилища для индексации</span><span class="sxs-lookup"><span data-stu-id="47a7d-131">Registering Stores for Indexing</span></span>

<span data-ttu-id="47a7d-132">Обработчик протокола MAPI проверяет реестра Windows для хранилищ, которые следует индексации для поиска.</span><span class="sxs-lookup"><span data-stu-id="47a7d-132">The MAPI Protocol Handler checks the Windows registry for stores that it should index for search purposes.</span></span> <span data-ttu-id="47a7d-133">Поставщики хранилища, чтобы быть индексированы должна быть зарегистрирована в реестре Windows.</span><span class="sxs-lookup"><span data-stu-id="47a7d-133">Store providers that want to be indexed must be registered in the Windows registry.</span></span> <span data-ttu-id="47a7d-134">Дополнительные сведения о регистрации поставщиков хранилища для индексации в Outlook 2010 или Outlook 2013 можно [О регистрации хранилища для индексирования](about-registering-stores-for-indexing.md).</span><span class="sxs-lookup"><span data-stu-id="47a7d-134">For more information about registering store providers for indexing in Outlook 2013 or Outlook 2010, see [About Registering Stores for Indexing](about-registering-stores-for-indexing.md).</span></span>
  
## <a name="indexing-stores"></a><span data-ttu-id="47a7d-135">Индексация хранилища</span><span class="sxs-lookup"><span data-stu-id="47a7d-135">Indexing Stores</span></span>

<span data-ttu-id="47a7d-136">Поставщики MAPI хранилища можно разрешить обработчик протокола MAPI для обхода и индексирования сообщения в хранилище или отправлять уведомления на индексатор только в том случае, если сообщений для индексирования.</span><span class="sxs-lookup"><span data-stu-id="47a7d-136">MAPI store providers can choose to allow the MAPI Protocol Handler to crawl and index messages in the store, or send notifications to the indexer only when there are messages to be indexed.</span></span> <span data-ttu-id="47a7d-137">Дополнительные сведения о на основе уведомлений индексирования видеть [About Notification-Based хранилища индексирования](about-notification-based-store-indexing.md).</span><span class="sxs-lookup"><span data-stu-id="47a7d-137">For more information about notifications-based indexing, see [About Notification-Based Store Indexing](about-notification-based-store-indexing.md).</span></span>
  

