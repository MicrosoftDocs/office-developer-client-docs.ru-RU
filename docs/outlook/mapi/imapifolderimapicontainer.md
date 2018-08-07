---
title: IMAPIFolder IMAPIContainer
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFolder
api_type:
- COM
ms.assetid: bc2e8d17-7687-43c2-8f01-b677703f7288
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 64a64029c3507d9ac4b520076a44e23170dd9bd4
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19808885"
---
# <a name="imapifolder--imapicontainer"></a><span data-ttu-id="311e6-103">IMAPIFolder : IMAPIContainer</span><span class="sxs-lookup"><span data-stu-id="311e6-103">IMAPIFolder : IMAPIContainer</span></span>

  
  
<span data-ttu-id="311e6-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="311e6-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="311e6-105">Выполняет операции на сообщения и вложенных папок в папке.</span><span class="sxs-lookup"><span data-stu-id="311e6-105">Performs operations on the messages and subfolders in a folder.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="311e6-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="311e6-106">Header file:</span></span>  <br/> |<span data-ttu-id="311e6-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="311e6-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="311e6-108">Предоставляемые:</span><span class="sxs-lookup"><span data-stu-id="311e6-108">Exposed by:</span></span>  <br/> |<span data-ttu-id="311e6-109">Объекты папок</span><span class="sxs-lookup"><span data-stu-id="311e6-109">Folder objects</span></span>  <br/> |
|<span data-ttu-id="311e6-110">Реализованный:</span><span class="sxs-lookup"><span data-stu-id="311e6-110">Implemented by:</span></span>  <br/> |<span data-ttu-id="311e6-111">Поставщики хранилища сообщений</span><span class="sxs-lookup"><span data-stu-id="311e6-111">Message store providers</span></span>  <br/> |
|<span data-ttu-id="311e6-112">Вызывается:</span><span class="sxs-lookup"><span data-stu-id="311e6-112">Called by:</span></span>  <br/> |<span data-ttu-id="311e6-113">Клиентские приложения и MAPI</span><span class="sxs-lookup"><span data-stu-id="311e6-113">Client applications and MAPI</span></span>  <br/> |
|<span data-ttu-id="311e6-114">Идентификатор интерфейса:</span><span class="sxs-lookup"><span data-stu-id="311e6-114">Interface identifier:</span></span>  <br/> |<span data-ttu-id="311e6-115">IID_IMAPIFolder</span><span class="sxs-lookup"><span data-stu-id="311e6-115">IID_IMAPIFolder</span></span>  <br/> |
|<span data-ttu-id="311e6-116">Тип указателя:</span><span class="sxs-lookup"><span data-stu-id="311e6-116">Pointer type:</span></span>  <br/> |<span data-ttu-id="311e6-117">LPMAPIFOLDER</span><span class="sxs-lookup"><span data-stu-id="311e6-117">LPMAPIFOLDER</span></span>  <br/> |
|<span data-ttu-id="311e6-118">Модель транзакций:</span><span class="sxs-lookup"><span data-stu-id="311e6-118">Transaction model:</span></span>  <br/> |<span data-ttu-id="311e6-119">Не входящих в транзакции</span><span class="sxs-lookup"><span data-stu-id="311e6-119">Nontransacted</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="311e6-120">Порядке vtable</span><span class="sxs-lookup"><span data-stu-id="311e6-120">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="311e6-121">CreateMessage</span><span class="sxs-lookup"><span data-stu-id="311e6-121">CreateMessage</span></span>](imapifolder-createmessage.md) <br/> |<span data-ttu-id="311e6-122">Создает новое сообщение.</span><span class="sxs-lookup"><span data-stu-id="311e6-122">Creates a new message.</span></span>  <br/> |
|[<span data-ttu-id="311e6-123">CopyMessages</span><span class="sxs-lookup"><span data-stu-id="311e6-123">CopyMessages</span></span>](imapifolder-copymessages.md) <br/> |<span data-ttu-id="311e6-124">Копирование или перемещение одно или несколько сообщений.</span><span class="sxs-lookup"><span data-stu-id="311e6-124">Copies or moves one or more messages.</span></span>  <br/> |
|[<span data-ttu-id="311e6-125">DeleteMessages</span><span class="sxs-lookup"><span data-stu-id="311e6-125">DeleteMessages</span></span>](imapifolder-deletemessages.md) <br/> |<span data-ttu-id="311e6-126">Удаляет одно или несколько сообщений.</span><span class="sxs-lookup"><span data-stu-id="311e6-126">Deletes one or more messages.</span></span>  <br/> |
|[<span data-ttu-id="311e6-127">CreateFolder</span><span class="sxs-lookup"><span data-stu-id="311e6-127">CreateFolder</span></span>](imapifolder-createfolder.md) <br/> |<span data-ttu-id="311e6-128">Создает папку.</span><span class="sxs-lookup"><span data-stu-id="311e6-128">Creates a new subfolder.</span></span>  <br/> |
|[<span data-ttu-id="311e6-129">CopyFolder</span><span class="sxs-lookup"><span data-stu-id="311e6-129">CopyFolder</span></span>](imapifolder-copyfolder.md) <br/> |<span data-ttu-id="311e6-130">Копирование или перемещение вложенной папке.</span><span class="sxs-lookup"><span data-stu-id="311e6-130">Copies or moves a subfolder.</span></span>  <br/> |
|[<span data-ttu-id="311e6-131">DeleteFolder</span><span class="sxs-lookup"><span data-stu-id="311e6-131">DeleteFolder</span></span>](imapifolder-deletefolder.md) <br/> |<span data-ttu-id="311e6-132">Удаляет вложенной папке.</span><span class="sxs-lookup"><span data-stu-id="311e6-132">Deletes a subfolder.</span></span>  <br/> |
|[<span data-ttu-id="311e6-133">SetReadFlags</span><span class="sxs-lookup"><span data-stu-id="311e6-133">SetReadFlags</span></span>](imapifolder-setreadflags.md) <br/> |<span data-ttu-id="311e6-134">Задает или сбрасывает MSGFLAG_READ в свойстве **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) из одного или нескольких сообщений, папок и управляет Отправка чтения отчеты.</span><span class="sxs-lookup"><span data-stu-id="311e6-134">Sets or clears the MSGFLAG_READ flag in the **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) property of one or more of the folder's messages, and manages the sending of read reports.</span></span>  <br/> |
|[<span data-ttu-id="311e6-135">GetMessageStatus</span><span class="sxs-lookup"><span data-stu-id="311e6-135">GetMessageStatus</span></span>](imapifolder-getmessagestatus.md) <br/> |<span data-ttu-id="311e6-136">Получение сведений о состоянии, связанные с сообщение в определенной папке.</span><span class="sxs-lookup"><span data-stu-id="311e6-136">Obtains the status associated with a message in a particular folder.</span></span>  <br/> |
|[<span data-ttu-id="311e6-137">SetMessageStatus</span><span class="sxs-lookup"><span data-stu-id="311e6-137">SetMessageStatus</span></span>](imapifolder-setmessagestatus.md) <br/> |<span data-ttu-id="311e6-138">Задание состояния, связанный с сообщением.</span><span class="sxs-lookup"><span data-stu-id="311e6-138">Sets the status associated with a message.</span></span>  <br/> |
|[<span data-ttu-id="311e6-139">SaveContentsSort</span><span class="sxs-lookup"><span data-stu-id="311e6-139">SaveContentsSort</span></span>](imapifolder-savecontentssort.md) <br/> |<span data-ttu-id="311e6-140">Задает порядок сортировки по умолчанию для папки содержимое таблицы.</span><span class="sxs-lookup"><span data-stu-id="311e6-140">Sets the default sort order for a folder's contents table.</span></span>  <br/> |
|[<span data-ttu-id="311e6-141">EmptyFolder</span><span class="sxs-lookup"><span data-stu-id="311e6-141">EmptyFolder</span></span>](imapifolder-emptyfolder.md) <br/> |<span data-ttu-id="311e6-142">Удаляет все сообщения и вложенные папки из папки без удаления самой папке.</span><span class="sxs-lookup"><span data-stu-id="311e6-142">Deletes all messages and subfolders from a folder without deleting the folder itself.</span></span>  <br/> |
   
