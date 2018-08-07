---
title: IOSTXGetLastError
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IOSTX.GetLastError
api_type:
- COM
ms.assetid: b25c9288-b391-6303-3643-5a5b66b75c48
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 69853dbec46b08c4dc402012fb7f1074f30ebf52
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19809453"
---
# <a name="iostxgetlasterror"></a><span data-ttu-id="adefd-103">IOSTX::GetLastError</span><span class="sxs-lookup"><span data-stu-id="adefd-103">IOSTX::GetLastError</span></span>

  
  
<span data-ttu-id="adefd-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="adefd-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="adefd-105">Получает расширенные сведения о последней ошибки.</span><span class="sxs-lookup"><span data-stu-id="adefd-105">Gets extended information about the last error.</span></span>
  
```cpp
HRESULT GetLastError( 
    HRESULT hResult, 
    ULONG ulFlags, 
    LPMAPIERROR *lppMAPIError 
);
```

## <a name="parameters"></a><span data-ttu-id="adefd-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="adefd-106">Parameters</span></span>

 <span data-ttu-id="adefd-107">_hResult_</span><span class="sxs-lookup"><span data-stu-id="adefd-107">_hResult_</span></span>
  
>  <span data-ttu-id="adefd-108">[in] Код ошибки.</span><span class="sxs-lookup"><span data-stu-id="adefd-108">[in] Error code.</span></span> 
    
 <span data-ttu-id="adefd-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="adefd-109">_ulFlags_</span></span>
  
>  <span data-ttu-id="adefd-110">[in] Flags to modify behavior.</span><span class="sxs-lookup"><span data-stu-id="adefd-110">[in] Flags to modify behavior.</span></span> <span data-ttu-id="adefd-111">Это должно быть равно 0.</span><span class="sxs-lookup"><span data-stu-id="adefd-111">This must be 0.</span></span> 
    
 <span data-ttu-id="adefd-112">_lppMAPIError_</span><span class="sxs-lookup"><span data-stu-id="adefd-112">_lppMAPIError_</span></span>
  
>  <span data-ttu-id="adefd-113">[out] Указатель на структуру **MAPIERROR** , который содержит дополнительные сведения об ошибке.</span><span class="sxs-lookup"><span data-stu-id="adefd-113">[out] Pointer to the **MAPIERROR** structure that contains the extended information for the error.</span></span> <span data-ttu-id="adefd-114">В разделе mapidefs.h для определения типа **LPMAPIERROR**.</span><span class="sxs-lookup"><span data-stu-id="adefd-114">See mapidefs.h for the type definition of **LPMAPIERROR**.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="adefd-115">См. также</span><span class="sxs-lookup"><span data-stu-id="adefd-115">See also</span></span>



[<span data-ttu-id="adefd-116">IOSTX::InitSync</span><span class="sxs-lookup"><span data-stu-id="adefd-116">IOSTX::InitSync</span></span>](iostx-initsync.md)
  
[<span data-ttu-id="adefd-117">IOSTX::SetSyncResult</span><span class="sxs-lookup"><span data-stu-id="adefd-117">IOSTX::SetSyncResult</span></span>](iostx-setsyncresult.md)
  
[<span data-ttu-id="adefd-118">IOSTX::SyncBeg</span><span class="sxs-lookup"><span data-stu-id="adefd-118">IOSTX::SyncBeg</span></span>](iostx-syncbeg.md)
  
[<span data-ttu-id="adefd-119">IOSTX::SyncEnd</span><span class="sxs-lookup"><span data-stu-id="adefd-119">IOSTX::SyncEnd</span></span>](iostx-syncend.md)
  
[<span data-ttu-id="adefd-120">IOSTX::SyncHdrBeg</span><span class="sxs-lookup"><span data-stu-id="adefd-120">IOSTX::SyncHdrBeg</span></span>](iostx-synchdrbeg.md)
  
[<span data-ttu-id="adefd-121">IOSTX::SyncHdrEnd</span><span class="sxs-lookup"><span data-stu-id="adefd-121">IOSTX::SyncHdrEnd</span></span>](iostx-synchdrend.md)
  
[<span data-ttu-id="adefd-122">IOSTX : IUnknown</span><span class="sxs-lookup"><span data-stu-id="adefd-122">IOSTX : IUnknown</span></span>](iostxiunknown.md)


[<span data-ttu-id="adefd-123">��������� MAPI</span><span class="sxs-lookup"><span data-stu-id="adefd-123">MAPI Constants</span></span>](mapi-constants.md)

