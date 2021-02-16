---
title: IOSTXSyncBeg
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IOSTX.SyncBeg
api_type:
- COM
ms.assetid: 4a935df3-98c4-2742-206e-4e16eda7b9bc
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: ae4497295328155780fc5208d1699169698e02d8
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33411941"
---
# <a name="iostxsyncbeg"></a><span data-ttu-id="c2efa-103">IOSTX::SyncBeg</span><span class="sxs-lookup"><span data-stu-id="c2efa-103">IOSTX::SyncBeg</span></span>

  
  
<span data-ttu-id="c2efa-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c2efa-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c2efa-105">Подготавливает локальное хранилище к синхронизации в определенном состоянии и извлекает необходимые сведения для репликации.</span><span class="sxs-lookup"><span data-stu-id="c2efa-105">Prepares the local store for synchronization in a particular state and retrieves the necessary information to replicate.</span></span>
  
```cpp
HRESULT SyncBeg( 
    UINT uiSync, 
    LPVOID *ppv 
);
```

## <a name="parameters"></a><span data-ttu-id="c2efa-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="c2efa-106">Parameters</span></span>

 <span data-ttu-id="c2efa-107">_uiSync_</span><span class="sxs-lookup"><span data-stu-id="c2efa-107">_uiSync_</span></span>
  
>  <span data-ttu-id="c2efa-108">[in] Состояние, которое будет вводить локальное хранилище.</span><span class="sxs-lookup"><span data-stu-id="c2efa-108">[in] The state that the local store will enter.</span></span> <span data-ttu-id="c2efa-109">Ниже приводится список отступов состояния.</span><span class="sxs-lookup"><span data-stu-id="c2efa-109">The following is a list of state identifers:</span></span> 
    
<span data-ttu-id="c2efa-110">LR_SYNC_IDLE</span><span class="sxs-lookup"><span data-stu-id="c2efa-110">LR_SYNC_IDLE</span></span>
  
> 
    
<span data-ttu-id="c2efa-111">LR_SYNC</span><span class="sxs-lookup"><span data-stu-id="c2efa-111">LR_SYNC</span></span>
  
> 
    
<span data-ttu-id="c2efa-112">LR_SYNC_UPLOAD_HIERARCHY</span><span class="sxs-lookup"><span data-stu-id="c2efa-112">LR_SYNC_UPLOAD_HIERARCHY</span></span>
  
> 
    
<span data-ttu-id="c2efa-113">LR_SYNC_UPLOAD_FOLDER</span><span class="sxs-lookup"><span data-stu-id="c2efa-113">LR_SYNC_UPLOAD_FOLDER</span></span>
  
> 
    
<span data-ttu-id="c2efa-114">LR_SYNC_CONTENTS</span><span class="sxs-lookup"><span data-stu-id="c2efa-114">LR_SYNC_CONTENTS</span></span>
  
> 
    
<span data-ttu-id="c2efa-115">LR_SYNC_UPLOAD_TABLE</span><span class="sxs-lookup"><span data-stu-id="c2efa-115">LR_SYNC_UPLOAD_TABLE</span></span>
  
> 
    
<span data-ttu-id="c2efa-116">LR_SYNC_UPLOAD_MESSAGE</span><span class="sxs-lookup"><span data-stu-id="c2efa-116">LR_SYNC_UPLOAD_MESSAGE</span></span>
  
> 
    
<span data-ttu-id="c2efa-117">LR_SYNC_UPLOAD_MESSAGE_READ</span><span class="sxs-lookup"><span data-stu-id="c2efa-117">LR_SYNC_UPLOAD_MESSAGE_READ</span></span>
  
> 
    
<span data-ttu-id="c2efa-118">LR_SYNC_UPLOAD_MESSAGE_DEL</span><span class="sxs-lookup"><span data-stu-id="c2efa-118">LR_SYNC_UPLOAD_MESSAGE_DEL</span></span>
  
> 
    
<span data-ttu-id="c2efa-119">LR_SYNC_DOWNLOAD_HIERARCHY</span><span class="sxs-lookup"><span data-stu-id="c2efa-119">LR_SYNC_DOWNLOAD_HIERARCHY</span></span>
  
> 
    
