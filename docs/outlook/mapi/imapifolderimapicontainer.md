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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32329493"
---
# <a name="imapifolder--imapicontainer"></a><span data-ttu-id="45eef-103">IMAPIFolder : IMAPIContainer</span><span class="sxs-lookup"><span data-stu-id="45eef-103">IMAPIFolder : IMAPIContainer</span></span>

  
  
<span data-ttu-id="45eef-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="45eef-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="45eef-105">Выполняет операции над сообщениями и вложенными папками в папке.</span><span class="sxs-lookup"><span data-stu-id="45eef-105">Performs operations on the messages and subfolders in a folder.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="45eef-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="45eef-106">Header file:</span></span>  <br/> |<span data-ttu-id="45eef-107">MAPIDEFS. h</span><span class="sxs-lookup"><span data-stu-id="45eef-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="45eef-108">Предоставлено:</span><span class="sxs-lookup"><span data-stu-id="45eef-108">Exposed by:</span></span>  <br/> |<span data-ttu-id="45eef-109">Объекты папок</span><span class="sxs-lookup"><span data-stu-id="45eef-109">Folder objects</span></span>  <br/> |
|<span data-ttu-id="45eef-110">Реализовано в:</span><span class="sxs-lookup"><span data-stu-id="45eef-110">Implemented by:</span></span>  <br/> |<span data-ttu-id="45eef-111">Поставщики хранилища сообщений</span><span class="sxs-lookup"><span data-stu-id="45eef-111">Message store providers</span></span>  <br/> |
|<span data-ttu-id="45eef-112">Вызывающая сторона:</span><span class="sxs-lookup"><span data-stu-id="45eef-112">Called by:</span></span>  <br/> |<span data-ttu-id="45eef-113">Клиентские приложения и MAPI</span><span class="sxs-lookup"><span data-stu-id="45eef-113">Client applications and MAPI</span></span>  <br/> |
|<span data-ttu-id="45eef-114">Идентификатор интерфейса:</span><span class="sxs-lookup"><span data-stu-id="45eef-114">Interface identifier:</span></span>  <br/> |<span data-ttu-id="45eef-115">Иид_имапифолдер</span><span class="sxs-lookup"><span data-stu-id="45eef-115">IID_IMAPIFolder</span></span>  <br/> |
|<span data-ttu-id="45eef-116">Тип указателя:</span><span class="sxs-lookup"><span data-stu-id="45eef-116">Pointer type:</span></span>  <br/> |<span data-ttu-id="45eef-117">ЛПМАПИФОЛДЕР</span><span class="sxs-lookup"><span data-stu-id="45eef-117">LPMAPIFOLDER</span></span>  <br/> |
|<span data-ttu-id="45eef-118">Модель транзакции:</span><span class="sxs-lookup"><span data-stu-id="45eef-118">Transaction model:</span></span>  <br/> |<span data-ttu-id="45eef-119">Не transactd</span><span class="sxs-lookup"><span data-stu-id="45eef-119">Nontransacted</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="45eef-120">Заказ vtable</span><span class="sxs-lookup"><span data-stu-id="45eef-120">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="45eef-121">CreateMessage</span><span class="sxs-lookup"><span data-stu-id="45eef-121">CreateMessage</span></span>](imapifolder-createmessage.md) <br/> |<span data-ttu-id="45eef-122">Создает новое сообщение.</span><span class="sxs-lookup"><span data-stu-id="45eef-122">Creates a new message.</span></span>  <br/> |
|[<span data-ttu-id="45eef-123">Копимессажес</span><span class="sxs-lookup"><span data-stu-id="45eef-123">CopyMessages</span></span>](imapifolder-copymessages.md) <br/> |<span data-ttu-id="45eef-124">Копирует или перемещает одно или несколько сообщений.</span><span class="sxs-lookup"><span data-stu-id="45eef-124">Copies or moves one or more messages.</span></span>  <br/> |
|[<span data-ttu-id="45eef-125">Делетемессажес</span><span class="sxs-lookup"><span data-stu-id="45eef-125">DeleteMessages</span></span>](imapifolder-deletemessages.md) <br/> |<span data-ttu-id="45eef-126">Удаляет одно или несколько сообщений.</span><span class="sxs-lookup"><span data-stu-id="45eef-126">Deletes one or more messages.</span></span>  <br/> |
|[<span data-ttu-id="45eef-127">CreateFolder</span><span class="sxs-lookup"><span data-stu-id="45eef-127">CreateFolder</span></span>](imapifolder-createfolder.md) <br/> |<span data-ttu-id="45eef-128">Создает новую вложенную папку.</span><span class="sxs-lookup"><span data-stu-id="45eef-128">Creates a new subfolder.</span></span>  <br/> |
|[<span data-ttu-id="45eef-129">CopyFolder</span><span class="sxs-lookup"><span data-stu-id="45eef-129">CopyFolder</span></span>](imapifolder-copyfolder.md) <br/> |<span data-ttu-id="45eef-130">Копирует или перемещает вложенную папку.</span><span class="sxs-lookup"><span data-stu-id="45eef-130">Copies or moves a subfolder.</span></span>  <br/> |
|[<span data-ttu-id="45eef-131">DeleteFolder</span><span class="sxs-lookup"><span data-stu-id="45eef-131">DeleteFolder</span></span>](imapifolder-deletefolder.md) <br/> |<span data-ttu-id="45eef-132">Удаляет вложенную папку.</span><span class="sxs-lookup"><span data-stu-id="45eef-132">Deletes a subfolder.</span></span>  <br/> |
|[<span data-ttu-id="45eef-133">Сетреадфлагс</span><span class="sxs-lookup"><span data-stu-id="45eef-133">SetReadFlags</span></span>](imapifolder-setreadflags.md) <br/> |<span data-ttu-id="45eef-134">Задает или очищает флаг МСГФЛАГ_РЕАД в свойстве \*\*пр_мессаже_флагс\*\* ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) одного или нескольких сообщений папки и управляет отправкой отчетов о прочтении.</span><span class="sxs-lookup"><span data-stu-id="45eef-134">Sets or clears the MSGFLAG_READ flag in the **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) property of one or more of the folder's messages, and manages the sending of read reports.</span></span>  <br/> |
|[<span data-ttu-id="45eef-135">Жетмессажестатус</span><span class="sxs-lookup"><span data-stu-id="45eef-135">GetMessageStatus</span></span>](imapifolder-getmessagestatus.md) <br/> |<span data-ttu-id="45eef-136">Получает состояние, связанное с сообщением в определенной папке.</span><span class="sxs-lookup"><span data-stu-id="45eef-136">Obtains the status associated with a message in a particular folder.</span></span>  <br/> |
|[<span data-ttu-id="45eef-137">Сетмессажестатус</span><span class="sxs-lookup"><span data-stu-id="45eef-137">SetMessageStatus</span></span>](imapifolder-setmessagestatus.md) <br/> |<span data-ttu-id="45eef-138">Задает состояние, связанное с сообщением.</span><span class="sxs-lookup"><span data-stu-id="45eef-138">Sets the status associated with a message.</span></span>  <br/> |
|[<span data-ttu-id="45eef-139">Савеконтентссорт</span><span class="sxs-lookup"><span data-stu-id="45eef-139">SaveContentsSort</span></span>](imapifolder-savecontentssort.md) <br/> |<span data-ttu-id="45eef-140">Задает порядок сортировки по умолчанию для таблицы содержимого папки.</span><span class="sxs-lookup"><span data-stu-id="45eef-140">Sets the default sort order for a folder's contents table.</span></span>  <br/> |
|[<span data-ttu-id="45eef-141">EmptyFolder</span><span class="sxs-lookup"><span data-stu-id="45eef-141">EmptyFolder</span></span>](imapifolder-emptyfolder.md) <br/> |<span data-ttu-id="45eef-142">Удаляет все сообщения и вложенные папки из папки без удаления самой папки.</span><span class="sxs-lookup"><span data-stu-id="45eef-142">Deletes all messages and subfolders from a folder without deleting the folder itself.</span></span>  <br/> |
   
