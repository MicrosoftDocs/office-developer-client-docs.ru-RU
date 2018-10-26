---
title: IOSTXSyncHdrBeg
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IOSTX.SyncHdrBeg
api_type:
- COM
ms.assetid: 7f8ca7cf-ac0b-9b77-c1dd-9f1d0871d603
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 2d05592d1fdcdcd53c8b7879f9cdcd432df1a3f7
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22579468"
---
# <a name="iostxsynchdrbeg"></a><span data-ttu-id="5601f-103">IOSTX::SyncHdrBeg</span><span class="sxs-lookup"><span data-stu-id="5601f-103">IOSTX::SyncHdrBeg</span></span>

  
  
<span data-ttu-id="5601f-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5601f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5601f-105">Запускает синхронизацию для заголовка сообщения.</span><span class="sxs-lookup"><span data-stu-id="5601f-105">Starts synchronization for a message header.</span></span>
  
```cpp
HRESULT SyncHdrBeg( 
    ULONG cbeid, 
    LPENTRYID lpeid, 
    LPVOID *ppv 
);
```

## <a name="parameters"></a><span data-ttu-id="5601f-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="5601f-106">Parameters</span></span>

 <span data-ttu-id="5601f-107">_cbeid_</span><span class="sxs-lookup"><span data-stu-id="5601f-107">_cbeid_</span></span>
  
> <span data-ttu-id="5601f-108">[in] Число байт в Идентификаторе запись для сообщения.</span><span class="sxs-lookup"><span data-stu-id="5601f-108">[in] The number of bytes in the entry ID for the message.</span></span>
    
 <span data-ttu-id="5601f-109">_lpeid_</span><span class="sxs-lookup"><span data-stu-id="5601f-109">_lpeid_</span></span>
  
> <span data-ttu-id="5601f-110">[in] Идентификатор записи сообщения.</span><span class="sxs-lookup"><span data-stu-id="5601f-110">[in] The entry ID for the message.</span></span>
    
 <span data-ttu-id="5601f-111">_ppv_</span><span class="sxs-lookup"><span data-stu-id="5601f-111">_ppv_</span></span>
  
>  <span data-ttu-id="5601f-112">[в] и [out] указатель на структуру **[HDRSYNC](hdrsync.md)** для заголовка сообщения.</span><span class="sxs-lookup"><span data-stu-id="5601f-112">[in]/[out] Pointer to the **[HDRSYNC](hdrsync.md)** structure for the message header.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="5601f-113">Замечания</span><span class="sxs-lookup"><span data-stu-id="5601f-113">Remarks</span></span>

<span data-ttu-id="5601f-114">После **IOSTX::SyncHdrBeg**локального хранилища переходы можно [загрузить состояние заголовка сообщения](download-message-header-state.md).</span><span class="sxs-lookup"><span data-stu-id="5601f-114">Upon **IOSTX::SyncHdrBeg**, the local store transitions to the [download message header state](download-message-header-state.md).</span></span> <span data-ttu-id="5601f-115">Для клиента Outlook инициализирует структуру **HDRSYNC** с текущее представление заголовок сообщения в хранилище и родительской папки.</span><span class="sxs-lookup"><span data-stu-id="5601f-115">Outlook initializes for the client the **HDRSYNC** structure with the current representation of the message header in the store and the parent folder.</span></span> <span data-ttu-id="5601f-116">Клиент затем необходимо загрузить элемента полного сообщения (как *pmsgFull* в **HDRSYNC** ).</span><span class="sxs-lookup"><span data-stu-id="5601f-116">The client must then download a full message item (as  *pmsgFull*  in **HDRSYNC** ).</span></span> <span data-ttu-id="5601f-117">Если это прошла успешно, клиент также задается *ulFlags* в **HDRSYNC** **HSF_OK**.</span><span class="sxs-lookup"><span data-stu-id="5601f-117">If this was successful, the client also sets  *ulFlags*  in **HDRSYNC** as **HSF_OK**.</span></span> <span data-ttu-id="5601f-118">После **[IOSTX::SyncHdrEnd](iostx-synchdrend.md)** Outlook проверяет результат в **HDRSYNC** и использует сведения из **HDRSYNC** для обновления заголовка локального сообщения.</span><span class="sxs-lookup"><span data-stu-id="5601f-118">Upon **[IOSTX::SyncHdrEnd](iostx-synchdrend.md)**, Outlook checks the result in **HDRSYNC** and uses the information in **HDRSYNC** to update the local message header.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="5601f-119">См. также</span><span class="sxs-lookup"><span data-stu-id="5601f-119">See also</span></span>



[<span data-ttu-id="5601f-120">IOSTX::GetLastError</span><span class="sxs-lookup"><span data-stu-id="5601f-120">IOSTX::GetLastError</span></span>](iostx-getlasterror.md)
  
[<span data-ttu-id="5601f-121">IOSTX::InitSync</span><span class="sxs-lookup"><span data-stu-id="5601f-121">IOSTX::InitSync</span></span>](iostx-initsync.md)
  
[<span data-ttu-id="5601f-122">IOSTX::SetSyncResult</span><span class="sxs-lookup"><span data-stu-id="5601f-122">IOSTX::SetSyncResult</span></span>](iostx-setsyncresult.md)
  
[<span data-ttu-id="5601f-123">IOSTX::SyncBeg</span><span class="sxs-lookup"><span data-stu-id="5601f-123">IOSTX::SyncBeg</span></span>](iostx-syncbeg.md)
  
[<span data-ttu-id="5601f-124">IOSTX::SyncEnd</span><span class="sxs-lookup"><span data-stu-id="5601f-124">IOSTX::SyncEnd</span></span>](iostx-syncend.md)
  
[<span data-ttu-id="5601f-125">IOSTX::SyncHdrEnd</span><span class="sxs-lookup"><span data-stu-id="5601f-125">IOSTX::SyncHdrEnd</span></span>](iostx-synchdrend.md)
  
[<span data-ttu-id="5601f-126">IOSTX : IUnknown</span><span class="sxs-lookup"><span data-stu-id="5601f-126">IOSTX : IUnknown</span></span>](iostxiunknown.md)


[<span data-ttu-id="5601f-127">Константы MAPI</span><span class="sxs-lookup"><span data-stu-id="5601f-127">MAPI Constants</span></span>](mapi-constants.md)

