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
ms.openlocfilehash: 74a4e299da6c0637c3da70c329569266d43dbd9a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19809463"
---
# <a name="iostxsetsyncresult"></a><span data-ttu-id="8ed15-103">IOSTX::SetSyncResult</span><span class="sxs-lookup"><span data-stu-id="8ed15-103">IOSTX::SetSyncResult</span></span>

  
  
<span data-ttu-id="8ed15-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="8ed15-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="8ed15-105">Задает в результате синхронизации.</span><span class="sxs-lookup"><span data-stu-id="8ed15-105">Sets the result of the synchronization.</span></span>
  
```cpp
HRESULT SetSyncResult( 
    HRESULT hrSync 
);
```

## <a name="parameters"></a><span data-ttu-id="8ed15-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="8ed15-106">Parameters</span></span>

 <span data-ttu-id="8ed15-107">_hrSync_</span><span class="sxs-lookup"><span data-stu-id="8ed15-107">_hrSync_</span></span>
  
>  <span data-ttu-id="8ed15-108">[in] В результате синхронизации.</span><span class="sxs-lookup"><span data-stu-id="8ed15-108">[in] The result of the synchronization.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="8ed15-109">Замечания</span><span class="sxs-lookup"><span data-stu-id="8ed15-109">Remarks</span></span>

<span data-ttu-id="8ed15-110">Вызовите **IOSTX::SetSyncResult** перед вызовом **IOSTX::SyncEnd** для оповещения локального хранилища в результате синхронизации.</span><span class="sxs-lookup"><span data-stu-id="8ed15-110">Call **IOSTX::SetSyncResult** before calling **IOSTX::SyncEnd** to inform the local store of the result of synchronization.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="8ed15-111">См. также</span><span class="sxs-lookup"><span data-stu-id="8ed15-111">See also</span></span>



[<span data-ttu-id="8ed15-112">IOSTX::GetLastError</span><span class="sxs-lookup"><span data-stu-id="8ed15-112">IOSTX::GetLastError</span></span>](iostx-getlasterror.md)
  
[<span data-ttu-id="8ed15-113">IOSTX::InitSync</span><span class="sxs-lookup"><span data-stu-id="8ed15-113">IOSTX::InitSync</span></span>](iostx-initsync.md)
  
[<span data-ttu-id="8ed15-114">IOSTX::SyncBeg</span><span class="sxs-lookup"><span data-stu-id="8ed15-114">IOSTX::SyncBeg</span></span>](iostx-syncbeg.md)
  
[<span data-ttu-id="8ed15-115">IOSTX::SyncEnd</span><span class="sxs-lookup"><span data-stu-id="8ed15-115">IOSTX::SyncEnd</span></span>](iostx-syncend.md)
  
[<span data-ttu-id="8ed15-116">IOSTX::SyncHdrBeg</span><span class="sxs-lookup"><span data-stu-id="8ed15-116">IOSTX::SyncHdrBeg</span></span>](iostx-synchdrbeg.md)
  
[<span data-ttu-id="8ed15-117">IOSTX::SyncHdrEnd</span><span class="sxs-lookup"><span data-stu-id="8ed15-117">IOSTX::SyncHdrEnd</span></span>](iostx-synchdrend.md)


[<span data-ttu-id="8ed15-118">��������� MAPI</span><span class="sxs-lookup"><span data-stu-id="8ed15-118">MAPI Constants</span></span>](mapi-constants.md)

