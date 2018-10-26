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
ms.openlocfilehash: 9c9252e83ce212bacf185d0eedb75d30617f9807
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22581750"
---
# <a name="iostx--iunknown"></a><span data-ttu-id="1e8b2-103">IOSTX : IUnknown</span><span class="sxs-lookup"><span data-stu-id="1e8b2-103">IOSTX : IUnknown</span></span>

  
  
<span data-ttu-id="1e8b2-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1e8b2-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1e8b2-105">Предоставляет методы для синхронизации.</span><span class="sxs-lookup"><span data-stu-id="1e8b2-105">Provides synchronization methods.</span></span> <span data-ttu-id="1e8b2-106">Этот интерфейс извлекает сведения, необходимые для репликации изменений локального сервера и сервера изменений в локальном хранилище.</span><span class="sxs-lookup"><span data-stu-id="1e8b2-106">This interface retrieves the necessary information to replicate local changes to the server and server changes to the local store.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="1e8b2-107">Предоставлено:</span><span class="sxs-lookup"><span data-stu-id="1e8b2-107">Provided by:</span></span>  <br/> |[<span data-ttu-id="1e8b2-108">IPSTX::GetSyncObject</span><span class="sxs-lookup"><span data-stu-id="1e8b2-108">IPSTX::GetSyncObject</span></span>](iostx-setsyncresult.md) <br/> |
|<span data-ttu-id="1e8b2-109">Идентификатор интерфейса:</span><span class="sxs-lookup"><span data-stu-id="1e8b2-109">Interface identifier:</span></span>  <br/> |<span data-ttu-id="1e8b2-110">IID_IOSTX</span><span class="sxs-lookup"><span data-stu-id="1e8b2-110">IID_IOSTX</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="1e8b2-111">Порядке vtable</span><span class="sxs-lookup"><span data-stu-id="1e8b2-111">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="1e8b2-112">GetLastError</span><span class="sxs-lookup"><span data-stu-id="1e8b2-112">GetLastError</span></span>](iostx-getlasterror.md) <br/> |<span data-ttu-id="1e8b2-113">Получает расширенные сведения о последней ошибки.</span><span class="sxs-lookup"><span data-stu-id="1e8b2-113">Gets extended information about the last error.</span></span>  <br/> |
|[<span data-ttu-id="1e8b2-114">InitSync</span><span class="sxs-lookup"><span data-stu-id="1e8b2-114">InitSync</span></span>](iostx-initsync.md) <br/> |<span data-ttu-id="1e8b2-115">Информирует локального хранилища, что синхронизация является запуск.</span><span class="sxs-lookup"><span data-stu-id="1e8b2-115">Informs the local store that synchronization is about to start.</span></span>  <br/> |
|[<span data-ttu-id="1e8b2-116">SyncBeg</span><span class="sxs-lookup"><span data-stu-id="1e8b2-116">SyncBeg</span></span>](iostx-syncbeg.md) <br/> |<span data-ttu-id="1e8b2-117">Подготавливает локального хранилища для синхронизации в определенное состояние и получает сведения, необходимые для репликации.</span><span class="sxs-lookup"><span data-stu-id="1e8b2-117">Prepares the local store for synchronization in a particular state and retrieves the necessary information to replicate.</span></span>  <br/> |
|[<span data-ttu-id="1e8b2-118">SyncEnd</span><span class="sxs-lookup"><span data-stu-id="1e8b2-118">SyncEnd</span></span>](iostx-syncend.md) <br/> |<span data-ttu-id="1e8b2-119">Завершает синхронизации в текущем состоянии и выходе из этого состояния.</span><span class="sxs-lookup"><span data-stu-id="1e8b2-119">Ends synchronization in the current state and exits that state.</span></span>  <br/> |
|[<span data-ttu-id="1e8b2-120">SyncHdrBeg</span><span class="sxs-lookup"><span data-stu-id="1e8b2-120">SyncHdrBeg</span></span>](iostx-synchdrbeg.md) <br/> |<span data-ttu-id="1e8b2-121">Запускает синхронизацию для заголовка сообщения.</span><span class="sxs-lookup"><span data-stu-id="1e8b2-121">Starts synchronization for a message header.</span></span>  <br/> |
|[<span data-ttu-id="1e8b2-122">SyncHdrEnd</span><span class="sxs-lookup"><span data-stu-id="1e8b2-122">SyncHdrEnd</span></span>](iostx-synchdrend.md) <br/> |<span data-ttu-id="1e8b2-123">Завершает синхронизации для заголовка сообщения.</span><span class="sxs-lookup"><span data-stu-id="1e8b2-123">Ends synchronization for a message header.</span></span>  <br/> |
|[<span data-ttu-id="1e8b2-124">SetSyncResult</span><span class="sxs-lookup"><span data-stu-id="1e8b2-124">SetSyncResult</span></span>](iostx-setsyncresult.md) <br/> |<span data-ttu-id="1e8b2-125">Задает в результате синхронизации.</span><span class="sxs-lookup"><span data-stu-id="1e8b2-125">Sets the result of the synchronization.</span></span>  <br/> |
| <span data-ttu-id="1e8b2-126">*Заполнитель члена*</span><span class="sxs-lookup"><span data-stu-id="1e8b2-126">*Placeholder member*</span></span>  <br/> | <span data-ttu-id="1e8b2-127">*Не поддерживается, документированных.*</span><span class="sxs-lookup"><span data-stu-id="1e8b2-127">*Not supported or documented.*</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="1e8b2-128">Замечания</span><span class="sxs-lookup"><span data-stu-id="1e8b2-128">Remarks</span></span>

