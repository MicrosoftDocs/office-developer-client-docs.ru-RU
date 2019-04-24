---
title: Иосткссинкбег
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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32317173"
---
# <a name="iostxsyncbeg"></a><span data-ttu-id="2fb87-103">IOSTX::SyncBeg</span><span class="sxs-lookup"><span data-stu-id="2fb87-103">IOSTX::SyncBeg</span></span>

  
  
<span data-ttu-id="2fb87-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2fb87-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="2fb87-105">ПодГотавливает локальное хранилище к синхронизации в определенном состоянии и получает сведения, необходимые для репликации.</span><span class="sxs-lookup"><span data-stu-id="2fb87-105">Prepares the local store for synchronization in a particular state and retrieves the necessary information to replicate.</span></span>
  
```cpp
HRESULT SyncBeg( 
    UINT uiSync, 
    LPVOID *ppv 
);
```

## <a name="parameters"></a><span data-ttu-id="2fb87-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="2fb87-106">Parameters</span></span>

 <span data-ttu-id="2fb87-107">_Уисинк_</span><span class="sxs-lookup"><span data-stu-id="2fb87-107">_uiSync_</span></span>
  
>  <span data-ttu-id="2fb87-108">возврата Состояние, которое будет вводить локальное хранилище.</span><span class="sxs-lookup"><span data-stu-id="2fb87-108">[in] The state that the local store will enter.</span></span> <span data-ttu-id="2fb87-109">Ниже приведен список состояний идентиферс:</span><span class="sxs-lookup"><span data-stu-id="2fb87-109">The following is a list of state identifers:</span></span> 
    
<span data-ttu-id="2fb87-110">ЛР_СИНК_ИДЛЕ</span><span class="sxs-lookup"><span data-stu-id="2fb87-110">LR_SYNC_IDLE</span></span>
  
> 
    
<span data-ttu-id="2fb87-111">ЛР_СИНК</span><span class="sxs-lookup"><span data-stu-id="2fb87-111">LR_SYNC</span></span>
  
> 
    
<span data-ttu-id="2fb87-112">ЛР_СИНК_УПЛОАД_ХИЕРАРЧИ</span><span class="sxs-lookup"><span data-stu-id="2fb87-112">LR_SYNC_UPLOAD_HIERARCHY</span></span>
  
> 
    
<span data-ttu-id="2fb87-113">ЛР_СИНК_УПЛОАД_ФОЛДЕР</span><span class="sxs-lookup"><span data-stu-id="2fb87-113">LR_SYNC_UPLOAD_FOLDER</span></span>
  
> 
    
<span data-ttu-id="2fb87-114">ЛР_СИНК_КОНТЕНТС</span><span class="sxs-lookup"><span data-stu-id="2fb87-114">LR_SYNC_CONTENTS</span></span>
  
> 
    
<span data-ttu-id="2fb87-115">ЛР_СИНК_УПЛОАД_ТАБЛЕ</span><span class="sxs-lookup"><span data-stu-id="2fb87-115">LR_SYNC_UPLOAD_TABLE</span></span>
  
> 
    
<span data-ttu-id="2fb87-116">ЛР_СИНК_УПЛОАД_МЕССАЖЕ</span><span class="sxs-lookup"><span data-stu-id="2fb87-116">LR_SYNC_UPLOAD_MESSAGE</span></span>
  
> 
    
<span data-ttu-id="2fb87-117">ЛР_СИНК_УПЛОАД_МЕССАЖЕ_РЕАД</span><span class="sxs-lookup"><span data-stu-id="2fb87-117">LR_SYNC_UPLOAD_MESSAGE_READ</span></span>
  
> 
    
<span data-ttu-id="2fb87-118">ЛР_СИНК_УПЛОАД_МЕССАЖЕ_ДЕЛ</span><span class="sxs-lookup"><span data-stu-id="2fb87-118">LR_SYNC_UPLOAD_MESSAGE_DEL</span></span>
  
> 
    
<span data-ttu-id="2fb87-119">ЛР_СИНК_ДОВНЛОАД_ХИЕРАРЧИ</span><span class="sxs-lookup"><span data-stu-id="2fb87-119">LR_SYNC_DOWNLOAD_HIERARCHY</span></span>
  
> 
    
