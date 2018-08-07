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
ms.openlocfilehash: 8ba00ecc1d9ff1c0b7db63d3e6d667b374245742
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19809861"
---
# <a name="mapiallocatebuffer"></a><span data-ttu-id="56408-103">MAPIAllocateBuffer</span><span class="sxs-lookup"><span data-stu-id="56408-103">MAPIAllocateBuffer</span></span>

  
  
<span data-ttu-id="56408-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="56408-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="56408-105">Выделяет буфер памяти.</span><span class="sxs-lookup"><span data-stu-id="56408-105">Allocates a memory buffer.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="56408-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="56408-106">Header file:</span></span>  <br/> |<span data-ttu-id="56408-107">Mapix.h</span><span class="sxs-lookup"><span data-stu-id="56408-107">Mapix.h</span></span>  <br/> |
|<span data-ttu-id="56408-108">Реализованный:</span><span class="sxs-lookup"><span data-stu-id="56408-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="56408-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="56408-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="56408-110">Вызывается:</span><span class="sxs-lookup"><span data-stu-id="56408-110">Called by:</span></span>  <br/> |<span data-ttu-id="56408-111">Клиентские приложения и поставщиков услуг</span><span class="sxs-lookup"><span data-stu-id="56408-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
SCODE MAPIAllocateBuffer(
  ULONG cbSize,
  LPVOID FAR * lppBuffer
);
```

## <a name="parameters"></a><span data-ttu-id="56408-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="56408-112">Parameters</span></span>

 <span data-ttu-id="56408-113">_cbSize_</span><span class="sxs-lookup"><span data-stu-id="56408-113">_cbSize_</span></span>
  
> <span data-ttu-id="56408-114">[in] Размер, в байтах, выделения буфера.</span><span class="sxs-lookup"><span data-stu-id="56408-114">[in] Size, in bytes, of the buffer to be allocated.</span></span> 
    
 <span data-ttu-id="56408-115">_lppBuffer_</span><span class="sxs-lookup"><span data-stu-id="56408-115">_lppBuffer_</span></span>
  
> <span data-ttu-id="56408-116">[out] Указатель на возвращаемый выделенный буфер.</span><span class="sxs-lookup"><span data-stu-id="56408-116">[out] Pointer to the returned allocated buffer.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="56408-117">������������ ��������</span><span class="sxs-lookup"><span data-stu-id="56408-117">Return value</span></span>

<span data-ttu-id="56408-118">ЗНАЧЕНИЕ S_OK</span><span class="sxs-lookup"><span data-stu-id="56408-118">S_OK</span></span> 
  
> <span data-ttu-id="56408-119">Вызов успешно и вернул буфер запрошенные памяти.</span><span class="sxs-lookup"><span data-stu-id="56408-119">The call succeeded and has returned the requested memory buffer.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="56408-120">Замечания</span><span class="sxs-lookup"><span data-stu-id="56408-120">Remarks</span></span>

<span data-ttu-id="56408-121">Во время **MAPIAllocateBuffer** вызовите обработки, вызывающий реализации Получает блок памяти от операционной системы.</span><span class="sxs-lookup"><span data-stu-id="56408-121">During **MAPIAllocateBuffer** call processing, the calling implementation acquires a block of memory from the operating system.</span></span> <span data-ttu-id="56408-122">Буфер памяти, выделенный на адрес четных байтов.</span><span class="sxs-lookup"><span data-stu-id="56408-122">The memory buffer is allocated on an even-numbered byte address.</span></span> <span data-ttu-id="56408-123">На платформах, где доступа "длинное целое" — это более эффективный операционная система выделяет буфера на адрес, размер которых в байтах делится на четыре.</span><span class="sxs-lookup"><span data-stu-id="56408-123">On platforms where long integer access is more efficient, the operating system allocates the buffer on an address whose size in bytes is a multiple of four.</span></span> 
  
<span data-ttu-id="56408-124">Вызов выпусков функция [MAPIFreeBuffer](mapifreebuffer.md) буфер памяти, выделенный с **MAPIAllocateBuffer**путем вызова функции [MAPIAllocateMore](mapiallocatemore.md) и буферов по ссылке, когда объем памяти больше не требуется.</span><span class="sxs-lookup"><span data-stu-id="56408-124">Calling the [MAPIFreeBuffer](mapifreebuffer.md) function releases the memory buffer allocated by **MAPIAllocateBuffer**, by calling the [MAPIAllocateMore](mapiallocatemore.md) function and any buffers linked to it, when the memory is no longer needed.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="56408-125">См. также</span><span class="sxs-lookup"><span data-stu-id="56408-125">See also</span></span>



[<span data-ttu-id="56408-126">MAPIReallocateBuffer</span><span class="sxs-lookup"><span data-stu-id="56408-126">MAPIReallocateBuffer</span></span>](mapireallocatebuffer.md)