<span data-ttu-id="1e8b2-129">Клиент передает или синхронизирует папок и их содержимого для локального хранилища, переводит локального хранилища из одного состояния в другое как показано на схеме перехода состояния в [О конечного автомата репликации](about-the-replication-state-machine.md).</span><span class="sxs-lookup"><span data-stu-id="1e8b2-129">When a client uploads or synchronizes folders and folder contents on a local store, it moves the local store from one state to another as depicted in the state transition diagram in [About the Replication State Machine](about-the-replication-state-machine.md).</span></span> <span data-ttu-id="1e8b2-130">Ниже приведен порядок событий для клиента для переноса в локальном хранилище из одного состояния в другое.</span><span class="sxs-lookup"><span data-stu-id="1e8b2-130">The following is the order of events for the client to move the local store from one state to another:</span></span>
  
1. <span data-ttu-id="1e8b2-131">Клиент вызывает **IOSTX::InitSync** для оповещения в локальном хранилище, что репликация запускается.</span><span class="sxs-lookup"><span data-stu-id="1e8b2-131">The client calls **IOSTX::InitSync** to inform the local store that replication is about to start.</span></span> 
    
2. <span data-ttu-id="1e8b2-132">В зависимости от направление репликации и объекты для репликации клиент вызывает **IOSTX::SyncBeg** для начала репликации в соответствующее состояние.</span><span class="sxs-lookup"><span data-stu-id="1e8b2-132">Depending on the direction of replication and the objects to replicate, the client calls **IOSTX::SyncBeg** to begin replication in the appropriate state.</span></span> <span data-ttu-id="1e8b2-133">Outlook предоставляет клиенту необходимые сведения и клиент выполняет репликации.</span><span class="sxs-lookup"><span data-stu-id="1e8b2-133">Outlook provides the client the necessary information, and the client performs the replication.</span></span> 
    
3. <span data-ttu-id="1e8b2-134">Клиент вызывает **IOSTX::SetSyncResult** для возврата результатов репликации.</span><span class="sxs-lookup"><span data-stu-id="1e8b2-134">The client calls **IOSTX::SetSyncResult** to return the result of the replication.</span></span> 
    
4. <span data-ttu-id="1e8b2-135">Клиент вызывает **IOSTX::SyncEnd** для завершения репликации, предоставляя сведения, необходимые для последующих репликации Outlook.</span><span class="sxs-lookup"><span data-stu-id="1e8b2-135">The client calls **IOSTX::SyncEnd** to end the replication, providing Outlook the necessary information for subsequent replication.</span></span> 
    
<span data-ttu-id="1e8b2-136">В частности при загрузке элементы сообщения, клиент использует **IOSTX::SyncHdrBeg** и **IOSTX::SyncHdrEnd** обновить элемент полное сообщение с заголовок сообщения в локальном хранилище:</span><span class="sxs-lookup"><span data-stu-id="1e8b2-136">In particular, when downloading message items, the client uses **IOSTX::SyncHdrBeg** and **IOSTX::SyncHdrEnd** to update a full message item with the message header on the local store:</span></span> 
  
1. <span data-ttu-id="1e8b2-137">После **IOSTX::SyncHdrBeg**локального хранилища переходы в состояние заголовка сообщения файл для загрузки.</span><span class="sxs-lookup"><span data-stu-id="1e8b2-137">Upon **IOSTX::SyncHdrBeg**, the local store transitions into the download message header state.</span></span> <span data-ttu-id="1e8b2-138">Изначально Outlook предоставляет клиенту текущий заголовок сообщения в локальном хранилище.</span><span class="sxs-lookup"><span data-stu-id="1e8b2-138">Outlook initially provides the client with the current message header on the local store.</span></span>
    
2. <span data-ttu-id="1e8b2-139">Клиент загружает элемент полного сообщения вместе с заголовок сообщения.</span><span class="sxs-lookup"><span data-stu-id="1e8b2-139">The client downloads a full message item together with the message header.</span></span>
    
3. <span data-ttu-id="1e8b2-140">Outlook вносит элемента на локальном хранилище полного сообщения элемента.</span><span class="sxs-lookup"><span data-stu-id="1e8b2-140">Outlook updates the item on the local store with the full message item.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="1e8b2-141">См. также</span><span class="sxs-lookup"><span data-stu-id="1e8b2-141">See also</span></span>



[<span data-ttu-id="1e8b2-142">Сведения об API репликации</span><span class="sxs-lookup"><span data-stu-id="1e8b2-142">About the Replication API</span></span>](about-the-replication-api.md)
  
[<span data-ttu-id="1e8b2-143">Константы MAPI</span><span class="sxs-lookup"><span data-stu-id="1e8b2-143">MAPI Constants</span></span>](mapi-constants.md)