<span data-ttu-id="2fb87-120">ЛР_СИНК_ДОВНЛОАД_ТАБЛЕ</span><span class="sxs-lookup"><span data-stu-id="2fb87-120">LR_SYNC_DOWNLOAD_TABLE</span></span>
  
> 
    
 <span data-ttu-id="2fb87-121">_ППВ_</span><span class="sxs-lookup"><span data-stu-id="2fb87-121">_ppv_</span></span>
  
>  <span data-ttu-id="2fb87-122">[in]/[out] указатель на структуру данных, соответствующую состоянию, которое необходимо ввести.</span><span class="sxs-lookup"><span data-stu-id="2fb87-122">[in]/[out] Pointer to the data structure corresponding to the state to enter.</span></span> 
    
[<span data-ttu-id="2fb87-123">DNHIER</span><span class="sxs-lookup"><span data-stu-id="2fb87-123">DNHIER</span></span>](dnhier.md)
  
> 
    
[<span data-ttu-id="2fb87-124">DNTBL</span><span class="sxs-lookup"><span data-stu-id="2fb87-124">DNTBL</span></span>](dntbl.md)
  
> 
    
[<span data-ttu-id="2fb87-125">DNTBL</span><span class="sxs-lookup"><span data-stu-id="2fb87-125">DNTBL</span></span>](dntbl.md)
  
> 
    
[<span data-ttu-id="2fb87-126">Синхр</span><span class="sxs-lookup"><span data-stu-id="2fb87-126">SYNC</span></span>](sync.md)
  
> 
    
[<span data-ttu-id="2fb87-127">SYNCCONT</span><span class="sxs-lookup"><span data-stu-id="2fb87-127">SYNCCONT</span></span>](synccont.md)
  
> 
    
[<span data-ttu-id="2fb87-128">UPDEL</span><span class="sxs-lookup"><span data-stu-id="2fb87-128">UPDEL</span></span>](updel.md)
  
> 
    
[<span data-ttu-id="2fb87-129">UPDELE</span><span class="sxs-lookup"><span data-stu-id="2fb87-129">UPDELE</span></span>](updele.md)
  
> 
    
[<span data-ttu-id="2fb87-130">UPFLD</span><span class="sxs-lookup"><span data-stu-id="2fb87-130">UPFLD</span></span>](upfld.md)
  
> 
    
[<span data-ttu-id="2fb87-131">UPHIER</span><span class="sxs-lookup"><span data-stu-id="2fb87-131">UPHIER</span></span>](uphier.md)
  
> 
    
[<span data-ttu-id="2fb87-132">UPMOV</span><span class="sxs-lookup"><span data-stu-id="2fb87-132">UPMOV</span></span>](upmov.md)
  
> 
    
[<span data-ttu-id="2fb87-133">UPMSG</span><span class="sxs-lookup"><span data-stu-id="2fb87-133">UPMSG</span></span>](upmsg.md)
  
> 
    
[<span data-ttu-id="2fb87-134">UPREAD</span><span class="sxs-lookup"><span data-stu-id="2fb87-134">UPREAD</span></span>](upread.md)
  
> 
    
[<span data-ttu-id="2fb87-135">UPREADE</span><span class="sxs-lookup"><span data-stu-id="2fb87-135">UPREADE</span></span>](upreade.md)
  
> 
    
[<span data-ttu-id="2fb87-136">UPTBL</span><span class="sxs-lookup"><span data-stu-id="2fb87-136">UPTBL</span></span>](uptbl.md)
  
> 
    
[<span data-ttu-id="2fb87-137">UPTBLE</span><span class="sxs-lookup"><span data-stu-id="2fb87-137">UPTBLE</span></span>](uptble.md)
  
> 
    
## <a name="remarks"></a><span data-ttu-id="2fb87-138">Замечания</span><span class="sxs-lookup"><span data-stu-id="2fb87-138">Remarks</span></span>

