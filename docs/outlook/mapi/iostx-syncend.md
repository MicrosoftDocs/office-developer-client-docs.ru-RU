---
title: Иосткссинценд
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
ms.openlocfilehash: 364914df1c5897241dfeb89cce2cc3c62018ce24
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32332153"
---
# <a name="iostxsyncend"></a><span data-ttu-id="40dff-103">IOSTX::SyncEnd</span><span class="sxs-lookup"><span data-stu-id="40dff-103">IOSTX::SyncEnd</span></span>

  
  
<span data-ttu-id="40dff-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="40dff-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="40dff-105">Завершает синхронизацию в текущем состоянии и выходит из этого состояния.</span><span class="sxs-lookup"><span data-stu-id="40dff-105">Ends synchronization in the current state and exits that state.</span></span>
  
```cpp
HRESULT SyncEnd();
```

## <a name="remarks"></a><span data-ttu-id="40dff-106">Комментарии</span><span class="sxs-lookup"><span data-stu-id="40dff-106">Remarks</span></span>

<span data-ttu-id="40dff-107">Клиент должен вызвать **иосткс:: синценд** для каждого вызова [Иосткс:: синкбег](iostx-syncbeg.md).</span><span class="sxs-lookup"><span data-stu-id="40dff-107">The client must call **IOSTX::SyncEnd** for each call to [IOSTX::SyncBeg](iostx-syncbeg.md).</span></span> <span data-ttu-id="40dff-108">Соответствующая структура данных содержит сведения, указывающие, успешно ли клиент завершил текущее состояние, чтобы Outlook мог очистить его внутреннее состояние.</span><span class="sxs-lookup"><span data-stu-id="40dff-108">The corresponding data structure holds information to indicate whether the client has successfully completed the current state so that Outlook can clean up its internal state.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="40dff-109">См. также</span><span class="sxs-lookup"><span data-stu-id="40dff-109">See also</span></span>



[<span data-ttu-id="40dff-110">IOSTX::GetLastError</span><span class="sxs-lookup"><span data-stu-id="40dff-110">IOSTX::GetLastError</span></span>](iostx-getlasterror.md)
  
[<span data-ttu-id="40dff-111">IOSTX::InitSync</span><span class="sxs-lookup"><span data-stu-id="40dff-111">IOSTX::InitSync</span></span>](iostx-initsync.md)
  
[<span data-ttu-id="40dff-112">IOSTX::SetSyncResult</span><span class="sxs-lookup"><span data-stu-id="40dff-112">IOSTX::SetSyncResult</span></span>](iostx-setsyncresult.md)
  
[<span data-ttu-id="40dff-113">IOSTX::SyncBeg</span><span class="sxs-lookup"><span data-stu-id="40dff-113">IOSTX::SyncBeg</span></span>](iostx-syncbeg.md)
  
[<span data-ttu-id="40dff-114">IOSTX::SyncHdrBeg</span><span class="sxs-lookup"><span data-stu-id="40dff-114">IOSTX::SyncHdrBeg</span></span>](iostx-synchdrbeg.md)
  
[<span data-ttu-id="40dff-115">IOSTX::SyncHdrEnd</span><span class="sxs-lookup"><span data-stu-id="40dff-115">IOSTX::SyncHdrEnd</span></span>](iostx-synchdrend.md)
  
[<span data-ttu-id="40dff-116">IOSTX : IUnknown</span><span class="sxs-lookup"><span data-stu-id="40dff-116">IOSTX : IUnknown</span></span>](iostxiunknown.md)


[<span data-ttu-id="40dff-117">Константы MAPI</span><span class="sxs-lookup"><span data-stu-id="40dff-117">MAPI Constants</span></span>](mapi-constants.md)

