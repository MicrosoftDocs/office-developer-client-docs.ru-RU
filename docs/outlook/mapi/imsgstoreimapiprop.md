---
title: IMsgStore IMAPIProp
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMsgStore
api_type:
- COM
ms.assetid: 20090114-b183-4767-8971-a304a9aa47e6
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 4ed17fd7f826432da9460fe01e5aa76802726bad
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22584634"
---
# <a name="imsgstore--imapiprop"></a><span data-ttu-id="f4c40-103">IMsgStore : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="f4c40-103">IMsgStore : IMAPIProp</span></span>

  
  
<span data-ttu-id="f4c40-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f4c40-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f4c40-105">Предоставляет доступ к информации о хранилища сообщений и сообщений и папок.</span><span class="sxs-lookup"><span data-stu-id="f4c40-105">Provides access to message store information and to messages and folders.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="f4c40-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="f4c40-106">Header file:</span></span>  <br/> |<span data-ttu-id="f4c40-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="f4c40-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="f4c40-108">Предоставляемые:</span><span class="sxs-lookup"><span data-stu-id="f4c40-108">Exposed by:</span></span>  <br/> |<span data-ttu-id="f4c40-109">Объект хранилища сообщений</span><span class="sxs-lookup"><span data-stu-id="f4c40-109">Message store object</span></span>  <br/> |
|<span data-ttu-id="f4c40-110">Реализованный:</span><span class="sxs-lookup"><span data-stu-id="f4c40-110">Implemented by:</span></span>  <br/> |<span data-ttu-id="f4c40-111">Поставщики хранилища сообщений</span><span class="sxs-lookup"><span data-stu-id="f4c40-111">Message store providers</span></span>  <br/> |
|<span data-ttu-id="f4c40-112">Вызывается:</span><span class="sxs-lookup"><span data-stu-id="f4c40-112">Called by:</span></span>  <br/> |<span data-ttu-id="f4c40-113">Клиентские приложения, диспетчер очереди MAPI и MAPI</span><span class="sxs-lookup"><span data-stu-id="f4c40-113">Client applications, the MAPI spooler, and MAPI</span></span>  <br/> |
|<span data-ttu-id="f4c40-114">Идентификатор интерфейса:</span><span class="sxs-lookup"><span data-stu-id="f4c40-114">Interface identifier:</span></span>  <br/> |<span data-ttu-id="f4c40-115">IID_IMsgStore</span><span class="sxs-lookup"><span data-stu-id="f4c40-115">IID_IMsgStore</span></span>  <br/> |
|<span data-ttu-id="f4c40-116">Тип указателя:</span><span class="sxs-lookup"><span data-stu-id="f4c40-116">Pointer type:</span></span>  <br/> |<span data-ttu-id="f4c40-117">LPMDB</span><span class="sxs-lookup"><span data-stu-id="f4c40-117">LPMDB</span></span>  <br/> |
|<span data-ttu-id="f4c40-118">Модель транзакций:</span><span class="sxs-lookup"><span data-stu-id="f4c40-118">Transaction model:</span></span>  <br/> |<span data-ttu-id="f4c40-119">Не входящих в транзакции</span><span class="sxs-lookup"><span data-stu-id="f4c40-119">Nontransacted</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="f4c40-120">Порядке vtable</span><span class="sxs-lookup"><span data-stu-id="f4c40-120">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="f4c40-121">Уведомить</span><span class="sxs-lookup"><span data-stu-id="f4c40-121">Advise</span></span>](imsgstore-advise.md) <br/> |<span data-ttu-id="f4c40-122">Регистрация для получения уведомлений о указанного события, которые влияют на хранилище сообщений.</span><span class="sxs-lookup"><span data-stu-id="f4c40-122">Registers to receive notification of specified events that affect the message store.</span></span>  <br/> |
|[<span data-ttu-id="f4c40-123">Unadvise</span><span class="sxs-lookup"><span data-stu-id="f4c40-123">Unadvise</span></span>](imsgstore-unadvise.md) <br/> |<span data-ttu-id="f4c40-124">Показано, как отменить отправку уведомлений, ранее настройка с помощью вызова метода **IMsgStore::Advise** .</span><span class="sxs-lookup"><span data-stu-id="f4c40-124">Cancels the sending of notifications previously set up with a call to the **IMsgStore::Advise** method.</span></span>  <br/> |
|[<span data-ttu-id="f4c40-125">CompareEntryIDs</span><span class="sxs-lookup"><span data-stu-id="f4c40-125">CompareEntryIDs</span></span>](imsgstore-compareentryids.md) <br/> |<span data-ttu-id="f4c40-126">Сравнение двух идентификаторы записей для определения, является ли они ссылаются на той же операции в банке сообщений.</span><span class="sxs-lookup"><span data-stu-id="f4c40-126">Compares two entry identifiers to determine whether they refer to the same entry in a message store.</span></span>  <br/> |
|[<span data-ttu-id="f4c40-127">OpenEntry</span><span class="sxs-lookup"><span data-stu-id="f4c40-127">OpenEntry</span></span>](imsgstore-openentry.md) <br/> |<span data-ttu-id="f4c40-128">Открывает папку или сообщение и возвращает указатель интерфейса для дальнейшей доступа.</span><span class="sxs-lookup"><span data-stu-id="f4c40-128">Opens a folder or message and returns an interface pointer for further access.</span></span>  <br/> |
|[<span data-ttu-id="f4c40-129">SetReceiveFolder</span><span class="sxs-lookup"><span data-stu-id="f4c40-129">SetReceiveFolder</span></span>](imsgstore-setreceivefolder.md) <br/> |<span data-ttu-id="f4c40-130">Устанавливает папки в качестве назначения для входящих сообщений класса определенного сообщения.</span><span class="sxs-lookup"><span data-stu-id="f4c40-130">Establishes a folder as the destination for incoming messages of a particular message class.</span></span>  <br/> |
|[<span data-ttu-id="f4c40-131">GetReceiveFolder</span><span class="sxs-lookup"><span data-stu-id="f4c40-131">GetReceiveFolder</span></span>](imsgstore-getreceivefolder.md) <br/> |<span data-ttu-id="f4c40-132">Получает к папке, где были установлены как место назначения для входящих сообщений из указанного класса сообщений или по умолчанию получают папки для хранения сообщений.</span><span class="sxs-lookup"><span data-stu-id="f4c40-132">Obtains the folder that was established as the destination for incoming messages of a specified message class or as the default receive folder for the message store.</span></span>  <br/> |
|[<span data-ttu-id="f4c40-133">GetReceiveFolderTable</span><span class="sxs-lookup"><span data-stu-id="f4c40-133">GetReceiveFolderTable</span></span>](imsgstore-getreceivefoldertable.md) <br/> |<span data-ttu-id="f4c40-134">Предоставляет доступ к таблице папок получения таблицу, содержащую сведения обо всех получения папки для хранения сообщений.</span><span class="sxs-lookup"><span data-stu-id="f4c40-134">Provides access to the receive folder table, a table with information about all of the receive folders for the message store.</span></span>  <br/> |
|[<span data-ttu-id="f4c40-135">StoreLogoff</span><span class="sxs-lookup"><span data-stu-id="f4c40-135">StoreLogoff</span></span>](imsgstore-storelogoff.md) <br/> |<span data-ttu-id="f4c40-136">Включение упорядоченного выхода хранилища сообщений.</span><span class="sxs-lookup"><span data-stu-id="f4c40-136">Enables the orderly logoff of the message store.</span></span>  <br/> |
|[<span data-ttu-id="f4c40-137">AbortSubmit</span><span class="sxs-lookup"><span data-stu-id="f4c40-137">AbortSubmit</span></span>](imsgstore-abortsubmit.md) <br/> |<span data-ttu-id="f4c40-138">Пытается удалить сообщения из очереди исходящих сообщений.</span><span class="sxs-lookup"><span data-stu-id="f4c40-138">Attempts to remove a message from the outgoing queue.</span></span>  <br/> |
|[<span data-ttu-id="f4c40-139">GetOutgoingQueue</span><span class="sxs-lookup"><span data-stu-id="f4c40-139">GetOutgoingQueue</span></span>](imsgstore-getoutgoingqueue.md) <br/> |<span data-ttu-id="f4c40-140">Предоставляет доступ к таблице исходящей очереди, таблицы, которая содержит сведения обо всех сообщений в очереди исходящих хранилища сообщений.</span><span class="sxs-lookup"><span data-stu-id="f4c40-140">Provides access to the outgoing queue table, a table that has information about all of the messages in the message store's outgoing queue.</span></span>  <br/> |
|[<span data-ttu-id="f4c40-141">SetLockState</span><span class="sxs-lookup"><span data-stu-id="f4c40-141">SetLockState</span></span>](imsgstore-setlockstate.md) <br/> |<span data-ttu-id="f4c40-142">Блокирует или разблокирует сообщение.</span><span class="sxs-lookup"><span data-stu-id="f4c40-142">Locks or unlocks a message.</span></span>  <br/> |
|[<span data-ttu-id="f4c40-143">FinishedMsg</span><span class="sxs-lookup"><span data-stu-id="f4c40-143">FinishedMsg</span></span>](imsgstore-finishedmsg.md) <br/> |<span data-ttu-id="f4c40-144">Включает поставщика хранилища сообщений для обработки на отправленное сообщение.</span><span class="sxs-lookup"><span data-stu-id="f4c40-144">Enables the message store provider to perform processing on a sent message.</span></span>  <br/> |
|[<span data-ttu-id="f4c40-145">NotifyNewMail</span><span class="sxs-lookup"><span data-stu-id="f4c40-145">NotifyNewMail</span></span>](imsgstore-notifynewmail.md) <br/> |<span data-ttu-id="f4c40-146">����������� ��������� ���������, ����� ���������.</span><span class="sxs-lookup"><span data-stu-id="f4c40-146">Informs the message store that a new message has arrived.</span></span>  <br/> |
   
