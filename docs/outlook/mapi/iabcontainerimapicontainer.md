---
title: Иабконтаинер IMAPIContainer
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
ms.openlocfilehash: 0905fbe2ba584aef49c50152aaf448267d477c10
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32348960"
---
# <a name="iabcontainer--imapicontainer"></a><span data-ttu-id="cd31d-103">IABContainer : IMAPIContainer</span><span class="sxs-lookup"><span data-stu-id="cd31d-103">IABContainer : IMAPIContainer</span></span>

<span data-ttu-id="cd31d-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="cd31d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="cd31d-105">Предоставляет доступ к контейнерам адресной книги.</span><span class="sxs-lookup"><span data-stu-id="cd31d-105">Provides access to address book containers.</span></span> <span data-ttu-id="cd31d-106">MAPI и клиентские приложения вызывают методы **иабконтаинер** , чтобы выполнять разрешение имен, а также создавать, копировать и удалять получателей.</span><span class="sxs-lookup"><span data-stu-id="cd31d-106">MAPI and client applications call the methods of **IABContainer** to perform name resolution and to create, copy, and delete recipients.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="cd31d-107">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="cd31d-107">Header file:</span></span>  <br/> |<span data-ttu-id="cd31d-108">MAPIDEFS. h</span><span class="sxs-lookup"><span data-stu-id="cd31d-108">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="cd31d-109">Предоставлено:</span><span class="sxs-lookup"><span data-stu-id="cd31d-109">Exposed by:</span></span>  <br/> |<span data-ttu-id="cd31d-110">Объекты контейнера адресной книги</span><span class="sxs-lookup"><span data-stu-id="cd31d-110">Address book container objects</span></span>  <br/> |
|<span data-ttu-id="cd31d-111">Реализовано в:</span><span class="sxs-lookup"><span data-stu-id="cd31d-111">Implemented by:</span></span>  <br/> |<span data-ttu-id="cd31d-112">Поставщики адресных книг</span><span class="sxs-lookup"><span data-stu-id="cd31d-112">Address book providers</span></span>  <br/> |
|<span data-ttu-id="cd31d-113">Вызывающая сторона:</span><span class="sxs-lookup"><span data-stu-id="cd31d-113">Called by:</span></span>  <br/> |<span data-ttu-id="cd31d-114">MAPI и клиентские приложения</span><span class="sxs-lookup"><span data-stu-id="cd31d-114">MAPI and client applications</span></span>  <br/> |
|<span data-ttu-id="cd31d-115">Идентификатор интерфейса:</span><span class="sxs-lookup"><span data-stu-id="cd31d-115">Interface identifier:</span></span>  <br/> |<span data-ttu-id="cd31d-116">IID_IABContainer</span><span class="sxs-lookup"><span data-stu-id="cd31d-116">IID_IABContainer</span></span>  <br/> |
|<span data-ttu-id="cd31d-117">Тип указателя:</span><span class="sxs-lookup"><span data-stu-id="cd31d-117">Pointer type:</span></span>  <br/> |<span data-ttu-id="cd31d-118">лпабконт</span><span class="sxs-lookup"><span data-stu-id="cd31d-118">LPABCONT</span></span>  <br/> |
|<span data-ttu-id="cd31d-119">Модель транзакции:</span><span class="sxs-lookup"><span data-stu-id="cd31d-119">Transaction model:</span></span>  <br/> |<span data-ttu-id="cd31d-120">Транзакции</span><span class="sxs-lookup"><span data-stu-id="cd31d-120">Transacted</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="cd31d-121">Заказ vtable</span><span class="sxs-lookup"><span data-stu-id="cd31d-121">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="cd31d-122">креатинтри</span><span class="sxs-lookup"><span data-stu-id="cd31d-122">CreateEntry</span></span>](iabcontainer-createentry.md) <br/> |<span data-ttu-id="cd31d-123">Создает новую запись, которая может быть пользователем обмена сообщениями, списком рассылки или другим контейнером.</span><span class="sxs-lookup"><span data-stu-id="cd31d-123">Creates a new entry, which can be a messaging user, a distribution list, or another container.</span></span>  <br/> |
|[<span data-ttu-id="cd31d-124">копентриес</span><span class="sxs-lookup"><span data-stu-id="cd31d-124">CopyEntries</span></span>](iabcontainer-copyentries.md) <br/> |<span data-ttu-id="cd31d-125">Копирует одну или несколько записей, как правило, пользователи системы обмена сообщениями или списки рассылки.</span><span class="sxs-lookup"><span data-stu-id="cd31d-125">Copies one or more entries, typically messaging users or distribution lists.</span></span>  <br/> |
|[<span data-ttu-id="cd31d-126">делетинтриес</span><span class="sxs-lookup"><span data-stu-id="cd31d-126">DeleteEntries</span></span>](iabcontainer-deleteentries.md) <br/> |<span data-ttu-id="cd31d-127">Удаляет одну или несколько записей, как правило, пользователи системы обмена сообщениями, списки рассылки или другие контейнеры.</span><span class="sxs-lookup"><span data-stu-id="cd31d-127">Removes one or more entries, typically messaging users, distribution lists, or other containers.</span></span>  <br/> |
|[<span data-ttu-id="cd31d-128">ResolveNames</span><span class="sxs-lookup"><span data-stu-id="cd31d-128">ResolveNames</span></span>](iabcontainer-resolvenames.md) <br/> |<span data-ttu-id="cd31d-129">Выполняет разрешение имен для одной или нескольких записей получателей.</span><span class="sxs-lookup"><span data-stu-id="cd31d-129">Performs name resolution for one or more recipient entries.</span></span>  <br/> |
   
