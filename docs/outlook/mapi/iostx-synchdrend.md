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
ms.openlocfilehash: ee68052f330bf3239cd12139ffbd77f5a180f6cc
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19809467"
---
# <a name="iostxsynchdrend"></a><span data-ttu-id="73483-103">IOSTX::SyncHdrEnd</span><span class="sxs-lookup"><span data-stu-id="73483-103">IOSTX::SyncHdrEnd</span></span>

 
  
<span data-ttu-id="73483-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="73483-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="73483-105">Завершает синхронизации для заголовка сообщения.</span><span class="sxs-lookup"><span data-stu-id="73483-105">Ends synchronization for a message header.</span></span>
  
```cpp
HRESULT SyncHdrEnd( 
    LPMAPIPROGRESS pprog 
);
```

## <a name="parameters"></a><span data-ttu-id="73483-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="73483-106">Parameters</span></span>

 <span data-ttu-id="73483-107">_pprog_</span><span class="sxs-lookup"><span data-stu-id="73483-107">_pprog_</span></span>
  
> <span data-ttu-id="73483-108">[in] Интерфейс **[IMAPIProgress](imapiprogressiunknown.md)** для синхронизации перемещения или копирования сообщения.</span><span class="sxs-lookup"><span data-stu-id="73483-108">[in] **[IMAPIProgress](imapiprogressiunknown.md)** interface for synchronization of moved or copied messages.</span></span> <span data-ttu-id="73483-109">В разделе mapidefs.h для определения типа **LPMAPIPROGRESS**.</span><span class="sxs-lookup"><span data-stu-id="73483-109">See mapidefs.h for the type definition of **LPMAPIPROGRESS**.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="73483-110">Замечания</span><span class="sxs-lookup"><span data-stu-id="73483-110">Remarks</span></span>

<span data-ttu-id="73483-111">После **[IOSTX::SyncBeg](iostx-syncbeg.md)** локального хранилища вводит [загрузить состояние заголовка сообщения](download-message-header-state.md).</span><span class="sxs-lookup"><span data-stu-id="73483-111">Upon **[IOSTX::SyncBeg](iostx-syncbeg.md)**, the local store enters the [download message header state](download-message-header-state.md).</span></span> <span data-ttu-id="73483-112">Клиент загружает элемент полного сообщения (как *pmsgFull* в **[HDRSYNC](hdrsync.md)** ).</span><span class="sxs-lookup"><span data-stu-id="73483-112">The client downloads a full message item (as  *pmsgFull*  in **[HDRSYNC](hdrsync.md)** ).</span></span> <span data-ttu-id="73483-113">Если это выполнена успешно, клиент также задается *ulFlags* в **HDRSYNC** **HSF_OK**.</span><span class="sxs-lookup"><span data-stu-id="73483-113">If this is successful, the client also sets  *ulFlags*  in **HDRSYNC** as **HSF_OK**.</span></span> <span data-ttu-id="73483-114">После **IOSTX::SyncHdrEnd**Outlook проверяет результат в **HDRSYNC** и использует *pprog* и данные в **HDRSYNC** для обновления заголовка локального сообщения.</span><span class="sxs-lookup"><span data-stu-id="73483-114">Upon **IOSTX::SyncHdrEnd**, Outlook checks the result in **HDRSYNC** and uses  *pprog*  and the information in **HDRSYNC** to update the local message header.</span></span> 
  
<span data-ttu-id="73483-115">Возвращает состояние, в котором он находился до предыдущей **[IOSTX::SyncHdrBeg](iostx-synchdrbeg.md)** локального хранилища.</span><span class="sxs-lookup"><span data-stu-id="73483-115">The local store returns to the state it was in before the preceding **[IOSTX::SyncHdrBeg](iostx-synchdrbeg.md)**.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="73483-116">См. также</span><span class="sxs-lookup"><span data-stu-id="73483-116">See also</span></span>



[<span data-ttu-id="73483-117">IOSTX::GetLastError</span><span class="sxs-lookup"><span data-stu-id="73483-117">IOSTX::GetLastError</span></span>](iostx-getlasterror.md)
  
[<span data-ttu-id="73483-118">IOSTX::InitSync</span><span class="sxs-lookup"><span data-stu-id="73483-118">IOSTX::InitSync</span></span>](iostx-initsync.md)
  
[<span data-ttu-id="73483-119">IOSTX::SetSyncResult</span><span class="sxs-lookup"><span data-stu-id="73483-119">IOSTX::SetSyncResult</span></span>](iostx-setsyncresult.md)
  
[<span data-ttu-id="73483-120">IOSTX::SyncBeg</span><span class="sxs-lookup"><span data-stu-id="73483-120">IOSTX::SyncBeg</span></span>](iostx-syncbeg.md)
  
[<span data-ttu-id="73483-121">IOSTX::SyncEnd</span><span class="sxs-lookup"><span data-stu-id="73483-121">IOSTX::SyncEnd</span></span>](iostx-syncend.md)
  
[<span data-ttu-id="73483-122">IOSTX::SyncHdrBeg</span><span class="sxs-lookup"><span data-stu-id="73483-122">IOSTX::SyncHdrBeg</span></span>](iostx-synchdrbeg.md)
  
[<span data-ttu-id="73483-123">IOSTX : IUnknown</span><span class="sxs-lookup"><span data-stu-id="73483-123">IOSTX : IUnknown</span></span>](iostxiunknown.md)


[<span data-ttu-id="73483-124">��������� MAPI</span><span class="sxs-lookup"><span data-stu-id="73483-124">MAPI Constants</span></span>](mapi-constants.md)

