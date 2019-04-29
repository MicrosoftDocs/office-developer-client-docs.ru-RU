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
# <a name="imapicontainer--imapiprop"></a><span data-ttu-id="42d9e-103">IMAPIContainer : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="42d9e-103">IMAPIContainer : IMAPIProp</span></span>

  
  
<span data-ttu-id="42d9e-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="42d9e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="42d9e-105">Управляет операциями высокого уровня для объектов контейнеров, таких как адресные книги, списки рассылки и папки.</span><span class="sxs-lookup"><span data-stu-id="42d9e-105">Manages high-level operations on container objects such as address books, distribution lists, and folders.</span></span> <span data-ttu-id="42d9e-106">Интерфейсы [IMAPIFolder: IMAPIContainer](imapifolderimapicontainer.md), [иабконтаинер: IMAPIContainer](iabcontainerimapicontainer.md)и [идистлист: IMAPIContainer](idistlistimapicontainer.md) являются производными от **IMAPIContainer**.</span><span class="sxs-lookup"><span data-stu-id="42d9e-106">The [IMAPIFolder : IMAPIContainer](imapifolderimapicontainer.md), [IABContainer : IMAPIContainer](iabcontainerimapicontainer.md), and [IDistList : IMAPIContainer](idistlistimapicontainer.md) interfaces are derived from **IMAPIContainer**.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="42d9e-107">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="42d9e-107">Header file:</span></span>  <br/> |<span data-ttu-id="42d9e-108">MAPIDEFS. h</span><span class="sxs-lookup"><span data-stu-id="42d9e-108">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="42d9e-109">Предоставлено:</span><span class="sxs-lookup"><span data-stu-id="42d9e-109">Exposed by:</span></span>  <br/> |<span data-ttu-id="42d9e-110">Папка, контейнер адресной книги и объекты списка рассылки</span><span class="sxs-lookup"><span data-stu-id="42d9e-110">Folder, address book container, and distribution list objects</span></span>  <br/> |
|<span data-ttu-id="42d9e-111">Реализовано в:</span><span class="sxs-lookup"><span data-stu-id="42d9e-111">Implemented by:</span></span>  <br/> |<span data-ttu-id="42d9e-112">Хранилище сообщений, адресные книги и удаленные поставщики транспорта</span><span class="sxs-lookup"><span data-stu-id="42d9e-112">Message store, address book, and remote transport providers</span></span>  <br/> |
|<span data-ttu-id="42d9e-113">Вызывающая сторона:</span><span class="sxs-lookup"><span data-stu-id="42d9e-113">Called by:</span></span>  <br/> |<span data-ttu-id="42d9e-114">Клиентские приложения</span><span class="sxs-lookup"><span data-stu-id="42d9e-114">Client applications</span></span>  <br/> |
|<span data-ttu-id="42d9e-115">Идентификатор интерфейса:</span><span class="sxs-lookup"><span data-stu-id="42d9e-115">Interface identifier:</span></span>  <br/> |<span data-ttu-id="42d9e-116">Иид_имапиконтаинер</span><span class="sxs-lookup"><span data-stu-id="42d9e-116">IID_IMAPIContainer</span></span>  <br/> |
|<span data-ttu-id="42d9e-117">Тип указателя:</span><span class="sxs-lookup"><span data-stu-id="42d9e-117">Pointer type:</span></span>  <br/> |<span data-ttu-id="42d9e-118">ЛПМАПИКОНТАИНЕР</span><span class="sxs-lookup"><span data-stu-id="42d9e-118">LPMAPICONTAINER</span></span>  <br/> |
|<span data-ttu-id="42d9e-119">Модель транзакции:</span><span class="sxs-lookup"><span data-stu-id="42d9e-119">Transaction model:</span></span>  <br/> |<span data-ttu-id="42d9e-120">Абстрактный класс, никогда не реализован</span><span class="sxs-lookup"><span data-stu-id="42d9e-120">Abstract class, never implemented</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="42d9e-121">Заказ vtable</span><span class="sxs-lookup"><span data-stu-id="42d9e-121">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="42d9e-122">Жетконтентстабле</span><span class="sxs-lookup"><span data-stu-id="42d9e-122">GetContentsTable</span></span>](imapicontainer-getcontentstable.md) <br/> |<span data-ttu-id="42d9e-123">Возвращает указатель на таблицу содержимого контейнера.</span><span class="sxs-lookup"><span data-stu-id="42d9e-123">Returns a pointer to the container's contents table.</span></span>  <br/> |
|[<span data-ttu-id="42d9e-124">Жесиерарчитабле</span><span class="sxs-lookup"><span data-stu-id="42d9e-124">GetHierarchyTable</span></span>](imapicontainer-gethierarchytable.md) <br/> |<span data-ttu-id="42d9e-125">Возвращает указатель на таблицу иерархии контейнера.</span><span class="sxs-lookup"><span data-stu-id="42d9e-125">Returns a pointer to the container's hierarchy table.</span></span>  <br/> |
|[<span data-ttu-id="42d9e-126">OpenEntry</span><span class="sxs-lookup"><span data-stu-id="42d9e-126">OpenEntry</span></span>](imapicontainer-openentry.md) <br/> |<span data-ttu-id="42d9e-127">Открывает объект в контейнере, возвращая указатель интерфейса для дальнейшего доступа.</span><span class="sxs-lookup"><span data-stu-id="42d9e-127">Opens an object in the container, returning an interface pointer for further access.</span></span>  <br/> |
|[<span data-ttu-id="42d9e-128">Сетсеарчкритериа</span><span class="sxs-lookup"><span data-stu-id="42d9e-128">SetSearchCriteria</span></span>](imapicontainer-setsearchcriteria.md) <br/> |<span data-ttu-id="42d9e-129">Устанавливает критерии поиска для контейнера.</span><span class="sxs-lookup"><span data-stu-id="42d9e-129">Establishes search criteria for the container.</span></span>  <br/> |
|[<span data-ttu-id="42d9e-130">Жетсеарчкритериа</span><span class="sxs-lookup"><span data-stu-id="42d9e-130">GetSearchCriteria</span></span>](imapicontainer-getsearchcriteria.md) <br/> |<span data-ttu-id="42d9e-131">Получает условия поиска для контейнера.</span><span class="sxs-lookup"><span data-stu-id="42d9e-131">Obtains the search criteria for the container.</span></span>  <br/> |
   
