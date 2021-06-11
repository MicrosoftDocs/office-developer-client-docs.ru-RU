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
description: 'Последнее изменение: 03 июля 2012 г.'
ms.openlocfilehash: 864c2d2dfd17c285b0d8a401d59ce5b7d0463864
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33432774"
---
# <a name="iostxsynchdrend"></a><span data-ttu-id="0442b-103">IOSTX::SyncHdrEnd</span><span class="sxs-lookup"><span data-stu-id="0442b-103">IOSTX::SyncHdrEnd</span></span>

 
  
<span data-ttu-id="0442b-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0442b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0442b-105">Завершается синхронизация для заглавного сообщения.</span><span class="sxs-lookup"><span data-stu-id="0442b-105">Ends synchronization for a message header.</span></span>
  
```cpp
HRESULT SyncHdrEnd( 
    LPMAPIPROGRESS pprog 
);
```

## <a name="parameters"></a><span data-ttu-id="0442b-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="0442b-106">Parameters</span></span>

 <span data-ttu-id="0442b-107">_pprog_</span><span class="sxs-lookup"><span data-stu-id="0442b-107">_pprog_</span></span>
  
> <span data-ttu-id="0442b-108">[in] **[Интерфейс IMAPIProgress](imapiprogressiunknown.md)** для синхронизации перемещений или копирования сообщений.</span><span class="sxs-lookup"><span data-stu-id="0442b-108">[in] **[IMAPIProgress](imapiprogressiunknown.md)** interface for synchronization of moved or copied messages.</span></span> <span data-ttu-id="0442b-109">См. mapidefs.h для определения типа **LPMAPIPROGRESS**.</span><span class="sxs-lookup"><span data-stu-id="0442b-109">See mapidefs.h for the type definition of **LPMAPIPROGRESS**.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="0442b-110">Примечания</span><span class="sxs-lookup"><span data-stu-id="0442b-110">Remarks</span></span>

<span data-ttu-id="0442b-111">После **[IOSTX::SyncBeg](iostx-syncbeg.md)** локальный магазин вводит состояние заглавного сообщения [для скачивания.](download-message-header-state.md)</span><span class="sxs-lookup"><span data-stu-id="0442b-111">Upon **[IOSTX::SyncBeg](iostx-syncbeg.md)**, the local store enters the [download message header state](download-message-header-state.md).</span></span> <span data-ttu-id="0442b-112">Клиент загружает полный элемент сообщения (как *pmsgFull* в **[HDRSYNC).](hdrsync.md)**</span><span class="sxs-lookup"><span data-stu-id="0442b-112">The client downloads a full message item (as  *pmsgFull*  in **[HDRSYNC](hdrsync.md)** ).</span></span> <span data-ttu-id="0442b-113">Если это успешно, клиент также задает  *ulFlags*  в **HDRSYNC** как **HSF_OK**.</span><span class="sxs-lookup"><span data-stu-id="0442b-113">If this is successful, the client also sets  *ulFlags*  in **HDRSYNC** as **HSF_OK**.</span></span> <span data-ttu-id="0442b-114">После **IOSTX::SyncHdrEnd** Outlook в **HDRSYNC** и использует *pprog* и сведения **в HDRSYNC** для обновления локального заголовка сообщений.</span><span class="sxs-lookup"><span data-stu-id="0442b-114">Upon **IOSTX::SyncHdrEnd**, Outlook checks the result in **HDRSYNC** and uses  *pprog*  and the information in **HDRSYNC** to update the local message header.</span></span> 
  
<span data-ttu-id="0442b-115">Локальный магазин возвращается в состояние, в который он был до предыдущего **[IOSTX::SyncHdrBeg](iostx-synchdrbeg.md)**.</span><span class="sxs-lookup"><span data-stu-id="0442b-115">The local store returns to the state it was in before the preceding **[IOSTX::SyncHdrBeg](iostx-synchdrbeg.md)**.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="0442b-116">См. также</span><span class="sxs-lookup"><span data-stu-id="0442b-116">See also</span></span>



[<span data-ttu-id="0442b-117">IOSTX::GetLastError</span><span class="sxs-lookup"><span data-stu-id="0442b-117">IOSTX::GetLastError</span></span>](iostx-getlasterror.md)
  
[<span data-ttu-id="0442b-118">IOSTX::InitSync</span><span class="sxs-lookup"><span data-stu-id="0442b-118">IOSTX::InitSync</span></span>](iostx-initsync.md)
  
[<span data-ttu-id="0442b-119">IOSTX::SetSyncResult</span><span class="sxs-lookup"><span data-stu-id="0442b-119">IOSTX::SetSyncResult</span></span>](iostx-setsyncresult.md)
  
[<span data-ttu-id="0442b-120">IOSTX::SyncBeg</span><span class="sxs-lookup"><span data-stu-id="0442b-120">IOSTX::SyncBeg</span></span>](iostx-syncbeg.md)
  
[<span data-ttu-id="0442b-121">IOSTX::SyncEnd</span><span class="sxs-lookup"><span data-stu-id="0442b-121">IOSTX::SyncEnd</span></span>](iostx-syncend.md)
  
[<span data-ttu-id="0442b-122">IOSTX::SyncHdrBeg</span><span class="sxs-lookup"><span data-stu-id="0442b-122">IOSTX::SyncHdrBeg</span></span>](iostx-synchdrbeg.md)
  
[<span data-ttu-id="0442b-123">IOSTX : IUnknown</span><span class="sxs-lookup"><span data-stu-id="0442b-123">IOSTX : IUnknown</span></span>](iostxiunknown.md)


[<span data-ttu-id="0442b-124">Константы MAPI</span><span class="sxs-lookup"><span data-stu-id="0442b-124">MAPI Constants</span></span>](mapi-constants.md)

