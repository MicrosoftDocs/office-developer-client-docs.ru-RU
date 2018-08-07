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
ms.openlocfilehash: ddc61aa42b1087ed5f0ecb7986125ceef27cddce
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19809462"
---
# <a name="iostxsyncbeg"></a><span data-ttu-id="3941d-103">IOSTX::SyncBeg</span><span class="sxs-lookup"><span data-stu-id="3941d-103">IOSTX::SyncBeg</span></span>

  
  
<span data-ttu-id="3941d-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="3941d-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="3941d-105">Подготавливает локального хранилища для синхронизации в определенное состояние и получает сведения, необходимые для репликации.</span><span class="sxs-lookup"><span data-stu-id="3941d-105">Prepares the local store for synchronization in a particular state and retrieves the necessary information to replicate.</span></span>
  
```cpp
HRESULT SyncBeg( 
    UINT uiSync, 
    LPVOID *ppv 
);
```

## <a name="parameters"></a><span data-ttu-id="3941d-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="3941d-106">Parameters</span></span>

 <span data-ttu-id="3941d-107">_uiSync_</span><span class="sxs-lookup"><span data-stu-id="3941d-107">_uiSync_</span></span>
  
>  <span data-ttu-id="3941d-108">[in] Состояние, которое будет ввести локального хранилища.</span><span class="sxs-lookup"><span data-stu-id="3941d-108">[in] The state that the local store will enter.</span></span> <span data-ttu-id="3941d-109">Ниже приведен список состояний идентификаторы:</span><span class="sxs-lookup"><span data-stu-id="3941d-109">The following is a list of state identifers:</span></span> 
    
<span data-ttu-id="3941d-110">LR_SYNC_IDLE</span><span class="sxs-lookup"><span data-stu-id="3941d-110">LR_SYNC_IDLE</span></span>
  
> 
    
<span data-ttu-id="3941d-111">LR_SYNC</span><span class="sxs-lookup"><span data-stu-id="3941d-111">LR_SYNC</span></span>
  
> 
    
<span data-ttu-id="3941d-112">LR_SYNC_UPLOAD_HIERARCHY</span><span class="sxs-lookup"><span data-stu-id="3941d-112">LR_SYNC_UPLOAD_HIERARCHY</span></span>
  
> 
    
<span data-ttu-id="3941d-113">LR_SYNC_UPLOAD_FOLDER</span><span class="sxs-lookup"><span data-stu-id="3941d-113">LR_SYNC_UPLOAD_FOLDER</span></span>
  
> 
    
<span data-ttu-id="3941d-114">LR_SYNC_CONTENTS</span><span class="sxs-lookup"><span data-stu-id="3941d-114">LR_SYNC_CONTENTS</span></span>
  
> 
    
<span data-ttu-id="3941d-115">LR_SYNC_UPLOAD_TABLE</span><span class="sxs-lookup"><span data-stu-id="3941d-115">LR_SYNC_UPLOAD_TABLE</span></span>
  
> 
    
<span data-ttu-id="3941d-116">LR_SYNC_UPLOAD_MESSAGE</span><span class="sxs-lookup"><span data-stu-id="3941d-116">LR_SYNC_UPLOAD_MESSAGE</span></span>
  
> 
    
<span data-ttu-id="3941d-117">LR_SYNC_UPLOAD_MESSAGE_READ</span><span class="sxs-lookup"><span data-stu-id="3941d-117">LR_SYNC_UPLOAD_MESSAGE_READ</span></span>
  
> 
    
<span data-ttu-id="3941d-118">LR_SYNC_UPLOAD_MESSAGE_DEL</span><span class="sxs-lookup"><span data-stu-id="3941d-118">LR_SYNC_UPLOAD_MESSAGE_DEL</span></span>
  
> 
    
<span data-ttu-id="3941d-119">LR_SYNC_DOWNLOAD_HIERARCHY</span><span class="sxs-lookup"><span data-stu-id="3941d-119">LR_SYNC_DOWNLOAD_HIERARCHY</span></span>
  
> 
    
