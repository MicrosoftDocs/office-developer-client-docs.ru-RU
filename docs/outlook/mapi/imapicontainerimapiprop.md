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
ms.openlocfilehash: 38094895fed03884b138b02d4aa1ed87bcc6ea9c
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22575702"
---
# <a name="imapicontainer--imapiprop"></a><span data-ttu-id="a1dc3-103">IMAPIContainer : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="a1dc3-103">IMAPIContainer : IMAPIProp</span></span>

  
  
<span data-ttu-id="a1dc3-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a1dc3-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a1dc3-105">Управляет высокого уровня операций в контейнере объекты, такие как адресных книг, списков рассылки и папок.</span><span class="sxs-lookup"><span data-stu-id="a1dc3-105">Manages high-level operations on container objects such as address books, distribution lists, and folders.</span></span> <span data-ttu-id="a1dc3-106">[IMAPIFolder: IMAPIContainer](imapifolderimapicontainer.md), [IABContainer: IMAPIContainer](iabcontainerimapicontainer.md), и [IDistList: IMAPIContainer](idistlistimapicontainer.md) интерфейсы являются производными от **IMAPIContainer**.</span><span class="sxs-lookup"><span data-stu-id="a1dc3-106">The [IMAPIFolder : IMAPIContainer](imapifolderimapicontainer.md), [IABContainer : IMAPIContainer](iabcontainerimapicontainer.md), and [IDistList : IMAPIContainer](idistlistimapicontainer.md) interfaces are derived from **IMAPIContainer**.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="a1dc3-107">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="a1dc3-107">Header file:</span></span>  <br/> |<span data-ttu-id="a1dc3-108">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="a1dc3-108">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="a1dc3-109">Предоставляемые:</span><span class="sxs-lookup"><span data-stu-id="a1dc3-109">Exposed by:</span></span>  <br/> |<span data-ttu-id="a1dc3-110">Папка, контейнер адресной книги и объекты списка рассылки</span><span class="sxs-lookup"><span data-stu-id="a1dc3-110">Folder, address book container, and distribution list objects</span></span>  <br/> |
|<span data-ttu-id="a1dc3-111">Реализованный:</span><span class="sxs-lookup"><span data-stu-id="a1dc3-111">Implemented by:</span></span>  <br/> |<span data-ttu-id="a1dc3-112">Хранение сообщений, адресной книги и поставщиков удаленных транспорта</span><span class="sxs-lookup"><span data-stu-id="a1dc3-112">Message store, address book, and remote transport providers</span></span>  <br/> |
|<span data-ttu-id="a1dc3-113">Вызывается:</span><span class="sxs-lookup"><span data-stu-id="a1dc3-113">Called by:</span></span>  <br/> |<span data-ttu-id="a1dc3-114">Клиентские приложения</span><span class="sxs-lookup"><span data-stu-id="a1dc3-114">Client applications</span></span>  <br/> |
|<span data-ttu-id="a1dc3-115">Идентификатор интерфейса:</span><span class="sxs-lookup"><span data-stu-id="a1dc3-115">Interface identifier:</span></span>  <br/> |<span data-ttu-id="a1dc3-116">IID_IMAPIContainer</span><span class="sxs-lookup"><span data-stu-id="a1dc3-116">IID_IMAPIContainer</span></span>  <br/> |
|<span data-ttu-id="a1dc3-117">Тип указателя:</span><span class="sxs-lookup"><span data-stu-id="a1dc3-117">Pointer type:</span></span>  <br/> |<span data-ttu-id="a1dc3-118">LPMAPICONTAINER</span><span class="sxs-lookup"><span data-stu-id="a1dc3-118">LPMAPICONTAINER</span></span>  <br/> |
|<span data-ttu-id="a1dc3-119">Модель транзакций:</span><span class="sxs-lookup"><span data-stu-id="a1dc3-119">Transaction model:</span></span>  <br/> |<span data-ttu-id="a1dc3-120">Абстрактный класс, никогда не реализовано</span><span class="sxs-lookup"><span data-stu-id="a1dc3-120">Abstract class, never implemented</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="a1dc3-121">Порядке vtable</span><span class="sxs-lookup"><span data-stu-id="a1dc3-121">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="a1dc3-122">GetContentsTable</span><span class="sxs-lookup"><span data-stu-id="a1dc3-122">GetContentsTable</span></span>](imapicontainer-getcontentstable.md) <br/> |<span data-ttu-id="a1dc3-123">Возвращает указатель на таблицу содержимого контейнера.</span><span class="sxs-lookup"><span data-stu-id="a1dc3-123">Returns a pointer to the container's contents table.</span></span>  <br/> |
|[<span data-ttu-id="a1dc3-124">GetHierarchyTable</span><span class="sxs-lookup"><span data-stu-id="a1dc3-124">GetHierarchyTable</span></span>](imapicontainer-gethierarchytable.md) <br/> |<span data-ttu-id="a1dc3-125">Возвращает указатель на таблицу иерархии контейнера.</span><span class="sxs-lookup"><span data-stu-id="a1dc3-125">Returns a pointer to the container's hierarchy table.</span></span>  <br/> |
|[<span data-ttu-id="a1dc3-126">OpenEntry</span><span class="sxs-lookup"><span data-stu-id="a1dc3-126">OpenEntry</span></span>](imapicontainer-openentry.md) <br/> |<span data-ttu-id="a1dc3-127">Открывает объект в контейнере, возвращает указатель интерфейса для дальнейшей доступа.</span><span class="sxs-lookup"><span data-stu-id="a1dc3-127">Opens an object in the container, returning an interface pointer for further access.</span></span>  <br/> |
|[<span data-ttu-id="a1dc3-128">SetSearchCriteria</span><span class="sxs-lookup"><span data-stu-id="a1dc3-128">SetSearchCriteria</span></span>](imapicontainer-setsearchcriteria.md) <br/> |<span data-ttu-id="a1dc3-129">Устанавливает условия поиска для контейнера.</span><span class="sxs-lookup"><span data-stu-id="a1dc3-129">Establishes search criteria for the container.</span></span>  <br/> |
|[<span data-ttu-id="a1dc3-130">GetSearchCriteria</span><span class="sxs-lookup"><span data-stu-id="a1dc3-130">GetSearchCriteria</span></span>](imapicontainer-getsearchcriteria.md) <br/> |<span data-ttu-id="a1dc3-131">Получает параметры поиска для контейнера.</span><span class="sxs-lookup"><span data-stu-id="a1dc3-131">Obtains the search criteria for the container.</span></span>  <br/> |
   
