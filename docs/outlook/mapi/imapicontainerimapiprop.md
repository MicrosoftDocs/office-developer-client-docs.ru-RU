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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32286722"
---
# <a name="imapicontainer--imapiprop"></a><span data-ttu-id="8398d-103">IMAPIContainer : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="8398d-103">IMAPIContainer : IMAPIProp</span></span>

  
  
<span data-ttu-id="8398d-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8398d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8398d-105">Управляет операциями высокого уровня для объектов контейнеров, таких как адресные книги, списки рассылки и папки.</span><span class="sxs-lookup"><span data-stu-id="8398d-105">Manages high-level operations on container objects such as address books, distribution lists, and folders.</span></span> <span data-ttu-id="8398d-106">Интерфейсы [IMAPIFolder: IMAPIContainer](imapifolderimapicontainer.md), [иабконтаинер: IMAPIContainer](iabcontainerimapicontainer.md)и [идистлист: IMAPIContainer](idistlistimapicontainer.md) являются производными от **IMAPIContainer**.</span><span class="sxs-lookup"><span data-stu-id="8398d-106">The [IMAPIFolder : IMAPIContainer](imapifolderimapicontainer.md), [IABContainer : IMAPIContainer](iabcontainerimapicontainer.md), and [IDistList : IMAPIContainer](idistlistimapicontainer.md) interfaces are derived from **IMAPIContainer**.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="8398d-107">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="8398d-107">Header file:</span></span>  <br/> |<span data-ttu-id="8398d-108">MAPIDEFS. h</span><span class="sxs-lookup"><span data-stu-id="8398d-108">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="8398d-109">Предоставлено:</span><span class="sxs-lookup"><span data-stu-id="8398d-109">Exposed by:</span></span>  <br/> |<span data-ttu-id="8398d-110">Папка, контейнер адресной книги и объекты списка рассылки</span><span class="sxs-lookup"><span data-stu-id="8398d-110">Folder, address book container, and distribution list objects</span></span>  <br/> |
|<span data-ttu-id="8398d-111">Реализовано в:</span><span class="sxs-lookup"><span data-stu-id="8398d-111">Implemented by:</span></span>  <br/> |<span data-ttu-id="8398d-112">Хранилище сообщений, адресные книги и удаленные поставщики транспорта</span><span class="sxs-lookup"><span data-stu-id="8398d-112">Message store, address book, and remote transport providers</span></span>  <br/> |
|<span data-ttu-id="8398d-113">Вызывающая сторона:</span><span class="sxs-lookup"><span data-stu-id="8398d-113">Called by:</span></span>  <br/> |<span data-ttu-id="8398d-114">Клиентские приложения</span><span class="sxs-lookup"><span data-stu-id="8398d-114">Client applications</span></span>  <br/> |
|<span data-ttu-id="8398d-115">Идентификатор интерфейса:</span><span class="sxs-lookup"><span data-stu-id="8398d-115">Interface identifier:</span></span>  <br/> |<span data-ttu-id="8398d-116">Иид_имапиконтаинер</span><span class="sxs-lookup"><span data-stu-id="8398d-116">IID_IMAPIContainer</span></span>  <br/> |
|<span data-ttu-id="8398d-117">Тип указателя:</span><span class="sxs-lookup"><span data-stu-id="8398d-117">Pointer type:</span></span>  <br/> |<span data-ttu-id="8398d-118">ЛПМАПИКОНТАИНЕР</span><span class="sxs-lookup"><span data-stu-id="8398d-118">LPMAPICONTAINER</span></span>  <br/> |
|<span data-ttu-id="8398d-119">Модель транзакции:</span><span class="sxs-lookup"><span data-stu-id="8398d-119">Transaction model:</span></span>  <br/> |<span data-ttu-id="8398d-120">Абстрактный класс, никогда не реализован</span><span class="sxs-lookup"><span data-stu-id="8398d-120">Abstract class, never implemented</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="8398d-121">Заказ vtable</span><span class="sxs-lookup"><span data-stu-id="8398d-121">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="8398d-122">Жетконтентстабле</span><span class="sxs-lookup"><span data-stu-id="8398d-122">GetContentsTable</span></span>](imapicontainer-getcontentstable.md) <br/> |<span data-ttu-id="8398d-123">Возвращает указатель на таблицу содержимого контейнера.</span><span class="sxs-lookup"><span data-stu-id="8398d-123">Returns a pointer to the container's contents table.</span></span>  <br/> |
|[<span data-ttu-id="8398d-124">Жесиерарчитабле</span><span class="sxs-lookup"><span data-stu-id="8398d-124">GetHierarchyTable</span></span>](imapicontainer-gethierarchytable.md) <br/> |<span data-ttu-id="8398d-125">Возвращает указатель на таблицу иерархии контейнера.</span><span class="sxs-lookup"><span data-stu-id="8398d-125">Returns a pointer to the container's hierarchy table.</span></span>  <br/> |
|[<span data-ttu-id="8398d-126">OpenEntry</span><span class="sxs-lookup"><span data-stu-id="8398d-126">OpenEntry</span></span>](imapicontainer-openentry.md) <br/> |<span data-ttu-id="8398d-127">Открывает объект в контейнере, возвращая указатель интерфейса для дальнейшего доступа.</span><span class="sxs-lookup"><span data-stu-id="8398d-127">Opens an object in the container, returning an interface pointer for further access.</span></span>  <br/> |
|[<span data-ttu-id="8398d-128">Сетсеарчкритериа</span><span class="sxs-lookup"><span data-stu-id="8398d-128">SetSearchCriteria</span></span>](imapicontainer-setsearchcriteria.md) <br/> |<span data-ttu-id="8398d-129">Устанавливает критерии поиска для контейнера.</span><span class="sxs-lookup"><span data-stu-id="8398d-129">Establishes search criteria for the container.</span></span>  <br/> |
|[<span data-ttu-id="8398d-130">Жетсеарчкритериа</span><span class="sxs-lookup"><span data-stu-id="8398d-130">GetSearchCriteria</span></span>](imapicontainer-getsearchcriteria.md) <br/> |<span data-ttu-id="8398d-131">Получает условия поиска для контейнера.</span><span class="sxs-lookup"><span data-stu-id="8398d-131">Obtains the search criteria for the container.</span></span>  <br/> |
   
