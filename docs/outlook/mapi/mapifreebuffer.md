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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32346664"
---
# <a name="mapifreebuffer"></a><span data-ttu-id="dc1a5-103">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="dc1a5-103">MAPIFreeBuffer</span></span>

  
  
<span data-ttu-id="dc1a5-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="dc1a5-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="dc1a5-105">Освобождает буфер памяти, выделенный с помощью вызова функции [мапиаллокатебуффер](mapiallocatebuffer.md) или функции [мапиаллокатеморе](mapiallocatemore.md) .</span><span class="sxs-lookup"><span data-stu-id="dc1a5-105">Frees a memory buffer allocated with a call to the [MAPIAllocateBuffer](mapiallocatebuffer.md) function or the [MAPIAllocateMore](mapiallocatemore.md) function.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="dc1a5-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="dc1a5-106">Header file:</span></span>  <br/> |<span data-ttu-id="dc1a5-107">Мапикс. h</span><span class="sxs-lookup"><span data-stu-id="dc1a5-107">Mapix.h</span></span>  <br/> |
|<span data-ttu-id="dc1a5-108">Реализовано в:</span><span class="sxs-lookup"><span data-stu-id="dc1a5-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="dc1a5-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="dc1a5-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="dc1a5-110">Вызывающая сторона:</span><span class="sxs-lookup"><span data-stu-id="dc1a5-110">Called by:</span></span>  <br/> |<span data-ttu-id="dc1a5-111">Клиентские приложения и поставщики услуг</span><span class="sxs-lookup"><span data-stu-id="dc1a5-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
ULONG MAPIFreeBuffer(
  LPVOID lpBuffer
);
```

## <a name="parameters"></a><span data-ttu-id="dc1a5-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="dc1a5-112">Parameters</span></span>

 <span data-ttu-id="dc1a5-113">_Лпбуффер_</span><span class="sxs-lookup"><span data-stu-id="dc1a5-113">_lpBuffer_</span></span>
  
> <span data-ttu-id="dc1a5-114">возврата Указатель на выделенный ранее буфер памяти.</span><span class="sxs-lookup"><span data-stu-id="dc1a5-114">[in] Pointer to a previously allocated memory buffer.</span></span> <span data-ttu-id="dc1a5-115">Если параметр _лпбуффер_ переДАЕТСЯ значение null, **мапифрибуффер** не выполняет никаких действий.</span><span class="sxs-lookup"><span data-stu-id="dc1a5-115">If NULL is passed in the  _lpBuffer_ parameter, **MAPIFreeBuffer** does nothing.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="dc1a5-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="dc1a5-116">Return value</span></span>

<span data-ttu-id="dc1a5-117">S_OK</span><span class="sxs-lookup"><span data-stu-id="dc1a5-117">S_OK</span></span> 
  
> <span data-ttu-id="dc1a5-118">Вызов завершился успешно и освободил запрошенный объем памяти.</span><span class="sxs-lookup"><span data-stu-id="dc1a5-118">The call succeeded and freed the memory requested.</span></span> <span data-ttu-id="dc1a5-119">**Мапифрибуффер** также может возВРАЩАТЬ значение S_OK в уже освобожденных расположениях, или если блок памяти не выделен с помощью **мапиаллокатебуффер** и **мапиаллокатеморе**.</span><span class="sxs-lookup"><span data-stu-id="dc1a5-119">**MAPIFreeBuffer** can also return S_OK on already freed locations or if memory block is not allocated with **MAPIAllocateBuffer** and **MAPIAllocateMore**.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="dc1a5-120">Примечания</span><span class="sxs-lookup"><span data-stu-id="dc1a5-120">Remarks</span></span>

<span data-ttu-id="dc1a5-121">Как правило, когда клиентское приложение или поставщик услуг вызывает [мапиаллокатебуффер](mapiallocatebuffer.md) или [мапиаллокатеморе](mapiallocatemore.md), операционная система создает одну или несколько сложных структур памяти в одном или нескольких сложных структурах с несколькими уровнями указателей.</span><span class="sxs-lookup"><span data-stu-id="dc1a5-121">Usually, when a client application or service provider calls [MAPIAllocateBuffer](mapiallocatebuffer.md) or [MAPIAllocateMore](mapiallocatemore.md), the operating system constructs in one contiguous memory buffer one or more complex structures with multiple levels of pointers.</span></span> <span data-ttu-id="dc1a5-122">Когда функция или метод MAPI создает буфер с таким содержимым, клиент может позже освободить все структуры, содержащиеся в буфере, передав **мапифрибуффер** указатель на буфер, возвращенный функцией MAPI, которая создала буфер.</span><span class="sxs-lookup"><span data-stu-id="dc1a5-122">When a MAPI function or method creates a buffer with such contents, a client can later free all the structures contained in the buffer by passing to **MAPIFreeBuffer** the pointer to the buffer returned by the MAPI function that created the buffer.</span></span> <span data-ttu-id="dc1a5-123">Чтобы поставщик услуг высвободить буфер памяти с помощью **мапифрибуффер**, он должен передать указатель на этот буфер, возвращенный с помощью объекта поддержки поставщика.</span><span class="sxs-lookup"><span data-stu-id="dc1a5-123">For a service provider to free a memory buffer using **MAPIFreeBuffer**, it must pass the pointer to that buffer returned with the provider's support object.</span></span> 
  
<span data-ttu-id="dc1a5-124">Вызов **мапифрибуффер** для освобождения определенного буфера должен быть выполнен сразу после завершения работы клиента или поставщика с помощью этого буфера.</span><span class="sxs-lookup"><span data-stu-id="dc1a5-124">The call to **MAPIFreeBuffer** to free a particular buffer must be made as soon as a client or provider is finished using this buffer.</span></span> <span data-ttu-id="dc1a5-125">Простое обращение к методу [IMAPISession:: logoff](imapisession-logoff.md) в конце сеанса MAPI не приводит к автоматическому освобождению буферов памяти.</span><span class="sxs-lookup"><span data-stu-id="dc1a5-125">Simply calling the [IMAPISession::Logoff](imapisession-logoff.md) method at the end of a MAPI session does not automatically release memory buffers.</span></span> 
  
<span data-ttu-id="dc1a5-126">Клиент или поставщик услуг должен работать в предположении, что указатель, переданный в _лпбуффер_ , является недопустимым после успешного возврата из **мапифрибуффер**.</span><span class="sxs-lookup"><span data-stu-id="dc1a5-126">A client or service provider should operate on the assumption that the pointer passed in  _lpBuffer_ is invalid after a successful return from **MAPIFreeBuffer**.</span></span> <span data-ttu-id="dc1a5-127">Если указатель указывает либо блок памяти, не выделенный системой обмена сообщениями, через **мапиаллокатебуффер** или **мапиаллокатеморе** или свободный блок памяти, поведение **мапифрибуффер** не определено.</span><span class="sxs-lookup"><span data-stu-id="dc1a5-127">If the pointer indicates either a memory block not allocated by the messaging system through **MAPIAllocateBuffer** or **MAPIAllocateMore** or a free memory block, the behavior of **MAPIFreeBuffer** is undefined.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="dc1a5-128">Передача пустого указателя в **мапифрибуффер** упрощает и уменьшает код очистки приложений, так как **мапифрибуффер** может инициализировать указатели на null и затем освобождать их в коде очистки, не проверяйте их первыми.</span><span class="sxs-lookup"><span data-stu-id="dc1a5-128">Passing a null pointer to **MAPIFreeBuffer** makes application cleanup code simpler and smaller because **MAPIFreeBuffer** can initialize pointers to NULL and then free them in the cleanup code without having to test them first.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="dc1a5-129">См. также</span><span class="sxs-lookup"><span data-stu-id="dc1a5-129">See also</span></span>



[<span data-ttu-id="dc1a5-130">IMAPISupport::GetMemAllocRoutines</span><span class="sxs-lookup"><span data-stu-id="dc1a5-130">IMAPISupport::GetMemAllocRoutines</span></span>](imapisupport-getmemallocroutines.md)

