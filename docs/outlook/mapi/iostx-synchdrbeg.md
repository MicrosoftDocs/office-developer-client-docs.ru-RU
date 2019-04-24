---
title: Иосткссинчдрбег
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
ms.openlocfilehash: 49ef9862d5156a1bed242652df32baab9a0123fc
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32317159"
---
# <a name="iostxsynchdrbeg"></a><span data-ttu-id="112b8-103">IOSTX::SyncHdrBeg</span><span class="sxs-lookup"><span data-stu-id="112b8-103">IOSTX::SyncHdrBeg</span></span>

  
  
<span data-ttu-id="112b8-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="112b8-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="112b8-105">Запускает синхронизацию для заголовка сообщения.</span><span class="sxs-lookup"><span data-stu-id="112b8-105">Starts synchronization for a message header.</span></span>
  
```cpp
HRESULT SyncHdrBeg( 
    ULONG cbeid, 
    LPENTRYID lpeid, 
    LPVOID *ppv 
);
```

## <a name="parameters"></a><span data-ttu-id="112b8-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="112b8-106">Parameters</span></span>

 <span data-ttu-id="112b8-107">_кбеид_</span><span class="sxs-lookup"><span data-stu-id="112b8-107">_cbeid_</span></span>
  
> <span data-ttu-id="112b8-108">возврата Число байтов в ИДЕНТИФИКАТОРе записи сообщения.</span><span class="sxs-lookup"><span data-stu-id="112b8-108">[in] The number of bytes in the entry ID for the message.</span></span>
    
 <span data-ttu-id="112b8-109">_лпеид_</span><span class="sxs-lookup"><span data-stu-id="112b8-109">_lpeid_</span></span>
  
> <span data-ttu-id="112b8-110">возврата Идентификатор элемента сообщения.</span><span class="sxs-lookup"><span data-stu-id="112b8-110">[in] The entry ID for the message.</span></span>
    
 <span data-ttu-id="112b8-111">_ППВ_</span><span class="sxs-lookup"><span data-stu-id="112b8-111">_ppv_</span></span>
  
>  <span data-ttu-id="112b8-112">[in]/[out] указатель на структуру **[хдрсинк](hdrsync.md)** для заголовка сообщения.</span><span class="sxs-lookup"><span data-stu-id="112b8-112">[in]/[out] Pointer to the **[HDRSYNC](hdrsync.md)** structure for the message header.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="112b8-113">Замечания</span><span class="sxs-lookup"><span data-stu-id="112b8-113">Remarks</span></span>

<span data-ttu-id="112b8-114">После **иосткс:: синчдрбег**локальное хранилище переходит в [состояние загрузка заголовка сообщения](download-message-header-state.md).</span><span class="sxs-lookup"><span data-stu-id="112b8-114">Upon **IOSTX::SyncHdrBeg**, the local store transitions to the [download message header state](download-message-header-state.md).</span></span> <span data-ttu-id="112b8-115">Outlook инициализирует клиентскую структуру **хдрсинк** с текущим представлением заголовка сообщения в хранилище и родительской папке.</span><span class="sxs-lookup"><span data-stu-id="112b8-115">Outlook initializes for the client the **HDRSYNC** structure with the current representation of the message header in the store and the parent folder.</span></span> <span data-ttu-id="112b8-116">После этого клиент должен скачать полный элемент сообщения (как *пмсгфулл* в **хдрсинк** ).</span><span class="sxs-lookup"><span data-stu-id="112b8-116">The client must then download a full message item (as  *pmsgFull*  in **HDRSYNC** ).</span></span> <span data-ttu-id="112b8-117">В случае успешного выполнения клиент также устанавливает *ulFlags* в **хдрсинк** как **хсф_ок**.</span><span class="sxs-lookup"><span data-stu-id="112b8-117">If this was successful, the client also sets  *ulFlags*  in **HDRSYNC** as **HSF_OK**.</span></span> <span data-ttu-id="112b8-118">После **[иосткс:: синчдренд](iostx-synchdrend.md)** Outlook проверяет результат в **хдрсинк** и использует информацию в **хдрсинк** для обновления заголовка локального сообщения.</span><span class="sxs-lookup"><span data-stu-id="112b8-118">Upon **[IOSTX::SyncHdrEnd](iostx-synchdrend.md)**, Outlook checks the result in **HDRSYNC** and uses the information in **HDRSYNC** to update the local message header.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="112b8-119">См. также</span><span class="sxs-lookup"><span data-stu-id="112b8-119">See also</span></span>



[<span data-ttu-id="112b8-120">IOSTX::GetLastError</span><span class="sxs-lookup"><span data-stu-id="112b8-120">IOSTX::GetLastError</span></span>](iostx-getlasterror.md)
  
[<span data-ttu-id="112b8-121">IOSTX::InitSync</span><span class="sxs-lookup"><span data-stu-id="112b8-121">IOSTX::InitSync</span></span>](iostx-initsync.md)
  
[<span data-ttu-id="112b8-122">IOSTX::SetSyncResult</span><span class="sxs-lookup"><span data-stu-id="112b8-122">IOSTX::SetSyncResult</span></span>](iostx-setsyncresult.md)
  
[<span data-ttu-id="112b8-123">IOSTX::SyncBeg</span><span class="sxs-lookup"><span data-stu-id="112b8-123">IOSTX::SyncBeg</span></span>](iostx-syncbeg.md)
  
[<span data-ttu-id="112b8-124">IOSTX::SyncEnd</span><span class="sxs-lookup"><span data-stu-id="112b8-124">IOSTX::SyncEnd</span></span>](iostx-syncend.md)
  
[<span data-ttu-id="112b8-125">IOSTX::SyncHdrEnd</span><span class="sxs-lookup"><span data-stu-id="112b8-125">IOSTX::SyncHdrEnd</span></span>](iostx-synchdrend.md)
  
[<span data-ttu-id="112b8-126">IOSTX : IUnknown</span><span class="sxs-lookup"><span data-stu-id="112b8-126">IOSTX : IUnknown</span></span>](iostxiunknown.md)


[<span data-ttu-id="112b8-127">Константы MAPI</span><span class="sxs-lookup"><span data-stu-id="112b8-127">MAPI Constants</span></span>](mapi-constants.md)

