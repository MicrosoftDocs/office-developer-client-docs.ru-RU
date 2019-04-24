---
title: Иосткссетсинкресулт
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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32332146"
---
# <a name="iostxsetsyncresult"></a><span data-ttu-id="8c91a-103">IOSTX::SetSyncResult</span><span class="sxs-lookup"><span data-stu-id="8c91a-103">IOSTX::SetSyncResult</span></span>

  
  
<span data-ttu-id="8c91a-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8c91a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8c91a-105">Задает результат синхронизации.</span><span class="sxs-lookup"><span data-stu-id="8c91a-105">Sets the result of the synchronization.</span></span>
  
```cpp
HRESULT SetSyncResult( 
    HRESULT hrSync 
);
```

## <a name="parameters"></a><span data-ttu-id="8c91a-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="8c91a-106">Parameters</span></span>

 <span data-ttu-id="8c91a-107">_Хрсинк_</span><span class="sxs-lookup"><span data-stu-id="8c91a-107">_hrSync_</span></span>
  
>  <span data-ttu-id="8c91a-108">возврата Результат синхронизации.</span><span class="sxs-lookup"><span data-stu-id="8c91a-108">[in] The result of the synchronization.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="8c91a-109">Комментарии</span><span class="sxs-lookup"><span data-stu-id="8c91a-109">Remarks</span></span>

<span data-ttu-id="8c91a-110">Call **иосткс:: сетсинкресулт** перед вызовом **Иосткс:: синценд** для информирования локального хранилища о результатах синхронизации.</span><span class="sxs-lookup"><span data-stu-id="8c91a-110">Call **IOSTX::SetSyncResult** before calling **IOSTX::SyncEnd** to inform the local store of the result of synchronization.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="8c91a-111">См. также</span><span class="sxs-lookup"><span data-stu-id="8c91a-111">See also</span></span>



[<span data-ttu-id="8c91a-112">IOSTX::GetLastError</span><span class="sxs-lookup"><span data-stu-id="8c91a-112">IOSTX::GetLastError</span></span>](iostx-getlasterror.md)
  
[<span data-ttu-id="8c91a-113">IOSTX::InitSync</span><span class="sxs-lookup"><span data-stu-id="8c91a-113">IOSTX::InitSync</span></span>](iostx-initsync.md)
  
[<span data-ttu-id="8c91a-114">IOSTX::SyncBeg</span><span class="sxs-lookup"><span data-stu-id="8c91a-114">IOSTX::SyncBeg</span></span>](iostx-syncbeg.md)
  
[<span data-ttu-id="8c91a-115">IOSTX::SyncEnd</span><span class="sxs-lookup"><span data-stu-id="8c91a-115">IOSTX::SyncEnd</span></span>](iostx-syncend.md)
  
[<span data-ttu-id="8c91a-116">IOSTX::SyncHdrBeg</span><span class="sxs-lookup"><span data-stu-id="8c91a-116">IOSTX::SyncHdrBeg</span></span>](iostx-synchdrbeg.md)
  
[<span data-ttu-id="8c91a-117">IOSTX::SyncHdrEnd</span><span class="sxs-lookup"><span data-stu-id="8c91a-117">IOSTX::SyncHdrEnd</span></span>](iostx-synchdrend.md)


[<span data-ttu-id="8c91a-118">Константы MAPI</span><span class="sxs-lookup"><span data-stu-id="8c91a-118">MAPI Constants</span></span>](mapi-constants.md)

