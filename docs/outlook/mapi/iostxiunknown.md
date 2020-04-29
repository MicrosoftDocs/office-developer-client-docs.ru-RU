---
title: ИОСТКС IUnknown
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
# <a name="iostx--iunknown"></a><span data-ttu-id="819e0-103">IOSTX : IUnknown</span><span class="sxs-lookup"><span data-stu-id="819e0-103">IOSTX : IUnknown</span></span>

  
  
<span data-ttu-id="819e0-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="819e0-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="819e0-105">Предоставляет методы синхронизации.</span><span class="sxs-lookup"><span data-stu-id="819e0-105">Provides synchronization methods.</span></span> <span data-ttu-id="819e0-106">Этот интерфейс получает необходимые сведения для репликации локальных изменений сервера и сервера в локальное хранилище.</span><span class="sxs-lookup"><span data-stu-id="819e0-106">This interface retrieves the necessary information to replicate local changes to the server and server changes to the local store.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="819e0-107">Предоставлено:</span><span class="sxs-lookup"><span data-stu-id="819e0-107">Provided by:</span></span>  <br/> |[<span data-ttu-id="819e0-108">IPSTX::GetSyncObject</span><span class="sxs-lookup"><span data-stu-id="819e0-108">IPSTX::GetSyncObject</span></span>](iostx-setsyncresult.md) <br/> |
|<span data-ttu-id="819e0-109">Идентификатор интерфейса:</span><span class="sxs-lookup"><span data-stu-id="819e0-109">Interface identifier:</span></span>  <br/> |<span data-ttu-id="819e0-110">IID_IOSTX</span><span class="sxs-lookup"><span data-stu-id="819e0-110">IID_IOSTX</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="819e0-111">Заказ vtable</span><span class="sxs-lookup"><span data-stu-id="819e0-111">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="819e0-112">GetLastError</span><span class="sxs-lookup"><span data-stu-id="819e0-112">GetLastError</span></span>](iostx-getlasterror.md) <br/> |<span data-ttu-id="819e0-113">Получает расширенные сведения о последней ошибке.</span><span class="sxs-lookup"><span data-stu-id="819e0-113">Gets extended information about the last error.</span></span>  <br/> |
|[<span data-ttu-id="819e0-114">инитсинк</span><span class="sxs-lookup"><span data-stu-id="819e0-114">InitSync</span></span>](iostx-initsync.md) <br/> |<span data-ttu-id="819e0-115">Информирует локальное хранилище о том, что синхронизация будет запущена.</span><span class="sxs-lookup"><span data-stu-id="819e0-115">Informs the local store that synchronization is about to start.</span></span>  <br/> |
|[<span data-ttu-id="819e0-116">синкбег</span><span class="sxs-lookup"><span data-stu-id="819e0-116">SyncBeg</span></span>](iostx-syncbeg.md) <br/> |<span data-ttu-id="819e0-117">Подготавливает локальное хранилище к синхронизации в определенном состоянии и получает сведения, необходимые для репликации.</span><span class="sxs-lookup"><span data-stu-id="819e0-117">Prepares the local store for synchronization in a particular state and retrieves the necessary information to replicate.</span></span>  <br/> |
|[<span data-ttu-id="819e0-118">SyncEnd</span><span class="sxs-lookup"><span data-stu-id="819e0-118">SyncEnd</span></span>](iostx-syncend.md) <br/> |<span data-ttu-id="819e0-119">Завершает синхронизацию в текущем состоянии и выходит из этого состояния.</span><span class="sxs-lookup"><span data-stu-id="819e0-119">Ends synchronization in the current state and exits that state.</span></span>  <br/> |
|[<span data-ttu-id="819e0-120">синчдрбег</span><span class="sxs-lookup"><span data-stu-id="819e0-120">SyncHdrBeg</span></span>](iostx-synchdrbeg.md) <br/> |<span data-ttu-id="819e0-121">Запускает синхронизацию для заголовка сообщения.</span><span class="sxs-lookup"><span data-stu-id="819e0-121">Starts synchronization for a message header.</span></span>  <br/> |
|[<span data-ttu-id="819e0-122">синчдренд</span><span class="sxs-lookup"><span data-stu-id="819e0-122">SyncHdrEnd</span></span>](iostx-synchdrend.md) <br/> |<span data-ttu-id="819e0-123">Завершает синхронизацию для заголовка сообщения.</span><span class="sxs-lookup"><span data-stu-id="819e0-123">Ends synchronization for a message header.</span></span>  <br/> |
|[<span data-ttu-id="819e0-124">сетсинкресулт</span><span class="sxs-lookup"><span data-stu-id="819e0-124">SetSyncResult</span></span>](iostx-setsyncresult.md) <br/> |<span data-ttu-id="819e0-125">Задает результат синхронизации.</span><span class="sxs-lookup"><span data-stu-id="819e0-125">Sets the result of the synchronization.</span></span>  <br/> |
| <span data-ttu-id="819e0-126">*Элемент PlaceHolder*</span><span class="sxs-lookup"><span data-stu-id="819e0-126">*Placeholder member*</span></span>  <br/> | <span data-ttu-id="819e0-127">*Не поддерживается или не задокументировано.*</span><span class="sxs-lookup"><span data-stu-id="819e0-127">*Not supported or documented.*</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="819e0-128">Примечания</span><span class="sxs-lookup"><span data-stu-id="819e0-128">Remarks</span></span>

