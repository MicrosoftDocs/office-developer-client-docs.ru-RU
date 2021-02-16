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
ms.openlocfilehash: 78ccf72f17ec350d77f2d22d0e6d2fa7c3d97543
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33432872"
---
# <a name="iostxsetsyncresult"></a><span data-ttu-id="60fd4-103">IOSTX::SetSyncResult</span><span class="sxs-lookup"><span data-stu-id="60fd4-103">IOSTX::SetSyncResult</span></span>

  
  
<span data-ttu-id="60fd4-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="60fd4-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="60fd4-105">Задает результат синхронизации.</span><span class="sxs-lookup"><span data-stu-id="60fd4-105">Sets the result of the synchronization.</span></span>
  
```cpp
HRESULT SetSyncResult( 
    HRESULT hrSync 
);
```

## <a name="parameters"></a><span data-ttu-id="60fd4-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="60fd4-106">Parameters</span></span>

 <span data-ttu-id="60fd4-107">_hrSync_</span><span class="sxs-lookup"><span data-stu-id="60fd4-107">_hrSync_</span></span>
  
>  <span data-ttu-id="60fd4-108">[in] Результат синхронизации.</span><span class="sxs-lookup"><span data-stu-id="60fd4-108">[in] The result of the synchronization.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="60fd4-109">Примечания</span><span class="sxs-lookup"><span data-stu-id="60fd4-109">Remarks</span></span>

<span data-ttu-id="60fd4-110">Вызовите **IOSTX::SetSyncResult** перед вызовом **IOSTX::SyncEnd,** чтобы сообщить локальному хранилище о результате синхронизации.</span><span class="sxs-lookup"><span data-stu-id="60fd4-110">Call **IOSTX::SetSyncResult** before calling **IOSTX::SyncEnd** to inform the local store of the result of synchronization.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="60fd4-111">См. также</span><span class="sxs-lookup"><span data-stu-id="60fd4-111">See also</span></span>



[<span data-ttu-id="60fd4-112">IOSTX::GetLastError</span><span class="sxs-lookup"><span data-stu-id="60fd4-112">IOSTX::GetLastError</span></span>](iostx-getlasterror.md)
  
[<span data-ttu-id="60fd4-113">IOSTX::InitSync</span><span class="sxs-lookup"><span data-stu-id="60fd4-113">IOSTX::InitSync</span></span>](iostx-initsync.md)
  
[<span data-ttu-id="60fd4-114">IOSTX::SyncBeg</span><span class="sxs-lookup"><span data-stu-id="60fd4-114">IOSTX::SyncBeg</span></span>](iostx-syncbeg.md)
  
[<span data-ttu-id="60fd4-115">IOSTX::SyncEnd</span><span class="sxs-lookup"><span data-stu-id="60fd4-115">IOSTX::SyncEnd</span></span>](iostx-syncend.md)
  
[<span data-ttu-id="60fd4-116">IOSTX::SyncHdrBeg</span><span class="sxs-lookup"><span data-stu-id="60fd4-116">IOSTX::SyncHdrBeg</span></span>](iostx-synchdrbeg.md)
  
[<span data-ttu-id="60fd4-117">IOSTX::SyncHdrEnd</span><span class="sxs-lookup"><span data-stu-id="60fd4-117">IOSTX::SyncHdrEnd</span></span>](iostx-synchdrend.md)


[<span data-ttu-id="60fd4-118">Константы MAPI</span><span class="sxs-lookup"><span data-stu-id="60fd4-118">MAPI Constants</span></span>](mapi-constants.md)

