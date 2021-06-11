---
title: IOSTX IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IOSTX
api_type:
- COM
ms.assetid: f374d8d9-be8e-2489-d5fe-8a92e0ecfc6f
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 6d7de4d6c14179ddaba4e2ad907f1acc1c53b125
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33431997"
---
# <a name="iostx--iunknown"></a><span data-ttu-id="45972-103">IOSTX : IUnknown</span><span class="sxs-lookup"><span data-stu-id="45972-103">IOSTX : IUnknown</span></span>

  
  
<span data-ttu-id="45972-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="45972-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="45972-105">Предоставляет методы синхронизации.</span><span class="sxs-lookup"><span data-stu-id="45972-105">Provides synchronization methods.</span></span> <span data-ttu-id="45972-106">Этот интерфейс извлекает необходимые сведения для репликации локальных изменений на сервер и сервер изменений в локальном магазине.</span><span class="sxs-lookup"><span data-stu-id="45972-106">This interface retrieves the necessary information to replicate local changes to the server and server changes to the local store.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="45972-107">Предоставлено:</span><span class="sxs-lookup"><span data-stu-id="45972-107">Provided by:</span></span>  <br/> |[<span data-ttu-id="45972-108">IPSTX::GetSyncObject</span><span class="sxs-lookup"><span data-stu-id="45972-108">IPSTX::GetSyncObject</span></span>](iostx-setsyncresult.md) <br/> |
|<span data-ttu-id="45972-109">Идентификатор интерфейса:</span><span class="sxs-lookup"><span data-stu-id="45972-109">Interface identifier:</span></span>  <br/> |<span data-ttu-id="45972-110">IID_IOSTX</span><span class="sxs-lookup"><span data-stu-id="45972-110">IID_IOSTX</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="45972-111">Заказ Vtable</span><span class="sxs-lookup"><span data-stu-id="45972-111">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="45972-112">GetLastError</span><span class="sxs-lookup"><span data-stu-id="45972-112">GetLastError</span></span>](iostx-getlasterror.md) <br/> |<span data-ttu-id="45972-113">Получает расширенные сведения о последней ошибке.</span><span class="sxs-lookup"><span data-stu-id="45972-113">Gets extended information about the last error.</span></span>  <br/> |
|[<span data-ttu-id="45972-114">InitSync</span><span class="sxs-lookup"><span data-stu-id="45972-114">InitSync</span></span>](iostx-initsync.md) <br/> |<span data-ttu-id="45972-115">Сообщает локальному магазину, что синхронизация вот-вот начнется.</span><span class="sxs-lookup"><span data-stu-id="45972-115">Informs the local store that synchronization is about to start.</span></span>  <br/> |
|[<span data-ttu-id="45972-116">SyncBeg</span><span class="sxs-lookup"><span data-stu-id="45972-116">SyncBeg</span></span>](iostx-syncbeg.md) <br/> |<span data-ttu-id="45972-117">Подготавливает локальный магазин для синхронизации в определенном состоянии и извлекает необходимые сведения для репликации.</span><span class="sxs-lookup"><span data-stu-id="45972-117">Prepares the local store for synchronization in a particular state and retrieves the necessary information to replicate.</span></span>  <br/> |
|[<span data-ttu-id="45972-118">SyncEnd</span><span class="sxs-lookup"><span data-stu-id="45972-118">SyncEnd</span></span>](iostx-syncend.md) <br/> |<span data-ttu-id="45972-119">Завершает синхронизацию в текущем состоянии и выходит из этого состояния.</span><span class="sxs-lookup"><span data-stu-id="45972-119">Ends synchronization in the current state and exits that state.</span></span>  <br/> |
|[<span data-ttu-id="45972-120">SyncHdrBeg</span><span class="sxs-lookup"><span data-stu-id="45972-120">SyncHdrBeg</span></span>](iostx-synchdrbeg.md) <br/> |<span data-ttu-id="45972-121">Начинается синхронизация для заглавного сообщения.</span><span class="sxs-lookup"><span data-stu-id="45972-121">Starts synchronization for a message header.</span></span>  <br/> |
|[<span data-ttu-id="45972-122">SyncHdrEnd</span><span class="sxs-lookup"><span data-stu-id="45972-122">SyncHdrEnd</span></span>](iostx-synchdrend.md) <br/> |<span data-ttu-id="45972-123">Завершается синхронизация для заглавного сообщения.</span><span class="sxs-lookup"><span data-stu-id="45972-123">Ends synchronization for a message header.</span></span>  <br/> |
|[<span data-ttu-id="45972-124">SetSyncResult</span><span class="sxs-lookup"><span data-stu-id="45972-124">SetSyncResult</span></span>](iostx-setsyncresult.md) <br/> |<span data-ttu-id="45972-125">Задает результат синхронизации.</span><span class="sxs-lookup"><span data-stu-id="45972-125">Sets the result of the synchronization.</span></span>  <br/> |
| <span data-ttu-id="45972-126">*Член placeholder*</span><span class="sxs-lookup"><span data-stu-id="45972-126">*Placeholder member*</span></span>  <br/> | <span data-ttu-id="45972-127">*Не поддерживается или не документируется.*</span><span class="sxs-lookup"><span data-stu-id="45972-127">*Not supported or documented.*</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="45972-128">Примечания</span><span class="sxs-lookup"><span data-stu-id="45972-128">Remarks</span></span>

