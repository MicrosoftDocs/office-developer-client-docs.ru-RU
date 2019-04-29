---
title: Иостксжетластеррор
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
ms.openlocfilehash: 9c29011ae2e9b59a7a0a38148fa6c5b673fd9590
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422301"
---
# <a name="iostxgetlasterror"></a><span data-ttu-id="47d53-103">IOSTX::GetLastError</span><span class="sxs-lookup"><span data-stu-id="47d53-103">IOSTX::GetLastError</span></span>

  
  
<span data-ttu-id="47d53-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="47d53-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="47d53-105">Получает расширенные сведения о последней ошибке.</span><span class="sxs-lookup"><span data-stu-id="47d53-105">Gets extended information about the last error.</span></span>
  
```cpp
HRESULT GetLastError( 
    HRESULT hResult, 
    ULONG ulFlags, 
    LPMAPIERROR *lppMAPIError 
);
```

## <a name="parameters"></a><span data-ttu-id="47d53-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="47d53-106">Parameters</span></span>

 <span data-ttu-id="47d53-107">_Состав_</span><span class="sxs-lookup"><span data-stu-id="47d53-107">_hResult_</span></span>
  
>  <span data-ttu-id="47d53-108">возврата Код ошибки.</span><span class="sxs-lookup"><span data-stu-id="47d53-108">[in] Error code.</span></span> 
    
 <span data-ttu-id="47d53-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="47d53-109">_ulFlags_</span></span>
  
>  <span data-ttu-id="47d53-110">[in] Flags to modify behavior.</span><span class="sxs-lookup"><span data-stu-id="47d53-110">[in] Flags to modify behavior.</span></span> <span data-ttu-id="47d53-111">Значение должно быть равно 0.</span><span class="sxs-lookup"><span data-stu-id="47d53-111">This must be 0.</span></span> 
    
 <span data-ttu-id="47d53-112">_Лппмапиеррор_</span><span class="sxs-lookup"><span data-stu-id="47d53-112">_lppMAPIError_</span></span>
  
>  <span data-ttu-id="47d53-113">вышли Указатель на структуру **мапиеррор** , которая содержит расширенные сведения об ошибке.</span><span class="sxs-lookup"><span data-stu-id="47d53-113">[out] Pointer to the **MAPIERROR** structure that contains the extended information for the error.</span></span> <span data-ttu-id="47d53-114">Определение типа **лпмапиеррор**можно найти в файле MAPIDEFS. h.</span><span class="sxs-lookup"><span data-stu-id="47d53-114">See mapidefs.h for the type definition of **LPMAPIERROR**.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="47d53-115">См. также</span><span class="sxs-lookup"><span data-stu-id="47d53-115">See also</span></span>



[<span data-ttu-id="47d53-116">IOSTX::InitSync</span><span class="sxs-lookup"><span data-stu-id="47d53-116">IOSTX::InitSync</span></span>](iostx-initsync.md)
  
[<span data-ttu-id="47d53-117">IOSTX::SetSyncResult</span><span class="sxs-lookup"><span data-stu-id="47d53-117">IOSTX::SetSyncResult</span></span>](iostx-setsyncresult.md)
  
[<span data-ttu-id="47d53-118">IOSTX::SyncBeg</span><span class="sxs-lookup"><span data-stu-id="47d53-118">IOSTX::SyncBeg</span></span>](iostx-syncbeg.md)
  
[<span data-ttu-id="47d53-119">IOSTX::SyncEnd</span><span class="sxs-lookup"><span data-stu-id="47d53-119">IOSTX::SyncEnd</span></span>](iostx-syncend.md)
  
[<span data-ttu-id="47d53-120">IOSTX::SyncHdrBeg</span><span class="sxs-lookup"><span data-stu-id="47d53-120">IOSTX::SyncHdrBeg</span></span>](iostx-synchdrbeg.md)
  
[<span data-ttu-id="47d53-121">IOSTX::SyncHdrEnd</span><span class="sxs-lookup"><span data-stu-id="47d53-121">IOSTX::SyncHdrEnd</span></span>](iostx-synchdrend.md)
  
[<span data-ttu-id="47d53-122">IOSTX : IUnknown</span><span class="sxs-lookup"><span data-stu-id="47d53-122">IOSTX : IUnknown</span></span>](iostxiunknown.md)


[<span data-ttu-id="47d53-123">Константы MAPI</span><span class="sxs-lookup"><span data-stu-id="47d53-123">MAPI Constants</span></span>](mapi-constants.md)

