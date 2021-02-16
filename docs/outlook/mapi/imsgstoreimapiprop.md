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
ms.openlocfilehash: af4bf73b58f7723066bb8fad7c087ba0238ceec2
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422329"
---
# <a name="imsgstore--imapiprop"></a><span data-ttu-id="3a42b-103">IMsgStore : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="3a42b-103">IMsgStore : IMAPIProp</span></span>

  
  
<span data-ttu-id="3a42b-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3a42b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3a42b-105">Предоставляет доступ к сведениям о хранилище сообщений, а также к письмам и папок.</span><span class="sxs-lookup"><span data-stu-id="3a42b-105">Provides access to message store information and to messages and folders.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="3a42b-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="3a42b-106">Header file:</span></span>  <br/> |<span data-ttu-id="3a42b-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="3a42b-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="3a42b-108">Выставим:</span><span class="sxs-lookup"><span data-stu-id="3a42b-108">Exposed by:</span></span>  <br/> |<span data-ttu-id="3a42b-109">Объект store сообщений</span><span class="sxs-lookup"><span data-stu-id="3a42b-109">Message store object</span></span>  <br/> |
|<span data-ttu-id="3a42b-110">Реализовано в:</span><span class="sxs-lookup"><span data-stu-id="3a42b-110">Implemented by:</span></span>  <br/> |<span data-ttu-id="3a42b-111">Поставщики store сообщений</span><span class="sxs-lookup"><span data-stu-id="3a42b-111">Message store providers</span></span>  <br/> |
|<span data-ttu-id="3a42b-112">Вызывающая сторона:</span><span class="sxs-lookup"><span data-stu-id="3a42b-112">Called by:</span></span>  <br/> |<span data-ttu-id="3a42b-113">Клиентские приложения, пул MAPI и MAPI</span><span class="sxs-lookup"><span data-stu-id="3a42b-113">Client applications, the MAPI spooler, and MAPI</span></span>  <br/> |
|<span data-ttu-id="3a42b-114">Идентификатор интерфейса:</span><span class="sxs-lookup"><span data-stu-id="3a42b-114">Interface identifier:</span></span>  <br/> |<span data-ttu-id="3a42b-115">IID_IMsgStore</span><span class="sxs-lookup"><span data-stu-id="3a42b-115">IID_IMsgStore</span></span>  <br/> |
|<span data-ttu-id="3a42b-116">Тип указателя:</span><span class="sxs-lookup"><span data-stu-id="3a42b-116">Pointer type:</span></span>  <br/> |<span data-ttu-id="3a42b-117">LPMDB</span><span class="sxs-lookup"><span data-stu-id="3a42b-117">LPMDB</span></span>  <br/> |
|<span data-ttu-id="3a42b-118">Модель транзакций:</span><span class="sxs-lookup"><span data-stu-id="3a42b-118">Transaction model:</span></span>  <br/> |<span data-ttu-id="3a42b-119">Nontransacted</span><span class="sxs-lookup"><span data-stu-id="3a42b-119">Nontransacted</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="3a42b-120">Порядок ветвей</span><span class="sxs-lookup"><span data-stu-id="3a42b-120">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="3a42b-121">Консультация</span><span class="sxs-lookup"><span data-stu-id="3a42b-121">Advise</span></span>](imsgstore-advise.md) <br/> |<span data-ttu-id="3a42b-122">Регистрируется для получения уведомлений об указанных событиях, влияющих на хранилище сообщений.</span><span class="sxs-lookup"><span data-stu-id="3a42b-122">Registers to receive notification of specified events that affect the message store.</span></span>  <br/> |
|[<span data-ttu-id="3a42b-123">Unadvise</span><span class="sxs-lookup"><span data-stu-id="3a42b-123">Unadvise</span></span>](imsgstore-unadvise.md) <br/> |<span data-ttu-id="3a42b-124">Отменяет отправку уведомлений, которые ранее были настроены с помощью вызова метода **IMsgStore::Advise.**</span><span class="sxs-lookup"><span data-stu-id="3a42b-124">Cancels the sending of notifications previously set up with a call to the **IMsgStore::Advise** method.</span></span>  <br/> |
|[<span data-ttu-id="3a42b-125">CompareEntryIDs</span><span class="sxs-lookup"><span data-stu-id="3a42b-125">CompareEntryIDs</span></span>](imsgstore-compareentryids.md) <br/> |<span data-ttu-id="3a42b-126">Сравнивает два идентификатора записей, чтобы определить, ссылаются ли они на ту же запись в хранилище сообщений.</span><span class="sxs-lookup"><span data-stu-id="3a42b-126">Compares two entry identifiers to determine whether they refer to the same entry in a message store.</span></span>  <br/> |
|[<span data-ttu-id="3a42b-127">OpenEntry</span><span class="sxs-lookup"><span data-stu-id="3a42b-127">OpenEntry</span></span>](imsgstore-openentry.md) <br/> |<span data-ttu-id="3a42b-128">Открывает папку или сообщение и возвращает указатель интерфейса для дальнейшего доступа.</span><span class="sxs-lookup"><span data-stu-id="3a42b-128">Opens a folder or message and returns an interface pointer for further access.</span></span>  <br/> |
|[<span data-ttu-id="3a42b-129">SetReceiveFolder</span><span class="sxs-lookup"><span data-stu-id="3a42b-129">SetReceiveFolder</span></span>](imsgstore-setreceivefolder.md) <br/> |<span data-ttu-id="3a42b-130">Устанавливает папку в качестве места назначения для входящих сообщений определенного класса сообщений.</span><span class="sxs-lookup"><span data-stu-id="3a42b-130">Establishes a folder as the destination for incoming messages of a particular message class.</span></span>  <br/> |
|[<span data-ttu-id="3a42b-131">GetReceiveFolder</span><span class="sxs-lookup"><span data-stu-id="3a42b-131">GetReceiveFolder</span></span>](imsgstore-getreceivefolder.md) <br/> |<span data-ttu-id="3a42b-132">Получает папку, которая была установлена в качестве места назначения для входящих сообщений указанного класса сообщений или в качестве папки получения по умолчанию для хранения сообщений.</span><span class="sxs-lookup"><span data-stu-id="3a42b-132">Obtains the folder that was established as the destination for incoming messages of a specified message class or as the default receive folder for the message store.</span></span>  <br/> |
|[<span data-ttu-id="3a42b-133">GetReceiveFolderTable</span><span class="sxs-lookup"><span data-stu-id="3a42b-133">GetReceiveFolderTable</span></span>](imsgstore-getreceivefoldertable.md) <br/> |<span data-ttu-id="3a42b-134">Предоставляет доступ к таблице папок получения, таблице со сведениями обо всех папках получения для хранения сообщений.</span><span class="sxs-lookup"><span data-stu-id="3a42b-134">Provides access to the receive folder table, a table with information about all of the receive folders for the message store.</span></span>  <br/> |
|[<span data-ttu-id="3a42b-135">StoreLogoff</span><span class="sxs-lookup"><span data-stu-id="3a42b-135">StoreLogoff</span></span>](imsgstore-storelogoff.md) <br/> |<span data-ttu-id="3a42b-136">Включает упорядоченный вход в хранилище сообщений.</span><span class="sxs-lookup"><span data-stu-id="3a42b-136">Enables the orderly logoff of the message store.</span></span>  <br/> |
|[<span data-ttu-id="3a42b-137">AbortSubmit</span><span class="sxs-lookup"><span data-stu-id="3a42b-137">AbortSubmit</span></span>](imsgstore-abortsubmit.md) <br/> |<span data-ttu-id="3a42b-138">Пытается удалить сообщение из исходя такой очереди.</span><span class="sxs-lookup"><span data-stu-id="3a42b-138">Attempts to remove a message from the outgoing queue.</span></span>  <br/> |
|[<span data-ttu-id="3a42b-139">GetOutgoingQueue</span><span class="sxs-lookup"><span data-stu-id="3a42b-139">GetOutgoingQueue</span></span>](imsgstore-getoutgoingqueue.md) <br/> |<span data-ttu-id="3a42b-140">Предоставляет доступ к таблице исходяющих очередей, которая содержит сведения обо всех сообщениях в исходя такой очереди.</span><span class="sxs-lookup"><span data-stu-id="3a42b-140">Provides access to the outgoing queue table, a table that has information about all of the messages in the message store's outgoing queue.</span></span>  <br/> |
|[<span data-ttu-id="3a42b-141">SetLockState</span><span class="sxs-lookup"><span data-stu-id="3a42b-141">SetLockState</span></span>](imsgstore-setlockstate.md) <br/> |<span data-ttu-id="3a42b-142">Блокирует или разблокирует сообщение.</span><span class="sxs-lookup"><span data-stu-id="3a42b-142">Locks or unlocks a message.</span></span>  <br/> |
|[<span data-ttu-id="3a42b-143">FinishedMsg</span><span class="sxs-lookup"><span data-stu-id="3a42b-143">FinishedMsg</span></span>](imsgstore-finishedmsg.md) <br/> |<span data-ttu-id="3a42b-144">Позволяет поставщику хранилище сообщений выполнять обработку отправленного сообщения.</span><span class="sxs-lookup"><span data-stu-id="3a42b-144">Enables the message store provider to perform processing on a sent message.</span></span>  <br/> |
|[<span data-ttu-id="3a42b-145">NotifyNewMail</span><span class="sxs-lookup"><span data-stu-id="3a42b-145">NotifyNewMail</span></span>](imsgstore-notifynewmail.md) <br/> |<span data-ttu-id="3a42b-146">����������� ��������� ���������, ����� ���������.</span><span class="sxs-lookup"><span data-stu-id="3a42b-146">Informs the message store that a new message has arrived.</span></span>  <br/> |
   