|<span data-ttu-id="42d9e-132">**Обязательные свойства**</span><span class="sxs-lookup"><span data-stu-id="42d9e-132">**Required properties**</span></span>|<span data-ttu-id="42d9e-133">**Access**</span><span class="sxs-lookup"><span data-stu-id="42d9e-133">**Access**</span></span>|
|:-----|:-----|
|<span data-ttu-id="42d9e-134">**Пр_контаинер_хиерарчи** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="42d9e-134">**PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="42d9e-135">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="42d9e-135">Read-only</span></span>  <br/> |
|<span data-ttu-id="42d9e-136">**Пр_контаинер_контентс** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="42d9e-136">**PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="42d9e-137">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="42d9e-137">Read-only</span></span>  <br/> |
|<span data-ttu-id="42d9e-138">**Пр_контаинер_флагс** ([PidTagContainerFlags](pidtagcontainerflags-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="42d9e-138">**PR_CONTAINER_FLAGS** ([PidTagContainerFlags](pidtagcontainerflags-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="42d9e-139">Чтение и запись</span><span class="sxs-lookup"><span data-stu-id="42d9e-139">Read/write</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="42d9e-140">См. также</span><span class="sxs-lookup"><span data-stu-id="42d9e-140">See also</span></span>



[<span data-ttu-id="42d9e-141">Интерфейсы MAPI</span><span class="sxs-lookup"><span data-stu-id="42d9e-141">MAPI Interfaces</span></span>](mapi-interfaces.md)

