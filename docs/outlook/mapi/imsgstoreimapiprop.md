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
# <a name="imsgstore--imapiprop"></a><span data-ttu-id="62461-103">IMsgStore : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="62461-103">IMsgStore : IMAPIProp</span></span>

  
  
<span data-ttu-id="62461-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="62461-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="62461-105">Предоставляет доступ к сведениям о хранилище сообщений, а также к сообщениям и папок.</span><span class="sxs-lookup"><span data-stu-id="62461-105">Provides access to message store information and to messages and folders.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="62461-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="62461-106">Header file:</span></span>  <br/> |<span data-ttu-id="62461-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="62461-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="62461-108">Подвергается:</span><span class="sxs-lookup"><span data-stu-id="62461-108">Exposed by:</span></span>  <br/> |<span data-ttu-id="62461-109">Объект магазина сообщений</span><span class="sxs-lookup"><span data-stu-id="62461-109">Message store object</span></span>  <br/> |
|<span data-ttu-id="62461-110">Реализовано в:</span><span class="sxs-lookup"><span data-stu-id="62461-110">Implemented by:</span></span>  <br/> |<span data-ttu-id="62461-111">Поставщики магазинов сообщений</span><span class="sxs-lookup"><span data-stu-id="62461-111">Message store providers</span></span>  <br/> |
|<span data-ttu-id="62461-112">Вызывающая сторона:</span><span class="sxs-lookup"><span data-stu-id="62461-112">Called by:</span></span>  <br/> |<span data-ttu-id="62461-113">Клиентские приложения, шпалер MAPI и MAPI</span><span class="sxs-lookup"><span data-stu-id="62461-113">Client applications, the MAPI spooler, and MAPI</span></span>  <br/> |
|<span data-ttu-id="62461-114">Идентификатор интерфейса:</span><span class="sxs-lookup"><span data-stu-id="62461-114">Interface identifier:</span></span>  <br/> |<span data-ttu-id="62461-115">IID_IMsgStore</span><span class="sxs-lookup"><span data-stu-id="62461-115">IID_IMsgStore</span></span>  <br/> |
|<span data-ttu-id="62461-116">Тип указателя:</span><span class="sxs-lookup"><span data-stu-id="62461-116">Pointer type:</span></span>  <br/> |<span data-ttu-id="62461-117">LPMDB</span><span class="sxs-lookup"><span data-stu-id="62461-117">LPMDB</span></span>  <br/> |
|<span data-ttu-id="62461-118">Модель транзакции:</span><span class="sxs-lookup"><span data-stu-id="62461-118">Transaction model:</span></span>  <br/> |<span data-ttu-id="62461-119">Nontransacted</span><span class="sxs-lookup"><span data-stu-id="62461-119">Nontransacted</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="62461-120">Заказ Vtable</span><span class="sxs-lookup"><span data-stu-id="62461-120">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="62461-121">Консультирование</span><span class="sxs-lookup"><span data-stu-id="62461-121">Advise</span></span>](imsgstore-advise.md) <br/> |<span data-ttu-id="62461-122">Регистрируется для получения уведомления о указанных событиях, влияющих на хранилище сообщений.</span><span class="sxs-lookup"><span data-stu-id="62461-122">Registers to receive notification of specified events that affect the message store.</span></span>  <br/> |
|[<span data-ttu-id="62461-123">Unadvise</span><span class="sxs-lookup"><span data-stu-id="62461-123">Unadvise</span></span>](imsgstore-unadvise.md) <br/> |<span data-ttu-id="62461-124">Отменяет отправку уведомлений, ранее установленных с помощью вызова в **метод IMsgStore::Advise.**</span><span class="sxs-lookup"><span data-stu-id="62461-124">Cancels the sending of notifications previously set up with a call to the **IMsgStore::Advise** method.</span></span>  <br/> |
|[<span data-ttu-id="62461-125">CompareEntryIDs</span><span class="sxs-lookup"><span data-stu-id="62461-125">CompareEntryIDs</span></span>](imsgstore-compareentryids.md) <br/> |<span data-ttu-id="62461-126">Сравнивает два идентификатора записи, чтобы определить, относятся ли они к одной и той же записи в хранилище сообщений.</span><span class="sxs-lookup"><span data-stu-id="62461-126">Compares two entry identifiers to determine whether they refer to the same entry in a message store.</span></span>  <br/> |
|[<span data-ttu-id="62461-127">OpenEntry</span><span class="sxs-lookup"><span data-stu-id="62461-127">OpenEntry</span></span>](imsgstore-openentry.md) <br/> |<span data-ttu-id="62461-128">Открывает папку или сообщение и возвращает указатель интерфейса для дальнейшего доступа.</span><span class="sxs-lookup"><span data-stu-id="62461-128">Opens a folder or message and returns an interface pointer for further access.</span></span>  <br/> |
|[<span data-ttu-id="62461-129">SetReceiveFolder</span><span class="sxs-lookup"><span data-stu-id="62461-129">SetReceiveFolder</span></span>](imsgstore-setreceivefolder.md) <br/> |<span data-ttu-id="62461-130">Устанавливает папку в качестве назначения для входящих сообщений определенного класса сообщений.</span><span class="sxs-lookup"><span data-stu-id="62461-130">Establishes a folder as the destination for incoming messages of a particular message class.</span></span>  <br/> |
|[<span data-ttu-id="62461-131">GetReceiveFolder</span><span class="sxs-lookup"><span data-stu-id="62461-131">GetReceiveFolder</span></span>](imsgstore-getreceivefolder.md) <br/> |<span data-ttu-id="62461-132">Получает папку, которая была установлена в качестве назначения для входящих сообщений указанного класса сообщений или в качестве папки получения по умолчанию для магазина сообщений.</span><span class="sxs-lookup"><span data-stu-id="62461-132">Obtains the folder that was established as the destination for incoming messages of a specified message class or as the default receive folder for the message store.</span></span>  <br/> |
|[<span data-ttu-id="62461-133">GetReceiveFolderTable</span><span class="sxs-lookup"><span data-stu-id="62461-133">GetReceiveFolderTable</span></span>](imsgstore-getreceivefoldertable.md) <br/> |<span data-ttu-id="62461-134">Предоставляет доступ к таблице папки получения, таблице с сведениями обо всех папках получения для магазина сообщений.</span><span class="sxs-lookup"><span data-stu-id="62461-134">Provides access to the receive folder table, a table with information about all of the receive folders for the message store.</span></span>  <br/> |
|[<span data-ttu-id="62461-135">StoreLogoff</span><span class="sxs-lookup"><span data-stu-id="62461-135">StoreLogoff</span></span>](imsgstore-storelogoff.md) <br/> |<span data-ttu-id="62461-136">Включает упорядоченный журнал магазина сообщений.</span><span class="sxs-lookup"><span data-stu-id="62461-136">Enables the orderly logoff of the message store.</span></span>  <br/> |
|[<span data-ttu-id="62461-137">AbortSubmit</span><span class="sxs-lookup"><span data-stu-id="62461-137">AbortSubmit</span></span>](imsgstore-abortsubmit.md) <br/> |<span data-ttu-id="62461-138">Попытки удалить сообщение из исходятой очереди.</span><span class="sxs-lookup"><span data-stu-id="62461-138">Attempts to remove a message from the outgoing queue.</span></span>  <br/> |
|[<span data-ttu-id="62461-139">GetOutgoingQueue</span><span class="sxs-lookup"><span data-stu-id="62461-139">GetOutgoingQueue</span></span>](imsgstore-getoutgoingqueue.md) <br/> |<span data-ttu-id="62461-140">Предоставляет доступ к исходя из таблицы очереди, таблице, которая содержит сведения обо всех сообщениях в исходях очередях магазина сообщений.</span><span class="sxs-lookup"><span data-stu-id="62461-140">Provides access to the outgoing queue table, a table that has information about all of the messages in the message store's outgoing queue.</span></span>  <br/> |
|[<span data-ttu-id="62461-141">SetLockState</span><span class="sxs-lookup"><span data-stu-id="62461-141">SetLockState</span></span>](imsgstore-setlockstate.md) <br/> |<span data-ttu-id="62461-142">Блокирует или разблокирует сообщение.</span><span class="sxs-lookup"><span data-stu-id="62461-142">Locks or unlocks a message.</span></span>  <br/> |
|[<span data-ttu-id="62461-143">FinishedMsg</span><span class="sxs-lookup"><span data-stu-id="62461-143">FinishedMsg</span></span>](imsgstore-finishedmsg.md) <br/> |<span data-ttu-id="62461-144">Позволяет поставщику хранения сообщений выполнять обработку отправленного сообщения.</span><span class="sxs-lookup"><span data-stu-id="62461-144">Enables the message store provider to perform processing on a sent message.</span></span>  <br/> |
|[<span data-ttu-id="62461-145">NotifyNewMail</span><span class="sxs-lookup"><span data-stu-id="62461-145">NotifyNewMail</span></span>](imsgstore-notifynewmail.md) <br/> |<span data-ttu-id="62461-146">����������� ��������� ���������, ����� ���������.</span><span class="sxs-lookup"><span data-stu-id="62461-146">Informs the message store that a new message has arrived.</span></span>  <br/> |
   
