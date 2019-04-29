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
# <a name="imsgstore--imapiprop"></a><span data-ttu-id="c145f-103">IMsgStore : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="c145f-103">IMsgStore : IMAPIProp</span></span>

  
  
<span data-ttu-id="c145f-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c145f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c145f-105">Предоставляет доступ к сведениям о хранилище сообщений, а также к сообщениям и папкам.</span><span class="sxs-lookup"><span data-stu-id="c145f-105">Provides access to message store information and to messages and folders.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="c145f-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="c145f-106">Header file:</span></span>  <br/> |<span data-ttu-id="c145f-107">MAPIDEFS. h</span><span class="sxs-lookup"><span data-stu-id="c145f-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="c145f-108">Предоставлено:</span><span class="sxs-lookup"><span data-stu-id="c145f-108">Exposed by:</span></span>  <br/> |<span data-ttu-id="c145f-109">Объект хранилища сообщений</span><span class="sxs-lookup"><span data-stu-id="c145f-109">Message store object</span></span>  <br/> |
|<span data-ttu-id="c145f-110">Реализовано в:</span><span class="sxs-lookup"><span data-stu-id="c145f-110">Implemented by:</span></span>  <br/> |<span data-ttu-id="c145f-111">Поставщики хранилища сообщений</span><span class="sxs-lookup"><span data-stu-id="c145f-111">Message store providers</span></span>  <br/> |
|<span data-ttu-id="c145f-112">Вызывающая сторона:</span><span class="sxs-lookup"><span data-stu-id="c145f-112">Called by:</span></span>  <br/> |<span data-ttu-id="c145f-113">Клиентские приложения, диспетчер очереди MAPI и MAPI</span><span class="sxs-lookup"><span data-stu-id="c145f-113">Client applications, the MAPI spooler, and MAPI</span></span>  <br/> |
|<span data-ttu-id="c145f-114">Идентификатор интерфейса:</span><span class="sxs-lookup"><span data-stu-id="c145f-114">Interface identifier:</span></span>  <br/> |<span data-ttu-id="c145f-115">Иид_имсгсторе</span><span class="sxs-lookup"><span data-stu-id="c145f-115">IID_IMsgStore</span></span>  <br/> |
|<span data-ttu-id="c145f-116">Тип указателя:</span><span class="sxs-lookup"><span data-stu-id="c145f-116">Pointer type:</span></span>  <br/> |<span data-ttu-id="c145f-117">ЛПМДБ</span><span class="sxs-lookup"><span data-stu-id="c145f-117">LPMDB</span></span>  <br/> |
|<span data-ttu-id="c145f-118">Модель транзакции:</span><span class="sxs-lookup"><span data-stu-id="c145f-118">Transaction model:</span></span>  <br/> |<span data-ttu-id="c145f-119">Не transactd</span><span class="sxs-lookup"><span data-stu-id="c145f-119">Nontransacted</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="c145f-120">Заказ vtable</span><span class="sxs-lookup"><span data-stu-id="c145f-120">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="c145f-121">Рекомендуем</span><span class="sxs-lookup"><span data-stu-id="c145f-121">Advise</span></span>](imsgstore-advise.md) <br/> |<span data-ttu-id="c145f-122">Регистрируется для получения уведомлений об указанных событиях, влияющих на хранилище сообщений.</span><span class="sxs-lookup"><span data-stu-id="c145f-122">Registers to receive notification of specified events that affect the message store.</span></span>  <br/> |
|[<span data-ttu-id="c145f-123">Unadvise</span><span class="sxs-lookup"><span data-stu-id="c145f-123">Unadvise</span></span>](imsgstore-unadvise.md) <br/> |<span data-ttu-id="c145f-124">ОтМеняет отправку уведомлений, ранее настроенных с помощью вызова метода **IMsgStore:: Advise** .</span><span class="sxs-lookup"><span data-stu-id="c145f-124">Cancels the sending of notifications previously set up with a call to the **IMsgStore::Advise** method.</span></span>  <br/> |
|[<span data-ttu-id="c145f-125">CompareEntryIDs</span><span class="sxs-lookup"><span data-stu-id="c145f-125">CompareEntryIDs</span></span>](imsgstore-compareentryids.md) <br/> |<span data-ttu-id="c145f-126">Сравнивает два идентификатора записи, чтобы определить, ссылаются ли они на одну и ту же запись в хранилище сообщений.</span><span class="sxs-lookup"><span data-stu-id="c145f-126">Compares two entry identifiers to determine whether they refer to the same entry in a message store.</span></span>  <br/> |
|[<span data-ttu-id="c145f-127">OpenEntry</span><span class="sxs-lookup"><span data-stu-id="c145f-127">OpenEntry</span></span>](imsgstore-openentry.md) <br/> |<span data-ttu-id="c145f-128">Открывает папку или сообщение и возвращает указатель интерфейса для получения дальнейших прав.</span><span class="sxs-lookup"><span data-stu-id="c145f-128">Opens a folder or message and returns an interface pointer for further access.</span></span>  <br/> |
|[<span data-ttu-id="c145f-129">Сетрецеивефолдер</span><span class="sxs-lookup"><span data-stu-id="c145f-129">SetReceiveFolder</span></span>](imsgstore-setreceivefolder.md) <br/> |<span data-ttu-id="c145f-130">Устанавливает папку в качестве назначения для входящих сообщений определенного класса сообщений.</span><span class="sxs-lookup"><span data-stu-id="c145f-130">Establishes a folder as the destination for incoming messages of a particular message class.</span></span>  <br/> |
|[<span data-ttu-id="c145f-131">Жетрецеивефолдер</span><span class="sxs-lookup"><span data-stu-id="c145f-131">GetReceiveFolder</span></span>](imsgstore-getreceivefolder.md) <br/> |<span data-ttu-id="c145f-132">Получает папку, которая была установлена в качестве назначения для входящих сообщений указанного класса сообщений или в качестве папки получения по умолчанию для хранилища сообщений.</span><span class="sxs-lookup"><span data-stu-id="c145f-132">Obtains the folder that was established as the destination for incoming messages of a specified message class or as the default receive folder for the message store.</span></span>  <br/> |
|[<span data-ttu-id="c145f-133">Жетрецеивефолдертабле</span><span class="sxs-lookup"><span data-stu-id="c145f-133">GetReceiveFolderTable</span></span>](imsgstore-getreceivefoldertable.md) <br/> |<span data-ttu-id="c145f-134">Предоставляет доступ к таблице получения папки, в которой содержатся сведения обо всех папках получения для хранилища сообщений.</span><span class="sxs-lookup"><span data-stu-id="c145f-134">Provides access to the receive folder table, a table with information about all of the receive folders for the message store.</span></span>  <br/> |
|[<span data-ttu-id="c145f-135">Сторелогофф</span><span class="sxs-lookup"><span data-stu-id="c145f-135">StoreLogoff</span></span>](imsgstore-storelogoff.md) <br/> |<span data-ttu-id="c145f-136">Позволяет выполнять упорядоченный выход из хранилища сообщений.</span><span class="sxs-lookup"><span data-stu-id="c145f-136">Enables the orderly logoff of the message store.</span></span>  <br/> |
|[<span data-ttu-id="c145f-137">Абортсубмит</span><span class="sxs-lookup"><span data-stu-id="c145f-137">AbortSubmit</span></span>](imsgstore-abortsubmit.md) <br/> |<span data-ttu-id="c145f-138">Пытается удалить сообщение из исходящей очереди.</span><span class="sxs-lookup"><span data-stu-id="c145f-138">Attempts to remove a message from the outgoing queue.</span></span>  <br/> |
|[<span data-ttu-id="c145f-139">Жетаутгоингкуеуе</span><span class="sxs-lookup"><span data-stu-id="c145f-139">GetOutgoingQueue</span></span>](imsgstore-getoutgoingqueue.md) <br/> |<span data-ttu-id="c145f-140">Предоставляет доступ к таблице исходящей очереди, таблице, содержащей сведения обо всех сообщениях в исходящей очереди хранилища сообщений.</span><span class="sxs-lookup"><span data-stu-id="c145f-140">Provides access to the outgoing queue table, a table that has information about all of the messages in the message store's outgoing queue.</span></span>  <br/> |
|[<span data-ttu-id="c145f-141">Сетлоккстате</span><span class="sxs-lookup"><span data-stu-id="c145f-141">SetLockState</span></span>](imsgstore-setlockstate.md) <br/> |<span data-ttu-id="c145f-142">Блокировка или разблокировка сообщения.</span><span class="sxs-lookup"><span data-stu-id="c145f-142">Locks or unlocks a message.</span></span>  <br/> |
|[<span data-ttu-id="c145f-143">Финишедмсг</span><span class="sxs-lookup"><span data-stu-id="c145f-143">FinishedMsg</span></span>](imsgstore-finishedmsg.md) <br/> |<span data-ttu-id="c145f-144">Позволяет поставщику хранилища сообщений выполнять обработку отправленного сообщения.</span><span class="sxs-lookup"><span data-stu-id="c145f-144">Enables the message store provider to perform processing on a sent message.</span></span>  <br/> |
|[<span data-ttu-id="c145f-145">Нотифиневмаил</span><span class="sxs-lookup"><span data-stu-id="c145f-145">NotifyNewMail</span></span>](imsgstore-notifynewmail.md) <br/> |<span data-ttu-id="c145f-146">����������� ��������� ���������, ����� ���������.</span><span class="sxs-lookup"><span data-stu-id="c145f-146">Informs the message store that a new message has arrived.</span></span>  <br/> |
   