|<span data-ttu-id="8398d-132">**Обязательные свойства**</span><span class="sxs-lookup"><span data-stu-id="8398d-132">**Required properties**</span></span>|<span data-ttu-id="8398d-133">**Access**</span><span class="sxs-lookup"><span data-stu-id="8398d-133">**Access**</span></span>|
|:-----|:-----|
|<span data-ttu-id="8398d-134">**Пр_контаинер_хиерарчи** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="8398d-134">**PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="8398d-135">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="8398d-135">Read-only</span></span>  <br/> |
|<span data-ttu-id="8398d-136">**Пр_контаинер_контентс** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="8398d-136">**PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="8398d-137">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="8398d-137">Read-only</span></span>  <br/> |
|<span data-ttu-id="8398d-138">**Пр_контаинер_флагс** ([PidTagContainerFlags](pidtagcontainerflags-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="8398d-138">**PR_CONTAINER_FLAGS** ([PidTagContainerFlags](pidtagcontainerflags-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="8398d-139">Чтение и запись</span><span class="sxs-lookup"><span data-stu-id="8398d-139">Read/write</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="8398d-140">См. также</span><span class="sxs-lookup"><span data-stu-id="8398d-140">See also</span></span>



[<span data-ttu-id="8398d-141">Интерфейсы MAPI</span><span class="sxs-lookup"><span data-stu-id="8398d-141">MAPI Interfaces</span></span>](mapi-interfaces.md)