|<span data-ttu-id="a1dc3-132">**Обязательные свойства**</span><span class="sxs-lookup"><span data-stu-id="a1dc3-132">**Required properties**</span></span>|<span data-ttu-id="a1dc3-133">**Access**</span><span class="sxs-lookup"><span data-stu-id="a1dc3-133">**Access**</span></span>|
|:-----|:-----|
|<span data-ttu-id="a1dc3-134">**PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="a1dc3-134">**PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="a1dc3-135">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="a1dc3-135">Read-only</span></span>  <br/> |
|<span data-ttu-id="a1dc3-136">**PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="a1dc3-136">**PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="a1dc3-137">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="a1dc3-137">Read-only</span></span>  <br/> |
|<span data-ttu-id="a1dc3-138">**PR_CONTAINER_FLAGS** ([PidTagContainerFlags](pidtagcontainerflags-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="a1dc3-138">**PR_CONTAINER_FLAGS** ([PidTagContainerFlags](pidtagcontainerflags-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="a1dc3-139">Чтение и запись</span><span class="sxs-lookup"><span data-stu-id="a1dc3-139">Read/write</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="a1dc3-140">См. также</span><span class="sxs-lookup"><span data-stu-id="a1dc3-140">See also</span></span>



[<span data-ttu-id="a1dc3-141">Интерфейсы MAPI</span><span class="sxs-lookup"><span data-stu-id="a1dc3-141">MAPI Interfaces</span></span>](mapi-interfaces.md)

