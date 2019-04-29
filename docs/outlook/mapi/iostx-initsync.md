---
title: Иостксинитсинк
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
ms.openlocfilehash: b9086383b45d40d5839284ac785d72438be60e00
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33413355"
---
# <a name="iostxinitsync"></a><span data-ttu-id="85c25-103">IOSTX::InitSync</span><span class="sxs-lookup"><span data-stu-id="85c25-103">IOSTX::InitSync</span></span>

  
  
<span data-ttu-id="85c25-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="85c25-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="85c25-105">Информирует локальное хранилище сообщений о том, что синхронизация будет запущена.</span><span class="sxs-lookup"><span data-stu-id="85c25-105">Informs the local message store that synchronization is about to start.</span></span>
  
```cpp
HRESULT InitSync( 
    ULONG ulFlags 
);
```

## <a name="parameters"></a><span data-ttu-id="85c25-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="85c25-106">Parameters</span></span>

 <span data-ttu-id="85c25-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="85c25-107">_ulFlags_</span></span>
  
> <span data-ttu-id="85c25-108">возврата Флаги для определения надлежащего поведения во время синхронизации.</span><span class="sxs-lookup"><span data-stu-id="85c25-108">[in] Flags to determine appropriate behavior during synchronization.</span></span> <span data-ttu-id="85c25-109">Outlook использует эти флаги в каждом состоянии конечного автомата репликации, чтобы определить сведения, которые он должен предоставить для клиента.</span><span class="sxs-lookup"><span data-stu-id="85c25-109">Outlook uses these flags in each state of the replication state machine to determine the information that it should provide for the client.</span></span> <span data-ttu-id="85c25-110">Например, если клиент передает **синк_онли_ассоЦиатед**, Outlook будет возвращать только сведения, относящиеся к связанным (или скрытым) элементам.</span><span class="sxs-lookup"><span data-stu-id="85c25-110">For example, if the client passes **SYNC_ONLY_ASSOCIATED**, Outlook will only return information related to associated (or hidden) items.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="85c25-111">См. также</span><span class="sxs-lookup"><span data-stu-id="85c25-111">See also</span></span>



[<span data-ttu-id="85c25-112">IOSTX::GetLastError</span><span class="sxs-lookup"><span data-stu-id="85c25-112">IOSTX::GetLastError</span></span>](iostx-getlasterror.md)
  
[<span data-ttu-id="85c25-113">IOSTX::SetSyncResult</span><span class="sxs-lookup"><span data-stu-id="85c25-113">IOSTX::SetSyncResult</span></span>](iostx-setsyncresult.md)
  
[<span data-ttu-id="85c25-114">IOSTX::SyncBeg</span><span class="sxs-lookup"><span data-stu-id="85c25-114">IOSTX::SyncBeg</span></span>](iostx-syncbeg.md)
  
[<span data-ttu-id="85c25-115">IOSTX::SyncEnd</span><span class="sxs-lookup"><span data-stu-id="85c25-115">IOSTX::SyncEnd</span></span>](iostx-syncend.md)
  
[<span data-ttu-id="85c25-116">IOSTX::SyncHdrBeg</span><span class="sxs-lookup"><span data-stu-id="85c25-116">IOSTX::SyncHdrBeg</span></span>](iostx-synchdrbeg.md)
  
[<span data-ttu-id="85c25-117">IOSTX::SyncHdrEnd</span><span class="sxs-lookup"><span data-stu-id="85c25-117">IOSTX::SyncHdrEnd</span></span>](iostx-synchdrend.md)
  
[<span data-ttu-id="85c25-118">IOSTX : IUnknown</span><span class="sxs-lookup"><span data-stu-id="85c25-118">IOSTX : IUnknown</span></span>](iostxiunknown.md)


[<span data-ttu-id="85c25-119">Константы MAPI</span><span class="sxs-lookup"><span data-stu-id="85c25-119">MAPI Constants</span></span>](mapi-constants.md)

