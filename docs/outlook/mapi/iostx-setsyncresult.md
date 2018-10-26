---
title: IOSTXSetSyncResult
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IOSTX.SetSyncResult
api_type:
- COM
ms.assetid: 7f083ee0-bf36-0059-1589-66e454fe0098
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: f8982bafc0678378ae46dc31a9417cc11bb695a7
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22563074"
---
# <a name="iostxsetsyncresult"></a><span data-ttu-id="e2c42-103">IOSTX::SetSyncResult</span><span class="sxs-lookup"><span data-stu-id="e2c42-103">IOSTX::SetSyncResult</span></span>

  
  
<span data-ttu-id="e2c42-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e2c42-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e2c42-105">Задает в результате синхронизации.</span><span class="sxs-lookup"><span data-stu-id="e2c42-105">Sets the result of the synchronization.</span></span>
  
```cpp
HRESULT SetSyncResult( 
    HRESULT hrSync 
);
```

## <a name="parameters"></a><span data-ttu-id="e2c42-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="e2c42-106">Parameters</span></span>

 <span data-ttu-id="e2c42-107">_hrSync_</span><span class="sxs-lookup"><span data-stu-id="e2c42-107">_hrSync_</span></span>
  
>  <span data-ttu-id="e2c42-108">[in] В результате синхронизации.</span><span class="sxs-lookup"><span data-stu-id="e2c42-108">[in] The result of the synchronization.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="e2c42-109">Замечания</span><span class="sxs-lookup"><span data-stu-id="e2c42-109">Remarks</span></span>

<span data-ttu-id="e2c42-110">Вызовите **IOSTX::SetSyncResult** перед вызовом **IOSTX::SyncEnd** для оповещения локального хранилища в результате синхронизации.</span><span class="sxs-lookup"><span data-stu-id="e2c42-110">Call **IOSTX::SetSyncResult** before calling **IOSTX::SyncEnd** to inform the local store of the result of synchronization.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="e2c42-111">См. также</span><span class="sxs-lookup"><span data-stu-id="e2c42-111">See also</span></span>



[<span data-ttu-id="e2c42-112">IOSTX::GetLastError</span><span class="sxs-lookup"><span data-stu-id="e2c42-112">IOSTX::GetLastError</span></span>](iostx-getlasterror.md)
  
[<span data-ttu-id="e2c42-113">IOSTX::InitSync</span><span class="sxs-lookup"><span data-stu-id="e2c42-113">IOSTX::InitSync</span></span>](iostx-initsync.md)
  
[<span data-ttu-id="e2c42-114">IOSTX::SyncBeg</span><span class="sxs-lookup"><span data-stu-id="e2c42-114">IOSTX::SyncBeg</span></span>](iostx-syncbeg.md)
  
[<span data-ttu-id="e2c42-115">IOSTX::SyncEnd</span><span class="sxs-lookup"><span data-stu-id="e2c42-115">IOSTX::SyncEnd</span></span>](iostx-syncend.md)
  
[<span data-ttu-id="e2c42-116">IOSTX::SyncHdrBeg</span><span class="sxs-lookup"><span data-stu-id="e2c42-116">IOSTX::SyncHdrBeg</span></span>](iostx-synchdrbeg.md)
  
[<span data-ttu-id="e2c42-117">IOSTX::SyncHdrEnd</span><span class="sxs-lookup"><span data-stu-id="e2c42-117">IOSTX::SyncHdrEnd</span></span>](iostx-synchdrend.md)


[<span data-ttu-id="e2c42-118">Константы MAPI</span><span class="sxs-lookup"><span data-stu-id="e2c42-118">MAPI Constants</span></span>](mapi-constants.md)

