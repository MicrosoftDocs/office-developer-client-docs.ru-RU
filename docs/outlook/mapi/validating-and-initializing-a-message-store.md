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
ms.openlocfilehash: 48883ec33db9ffd6b3e7cc6e16ae9c2487a31607
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19812601"
---
# <a name="validating-and-initializing-a-message-store"></a><span data-ttu-id="1e464-103">Проверка и инициализация хранилища сообщений</span><span class="sxs-lookup"><span data-stu-id="1e464-103">Validating and Initializing a Message Store</span></span>

  
  
<span data-ttu-id="1e464-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="1e464-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="1e464-105">При открытии хранилища сообщений через метод [IMAPISession::OpenMsgStore](imapisession-openmsgstore.md) без установки флага MDB_NO_MAIL MAPI создается несколько папок и присваивает им имена по умолчанию и роли.</span><span class="sxs-lookup"><span data-stu-id="1e464-105">When you open a message store through the [IMAPISession::OpenMsgStore](imapisession-openmsgstore.md) method without setting the MDB_NO_MAIL flag, MAPI creates several folders and assigns them default names and roles.</span></span> <span data-ttu-id="1e464-106">MAPI несет ответственность за создание этих папок, чтобы избежать несовместимости, неизменно может возникать, если были ответственность за создание клиентов или поставщиков хранилища сообщений.</span><span class="sxs-lookup"><span data-stu-id="1e464-106">MAPI is responsible for creating these folders to avoid the incompatibilities that would inevitably occur if either clients or message store providers were responsible for the creation.</span></span> 
  
<span data-ttu-id="1e464-107">Иногда бывает необходимо убедиться, что были созданы соответствующие папки и что они действительны.</span><span class="sxs-lookup"><span data-stu-id="1e464-107">Sometimes it is necessary to verify that the appropriate folders have been created and that they are valid.</span></span> <span data-ttu-id="1e464-108">Функция [HrValidateIPMSubtree](hrvalidateipmsubtree.md) доступна для этой цели.</span><span class="sxs-lookup"><span data-stu-id="1e464-108">The [HrValidateIPMSubtree](hrvalidateipmsubtree.md) function is available for this purpose.</span></span> <span data-ttu-id="1e464-109">При проверке хранилище сообщений по умолчанию, передайте флаг MAPI_FULL_IPM_TREE.</span><span class="sxs-lookup"><span data-stu-id="1e464-109">If you are validating the default message store, pass the MAPI_FULL_IPM_TREE flag.</span></span> <span data-ttu-id="1e464-110">Расширенный группы папок будет создан хранилище сообщений по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="1e464-110">A more extensive group of folders is created for the default message store.</span></span> <span data-ttu-id="1e464-111">Когда **HrValidateIPMSubtree** Получает флаг MAPI_FULL_IPM_TREE, проверяет наличие следующих папках:</span><span class="sxs-lookup"><span data-stu-id="1e464-111">When **HrValidateIPMSubtree** receives the MAPI_FULL_IPM_TREE flag, it checks for the following folders:</span></span> 
  
- <span data-ttu-id="1e464-112">Корневой папки для поддерева IPM</span><span class="sxs-lookup"><span data-stu-id="1e464-112">Root folder for the IPM subtree</span></span>
    
- <span data-ttu-id="1e464-113">Папка "Удаленные" в корневой папке IPM</span><span class="sxs-lookup"><span data-stu-id="1e464-113">Deleted Items folder in the IPM root folder</span></span>
    
- <span data-ttu-id="1e464-114">Папка "Входящие" в корневой папке IPM</span><span class="sxs-lookup"><span data-stu-id="1e464-114">Inbox folder in the IPM root folder</span></span>
    
- <span data-ttu-id="1e464-115">Исходящие папки в корневой папке IPM</span><span class="sxs-lookup"><span data-stu-id="1e464-115">Outbox folder in the IPM root folder</span></span>
    
- <span data-ttu-id="1e464-116">Папка «Отправленные» в корневой папке IPM</span><span class="sxs-lookup"><span data-stu-id="1e464-116">Sent Items folder in the IPM root folder</span></span>
    
- <span data-ttu-id="1e464-117">Представления папок в корневой папке хранилища сообщений</span><span class="sxs-lookup"><span data-stu-id="1e464-117">Folder views in the message store's root folder</span></span>
    
- <span data-ttu-id="1e464-118">Общие представления в корневую папку хранилища сообщений</span><span class="sxs-lookup"><span data-stu-id="1e464-118">Common views in the message store's root folder</span></span>
    
- <span data-ttu-id="1e464-119">Папки поиска в корневую папку хранилища сообщений</span><span class="sxs-lookup"><span data-stu-id="1e464-119">Search folder in the message store's root folder</span></span>
    
