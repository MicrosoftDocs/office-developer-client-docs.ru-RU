---
title: MAPIAllocateMore
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPIAllocateMore
api_type:
- HeaderDef
ms.assetid: 3e48f76a-bc97-4cbc-9082-c07dd674b73e
description: '���� ���������� ���������: 9 ����� 2015 �.'
ms.openlocfilehash: f6f986ae811f2c7a886231a3046038889b82d683
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19809874"
---
# <a name="mapiallocatemore"></a><span data-ttu-id="07f7b-103">MAPIAllocateMore</span><span class="sxs-lookup"><span data-stu-id="07f7b-103">MAPIAllocateMore</span></span>

  
  
<span data-ttu-id="07f7b-104">**Применимо к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="07f7b-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="07f7b-105">Выделяет буфер памяти, который связан с другой буфера, выделенного ранее с помощью функции [MAPIAllocateBuffer](mapiallocatebuffer.md) .</span><span class="sxs-lookup"><span data-stu-id="07f7b-105">Allocates a memory buffer that is linked to another buffer previously allocated with the [MAPIAllocateBuffer](mapiallocatebuffer.md) function.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="07f7b-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="07f7b-106">Header file:</span></span>  <br/> |<span data-ttu-id="07f7b-107">Mapix.h</span><span class="sxs-lookup"><span data-stu-id="07f7b-107">Mapix.h</span></span>  <br/> |
|<span data-ttu-id="07f7b-108">Реализованный:</span><span class="sxs-lookup"><span data-stu-id="07f7b-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="07f7b-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="07f7b-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="07f7b-110">Вызывается:</span><span class="sxs-lookup"><span data-stu-id="07f7b-110">Called by:</span></span>  <br/> |<span data-ttu-id="07f7b-111">Клиентские приложения и поставщиков услуг</span><span class="sxs-lookup"><span data-stu-id="07f7b-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
SCODE MAPIAllocateMore(
  ULONG cbSize,
  LPVOID lpObject,
  LPVOID FAR * lppBuffer
);
```

## <a name="parameters"></a><span data-ttu-id="07f7b-112">Parameters</span><span class="sxs-lookup"><span data-stu-id="07f7b-112">Parameters</span></span>

 <span data-ttu-id="07f7b-113">_cbSize_</span><span class="sxs-lookup"><span data-stu-id="07f7b-113">_cbSize_</span></span>
  
> <span data-ttu-id="07f7b-114">[in] Размер, в байтах, выделения нового буфера.</span><span class="sxs-lookup"><span data-stu-id="07f7b-114">[in] Size, in bytes, of the new buffer to be allocated.</span></span> 
    
 <span data-ttu-id="07f7b-115">_lpObject_</span><span class="sxs-lookup"><span data-stu-id="07f7b-115">_lpObject_</span></span>
  
> <span data-ttu-id="07f7b-116">[in] Указатель на существующий MAPI буфер, выделенный с помощью **MAPIAllocateBuffer**.</span><span class="sxs-lookup"><span data-stu-id="07f7b-116">[in] Pointer to an existing MAPI buffer allocated using **MAPIAllocateBuffer**.</span></span>
    
 <span data-ttu-id="07f7b-117">_lppBuffer_</span><span class="sxs-lookup"><span data-stu-id="07f7b-117">_lppBuffer_</span></span>
  
> <span data-ttu-id="07f7b-118">[out] Указатель на возвращенное вновь выделенный буфер.</span><span class="sxs-lookup"><span data-stu-id="07f7b-118">[out] Pointer to the returned, newly allocated buffer.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="07f7b-119">������������ ��������</span><span class="sxs-lookup"><span data-stu-id="07f7b-119">Return value</span></span>

<span data-ttu-id="07f7b-120">ЗНАЧЕНИЕ S_OK</span><span class="sxs-lookup"><span data-stu-id="07f7b-120">S_OK</span></span> 
  
> <span data-ttu-id="07f7b-121">Вызов успешно и вернул указатель на запрошенный память.</span><span class="sxs-lookup"><span data-stu-id="07f7b-121">The call succeeded and has returned a pointer to the requested memory.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="07f7b-122">Замечания</span><span class="sxs-lookup"><span data-stu-id="07f7b-122">Remarks</span></span>

<span data-ttu-id="07f7b-123">Во время **MAPIAllocateMore** вызовите обработки, вызывающий реализации Получает блок памяти от операционной системы.</span><span class="sxs-lookup"><span data-stu-id="07f7b-123">During **MAPIAllocateMore** call processing, the calling implementation acquires a block of memory from the operating system.</span></span> <span data-ttu-id="07f7b-124">Буфер памяти, выделенный на адрес четных байтов.</span><span class="sxs-lookup"><span data-stu-id="07f7b-124">The memory buffer is allocated on an even-numbered byte address.</span></span> <span data-ttu-id="07f7b-125">На платформах, где доступа "длинное целое" — это более эффективный операционная система выделяет буфера на адрес, размер которых в байтах делится на четыре.</span><span class="sxs-lookup"><span data-stu-id="07f7b-125">On platforms where long integer access is more efficient, the operating system allocates the buffer on an address whose size in bytes is a multiple of four.</span></span> 
  
<span data-ttu-id="07f7b-126">— Это единственный способ освободить буфер, выделенный с **MAPIAllocateMore** указателя буфера, указанный в параметре _lpObject_ функции [MAPIFreeBuffer](mapifreebuffer.md) .</span><span class="sxs-lookup"><span data-stu-id="07f7b-126">The only way to release a buffer allocated with **MAPIAllocateMore** is to pass the buffer pointer specified in the  _lpObject_ parameter to the [MAPIFreeBuffer](mapifreebuffer.md) function.</span></span> <span data-ttu-id="07f7b-127">Связь между буферов памяти, выделенный с [MAPIAllocateBuffer](mapiallocatebuffer.md) и **MAPIAllocateMore** позволяет **MAPIFreeBuffer** для освобождения обоих буферов с помощью одного вызова.</span><span class="sxs-lookup"><span data-stu-id="07f7b-127">The link between the memory buffers allocated with [MAPIAllocateBuffer](mapiallocatebuffer.md) and **MAPIAllocateMore** enables **MAPIFreeBuffer** to release both buffers with a single call.</span></span> 
  

