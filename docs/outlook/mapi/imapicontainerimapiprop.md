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
ms.openlocfilehash: e24f5ebd73a4652876282099f1460762c150b94d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19808832"
---
# <a name="imapicontainer--imapiprop"></a><span data-ttu-id="3a867-103">IMAPIContainer : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="3a867-103">IMAPIContainer : IMAPIProp</span></span>

  
  
<span data-ttu-id="3a867-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="3a867-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="3a867-105">Управляет высокого уровня операций в контейнере объекты, такие как адресных книг, списков рассылки и папок.</span><span class="sxs-lookup"><span data-stu-id="3a867-105">Manages high-level operations on container objects such as address books, distribution lists, and folders.</span></span> <span data-ttu-id="3a867-106">[IMAPIFolder: IMAPIContainer](imapifolderimapicontainer.md), [IABContainer: IMAPIContainer](iabcontainerimapicontainer.md), и [IDistList: IMAPIContainer](idistlistimapicontainer.md) интерфейсы являются производными от **IMAPIContainer**.</span><span class="sxs-lookup"><span data-stu-id="3a867-106">The [IMAPIFolder : IMAPIContainer](imapifolderimapicontainer.md), [IABContainer : IMAPIContainer](iabcontainerimapicontainer.md), and [IDistList : IMAPIContainer](idistlistimapicontainer.md) interfaces are derived from **IMAPIContainer**.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="3a867-107">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="3a867-107">Header file:</span></span>  <br/> |<span data-ttu-id="3a867-108">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="3a867-108">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="3a867-109">Предоставляемые:</span><span class="sxs-lookup"><span data-stu-id="3a867-109">Exposed by:</span></span>  <br/> |<span data-ttu-id="3a867-110">Папка, контейнер адресной книги и объекты списка рассылки</span><span class="sxs-lookup"><span data-stu-id="3a867-110">Folder, address book container, and distribution list objects</span></span>  <br/> |
|<span data-ttu-id="3a867-111">Реализованный:</span><span class="sxs-lookup"><span data-stu-id="3a867-111">Implemented by:</span></span>  <br/> |<span data-ttu-id="3a867-112">Хранение сообщений, адресной книги и поставщиков удаленных транспорта</span><span class="sxs-lookup"><span data-stu-id="3a867-112">Message store, address book, and remote transport providers</span></span>  <br/> |
|<span data-ttu-id="3a867-113">Вызывается:</span><span class="sxs-lookup"><span data-stu-id="3a867-113">Called by:</span></span>  <br/> |<span data-ttu-id="3a867-114">Клиентские приложения</span><span class="sxs-lookup"><span data-stu-id="3a867-114">Client applications</span></span>  <br/> |
|<span data-ttu-id="3a867-115">Идентификатор интерфейса:</span><span class="sxs-lookup"><span data-stu-id="3a867-115">Interface identifier:</span></span>  <br/> |<span data-ttu-id="3a867-116">IID_IMAPIContainer</span><span class="sxs-lookup"><span data-stu-id="3a867-116">IID_IMAPIContainer</span></span>  <br/> |
|<span data-ttu-id="3a867-117">Тип указателя:</span><span class="sxs-lookup"><span data-stu-id="3a867-117">Pointer type:</span></span>  <br/> |<span data-ttu-id="3a867-118">LPMAPICONTAINER</span><span class="sxs-lookup"><span data-stu-id="3a867-118">LPMAPICONTAINER</span></span>  <br/> |
|<span data-ttu-id="3a867-119">Модель транзакций:</span><span class="sxs-lookup"><span data-stu-id="3a867-119">Transaction model:</span></span>  <br/> |<span data-ttu-id="3a867-120">Абстрактный класс, никогда не реализовано</span><span class="sxs-lookup"><span data-stu-id="3a867-120">Abstract class, never implemented</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="3a867-121">Порядке vtable</span><span class="sxs-lookup"><span data-stu-id="3a867-121">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="3a867-122">GetContentsTable</span><span class="sxs-lookup"><span data-stu-id="3a867-122">GetContentsTable</span></span>](imapicontainer-getcontentstable.md) <br/> |<span data-ttu-id="3a867-123">Возвращает указатель на таблицу содержимого контейнера.</span><span class="sxs-lookup"><span data-stu-id="3a867-123">Returns a pointer to the container's contents table.</span></span>  <br/> |
|[<span data-ttu-id="3a867-124">GetHierarchyTable</span><span class="sxs-lookup"><span data-stu-id="3a867-124">GetHierarchyTable</span></span>](imapicontainer-gethierarchytable.md) <br/> |<span data-ttu-id="3a867-125">Возвращает указатель на таблицу иерархии контейнера.</span><span class="sxs-lookup"><span data-stu-id="3a867-125">Returns a pointer to the container's hierarchy table.</span></span>  <br/> |
|[<span data-ttu-id="3a867-126">OpenEntry</span><span class="sxs-lookup"><span data-stu-id="3a867-126">OpenEntry</span></span>](imapicontainer-openentry.md) <br/> |<span data-ttu-id="3a867-127">Открывает объект в контейнере, возвращает указатель интерфейса для дальнейшей доступа.</span><span class="sxs-lookup"><span data-stu-id="3a867-127">Opens an object in the container, returning an interface pointer for further access.</span></span>  <br/> |
|[<span data-ttu-id="3a867-128">SetSearchCriteria</span><span class="sxs-lookup"><span data-stu-id="3a867-128">SetSearchCriteria</span></span>](imapicontainer-setsearchcriteria.md) <br/> |<span data-ttu-id="3a867-129">Устанавливает условия поиска для контейнера.</span><span class="sxs-lookup"><span data-stu-id="3a867-129">Establishes search criteria for the container.</span></span>  <br/> |
|[<span data-ttu-id="3a867-130">GetSearchCriteria</span><span class="sxs-lookup"><span data-stu-id="3a867-130">GetSearchCriteria</span></span>](imapicontainer-getsearchcriteria.md) <br/> |<span data-ttu-id="3a867-131">Получает параметры поиска для контейнера.</span><span class="sxs-lookup"><span data-stu-id="3a867-131">Obtains the search criteria for the container.</span></span>  <br/> |
   
|<span data-ttu-id="3a867-132">**Обязательные свойства**</span><span class="sxs-lookup"><span data-stu-id="3a867-132">**Required properties**</span></span>|<span data-ttu-id="3a867-133">**Access**</span><span class="sxs-lookup"><span data-stu-id="3a867-133">**Access**</span></span>|
|:-----|:-----|
|<span data-ttu-id="3a867-134">**PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="3a867-134">**PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="3a867-135">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="3a867-135">Read-only</span></span>  <br/> |
|<span data-ttu-id="3a867-136">**PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="3a867-136">**PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="3a867-137">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="3a867-137">Read-only</span></span>  <br/> |
|<span data-ttu-id="3a867-138">**PR_CONTAINER_FLAGS** ([PidTagContainerFlags](pidtagcontainerflags-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="3a867-138">**PR_CONTAINER_FLAGS** ([PidTagContainerFlags](pidtagcontainerflags-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="3a867-139">Чтение и запись</span><span class="sxs-lookup"><span data-stu-id="3a867-139">Read/write</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="3a867-140">См. также</span><span class="sxs-lookup"><span data-stu-id="3a867-140">See also</span></span>



[<span data-ttu-id="3a867-141">Интерфейсы MAPI</span><span class="sxs-lookup"><span data-stu-id="3a867-141">MAPI Interfaces</span></span>](mapi-interfaces.md)

