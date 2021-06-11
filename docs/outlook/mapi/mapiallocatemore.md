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
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 01980b2da735838eeffa9afa5a0d139b69e76d0c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435392"
---
# <a name="mapiallocatemore"></a><span data-ttu-id="d698f-103">MAPIAllocateMore</span><span class="sxs-lookup"><span data-stu-id="d698f-103">MAPIAllocateMore</span></span>

  
  
<span data-ttu-id="d698f-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d698f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d698f-105">Выделяет буфер памяти, связанный с другим буфером, ранее выделенным с функцией [MAPIAllocateBuffer.](mapiallocatebuffer.md)</span><span class="sxs-lookup"><span data-stu-id="d698f-105">Allocates a memory buffer that is linked to another buffer previously allocated with the [MAPIAllocateBuffer](mapiallocatebuffer.md) function.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="d698f-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="d698f-106">Header file:</span></span>  <br/> |<span data-ttu-id="d698f-107">Mapix.h</span><span class="sxs-lookup"><span data-stu-id="d698f-107">Mapix.h</span></span>  <br/> |
|<span data-ttu-id="d698f-108">Реализовано в:</span><span class="sxs-lookup"><span data-stu-id="d698f-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="d698f-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="d698f-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="d698f-110">Вызывающая сторона:</span><span class="sxs-lookup"><span data-stu-id="d698f-110">Called by:</span></span>  <br/> |<span data-ttu-id="d698f-111">Клиентские приложения и поставщики услуг</span><span class="sxs-lookup"><span data-stu-id="d698f-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
SCODE MAPIAllocateMore(
  ULONG cbSize,
  LPVOID lpObject,
  LPVOID FAR * lppBuffer
);
```

## <a name="parameters"></a><span data-ttu-id="d698f-112">Parameters</span><span class="sxs-lookup"><span data-stu-id="d698f-112">Parameters</span></span>

 <span data-ttu-id="d698f-113">_cbSize_</span><span class="sxs-lookup"><span data-stu-id="d698f-113">_cbSize_</span></span>
  
> <span data-ttu-id="d698f-114">[in] Размер, в bytes, нового буфера, который будет выделен.</span><span class="sxs-lookup"><span data-stu-id="d698f-114">[in] Size, in bytes, of the new buffer to be allocated.</span></span> 
    
 <span data-ttu-id="d698f-115">_lpObject_</span><span class="sxs-lookup"><span data-stu-id="d698f-115">_lpObject_</span></span>
  
> <span data-ttu-id="d698f-116">[in] Указатель на существующий буфер MAPI, выделенный с помощью **MAPIAllocateBuffer.**</span><span class="sxs-lookup"><span data-stu-id="d698f-116">[in] Pointer to an existing MAPI buffer allocated using **MAPIAllocateBuffer**.</span></span>
    
 <span data-ttu-id="d698f-117">_lppBuffer_</span><span class="sxs-lookup"><span data-stu-id="d698f-117">_lppBuffer_</span></span>
  
> <span data-ttu-id="d698f-118">[вышел] Указатель на возвращенный, недавно выделенный буфер.</span><span class="sxs-lookup"><span data-stu-id="d698f-118">[out] Pointer to the returned, newly allocated buffer.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="d698f-119">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="d698f-119">Return value</span></span>

<span data-ttu-id="d698f-120">S_OK</span><span class="sxs-lookup"><span data-stu-id="d698f-120">S_OK</span></span> 
  
> <span data-ttu-id="d698f-121">Вызов удался и вернул указатель в запрашиваемую память.</span><span class="sxs-lookup"><span data-stu-id="d698f-121">The call succeeded and has returned a pointer to the requested memory.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="d698f-122">Примечания</span><span class="sxs-lookup"><span data-stu-id="d698f-122">Remarks</span></span>

<span data-ttu-id="d698f-123">Во **время обработки вызовов MAPIAllocateMore** реализация вызовов получает блок памяти из операционной системы.</span><span class="sxs-lookup"><span data-stu-id="d698f-123">During **MAPIAllocateMore** call processing, the calling implementation acquires a block of memory from the operating system.</span></span> <span data-ttu-id="d698f-124">Буфер памяти выделяется на 10-номерный byte-адрес.</span><span class="sxs-lookup"><span data-stu-id="d698f-124">The memory buffer is allocated on an even-numbered byte address.</span></span> <span data-ttu-id="d698f-125">На платформах, где более эффективным является длительный доступ к сети, операционная система выделяет буфер на адрес, размер которого в bytes — несколько из четырех.</span><span class="sxs-lookup"><span data-stu-id="d698f-125">On platforms where long integer access is more efficient, the operating system allocates the buffer on an address whose size in bytes is a multiple of four.</span></span> 
  
<span data-ttu-id="d698f-126">Единственный способ освободить буфер, выделенный **с помощью MAPIAllocateMore,** — передать указатель буфера, указанный в параметре _lpObject,_ функции [MAPIFreeBuffer.](mapifreebuffer.md)</span><span class="sxs-lookup"><span data-stu-id="d698f-126">The only way to release a buffer allocated with **MAPIAllocateMore** is to pass the buffer pointer specified in the  _lpObject_ parameter to the [MAPIFreeBuffer](mapifreebuffer.md) function.</span></span> <span data-ttu-id="d698f-127">Связь между буферами памяти, выделенными [MAPIAllocateBuffer](mapiallocatebuffer.md) и **MAPIAllocateMore,** позволяет **MAPIFreeBuffer** освободить оба буфера одним вызовом.</span><span class="sxs-lookup"><span data-stu-id="d698f-127">The link between the memory buffers allocated with [MAPIAllocateBuffer](mapiallocatebuffer.md) and **MAPIAllocateMore** enables **MAPIFreeBuffer** to release both buffers with a single call.</span></span> 
  