|<span data-ttu-id="45eef-143">**Обязательные свойства**</span><span class="sxs-lookup"><span data-stu-id="45eef-143">**Required properties**</span></span>|<span data-ttu-id="45eef-144">**Access**</span><span class="sxs-lookup"><span data-stu-id="45eef-144">**Access**</span></span>|
|:-----|:-----|
|<span data-ttu-id="45eef-145">**Пр_дисплай_наме** ([PidTagDisplayNamePrefix](pidtagdisplaynameprefix-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="45eef-145">**PR_DISPLAY_NAME** ([PidTagDisplayNamePrefix](pidtagdisplaynameprefix-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="45eef-146">Чтение и запись</span><span class="sxs-lookup"><span data-stu-id="45eef-146">Read/write</span></span>  <br/> |
|<span data-ttu-id="45eef-147">**Пр_ентрид** ([PidTagEntryId](pidtagentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="45eef-147">**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="45eef-148">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="45eef-148">Read-only</span></span>  <br/> |
|<span data-ttu-id="45eef-149">**Пр_фолдер_типе** ([PidTagFolderType](pidtagfoldertype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="45eef-149">**PR_FOLDER_TYPE** ([PidTagFolderType](pidtagfoldertype-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="45eef-150">Чтение и запись</span><span class="sxs-lookup"><span data-stu-id="45eef-150">Read/write</span></span>  <br/> |
|<span data-ttu-id="45eef-151">**Пр_обжект_типе** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="45eef-151">**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="45eef-152">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="45eef-152">Read-only</span></span>  <br/> |
|<span data-ttu-id="45eef-153">**Пр_парент_ентрид** ([PidTagParentEntryId](pidtagparententryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="45eef-153">**PR_PARENT_ENTRYID** ([PidTagParentEntryId](pidtagparententryid-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="45eef-154">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="45eef-154">Read-only</span></span>  <br/> |
|<span data-ttu-id="45eef-155">**Пр_рекорд_кэй** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="45eef-155">**PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="45eef-156">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="45eef-156">Read-only</span></span>  <br/> |
|<span data-ttu-id="45eef-157">**Пр_сторе_ентрид** ([PidTagStoreEntryId](pidtagstoreentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="45eef-157">**PR_STORE_ENTRYID** ([PidTagStoreEntryId](pidtagstoreentryid-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="45eef-158">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="45eef-158">Read-only</span></span>  <br/> |
|<span data-ttu-id="45eef-159">**Пр_сторе_рекорд_кэй** ([PidTagStoreRecordKey](pidtagstorerecordkey-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="45eef-159">**PR_STORE_RECORD_KEY** ([PidTagStoreRecordKey](pidtagstorerecordkey-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="45eef-160">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="45eef-160">Read-only</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="45eef-161">См. также</span><span class="sxs-lookup"><span data-stu-id="45eef-161">See also</span></span>



[<span data-ttu-id="45eef-162">Интерфейсы MAPI</span><span class="sxs-lookup"><span data-stu-id="45eef-162">MAPI Interfaces</span></span>](mapi-interfaces.md)

