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
# <a name="about-the-store-api"></a><span data-ttu-id="f9883-103">Сведения об API хранилищ</span><span class="sxs-lookup"><span data-stu-id="f9883-103">About the Store API</span></span>

  
  
<span data-ttu-id="f9883-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f9883-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f9883-105">API Store предоставляет различные функции хранения для хранения поставщиков.</span><span class="sxs-lookup"><span data-stu-id="f9883-105">The Store API provides miscellaneous store functionality to store providers.</span></span> <span data-ttu-id="f9883-106">Он предоставляет следующие дефинтионс, типы данных, свойства и интерфейсы.</span><span class="sxs-lookup"><span data-stu-id="f9883-106">It provides the following defintions, data types, properties, and interfaces.</span></span>
  
<span data-ttu-id="f9883-107">Определения</span><span class="sxs-lookup"><span data-stu-id="f9883-107">Definitions:</span></span>
  
- [<span data-ttu-id="f9883-108">Константы для API Store</span><span class="sxs-lookup"><span data-stu-id="f9883-108">Constants for the Store API</span></span>](mapi-constants.md)
    
<span data-ttu-id="f9883-109">Типы данных:</span><span class="sxs-lookup"><span data-stu-id="f9883-109">Data types:</span></span>
  
- <span data-ttu-id="f9883-110">**[INDEX_SEARCH_PUSHER_PROCESS](index_search_pusher_process.md)**</span><span class="sxs-lookup"><span data-stu-id="f9883-110">**[INDEX_SEARCH_PUSHER_PROCESS](index_search_pusher_process.md)**</span></span>
    
- <span data-ttu-id="f9883-111">**[MSCAP_SELECTOR](mscap_selector.md)**</span><span class="sxs-lookup"><span data-stu-id="f9883-111">**[MSCAP_SELECTOR](mscap_selector.md)**</span></span>
    
<span data-ttu-id="f9883-112">Именованные свойства:</span><span class="sxs-lookup"><span data-stu-id="f9883-112">Named Properties:</span></span>
  
- <span data-ttu-id="f9883-113">**[ArchiveSourceSupportMask](archivesourcesupportmask.md)**</span><span class="sxs-lookup"><span data-stu-id="f9883-113">**[ArchiveSourceSupportMask](archivesourcesupportmask.md)**</span></span>
    
- <span data-ttu-id="f9883-114">**[CrawlSourceSupportMask](crawlsourcesupportmask.md)**</span><span class="sxs-lookup"><span data-stu-id="f9883-114">**[CrawlSourceSupportMask](crawlsourcesupportmask.md)**</span></span>
    
- <span data-ttu-id="f9883-115">**[Отображение размеров папок сервера](display-server-folder-sizes-property.md)**</span><span class="sxs-lookup"><span data-stu-id="f9883-115">**[Display Server Folder Sizes](display-server-folder-sizes-property.md)**</span></span>
    
- <span data-ttu-id="f9883-116">**[Параметр "Скрыть обновление собрания"](hide-meeting-update-option-property.md)**</span><span class="sxs-lookup"><span data-stu-id="f9883-116">**[Hide Meeting Update Option](hide-meeting-update-option-property.md)**</span></span>
    
- <span data-ttu-id="f9883-117">**[Сделать тип хранилища частным](make-store-type-private-property.md)**</span><span class="sxs-lookup"><span data-stu-id="f9883-117">**[Make Store Type Private](make-store-type-private-property.md)**</span></span>
    
- <span data-ttu-id="f9883-118">**[NoFolderScan](nofolderscan.md)**</span><span class="sxs-lookup"><span data-stu-id="f9883-118">**[NoFolderScan](nofolderscan.md)**</span></span>
    
> [!NOTE]
> <span data-ttu-id="f9883-119">Поставщики хранилища, не требующие функциональных возможностей, предоставляемых этими именованными свойствами, могут просто игнорировать их и не реализовать поддержку в интерфейсе **IMAPIProp** .</span><span class="sxs-lookup"><span data-stu-id="f9883-119">Store providers that do not require any of the functionality offered by these named properties can simply ignore them and not implement support in the **IMAPIProp** interface.</span></span> <span data-ttu-id="f9883-120">Так как эти свойства предоставляются начиная с Microsoft Outlook 2003 с пакетом обновления 1 (SP1), добавление их в хранилище в более ранней версии Microsoft Outlook не оказывает никакого действия.</span><span class="sxs-lookup"><span data-stu-id="f9883-120">Because these properties are provided starting in Microsoft Outlook 2003 Service Pack 1, adding them to a store in an earlier version of Microsoft Outlook has no effect.</span></span> <span data-ttu-id="f9883-121">Они игнорируются, если они не существуют, или если их значение равно **false**.</span><span class="sxs-lookup"><span data-stu-id="f9883-121">They are ignored if they do not exist or if their value is **false**.</span></span> 
  
