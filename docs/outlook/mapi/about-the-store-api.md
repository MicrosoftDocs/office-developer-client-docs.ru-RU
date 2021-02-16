---
title: Сведения об API хранилищ
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 166a8e60-e09d-7473-b61b-35d78a863192
description: '���� ���������� ���������: 25 ���� 2012 �.'
ms.openlocfilehash: fb9b0a4c8ac1a2f41a0fddcd746dba5fc4bae1a2
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33405557"
---
# <a name="about-the-store-api"></a><span data-ttu-id="87f3d-103">Сведения об API хранилищ</span><span class="sxs-lookup"><span data-stu-id="87f3d-103">About the Store API</span></span>

  
  
<span data-ttu-id="87f3d-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="87f3d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="87f3d-105">API Магазина предоставляет различные функции магазина для хранения поставщиков.</span><span class="sxs-lookup"><span data-stu-id="87f3d-105">The Store API provides miscellaneous store functionality to store providers.</span></span> <span data-ttu-id="87f3d-106">Он предоставляет следующие отсрочки, типы данных, свойства и интерфейсы.</span><span class="sxs-lookup"><span data-stu-id="87f3d-106">It provides the following defintions, data types, properties, and interfaces.</span></span>
  
<span data-ttu-id="87f3d-107">Определения</span><span class="sxs-lookup"><span data-stu-id="87f3d-107">Definitions:</span></span>
  
- [<span data-ttu-id="87f3d-108">Константы для API Магазина</span><span class="sxs-lookup"><span data-stu-id="87f3d-108">Constants for the Store API</span></span>](mapi-constants.md)
    
<span data-ttu-id="87f3d-109">Типы данных:</span><span class="sxs-lookup"><span data-stu-id="87f3d-109">Data types:</span></span>
  
- <span data-ttu-id="87f3d-110">**[INDEX_SEARCH_PUSHER_PROCESS](index_search_pusher_process.md)**</span><span class="sxs-lookup"><span data-stu-id="87f3d-110">**[INDEX_SEARCH_PUSHER_PROCESS](index_search_pusher_process.md)**</span></span>
    
- <span data-ttu-id="87f3d-111">**[MSCAP_SELECTOR](mscap_selector.md)**</span><span class="sxs-lookup"><span data-stu-id="87f3d-111">**[MSCAP_SELECTOR](mscap_selector.md)**</span></span>
    
<span data-ttu-id="87f3d-112">Именуемые свойства:</span><span class="sxs-lookup"><span data-stu-id="87f3d-112">Named Properties:</span></span>
  
- <span data-ttu-id="87f3d-113">**[ArchiveSourceSupportMask](archivesourcesupportmask.md)**</span><span class="sxs-lookup"><span data-stu-id="87f3d-113">**[ArchiveSourceSupportMask](archivesourcesupportmask.md)**</span></span>
    
- <span data-ttu-id="87f3d-114">**[CrawlSourceSupportMask](crawlsourcesupportmask.md)**</span><span class="sxs-lookup"><span data-stu-id="87f3d-114">**[CrawlSourceSupportMask](crawlsourcesupportmask.md)**</span></span>
    
- <span data-ttu-id="87f3d-115">**[Размеры папок сервера отображения](display-server-folder-sizes-property.md)**</span><span class="sxs-lookup"><span data-stu-id="87f3d-115">**[Display Server Folder Sizes](display-server-folder-sizes-property.md)**</span></span>
    
- <span data-ttu-id="87f3d-116">**[Скрытие параметра обновления собрания](hide-meeting-update-option-property.md)**</span><span class="sxs-lookup"><span data-stu-id="87f3d-116">**[Hide Meeting Update Option](hide-meeting-update-option-property.md)**</span></span>
    
- <span data-ttu-id="87f3d-117">**[Сделайте тип магазина частным](make-store-type-private-property.md)**</span><span class="sxs-lookup"><span data-stu-id="87f3d-117">**[Make Store Type Private](make-store-type-private-property.md)**</span></span>
    
- <span data-ttu-id="87f3d-118">**[NoFolderScan](nofolderscan.md)**</span><span class="sxs-lookup"><span data-stu-id="87f3d-118">**[NoFolderScan](nofolderscan.md)**</span></span>
    
> [!NOTE]
> <span data-ttu-id="87f3d-119">Поставщики магазина, для которых не требуются функции этих именуемого свойства, могут просто игнорировать их и не реализовать поддержку в **интерфейсе IMAPIProp.**</span><span class="sxs-lookup"><span data-stu-id="87f3d-119">Store providers that do not require any of the functionality offered by these named properties can simply ignore them and not implement support in the **IMAPIProp** interface.</span></span> <span data-ttu-id="87f3d-120">Так как эти свойства предоставляются начиная с Microsoft Outlook 2003 Пакет обновления 1, их добавление в магазин в более ранней версии Microsoft Outlook не влияет.</span><span class="sxs-lookup"><span data-stu-id="87f3d-120">Because these properties are provided starting in Microsoft Outlook 2003 Service Pack 1, adding them to a store in an earlier version of Microsoft Outlook has no effect.</span></span> <span data-ttu-id="87f3d-121">Они игнорируются, если они не существуют или если их значение **false.**</span><span class="sxs-lookup"><span data-stu-id="87f3d-121">They are ignored if they do not exist or if their value is **false**.</span></span> 
  