<span data-ttu-id="c2efa-120">LR_SYNC_DOWNLOAD_TABLE</span><span class="sxs-lookup"><span data-stu-id="c2efa-120">LR_SYNC_DOWNLOAD_TABLE</span></span>
  
> 
    
 <span data-ttu-id="c2efa-121">_ppv_</span><span class="sxs-lookup"><span data-stu-id="c2efa-121">_ppv_</span></span>
  
>  <span data-ttu-id="c2efa-122">[in]/[out] Pointer to the data structure corresponding to the state to enter.</span><span class="sxs-lookup"><span data-stu-id="c2efa-122">[in]/[out] Pointer to the data structure corresponding to the state to enter.</span></span> 
    
[<span data-ttu-id="c2efa-123">DNHIER</span><span class="sxs-lookup"><span data-stu-id="c2efa-123">DNHIER</span></span>](dnhier.md)
  
> 
    
[<span data-ttu-id="c2efa-124">DNTBL</span><span class="sxs-lookup"><span data-stu-id="c2efa-124">DNTBL</span></span>](dntbl.md)
  
> 
    
[<span data-ttu-id="c2efa-125">DNTBL</span><span class="sxs-lookup"><span data-stu-id="c2efa-125">DNTBL</span></span>](dntbl.md)
  
> 
    
[<span data-ttu-id="c2efa-126">SYNC</span><span class="sxs-lookup"><span data-stu-id="c2efa-126">SYNC</span></span>](sync.md)
  
> 
    
[<span data-ttu-id="c2efa-127">SYNCCONT</span><span class="sxs-lookup"><span data-stu-id="c2efa-127">SYNCCONT</span></span>](synccont.md)
  
> 
    
[<span data-ttu-id="c2efa-128">UPDEL</span><span class="sxs-lookup"><span data-stu-id="c2efa-128">UPDEL</span></span>](updel.md)
  
> 
    
[<span data-ttu-id="c2efa-129">UPDELE</span><span class="sxs-lookup"><span data-stu-id="c2efa-129">UPDELE</span></span>](updele.md)
  
> 
    
[<span data-ttu-id="c2efa-130">UPFLD</span><span class="sxs-lookup"><span data-stu-id="c2efa-130">UPFLD</span></span>](upfld.md)
  
> 
    
[<span data-ttu-id="c2efa-131">UPHIER</span><span class="sxs-lookup"><span data-stu-id="c2efa-131">UPHIER</span></span>](uphier.md)
  
> 
    
[<span data-ttu-id="c2efa-132">UPMOV</span><span class="sxs-lookup"><span data-stu-id="c2efa-132">UPMOV</span></span>](upmov.md)
  
> 
    
[<span data-ttu-id="c2efa-133">UPMSG</span><span class="sxs-lookup"><span data-stu-id="c2efa-133">UPMSG</span></span>](upmsg.md)
  
> 
    
[<span data-ttu-id="c2efa-134">UPREAD</span><span class="sxs-lookup"><span data-stu-id="c2efa-134">UPREAD</span></span>](upread.md)
  
> 
    
[<span data-ttu-id="c2efa-135">UPREADE</span><span class="sxs-lookup"><span data-stu-id="c2efa-135">UPREADE</span></span>](upreade.md)
  
> 
    
[<span data-ttu-id="c2efa-136">UPTBL</span><span class="sxs-lookup"><span data-stu-id="c2efa-136">UPTBL</span></span>](uptbl.md)
  
> 
    
[<span data-ttu-id="c2efa-137">UPTBLE</span><span class="sxs-lookup"><span data-stu-id="c2efa-137">UPTBLE</span></span>](uptble.md)
  
> 
    
## <a name="remarks"></a><span data-ttu-id="c2efa-138">Примечания</span><span class="sxs-lookup"><span data-stu-id="c2efa-138">Remarks</span></span>

