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
ms.openlocfilehash: 0905fbe2ba584aef49c50152aaf448267d477c10
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32348960"
---
# <a name="iabcontainer--imapicontainer"></a><span data-ttu-id="a8a67-103">IABContainer : IMAPIContainer</span><span class="sxs-lookup"><span data-stu-id="a8a67-103">IABContainer : IMAPIContainer</span></span>

<span data-ttu-id="a8a67-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a8a67-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a8a67-105">Предоставляет доступ к контейнерам адресной книги.</span><span class="sxs-lookup"><span data-stu-id="a8a67-105">Provides access to address book containers.</span></span> <span data-ttu-id="a8a67-106">MAPI и клиентские приложения называют методы **IABContainer** для выполнения разрешения имен и создания, копирования и удаления получателей.</span><span class="sxs-lookup"><span data-stu-id="a8a67-106">MAPI and client applications call the methods of **IABContainer** to perform name resolution and to create, copy, and delete recipients.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="a8a67-107">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="a8a67-107">Header file:</span></span>  <br/> |<span data-ttu-id="a8a67-108">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="a8a67-108">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="a8a67-109">Подвергается:</span><span class="sxs-lookup"><span data-stu-id="a8a67-109">Exposed by:</span></span>  <br/> |<span data-ttu-id="a8a67-110">Объекты контейнера адресной книги</span><span class="sxs-lookup"><span data-stu-id="a8a67-110">Address book container objects</span></span>  <br/> |
|<span data-ttu-id="a8a67-111">Реализовано в:</span><span class="sxs-lookup"><span data-stu-id="a8a67-111">Implemented by:</span></span>  <br/> |<span data-ttu-id="a8a67-112">Поставщики адресных книг</span><span class="sxs-lookup"><span data-stu-id="a8a67-112">Address book providers</span></span>  <br/> |
|<span data-ttu-id="a8a67-113">Вызывающая сторона:</span><span class="sxs-lookup"><span data-stu-id="a8a67-113">Called by:</span></span>  <br/> |<span data-ttu-id="a8a67-114">MAPI и клиентские приложения</span><span class="sxs-lookup"><span data-stu-id="a8a67-114">MAPI and client applications</span></span>  <br/> |
|<span data-ttu-id="a8a67-115">Идентификатор интерфейса:</span><span class="sxs-lookup"><span data-stu-id="a8a67-115">Interface identifier:</span></span>  <br/> |<span data-ttu-id="a8a67-116">IID_IABContainer</span><span class="sxs-lookup"><span data-stu-id="a8a67-116">IID_IABContainer</span></span>  <br/> |
|<span data-ttu-id="a8a67-117">Тип указателя:</span><span class="sxs-lookup"><span data-stu-id="a8a67-117">Pointer type:</span></span>  <br/> |<span data-ttu-id="a8a67-118">LPABCONT</span><span class="sxs-lookup"><span data-stu-id="a8a67-118">LPABCONT</span></span>  <br/> |
|<span data-ttu-id="a8a67-119">Модель транзакции:</span><span class="sxs-lookup"><span data-stu-id="a8a67-119">Transaction model:</span></span>  <br/> |<span data-ttu-id="a8a67-120">Transacted</span><span class="sxs-lookup"><span data-stu-id="a8a67-120">Transacted</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="a8a67-121">Заказ Vtable</span><span class="sxs-lookup"><span data-stu-id="a8a67-121">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="a8a67-122">CreateEntry</span><span class="sxs-lookup"><span data-stu-id="a8a67-122">CreateEntry</span></span>](iabcontainer-createentry.md) <br/> |<span data-ttu-id="a8a67-123">Создает новую запись, которая может быть пользователем обмена сообщениями, списком рассылки или другим контейнером.</span><span class="sxs-lookup"><span data-stu-id="a8a67-123">Creates a new entry, which can be a messaging user, a distribution list, or another container.</span></span>  <br/> |
|[<span data-ttu-id="a8a67-124">CopyEntries</span><span class="sxs-lookup"><span data-stu-id="a8a67-124">CopyEntries</span></span>](iabcontainer-copyentries.md) <br/> |<span data-ttu-id="a8a67-125">Копирует одну или несколько записей, как правило, пользователей сообщений или списки рассылки.</span><span class="sxs-lookup"><span data-stu-id="a8a67-125">Copies one or more entries, typically messaging users or distribution lists.</span></span>  <br/> |
|[<span data-ttu-id="a8a67-126">DeleteEntries</span><span class="sxs-lookup"><span data-stu-id="a8a67-126">DeleteEntries</span></span>](iabcontainer-deleteentries.md) <br/> |<span data-ttu-id="a8a67-127">Удаляет одну или несколько записей, как правило, пользователей сообщений, списки рассылки или другие контейнеры.</span><span class="sxs-lookup"><span data-stu-id="a8a67-127">Removes one or more entries, typically messaging users, distribution lists, or other containers.</span></span>  <br/> |
|[<span data-ttu-id="a8a67-128">ResolveNames</span><span class="sxs-lookup"><span data-stu-id="a8a67-128">ResolveNames</span></span>](iabcontainer-resolvenames.md) <br/> |<span data-ttu-id="a8a67-129">Выполняет разрешение имен для одной или более записей получателей.</span><span class="sxs-lookup"><span data-stu-id="a8a67-129">Performs name resolution for one or more recipient entries.</span></span>  <br/> |
   
