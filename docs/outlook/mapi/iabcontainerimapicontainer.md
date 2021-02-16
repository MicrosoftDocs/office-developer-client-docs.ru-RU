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
# <a name="iabcontainer--imapicontainer"></a><span data-ttu-id="1cf14-103">IABContainer : IMAPIContainer</span><span class="sxs-lookup"><span data-stu-id="1cf14-103">IABContainer : IMAPIContainer</span></span>

<span data-ttu-id="1cf14-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1cf14-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1cf14-105">Предоставляет доступ к контейнерам адресной книги.</span><span class="sxs-lookup"><span data-stu-id="1cf14-105">Provides access to address book containers.</span></span> <span data-ttu-id="1cf14-106">MAPI и клиентские приложения вызывали методы **IABContainer** для разрешения имен и создания, копирования и удаления получателей.</span><span class="sxs-lookup"><span data-stu-id="1cf14-106">MAPI and client applications call the methods of **IABContainer** to perform name resolution and to create, copy, and delete recipients.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="1cf14-107">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="1cf14-107">Header file:</span></span>  <br/> |<span data-ttu-id="1cf14-108">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="1cf14-108">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="1cf14-109">Выставим:</span><span class="sxs-lookup"><span data-stu-id="1cf14-109">Exposed by:</span></span>  <br/> |<span data-ttu-id="1cf14-110">Объекты контейнеров адресной книги</span><span class="sxs-lookup"><span data-stu-id="1cf14-110">Address book container objects</span></span>  <br/> |
|<span data-ttu-id="1cf14-111">Реализовано в:</span><span class="sxs-lookup"><span data-stu-id="1cf14-111">Implemented by:</span></span>  <br/> |<span data-ttu-id="1cf14-112">Поставщики адресных книг</span><span class="sxs-lookup"><span data-stu-id="1cf14-112">Address book providers</span></span>  <br/> |
|<span data-ttu-id="1cf14-113">Вызывающая сторона:</span><span class="sxs-lookup"><span data-stu-id="1cf14-113">Called by:</span></span>  <br/> |<span data-ttu-id="1cf14-114">MAPI и клиентские приложения</span><span class="sxs-lookup"><span data-stu-id="1cf14-114">MAPI and client applications</span></span>  <br/> |
|<span data-ttu-id="1cf14-115">Идентификатор интерфейса:</span><span class="sxs-lookup"><span data-stu-id="1cf14-115">Interface identifier:</span></span>  <br/> |<span data-ttu-id="1cf14-116">IID_IABContainer</span><span class="sxs-lookup"><span data-stu-id="1cf14-116">IID_IABContainer</span></span>  <br/> |
|<span data-ttu-id="1cf14-117">Тип указателя:</span><span class="sxs-lookup"><span data-stu-id="1cf14-117">Pointer type:</span></span>  <br/> |<span data-ttu-id="1cf14-118">LPABCONT</span><span class="sxs-lookup"><span data-stu-id="1cf14-118">LPABCONT</span></span>  <br/> |
|<span data-ttu-id="1cf14-119">Модель транзакций:</span><span class="sxs-lookup"><span data-stu-id="1cf14-119">Transaction model:</span></span>  <br/> |<span data-ttu-id="1cf14-120">Transacted</span><span class="sxs-lookup"><span data-stu-id="1cf14-120">Transacted</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="1cf14-121">Порядок ветвей</span><span class="sxs-lookup"><span data-stu-id="1cf14-121">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="1cf14-122">CreateEntry</span><span class="sxs-lookup"><span data-stu-id="1cf14-122">CreateEntry</span></span>](iabcontainer-createentry.md) <br/> |<span data-ttu-id="1cf14-123">Создает новую запись, которая может быть пользователем системы обмена сообщениями, списком рассылки или другим контейнером.</span><span class="sxs-lookup"><span data-stu-id="1cf14-123">Creates a new entry, which can be a messaging user, a distribution list, or another container.</span></span>  <br/> |
|[<span data-ttu-id="1cf14-124">CopyEntries</span><span class="sxs-lookup"><span data-stu-id="1cf14-124">CopyEntries</span></span>](iabcontainer-copyentries.md) <br/> |<span data-ttu-id="1cf14-125">Копирует одну или несколько записей, как правило, для обмена сообщениями с пользователями или списками рассылки.</span><span class="sxs-lookup"><span data-stu-id="1cf14-125">Copies one or more entries, typically messaging users or distribution lists.</span></span>  <br/> |
|[<span data-ttu-id="1cf14-126">DeleteEntries</span><span class="sxs-lookup"><span data-stu-id="1cf14-126">DeleteEntries</span></span>](iabcontainer-deleteentries.md) <br/> |<span data-ttu-id="1cf14-127">Удаляет одну или несколько записей, обычно для обмена сообщениями пользователей, списков рассылки или других контейнеров.</span><span class="sxs-lookup"><span data-stu-id="1cf14-127">Removes one or more entries, typically messaging users, distribution lists, or other containers.</span></span>  <br/> |
|[<span data-ttu-id="1cf14-128">ResolveNames</span><span class="sxs-lookup"><span data-stu-id="1cf14-128">ResolveNames</span></span>](iabcontainer-resolvenames.md) <br/> |<span data-ttu-id="1cf14-129">Выполняет разрешение имен для одной или более записей получателей.</span><span class="sxs-lookup"><span data-stu-id="1cf14-129">Performs name resolution for one or more recipient entries.</span></span>  <br/> |
   
