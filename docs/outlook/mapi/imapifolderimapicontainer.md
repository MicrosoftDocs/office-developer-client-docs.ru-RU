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
# <a name="imapifolder--imapicontainer"></a><span data-ttu-id="3a05a-103">IMAPIFolder : IMAPIContainer</span><span class="sxs-lookup"><span data-stu-id="3a05a-103">IMAPIFolder : IMAPIContainer</span></span>

  
  
<span data-ttu-id="3a05a-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3a05a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3a05a-105">Выполняет операции над сообщениями и вложенными папками в папке.</span><span class="sxs-lookup"><span data-stu-id="3a05a-105">Performs operations on the messages and subfolders in a folder.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="3a05a-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="3a05a-106">Header file:</span></span>  <br/> |<span data-ttu-id="3a05a-107">MAPIDEFS. h</span><span class="sxs-lookup"><span data-stu-id="3a05a-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="3a05a-108">Предоставлено:</span><span class="sxs-lookup"><span data-stu-id="3a05a-108">Exposed by:</span></span>  <br/> |<span data-ttu-id="3a05a-109">Объекты папок</span><span class="sxs-lookup"><span data-stu-id="3a05a-109">Folder objects</span></span>  <br/> |
|<span data-ttu-id="3a05a-110">Реализовано в:</span><span class="sxs-lookup"><span data-stu-id="3a05a-110">Implemented by:</span></span>  <br/> |<span data-ttu-id="3a05a-111">Поставщики хранилища сообщений</span><span class="sxs-lookup"><span data-stu-id="3a05a-111">Message store providers</span></span>  <br/> |
|<span data-ttu-id="3a05a-112">Вызывающая сторона:</span><span class="sxs-lookup"><span data-stu-id="3a05a-112">Called by:</span></span>  <br/> |<span data-ttu-id="3a05a-113">Клиентские приложения и MAPI</span><span class="sxs-lookup"><span data-stu-id="3a05a-113">Client applications and MAPI</span></span>  <br/> |
|<span data-ttu-id="3a05a-114">Идентификатор интерфейса:</span><span class="sxs-lookup"><span data-stu-id="3a05a-114">Interface identifier:</span></span>  <br/> |<span data-ttu-id="3a05a-115">Иид_имапифолдер</span><span class="sxs-lookup"><span data-stu-id="3a05a-115">IID_IMAPIFolder</span></span>  <br/> |
|<span data-ttu-id="3a05a-116">Тип указателя:</span><span class="sxs-lookup"><span data-stu-id="3a05a-116">Pointer type:</span></span>  <br/> |<span data-ttu-id="3a05a-117">ЛПМАПИФОЛДЕР</span><span class="sxs-lookup"><span data-stu-id="3a05a-117">LPMAPIFOLDER</span></span>  <br/> |
|<span data-ttu-id="3a05a-118">Модель транзакции:</span><span class="sxs-lookup"><span data-stu-id="3a05a-118">Transaction model:</span></span>  <br/> |<span data-ttu-id="3a05a-119">Не transactd</span><span class="sxs-lookup"><span data-stu-id="3a05a-119">Nontransacted</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="3a05a-120">Заказ vtable</span><span class="sxs-lookup"><span data-stu-id="3a05a-120">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="3a05a-121">CreateMessage</span><span class="sxs-lookup"><span data-stu-id="3a05a-121">CreateMessage</span></span>](imapifolder-createmessage.md) <br/> |<span data-ttu-id="3a05a-122">Создает новое сообщение.</span><span class="sxs-lookup"><span data-stu-id="3a05a-122">Creates a new message.</span></span>  <br/> |
|[<span data-ttu-id="3a05a-123">Копимессажес</span><span class="sxs-lookup"><span data-stu-id="3a05a-123">CopyMessages</span></span>](imapifolder-copymessages.md) <br/> |<span data-ttu-id="3a05a-124">Копирует или перемещает одно или несколько сообщений.</span><span class="sxs-lookup"><span data-stu-id="3a05a-124">Copies or moves one or more messages.</span></span>  <br/> |
|[<span data-ttu-id="3a05a-125">Делетемессажес</span><span class="sxs-lookup"><span data-stu-id="3a05a-125">DeleteMessages</span></span>](imapifolder-deletemessages.md) <br/> |<span data-ttu-id="3a05a-126">Удаляет одно или несколько сообщений.</span><span class="sxs-lookup"><span data-stu-id="3a05a-126">Deletes one or more messages.</span></span>  <br/> |
|[<span data-ttu-id="3a05a-127">CreateFolder</span><span class="sxs-lookup"><span data-stu-id="3a05a-127">CreateFolder</span></span>](imapifolder-createfolder.md) <br/> |<span data-ttu-id="3a05a-128">Создает новую вложенную папку.</span><span class="sxs-lookup"><span data-stu-id="3a05a-128">Creates a new subfolder.</span></span>  <br/> |
|[<span data-ttu-id="3a05a-129">CopyFolder</span><span class="sxs-lookup"><span data-stu-id="3a05a-129">CopyFolder</span></span>](imapifolder-copyfolder.md) <br/> |<span data-ttu-id="3a05a-130">Копирует или перемещает вложенную папку.</span><span class="sxs-lookup"><span data-stu-id="3a05a-130">Copies or moves a subfolder.</span></span>  <br/> |
|[<span data-ttu-id="3a05a-131">DeleteFolder</span><span class="sxs-lookup"><span data-stu-id="3a05a-131">DeleteFolder</span></span>](imapifolder-deletefolder.md) <br/> |<span data-ttu-id="3a05a-132">Удаляет вложенную папку.</span><span class="sxs-lookup"><span data-stu-id="3a05a-132">Deletes a subfolder.</span></span>  <br/> |
|[<span data-ttu-id="3a05a-133">Сетреадфлагс</span><span class="sxs-lookup"><span data-stu-id="3a05a-133">SetReadFlags</span></span>](imapifolder-setreadflags.md) <br/> |<span data-ttu-id="3a05a-134">Задает или очищает флаг МСГФЛАГ_РЕАД в свойстве \*\*пр_мессаже_флагс\*\* ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) одного или нескольких сообщений папки и управляет отправкой отчетов о прочтении.</span><span class="sxs-lookup"><span data-stu-id="3a05a-134">Sets or clears the MSGFLAG_READ flag in the **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) property of one or more of the folder's messages, and manages the sending of read reports.</span></span>  <br/> |
|[<span data-ttu-id="3a05a-135">Жетмессажестатус</span><span class="sxs-lookup"><span data-stu-id="3a05a-135">GetMessageStatus</span></span>](imapifolder-getmessagestatus.md) <br/> |<span data-ttu-id="3a05a-136">Получает состояние, связанное с сообщением в определенной папке.</span><span class="sxs-lookup"><span data-stu-id="3a05a-136">Obtains the status associated with a message in a particular folder.</span></span>  <br/> |
|[<span data-ttu-id="3a05a-137">Сетмессажестатус</span><span class="sxs-lookup"><span data-stu-id="3a05a-137">SetMessageStatus</span></span>](imapifolder-setmessagestatus.md) <br/> |<span data-ttu-id="3a05a-138">Задает состояние, связанное с сообщением.</span><span class="sxs-lookup"><span data-stu-id="3a05a-138">Sets the status associated with a message.</span></span>  <br/> |
|[<span data-ttu-id="3a05a-139">Савеконтентссорт</span><span class="sxs-lookup"><span data-stu-id="3a05a-139">SaveContentsSort</span></span>](imapifolder-savecontentssort.md) <br/> |<span data-ttu-id="3a05a-140">Задает порядок сортировки по умолчанию для таблицы содержимого папки.</span><span class="sxs-lookup"><span data-stu-id="3a05a-140">Sets the default sort order for a folder's contents table.</span></span>  <br/> |
|[<span data-ttu-id="3a05a-141">EmptyFolder</span><span class="sxs-lookup"><span data-stu-id="3a05a-141">EmptyFolder</span></span>](imapifolder-emptyfolder.md) <br/> |<span data-ttu-id="3a05a-142">Удаляет все сообщения и вложенные папки из папки без удаления самой папки.</span><span class="sxs-lookup"><span data-stu-id="3a05a-142">Deletes all messages and subfolders from a folder without deleting the folder itself.</span></span>  <br/> |
   
