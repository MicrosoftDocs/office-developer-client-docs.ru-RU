---
title: MAPIFreeBuffer
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPIFreeBuffer
api_type:
- HeaderDef
ms.assetid: 9412594f-8acc-4c7e-a668-4ec1da0ad9cf
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 8794bb233eb69d0f246fb1019954ab718db6f464
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33410555"
---
# <a name="mapifreebuffer"></a><span data-ttu-id="0fb1a-103">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="0fb1a-103">MAPIFreeBuffer</span></span>

  
  
<span data-ttu-id="0fb1a-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0fb1a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0fb1a-105">Освободит буфер памяти, выделенный с помощью вызова функции [MAPIAllocateBuffer](mapiallocatebuffer.md) или [функции MAPIAllocateMore.](mapiallocatemore.md)</span><span class="sxs-lookup"><span data-stu-id="0fb1a-105">Frees a memory buffer allocated with a call to the [MAPIAllocateBuffer](mapiallocatebuffer.md) function or the [MAPIAllocateMore](mapiallocatemore.md) function.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="0fb1a-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="0fb1a-106">Header file:</span></span>  <br/> |<span data-ttu-id="0fb1a-107">Mapix.h</span><span class="sxs-lookup"><span data-stu-id="0fb1a-107">Mapix.h</span></span>  <br/> |
|<span data-ttu-id="0fb1a-108">Реализовано в:</span><span class="sxs-lookup"><span data-stu-id="0fb1a-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="0fb1a-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="0fb1a-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="0fb1a-110">Вызывающая сторона:</span><span class="sxs-lookup"><span data-stu-id="0fb1a-110">Called by:</span></span>  <br/> |<span data-ttu-id="0fb1a-111">Клиентские приложения и поставщики услуг</span><span class="sxs-lookup"><span data-stu-id="0fb1a-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
ULONG MAPIFreeBuffer(
  LPVOID lpBuffer
);
```

## <a name="parameters"></a><span data-ttu-id="0fb1a-112">Parameters</span><span class="sxs-lookup"><span data-stu-id="0fb1a-112">Parameters</span></span>

 <span data-ttu-id="0fb1a-113">_lpBuffer_</span><span class="sxs-lookup"><span data-stu-id="0fb1a-113">_lpBuffer_</span></span>
  
> <span data-ttu-id="0fb1a-114">[in] Указатель на ранее выделенный буфер памяти.</span><span class="sxs-lookup"><span data-stu-id="0fb1a-114">[in] Pointer to a previously allocated memory buffer.</span></span> <span data-ttu-id="0fb1a-115">Если NULL передается в  _параметре lpBuffer,_ **MAPIFreeBuffer** ничего не делает.</span><span class="sxs-lookup"><span data-stu-id="0fb1a-115">If NULL is passed in the  _lpBuffer_ parameter, **MAPIFreeBuffer** does nothing.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="0fb1a-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="0fb1a-116">Return value</span></span>

<span data-ttu-id="0fb1a-117">S_OK</span><span class="sxs-lookup"><span data-stu-id="0fb1a-117">S_OK</span></span> 
  
> <span data-ttu-id="0fb1a-118">Вызов удался и освободил запрашиваемую память.</span><span class="sxs-lookup"><span data-stu-id="0fb1a-118">The call succeeded and freed the memory requested.</span></span> <span data-ttu-id="0fb1a-119">**MAPIFreeBuffer** также может возвращать S_OK уже освобожденных расположениях или если блок памяти не выделен **с MAPIAllocateBuffer** и **MAPIAllocateMore**.</span><span class="sxs-lookup"><span data-stu-id="0fb1a-119">**MAPIFreeBuffer** can also return S_OK on already freed locations or if memory block is not allocated with **MAPIAllocateBuffer** and **MAPIAllocateMore**.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="0fb1a-120">Примечания</span><span class="sxs-lookup"><span data-stu-id="0fb1a-120">Remarks</span></span>

<span data-ttu-id="0fb1a-121">Обычно, когда клиентские приложения или поставщик услуг вызывает [MAPIAllocateBuffer](mapiallocatebuffer.md) или [MAPIAllocateMore,](mapiallocatemore.md)операционная система строит в одном соразмерном буфере памяти одну или несколько сложных структур с несколькими уровнями указателей.</span><span class="sxs-lookup"><span data-stu-id="0fb1a-121">Usually, when a client application or service provider calls [MAPIAllocateBuffer](mapiallocatebuffer.md) or [MAPIAllocateMore](mapiallocatemore.md), the operating system constructs in one contiguous memory buffer one or more complex structures with multiple levels of pointers.</span></span> <span data-ttu-id="0fb1a-122">Когда функция MAPI или метод создает буфер с таким содержимым, клиент может освободить все структуры, содержащиеся в буфере, передав **MAPIFreeBuffer** указатель в буфер, возвращенный функцией MAPI, создав буфер.</span><span class="sxs-lookup"><span data-stu-id="0fb1a-122">When a MAPI function or method creates a buffer with such contents, a client can later free all the structures contained in the buffer by passing to **MAPIFreeBuffer** the pointer to the buffer returned by the MAPI function that created the buffer.</span></span> <span data-ttu-id="0fb1a-123">Чтобы поставщик службы освободил буфер памяти с помощью **MAPIFreeBuffer,** он должен передать указатель в буфер, возвращенный с помощью объекта поддержки поставщика.</span><span class="sxs-lookup"><span data-stu-id="0fb1a-123">For a service provider to free a memory buffer using **MAPIFreeBuffer**, it must pass the pointer to that buffer returned with the provider's support object.</span></span> 
  
<span data-ttu-id="0fb1a-124">Вызов **MAPIFreeBuffer,** чтобы освободить определенный буфер, должен быть выполнен сразу после завершения использования этого буфера клиентом или поставщиком.</span><span class="sxs-lookup"><span data-stu-id="0fb1a-124">The call to **MAPIFreeBuffer** to free a particular buffer must be made as soon as a client or provider is finished using this buffer.</span></span> <span data-ttu-id="0fb1a-125">Просто вызов [метода IMAPISession::Logoff](imapisession-logoff.md) в конце сеанса MAPI автоматически не освобождает буферы памяти.</span><span class="sxs-lookup"><span data-stu-id="0fb1a-125">Simply calling the [IMAPISession::Logoff](imapisession-logoff.md) method at the end of a MAPI session does not automatically release memory buffers.</span></span> 
  
<span data-ttu-id="0fb1a-126">Клиент или поставщик услуг должны работать с предположением о том, что указатель, переданный _в lpBuffer,_ недействителен после успешного возвращения **из MAPIFreeBuffer.**</span><span class="sxs-lookup"><span data-stu-id="0fb1a-126">A client or service provider should operate on the assumption that the pointer passed in  _lpBuffer_ is invalid after a successful return from **MAPIFreeBuffer**.</span></span> <span data-ttu-id="0fb1a-127">Если указатель указывает либо блок памяти, не выделенный системой обмена сообщениями через **MAPIAllocateBuffer** или **MAPIAllocateMore,** либо свободный блок памяти, поведение **MAPIFreeBuffer** неопределяется.</span><span class="sxs-lookup"><span data-stu-id="0fb1a-127">If the pointer indicates either a memory block not allocated by the messaging system through **MAPIAllocateBuffer** or **MAPIAllocateMore** or a free memory block, the behavior of **MAPIFreeBuffer** is undefined.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="0fb1a-128">Передача указателя null в **MAPIFreeBuffer** упрощает и меньше код очистки приложений, так как **MAPIFreeBuffer** может инициализировать указатели в NULL, а затем освободить их в коде очистки, не тестировать их сначала.</span><span class="sxs-lookup"><span data-stu-id="0fb1a-128">Passing a null pointer to **MAPIFreeBuffer** makes application cleanup code simpler and smaller because **MAPIFreeBuffer** can initialize pointers to NULL and then free them in the cleanup code without having to test them first.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="0fb1a-129">См. также</span><span class="sxs-lookup"><span data-stu-id="0fb1a-129">See also</span></span>



[<span data-ttu-id="0fb1a-130">IMAPISupport::GetMemAllocRoutines</span><span class="sxs-lookup"><span data-stu-id="0fb1a-130">IMAPISupport::GetMemAllocRoutines</span></span>](imapisupport-getmemallocroutines.md)