<span data-ttu-id="2fb87-139">Клиент вызывает **[иосткс:: сетсинкресулт](iostx-setsyncresult.md)** , чтобы задать результат синхронизации, а затем вызывает **[Иосткс:: синценд](iostx-syncend.md)** , чтобы завершить это состояние.</span><span class="sxs-lookup"><span data-stu-id="2fb87-139">The client calls **[IOSTX::SetSyncResult](iostx-setsyncresult.md)** to set the result of the synchronization, and then calls **[IOSTX::SyncEnd](iostx-syncend.md)** to end that state.</span></span> <span data-ttu-id="2fb87-140">Клиент должен вызвать **[иосткс:: синценд](iostx-syncend.md)** для каждого вызова **Иосткс:: синкбег** для определения успешности репликации состояния.</span><span class="sxs-lookup"><span data-stu-id="2fb87-140">The client must call **[IOSTX::SyncEnd](iostx-syncend.md)** for each call to **IOSTX::SyncBeg** in order to determine whether the state has been successfully replicated.</span></span> <span data-ttu-id="2fb87-141">После того как это будет определено, Outlook может начать очистку своего внутреннего состояния.</span><span class="sxs-lookup"><span data-stu-id="2fb87-141">Once this has been determined, Outlook can begin to clean up its internal state.</span></span> 
  
<span data-ttu-id="2fb87-142">Большая часть этих структур содержит сведения [out]/[in], позволяя Outlook передавать информацию клиенту, а клиент — передавать информацию в Outlook.</span><span class="sxs-lookup"><span data-stu-id="2fb87-142">Most of these structures contain [out]/[in] information, allowing Outlook to pass information to the client, and the client to pass information to Outlook.</span></span> <span data-ttu-id="2fb87-143">Когда клиент вызывает **иосткс:: синкбег**, Outlook выделяет структуру данных для определенного состояния и инициализирует ее информацией для этого состояния.</span><span class="sxs-lookup"><span data-stu-id="2fb87-143">When the client calls **IOSTX::SyncBeg**, Outlook allocates the data structure for a given state and initializes it with information for that state.</span></span> <span data-ttu-id="2fb87-144">Сведения о [выходе].</span><span class="sxs-lookup"><span data-stu-id="2fb87-144">This is the [out] information.</span></span> <span data-ttu-id="2fb87-145">НаХодясь в состоянии, клиент обновляет соответствующую структуру данных для этого состояния.</span><span class="sxs-lookup"><span data-stu-id="2fb87-145">While in a state, the client updates the corresponding data structure for that state.</span></span> <span data-ttu-id="2fb87-146">Это сведения о [in].</span><span class="sxs-lookup"><span data-stu-id="2fb87-146">This is the [in] information.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="2fb87-147">См. также</span><span class="sxs-lookup"><span data-stu-id="2fb87-147">See also</span></span>



[<span data-ttu-id="2fb87-148">IOSTX::GetLastError</span><span class="sxs-lookup"><span data-stu-id="2fb87-148">IOSTX::GetLastError</span></span>](iostx-getlasterror.md)
  
[<span data-ttu-id="2fb87-149">IOSTX::InitSync</span><span class="sxs-lookup"><span data-stu-id="2fb87-149">IOSTX::InitSync</span></span>](iostx-initsync.md)
  
[<span data-ttu-id="2fb87-150">IOSTX::SetSyncResult</span><span class="sxs-lookup"><span data-stu-id="2fb87-150">IOSTX::SetSyncResult</span></span>](iostx-setsyncresult.md)
  
[<span data-ttu-id="2fb87-151">IOSTX::SyncEnd</span><span class="sxs-lookup"><span data-stu-id="2fb87-151">IOSTX::SyncEnd</span></span>](iostx-syncend.md)
  
[<span data-ttu-id="2fb87-152">IOSTX::SyncHdrBeg</span><span class="sxs-lookup"><span data-stu-id="2fb87-152">IOSTX::SyncHdrBeg</span></span>](iostx-synchdrbeg.md)
  
[<span data-ttu-id="2fb87-153">IOSTX::SyncHdrEnd</span><span class="sxs-lookup"><span data-stu-id="2fb87-153">IOSTX::SyncHdrEnd</span></span>](iostx-synchdrend.md)
  
[<span data-ttu-id="2fb87-154">IOSTX : IUnknown</span><span class="sxs-lookup"><span data-stu-id="2fb87-154">IOSTX : IUnknown</span></span>](iostxiunknown.md)


[<span data-ttu-id="2fb87-155">Константы MAPI</span><span class="sxs-lookup"><span data-stu-id="2fb87-155">MAPI Constants</span></span>](mapi-constants.md)

