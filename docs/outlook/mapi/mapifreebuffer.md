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
# <a name="mapifreebuffer"></a><span data-ttu-id="3c6f2-103">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="3c6f2-103">MAPIFreeBuffer</span></span>

  
  
<span data-ttu-id="3c6f2-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3c6f2-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3c6f2-105">Освободить буфер памяти, выделенный вызовом функции [MAPIAllocateBuffer](mapiallocatebuffer.md) или [MAPIAllocateMore.](mapiallocatemore.md)</span><span class="sxs-lookup"><span data-stu-id="3c6f2-105">Frees a memory buffer allocated with a call to the [MAPIAllocateBuffer](mapiallocatebuffer.md) function or the [MAPIAllocateMore](mapiallocatemore.md) function.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="3c6f2-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="3c6f2-106">Header file:</span></span>  <br/> |<span data-ttu-id="3c6f2-107">Mapix.h</span><span class="sxs-lookup"><span data-stu-id="3c6f2-107">Mapix.h</span></span>  <br/> |
|<span data-ttu-id="3c6f2-108">Реализовано в:</span><span class="sxs-lookup"><span data-stu-id="3c6f2-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="3c6f2-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="3c6f2-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="3c6f2-110">Вызывающая сторона:</span><span class="sxs-lookup"><span data-stu-id="3c6f2-110">Called by:</span></span>  <br/> |<span data-ttu-id="3c6f2-111">Клиентские приложения и поставщики услуг</span><span class="sxs-lookup"><span data-stu-id="3c6f2-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
ULONG MAPIFreeBuffer(
  LPVOID lpBuffer
);
```

## <a name="parameters"></a><span data-ttu-id="3c6f2-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="3c6f2-112">Parameters</span></span>

 <span data-ttu-id="3c6f2-113">_lpBuffer_</span><span class="sxs-lookup"><span data-stu-id="3c6f2-113">_lpBuffer_</span></span>
  
> <span data-ttu-id="3c6f2-114">[in] Указатель на ранее выделенный буфер памяти.</span><span class="sxs-lookup"><span data-stu-id="3c6f2-114">[in] Pointer to a previously allocated memory buffer.</span></span> <span data-ttu-id="3c6f2-115">Если в параметре  _lpBuffer_ передается NULL, **MAPIFreeBuffer** ничего не делает.</span><span class="sxs-lookup"><span data-stu-id="3c6f2-115">If NULL is passed in the  _lpBuffer_ parameter, **MAPIFreeBuffer** does nothing.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="3c6f2-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="3c6f2-116">Return value</span></span>

<span data-ttu-id="3c6f2-117">S_OK</span><span class="sxs-lookup"><span data-stu-id="3c6f2-117">S_OK</span></span> 
  
> <span data-ttu-id="3c6f2-118">Вызов был успешным и освобожден запрашиваемой памяти.</span><span class="sxs-lookup"><span data-stu-id="3c6f2-118">The call succeeded and freed the memory requested.</span></span> <span data-ttu-id="3c6f2-119">**MAPIFreeBuffer** также может возвращать S_OK уже освобожденных расположениях или если блок памяти не выделен с **помощью MAPIAllocateBuffer** и **MAPIAllocateMore.**</span><span class="sxs-lookup"><span data-stu-id="3c6f2-119">**MAPIFreeBuffer** can also return S_OK on already freed locations or if memory block is not allocated with **MAPIAllocateBuffer** and **MAPIAllocateMore**.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="3c6f2-120">Примечания</span><span class="sxs-lookup"><span data-stu-id="3c6f2-120">Remarks</span></span>

<span data-ttu-id="3c6f2-121">Обычно, когда клиентский приложение или поставщик услуг вызывает [MAPIAllocateBuffer](mapiallocatebuffer.md) или [MAPIAllocateMore,](mapiallocatemore.md)операционная система строит в одном буфере памяти одну или несколько сложных структур с несколькими уровнями указателей.</span><span class="sxs-lookup"><span data-stu-id="3c6f2-121">Usually, when a client application or service provider calls [MAPIAllocateBuffer](mapiallocatebuffer.md) or [MAPIAllocateMore](mapiallocatemore.md), the operating system constructs in one contiguous memory buffer one or more complex structures with multiple levels of pointers.</span></span> <span data-ttu-id="3c6f2-122">Когда функция или метод MAPI создает буфер с таким содержимым, клиент позднее может освободить все структуры, содержащиеся в буфере, передав **MAPIFreeBuffer** указатель на буфер, возвращенный функцией MAPI, которая создала буфер.</span><span class="sxs-lookup"><span data-stu-id="3c6f2-122">When a MAPI function or method creates a buffer with such contents, a client can later free all the structures contained in the buffer by passing to **MAPIFreeBuffer** the pointer to the buffer returned by the MAPI function that created the buffer.</span></span> <span data-ttu-id="3c6f2-123">Чтобы поставщик услуг освободил буфер памяти с помощью **MAPIFreeBuffer,** он должен передать указатель в этот буфер, возвращенный объектом поддержки поставщика.</span><span class="sxs-lookup"><span data-stu-id="3c6f2-123">For a service provider to free a memory buffer using **MAPIFreeBuffer**, it must pass the pointer to that buffer returned with the provider's support object.</span></span> 
  
<span data-ttu-id="3c6f2-124">Вызов **MAPIFreeBuffer** для освободить определенный буфер должен быть выполнен, как только клиент или поставщик завершит использование этого буфера.</span><span class="sxs-lookup"><span data-stu-id="3c6f2-124">The call to **MAPIFreeBuffer** to free a particular buffer must be made as soon as a client or provider is finished using this buffer.</span></span> <span data-ttu-id="3c6f2-125">Вызов метода [IMAPISession::Logoff](imapisession-logoff.md) в конце сеанса MAPI не освобождает автоматически буферы памяти.</span><span class="sxs-lookup"><span data-stu-id="3c6f2-125">Simply calling the [IMAPISession::Logoff](imapisession-logoff.md) method at the end of a MAPI session does not automatically release memory buffers.</span></span> 
  
<span data-ttu-id="3c6f2-126">Клиент или поставщик услуг должен работать, предполагая, что указатель, переданный _в lpBuffer,_ недействителен после успешного возврата **от MAPIFreeBuffer.**</span><span class="sxs-lookup"><span data-stu-id="3c6f2-126">A client or service provider should operate on the assumption that the pointer passed in  _lpBuffer_ is invalid after a successful return from **MAPIFreeBuffer**.</span></span> <span data-ttu-id="3c6f2-127">Если указатель указывает на блок памяти, не выделенный системой обмена сообщениями через **MAPIAllocateBuffer** или **MAPIAllocateMore,** либо на свободный блок памяти, поведение **MAPIFreeBuffer** будет неопределенным.</span><span class="sxs-lookup"><span data-stu-id="3c6f2-127">If the pointer indicates either a memory block not allocated by the messaging system through **MAPIAllocateBuffer** or **MAPIAllocateMore** or a free memory block, the behavior of **MAPIFreeBuffer** is undefined.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="3c6f2-128">Передача NULL-указателя в **MAPIFreeBuffer** упрощает и меньше кода очистки приложения, так как **MAPIFreeBuffer** может инициализировать указатели на NULL, а затем освободить их в коде очистки, не тестировать их в первую очередь.</span><span class="sxs-lookup"><span data-stu-id="3c6f2-128">Passing a null pointer to **MAPIFreeBuffer** makes application cleanup code simpler and smaller because **MAPIFreeBuffer** can initialize pointers to NULL and then free them in the cleanup code without having to test them first.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="3c6f2-129">См. также</span><span class="sxs-lookup"><span data-stu-id="3c6f2-129">See also</span></span>



[<span data-ttu-id="3c6f2-130">IMAPISupport::GetMemAllocRoutines</span><span class="sxs-lookup"><span data-stu-id="3c6f2-130">IMAPISupport::GetMemAllocRoutines</span></span>](imapisupport-getmemallocroutines.md)