|<span data-ttu-id="a8a67-130">**Обязательные свойства**</span><span class="sxs-lookup"><span data-stu-id="a8a67-130">**Required properties**</span></span>|<span data-ttu-id="a8a67-131">**Access**</span><span class="sxs-lookup"><span data-stu-id="a8a67-131">**Access**</span></span>|
|:-----|:-----|
|<span data-ttu-id="a8a67-132">**PR_CONTAINER_FLAGS** [(PidTagContainerFlags)](pidtagcontainerflags-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="a8a67-132">**PR_CONTAINER_FLAGS** ([PidTagContainerFlags](pidtagcontainerflags-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="a8a67-133">Чтение и запись</span><span class="sxs-lookup"><span data-stu-id="a8a67-133">Read/write</span></span>  <br/> |
|<span data-ttu-id="a8a67-134">**PR_DISPLAY_NAME** [(PidTagDisplayName)](pidtagdisplayname-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="a8a67-134">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="a8a67-135">Чтение и запись</span><span class="sxs-lookup"><span data-stu-id="a8a67-135">Read/write</span></span>  <br/> |
|<span data-ttu-id="a8a67-136">**PR_ENTRYID** [(PidTagEntryId)](pidtagentryid-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="a8a67-136">**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="a8a67-137">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="a8a67-137">Read-only</span></span>  <br/> |
|<span data-ttu-id="a8a67-138">**PR_OBJECT_TYPE** [(PidTagObjectType)](pidtagobjecttype-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="a8a67-138">**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="a8a67-139">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="a8a67-139">Read-only</span></span>  <br/> |
|<span data-ttu-id="a8a67-140">**PR_RECORD_KEY** [(PidTagRecordKey](pidtagrecordkey-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="a8a67-140">**PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="a8a67-141">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="a8a67-141">Read-only</span></span>  <br/> |
   
|<span data-ttu-id="a8a67-142">**Необязательные свойства**</span><span class="sxs-lookup"><span data-stu-id="a8a67-142">**Optional properties**</span></span>|<span data-ttu-id="a8a67-143">**Access**</span><span class="sxs-lookup"><span data-stu-id="a8a67-143">**Access**</span></span>|
|:-----|:-----|
|<span data-ttu-id="a8a67-144">**PR_CONTAINER_CONTENTS** [(PidTagContainerContents)](pidtagcontainercontents-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="a8a67-144">**PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="a8a67-145">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="a8a67-145">Read-only</span></span>  <br/> |
|<span data-ttu-id="a8a67-146">**PR_CONTAINER_HIERARCHY** [(PidTagContainerHierarchy)](pidtagcontainerhierarchy-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="a8a67-146">**PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="a8a67-147">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="a8a67-147">Read-only</span></span>  <br/> |
|<span data-ttu-id="a8a67-148">**PR_DEF_CREATE_DL** [(PidTagDefCreateDl](pidtagdefcreatedl-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="a8a67-148">**PR_DEF_CREATE_DL** ([PidTagDefCreateDl](pidtagdefcreatedl-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="a8a67-149">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="a8a67-149">Read-only</span></span>  <br/> |
|<span data-ttu-id="a8a67-150">**PR_DEF_CREATE_MAILUSER** [(PidTagDefCreateMailuser)](pidtagdefcreatemailuser-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="a8a67-150">**PR_DEF_CREATE_MAILUSER** ([PidTagDefCreateMailuser](pidtagdefcreatemailuser-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="a8a67-151">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="a8a67-151">Read-only</span></span>  <br/> |
|<span data-ttu-id="a8a67-152">**PR_DISPLAY_TYPE** [(PidTagDisplayType)](pidtagdisplaytype-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="a8a67-152">**PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="a8a67-153">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="a8a67-153">Read-only</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a8a67-154">Примечания</span><span class="sxs-lookup"><span data-stu-id="a8a67-154">Remarks</span></span>

<span data-ttu-id="a8a67-155">Интерфейс **IABContainer** косвенно наследуется от интерфейса IUnknown через [интерфейс IMAPIContainer: IMAPIProp и IMAPIProp:](imapicontainerimapiprop.md) интерфейсы [IUnknown.](imapipropiunknown.md) [](https://msdn.microsoft.com/library/ms680509%28VS.85%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="a8a67-155">The **IABContainer** interface inherits indirectly from the [IUnknown](https://msdn.microsoft.com/library/ms680509%28VS.85%29.aspx) interface through the [IMAPIContainer : IMAPIProp](imapicontainerimapiprop.md) and [IMAPIProp : IUnknown](imapipropiunknown.md) interfaces.</span></span> <span data-ttu-id="a8a67-156">Поставщики адресных книг реализуют **интерфейс IABContainer.**</span><span class="sxs-lookup"><span data-stu-id="a8a67-156">Address book providers implement the **IABContainer** interface.</span></span> 
  
<span data-ttu-id="a8a67-157">Любое количество объектов пользователей обмена сообщениями, списков рассылки и других контейнеров адресной книги может существовать в контейнере адресной книги.</span><span class="sxs-lookup"><span data-stu-id="a8a67-157">Any number of messaging user objects, distribution lists, and other address book containers can exist in an address book container.</span></span> <span data-ttu-id="a8a67-158">Как и в любом контейнере, клиенты или поставщики услуг могут использовать контейнер адресной книги для открытия одной из его записей или получения таблицы иерархии или таблицы содержимого.</span><span class="sxs-lookup"><span data-stu-id="a8a67-158">As with any container, clients or service providers can use an address book container to open one of its entries or to retrieve a hierarchy table or contents table.</span></span> <span data-ttu-id="a8a67-159">Контейнеры адресной книги также предоставляют разрешение имен и, в зависимости от поставщика, возможность добавлять, удалять или изменять записи.</span><span class="sxs-lookup"><span data-stu-id="a8a67-159">Address book containers also provide name resolution and, depending on the provider, the ability to add, remove, or modify entries.</span></span>
  
<span data-ttu-id="a8a67-160">MAPI определяет специальный контейнер адресной книги под названием личная адресная книга (PAB), который содержит записи, скопированные из других контейнеров.</span><span class="sxs-lookup"><span data-stu-id="a8a67-160">MAPI defines a special address book container called the personal address book (PAB) that holds entries copied from other containers.</span></span> <span data-ttu-id="a8a67-161">PAB всегда можно модификабельно.</span><span class="sxs-lookup"><span data-stu-id="a8a67-161">A PAB is always modifiable.</span></span> <span data-ttu-id="a8a67-162">Обычно пользователи заполняют свои PAB записями, обозначающие получателей, с которыми они чаще всего общаются.</span><span class="sxs-lookup"><span data-stu-id="a8a67-162">Users typically populate their PAB with entries designating the recipients with which they most frequently communicate.</span></span> <span data-ttu-id="a8a67-163">Кроме того, PAB может держать разовую адресную часть, а новые получатели еще не являются частью контейнера адресной книги.</span><span class="sxs-lookup"><span data-stu-id="a8a67-163">A PAB can also hold one-off addresses and new recipients not yet a part of any address book container.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="a8a67-164">См. также</span><span class="sxs-lookup"><span data-stu-id="a8a67-164">See also</span></span>

- [<span data-ttu-id="a8a67-165">Интерфейсы MAPI</span><span class="sxs-lookup"><span data-stu-id="a8a67-165">MAPI Interfaces</span></span>](mapi-interfaces.md)