<span data-ttu-id="819e0-129">Когда клиент отправляет или синхронизирует папки и содержимое папок в локальном хранилище, он перемещает локальное хранилище из одного состояния в другое, как показано на схеме смены состояний в разделе [состояние машины репликации](about-the-replication-state-machine.md).</span><span class="sxs-lookup"><span data-stu-id="819e0-129">When a client uploads or synchronizes folders and folder contents on a local store, it moves the local store from one state to another as depicted in the state transition diagram in [About the Replication State Machine](about-the-replication-state-machine.md).</span></span> <span data-ttu-id="819e0-130">Ниже приведен порядок событий, по которым клиент может переместить локальное хранилище из одного состояния в другое.</span><span class="sxs-lookup"><span data-stu-id="819e0-130">The following is the order of events for the client to move the local store from one state to another:</span></span>
  
1. <span data-ttu-id="819e0-131">Клиент вызывает **иосткс:: инитсинк** , чтобы уведомить локальное хранилище о том, что репликация будет запущена.</span><span class="sxs-lookup"><span data-stu-id="819e0-131">The client calls **IOSTX::InitSync** to inform the local store that replication is about to start.</span></span> 
    
2. <span data-ttu-id="819e0-132">В зависимости от направления репликации и реплицируемых объектов клиент вызывает **иосткс:: синкбег** для начала репликации в соответствующем состоянии.</span><span class="sxs-lookup"><span data-stu-id="819e0-132">Depending on the direction of replication and the objects to replicate, the client calls **IOSTX::SyncBeg** to begin replication in the appropriate state.</span></span> <span data-ttu-id="819e0-133">Outlook предоставляет клиенту необходимую информацию, а клиент выполняет репликацию.</span><span class="sxs-lookup"><span data-stu-id="819e0-133">Outlook provides the client the necessary information, and the client performs the replication.</span></span> 
    
3. <span data-ttu-id="819e0-134">Клиент вызывает **иосткс:: сетсинкресулт** для возврата результата репликации.</span><span class="sxs-lookup"><span data-stu-id="819e0-134">The client calls **IOSTX::SetSyncResult** to return the result of the replication.</span></span> 
    
4. <span data-ttu-id="819e0-135">Клиент вызывает **иосткс:: синценд** для завершения репликации, предоставляя Outlook необходимые сведения для последующей репликации.</span><span class="sxs-lookup"><span data-stu-id="819e0-135">The client calls **IOSTX::SyncEnd** to end the replication, providing Outlook the necessary information for subsequent replication.</span></span> 
    
<span data-ttu-id="819e0-136">В частности, при загрузке элементов сообщения клиент использует **иосткс:: синчдрбег** и **Иосткс:: синчдренд** для обновления полного элемента сообщения с помощью заголовка сообщения в локальном хранилище:</span><span class="sxs-lookup"><span data-stu-id="819e0-136">In particular, when downloading message items, the client uses **IOSTX::SyncHdrBeg** and **IOSTX::SyncHdrEnd** to update a full message item with the message header on the local store:</span></span> 
  
1. <span data-ttu-id="819e0-137">При **иосткс:: синчдрбег**локальное хранилище переходит в состояние загрузки сообщения.</span><span class="sxs-lookup"><span data-stu-id="819e0-137">Upon **IOSTX::SyncHdrBeg**, the local store transitions into the download message header state.</span></span> <span data-ttu-id="819e0-138">Сначала Outlook предоставляет клиент с текущим заголовком сообщения в локальном хранилище.</span><span class="sxs-lookup"><span data-stu-id="819e0-138">Outlook initially provides the client with the current message header on the local store.</span></span>
    
2. <span data-ttu-id="819e0-139">Клиент загружает полный элемент сообщения вместе с заголовком сообщения.</span><span class="sxs-lookup"><span data-stu-id="819e0-139">The client downloads a full message item together with the message header.</span></span>
    
3. <span data-ttu-id="819e0-140">Outlook обновляет элемент в локальном хранилище, используя полный элемент сообщения.</span><span class="sxs-lookup"><span data-stu-id="819e0-140">Outlook updates the item on the local store with the full message item.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="819e0-141">См. также</span><span class="sxs-lookup"><span data-stu-id="819e0-141">See also</span></span>



[<span data-ttu-id="819e0-142">Сведения об API репликации</span><span class="sxs-lookup"><span data-stu-id="819e0-142">About the Replication API</span></span>](about-the-replication-api.md)
  
[<span data-ttu-id="819e0-143">Константы MAPI</span><span class="sxs-lookup"><span data-stu-id="819e0-143">MAPI Constants</span></span>](mapi-constants.md)

