---
title: IMAPIContainer IMAPIProp
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIContainer
api_type:
- COM
ms.assetid: d83fdd83-3e86-43c8-a73f-8e9e01b53371
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 8be3b1857d539f81e42d2ac3e5813afa73513a16
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33406124"
---
# <a name="imapicontainer--imapiprop"></a><span data-ttu-id="f1d0a-103">IMAPIContainer : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="f1d0a-103">IMAPIContainer : IMAPIProp</span></span>

  
  
<span data-ttu-id="f1d0a-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f1d0a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f1d0a-105">Управление высокоуровневой операцией на контейнерных объектах, таких как адресные книги, списки рассылки и папки.</span><span class="sxs-lookup"><span data-stu-id="f1d0a-105">Manages high-level operations on container objects such as address books, distribution lists, and folders.</span></span> <span data-ttu-id="f1d0a-106">ИнтерфейсЫ [IMAPIFolder : IMAPIContainer,](imapifolderimapicontainer.md) [IABContainer : IMAPIContainer](iabcontainerimapicontainer.md)и [IDistList: интерфейсы IMAPIContainer](idistlistimapicontainer.md) получены из **интерфейсов IMAPIContainer**.</span><span class="sxs-lookup"><span data-stu-id="f1d0a-106">The [IMAPIFolder : IMAPIContainer](imapifolderimapicontainer.md), [IABContainer : IMAPIContainer](iabcontainerimapicontainer.md), and [IDistList : IMAPIContainer](idistlistimapicontainer.md) interfaces are derived from **IMAPIContainer**.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="f1d0a-107">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="f1d0a-107">Header file:</span></span>  <br/> |<span data-ttu-id="f1d0a-108">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="f1d0a-108">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="f1d0a-109">Подвергается:</span><span class="sxs-lookup"><span data-stu-id="f1d0a-109">Exposed by:</span></span>  <br/> |<span data-ttu-id="f1d0a-110">Папка, контейнер адресной книги и объекты списка рассылки</span><span class="sxs-lookup"><span data-stu-id="f1d0a-110">Folder, address book container, and distribution list objects</span></span>  <br/> |
|<span data-ttu-id="f1d0a-111">Реализовано в:</span><span class="sxs-lookup"><span data-stu-id="f1d0a-111">Implemented by:</span></span>  <br/> |<span data-ttu-id="f1d0a-112">Хранилище сообщений, адресная книга и поставщики удаленных транспортных средств</span><span class="sxs-lookup"><span data-stu-id="f1d0a-112">Message store, address book, and remote transport providers</span></span>  <br/> |
|<span data-ttu-id="f1d0a-113">Вызывающая сторона:</span><span class="sxs-lookup"><span data-stu-id="f1d0a-113">Called by:</span></span>  <br/> |<span data-ttu-id="f1d0a-114">Клиентские приложения</span><span class="sxs-lookup"><span data-stu-id="f1d0a-114">Client applications</span></span>  <br/> |
|<span data-ttu-id="f1d0a-115">Идентификатор интерфейса:</span><span class="sxs-lookup"><span data-stu-id="f1d0a-115">Interface identifier:</span></span>  <br/> |<span data-ttu-id="f1d0a-116">IID_IMAPIContainer</span><span class="sxs-lookup"><span data-stu-id="f1d0a-116">IID_IMAPIContainer</span></span>  <br/> |
|<span data-ttu-id="f1d0a-117">Тип указателя:</span><span class="sxs-lookup"><span data-stu-id="f1d0a-117">Pointer type:</span></span>  <br/> |<span data-ttu-id="f1d0a-118">LPMAPICONTAINER</span><span class="sxs-lookup"><span data-stu-id="f1d0a-118">LPMAPICONTAINER</span></span>  <br/> |
|<span data-ttu-id="f1d0a-119">Модель транзакции:</span><span class="sxs-lookup"><span data-stu-id="f1d0a-119">Transaction model:</span></span>  <br/> |<span data-ttu-id="f1d0a-120">Абстрактный класс, никогда не реализованный</span><span class="sxs-lookup"><span data-stu-id="f1d0a-120">Abstract class, never implemented</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="f1d0a-121">Заказ Vtable</span><span class="sxs-lookup"><span data-stu-id="f1d0a-121">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="f1d0a-122">GetContentsTable</span><span class="sxs-lookup"><span data-stu-id="f1d0a-122">GetContentsTable</span></span>](imapicontainer-getcontentstable.md) <br/> |<span data-ttu-id="f1d0a-123">Возвращает указатель в таблицу содержимого контейнера.</span><span class="sxs-lookup"><span data-stu-id="f1d0a-123">Returns a pointer to the container's contents table.</span></span>  <br/> |
|[<span data-ttu-id="f1d0a-124">GetHierarchyTable</span><span class="sxs-lookup"><span data-stu-id="f1d0a-124">GetHierarchyTable</span></span>](imapicontainer-gethierarchytable.md) <br/> |<span data-ttu-id="f1d0a-125">Возвращает указатель в таблицу иерархии контейнера.</span><span class="sxs-lookup"><span data-stu-id="f1d0a-125">Returns a pointer to the container's hierarchy table.</span></span>  <br/> |
|[<span data-ttu-id="f1d0a-126">OpenEntry</span><span class="sxs-lookup"><span data-stu-id="f1d0a-126">OpenEntry</span></span>](imapicontainer-openentry.md) <br/> |<span data-ttu-id="f1d0a-127">Открывает объект в контейнере, возвращая указатель интерфейса для дальнейшего доступа.</span><span class="sxs-lookup"><span data-stu-id="f1d0a-127">Opens an object in the container, returning an interface pointer for further access.</span></span>  <br/> |
|[<span data-ttu-id="f1d0a-128">SetSearchCriteria</span><span class="sxs-lookup"><span data-stu-id="f1d0a-128">SetSearchCriteria</span></span>](imapicontainer-setsearchcriteria.md) <br/> |<span data-ttu-id="f1d0a-129">Устанавливает критерии поиска для контейнера.</span><span class="sxs-lookup"><span data-stu-id="f1d0a-129">Establishes search criteria for the container.</span></span>  <br/> |
|[<span data-ttu-id="f1d0a-130">GetSearchCriteria</span><span class="sxs-lookup"><span data-stu-id="f1d0a-130">GetSearchCriteria</span></span>](imapicontainer-getsearchcriteria.md) <br/> |<span data-ttu-id="f1d0a-131">Получает критерии поиска для контейнера.</span><span class="sxs-lookup"><span data-stu-id="f1d0a-131">Obtains the search criteria for the container.</span></span>  <br/> |
   
