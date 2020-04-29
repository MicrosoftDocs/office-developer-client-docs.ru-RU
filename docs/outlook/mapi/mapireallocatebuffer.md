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
# <a name="mapireallocatebuffer"></a><span data-ttu-id="e95f6-103">MAPIReallocateBuffer</span><span class="sxs-lookup"><span data-stu-id="e95f6-103">MAPIReallocateBuffer</span></span>

  
  
<span data-ttu-id="e95f6-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e95f6-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e95f6-105">Перераспределяет буфер памяти.</span><span class="sxs-lookup"><span data-stu-id="e95f6-105">Reallocates a memory buffer.</span></span> <span data-ttu-id="e95f6-106">Он используется с функцией [мапиаллокатебуффер](mapiallocatebuffer.md) .</span><span class="sxs-lookup"><span data-stu-id="e95f6-106">It is used with the [MAPIAllocateBuffer](mapiallocatebuffer.md) function.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="e95f6-107">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="e95f6-107">Header file:</span></span>  <br/> |<span data-ttu-id="e95f6-108">омапикс. h</span><span class="sxs-lookup"><span data-stu-id="e95f6-108">omapix.h</span></span>  <br/> |
|<span data-ttu-id="e95f6-109">Вызывающая сторона:</span><span class="sxs-lookup"><span data-stu-id="e95f6-109">Called by:</span></span>  <br/> |<span data-ttu-id="e95f6-110">Клиентские приложения и поставщики услуг</span><span class="sxs-lookup"><span data-stu-id="e95f6-110">Client applications and service providers</span></span>  <br/> |
   
```cpp
STDMETHODIMP_(SCODE) MAPIReallocateBuffer
(
LPVOID lpv, 
ULONG ulSize, 
LPVOID * lppv
);
```

## <a name="parameters"></a><span data-ttu-id="e95f6-111">Параметры</span><span class="sxs-lookup"><span data-stu-id="e95f6-111">Parameters</span></span>

 <span data-ttu-id="e95f6-112">_лпв_</span><span class="sxs-lookup"><span data-stu-id="e95f6-112">_lpv_</span></span>
  
> <span data-ttu-id="e95f6-113">Указатель на память, которую необходимо перераспределить.</span><span class="sxs-lookup"><span data-stu-id="e95f6-113">A pointer to the memory to be reallocated.</span></span>
    
 <span data-ttu-id="e95f6-114">_улсизе_</span><span class="sxs-lookup"><span data-stu-id="e95f6-114">_ulSize_</span></span>
  
> <span data-ttu-id="e95f6-115">Размер выделяемого буфера (в байтах).</span><span class="sxs-lookup"><span data-stu-id="e95f6-115">The size, in bytes, of the buffer to be allocated.</span></span>
    
 <span data-ttu-id="e95f6-116">_лппв_</span><span class="sxs-lookup"><span data-stu-id="e95f6-116">_lppv_</span></span>
  
> <span data-ttu-id="e95f6-117">Указатель на возвращенный выделенный буфер.</span><span class="sxs-lookup"><span data-stu-id="e95f6-117">A pointer to the returned allocated buffer.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="e95f6-118">Примечания</span><span class="sxs-lookup"><span data-stu-id="e95f6-118">Remarks</span></span>

 <span data-ttu-id="e95f6-119">**Мапиреаллокатебуффер** выделяет новый блок памяти запрошенного размера и копирует содержимое буфера, переданного в новый блок памяти.</span><span class="sxs-lookup"><span data-stu-id="e95f6-119">**MAPIReallocateBuffer** allocates a new block of memory of the requested size and copies the contents of the buffer that is passed into this new block of memory.</span></span> <span data-ttu-id="e95f6-120">Если блок памяти, который передается, содержит внутренние указатели, указатели не меняются для согласования с новым расположением.</span><span class="sxs-lookup"><span data-stu-id="e95f6-120">If the block of memory that is passed contains internal pointers, the pointers do not change to match the new location.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="e95f6-121">См. также</span><span class="sxs-lookup"><span data-stu-id="e95f6-121">See also</span></span>



[<span data-ttu-id="e95f6-122">MAPIAllocateBuffer</span><span class="sxs-lookup"><span data-stu-id="e95f6-122">MAPIAllocateBuffer</span></span>](mapiallocatebuffer.md)