|<span data-ttu-id="c145f-147">**Обязательные свойства**</span><span class="sxs-lookup"><span data-stu-id="c145f-147">**Required properties**</span></span>|<span data-ttu-id="c145f-148">**Уровень доступа**</span><span class="sxs-lookup"><span data-stu-id="c145f-148">**Access level**</span></span>|
|:-----|:-----|
|<span data-ttu-id="c145f-149">**Пр_дисплай_наме** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="c145f-149">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="c145f-150">Чтение и запись</span><span class="sxs-lookup"><span data-stu-id="c145f-150">Read/write</span></span>  <br/> |
|<span data-ttu-id="c145f-151">**Пр_ентрид** ([PidTagEntryId](pidtagentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="c145f-151">**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="c145f-152">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="c145f-152">Read-only</span></span>  <br/> |
|<span data-ttu-id="c145f-153">**Пр_обжект_типе** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="c145f-153">**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="c145f-154">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="c145f-154">Read-only</span></span>  <br/> |
|<span data-ttu-id="c145f-155">**Пр_рекорд_кэй** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="c145f-155">**PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="c145f-156">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="c145f-156">Read-only</span></span>  <br/> |
|<span data-ttu-id="c145f-157">**Пр_сторе_ентрид** ([PidTagStoreEntryId](pidtagstoreentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="c145f-157">**PR_STORE_ENTRYID** ([PidTagStoreEntryId](pidtagstoreentryid-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="c145f-158">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="c145f-158">Read-only</span></span>  <br/> |
|<span data-ttu-id="c145f-159">**Пр_сторе_рекорд_кэй** ([PidTagStoreRecordKey](pidtagstorerecordkey-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="c145f-159">**PR_STORE_RECORD_KEY** ([PidTagStoreRecordKey](pidtagstorerecordkey-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="c145f-160">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="c145f-160">Read-only</span></span>  <br/> |
|<span data-ttu-id="c145f-161">**Пр_мдб_провидер** ([PidTagStoreProvider](pidtagstoreprovider-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="c145f-161">**PR_MDB_PROVIDER** ([PidTagStoreProvider](pidtagstoreprovider-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="c145f-162">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="c145f-162">Read-only</span></span>  <br/> |
|<span data-ttu-id="c145f-163">**Пр_сторе_суппорт_маск** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="c145f-163">**PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="c145f-164">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="c145f-164">Read-only</span></span>  <br/> |
   
<span data-ttu-id="c145f-165">Для хранилищ сообщений взаимосвязанных сообщений (IPM) используются следующие свойства:</span><span class="sxs-lookup"><span data-stu-id="c145f-165">The following properties are for interpersonal message (IPM) message stores:</span></span>
  
- <span data-ttu-id="c145f-166">**Пр_ипм_аутбокс_ентрид** ([PidTagIpmOutboxEntryId](pidtagipmoutboxentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="c145f-166">**PR_IPM_OUTBOX_ENTRYID** ([PidTagIpmOutboxEntryId](pidtagipmoutboxentryid-canonical-property.md))</span></span>
    
- <span data-ttu-id="c145f-167">**Пр_ипм_сентмаил_ентрид** ([PidTagIpmSentMailEntryId](pidtagipmsentmailentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="c145f-167">**PR_IPM_SENTMAIL_ENTRYID** ([PidTagIpmSentMailEntryId](pidtagipmsentmailentryid-canonical-property.md))</span></span>
    
- <span data-ttu-id="c145f-168">**Пр_ипм_субтри_ентрид** ([PidTagIpmSubtreeEntryId](pidtagipmsubtreeentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="c145f-168">**PR_IPM_SUBTREE_ENTRYID** ([PidTagIpmSubtreeEntryId](pidtagipmsubtreeentryid-canonical-property.md))</span></span>
    
- <span data-ttu-id="c145f-169">**Пр_ипм_вастебаскет_ентрид** ([PidTagIpmWastebasketEntryId](pidtagipmwastebasketentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="c145f-169">**PR_IPM_WASTEBASKET_ENTRYID** ([PidTagIpmWastebasketEntryId](pidtagipmwastebasketentryid-canonical-property.md))</span></span>
    
- <span data-ttu-id="c145f-170">**ПР_МДБ_ПРОВИДЕР**</span><span class="sxs-lookup"><span data-stu-id="c145f-170">**PR_MDB_PROVIDER**</span></span>
    
- <span data-ttu-id="c145f-171">**ПР_СТОРЕ_СУППОРТ_МАСК**</span><span class="sxs-lookup"><span data-stu-id="c145f-171">**PR_STORE_SUPPORT_MASK**</span></span>
    
## <a name="see-also"></a><span data-ttu-id="c145f-172">См. также</span><span class="sxs-lookup"><span data-stu-id="c145f-172">See also</span></span>



[<span data-ttu-id="c145f-173">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="c145f-173">MAPI Properties</span></span>](mapi-properties.md)

