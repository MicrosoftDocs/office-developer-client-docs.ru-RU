---
title: IOSTXSyncHdrEnd
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IOSTX.SyncHdrEnd
api_type:
- COM
ms.assetid: a0beb6eb-7978-c64e-dba1-89f0caf2090e
description: 'Last modified: July 03, 2012'
ms.openlocfilehash: 864c2d2dfd17c285b0d8a401d59ce5b7d0463864
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33432774"
---
# <a name="iostxsynchdrend"></a><span data-ttu-id="72744-103">IOSTX::SyncHdrEnd</span><span class="sxs-lookup"><span data-stu-id="72744-103">IOSTX::SyncHdrEnd</span></span>

 
  
<span data-ttu-id="72744-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="72744-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="72744-105">Завершает синхронизацию для загона сообщения.</span><span class="sxs-lookup"><span data-stu-id="72744-105">Ends synchronization for a message header.</span></span>
  
```cpp
HRESULT SyncHdrEnd( 
    LPMAPIPROGRESS pprog 
);
```

## <a name="parameters"></a><span data-ttu-id="72744-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="72744-106">Parameters</span></span>

 <span data-ttu-id="72744-107">_pp де_</span><span class="sxs-lookup"><span data-stu-id="72744-107">_pprog_</span></span>
  
> <span data-ttu-id="72744-108">[in] **[Интерфейс IMAPIProgress](imapiprogressiunknown.md)** для синхронизации перемещенных или скопированные сообщения.</span><span class="sxs-lookup"><span data-stu-id="72744-108">[in] **[IMAPIProgress](imapiprogressiunknown.md)** interface for synchronization of moved or copied messages.</span></span> <span data-ttu-id="72744-109">Определение типа **LPMAPIPROGRESS** см. в mapidefs.h.</span><span class="sxs-lookup"><span data-stu-id="72744-109">See mapidefs.h for the type definition of **LPMAPIPROGRESS**.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="72744-110">Примечания</span><span class="sxs-lookup"><span data-stu-id="72744-110">Remarks</span></span>

<span data-ttu-id="72744-111">После **[IOSTX::SyncBeg](iostx-syncbeg.md)** локальное хранилище введет состояние [скачивания сообщения в состояние загона.](download-message-header-state.md)</span><span class="sxs-lookup"><span data-stu-id="72744-111">Upon **[IOSTX::SyncBeg](iostx-syncbeg.md)**, the local store enters the [download message header state](download-message-header-state.md).</span></span> <span data-ttu-id="72744-112">Клиент скачивает полный элемент сообщения (как *pmsgFull* в **[HDRSYNC).](hdrsync.md)**</span><span class="sxs-lookup"><span data-stu-id="72744-112">The client downloads a full message item (as  *pmsgFull*  in **[HDRSYNC](hdrsync.md)** ).</span></span> <span data-ttu-id="72744-113">Если это успешно, клиент также устанавливает *ulFlags* в **HDRSYNC** как **HSF_OK.**</span><span class="sxs-lookup"><span data-stu-id="72744-113">If this is successful, the client also sets  *ulFlags*  in **HDRSYNC** as **HSF_OK**.</span></span> <span data-ttu-id="72744-114">После **IOSTX::SyncHdrEnd** Outlook проверяет результат в **HDRSYNC** и использует  *ppлага*  и сведения в **HDRSYNC** для обновления локального заголовка сообщения.</span><span class="sxs-lookup"><span data-stu-id="72744-114">Upon **IOSTX::SyncHdrEnd**, Outlook checks the result in **HDRSYNC** and uses  *pprog*  and the information in **HDRSYNC** to update the local message header.</span></span> 
  
<span data-ttu-id="72744-115">Локальное хранилище возвращается в состояние до предыдущего **[IOSTX::SyncHdrBeg](iostx-synchdrbeg.md)**.</span><span class="sxs-lookup"><span data-stu-id="72744-115">The local store returns to the state it was in before the preceding **[IOSTX::SyncHdrBeg](iostx-synchdrbeg.md)**.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="72744-116">См. также</span><span class="sxs-lookup"><span data-stu-id="72744-116">See also</span></span>



[<span data-ttu-id="72744-117">IOSTX::GetLastError</span><span class="sxs-lookup"><span data-stu-id="72744-117">IOSTX::GetLastError</span></span>](iostx-getlasterror.md)
  
[<span data-ttu-id="72744-118">IOSTX::InitSync</span><span class="sxs-lookup"><span data-stu-id="72744-118">IOSTX::InitSync</span></span>](iostx-initsync.md)
  
[<span data-ttu-id="72744-119">IOSTX::SetSyncResult</span><span class="sxs-lookup"><span data-stu-id="72744-119">IOSTX::SetSyncResult</span></span>](iostx-setsyncresult.md)
  
[<span data-ttu-id="72744-120">IOSTX::SyncBeg</span><span class="sxs-lookup"><span data-stu-id="72744-120">IOSTX::SyncBeg</span></span>](iostx-syncbeg.md)
  
[<span data-ttu-id="72744-121">IOSTX::SyncEnd</span><span class="sxs-lookup"><span data-stu-id="72744-121">IOSTX::SyncEnd</span></span>](iostx-syncend.md)
  
[<span data-ttu-id="72744-122">IOSTX::SyncHdrBeg</span><span class="sxs-lookup"><span data-stu-id="72744-122">IOSTX::SyncHdrBeg</span></span>](iostx-synchdrbeg.md)
  
[<span data-ttu-id="72744-123">IOSTX : IUnknown</span><span class="sxs-lookup"><span data-stu-id="72744-123">IOSTX : IUnknown</span></span>](iostxiunknown.md)


[<span data-ttu-id="72744-124">Константы MAPI</span><span class="sxs-lookup"><span data-stu-id="72744-124">MAPI Constants</span></span>](mapi-constants.md)