|<span data-ttu-id="1cf14-130">**Обязательные свойства**</span><span class="sxs-lookup"><span data-stu-id="1cf14-130">**Required properties**</span></span>|<span data-ttu-id="1cf14-131">**Access**</span><span class="sxs-lookup"><span data-stu-id="1cf14-131">**Access**</span></span>|
|:-----|:-----|
|<span data-ttu-id="1cf14-132">**PR_CONTAINER_FLAGS** ([PidTagContainerFlags)](pidtagcontainerflags-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="1cf14-132">**PR_CONTAINER_FLAGS** ([PidTagContainerFlags](pidtagcontainerflags-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="1cf14-133">Чтение и запись</span><span class="sxs-lookup"><span data-stu-id="1cf14-133">Read/write</span></span>  <br/> |
|<span data-ttu-id="1cf14-134">**PR_DISPLAY_NAME** ([PidTagDisplayName)](pidtagdisplayname-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="1cf14-134">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="1cf14-135">Чтение и запись</span><span class="sxs-lookup"><span data-stu-id="1cf14-135">Read/write</span></span>  <br/> |
|<span data-ttu-id="1cf14-136">**PR_ENTRYID** ([PidTagEntryId)](pidtagentryid-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="1cf14-136">**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="1cf14-137">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="1cf14-137">Read-only</span></span>  <br/> |
|<span data-ttu-id="1cf14-138">**PR_OBJECT_TYPE** ([PidTagObjectType)](pidtagobjecttype-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="1cf14-138">**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="1cf14-139">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="1cf14-139">Read-only</span></span>  <br/> |
|<span data-ttu-id="1cf14-140">**PR_RECORD_KEY** ([PidTagRecordKey)](pidtagrecordkey-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="1cf14-140">**PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="1cf14-141">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="1cf14-141">Read-only</span></span>  <br/> |
   
|<span data-ttu-id="1cf14-142">**Необязательные свойства**</span><span class="sxs-lookup"><span data-stu-id="1cf14-142">**Optional properties**</span></span>|<span data-ttu-id="1cf14-143">**Access**</span><span class="sxs-lookup"><span data-stu-id="1cf14-143">**Access**</span></span>|
|:-----|:-----|
|<span data-ttu-id="1cf14-144">**PR_CONTAINER_CONTENTS** ([PidTagContainerContents)](pidtagcontainercontents-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="1cf14-144">**PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="1cf14-145">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="1cf14-145">Read-only</span></span>  <br/> |
|<span data-ttu-id="1cf14-146">**PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy)](pidtagcontainerhierarchy-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="1cf14-146">**PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="1cf14-147">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="1cf14-147">Read-only</span></span>  <br/> |
|<span data-ttu-id="1cf14-148">**PR_DEF_CREATE_DL** ([PidTagDefCreateDl](pidtagdefcreatedl-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="1cf14-148">**PR_DEF_CREATE_DL** ([PidTagDefCreateDl](pidtagdefcreatedl-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="1cf14-149">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="1cf14-149">Read-only</span></span>  <br/> |
|<span data-ttu-id="1cf14-150">**PR_DEF_CREATE_MAILUSER** ([PidTagDefCreateMailuser)](pidtagdefcreatemailuser-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="1cf14-150">**PR_DEF_CREATE_MAILUSER** ([PidTagDefCreateMailuser](pidtagdefcreatemailuser-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="1cf14-151">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="1cf14-151">Read-only</span></span>  <br/> |
|<span data-ttu-id="1cf14-152">**PR_DISPLAY_TYPE** ([PidTagDisplayType)](pidtagdisplaytype-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="1cf14-152">**PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="1cf14-153">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="1cf14-153">Read-only</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="1cf14-154">Примечания</span><span class="sxs-lookup"><span data-stu-id="1cf14-154">Remarks</span></span>

<span data-ttu-id="1cf14-155">Интерфейс **IABContainer** косвенно наследуется от интерфейса [IUnknown](https://msdn.microsoft.com/library/ms680509%28VS.85%29.aspx) через [интерфейс IMAPIContainer : IMAPIProp](imapicontainerimapiprop.md) и [IMAPIProp : интерфейсы IUnknown.](imapipropiunknown.md)</span><span class="sxs-lookup"><span data-stu-id="1cf14-155">The **IABContainer** interface inherits indirectly from the [IUnknown](https://msdn.microsoft.com/library/ms680509%28VS.85%29.aspx) interface through the [IMAPIContainer : IMAPIProp](imapicontainerimapiprop.md) and [IMAPIProp : IUnknown](imapipropiunknown.md) interfaces.</span></span> <span data-ttu-id="1cf14-156">Поставщики адресных книг реализуют **интерфейс IABContainer.**</span><span class="sxs-lookup"><span data-stu-id="1cf14-156">Address book providers implement the **IABContainer** interface.</span></span> 
  
<span data-ttu-id="1cf14-157">В контейнере адресной книги может существовать любое количество объектов пользователей системы обмена сообщениями, списков рассылки и других контейнеров адресной книги.</span><span class="sxs-lookup"><span data-stu-id="1cf14-157">Any number of messaging user objects, distribution lists, and other address book containers can exist in an address book container.</span></span> <span data-ttu-id="1cf14-158">Как и в случае с любым контейнером, клиенты или поставщики услуг могут использовать контейнер адресной книги для открытия одной из записей или для извлечения таблицы иерархии или таблицы содержимого.</span><span class="sxs-lookup"><span data-stu-id="1cf14-158">As with any container, clients or service providers can use an address book container to open one of its entries or to retrieve a hierarchy table or contents table.</span></span> <span data-ttu-id="1cf14-159">Контейнеры адресной книги также обеспечивают разрешение имен и, в зависимости от поставщика, возможность добавления, удаления или изменения записей.</span><span class="sxs-lookup"><span data-stu-id="1cf14-159">Address book containers also provide name resolution and, depending on the provider, the ability to add, remove, or modify entries.</span></span>
  
<span data-ttu-id="1cf14-160">MAPI определяет специальный контейнер адресной книги под названием "личная адресная книга", который содержит записи, скопированные из других контейнеров.</span><span class="sxs-lookup"><span data-stu-id="1cf14-160">MAPI defines a special address book container called the personal address book (PAB) that holds entries copied from other containers.</span></span> <span data-ttu-id="1cf14-161">PAB всегда можно модификабельно.</span><span class="sxs-lookup"><span data-stu-id="1cf14-161">A PAB is always modifiable.</span></span> <span data-ttu-id="1cf14-162">Пользователи обычно заполняют свою PAB записями, указывающими получателей, с которыми они чаще всего общаются.</span><span class="sxs-lookup"><span data-stu-id="1cf14-162">Users typically populate their PAB with entries designating the recipients with which they most frequently communicate.</span></span> <span data-ttu-id="1cf14-163">В PAB также могут быть разротные адреса, а новые получатели еще не являются частью контейнера адресной книги.</span><span class="sxs-lookup"><span data-stu-id="1cf14-163">A PAB can also hold one-off addresses and new recipients not yet a part of any address book container.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="1cf14-164">См. также</span><span class="sxs-lookup"><span data-stu-id="1cf14-164">See also</span></span>

- [<span data-ttu-id="1cf14-165">Интерфейсы MAPI</span><span class="sxs-lookup"><span data-stu-id="1cf14-165">MAPI Interfaces</span></span>](mapi-interfaces.md)