|<span data-ttu-id="f4c40-147">**Обязательные свойства**</span><span class="sxs-lookup"><span data-stu-id="f4c40-147">**Required properties**</span></span>|<span data-ttu-id="f4c40-148">**Уровень доступа**</span><span class="sxs-lookup"><span data-stu-id="f4c40-148">**Access level**</span></span>|
|:-----|:-----|
|<span data-ttu-id="f4c40-149">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="f4c40-149">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="f4c40-150">Чтение и запись</span><span class="sxs-lookup"><span data-stu-id="f4c40-150">Read/write</span></span>  <br/> |
|<span data-ttu-id="f4c40-151">**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="f4c40-151">**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="f4c40-152">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="f4c40-152">Read-only</span></span>  <br/> |
|<span data-ttu-id="f4c40-153">**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="f4c40-153">**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="f4c40-154">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="f4c40-154">Read-only</span></span>  <br/> |
|<span data-ttu-id="f4c40-155">**PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="f4c40-155">**PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="f4c40-156">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="f4c40-156">Read-only</span></span>  <br/> |
|<span data-ttu-id="f4c40-157">**PR_STORE_ENTRYID** ([PidTagStoreEntryId](pidtagstoreentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="f4c40-157">**PR_STORE_ENTRYID** ([PidTagStoreEntryId](pidtagstoreentryid-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="f4c40-158">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="f4c40-158">Read-only</span></span>  <br/> |
|<span data-ttu-id="f4c40-159">**PR_STORE_RECORD_KEY** ([PidTagStoreRecordKey](pidtagstorerecordkey-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="f4c40-159">**PR_STORE_RECORD_KEY** ([PidTagStoreRecordKey](pidtagstorerecordkey-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="f4c40-160">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="f4c40-160">Read-only</span></span>  <br/> |
|<span data-ttu-id="f4c40-161">**PR_MDB_PROVIDER** ([PidTagStoreProvider](pidtagstoreprovider-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="f4c40-161">**PR_MDB_PROVIDER** ([PidTagStoreProvider](pidtagstoreprovider-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="f4c40-162">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="f4c40-162">Read-only</span></span>  <br/> |
|<span data-ttu-id="f4c40-163">**PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="f4c40-163">**PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="f4c40-164">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="f4c40-164">Read-only</span></span>  <br/> |
   
<span data-ttu-id="f4c40-165">Для хранилищ сообщений электронной почты — это сообщение (IPM) выполнение следующих условий:</span><span class="sxs-lookup"><span data-stu-id="f4c40-165">The following properties are for interpersonal message (IPM) message stores:</span></span>
  
- <span data-ttu-id="f4c40-166">**PR_IPM_OUTBOX_ENTRYID** ([PidTagIpmOutboxEntryId](pidtagipmoutboxentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="f4c40-166">**PR_IPM_OUTBOX_ENTRYID** ([PidTagIpmOutboxEntryId](pidtagipmoutboxentryid-canonical-property.md))</span></span>
    
- <span data-ttu-id="f4c40-167">**PR_IPM_SENTMAIL_ENTRYID** ([PidTagIpmSentMailEntryId](pidtagipmsentmailentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="f4c40-167">**PR_IPM_SENTMAIL_ENTRYID** ([PidTagIpmSentMailEntryId](pidtagipmsentmailentryid-canonical-property.md))</span></span>
    
- <span data-ttu-id="f4c40-168">**PR_IPM_SUBTREE_ENTRYID** ([PidTagIpmSubtreeEntryId](pidtagipmsubtreeentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="f4c40-168">**PR_IPM_SUBTREE_ENTRYID** ([PidTagIpmSubtreeEntryId](pidtagipmsubtreeentryid-canonical-property.md))</span></span>
    
- <span data-ttu-id="f4c40-169">**PR_IPM_WASTEBASKET_ENTRYID** ([PidTagIpmWastebasketEntryId](pidtagipmwastebasketentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="f4c40-169">**PR_IPM_WASTEBASKET_ENTRYID** ([PidTagIpmWastebasketEntryId](pidtagipmwastebasketentryid-canonical-property.md))</span></span>
    
- <span data-ttu-id="f4c40-170">**PR_MDB_PROVIDER**</span><span class="sxs-lookup"><span data-stu-id="f4c40-170">**PR_MDB_PROVIDER**</span></span>
    
- <span data-ttu-id="f4c40-171">**PR_STORE_SUPPORT_MASK**</span><span class="sxs-lookup"><span data-stu-id="f4c40-171">**PR_STORE_SUPPORT_MASK**</span></span>
    
## <a name="see-also"></a><span data-ttu-id="f4c40-172">См. также</span><span class="sxs-lookup"><span data-stu-id="f4c40-172">See also</span></span>



[<span data-ttu-id="f4c40-173">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="f4c40-173">MAPI Properties</span></span>](mapi-properties.md)