<span data-ttu-id="f9883-122">Свойства:</span><span class="sxs-lookup"><span data-stu-id="f9883-122">Properties:</span></span>
  
- <span data-ttu-id="f9883-123">**[PR_ADDITIONAL_REN_ENTRYIDS](pidtagadditionalrenentryids-canonical-property.md)**</span><span class="sxs-lookup"><span data-stu-id="f9883-123">**[PR_ADDITIONAL_REN_ENTRYIDS](pidtagadditionalrenentryids-canonical-property.md)**</span></span>
    
- <span data-ttu-id="f9883-124">**[PR_PROVIDER_ITEMID](pidtagprovideritemid-canonical-property.md)**</span><span class="sxs-lookup"><span data-stu-id="f9883-124">**[PR_PROVIDER_ITEMID](pidtagprovideritemid-canonical-property.md)**</span></span>
    
- <span data-ttu-id="f9883-125">**[PR_PROVIDER_PARENT_ITEMID](pidtagproviderparentitemid-canonical-property.md)**</span><span class="sxs-lookup"><span data-stu-id="f9883-125">**[PR_PROVIDER_PARENT_ITEMID](pidtagproviderparentitemid-canonical-property.md)**</span></span>
    
- <span data-ttu-id="f9883-126">**[PR_SEARCH_OWNER_ID](pidtagsearchownerid-canonical-property.md)**</span><span class="sxs-lookup"><span data-stu-id="f9883-126">**[PR_SEARCH_OWNER_ID](pidtagsearchownerid-canonical-property.md)**</span></span>
    
<span data-ttu-id="f9883-127">Интерфейс</span><span class="sxs-lookup"><span data-stu-id="f9883-127">Interfaces:</span></span>
  
- <span data-ttu-id="f9883-128">**[IFolderSupport](ifoldersupportiunknown.md)**</span><span class="sxs-lookup"><span data-stu-id="f9883-128">**[IFolderSupport](ifoldersupportiunknown.md)**</span></span>
    
- <span data-ttu-id="f9883-129">**[IMSCapabilities](imscapabilitiesiunknown.md)**</span><span class="sxs-lookup"><span data-stu-id="f9883-129">**[IMSCapabilities](imscapabilitiesiunknown.md)**</span></span>
    
- <span data-ttu-id="f9883-130">**[IProxyStoreObject](iproxystoreobject.md)**</span><span class="sxs-lookup"><span data-stu-id="f9883-130">**[IProxyStoreObject](iproxystoreobject.md)**</span></span>
    
## <a name="registering-stores-for-indexing"></a><span data-ttu-id="f9883-131">Регистрация хранилищ для индексирования</span><span class="sxs-lookup"><span data-stu-id="f9883-131">Registering Stores for Indexing</span></span>

<span data-ttu-id="f9883-132">Обработчик протокола MAPI проверяет реестр Windows для хранения, который он должен индексировать для целей поиска.</span><span class="sxs-lookup"><span data-stu-id="f9883-132">The MAPI Protocol Handler checks the Windows registry for stores that it should index for search purposes.</span></span> <span data-ttu-id="f9883-133">Поставщики хранилища, которые требуется индексировать, должны быть зарегистрированы в реестре Windows.</span><span class="sxs-lookup"><span data-stu-id="f9883-133">Store providers that want to be indexed must be registered in the Windows registry.</span></span> <span data-ttu-id="f9883-134">Дополнительные сведения о регистрации поставщиков услуг хранения для индексации в Outlook 2013 или Outlook 2010 приведены в статье [Регистрация хранилищ для индексирования](about-registering-stores-for-indexing.md).</span><span class="sxs-lookup"><span data-stu-id="f9883-134">For more information about registering store providers for indexing in Outlook 2013 or Outlook 2010, see [About Registering Stores for Indexing](about-registering-stores-for-indexing.md).</span></span>
  
## <a name="indexing-stores"></a><span data-ttu-id="f9883-135">Индексирование хранилищ</span><span class="sxs-lookup"><span data-stu-id="f9883-135">Indexing Stores</span></span>

<span data-ttu-id="f9883-136">Поставщики хранилища MAPI могут разрешить обработчику протокола MAPI обходить и индексировать сообщения в хранилище, а также отправлять уведомления индексатору только при наличии сообщений для индексирования.</span><span class="sxs-lookup"><span data-stu-id="f9883-136">MAPI store providers can choose to allow the MAPI Protocol Handler to crawl and index messages in the store, or send notifications to the indexer only when there are messages to be indexed.</span></span> <span data-ttu-id="f9883-137">Более подробную информацию об индексировании хранилищ на основе уведомлений можно узнать в статье [об индексировании хранилищ на основе уведомлений](about-notification-based-store-indexing.md).</span><span class="sxs-lookup"><span data-stu-id="f9883-137">For more information about notifications-based indexing, see [About Notification-Based Store Indexing](about-notification-based-store-indexing.md).</span></span>
  

