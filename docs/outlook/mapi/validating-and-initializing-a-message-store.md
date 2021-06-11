---
title: Проверка и инициализация магазина сообщений
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 74f0a1fe-2a79-4b32-ab88-85a8839a2639
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 77b3f707fc36a868de5acd7c7ba4642a1da4e3c9
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33433691"
---
# <a name="validating-and-initializing-a-message-store"></a><span data-ttu-id="0010c-103">Проверка и инициализация магазина сообщений</span><span class="sxs-lookup"><span data-stu-id="0010c-103">Validating and Initializing a Message Store</span></span>

  
  
<span data-ttu-id="0010c-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0010c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0010c-105">Когда вы открываете хранилище сообщений с помощью метода [IMAPISession::OpenMsgStore](imapisession-openmsgstore.md) без установки флага MDB_NO_MAIL, MAPI создает несколько папок и назначает им имена и роли по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="0010c-105">When you open a message store through the [IMAPISession::OpenMsgStore](imapisession-openmsgstore.md) method without setting the MDB_NO_MAIL flag, MAPI creates several folders and assigns them default names and roles.</span></span> <span data-ttu-id="0010c-106">MAPI отвечает за создание этих папок, чтобы избежать несовместимости, которая неизбежно возникает, если за создание отвечали клиенты или поставщики магазинов сообщений.</span><span class="sxs-lookup"><span data-stu-id="0010c-106">MAPI is responsible for creating these folders to avoid the incompatibilities that would inevitably occur if either clients or message store providers were responsible for the creation.</span></span> 
  
<span data-ttu-id="0010c-107">Иногда необходимо убедиться, что соответствующие папки созданы и являются допустимы.</span><span class="sxs-lookup"><span data-stu-id="0010c-107">Sometimes it is necessary to verify that the appropriate folders have been created and that they are valid.</span></span> <span data-ttu-id="0010c-108">Для [этого доступна функция HrValidateIPMSubtree.](hrvalidateipmsubtree.md)</span><span class="sxs-lookup"><span data-stu-id="0010c-108">The [HrValidateIPMSubtree](hrvalidateipmsubtree.md) function is available for this purpose.</span></span> <span data-ttu-id="0010c-109">Если вы проходите проверку магазина сообщений по умолчанию, передай MAPI_FULL_IPM_TREE флаг.</span><span class="sxs-lookup"><span data-stu-id="0010c-109">If you are validating the default message store, pass the MAPI_FULL_IPM_TREE flag.</span></span> <span data-ttu-id="0010c-110">Для магазина сообщений по умолчанию создается более обширная группа папок.</span><span class="sxs-lookup"><span data-stu-id="0010c-110">A more extensive group of folders is created for the default message store.</span></span> <span data-ttu-id="0010c-111">Когда **hrValidateIPMSubtree** получает флаг MAPI_FULL_IPM_TREE, он проверяет следующие папки:</span><span class="sxs-lookup"><span data-stu-id="0010c-111">When **HrValidateIPMSubtree** receives the MAPI_FULL_IPM_TREE flag, it checks for the following folders:</span></span> 
  
- <span data-ttu-id="0010c-112">Корневая папка для подтриба IPM</span><span class="sxs-lookup"><span data-stu-id="0010c-112">Root folder for the IPM subtree</span></span>
    
- <span data-ttu-id="0010c-113">Папка "Удаленные элементы" в корневой папке IPM</span><span class="sxs-lookup"><span data-stu-id="0010c-113">Deleted Items folder in the IPM root folder</span></span>
    
- <span data-ttu-id="0010c-114">Папка "Входящие" в корневой папке IPM</span><span class="sxs-lookup"><span data-stu-id="0010c-114">Inbox folder in the IPM root folder</span></span>
    
- <span data-ttu-id="0010c-115">Папка "Outbox" в корневой папке IPM</span><span class="sxs-lookup"><span data-stu-id="0010c-115">Outbox folder in the IPM root folder</span></span>
    
- <span data-ttu-id="0010c-116">Папка Отправленные элементы в корневой папке IPM</span><span class="sxs-lookup"><span data-stu-id="0010c-116">Sent Items folder in the IPM root folder</span></span>
    
- <span data-ttu-id="0010c-117">Представления папок в корневой папке магазина сообщений</span><span class="sxs-lookup"><span data-stu-id="0010c-117">Folder views in the message store's root folder</span></span>
    
- <span data-ttu-id="0010c-118">Общие представления в корневой папке магазина сообщений</span><span class="sxs-lookup"><span data-stu-id="0010c-118">Common views in the message store's root folder</span></span>
    
- <span data-ttu-id="0010c-119">Папка поиска в корневой папке магазина сообщений</span><span class="sxs-lookup"><span data-stu-id="0010c-119">Search folder in the message store's root folder</span></span>
    
