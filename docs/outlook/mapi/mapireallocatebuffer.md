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
ms.openlocfilehash: e85e2da4d63442dc1fb912c5941be9d6f6f53824
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22593790"
---
# <a name="mapireallocatebuffer"></a><span data-ttu-id="47979-103">MAPIReallocateBuffer</span><span class="sxs-lookup"><span data-stu-id="47979-103">MAPIReallocateBuffer</span></span>

  
  
<span data-ttu-id="47979-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="47979-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="47979-105">Перешла к буфер памяти.</span><span class="sxs-lookup"><span data-stu-id="47979-105">Reallocates a memory buffer.</span></span> <span data-ttu-id="47979-106">Он используется с функцией [MAPIAllocateBuffer](mapiallocatebuffer.md) .</span><span class="sxs-lookup"><span data-stu-id="47979-106">It is used with the [MAPIAllocateBuffer](mapiallocatebuffer.md) function.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="47979-107">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="47979-107">Header file:</span></span>  <br/> |<span data-ttu-id="47979-108">omapix.h</span><span class="sxs-lookup"><span data-stu-id="47979-108">omapix.h</span></span>  <br/> |
|<span data-ttu-id="47979-109">Вызывается:</span><span class="sxs-lookup"><span data-stu-id="47979-109">Called by:</span></span>  <br/> |<span data-ttu-id="47979-110">Клиентские приложения и поставщиков услуг</span><span class="sxs-lookup"><span data-stu-id="47979-110">Client applications and service providers</span></span>  <br/> |
   
```cpp
STDMETHODIMP_(SCODE) MAPIReallocateBuffer
(
LPVOID lpv, 
ULONG ulSize, 
LPVOID * lppv
);
```

## <a name="parameters"></a><span data-ttu-id="47979-111">Параметры</span><span class="sxs-lookup"><span data-stu-id="47979-111">Parameters</span></span>

 <span data-ttu-id="47979-112">_lpv_</span><span class="sxs-lookup"><span data-stu-id="47979-112">_lpv_</span></span>
  
> <span data-ttu-id="47979-113">Указатель на память перераспределить.</span><span class="sxs-lookup"><span data-stu-id="47979-113">A pointer to the memory to be reallocated.</span></span>
    
 <span data-ttu-id="47979-114">_ulSize_</span><span class="sxs-lookup"><span data-stu-id="47979-114">_ulSize_</span></span>
  
> <span data-ttu-id="47979-115">Размер в байтах, выделения буфера.</span><span class="sxs-lookup"><span data-stu-id="47979-115">The size, in bytes, of the buffer to be allocated.</span></span>
    
 <span data-ttu-id="47979-116">_lppv_</span><span class="sxs-lookup"><span data-stu-id="47979-116">_lppv_</span></span>
  
> <span data-ttu-id="47979-117">Указатель на возвращаемый выделенный буфер.</span><span class="sxs-lookup"><span data-stu-id="47979-117">A pointer to the returned allocated buffer.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="47979-118">Замечания</span><span class="sxs-lookup"><span data-stu-id="47979-118">Remarks</span></span>

 <span data-ttu-id="47979-119">**MAPIReallocateBuffer** выделяет новый блок памяти запрошенный размер и копирует содержимое буфера, которое передается в этот новый блок памяти.</span><span class="sxs-lookup"><span data-stu-id="47979-119">**MAPIReallocateBuffer** allocates a new block of memory of the requested size and copies the contents of the buffer that is passed into this new block of memory.</span></span> <span data-ttu-id="47979-120">Если блок памяти, который передается содержит внутренних указателей, указатели не изменяйте в соответствии с в новом месте.</span><span class="sxs-lookup"><span data-stu-id="47979-120">If the block of memory that is passed contains internal pointers, the pointers do not change to match the new location.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="47979-121">См. также</span><span class="sxs-lookup"><span data-stu-id="47979-121">See also</span></span>



[<span data-ttu-id="47979-122">MAPIAllocateBuffer</span><span class="sxs-lookup"><span data-stu-id="47979-122">MAPIAllocateBuffer</span></span>](mapiallocatebuffer.md)