|<span data-ttu-id="f1d0a-132">**Обязательные свойства**</span><span class="sxs-lookup"><span data-stu-id="f1d0a-132">**Required properties**</span></span>|<span data-ttu-id="f1d0a-133">**Access**</span><span class="sxs-lookup"><span data-stu-id="f1d0a-133">**Access**</span></span>|
|:-----|:-----|
|<span data-ttu-id="f1d0a-134">**PR_CONTAINER_HIERARCHY** [(PidTagContainerHierarchy)](pidtagcontainerhierarchy-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="f1d0a-134">**PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="f1d0a-135">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="f1d0a-135">Read-only</span></span>  <br/> |
|<span data-ttu-id="f1d0a-136">**PR_CONTAINER_CONTENTS** [(PidTagContainerContents)](pidtagcontainercontents-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="f1d0a-136">**PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="f1d0a-137">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="f1d0a-137">Read-only</span></span>  <br/> |
|<span data-ttu-id="f1d0a-138">**PR_CONTAINER_FLAGS** [(PidTagContainerFlags)](pidtagcontainerflags-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="f1d0a-138">**PR_CONTAINER_FLAGS** ([PidTagContainerFlags](pidtagcontainerflags-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="f1d0a-139">Чтение и запись</span><span class="sxs-lookup"><span data-stu-id="f1d0a-139">Read/write</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="f1d0a-140">См. также</span><span class="sxs-lookup"><span data-stu-id="f1d0a-140">See also</span></span>



[<span data-ttu-id="f1d0a-141">Интерфейсы MAPI</span><span class="sxs-lookup"><span data-stu-id="f1d0a-141">MAPI Interfaces</span></span>](mapi-interfaces.md)