<span data-ttu-id="45972-129">Когда клиент загружает или синхронизирует содержимое папок и папок в локальном магазине, он перемещает локальный магазин из одного состояния в другое, как повеяно на схеме перехода состояния в компьютере состояния [репликации.](about-the-replication-state-machine.md)</span><span class="sxs-lookup"><span data-stu-id="45972-129">When a client uploads or synchronizes folders and folder contents on a local store, it moves the local store from one state to another as depicted in the state transition diagram in [About the Replication State Machine](about-the-replication-state-machine.md).</span></span> <span data-ttu-id="45972-130">Ниже приводится порядок событий для клиента для перемещения локального магазина из одного состояния в другое:</span><span class="sxs-lookup"><span data-stu-id="45972-130">The following is the order of events for the client to move the local store from one state to another:</span></span>
  
1. <span data-ttu-id="45972-131">Клиент вызывает **IOSTX::InitSync,** чтобы сообщить локальному магазину, что репликация вот-вот начнется.</span><span class="sxs-lookup"><span data-stu-id="45972-131">The client calls **IOSTX::InitSync** to inform the local store that replication is about to start.</span></span> 
    
2. <span data-ttu-id="45972-132">В зависимости от направления репликации и репликации объектов клиент вызывает **IOSTX::SyncBeg,** чтобы начать репликацию в соответствующем состоянии.</span><span class="sxs-lookup"><span data-stu-id="45972-132">Depending on the direction of replication and the objects to replicate, the client calls **IOSTX::SyncBeg** to begin replication in the appropriate state.</span></span> <span data-ttu-id="45972-133">Outlook предоставляет клиенту необходимые сведения, и клиент выполняет репликацию.</span><span class="sxs-lookup"><span data-stu-id="45972-133">Outlook provides the client the necessary information, and the client performs the replication.</span></span> 
    
3. <span data-ttu-id="45972-134">Клиент вызывает **IOSTX::SetSyncResult,** чтобы вернуть результат репликации.</span><span class="sxs-lookup"><span data-stu-id="45972-134">The client calls **IOSTX::SetSyncResult** to return the result of the replication.</span></span> 
    
4. <span data-ttu-id="45972-135">Клиент вызывает **IOSTX::SyncEnd,** чтобы закончить репликацию, Outlook необходимую информацию для последующей репликации.</span><span class="sxs-lookup"><span data-stu-id="45972-135">The client calls **IOSTX::SyncEnd** to end the replication, providing Outlook the necessary information for subsequent replication.</span></span> 
    
<span data-ttu-id="45972-136">В частности, при загрузке элементов сообщений клиент использует **IOSTX::SyncHdrBeg** и **IOSTX::SyncHdrEnd,** чтобы обновить полный элемент сообщения с помощью загона сообщений в локальном магазине:</span><span class="sxs-lookup"><span data-stu-id="45972-136">In particular, when downloading message items, the client uses **IOSTX::SyncHdrBeg** and **IOSTX::SyncHdrEnd** to update a full message item with the message header on the local store:</span></span> 
  
1. <span data-ttu-id="45972-137">После **IOSTX::SyncHdrBeg** локальный магазин переходит в состояние загонщика сообщений для скачивания.</span><span class="sxs-lookup"><span data-stu-id="45972-137">Upon **IOSTX::SyncHdrBeg**, the local store transitions into the download message header state.</span></span> <span data-ttu-id="45972-138">Outlook сначала предоставляет клиенту текущий заглавной текст сообщения в локальном магазине.</span><span class="sxs-lookup"><span data-stu-id="45972-138">Outlook initially provides the client with the current message header on the local store.</span></span>
    
2. <span data-ttu-id="45972-139">Клиент загружает полный элемент сообщения вместе с загонами сообщений.</span><span class="sxs-lookup"><span data-stu-id="45972-139">The client downloads a full message item together with the message header.</span></span>
    
3. <span data-ttu-id="45972-140">Outlook элемент в локальном магазине с полным элементом сообщения.</span><span class="sxs-lookup"><span data-stu-id="45972-140">Outlook updates the item on the local store with the full message item.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="45972-141">См. также</span><span class="sxs-lookup"><span data-stu-id="45972-141">See also</span></span>



[<span data-ttu-id="45972-142">Сведения об API репликации</span><span class="sxs-lookup"><span data-stu-id="45972-142">About the Replication API</span></span>](about-the-replication-api.md)
  
[<span data-ttu-id="45972-143">Константы MAPI</span><span class="sxs-lookup"><span data-stu-id="45972-143">MAPI Constants</span></span>](mapi-constants.md)

