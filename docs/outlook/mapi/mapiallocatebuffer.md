---
title: MAPIAllocateBuffer
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPIAllocateBuffer
api_type:
- HeaderDef
ms.assetid: f1fc7fc5-c71f-44f7-930a-571773eb6809
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 589ad42199e6f2ec1039499dfd9beda044ccc3dd
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425696"
---
# <a name="mapiallocatebuffer"></a><span data-ttu-id="3e937-103">MAPIAllocateBuffer</span><span class="sxs-lookup"><span data-stu-id="3e937-103">MAPIAllocateBuffer</span></span>

  
  
<span data-ttu-id="3e937-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3e937-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3e937-105">Выделяет буфер памяти.</span><span class="sxs-lookup"><span data-stu-id="3e937-105">Allocates a memory buffer.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="3e937-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="3e937-106">Header file:</span></span>  <br/> |<span data-ttu-id="3e937-107">Mapix.h</span><span class="sxs-lookup"><span data-stu-id="3e937-107">Mapix.h</span></span>  <br/> |
|<span data-ttu-id="3e937-108">Реализовано в:</span><span class="sxs-lookup"><span data-stu-id="3e937-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="3e937-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="3e937-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="3e937-110">Вызывающая сторона:</span><span class="sxs-lookup"><span data-stu-id="3e937-110">Called by:</span></span>  <br/> |<span data-ttu-id="3e937-111">Клиентские приложения и поставщики услуг</span><span class="sxs-lookup"><span data-stu-id="3e937-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
SCODE MAPIAllocateBuffer(
  ULONG cbSize,
  LPVOID FAR * lppBuffer
);
```

## <a name="parameters"></a><span data-ttu-id="3e937-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="3e937-112">Parameters</span></span>

 <span data-ttu-id="3e937-113">_cbSize_</span><span class="sxs-lookup"><span data-stu-id="3e937-113">_cbSize_</span></span>
  
> <span data-ttu-id="3e937-114">[in] Размер выделяемого буфера (в bytes).</span><span class="sxs-lookup"><span data-stu-id="3e937-114">[in] Size, in bytes, of the buffer to be allocated.</span></span> 
    
 <span data-ttu-id="3e937-115">_lppBuffer_</span><span class="sxs-lookup"><span data-stu-id="3e937-115">_lppBuffer_</span></span>
  
> <span data-ttu-id="3e937-116">[out] Указатель на возвращенный выделенный буфер.</span><span class="sxs-lookup"><span data-stu-id="3e937-116">[out] Pointer to the returned allocated buffer.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="3e937-117">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="3e937-117">Return value</span></span>

<span data-ttu-id="3e937-118">S_OK</span><span class="sxs-lookup"><span data-stu-id="3e937-118">S_OK</span></span> 
  
> <span data-ttu-id="3e937-119">Вызов был успешным и возвращен запрашиваемой памяти.</span><span class="sxs-lookup"><span data-stu-id="3e937-119">The call succeeded and has returned the requested memory buffer.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="3e937-120">Примечания</span><span class="sxs-lookup"><span data-stu-id="3e937-120">Remarks</span></span>

<span data-ttu-id="3e937-121">Во время обработки вызовов **MAPIAllocateBuffer** реализация вызова получает блок памяти из операционной системы.</span><span class="sxs-lookup"><span data-stu-id="3e937-121">During **MAPIAllocateBuffer** call processing, the calling implementation acquires a block of memory from the operating system.</span></span> <span data-ttu-id="3e937-122">Буфер памяти выделяется для even-numbered byte address.</span><span class="sxs-lookup"><span data-stu-id="3e937-122">The memory buffer is allocated on an even-numbered byte address.</span></span> <span data-ttu-id="3e937-123">На платформах, где длинный полный доступ более эффективен, операционная система выделяет буфер на адресе, размер которого в кратном размере кратно четырем.</span><span class="sxs-lookup"><span data-stu-id="3e937-123">On platforms where long integer access is more efficient, the operating system allocates the buffer on an address whose size in bytes is a multiple of four.</span></span> 
  
<span data-ttu-id="3e937-124">Вызов функции [MAPIFreeBuffer](mapifreebuffer.md) освобождает буфер памяти, выделенный **MAPIAllocateBuffer,** путем вызова функции [MAPIAllocateMore](mapiallocatemore.md) и всех связанных с ней буферов, когда память больше не требуется.</span><span class="sxs-lookup"><span data-stu-id="3e937-124">Calling the [MAPIFreeBuffer](mapifreebuffer.md) function releases the memory buffer allocated by **MAPIAllocateBuffer**, by calling the [MAPIAllocateMore](mapiallocatemore.md) function and any buffers linked to it, when the memory is no longer needed.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="3e937-125">См. также</span><span class="sxs-lookup"><span data-stu-id="3e937-125">See also</span></span>



[<span data-ttu-id="3e937-126">MAPIReallocateBuffer</span><span class="sxs-lookup"><span data-stu-id="3e937-126">MAPIReallocateBuffer</span></span>](mapireallocatebuffer.md)

