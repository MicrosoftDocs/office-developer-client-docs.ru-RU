---
title: IOSTXSyncEnd
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IOSTX.SyncEnd
api_type:
- COM
ms.assetid: da9de705-bdab-6cb8-35ea-61f03cdc4ff5
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: fd5b2ed23eba30cbe861a20c4fd100cb8ea1aeb0
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22568842"
---
# <a name="iostxsyncend"></a><span data-ttu-id="b8f0a-103">IOSTX::SyncEnd</span><span class="sxs-lookup"><span data-stu-id="b8f0a-103">IOSTX::SyncEnd</span></span>

  
  
<span data-ttu-id="b8f0a-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b8f0a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b8f0a-105">Завершает синхронизации в текущем состоянии и выходе из этого состояния.</span><span class="sxs-lookup"><span data-stu-id="b8f0a-105">Ends synchronization in the current state and exits that state.</span></span>
  
```cpp
HRESULT SyncEnd();
```

## <a name="remarks"></a><span data-ttu-id="b8f0a-106">Примечания</span><span class="sxs-lookup"><span data-stu-id="b8f0a-106">Remarks</span></span>

<span data-ttu-id="b8f0a-107">Клиент должен вызывать **IOSTX::SyncEnd** для каждого вызова [IOSTX::SyncBeg](iostx-syncbeg.md).</span><span class="sxs-lookup"><span data-stu-id="b8f0a-107">The client must call **IOSTX::SyncEnd** for each call to [IOSTX::SyncBeg](iostx-syncbeg.md).</span></span> <span data-ttu-id="b8f0a-108">Соответствующий структура данных содержит сведения, которые указывают ли клиент успешного завершения текущего состояния, Outlook может Очистка внутреннего состояния.</span><span class="sxs-lookup"><span data-stu-id="b8f0a-108">The corresponding data structure holds information to indicate whether the client has successfully completed the current state so that Outlook can clean up its internal state.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="b8f0a-109">См. также</span><span class="sxs-lookup"><span data-stu-id="b8f0a-109">See also</span></span>



[<span data-ttu-id="b8f0a-110">IOSTX::GetLastError</span><span class="sxs-lookup"><span data-stu-id="b8f0a-110">IOSTX::GetLastError</span></span>](iostx-getlasterror.md)
  
[<span data-ttu-id="b8f0a-111">IOSTX::InitSync</span><span class="sxs-lookup"><span data-stu-id="b8f0a-111">IOSTX::InitSync</span></span>](iostx-initsync.md)
  
[<span data-ttu-id="b8f0a-112">IOSTX::SetSyncResult</span><span class="sxs-lookup"><span data-stu-id="b8f0a-112">IOSTX::SetSyncResult</span></span>](iostx-setsyncresult.md)
  
[<span data-ttu-id="b8f0a-113">IOSTX::SyncBeg</span><span class="sxs-lookup"><span data-stu-id="b8f0a-113">IOSTX::SyncBeg</span></span>](iostx-syncbeg.md)
  
[<span data-ttu-id="b8f0a-114">IOSTX::SyncHdrBeg</span><span class="sxs-lookup"><span data-stu-id="b8f0a-114">IOSTX::SyncHdrBeg</span></span>](iostx-synchdrbeg.md)
  
[<span data-ttu-id="b8f0a-115">IOSTX::SyncHdrEnd</span><span class="sxs-lookup"><span data-stu-id="b8f0a-115">IOSTX::SyncHdrEnd</span></span>](iostx-synchdrend.md)
  
[<span data-ttu-id="b8f0a-116">IOSTX : IUnknown</span><span class="sxs-lookup"><span data-stu-id="b8f0a-116">IOSTX : IUnknown</span></span>](iostxiunknown.md)


[<span data-ttu-id="b8f0a-117">Константы MAPI</span><span class="sxs-lookup"><span data-stu-id="b8f0a-117">MAPI Constants</span></span>](mapi-constants.md)

