---
title: IABContainer IMAPIContainer
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IABContainer
api_type:
- COM
ms.assetid: 1f5ce6e0-b79a-4da2-b014-8c00cd72912e
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 0eb6d62b64595474957415e94275d0ac52cc2b6b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19808708"
---
# <a name="iabcontainer--imapicontainer"></a><span data-ttu-id="60cb2-103">IABContainer : IMAPIContainer</span><span class="sxs-lookup"><span data-stu-id="60cb2-103">IABContainer : IMAPIContainer</span></span>

<span data-ttu-id="60cb2-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="60cb2-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="60cb2-105">Предоставляет доступ к адресной книге контейнеров.</span><span class="sxs-lookup"><span data-stu-id="60cb2-105">Provides access to address book containers.</span></span> <span data-ttu-id="60cb2-106">MAPI и клиентских приложениях вызвать методы **IABContainer** выполнять разрешение имен и создание, копирование и удаление получателей.</span><span class="sxs-lookup"><span data-stu-id="60cb2-106">MAPI and client applications call the methods of **IABContainer** to perform name resolution and to create, copy, and delete recipients.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="60cb2-107">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="60cb2-107">Header file:</span></span>  <br/> |<span data-ttu-id="60cb2-108">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="60cb2-108">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="60cb2-109">Предоставляемые:</span><span class="sxs-lookup"><span data-stu-id="60cb2-109">Exposed by:</span></span>  <br/> |<span data-ttu-id="60cb2-110">Адресной книги контейнер объектов</span><span class="sxs-lookup"><span data-stu-id="60cb2-110">Address book container objects</span></span>  <br/> |
|<span data-ttu-id="60cb2-111">Реализованный:</span><span class="sxs-lookup"><span data-stu-id="60cb2-111">Implemented by:</span></span>  <br/> |<span data-ttu-id="60cb2-112">Поставщиками адресных книг</span><span class="sxs-lookup"><span data-stu-id="60cb2-112">Address book providers</span></span>  <br/> |
|<span data-ttu-id="60cb2-113">Вызывается:</span><span class="sxs-lookup"><span data-stu-id="60cb2-113">Called by:</span></span>  <br/> |<span data-ttu-id="60cb2-114">MAPI и клиентских приложениях</span><span class="sxs-lookup"><span data-stu-id="60cb2-114">MAPI and client applications</span></span>  <br/> |
|<span data-ttu-id="60cb2-115">Идентификатор интерфейса:</span><span class="sxs-lookup"><span data-stu-id="60cb2-115">Interface identifier:</span></span>  <br/> |<span data-ttu-id="60cb2-116">IID_IABContainer</span><span class="sxs-lookup"><span data-stu-id="60cb2-116">IID_IABContainer</span></span>  <br/> |
|<span data-ttu-id="60cb2-117">Тип указателя:</span><span class="sxs-lookup"><span data-stu-id="60cb2-117">Pointer type:</span></span>  <br/> |<span data-ttu-id="60cb2-118">LPABCONT</span><span class="sxs-lookup"><span data-stu-id="60cb2-118">LPABCONT</span></span>  <br/> |
|<span data-ttu-id="60cb2-119">Модель транзакций:</span><span class="sxs-lookup"><span data-stu-id="60cb2-119">Transaction model:</span></span>  <br/> |<span data-ttu-id="60cb2-120">В транзакции</span><span class="sxs-lookup"><span data-stu-id="60cb2-120">Transacted</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="60cb2-121">Порядке vtable</span><span class="sxs-lookup"><span data-stu-id="60cb2-121">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="60cb2-122">CreateEntry</span><span class="sxs-lookup"><span data-stu-id="60cb2-122">CreateEntry</span></span>](iabcontainer-createentry.md) <br/> |<span data-ttu-id="60cb2-123">Создает новый объект, который может быть обмена сообщениями пользователя, в список рассылки или другой контейнер.</span><span class="sxs-lookup"><span data-stu-id="60cb2-123">Creates a new entry, which can be a messaging user, a distribution list, or another container.</span></span>  <br/> |
|[<span data-ttu-id="60cb2-124">CopyEntries</span><span class="sxs-lookup"><span data-stu-id="60cb2-124">CopyEntries</span></span>](iabcontainer-copyentries.md) <br/> |<span data-ttu-id="60cb2-125">Копирует один или несколько операций, пользователи обычно обмена мгновенными сообщениями или списки рассылки.</span><span class="sxs-lookup"><span data-stu-id="60cb2-125">Copies one or more entries, typically messaging users or distribution lists.</span></span>  <br/> |
|[<span data-ttu-id="60cb2-126">Внешнее</span><span class="sxs-lookup"><span data-stu-id="60cb2-126">DeleteEntries</span></span>](iabcontainer-deleteentries.md) <br/> |<span data-ttu-id="60cb2-127">Удаляет один или несколько операций, обычно системы обмена сообщениями пользователи, списков рассылки или других контейнеров.</span><span class="sxs-lookup"><span data-stu-id="60cb2-127">Removes one or more entries, typically messaging users, distribution lists, or other containers.</span></span>  <br/> |
|[<span data-ttu-id="60cb2-128">ResolveNames</span><span class="sxs-lookup"><span data-stu-id="60cb2-128">ResolveNames</span></span>](iabcontainer-resolvenames.md) <br/> |<span data-ttu-id="60cb2-129">Выполняет разрешение имен для одного или нескольких получателей записей.</span><span class="sxs-lookup"><span data-stu-id="60cb2-129">Performs name resolution for one or more recipient entries.</span></span>  <br/> |
   