<span data-ttu-id="0010c-120">Если хранилище сообщений не является по умолчанию, можно установить или MAPI_FULL_IPM_TREE флаг.</span><span class="sxs-lookup"><span data-stu-id="0010c-120">If the message store is not the default, you can either set or not set the MAPI_FULL_IPM_TREE flag.</span></span> <span data-ttu-id="0010c-121">Если этот флаг не задан, **HrValidateIPMSubtree** проверяет только корневую папку для подтрия, папку Удаленные элементы и корневую папку для результатов поиска в хранилище сообщений.</span><span class="sxs-lookup"><span data-stu-id="0010c-121">When this flag is not set, **HrValidateIPMSubtree** checks for only the root folder for the subtree, the Deleted Items folder, and the root folder for message store search results.</span></span> 
  
<span data-ttu-id="0010c-122">Чтобы инициализировать хранилище сообщений, храните следующие свойства в памяти, чтобы они были легко доступны:</span><span class="sxs-lookup"><span data-stu-id="0010c-122">To initialize a message store, store the following properties in memory so that they are readily available:</span></span>
  
- <span data-ttu-id="0010c-123">**PR_VALID_FOLDER_MASK** [(PidTagValidFolderMask](pidtagvalidfoldermask-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="0010c-123">**PR_VALID_FOLDER_MASK** ([PidTagValidFolderMask](pidtagvalidfoldermask-canonical-property.md))</span></span>
    
- <span data-ttu-id="0010c-124">**PR_STORE_SUPPORT_MASK** [(PidTagStoreSupportMask)](pidtagstoresupportmask-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="0010c-124">**PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md))</span></span>
    
<span data-ttu-id="0010c-125">Эти свойства — битмаски, описывая функции магазина сообщений.</span><span class="sxs-lookup"><span data-stu-id="0010c-125">These properties are bitmasks that describe features of the message store.</span></span> <span data-ttu-id="0010c-126">**PR_VALID_FOLDER_MASK** имеет один бит для каждой специальной папки, которая существует в хранилище сообщений, и имеет допустимый идентификатор записи.</span><span class="sxs-lookup"><span data-stu-id="0010c-126">**PR_VALID_FOLDER_MASK** has one bit set for every special folder that exists in the message store and has an assigned entry identifier that is valid.</span></span> <span data-ttu-id="0010c-127">Дополнительные сведения о доступе к этим папкам и их идентификаторам записей см. в документе [Opening a Message Store Folder.](opening-a-message-store-folder.md)</span><span class="sxs-lookup"><span data-stu-id="0010c-127">For more information about accessing these folders and their entry identifiers, see [Opening a Message Store Folder](opening-a-message-store-folder.md).</span></span> 
  
 <span data-ttu-id="0010c-128">**PR_STORE_SUPPORT_MASK** имеет один бит для каждой функции, поддерживаемой в хранилище сообщений.</span><span class="sxs-lookup"><span data-stu-id="0010c-128">**PR_STORE_SUPPORT_MASK** has one bit set for every feature supported in the message store.</span></span> <span data-ttu-id="0010c-129">Например, если хранилище сообщений поддерживает уведомление и  форматированный текст, PR_STORE_SUPPORT_MASK его STORE_NOTIFY_OK и STORE_RTF_OK битов.</span><span class="sxs-lookup"><span data-stu-id="0010c-129">For example, if a message store supports notification and formatted text, its **PR_STORE_SUPPORT_MASK** will have the STORE_NOTIFY_OK and STORE_RTF_OK bits set.</span></span> 
  
<span data-ttu-id="0010c-130">Другие свойства, которые должны храниться локально, включают идентификаторы записей для папок, **которые** свойство PR_VALID_FOLDER_MASK описывает как допустимые.</span><span class="sxs-lookup"><span data-stu-id="0010c-130">Other properties that should be stored locally include the entry identifiers for the folders that the **PR_VALID_FOLDER_MASK** property describes as valid.</span></span> <span data-ttu-id="0010c-131">Каждая из этих специальных папок, за исключением папки "Входящие", имеет свойство идентификатора входа, связанное с ним.</span><span class="sxs-lookup"><span data-stu-id="0010c-131">Each of these special folders, except for the Inbox folder, has an entry identifier property associated with it.</span></span> <span data-ttu-id="0010c-132">Например, идентификатор входа для папки "Избокс" — это **свойство** [PR_IPM_OUTBOX_ENTRYID (PidTagIpIpmOutboxEntryId).](pidtagipmoutboxentryid-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="0010c-132">For example, the entry identifier for the Outbox folder is its **PR_IPM_OUTBOX_ENTRYID** ([PidTagIpmOutboxEntryId](pidtagipmoutboxentryid-canonical-property.md)) property.</span></span> <span data-ttu-id="0010c-133">Поскольку эти папки являются папками, которые будут открываться часто, лучше иметь их идентификаторы записи легко доступны.</span><span class="sxs-lookup"><span data-stu-id="0010c-133">Because these folders are the folders that will be opened frequently, it is a good idea to have their entry identifiers readily available.</span></span>
  

