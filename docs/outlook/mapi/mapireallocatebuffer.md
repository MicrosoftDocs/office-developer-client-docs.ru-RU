---
title: MAPIReallocateBuffer
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 182ab0c6-c9d3-4cc8-892f-f6b09312ceb9
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 26dcc31f2ebdd1892f966bfb95fda1a65c5140cb
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19809899"
---
# <a name="mapireallocatebuffer"></a><span data-ttu-id="ff047-103">MAPIReallocateBuffer</span><span class="sxs-lookup"><span data-stu-id="ff047-103">MAPIReallocateBuffer</span></span>

  
  
<span data-ttu-id="ff047-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="ff047-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="ff047-105">Перешла к буфер памяти.</span><span class="sxs-lookup"><span data-stu-id="ff047-105">Reallocates a memory buffer.</span></span> <span data-ttu-id="ff047-106">Он используется с функцией [MAPIAllocateBuffer](mapiallocatebuffer.md) .</span><span class="sxs-lookup"><span data-stu-id="ff047-106">It is used with the [MAPIAllocateBuffer](mapiallocatebuffer.md) function.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="ff047-107">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="ff047-107">Header file:</span></span>  <br/> |<span data-ttu-id="ff047-108">omapix.h</span><span class="sxs-lookup"><span data-stu-id="ff047-108">omapix.h</span></span>  <br/> |
|<span data-ttu-id="ff047-109">Вызывается:</span><span class="sxs-lookup"><span data-stu-id="ff047-109">Called by:</span></span>  <br/> |<span data-ttu-id="ff047-110">Клиентские приложения и поставщиков услуг</span><span class="sxs-lookup"><span data-stu-id="ff047-110">Client applications and service providers</span></span>  <br/> |
   
```cpp
STDMETHODIMP_(SCODE) MAPIReallocateBuffer
(
LPVOID lpv, 
ULONG ulSize, 
LPVOID * lppv
);
```

## <a name="parameters"></a><span data-ttu-id="ff047-111">Параметры</span><span class="sxs-lookup"><span data-stu-id="ff047-111">Parameters</span></span>

 <span data-ttu-id="ff047-112">_lpv_</span><span class="sxs-lookup"><span data-stu-id="ff047-112">_lpv_</span></span>
  
> <span data-ttu-id="ff047-113">Указатель на память перераспределить.</span><span class="sxs-lookup"><span data-stu-id="ff047-113">A pointer to the memory to be reallocated.</span></span>
    
 <span data-ttu-id="ff047-114">_ulSize_</span><span class="sxs-lookup"><span data-stu-id="ff047-114">_ulSize_</span></span>
  
> <span data-ttu-id="ff047-115">Размер в байтах, выделения буфера.</span><span class="sxs-lookup"><span data-stu-id="ff047-115">The size, in bytes, of the buffer to be allocated.</span></span>
    
 <span data-ttu-id="ff047-116">_lppv_</span><span class="sxs-lookup"><span data-stu-id="ff047-116">_lppv_</span></span>
  
> <span data-ttu-id="ff047-117">Указатель на возвращаемый выделенный буфер.</span><span class="sxs-lookup"><span data-stu-id="ff047-117">A pointer to the returned allocated buffer.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="ff047-118">Замечания</span><span class="sxs-lookup"><span data-stu-id="ff047-118">Remarks</span></span>

 <span data-ttu-id="ff047-119">**MAPIReallocateBuffer** выделяет новый блок памяти запрошенный размер и копирует содержимое буфера, которое передается в этот новый блок памяти.</span><span class="sxs-lookup"><span data-stu-id="ff047-119">**MAPIReallocateBuffer** allocates a new block of memory of the requested size and copies the contents of the buffer that is passed into this new block of memory.</span></span> <span data-ttu-id="ff047-120">Если блок памяти, который передается содержит внутренних указателей, указатели не изменяйте в соответствии с в новом месте.</span><span class="sxs-lookup"><span data-stu-id="ff047-120">If the block of memory that is passed contains internal pointers, the pointers do not change to match the new location.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="ff047-121">См. также</span><span class="sxs-lookup"><span data-stu-id="ff047-121">See also</span></span>



[<span data-ttu-id="ff047-122">MAPIAllocateBuffer</span><span class="sxs-lookup"><span data-stu-id="ff047-122">MAPIAllocateBuffer</span></span>](mapiallocatebuffer.md)

