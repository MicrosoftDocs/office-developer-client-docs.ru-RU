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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32270240"
---
# <a name="mapireallocatebuffer"></a><span data-ttu-id="d8867-103">MAPIReallocateBuffer</span><span class="sxs-lookup"><span data-stu-id="d8867-103">MAPIReallocateBuffer</span></span>

  
  
<span data-ttu-id="d8867-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d8867-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d8867-105">Перераспределяет буфер памяти.</span><span class="sxs-lookup"><span data-stu-id="d8867-105">Reallocates a memory buffer.</span></span> <span data-ttu-id="d8867-106">Он используется с функцией [мапиаллокатебуффер](mapiallocatebuffer.md) .</span><span class="sxs-lookup"><span data-stu-id="d8867-106">It is used with the [MAPIAllocateBuffer](mapiallocatebuffer.md) function.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="d8867-107">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="d8867-107">Header file:</span></span>  <br/> |<span data-ttu-id="d8867-108">омапикс. h</span><span class="sxs-lookup"><span data-stu-id="d8867-108">omapix.h</span></span>  <br/> |
|<span data-ttu-id="d8867-109">Вызывающая сторона:</span><span class="sxs-lookup"><span data-stu-id="d8867-109">Called by:</span></span>  <br/> |<span data-ttu-id="d8867-110">Клиентские приложения и поставщики услуг</span><span class="sxs-lookup"><span data-stu-id="d8867-110">Client applications and service providers</span></span>  <br/> |
   
```cpp
STDMETHODIMP_(SCODE) MAPIReallocateBuffer
(
LPVOID lpv, 
ULONG ulSize, 
LPVOID * lppv
);
```

## <a name="parameters"></a><span data-ttu-id="d8867-111">Параметры</span><span class="sxs-lookup"><span data-stu-id="d8867-111">Parameters</span></span>

 <span data-ttu-id="d8867-112">_лпв_</span><span class="sxs-lookup"><span data-stu-id="d8867-112">_lpv_</span></span>
  
> <span data-ttu-id="d8867-113">Указатель на память, которую необходимо перераспределить.</span><span class="sxs-lookup"><span data-stu-id="d8867-113">A pointer to the memory to be reallocated.</span></span>
    
 <span data-ttu-id="d8867-114">_Улсизе_</span><span class="sxs-lookup"><span data-stu-id="d8867-114">_ulSize_</span></span>
  
> <span data-ttu-id="d8867-115">Размер выделяемого буфера (в байтах).</span><span class="sxs-lookup"><span data-stu-id="d8867-115">The size, in bytes, of the buffer to be allocated.</span></span>
    
 <span data-ttu-id="d8867-116">_лппв_</span><span class="sxs-lookup"><span data-stu-id="d8867-116">_lppv_</span></span>
  
> <span data-ttu-id="d8867-117">Указатель на возвращенный выделенный буфер.</span><span class="sxs-lookup"><span data-stu-id="d8867-117">A pointer to the returned allocated buffer.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="d8867-118">Замечания</span><span class="sxs-lookup"><span data-stu-id="d8867-118">Remarks</span></span>

 <span data-ttu-id="d8867-119">**Мапиреаллокатебуффер** выделяет новый блок памяти запрошенного размера и копирует содержимое буфера, переданного в новый блок памяти.</span><span class="sxs-lookup"><span data-stu-id="d8867-119">**MAPIReallocateBuffer** allocates a new block of memory of the requested size and copies the contents of the buffer that is passed into this new block of memory.</span></span> <span data-ttu-id="d8867-120">Если блок памяти, который передается, содержит внутренние указатели, указатели не меняются для согласования с новым расположением.</span><span class="sxs-lookup"><span data-stu-id="d8867-120">If the block of memory that is passed contains internal pointers, the pointers do not change to match the new location.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="d8867-121">См. также</span><span class="sxs-lookup"><span data-stu-id="d8867-121">See also</span></span>



[<span data-ttu-id="d8867-122">MAPIAllocateBuffer</span><span class="sxs-lookup"><span data-stu-id="d8867-122">MAPIAllocateBuffer</span></span>](mapiallocatebuffer.md)