|<span data-ttu-id="cd31d-130">**Обязательные свойства**</span><span class="sxs-lookup"><span data-stu-id="cd31d-130">**Required properties**</span></span>|<span data-ttu-id="cd31d-131">**Access**</span><span class="sxs-lookup"><span data-stu-id="cd31d-131">**Access**</span></span>|
|:-----|:-----|
|<span data-ttu-id="cd31d-132">**PR_CONTAINER_FLAGS** ([PidTagContainerFlags](pidtagcontainerflags-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="cd31d-132">**PR_CONTAINER_FLAGS** ([PidTagContainerFlags](pidtagcontainerflags-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="cd31d-133">Чтение и запись</span><span class="sxs-lookup"><span data-stu-id="cd31d-133">Read/write</span></span>  <br/> |
|<span data-ttu-id="cd31d-134">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="cd31d-134">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="cd31d-135">Чтение и запись</span><span class="sxs-lookup"><span data-stu-id="cd31d-135">Read/write</span></span>  <br/> |
|<span data-ttu-id="cd31d-136">**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="cd31d-136">**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="cd31d-137">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="cd31d-137">Read-only</span></span>  <br/> |
|<span data-ttu-id="cd31d-138">**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="cd31d-138">**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="cd31d-139">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="cd31d-139">Read-only</span></span>  <br/> |
|<span data-ttu-id="cd31d-140">**PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="cd31d-140">**PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="cd31d-141">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="cd31d-141">Read-only</span></span>  <br/> |
   
|<span data-ttu-id="cd31d-142">**Необязательные свойства**</span><span class="sxs-lookup"><span data-stu-id="cd31d-142">**Optional properties**</span></span>|<span data-ttu-id="cd31d-143">**Access**</span><span class="sxs-lookup"><span data-stu-id="cd31d-143">**Access**</span></span>|
|:-----|:-----|
|<span data-ttu-id="cd31d-144">**PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="cd31d-144">**PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="cd31d-145">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="cd31d-145">Read-only</span></span>  <br/> |
|<span data-ttu-id="cd31d-146">**PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="cd31d-146">**PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="cd31d-147">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="cd31d-147">Read-only</span></span>  <br/> |
|<span data-ttu-id="cd31d-148">**PR_DEF_CREATE_DL** ([PidTagDefCreateDl](pidtagdefcreatedl-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="cd31d-148">**PR_DEF_CREATE_DL** ([PidTagDefCreateDl](pidtagdefcreatedl-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="cd31d-149">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="cd31d-149">Read-only</span></span>  <br/> |
|<span data-ttu-id="cd31d-150">**PR_DEF_CREATE_MAILUSER** ([PidTagDefCreateMailuser](pidtagdefcreatemailuser-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="cd31d-150">**PR_DEF_CREATE_MAILUSER** ([PidTagDefCreateMailuser](pidtagdefcreatemailuser-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="cd31d-151">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="cd31d-151">Read-only</span></span>  <br/> |
|<span data-ttu-id="cd31d-152">**PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="cd31d-152">**PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="cd31d-153">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="cd31d-153">Read-only</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="cd31d-154">Примечания</span><span class="sxs-lookup"><span data-stu-id="cd31d-154">Remarks</span></span>

<span data-ttu-id="cd31d-155">Интерфейс **иабконтаинер** наследует косвенно от интерфейса [IUnknown](https://msdn.microsoft.com/library/ms680509%28VS.85%29.aspx) через интерфейс [IMAPIContainer: IMAPIProp](imapicontainerimapiprop.md) и [IMAPIProp: интерфейс IUnknown](imapipropiunknown.md) .</span><span class="sxs-lookup"><span data-stu-id="cd31d-155">The **IABContainer** interface inherits indirectly from the [IUnknown](https://msdn.microsoft.com/library/ms680509%28VS.85%29.aspx) interface through the [IMAPIContainer : IMAPIProp](imapicontainerimapiprop.md) and [IMAPIProp : IUnknown](imapipropiunknown.md) interfaces.</span></span> <span data-ttu-id="cd31d-156">Поставщики адресных книг реализуют интерфейс **иабконтаинер** .</span><span class="sxs-lookup"><span data-stu-id="cd31d-156">Address book providers implement the **IABContainer** interface.</span></span> 
  
<span data-ttu-id="cd31d-157">В контейнере адресной книги может существовать любое количество объектов User Messaging, списков рассылки и других контейнеров адресных книг.</span><span class="sxs-lookup"><span data-stu-id="cd31d-157">Any number of messaging user objects, distribution lists, and other address book containers can exist in an address book container.</span></span> <span data-ttu-id="cd31d-158">Как и в случае с любым контейнером, клиенты или поставщики услуг могут использовать контейнер адресной книги для открытия одной из записей или для получения таблицы иерархии или таблицы контента.</span><span class="sxs-lookup"><span data-stu-id="cd31d-158">As with any container, clients or service providers can use an address book container to open one of its entries or to retrieve a hierarchy table or contents table.</span></span> <span data-ttu-id="cd31d-159">Контейнеры адресных книг также обеспечивают разрешение имен и, в зависимости от поставщика, возможность добавлять, удалять или изменять записи.</span><span class="sxs-lookup"><span data-stu-id="cd31d-159">Address book containers also provide name resolution and, depending on the provider, the ability to add, remove, or modify entries.</span></span>
  
<span data-ttu-id="cd31d-160">MAPI определяет специальный контейнер адресной книги, который называется личной адресной книгой (PAB), которая содержит записи, скопированные из других контейнеров.</span><span class="sxs-lookup"><span data-stu-id="cd31d-160">MAPI defines a special address book container called the personal address book (PAB) that holds entries copied from other containers.</span></span> <span data-ttu-id="cd31d-161">Адрес личной адресной книги всегда является изменяемым.</span><span class="sxs-lookup"><span data-stu-id="cd31d-161">A PAB is always modifiable.</span></span> <span data-ttu-id="cd31d-162">Обычно пользователи заполняют личную адресную книгу записями, указывающими получателям, с которыми они чаще всего часто обмениваются данными.</span><span class="sxs-lookup"><span data-stu-id="cd31d-162">Users typically populate their PAB with entries designating the recipients with which they most frequently communicate.</span></span> <span data-ttu-id="cd31d-163">Адресная книга также может содержать один и тот же адрес, а новые получатели не являются частью какого бы то ни было контейнера адресной книги.</span><span class="sxs-lookup"><span data-stu-id="cd31d-163">A PAB can also hold one-off addresses and new recipients not yet a part of any address book container.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="cd31d-164">См. также</span><span class="sxs-lookup"><span data-stu-id="cd31d-164">See also</span></span>

- [<span data-ttu-id="cd31d-165">Интерфейсы MAPI</span><span class="sxs-lookup"><span data-stu-id="cd31d-165">MAPI Interfaces</span></span>](mapi-interfaces.md)