<span data-ttu-id="3941d-120">LR_SYNC_DOWNLOAD_TABLE</span><span class="sxs-lookup"><span data-stu-id="3941d-120">LR_SYNC_DOWNLOAD_TABLE</span></span>
  
> 
    
 <span data-ttu-id="3941d-121">_ppv_</span><span class="sxs-lookup"><span data-stu-id="3941d-121">_ppv_</span></span>
  
>  <span data-ttu-id="3941d-122">[в] / [out] указатель на структуру данных, соответствующее состоянию для ввода.</span><span class="sxs-lookup"><span data-stu-id="3941d-122">[in]/[out] Pointer to the data structure corresponding to the state to enter.</span></span> 
    
[<span data-ttu-id="3941d-123">DNHIER</span><span class="sxs-lookup"><span data-stu-id="3941d-123">DNHIER</span></span>](dnhier.md)
  
> 
    
[<span data-ttu-id="3941d-124">DNTBL</span><span class="sxs-lookup"><span data-stu-id="3941d-124">DNTBL</span></span>](dntbl.md)
  
> 
    
[<span data-ttu-id="3941d-125">DNTBL</span><span class="sxs-lookup"><span data-stu-id="3941d-125">DNTBL</span></span>](dntbl.md)
  
> 
    
[<span data-ttu-id="3941d-126">SYNC</span><span class="sxs-lookup"><span data-stu-id="3941d-126">SYNC</span></span>](sync.md)
  
> 
    
[<span data-ttu-id="3941d-127">SYNCCONT</span><span class="sxs-lookup"><span data-stu-id="3941d-127">SYNCCONT</span></span>](synccont.md)
  
> 
    
[<span data-ttu-id="3941d-128">UPDEL</span><span class="sxs-lookup"><span data-stu-id="3941d-128">UPDEL</span></span>](updel.md)
  
> 
    
[<span data-ttu-id="3941d-129">UPDELE</span><span class="sxs-lookup"><span data-stu-id="3941d-129">UPDELE</span></span>](updele.md)
  
> 
    
[<span data-ttu-id="3941d-130">UPFLD</span><span class="sxs-lookup"><span data-stu-id="3941d-130">UPFLD</span></span>](upfld.md)
  
> 
    
[<span data-ttu-id="3941d-131">UPHIER</span><span class="sxs-lookup"><span data-stu-id="3941d-131">UPHIER</span></span>](uphier.md)
  
> 
    
[<span data-ttu-id="3941d-132">UPMOV</span><span class="sxs-lookup"><span data-stu-id="3941d-132">UPMOV</span></span>](upmov.md)
  
> 
    
[<span data-ttu-id="3941d-133">UPMSG</span><span class="sxs-lookup"><span data-stu-id="3941d-133">UPMSG</span></span>](upmsg.md)
  
> 
    
[<span data-ttu-id="3941d-134">UPREAD</span><span class="sxs-lookup"><span data-stu-id="3941d-134">UPREAD</span></span>](upread.md)
  
> 
    
[<span data-ttu-id="3941d-135">UPREADE</span><span class="sxs-lookup"><span data-stu-id="3941d-135">UPREADE</span></span>](upreade.md)
  
> 
    
[<span data-ttu-id="3941d-136">UPTBL</span><span class="sxs-lookup"><span data-stu-id="3941d-136">UPTBL</span></span>](uptbl.md)
  
> 
    
[<span data-ttu-id="3941d-137">UPTBLE</span><span class="sxs-lookup"><span data-stu-id="3941d-137">UPTBLE</span></span>](uptble.md)
  
> 
    
## <a name="remarks"></a><span data-ttu-id="3941d-138">Замечания</span><span class="sxs-lookup"><span data-stu-id="3941d-138">Remarks</span></span>