|<span data-ttu-id="3a05a-143">**Обязательные свойства**</span><span class="sxs-lookup"><span data-stu-id="3a05a-143">**Required properties**</span></span>|<span data-ttu-id="3a05a-144">**Access**</span><span class="sxs-lookup"><span data-stu-id="3a05a-144">**Access**</span></span>|
|:-----|:-----|
|<span data-ttu-id="3a05a-145">**Пр_дисплай_наме** ([PidTagDisplayNamePrefix](pidtagdisplaynameprefix-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="3a05a-145">**PR_DISPLAY_NAME** ([PidTagDisplayNamePrefix](pidtagdisplaynameprefix-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="3a05a-146">Чтение и запись</span><span class="sxs-lookup"><span data-stu-id="3a05a-146">Read/write</span></span>  <br/> |
|<span data-ttu-id="3a05a-147">**Пр_ентрид** ([PidTagEntryId](pidtagentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="3a05a-147">**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="3a05a-148">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="3a05a-148">Read-only</span></span>  <br/> |
|<span data-ttu-id="3a05a-149">**Пр_фолдер_типе** ([PidTagFolderType](pidtagfoldertype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="3a05a-149">**PR_FOLDER_TYPE** ([PidTagFolderType](pidtagfoldertype-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="3a05a-150">Чтение и запись</span><span class="sxs-lookup"><span data-stu-id="3a05a-150">Read/write</span></span>  <br/> |
|<span data-ttu-id="3a05a-151">**Пр_обжект_типе** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="3a05a-151">**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="3a05a-152">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="3a05a-152">Read-only</span></span>  <br/> |
|<span data-ttu-id="3a05a-153">**Пр_парент_ентрид** ([PidTagParentEntryId](pidtagparententryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="3a05a-153">**PR_PARENT_ENTRYID** ([PidTagParentEntryId](pidtagparententryid-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="3a05a-154">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="3a05a-154">Read-only</span></span>  <br/> |
|<span data-ttu-id="3a05a-155">**Пр_рекорд_кэй** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="3a05a-155">**PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="3a05a-156">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="3a05a-156">Read-only</span></span>  <br/> |
|<span data-ttu-id="3a05a-157">**Пр_сторе_ентрид** ([PidTagStoreEntryId](pidtagstoreentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="3a05a-157">**PR_STORE_ENTRYID** ([PidTagStoreEntryId](pidtagstoreentryid-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="3a05a-158">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="3a05a-158">Read-only</span></span>  <br/> |
|<span data-ttu-id="3a05a-159">**Пр_сторе_рекорд_кэй** ([PidTagStoreRecordKey](pidtagstorerecordkey-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="3a05a-159">**PR_STORE_RECORD_KEY** ([PidTagStoreRecordKey](pidtagstorerecordkey-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="3a05a-160">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="3a05a-160">Read-only</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="3a05a-161">См. также</span><span class="sxs-lookup"><span data-stu-id="3a05a-161">See also</span></span>



[<span data-ttu-id="3a05a-162">Интерфейсы MAPI</span><span class="sxs-lookup"><span data-stu-id="3a05a-162">MAPI Interfaces</span></span>](mapi-interfaces.md)

