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
# <a name="validating-and-initializing-a-message-store"></a><span data-ttu-id="20a6f-103">Проверка и инициализация магазина сообщений</span><span class="sxs-lookup"><span data-stu-id="20a6f-103">Validating and Initializing a Message Store</span></span>

  
  
<span data-ttu-id="20a6f-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="20a6f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="20a6f-105">Когда вы открываете хранилище сообщений с помощью метода [IMAPISession::OpenMsgStore](imapisession-openmsgstore.md) без установки флага MDB_NO_MAIL, MAPI создает несколько папок и назначает им имена и роли по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="20a6f-105">When you open a message store through the [IMAPISession::OpenMsgStore](imapisession-openmsgstore.md) method without setting the MDB_NO_MAIL flag, MAPI creates several folders and assigns them default names and roles.</span></span> <span data-ttu-id="20a6f-106">MAPI отвечает за создание этих папок, чтобы избежать несовместимостей, которые неизбежно возникнут, если за создание отвечает клиенты или поставщики store сообщений.</span><span class="sxs-lookup"><span data-stu-id="20a6f-106">MAPI is responsible for creating these folders to avoid the incompatibilities that would inevitably occur if either clients or message store providers were responsible for the creation.</span></span> 
  
<span data-ttu-id="20a6f-107">Иногда необходимо проверить, созданы ли соответствующие папки и являются ли они действительными.</span><span class="sxs-lookup"><span data-stu-id="20a6f-107">Sometimes it is necessary to verify that the appropriate folders have been created and that they are valid.</span></span> <span data-ttu-id="20a6f-108">Функция [HrValidateIPMSubtree](hrvalidateipmsubtree.md) доступна для этой цели.</span><span class="sxs-lookup"><span data-stu-id="20a6f-108">The [HrValidateIPMSubtree](hrvalidateipmsubtree.md) function is available for this purpose.</span></span> <span data-ttu-id="20a6f-109">При проверке стандартного хранения сообщений передай флаг MAPI_FULL_IPM_TREE сообщений.</span><span class="sxs-lookup"><span data-stu-id="20a6f-109">If you are validating the default message store, pass the MAPI_FULL_IPM_TREE flag.</span></span> <span data-ttu-id="20a6f-110">Для хранения сообщений по умолчанию создается более широкая группа папок.</span><span class="sxs-lookup"><span data-stu-id="20a6f-110">A more extensive group of folders is created for the default message store.</span></span> <span data-ttu-id="20a6f-111">Когда **HrValidateIPMSubtree** получает флаг MAPI_FULL_IPM_TREE, он проверяет наличие следующих папок:</span><span class="sxs-lookup"><span data-stu-id="20a6f-111">When **HrValidateIPMSubtree** receives the MAPI_FULL_IPM_TREE flag, it checks for the following folders:</span></span> 
  
- <span data-ttu-id="20a6f-112">Корневая папка для поддерево IPM</span><span class="sxs-lookup"><span data-stu-id="20a6f-112">Root folder for the IPM subtree</span></span>
    
- <span data-ttu-id="20a6f-113">Папка "Удаленные" в корневой папке IPM</span><span class="sxs-lookup"><span data-stu-id="20a6f-113">Deleted Items folder in the IPM root folder</span></span>
    
- <span data-ttu-id="20a6f-114">Папка "Входящие" в корневой папке IPM</span><span class="sxs-lookup"><span data-stu-id="20a6f-114">Inbox folder in the IPM root folder</span></span>
    
- <span data-ttu-id="20a6f-115">Папка "Outbox" в корневой папке IPM</span><span class="sxs-lookup"><span data-stu-id="20a6f-115">Outbox folder in the IPM root folder</span></span>
    
- <span data-ttu-id="20a6f-116">Папка "Отправленные" в корневой папке IPM</span><span class="sxs-lookup"><span data-stu-id="20a6f-116">Sent Items folder in the IPM root folder</span></span>
    
- <span data-ttu-id="20a6f-117">Представления папок в корневой папке хранения сообщений</span><span class="sxs-lookup"><span data-stu-id="20a6f-117">Folder views in the message store's root folder</span></span>
    
- <span data-ttu-id="20a6f-118">Общие представления в корневой папке хранения сообщений</span><span class="sxs-lookup"><span data-stu-id="20a6f-118">Common views in the message store's root folder</span></span>
    
- <span data-ttu-id="20a6f-119">Папка поиска в корневой папке хранения сообщений</span><span class="sxs-lookup"><span data-stu-id="20a6f-119">Search folder in the message store's root folder</span></span>
    