|<span data-ttu-id="3a42b-147">**Обязательные свойства**</span><span class="sxs-lookup"><span data-stu-id="3a42b-147">**Required properties**</span></span>|<span data-ttu-id="3a42b-148">**Уровень доступа**</span><span class="sxs-lookup"><span data-stu-id="3a42b-148">**Access level**</span></span>|
|:-----|:-----|
|<span data-ttu-id="3a42b-149">**PR_DISPLAY_NAME** ([PidTagDisplayName)](pidtagdisplayname-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="3a42b-149">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="3a42b-150">Чтение и запись</span><span class="sxs-lookup"><span data-stu-id="3a42b-150">Read/write</span></span>  <br/> |
|<span data-ttu-id="3a42b-151">**PR_ENTRYID** ([PidTagEntryId)](pidtagentryid-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="3a42b-151">**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="3a42b-152">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="3a42b-152">Read-only</span></span>  <br/> |
|<span data-ttu-id="3a42b-153">**PR_OBJECT_TYPE** ([PidTagObjectType)](pidtagobjecttype-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="3a42b-153">**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="3a42b-154">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="3a42b-154">Read-only</span></span>  <br/> |
|<span data-ttu-id="3a42b-155">**PR_RECORD_KEY** ([PidTagRecordKey)](pidtagrecordkey-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="3a42b-155">**PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="3a42b-156">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="3a42b-156">Read-only</span></span>  <br/> |
|<span data-ttu-id="3a42b-157">**PR_STORE_ENTRYID** ([PidTagStoreEntryId)](pidtagstoreentryid-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="3a42b-157">**PR_STORE_ENTRYID** ([PidTagStoreEntryId](pidtagstoreentryid-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="3a42b-158">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="3a42b-158">Read-only</span></span>  <br/> |
|<span data-ttu-id="3a42b-159">**PR_STORE_RECORD_KEY** ([PidTagStoreRecordKey)](pidtagstorerecordkey-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="3a42b-159">**PR_STORE_RECORD_KEY** ([PidTagStoreRecordKey](pidtagstorerecordkey-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="3a42b-160">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="3a42b-160">Read-only</span></span>  <br/> |
|<span data-ttu-id="3a42b-161">**PR_MDB_PROVIDER** ([PidTagStoreProvider)](pidtagstoreprovider-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="3a42b-161">**PR_MDB_PROVIDER** ([PidTagStoreProvider](pidtagstoreprovider-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="3a42b-162">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="3a42b-162">Read-only</span></span>  <br/> |
|<span data-ttu-id="3a42b-163">**PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask)](pidtagstoresupportmask-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="3a42b-163">**PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="3a42b-164">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="3a42b-164">Read-only</span></span>  <br/> |
   
<span data-ttu-id="3a42b-165">Для хранилищ сообщений между межличностным сообщением (IPM) имеются следующие свойства:</span><span class="sxs-lookup"><span data-stu-id="3a42b-165">The following properties are for interpersonal message (IPM) message stores:</span></span>
  
- <span data-ttu-id="3a42b-166">**PR_IPM_OUTBOX_ENTRYID** ([PidTagIpmOutboxEntryId)](pidtagipmoutboxentryid-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="3a42b-166">**PR_IPM_OUTBOX_ENTRYID** ([PidTagIpmOutboxEntryId](pidtagipmoutboxentryid-canonical-property.md))</span></span>
    
- <span data-ttu-id="3a42b-167">**PR_IPM_SENTMAIL_ENTRYID** ([PidTagIpmSentMailEntryId)](pidtagipmsentmailentryid-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="3a42b-167">**PR_IPM_SENTMAIL_ENTRYID** ([PidTagIpmSentMailEntryId](pidtagipmsentmailentryid-canonical-property.md))</span></span>
    
- <span data-ttu-id="3a42b-168">**PR_IPM_SUBTREE_ENTRYID** ([PidTagIpmSubtreeEntryId)](pidtagipmsubtreeentryid-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="3a42b-168">**PR_IPM_SUBTREE_ENTRYID** ([PidTagIpmSubtreeEntryId](pidtagipmsubtreeentryid-canonical-property.md))</span></span>
    
- <span data-ttu-id="3a42b-169">**PR_IPM_WASTEBASKET_ENTRYID** ([PidTagIpmWastebasketEntryId)](pidtagipmwastebasketentryid-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="3a42b-169">**PR_IPM_WASTEBASKET_ENTRYID** ([PidTagIpmWastebasketEntryId](pidtagipmwastebasketentryid-canonical-property.md))</span></span>
    
- <span data-ttu-id="3a42b-170">**PR_MDB_PROVIDER**</span><span class="sxs-lookup"><span data-stu-id="3a42b-170">**PR_MDB_PROVIDER**</span></span>
    
- <span data-ttu-id="3a42b-171">**PR_STORE_SUPPORT_MASK**</span><span class="sxs-lookup"><span data-stu-id="3a42b-171">**PR_STORE_SUPPORT_MASK**</span></span>
    
## <a name="see-also"></a><span data-ttu-id="3a42b-172">См. также</span><span class="sxs-lookup"><span data-stu-id="3a42b-172">See also</span></span>



[<span data-ttu-id="3a42b-173">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="3a42b-173">MAPI Properties</span></span>](mapi-properties.md)