|<span data-ttu-id="60cb2-130">**Обязательные свойства**</span><span class="sxs-lookup"><span data-stu-id="60cb2-130">**Required properties**</span></span>|<span data-ttu-id="60cb2-131">**Access**</span><span class="sxs-lookup"><span data-stu-id="60cb2-131">**Access**</span></span>|
|:-----|:-----|
|<span data-ttu-id="60cb2-132">**PR_CONTAINER_FLAGS** ([PidTagContainerFlags](pidtagcontainerflags-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="60cb2-132">**PR_CONTAINER_FLAGS** ([PidTagContainerFlags](pidtagcontainerflags-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="60cb2-133">Чтение и запись</span><span class="sxs-lookup"><span data-stu-id="60cb2-133">Read/write</span></span>  <br/> |
|<span data-ttu-id="60cb2-134">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="60cb2-134">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="60cb2-135">Чтение и запись</span><span class="sxs-lookup"><span data-stu-id="60cb2-135">Read/write</span></span>  <br/> |
|<span data-ttu-id="60cb2-136">**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="60cb2-136">**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="60cb2-137">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="60cb2-137">Read-only</span></span>  <br/> |
|<span data-ttu-id="60cb2-138">**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="60cb2-138">**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="60cb2-139">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="60cb2-139">Read-only</span></span>  <br/> |
|<span data-ttu-id="60cb2-140">**PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="60cb2-140">**PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="60cb2-141">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="60cb2-141">Read-only</span></span>  <br/> |
   
|<span data-ttu-id="60cb2-142">**Дополнительные свойства**</span><span class="sxs-lookup"><span data-stu-id="60cb2-142">**Optional properties**</span></span>|<span data-ttu-id="60cb2-143">**Access**</span><span class="sxs-lookup"><span data-stu-id="60cb2-143">**Access**</span></span>|
|:-----|:-----|
|<span data-ttu-id="60cb2-144">**PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="60cb2-144">**PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="60cb2-145">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="60cb2-145">Read-only</span></span>  <br/> |
|<span data-ttu-id="60cb2-146">**PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="60cb2-146">**PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="60cb2-147">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="60cb2-147">Read-only</span></span>  <br/> |
|<span data-ttu-id="60cb2-148">**PR_DEF_CREATE_DL** ([PidTagDefCreateDl](pidtagdefcreatedl-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="60cb2-148">**PR_DEF_CREATE_DL** ([PidTagDefCreateDl](pidtagdefcreatedl-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="60cb2-149">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="60cb2-149">Read-only</span></span>  <br/> |
|<span data-ttu-id="60cb2-150">**PR_DEF_CREATE_MAILUSER** ([PidTagDefCreateMailuser](pidtagdefcreatemailuser-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="60cb2-150">**PR_DEF_CREATE_MAILUSER** ([PidTagDefCreateMailuser](pidtagdefcreatemailuser-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="60cb2-151">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="60cb2-151">Read-only</span></span>  <br/> |
|<span data-ttu-id="60cb2-152">**PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="60cb2-152">**PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="60cb2-153">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="60cb2-153">Read-only</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="60cb2-154">Замечания</span><span class="sxs-lookup"><span data-stu-id="60cb2-154">Remarks</span></span>

<span data-ttu-id="60cb2-155">Интерфейс **IABContainer** косвенно наследуется от интерфейс [IUnknown](http://msdn.microsoft.com/en-us/library/ms680509%28VS.85%29.aspx) через [IMAPIContainer: IMAPIProp](imapicontainerimapiprop.md) и [IMAPIProp: IUnknown](imapipropiunknown.md) интерфейсов.</span><span class="sxs-lookup"><span data-stu-id="60cb2-155">The **IABContainer** interface inherits indirectly from the [IUnknown](http://msdn.microsoft.com/en-us/library/ms680509%28VS.85%29.aspx) interface through the [IMAPIContainer : IMAPIProp](imapicontainerimapiprop.md) and [IMAPIProp : IUnknown](imapipropiunknown.md) interfaces.</span></span> <span data-ttu-id="60cb2-156">Интерфейс **IABContainer** внедряемые поставщиками адресной книги.</span><span class="sxs-lookup"><span data-stu-id="60cb2-156">Address book providers implement the **IABContainer** interface.</span></span> 
  
<span data-ttu-id="60cb2-157">В контейнер адресной книги может быть любое количество обмена сообщениями объектов-пользователей, списков рассылки и других контейнеров адресной книги.</span><span class="sxs-lookup"><span data-stu-id="60cb2-157">Any number of messaging user objects, distribution lists, and other address book containers can exist in an address book container.</span></span> <span data-ttu-id="60cb2-158">Как и в любой контейнер клиентов или поставщиков услуг можно использовать контейнер адресной книги для открытия один из его записи или для получения таблицы иерархии или таблицу содержимого.</span><span class="sxs-lookup"><span data-stu-id="60cb2-158">As with any container, clients or service providers can use an address book container to open one of its entries or to retrieve a hierarchy table or contents table.</span></span> <span data-ttu-id="60cb2-159">Адресная книга также предоставить разрешение имен и контейнеры, в зависимости от поставщика, возможность добавления, удаления или изменения записей.</span><span class="sxs-lookup"><span data-stu-id="60cb2-159">Address book containers also provide name resolution and, depending on the provider, the ability to add, remove, or modify entries.</span></span>
  
<span data-ttu-id="60cb2-160">MAPI определяет контейнер специальные адресной книги, называется Личная адресная книга (PAB-файла), в котором содержатся элементы, скопированные из других контейнеров.</span><span class="sxs-lookup"><span data-stu-id="60cb2-160">MAPI defines a special address book container called the personal address book (PAB) that holds entries copied from other containers.</span></span> <span data-ttu-id="60cb2-161">Адресной книги всегда можно изменить.</span><span class="sxs-lookup"><span data-stu-id="60cb2-161">A PAB is always modifiable.</span></span> <span data-ttu-id="60cb2-162">Пользователи обычно заполнения их адресной книги с записями, обозначение получателей, с которыми они наиболее часто общаетесь.</span><span class="sxs-lookup"><span data-stu-id="60cb2-162">Users typically populate their PAB with entries designating the recipients with which they most frequently communicate.</span></span> <span data-ttu-id="60cb2-163">Адресной книги, удерживая одноразовых адресов и новых получателей еще не являющихся частью любой контейнер адресной книги.</span><span class="sxs-lookup"><span data-stu-id="60cb2-163">A PAB can also hold one-off addresses and new recipients not yet a part of any address book container.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="60cb2-164">См. также</span><span class="sxs-lookup"><span data-stu-id="60cb2-164">See also</span></span>

- [<span data-ttu-id="60cb2-165">Интерфейсы MAPI</span><span class="sxs-lookup"><span data-stu-id="60cb2-165">MAPI Interfaces</span></span>](mapi-interfaces.md)

