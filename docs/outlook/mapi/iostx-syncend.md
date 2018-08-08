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
ms.openlocfilehash: 66542d2cc7600ecbcd8de9043b6b40559744c2ad
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19809472"
---
# <a name="iostxsyncend"></a><span data-ttu-id="7610c-103">IOSTX::SyncEnd</span><span class="sxs-lookup"><span data-stu-id="7610c-103">IOSTX::SyncEnd</span></span>

  
  
<span data-ttu-id="7610c-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="7610c-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="7610c-105">Завершает синхронизации в текущем состоянии и выходе из этого состояния.</span><span class="sxs-lookup"><span data-stu-id="7610c-105">Ends synchronization in the current state and exits that state.</span></span>
  
```cpp
HRESULT SyncEnd();
```

## <a name="remarks"></a><span data-ttu-id="7610c-106">Замечания</span><span class="sxs-lookup"><span data-stu-id="7610c-106">Remarks</span></span>

<span data-ttu-id="7610c-107">Клиент должен вызывать **IOSTX::SyncEnd** для каждого вызова [IOSTX::SyncBeg](iostx-syncbeg.md).</span><span class="sxs-lookup"><span data-stu-id="7610c-107">The client must call **IOSTX::SyncEnd** for each call to [IOSTX::SyncBeg](iostx-syncbeg.md).</span></span> <span data-ttu-id="7610c-108">Соответствующий структура данных содержит сведения, которые указывают ли клиент успешного завершения текущего состояния, Outlook может Очистка внутреннего состояния.</span><span class="sxs-lookup"><span data-stu-id="7610c-108">The corresponding data structure holds information to indicate whether the client has successfully completed the current state so that Outlook can clean up its internal state.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="7610c-109">См. также</span><span class="sxs-lookup"><span data-stu-id="7610c-109">See also</span></span>



[<span data-ttu-id="7610c-110">IOSTX::GetLastError</span><span class="sxs-lookup"><span data-stu-id="7610c-110">IOSTX::GetLastError</span></span>](iostx-getlasterror.md)
  
[<span data-ttu-id="7610c-111">IOSTX::InitSync</span><span class="sxs-lookup"><span data-stu-id="7610c-111">IOSTX::InitSync</span></span>](iostx-initsync.md)
  
[<span data-ttu-id="7610c-112">IOSTX::SetSyncResult</span><span class="sxs-lookup"><span data-stu-id="7610c-112">IOSTX::SetSyncResult</span></span>](iostx-setsyncresult.md)
  
[<span data-ttu-id="7610c-113">IOSTX::SyncBeg</span><span class="sxs-lookup"><span data-stu-id="7610c-113">IOSTX::SyncBeg</span></span>](iostx-syncbeg.md)
  
[<span data-ttu-id="7610c-114">IOSTX::SyncHdrBeg</span><span class="sxs-lookup"><span data-stu-id="7610c-114">IOSTX::SyncHdrBeg</span></span>](iostx-synchdrbeg.md)
  
[<span data-ttu-id="7610c-115">IOSTX::SyncHdrEnd</span><span class="sxs-lookup"><span data-stu-id="7610c-115">IOSTX::SyncHdrEnd</span></span>](iostx-synchdrend.md)
  
[<span data-ttu-id="7610c-116">IOSTX : IUnknown</span><span class="sxs-lookup"><span data-stu-id="7610c-116">IOSTX : IUnknown</span></span>](iostxiunknown.md)


[<span data-ttu-id="7610c-117">��������� MAPI</span><span class="sxs-lookup"><span data-stu-id="7610c-117">MAPI Constants</span></span>](mapi-constants.md)