<span data-ttu-id="87f3d-122">Свойства:</span><span class="sxs-lookup"><span data-stu-id="87f3d-122">Properties:</span></span>
  
- <span data-ttu-id="87f3d-123">**[PR_ADDITIONAL_REN_ENTRYIDS](pidtagadditionalrenentryids-canonical-property.md)**</span><span class="sxs-lookup"><span data-stu-id="87f3d-123">**[PR_ADDITIONAL_REN_ENTRYIDS](pidtagadditionalrenentryids-canonical-property.md)**</span></span>
    
- <span data-ttu-id="87f3d-124">**[PR_PROVIDER_ITEMID](pidtagprovideritemid-canonical-property.md)**</span><span class="sxs-lookup"><span data-stu-id="87f3d-124">**[PR_PROVIDER_ITEMID](pidtagprovideritemid-canonical-property.md)**</span></span>
    
- <span data-ttu-id="87f3d-125">**[PR_PROVIDER_PARENT_ITEMID](pidtagproviderparentitemid-canonical-property.md)**</span><span class="sxs-lookup"><span data-stu-id="87f3d-125">**[PR_PROVIDER_PARENT_ITEMID](pidtagproviderparentitemid-canonical-property.md)**</span></span>
    
- <span data-ttu-id="87f3d-126">**[PR_SEARCH_OWNER_ID](pidtagsearchownerid-canonical-property.md)**</span><span class="sxs-lookup"><span data-stu-id="87f3d-126">**[PR_SEARCH_OWNER_ID](pidtagsearchownerid-canonical-property.md)**</span></span>
    
<span data-ttu-id="87f3d-127">Интерфейсы:</span><span class="sxs-lookup"><span data-stu-id="87f3d-127">Interfaces:</span></span>
  
- <span data-ttu-id="87f3d-128">**[IFolderSupport](ifoldersupportiunknown.md)**</span><span class="sxs-lookup"><span data-stu-id="87f3d-128">**[IFolderSupport](ifoldersupportiunknown.md)**</span></span>
    
- <span data-ttu-id="87f3d-129">**[IMSCapabilities](imscapabilitiesiunknown.md)**</span><span class="sxs-lookup"><span data-stu-id="87f3d-129">**[IMSCapabilities](imscapabilitiesiunknown.md)**</span></span>
    
- <span data-ttu-id="87f3d-130">**[IProxyStoreObject](iproxystoreobject.md)**</span><span class="sxs-lookup"><span data-stu-id="87f3d-130">**[IProxyStoreObject](iproxystoreobject.md)**</span></span>
    
## <a name="registering-stores-for-indexing"></a><span data-ttu-id="87f3d-131">Регистрация хранилищ для индексации</span><span class="sxs-lookup"><span data-stu-id="87f3d-131">Registering Stores for Indexing</span></span>

<span data-ttu-id="87f3d-132">Обработник протокола MAPI проверяет реестр Windows на наличие хранилищ, которые он должен индексировать в целях поиска.</span><span class="sxs-lookup"><span data-stu-id="87f3d-132">The MAPI Protocol Handler checks the Windows registry for stores that it should index for search purposes.</span></span> <span data-ttu-id="87f3d-133">Поставщики магазина, которые хотят индексироваться, должны быть зарегистрированы в реестре Windows.</span><span class="sxs-lookup"><span data-stu-id="87f3d-133">Store providers that want to be indexed must be registered in the Windows registry.</span></span> <span data-ttu-id="87f3d-134">Дополнительные сведения о регистрации поставщиков хранилища для индексации в Outlook 2013 или Outlook 2010 см. в сведениях о регистрации хранилищ для [индексации.](about-registering-stores-for-indexing.md)</span><span class="sxs-lookup"><span data-stu-id="87f3d-134">For more information about registering store providers for indexing in Outlook 2013 or Outlook 2010, see [About Registering Stores for Indexing](about-registering-stores-for-indexing.md).</span></span>
  
## <a name="indexing-stores"></a><span data-ttu-id="87f3d-135">Хранилища индексации</span><span class="sxs-lookup"><span data-stu-id="87f3d-135">Indexing Stores</span></span>

<span data-ttu-id="87f3d-136">Поставщики store MAPI могут разрешить обработщику протокола MAPI обходить и индексировать сообщения в хранилище или отправлять уведомления индекселю только при индексации сообщений.</span><span class="sxs-lookup"><span data-stu-id="87f3d-136">MAPI store providers can choose to allow the MAPI Protocol Handler to crawl and index messages in the store, or send notifications to the indexer only when there are messages to be indexed.</span></span> <span data-ttu-id="87f3d-137">Дополнительные сведения об индексации на основе уведомлений см. в Notification-Based [Store.](about-notification-based-store-indexing.md)</span><span class="sxs-lookup"><span data-stu-id="87f3d-137">For more information about notifications-based indexing, see [About Notification-Based Store Indexing](about-notification-based-store-indexing.md).</span></span>
  

