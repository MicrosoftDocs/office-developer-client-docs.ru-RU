---
title: IOSTXInitSync
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IOSTX.InitSync
api_type:
- COM
ms.assetid: e22244a2-ac5f-910a-501f-4483ea0667c2
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 5a0632ffd892c08fdf19de2c9b34607c27534f19
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22594042"
---
# <a name="iostxinitsync"></a><span data-ttu-id="b74e5-103">IOSTX::InitSync</span><span class="sxs-lookup"><span data-stu-id="b74e5-103">IOSTX::InitSync</span></span>

  
  
<span data-ttu-id="b74e5-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b74e5-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b74e5-105">Информирует хранилище локального сообщений, что синхронизация является запуск.</span><span class="sxs-lookup"><span data-stu-id="b74e5-105">Informs the local message store that synchronization is about to start.</span></span>
  
```cpp
HRESULT InitSync( 
    ULONG ulFlags 
);
```

## <a name="parameters"></a><span data-ttu-id="b74e5-106">���������</span><span class="sxs-lookup"><span data-stu-id="b74e5-106">Parameters</span></span>

 <span data-ttu-id="b74e5-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="b74e5-107">_ulFlags_</span></span>
  
> <span data-ttu-id="b74e5-108">[in] Флаги для определения соответствующего поведения при синхронизации.</span><span class="sxs-lookup"><span data-stu-id="b74e5-108">[in] Flags to determine appropriate behavior during synchronization.</span></span> <span data-ttu-id="b74e5-109">Outlook использует эти флаги в каждом состояние конечного автомата репликации, чтобы определить сведения, которые следует предоставить для клиента.</span><span class="sxs-lookup"><span data-stu-id="b74e5-109">Outlook uses these flags in each state of the replication state machine to determine the information that it should provide for the client.</span></span> <span data-ttu-id="b74e5-110">Например если клиент передает **SYNC_ONLY_ASSOCIATED**, Outlook будет возвращать только данные, связанные с элементами связанные (или скрытых).</span><span class="sxs-lookup"><span data-stu-id="b74e5-110">For example, if the client passes **SYNC_ONLY_ASSOCIATED**, Outlook will only return information related to associated (or hidden) items.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="b74e5-111">См. также</span><span class="sxs-lookup"><span data-stu-id="b74e5-111">See also</span></span>



[<span data-ttu-id="b74e5-112">IOSTX::GetLastError</span><span class="sxs-lookup"><span data-stu-id="b74e5-112">IOSTX::GetLastError</span></span>](iostx-getlasterror.md)
  
[<span data-ttu-id="b74e5-113">IOSTX::SetSyncResult</span><span class="sxs-lookup"><span data-stu-id="b74e5-113">IOSTX::SetSyncResult</span></span>](iostx-setsyncresult.md)
  
[<span data-ttu-id="b74e5-114">IOSTX::SyncBeg</span><span class="sxs-lookup"><span data-stu-id="b74e5-114">IOSTX::SyncBeg</span></span>](iostx-syncbeg.md)
  
[<span data-ttu-id="b74e5-115">IOSTX::SyncEnd</span><span class="sxs-lookup"><span data-stu-id="b74e5-115">IOSTX::SyncEnd</span></span>](iostx-syncend.md)
  
[<span data-ttu-id="b74e5-116">IOSTX::SyncHdrBeg</span><span class="sxs-lookup"><span data-stu-id="b74e5-116">IOSTX::SyncHdrBeg</span></span>](iostx-synchdrbeg.md)
  
[<span data-ttu-id="b74e5-117">IOSTX::SyncHdrEnd</span><span class="sxs-lookup"><span data-stu-id="b74e5-117">IOSTX::SyncHdrEnd</span></span>](iostx-synchdrend.md)
  
[<span data-ttu-id="b74e5-118">IOSTX : IUnknown</span><span class="sxs-lookup"><span data-stu-id="b74e5-118">IOSTX : IUnknown</span></span>](iostxiunknown.md)


[<span data-ttu-id="b74e5-119">Константы MAPI</span><span class="sxs-lookup"><span data-stu-id="b74e5-119">MAPI Constants</span></span>](mapi-constants.md)