<span data-ttu-id="c2efa-139">Клиент вызывает **[IOSTX::SetSyncResult,](iostx-setsyncresult.md)** чтобы установить результат синхронизации, а затем вызывает **[IOSTX::SyncEnd,](iostx-syncend.md)** чтобы закончить это состояние.</span><span class="sxs-lookup"><span data-stu-id="c2efa-139">The client calls **[IOSTX::SetSyncResult](iostx-setsyncresult.md)** to set the result of the synchronization, and then calls **[IOSTX::SyncEnd](iostx-syncend.md)** to end that state.</span></span> <span data-ttu-id="c2efa-140">Клиент должен вызывать **[IOSTX::SyncEnd](iostx-syncend.md)** для каждого вызова **IOSTX::SyncBeg,** чтобы определить, успешно ли реплицировано состояние.</span><span class="sxs-lookup"><span data-stu-id="c2efa-140">The client must call **[IOSTX::SyncEnd](iostx-syncend.md)** for each call to **IOSTX::SyncBeg** in order to determine whether the state has been successfully replicated.</span></span> <span data-ttu-id="c2efa-141">После этого Outlook может начать очищать свое внутреннее состояние.</span><span class="sxs-lookup"><span data-stu-id="c2efa-141">Once this has been determined, Outlook can begin to clean up its internal state.</span></span> 
  
<span data-ttu-id="c2efa-142">Большинство из этих структур содержат сведения [out]/[in], что позволяет Outlook передавать данные клиенту, а клиент — в Outlook.</span><span class="sxs-lookup"><span data-stu-id="c2efa-142">Most of these structures contain [out]/[in] information, allowing Outlook to pass information to the client, and the client to pass information to Outlook.</span></span> <span data-ttu-id="c2efa-143">Когда клиент вызывает **IOSTX::SyncBeg,** Outlook выделяет структуру данных для заданного состояния и инициализирует ее с информацией для этого состояния.</span><span class="sxs-lookup"><span data-stu-id="c2efa-143">When the client calls **IOSTX::SyncBeg**, Outlook allocates the data structure for a given state and initializes it with information for that state.</span></span> <span data-ttu-id="c2efa-144">Это сведения о [выходе].</span><span class="sxs-lookup"><span data-stu-id="c2efa-144">This is the [out] information.</span></span> <span data-ttu-id="c2efa-145">Находясь в состоянии, клиент обновляет соответствующую структуру данных для этого состояния.</span><span class="sxs-lookup"><span data-stu-id="c2efa-145">While in a state, the client updates the corresponding data structure for that state.</span></span> <span data-ttu-id="c2efa-146">Это сведения о [в].</span><span class="sxs-lookup"><span data-stu-id="c2efa-146">This is the [in] information.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="c2efa-147">См. также</span><span class="sxs-lookup"><span data-stu-id="c2efa-147">See also</span></span>



[<span data-ttu-id="c2efa-148">IOSTX::GetLastError</span><span class="sxs-lookup"><span data-stu-id="c2efa-148">IOSTX::GetLastError</span></span>](iostx-getlasterror.md)
  
[<span data-ttu-id="c2efa-149">IOSTX::InitSync</span><span class="sxs-lookup"><span data-stu-id="c2efa-149">IOSTX::InitSync</span></span>](iostx-initsync.md)
  
[<span data-ttu-id="c2efa-150">IOSTX::SetSyncResult</span><span class="sxs-lookup"><span data-stu-id="c2efa-150">IOSTX::SetSyncResult</span></span>](iostx-setsyncresult.md)
  
[<span data-ttu-id="c2efa-151">IOSTX::SyncEnd</span><span class="sxs-lookup"><span data-stu-id="c2efa-151">IOSTX::SyncEnd</span></span>](iostx-syncend.md)
  
[<span data-ttu-id="c2efa-152">IOSTX::SyncHdrBeg</span><span class="sxs-lookup"><span data-stu-id="c2efa-152">IOSTX::SyncHdrBeg</span></span>](iostx-synchdrbeg.md)
  
[<span data-ttu-id="c2efa-153">IOSTX::SyncHdrEnd</span><span class="sxs-lookup"><span data-stu-id="c2efa-153">IOSTX::SyncHdrEnd</span></span>](iostx-synchdrend.md)
  
[<span data-ttu-id="c2efa-154">IOSTX : IUnknown</span><span class="sxs-lookup"><span data-stu-id="c2efa-154">IOSTX : IUnknown</span></span>](iostxiunknown.md)


[<span data-ttu-id="c2efa-155">Константы MAPI</span><span class="sxs-lookup"><span data-stu-id="c2efa-155">MAPI Constants</span></span>](mapi-constants.md)

