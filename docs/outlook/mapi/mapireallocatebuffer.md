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
ms.openlocfilehash: 59d0ce192605257dc0aebed46d8093a352fce05f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435287"
---
# <a name="mapireallocatebuffer"></a><span data-ttu-id="9581a-103">MAPIReallocateBuffer</span><span class="sxs-lookup"><span data-stu-id="9581a-103">MAPIReallocateBuffer</span></span>

  
  
<span data-ttu-id="9581a-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9581a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9581a-105">Перераспределение буфера памяти.</span><span class="sxs-lookup"><span data-stu-id="9581a-105">Reallocates a memory buffer.</span></span> <span data-ttu-id="9581a-106">Он используется с функцией [MAPIAllocateBuffer.](mapiallocatebuffer.md)</span><span class="sxs-lookup"><span data-stu-id="9581a-106">It is used with the [MAPIAllocateBuffer](mapiallocatebuffer.md) function.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="9581a-107">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="9581a-107">Header file:</span></span>  <br/> |<span data-ttu-id="9581a-108">omapix.h</span><span class="sxs-lookup"><span data-stu-id="9581a-108">omapix.h</span></span>  <br/> |
|<span data-ttu-id="9581a-109">Вызывающая сторона:</span><span class="sxs-lookup"><span data-stu-id="9581a-109">Called by:</span></span>  <br/> |<span data-ttu-id="9581a-110">Клиентские приложения и поставщики услуг</span><span class="sxs-lookup"><span data-stu-id="9581a-110">Client applications and service providers</span></span>  <br/> |
   
```cpp
STDMETHODIMP_(SCODE) MAPIReallocateBuffer
(
LPVOID lpv, 
ULONG ulSize, 
LPVOID * lppv
);
```

## <a name="parameters"></a><span data-ttu-id="9581a-111">Parameters</span><span class="sxs-lookup"><span data-stu-id="9581a-111">Parameters</span></span>

 <span data-ttu-id="9581a-112">_lpv_</span><span class="sxs-lookup"><span data-stu-id="9581a-112">_lpv_</span></span>
  
> <span data-ttu-id="9581a-113">Указатель на память, которая должна быть перенадвижена.</span><span class="sxs-lookup"><span data-stu-id="9581a-113">A pointer to the memory to be reallocated.</span></span>
    
 <span data-ttu-id="9581a-114">_ulSize_</span><span class="sxs-lookup"><span data-stu-id="9581a-114">_ulSize_</span></span>
  
> <span data-ttu-id="9581a-115">Размер выделенного буфера в bytes.</span><span class="sxs-lookup"><span data-stu-id="9581a-115">The size, in bytes, of the buffer to be allocated.</span></span>
    
 <span data-ttu-id="9581a-116">_lppv_</span><span class="sxs-lookup"><span data-stu-id="9581a-116">_lppv_</span></span>
  
> <span data-ttu-id="9581a-117">Указатель на возвращенный выделенный буфер.</span><span class="sxs-lookup"><span data-stu-id="9581a-117">A pointer to the returned allocated buffer.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="9581a-118">Примечания</span><span class="sxs-lookup"><span data-stu-id="9581a-118">Remarks</span></span>

 <span data-ttu-id="9581a-119">**MAPIReallocateBuffer** выделяет новый блок памяти запрашиваемого размера и копирует содержимое буфера, который передается в этот новый блок памяти.</span><span class="sxs-lookup"><span data-stu-id="9581a-119">**MAPIReallocateBuffer** allocates a new block of memory of the requested size and copies the contents of the buffer that is passed into this new block of memory.</span></span> <span data-ttu-id="9581a-120">Если пройденный блок памяти содержит внутренние указатели, указатели не изменяются, чтобы соответствовать новому расположению.</span><span class="sxs-lookup"><span data-stu-id="9581a-120">If the block of memory that is passed contains internal pointers, the pointers do not change to match the new location.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="9581a-121">См. также</span><span class="sxs-lookup"><span data-stu-id="9581a-121">See also</span></span>



[<span data-ttu-id="9581a-122">MAPIAllocateBuffer</span><span class="sxs-lookup"><span data-stu-id="9581a-122">MAPIAllocateBuffer</span></span>](mapiallocatebuffer.md)

