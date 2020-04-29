---
title: Проверка и инициализация хранилища сообщений
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
# <a name="validating-and-initializing-a-message-store"></a><span data-ttu-id="cce8c-103">Проверка и инициализация хранилища сообщений</span><span class="sxs-lookup"><span data-stu-id="cce8c-103">Validating and Initializing a Message Store</span></span>

  
  
<span data-ttu-id="cce8c-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="cce8c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="cce8c-105">При открытии хранилища сообщений с помощью метода [IMAPISession:: опенмсгсторе](imapisession-openmsgstore.md) без установки флага MDB_NO_MAIL MAPI создает несколько папок и назначает им имена по умолчанию и роли.</span><span class="sxs-lookup"><span data-stu-id="cce8c-105">When you open a message store through the [IMAPISession::OpenMsgStore](imapisession-openmsgstore.md) method without setting the MDB_NO_MAIL flag, MAPI creates several folders and assigns them default names and roles.</span></span> <span data-ttu-id="cce8c-106">Служба MAPI отвечает за создание этих папок, чтобы избежать несовместимости, которые неизбежно возникать, если клиенты или поставщики хранилища сообщений несут ответственность за создание.</span><span class="sxs-lookup"><span data-stu-id="cce8c-106">MAPI is responsible for creating these folders to avoid the incompatibilities that would inevitably occur if either clients or message store providers were responsible for the creation.</span></span> 
  
<span data-ttu-id="cce8c-107">Иногда необходимо убедиться, что созданы соответствующие папки, и что они действительны.</span><span class="sxs-lookup"><span data-stu-id="cce8c-107">Sometimes it is necessary to verify that the appropriate folders have been created and that they are valid.</span></span> <span data-ttu-id="cce8c-108">Для этой цели доступна функция [хрвалидатеипмсубтри](hrvalidateipmsubtree.md) .</span><span class="sxs-lookup"><span data-stu-id="cce8c-108">The [HrValidateIPMSubtree](hrvalidateipmsubtree.md) function is available for this purpose.</span></span> <span data-ttu-id="cce8c-109">При проверке хранилища сообщений по умолчанию передайте флаг MAPI_FULL_IPM_TREE.</span><span class="sxs-lookup"><span data-stu-id="cce8c-109">If you are validating the default message store, pass the MAPI_FULL_IPM_TREE flag.</span></span> <span data-ttu-id="cce8c-110">Для хранилища сообщений по умолчанию создается более обширная группа папок.</span><span class="sxs-lookup"><span data-stu-id="cce8c-110">A more extensive group of folders is created for the default message store.</span></span> <span data-ttu-id="cce8c-111">Когда **хрвалидатеипмсубтри** получает флаг MAPI_FULL_IPM_TREE, он проверяет наличие следующих папок:</span><span class="sxs-lookup"><span data-stu-id="cce8c-111">When **HrValidateIPMSubtree** receives the MAPI_FULL_IPM_TREE flag, it checks for the following folders:</span></span> 
  
- <span data-ttu-id="cce8c-112">Корневая папка для поддерева IPM</span><span class="sxs-lookup"><span data-stu-id="cce8c-112">Root folder for the IPM subtree</span></span>
    
- <span data-ttu-id="cce8c-113">Папка "Удаленные" в корневой папке IPM</span><span class="sxs-lookup"><span data-stu-id="cce8c-113">Deleted Items folder in the IPM root folder</span></span>
    
- <span data-ttu-id="cce8c-114">Папка "Входящие" в корневой папке IPM</span><span class="sxs-lookup"><span data-stu-id="cce8c-114">Inbox folder in the IPM root folder</span></span>
    
- <span data-ttu-id="cce8c-115">Папка "Исходящие" в корневой папке IPM</span><span class="sxs-lookup"><span data-stu-id="cce8c-115">Outbox folder in the IPM root folder</span></span>
    
- <span data-ttu-id="cce8c-116">Папка "Отправленные" в корневой папке IPM</span><span class="sxs-lookup"><span data-stu-id="cce8c-116">Sent Items folder in the IPM root folder</span></span>
    
- <span data-ttu-id="cce8c-117">Представления папки в корневой папке хранилища сообщений</span><span class="sxs-lookup"><span data-stu-id="cce8c-117">Folder views in the message store's root folder</span></span>
    
- <span data-ttu-id="cce8c-118">Общие представления в корневой папке хранилища сообщений</span><span class="sxs-lookup"><span data-stu-id="cce8c-118">Common views in the message store's root folder</span></span>
    
- <span data-ttu-id="cce8c-119">Папка поиска в корневой папке хранилища сообщений</span><span class="sxs-lookup"><span data-stu-id="cce8c-119">Search folder in the message store's root folder</span></span>
    
