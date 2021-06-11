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
ms.openlocfilehash: 5e31896354141999e02f2cba117ef9739340be61
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33424240"
---
# <a name="imapifolder--imapicontainer"></a><span data-ttu-id="51b66-103">IMAPIFolder : IMAPIContainer</span><span class="sxs-lookup"><span data-stu-id="51b66-103">IMAPIFolder : IMAPIContainer</span></span>

  
  
<span data-ttu-id="51b66-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="51b66-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="51b66-105">Выполняет операции на сообщениях и подмостках в папке.</span><span class="sxs-lookup"><span data-stu-id="51b66-105">Performs operations on the messages and subfolders in a folder.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="51b66-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="51b66-106">Header file:</span></span>  <br/> |<span data-ttu-id="51b66-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="51b66-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="51b66-108">Подвергается:</span><span class="sxs-lookup"><span data-stu-id="51b66-108">Exposed by:</span></span>  <br/> |<span data-ttu-id="51b66-109">Объекты папок</span><span class="sxs-lookup"><span data-stu-id="51b66-109">Folder objects</span></span>  <br/> |
|<span data-ttu-id="51b66-110">Реализовано в:</span><span class="sxs-lookup"><span data-stu-id="51b66-110">Implemented by:</span></span>  <br/> |<span data-ttu-id="51b66-111">Поставщики магазинов сообщений</span><span class="sxs-lookup"><span data-stu-id="51b66-111">Message store providers</span></span>  <br/> |
|<span data-ttu-id="51b66-112">Вызывающая сторона:</span><span class="sxs-lookup"><span data-stu-id="51b66-112">Called by:</span></span>  <br/> |<span data-ttu-id="51b66-113">Клиентские приложения и MAPI</span><span class="sxs-lookup"><span data-stu-id="51b66-113">Client applications and MAPI</span></span>  <br/> |
|<span data-ttu-id="51b66-114">Идентификатор интерфейса:</span><span class="sxs-lookup"><span data-stu-id="51b66-114">Interface identifier:</span></span>  <br/> |<span data-ttu-id="51b66-115">IID_IMAPIFolder</span><span class="sxs-lookup"><span data-stu-id="51b66-115">IID_IMAPIFolder</span></span>  <br/> |
|<span data-ttu-id="51b66-116">Тип указателя:</span><span class="sxs-lookup"><span data-stu-id="51b66-116">Pointer type:</span></span>  <br/> |<span data-ttu-id="51b66-117">LPMAPIFOLDER</span><span class="sxs-lookup"><span data-stu-id="51b66-117">LPMAPIFOLDER</span></span>  <br/> |
|<span data-ttu-id="51b66-118">Модель транзакции:</span><span class="sxs-lookup"><span data-stu-id="51b66-118">Transaction model:</span></span>  <br/> |<span data-ttu-id="51b66-119">Nontransacted</span><span class="sxs-lookup"><span data-stu-id="51b66-119">Nontransacted</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="51b66-120">Заказ Vtable</span><span class="sxs-lookup"><span data-stu-id="51b66-120">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="51b66-121">CreateMessage</span><span class="sxs-lookup"><span data-stu-id="51b66-121">CreateMessage</span></span>](imapifolder-createmessage.md) <br/> |<span data-ttu-id="51b66-122">Создает новое сообщение.</span><span class="sxs-lookup"><span data-stu-id="51b66-122">Creates a new message.</span></span>  <br/> |
|[<span data-ttu-id="51b66-123">CopyMessages</span><span class="sxs-lookup"><span data-stu-id="51b66-123">CopyMessages</span></span>](imapifolder-copymessages.md) <br/> |<span data-ttu-id="51b66-124">Копирует или перемещает одно или несколько сообщений.</span><span class="sxs-lookup"><span data-stu-id="51b66-124">Copies or moves one or more messages.</span></span>  <br/> |
|[<span data-ttu-id="51b66-125">DeleteMessages</span><span class="sxs-lookup"><span data-stu-id="51b66-125">DeleteMessages</span></span>](imapifolder-deletemessages.md) <br/> |<span data-ttu-id="51b66-126">Удаляет одно или несколько сообщений.</span><span class="sxs-lookup"><span data-stu-id="51b66-126">Deletes one or more messages.</span></span>  <br/> |
|[<span data-ttu-id="51b66-127">CreateFolder</span><span class="sxs-lookup"><span data-stu-id="51b66-127">CreateFolder</span></span>](imapifolder-createfolder.md) <br/> |<span data-ttu-id="51b66-128">Создает новый подмосток.</span><span class="sxs-lookup"><span data-stu-id="51b66-128">Creates a new subfolder.</span></span>  <br/> |
|[<span data-ttu-id="51b66-129">CopyFolder</span><span class="sxs-lookup"><span data-stu-id="51b66-129">CopyFolder</span></span>](imapifolder-copyfolder.md) <br/> |<span data-ttu-id="51b66-130">Копирует или перемещает подмостки.</span><span class="sxs-lookup"><span data-stu-id="51b66-130">Copies or moves a subfolder.</span></span>  <br/> |
|[<span data-ttu-id="51b66-131">DeleteFolder</span><span class="sxs-lookup"><span data-stu-id="51b66-131">DeleteFolder</span></span>](imapifolder-deletefolder.md) <br/> |<span data-ttu-id="51b66-132">Удаляет подмостки.</span><span class="sxs-lookup"><span data-stu-id="51b66-132">Deletes a subfolder.</span></span>  <br/> |
|[<span data-ttu-id="51b66-133">SetReadFlags</span><span class="sxs-lookup"><span data-stu-id="51b66-133">SetReadFlags</span></span>](imapifolder-setreadflags.md) <br/> |<span data-ttu-id="51b66-134">Задает или очищает флаг MSGFLAG_READ в **PR_MESSAGE_FLAGS** [(PidTagMessageFlags)](pidtagmessageflags-canonical-property.md)свойства одного или более сообщений папки и управляет отправкой отчетов о считывке.</span><span class="sxs-lookup"><span data-stu-id="51b66-134">Sets or clears the MSGFLAG_READ flag in the **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) property of one or more of the folder's messages, and manages the sending of read reports.</span></span>  <br/> |
|[<span data-ttu-id="51b66-135">GetMessageStatus</span><span class="sxs-lookup"><span data-stu-id="51b66-135">GetMessageStatus</span></span>](imapifolder-getmessagestatus.md) <br/> |<span data-ttu-id="51b66-136">Получает состояние, связанное с сообщением в определенной папке.</span><span class="sxs-lookup"><span data-stu-id="51b66-136">Obtains the status associated with a message in a particular folder.</span></span>  <br/> |
|[<span data-ttu-id="51b66-137">SetMessageStatus</span><span class="sxs-lookup"><span data-stu-id="51b66-137">SetMessageStatus</span></span>](imapifolder-setmessagestatus.md) <br/> |<span data-ttu-id="51b66-138">Задает состояние, связанное с сообщением.</span><span class="sxs-lookup"><span data-stu-id="51b66-138">Sets the status associated with a message.</span></span>  <br/> |
|[<span data-ttu-id="51b66-139">SaveContentsSort</span><span class="sxs-lookup"><span data-stu-id="51b66-139">SaveContentsSort</span></span>](imapifolder-savecontentssort.md) <br/> |<span data-ttu-id="51b66-140">Задает порядок сортировки по умолчанию для таблицы содержимого папки.</span><span class="sxs-lookup"><span data-stu-id="51b66-140">Sets the default sort order for a folder's contents table.</span></span>  <br/> |
|[<span data-ttu-id="51b66-141">EmptyFolder</span><span class="sxs-lookup"><span data-stu-id="51b66-141">EmptyFolder</span></span>](imapifolder-emptyfolder.md) <br/> |<span data-ttu-id="51b66-142">Удаляет все сообщения и подмостки из папки без удаления самой папки.</span><span class="sxs-lookup"><span data-stu-id="51b66-142">Deletes all messages and subfolders from a folder without deleting the folder itself.</span></span>  <br/> |
   