|<span data-ttu-id="311e6-143">**Обязательные свойства**</span><span class="sxs-lookup"><span data-stu-id="311e6-143">**Required properties**</span></span>|<span data-ttu-id="311e6-144">**Access**</span><span class="sxs-lookup"><span data-stu-id="311e6-144">**Access**</span></span>|
|:-----|:-----|
|<span data-ttu-id="311e6-145">**PR_DISPLAY_NAME** ([PidTagDisplayNamePrefix](pidtagdisplaynameprefix-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="311e6-145">**PR_DISPLAY_NAME** ([PidTagDisplayNamePrefix](pidtagdisplaynameprefix-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="311e6-146">Чтение и запись</span><span class="sxs-lookup"><span data-stu-id="311e6-146">Read/write</span></span>  <br/> |
|<span data-ttu-id="311e6-147">**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="311e6-147">**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="311e6-148">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="311e6-148">Read-only</span></span>  <br/> |
|<span data-ttu-id="311e6-149">**PR_FOLDER_TYPE** ([PidTagFolderType](pidtagfoldertype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="311e6-149">**PR_FOLDER_TYPE** ([PidTagFolderType](pidtagfoldertype-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="311e6-150">Чтение и запись</span><span class="sxs-lookup"><span data-stu-id="311e6-150">Read/write</span></span>  <br/> |
|<span data-ttu-id="311e6-151">**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="311e6-151">**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="311e6-152">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="311e6-152">Read-only</span></span>  <br/> |
|<span data-ttu-id="311e6-153">**PR_PARENT_ENTRYID** ([PidTagParentEntryId](pidtagparententryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="311e6-153">**PR_PARENT_ENTRYID** ([PidTagParentEntryId](pidtagparententryid-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="311e6-154">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="311e6-154">Read-only</span></span>  <br/> |
|<span data-ttu-id="311e6-155">**PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="311e6-155">**PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="311e6-156">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="311e6-156">Read-only</span></span>  <br/> |
|<span data-ttu-id="311e6-157">**PR_STORE_ENTRYID** ([PidTagStoreEntryId](pidtagstoreentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="311e6-157">**PR_STORE_ENTRYID** ([PidTagStoreEntryId](pidtagstoreentryid-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="311e6-158">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="311e6-158">Read-only</span></span>  <br/> |
|<span data-ttu-id="311e6-159">**PR_STORE_RECORD_KEY** ([PidTagStoreRecordKey](pidtagstorerecordkey-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="311e6-159">**PR_STORE_RECORD_KEY** ([PidTagStoreRecordKey](pidtagstorerecordkey-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="311e6-160">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="311e6-160">Read-only</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="311e6-161">См. также</span><span class="sxs-lookup"><span data-stu-id="311e6-161">See also</span></span>



[<span data-ttu-id="311e6-162">Интерфейсы MAPI</span><span class="sxs-lookup"><span data-stu-id="311e6-162">MAPI Interfaces</span></span>](mapi-interfaces.md)