<span data-ttu-id="20a6f-120">Если хранилище сообщений не является хранилищем по умолчанию, вы можете установить или не установить флаг MAPI_FULL_IPM_TREE сообщений.</span><span class="sxs-lookup"><span data-stu-id="20a6f-120">If the message store is not the default, you can either set or not set the MAPI_FULL_IPM_TREE flag.</span></span> <span data-ttu-id="20a6f-121">Если этот флаг не установлен, **HrValidateIPMSubtree** проверяет только корневую папку для поддерева, папку "Удаленные" и корневую папку для результатов поиска в хранилище сообщений.</span><span class="sxs-lookup"><span data-stu-id="20a6f-121">When this flag is not set, **HrValidateIPMSubtree** checks for only the root folder for the subtree, the Deleted Items folder, and the root folder for message store search results.</span></span> 
  
<span data-ttu-id="20a6f-122">Чтобы инициализировать хранилище сообщений, храните в памяти следующие свойства, чтобы они были доступны:</span><span class="sxs-lookup"><span data-stu-id="20a6f-122">To initialize a message store, store the following properties in memory so that they are readily available:</span></span>
  
- <span data-ttu-id="20a6f-123">**PR_VALID_FOLDER_MASK** ([PidTagValidFolderMask)](pidtagvalidfoldermask-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="20a6f-123">**PR_VALID_FOLDER_MASK** ([PidTagValidFolderMask](pidtagvalidfoldermask-canonical-property.md))</span></span>
    
- <span data-ttu-id="20a6f-124">**PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask)](pidtagstoresupportmask-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="20a6f-124">**PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md))</span></span>
    
<span data-ttu-id="20a6f-125">Эти свойства являются битами, которые описывают функции хранения сообщений.</span><span class="sxs-lookup"><span data-stu-id="20a6f-125">These properties are bitmasks that describe features of the message store.</span></span> <span data-ttu-id="20a6f-126">**PR_VALID_FOLDER_MASK** имеет один бит для каждой специальной папки, которая существует в хранилище сообщений, и имеет действительный идентификатор назначенной записи.</span><span class="sxs-lookup"><span data-stu-id="20a6f-126">**PR_VALID_FOLDER_MASK** has one bit set for every special folder that exists in the message store and has an assigned entry identifier that is valid.</span></span> <span data-ttu-id="20a6f-127">Дополнительные сведения о доступе к этим папок и их идентификаторам записей см. в открываемой папке [магазина сообщений.](opening-a-message-store-folder.md)</span><span class="sxs-lookup"><span data-stu-id="20a6f-127">For more information about accessing these folders and their entry identifiers, see [Opening a Message Store Folder](opening-a-message-store-folder.md).</span></span> 
  
 <span data-ttu-id="20a6f-128">**PR_STORE_SUPPORT_MASK** каждый из функций, поддерживаемых в хранилище сообщений, имеет по одному биту.</span><span class="sxs-lookup"><span data-stu-id="20a6f-128">**PR_STORE_SUPPORT_MASK** has one bit set for every feature supported in the message store.</span></span> <span data-ttu-id="20a6f-129">Например, если хранилище сообщений поддерживает уведомление и  форматированный текст, PR_STORE_SUPPORT_MASK его STORE_NOTIFY_OK и STORE_RTF_OK биты.</span><span class="sxs-lookup"><span data-stu-id="20a6f-129">For example, if a message store supports notification and formatted text, its **PR_STORE_SUPPORT_MASK** will have the STORE_NOTIFY_OK and STORE_RTF_OK bits set.</span></span> 
  
<span data-ttu-id="20a6f-130">Другие свойства, которые должны храниться локально, включают идентификаторы записей для папок, **которые** свойство PR_VALID_FOLDER_MASK как допустимые.</span><span class="sxs-lookup"><span data-stu-id="20a6f-130">Other properties that should be stored locally include the entry identifiers for the folders that the **PR_VALID_FOLDER_MASK** property describes as valid.</span></span> <span data-ttu-id="20a6f-131">Каждая из этих специальных папок, кроме папки "Входящие", имеет связанное с ней свойство идентификатора записи.</span><span class="sxs-lookup"><span data-stu-id="20a6f-131">Each of these special folders, except for the Inbox folder, has an entry identifier property associated with it.</span></span> <span data-ttu-id="20a6f-132">Например, идентификатором записи для папки "Outbox" является свойство **PR_IPM_OUTBOX_ENTRYID** ([PidTagIpmOutboxEntryId).](pidtagipmoutboxentryid-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="20a6f-132">For example, the entry identifier for the Outbox folder is its **PR_IPM_OUTBOX_ENTRYID** ([PidTagIpmOutboxEntryId](pidtagipmoutboxentryid-canonical-property.md)) property.</span></span> <span data-ttu-id="20a6f-133">Так как эти папки являются папками, которые будут открываться часто, лучше, чтобы их идентификаторы записей были легко доступны.</span><span class="sxs-lookup"><span data-stu-id="20a6f-133">Because these folders are the folders that will be opened frequently, it is a good idea to have their entry identifiers readily available.</span></span>
  