<span data-ttu-id="1e464-120">Если хранилище сообщений не по умолчанию, можно задать или не задан флаг MAPI_FULL_IPM_TREE.</span><span class="sxs-lookup"><span data-stu-id="1e464-120">If the message store is not the default, you can either set or not set the MAPI_FULL_IPM_TREE flag.</span></span> <span data-ttu-id="1e464-121">Если этот флаг не задан, **HrValidateIPMSubtree** проверяет наличие только корневой папки для поддерева, папки «Удаленные», корневой папки для сообщения хранилища и результатов поиска.</span><span class="sxs-lookup"><span data-stu-id="1e464-121">When this flag is not set, **HrValidateIPMSubtree** checks for only the root folder for the subtree, the Deleted Items folder, and the root folder for message store search results.</span></span> 
  
<span data-ttu-id="1e464-122">Для инициализации хранилища сообщений, хранят следующие свойства в памяти, чтобы они были легко доступны.</span><span class="sxs-lookup"><span data-stu-id="1e464-122">To initialize a message store, store the following properties in memory so that they are readily available:</span></span>
  
- <span data-ttu-id="1e464-123">**PR_VALID_FOLDER_MASK** ([PidTagValidFolderMask](pidtagvalidfoldermask-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="1e464-123">**PR_VALID_FOLDER_MASK** ([PidTagValidFolderMask](pidtagvalidfoldermask-canonical-property.md))</span></span>
    
- <span data-ttu-id="1e464-124">**PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="1e464-124">**PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md))</span></span>
    
<span data-ttu-id="1e464-125">Эти свойства — это битовой маски, описаны функции хранилища сообщений.</span><span class="sxs-lookup"><span data-stu-id="1e464-125">These properties are bitmasks that describe features of the message store.</span></span> <span data-ttu-id="1e464-126">**PR_VALID_FOLDER_MASK** имеет одно битовое значение для каждой отдельной папки, который существует в хранилище сообщений и имеет идентификатор назначенный запись, который является допустимым.</span><span class="sxs-lookup"><span data-stu-id="1e464-126">**PR_VALID_FOLDER_MASK** has one bit set for every special folder that exists in the message store and has an assigned entry identifier that is valid.</span></span> <span data-ttu-id="1e464-127">Дополнительные сведения о доступе к этим папкам и их идентификаторы записей можно [Открытие папки хранения сообщений](opening-a-message-store-folder.md).</span><span class="sxs-lookup"><span data-stu-id="1e464-127">For more information about accessing these folders and their entry identifiers, see [Opening a Message Store Folder](opening-a-message-store-folder.md).</span></span> 
  
 <span data-ttu-id="1e464-128">**PR_STORE_SUPPORT_MASK** имеет одно битовое значение для каждой функции, поддерживаемые в хранилище сообщений.</span><span class="sxs-lookup"><span data-stu-id="1e464-128">**PR_STORE_SUPPORT_MASK** has one bit set for every feature supported in the message store.</span></span> <span data-ttu-id="1e464-129">К примеру Если хранилища сообщений поддерживает уведомления и форматированный текст, его **PR_STORE_SUPPORT_MASK** будут иметь набор битов STORE_NOTIFY_OK и STORE_RTF_OK.</span><span class="sxs-lookup"><span data-stu-id="1e464-129">For example, if a message store supports notification and formatted text, its **PR_STORE_SUPPORT_MASK** will have the STORE_NOTIFY_OK and STORE_RTF_OK bits set.</span></span> 
  
<span data-ttu-id="1e464-130">Другие свойства, которые должны сохраняться локально включают идентификаторы записей для папки, в которых описываются свойства **PR_VALID_FOLDER_MASK** как допустимый.</span><span class="sxs-lookup"><span data-stu-id="1e464-130">Other properties that should be stored locally include the entry identifiers for the folders that the **PR_VALID_FOLDER_MASK** property describes as valid.</span></span> <span data-ttu-id="1e464-131">Каждый из этих папок, за исключением папке "Входящие" имеет свойство идентификатор записи связанных с ним.</span><span class="sxs-lookup"><span data-stu-id="1e464-131">Each of these special folders, except for the Inbox folder, has an entry identifier property associated with it.</span></span> <span data-ttu-id="1e464-132">Например идентификатор записи для папки "Исходящие" — это его свойство **PR_IPM_OUTBOX_ENTRYID** ([PidTagIpmOutboxEntryId](pidtagipmoutboxentryid-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="1e464-132">For example, the entry identifier for the Outbox folder is its **PR_IPM_OUTBOX_ENTRYID** ([PidTagIpmOutboxEntryId](pidtagipmoutboxentryid-canonical-property.md)) property.</span></span> <span data-ttu-id="1e464-133">Так как эти папки все папках, которые будут открывать часто, рекомендуется иметь быстрый доступ к идентификаторам запись.</span><span class="sxs-lookup"><span data-stu-id="1e464-133">Because these folders are the folders that will be opened frequently, it is a good idea to have their entry identifiers readily available.</span></span>
  