|<span data-ttu-id="51b66-143">**Обязательные свойства**</span><span class="sxs-lookup"><span data-stu-id="51b66-143">**Required properties**</span></span>|<span data-ttu-id="51b66-144">**Access**</span><span class="sxs-lookup"><span data-stu-id="51b66-144">**Access**</span></span>|
|:-----|:-----|
|<span data-ttu-id="51b66-145">**PR_DISPLAY_NAME** [(PidTagDisplayNamePrefix)](pidtagdisplaynameprefix-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="51b66-145">**PR_DISPLAY_NAME** ([PidTagDisplayNamePrefix](pidtagdisplaynameprefix-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="51b66-146">Чтение и запись</span><span class="sxs-lookup"><span data-stu-id="51b66-146">Read/write</span></span>  <br/> |
|<span data-ttu-id="51b66-147">**PR_ENTRYID** [(PidTagEntryId)](pidtagentryid-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="51b66-147">**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="51b66-148">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="51b66-148">Read-only</span></span>  <br/> |
|<span data-ttu-id="51b66-149">**PR_FOLDER_TYPE** [(PidTagFolderType)](pidtagfoldertype-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="51b66-149">**PR_FOLDER_TYPE** ([PidTagFolderType](pidtagfoldertype-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="51b66-150">Чтение и запись</span><span class="sxs-lookup"><span data-stu-id="51b66-150">Read/write</span></span>  <br/> |
|<span data-ttu-id="51b66-151">**PR_OBJECT_TYPE** [(PidTagObjectType)](pidtagobjecttype-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="51b66-151">**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="51b66-152">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="51b66-152">Read-only</span></span>  <br/> |
|<span data-ttu-id="51b66-153">**PR_PARENT_ENTRYID** [(PidTagParentEntryId)](pidtagparententryid-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="51b66-153">**PR_PARENT_ENTRYID** ([PidTagParentEntryId](pidtagparententryid-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="51b66-154">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="51b66-154">Read-only</span></span>  <br/> |
|<span data-ttu-id="51b66-155">**PR_RECORD_KEY** [(PidTagRecordKey](pidtagrecordkey-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="51b66-155">**PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="51b66-156">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="51b66-156">Read-only</span></span>  <br/> |
|<span data-ttu-id="51b66-157">**PR_STORE_ENTRYID** [(PidTagStoreEntryId)](pidtagstoreentryid-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="51b66-157">**PR_STORE_ENTRYID** ([PidTagStoreEntryId](pidtagstoreentryid-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="51b66-158">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="51b66-158">Read-only</span></span>  <br/> |
|<span data-ttu-id="51b66-159">**PR_STORE_RECORD_KEY** [(PidTagStoreRecordKey)](pidtagstorerecordkey-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="51b66-159">**PR_STORE_RECORD_KEY** ([PidTagStoreRecordKey](pidtagstorerecordkey-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="51b66-160">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="51b66-160">Read-only</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="51b66-161">См. также</span><span class="sxs-lookup"><span data-stu-id="51b66-161">See also</span></span>



[<span data-ttu-id="51b66-162">Интерфейсы MAPI</span><span class="sxs-lookup"><span data-stu-id="51b66-162">MAPI Interfaces</span></span>](mapi-interfaces.md)