|<span data-ttu-id="62461-147">**Обязательные свойства**</span><span class="sxs-lookup"><span data-stu-id="62461-147">**Required properties**</span></span>|<span data-ttu-id="62461-148">**Уровень доступа**</span><span class="sxs-lookup"><span data-stu-id="62461-148">**Access level**</span></span>|
|:-----|:-----|
|<span data-ttu-id="62461-149">**PR_DISPLAY_NAME** [(PidTagDisplayName)](pidtagdisplayname-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="62461-149">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="62461-150">Чтение и запись</span><span class="sxs-lookup"><span data-stu-id="62461-150">Read/write</span></span>  <br/> |
|<span data-ttu-id="62461-151">**PR_ENTRYID** [(PidTagEntryId)](pidtagentryid-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="62461-151">**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="62461-152">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="62461-152">Read-only</span></span>  <br/> |
|<span data-ttu-id="62461-153">**PR_OBJECT_TYPE** [(PidTagObjectType)](pidtagobjecttype-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="62461-153">**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="62461-154">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="62461-154">Read-only</span></span>  <br/> |
|<span data-ttu-id="62461-155">**PR_RECORD_KEY** [(PidTagRecordKey](pidtagrecordkey-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="62461-155">**PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="62461-156">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="62461-156">Read-only</span></span>  <br/> |
|<span data-ttu-id="62461-157">**PR_STORE_ENTRYID** [(PidTagStoreEntryId)](pidtagstoreentryid-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="62461-157">**PR_STORE_ENTRYID** ([PidTagStoreEntryId](pidtagstoreentryid-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="62461-158">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="62461-158">Read-only</span></span>  <br/> |
|<span data-ttu-id="62461-159">**PR_STORE_RECORD_KEY** [(PidTagStoreRecordKey)](pidtagstorerecordkey-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="62461-159">**PR_STORE_RECORD_KEY** ([PidTagStoreRecordKey](pidtagstorerecordkey-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="62461-160">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="62461-160">Read-only</span></span>  <br/> |
|<span data-ttu-id="62461-161">**PR_MDB_PROVIDER** [(PidTagStoreProvider)](pidtagstoreprovider-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="62461-161">**PR_MDB_PROVIDER** ([PidTagStoreProvider](pidtagstoreprovider-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="62461-162">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="62461-162">Read-only</span></span>  <br/> |
|<span data-ttu-id="62461-163">**PR_STORE_SUPPORT_MASK** [(PidTagStoreSupportMask)](pidtagstoresupportmask-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="62461-163">**PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="62461-164">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="62461-164">Read-only</span></span>  <br/> |
   
<span data-ttu-id="62461-165">Следующие свойства для магазинов сообщений для межличностных сообщений (IPM):</span><span class="sxs-lookup"><span data-stu-id="62461-165">The following properties are for interpersonal message (IPM) message stores:</span></span>
  
- <span data-ttu-id="62461-166">**PR_IPM_OUTBOX_ENTRYID** [(PidTagIpmOutboxEntryId)](pidtagipmoutboxentryid-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="62461-166">**PR_IPM_OUTBOX_ENTRYID** ([PidTagIpmOutboxEntryId](pidtagipmoutboxentryid-canonical-property.md))</span></span>
    
- <span data-ttu-id="62461-167">**PR_IPM_SENTMAIL_ENTRYID** [(PidTagIpmSentMailEntryId)](pidtagipmsentmailentryid-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="62461-167">**PR_IPM_SENTMAIL_ENTRYID** ([PidTagIpmSentMailEntryId](pidtagipmsentmailentryid-canonical-property.md))</span></span>
    
- <span data-ttu-id="62461-168">**PR_IPM_SUBTREE_ENTRYID** [(PidTagIpmSubtreeEntryId](pidtagipmsubtreeentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="62461-168">**PR_IPM_SUBTREE_ENTRYID** ([PidTagIpmSubtreeEntryId](pidtagipmsubtreeentryid-canonical-property.md))</span></span>
    
- <span data-ttu-id="62461-169">**PR_IPM_WASTEBASKET_ENTRYID** [(PidTagIpmWastebasketEntryId)](pidtagipmwastebasketentryid-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="62461-169">**PR_IPM_WASTEBASKET_ENTRYID** ([PidTagIpmWastebasketEntryId](pidtagipmwastebasketentryid-canonical-property.md))</span></span>
    
- <span data-ttu-id="62461-170">**PR_MDB_PROVIDER**</span><span class="sxs-lookup"><span data-stu-id="62461-170">**PR_MDB_PROVIDER**</span></span>
    
- <span data-ttu-id="62461-171">**PR_STORE_SUPPORT_MASK**</span><span class="sxs-lookup"><span data-stu-id="62461-171">**PR_STORE_SUPPORT_MASK**</span></span>
    
## <a name="see-also"></a><span data-ttu-id="62461-172">См. также</span><span class="sxs-lookup"><span data-stu-id="62461-172">See also</span></span>



[<span data-ttu-id="62461-173">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="62461-173">MAPI Properties</span></span>](mapi-properties.md)