<span data-ttu-id="cce8c-120">Если хранилище сообщений не является значением по умолчанию, можно установить или не устанавливать флаг MAPI_FULL_IPM_TREE.</span><span class="sxs-lookup"><span data-stu-id="cce8c-120">If the message store is not the default, you can either set or not set the MAPI_FULL_IPM_TREE flag.</span></span> <span data-ttu-id="cce8c-121">Если этот флаг не задан, **хрвалидатеипмсубтри** проверяет только корневую папку для поддерева, папки "Удаленные" и корневой папки для результатов поиска хранилища сообщений.</span><span class="sxs-lookup"><span data-stu-id="cce8c-121">When this flag is not set, **HrValidateIPMSubtree** checks for only the root folder for the subtree, the Deleted Items folder, and the root folder for message store search results.</span></span> 
  
<span data-ttu-id="cce8c-122">Чтобы инициализировать хранилище сообщений, сохраните следующие свойства в памяти, чтобы они были доступны для совместного доступа:</span><span class="sxs-lookup"><span data-stu-id="cce8c-122">To initialize a message store, store the following properties in memory so that they are readily available:</span></span>
  
- <span data-ttu-id="cce8c-123">**PR_VALID_FOLDER_MASK** ([PidTagValidFolderMask](pidtagvalidfoldermask-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="cce8c-123">**PR_VALID_FOLDER_MASK** ([PidTagValidFolderMask](pidtagvalidfoldermask-canonical-property.md))</span></span>
    
- <span data-ttu-id="cce8c-124">**PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="cce8c-124">**PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md))</span></span>
    
<span data-ttu-id="cce8c-125">Эти свойства представляют собой битовые маски, описывающие функции хранилища сообщений.</span><span class="sxs-lookup"><span data-stu-id="cce8c-125">These properties are bitmasks that describe features of the message store.</span></span> <span data-ttu-id="cce8c-126">В **PR_VALID_FOLDER_MASK** для каждой специальной папки, которая существует в хранилище сообщений, задан один бит, а также назначен допустимый идентификатор записи.</span><span class="sxs-lookup"><span data-stu-id="cce8c-126">**PR_VALID_FOLDER_MASK** has one bit set for every special folder that exists in the message store and has an assigned entry identifier that is valid.</span></span> <span data-ttu-id="cce8c-127">Дополнительные сведения о доступе к этим папкам и их идентификаторам записей можно узнать [в разделе Открытие папки хранилища сообщений](opening-a-message-store-folder.md).</span><span class="sxs-lookup"><span data-stu-id="cce8c-127">For more information about accessing these folders and their entry identifiers, see [Opening a Message Store Folder](opening-a-message-store-folder.md).</span></span> 
  
 <span data-ttu-id="cce8c-128">Для каждого компонента, поддерживаемого в банке сообщений, в **PR_STORE_SUPPORT_MASK** установлен один бит.</span><span class="sxs-lookup"><span data-stu-id="cce8c-128">**PR_STORE_SUPPORT_MASK** has one bit set for every feature supported in the message store.</span></span> <span data-ttu-id="cce8c-129">Например, если хранилище сообщений поддерживает уведомление и форматированный текст, для его **PR_STORE_SUPPORT_MASK** будут заданы STORE_NOTIFY_OK и STORE_RTF_OK BITS.</span><span class="sxs-lookup"><span data-stu-id="cce8c-129">For example, if a message store supports notification and formatted text, its **PR_STORE_SUPPORT_MASK** will have the STORE_NOTIFY_OK and STORE_RTF_OK bits set.</span></span> 
  
<span data-ttu-id="cce8c-130">К другим свойствам, которые должны храниться локально, относятся идентификаторы для папок, которые в качестве свойства **PR_VALID_FOLDER_MASK** описывает допустимые.</span><span class="sxs-lookup"><span data-stu-id="cce8c-130">Other properties that should be stored locally include the entry identifiers for the folders that the **PR_VALID_FOLDER_MASK** property describes as valid.</span></span> <span data-ttu-id="cce8c-131">Каждый из этих специальных папок, за исключением папки "Входящие", имеет связанное с ним свойство идентификатора записи.</span><span class="sxs-lookup"><span data-stu-id="cce8c-131">Each of these special folders, except for the Inbox folder, has an entry identifier property associated with it.</span></span> <span data-ttu-id="cce8c-132">Например, идентификатором записи для папки "Исходящие" является свойство **PR_IPM_OUTBOX_ENTRYID** ([PidTagIpmOutboxEntryId](pidtagipmoutboxentryid-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="cce8c-132">For example, the entry identifier for the Outbox folder is its **PR_IPM_OUTBOX_ENTRYID** ([PidTagIpmOutboxEntryId](pidtagipmoutboxentryid-canonical-property.md)) property.</span></span> <span data-ttu-id="cce8c-133">Так как эти папки представляют собой папки, которые будут открываться часто, рекомендуется иметь общедоступные идентификаторы записей.</span><span class="sxs-lookup"><span data-stu-id="cce8c-133">Because these folders are the folders that will be opened frequently, it is a good idea to have their entry identifiers readily available.</span></span>
  