<span data-ttu-id="3941d-139">Клиент вызывает **[IOSTX::SetSyncResult](iostx-setsyncresult.md)** для установки в результате синхронизации и затем вызывает **[IOSTX::SyncEnd](iostx-syncend.md)** для завершения этого состояния.</span><span class="sxs-lookup"><span data-stu-id="3941d-139">The client calls **[IOSTX::SetSyncResult](iostx-setsyncresult.md)** to set the result of the synchronization, and then calls **[IOSTX::SyncEnd](iostx-syncend.md)** to end that state.</span></span> <span data-ttu-id="3941d-140">Клиент должен вызывать **[IOSTX::SyncEnd](iostx-syncend.md)** для каждого вызова **IOSTX::SyncBeg** для определения, была ли успешно реплицирована состояние.</span><span class="sxs-lookup"><span data-stu-id="3941d-140">The client must call **[IOSTX::SyncEnd](iostx-syncend.md)** for each call to **IOSTX::SyncBeg** in order to determine whether the state has been successfully replicated.</span></span> <span data-ttu-id="3941d-141">После этого определения Outlook можно приступать к Очистка внутреннего состояния.</span><span class="sxs-lookup"><span data-stu-id="3941d-141">Once this has been determined, Outlook can begin to clean up its internal state.</span></span> 
  
<span data-ttu-id="3941d-142">Большинство этих структур содержат [out] / [in] сведения, и для передачи информации клиент и клиента для передачи сведений об Outlook в Outlook.</span><span class="sxs-lookup"><span data-stu-id="3941d-142">Most of these structures contain [out]/[in] information, allowing Outlook to pass information to the client, and the client to pass information to Outlook.</span></span> <span data-ttu-id="3941d-143">Когда клиент вызывает **IOSTX::SyncBeg**, Outlook выделяет структуру данных для указанного состояния и инициализирует со сведениями для этого состояния.</span><span class="sxs-lookup"><span data-stu-id="3941d-143">When the client calls **IOSTX::SyncBeg**, Outlook allocates the data structure for a given state and initializes it with information for that state.</span></span> <span data-ttu-id="3941d-144">Это [out] данные.</span><span class="sxs-lookup"><span data-stu-id="3941d-144">This is the [out] information.</span></span> <span data-ttu-id="3941d-145">В состоянии, клиент обновляет соответствующие структуры данных для этого состояния.</span><span class="sxs-lookup"><span data-stu-id="3941d-145">While in a state, the client updates the corresponding data structure for that state.</span></span> <span data-ttu-id="3941d-146">Это [in] сведения.</span><span class="sxs-lookup"><span data-stu-id="3941d-146">This is the [in] information.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="3941d-147">См. также</span><span class="sxs-lookup"><span data-stu-id="3941d-147">See also</span></span>



[<span data-ttu-id="3941d-148">IOSTX::GetLastError</span><span class="sxs-lookup"><span data-stu-id="3941d-148">IOSTX::GetLastError</span></span>](iostx-getlasterror.md)
  
[<span data-ttu-id="3941d-149">IOSTX::InitSync</span><span class="sxs-lookup"><span data-stu-id="3941d-149">IOSTX::InitSync</span></span>](iostx-initsync.md)
  
[<span data-ttu-id="3941d-150">IOSTX::SetSyncResult</span><span class="sxs-lookup"><span data-stu-id="3941d-150">IOSTX::SetSyncResult</span></span>](iostx-setsyncresult.md)
  
[<span data-ttu-id="3941d-151">IOSTX::SyncEnd</span><span class="sxs-lookup"><span data-stu-id="3941d-151">IOSTX::SyncEnd</span></span>](iostx-syncend.md)
  
[<span data-ttu-id="3941d-152">IOSTX::SyncHdrBeg</span><span class="sxs-lookup"><span data-stu-id="3941d-152">IOSTX::SyncHdrBeg</span></span>](iostx-synchdrbeg.md)
  
[<span data-ttu-id="3941d-153">IOSTX::SyncHdrEnd</span><span class="sxs-lookup"><span data-stu-id="3941d-153">IOSTX::SyncHdrEnd</span></span>](iostx-synchdrend.md)
  
[<span data-ttu-id="3941d-154">IOSTX : IUnknown</span><span class="sxs-lookup"><span data-stu-id="3941d-154">IOSTX : IUnknown</span></span>](iostxiunknown.md)


[<span data-ttu-id="3941d-155">��������� MAPI</span><span class="sxs-lookup"><span data-stu-id="3941d-155">MAPI Constants</span></span>](mapi-constants.md)

