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
# <a name="mapiallocatemore"></a><span data-ttu-id="c6816-103">MAPIAllocateMore</span><span class="sxs-lookup"><span data-stu-id="c6816-103">MAPIAllocateMore</span></span>

  
  
<span data-ttu-id="c6816-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c6816-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c6816-105">Выделяет буфер памяти, связанный с другим буфером, ранее выделенным [функцией MAPIAllocateBuffer.](mapiallocatebuffer.md)</span><span class="sxs-lookup"><span data-stu-id="c6816-105">Allocates a memory buffer that is linked to another buffer previously allocated with the [MAPIAllocateBuffer](mapiallocatebuffer.md) function.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="c6816-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="c6816-106">Header file:</span></span>  <br/> |<span data-ttu-id="c6816-107">Mapix.h</span><span class="sxs-lookup"><span data-stu-id="c6816-107">Mapix.h</span></span>  <br/> |
|<span data-ttu-id="c6816-108">Реализовано в:</span><span class="sxs-lookup"><span data-stu-id="c6816-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="c6816-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="c6816-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="c6816-110">Вызывающая сторона:</span><span class="sxs-lookup"><span data-stu-id="c6816-110">Called by:</span></span>  <br/> |<span data-ttu-id="c6816-111">Клиентские приложения и поставщики услуг</span><span class="sxs-lookup"><span data-stu-id="c6816-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
SCODE MAPIAllocateMore(
  ULONG cbSize,
  LPVOID lpObject,
  LPVOID FAR * lppBuffer
);
```

## <a name="parameters"></a><span data-ttu-id="c6816-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="c6816-112">Parameters</span></span>

 <span data-ttu-id="c6816-113">_cbSize_</span><span class="sxs-lookup"><span data-stu-id="c6816-113">_cbSize_</span></span>
  
> <span data-ttu-id="c6816-114">[in] Размер нового буфера, который необходимо выделить, в вахтах.</span><span class="sxs-lookup"><span data-stu-id="c6816-114">[in] Size, in bytes, of the new buffer to be allocated.</span></span> 
    
 <span data-ttu-id="c6816-115">_lpObject_</span><span class="sxs-lookup"><span data-stu-id="c6816-115">_lpObject_</span></span>
  
> <span data-ttu-id="c6816-116">[in] Указатель на существующий буфер MAPI, выделенный с помощью **MAPIAllocateBuffer.**</span><span class="sxs-lookup"><span data-stu-id="c6816-116">[in] Pointer to an existing MAPI buffer allocated using **MAPIAllocateBuffer**.</span></span>
    
 <span data-ttu-id="c6816-117">_lppBuffer_</span><span class="sxs-lookup"><span data-stu-id="c6816-117">_lppBuffer_</span></span>
  
> <span data-ttu-id="c6816-118">[out] Указатель на возвращенный недавно выделенный буфер.</span><span class="sxs-lookup"><span data-stu-id="c6816-118">[out] Pointer to the returned, newly allocated buffer.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="c6816-119">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="c6816-119">Return value</span></span>

<span data-ttu-id="c6816-120">S_OK</span><span class="sxs-lookup"><span data-stu-id="c6816-120">S_OK</span></span> 
  
> <span data-ttu-id="c6816-121">Вызов был успешным и возвращен указатель на запрашиваемую память.</span><span class="sxs-lookup"><span data-stu-id="c6816-121">The call succeeded and has returned a pointer to the requested memory.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="c6816-122">Примечания</span><span class="sxs-lookup"><span data-stu-id="c6816-122">Remarks</span></span>

<span data-ttu-id="c6816-123">Во время обработки вызовов **MAPIAllocateMore** реализация вызова получает блок памяти из операционной системы.</span><span class="sxs-lookup"><span data-stu-id="c6816-123">During **MAPIAllocateMore** call processing, the calling implementation acquires a block of memory from the operating system.</span></span> <span data-ttu-id="c6816-124">Буфер памяти выделяется для even-numbered byte address.</span><span class="sxs-lookup"><span data-stu-id="c6816-124">The memory buffer is allocated on an even-numbered byte address.</span></span> <span data-ttu-id="c6816-125">На платформах, где длинный полный доступ более эффективен, операционная система выделяет буфер на адресе, размер которого в кратном размере кратно четырем.</span><span class="sxs-lookup"><span data-stu-id="c6816-125">On platforms where long integer access is more efficient, the operating system allocates the buffer on an address whose size in bytes is a multiple of four.</span></span> 
  
<span data-ttu-id="c6816-126">Единственный способ освободить буфер, выделенный с помощью **MAPIAllocateMore,** — передать указатель буфера, указанный в параметре _lpObject,_ функции [MAPIFreeBuffer.](mapifreebuffer.md)</span><span class="sxs-lookup"><span data-stu-id="c6816-126">The only way to release a buffer allocated with **MAPIAllocateMore** is to pass the buffer pointer specified in the  _lpObject_ parameter to the [MAPIFreeBuffer](mapifreebuffer.md) function.</span></span> <span data-ttu-id="c6816-127">Связь между буферами памяти, выделенными с помощью [MAPIAllocateBuffer](mapiallocatebuffer.md) и **MAPIAllocateMore,** позволяет **MAPIFreeBuffer** освободить оба буфера одним вызовом.</span><span class="sxs-lookup"><span data-stu-id="c6816-127">The link between the memory buffers allocated with [MAPIAllocateBuffer](mapiallocatebuffer.md) and **MAPIAllocateMore** enables **MAPIFreeBuffer** to release both buffers with a single call.</span></span> 
  

