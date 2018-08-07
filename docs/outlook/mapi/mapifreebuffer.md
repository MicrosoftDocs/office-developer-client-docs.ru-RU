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
ms.openlocfilehash: 22aad12010a4f367e18443d8c0831c6262cc37fc
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19809898"
---
# <a name="mapifreebuffer"></a><span data-ttu-id="9c119-103">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="9c119-103">MAPIFreeBuffer</span></span>

  
  
<span data-ttu-id="9c119-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="9c119-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="9c119-105">Освобождает буфер памяти, выделенный с помощью вызова функции [MAPIAllocateBuffer](mapiallocatebuffer.md) или функцию [MAPIAllocateMore](mapiallocatemore.md) .</span><span class="sxs-lookup"><span data-stu-id="9c119-105">Frees a memory buffer allocated with a call to the [MAPIAllocateBuffer](mapiallocatebuffer.md) function or the [MAPIAllocateMore](mapiallocatemore.md) function.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="9c119-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="9c119-106">Header file:</span></span>  <br/> |<span data-ttu-id="9c119-107">Mapix.h</span><span class="sxs-lookup"><span data-stu-id="9c119-107">Mapix.h</span></span>  <br/> |
|<span data-ttu-id="9c119-108">Реализованный:</span><span class="sxs-lookup"><span data-stu-id="9c119-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="9c119-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="9c119-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="9c119-110">Вызывается:</span><span class="sxs-lookup"><span data-stu-id="9c119-110">Called by:</span></span>  <br/> |<span data-ttu-id="9c119-111">Клиентские приложения и поставщиков услуг</span><span class="sxs-lookup"><span data-stu-id="9c119-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
ULONG MAPIFreeBuffer(
  LPVOID lpBuffer
);
```

## <a name="parameters"></a><span data-ttu-id="9c119-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="9c119-112">Parameters</span></span>

 <span data-ttu-id="9c119-113">_lpBuffer_</span><span class="sxs-lookup"><span data-stu-id="9c119-113">_lpBuffer_</span></span>
  
> <span data-ttu-id="9c119-114">[in] Указатель на буфер ранее выделенной памяти.</span><span class="sxs-lookup"><span data-stu-id="9c119-114">[in] Pointer to a previously allocated memory buffer.</span></span> <span data-ttu-id="9c119-115">Если значение NULL передается в параметре _lpBuffer_ , **MAPIFreeBuffer** не имеет никакого эффекта.</span><span class="sxs-lookup"><span data-stu-id="9c119-115">If NULL is passed in the  _lpBuffer_ parameter, **MAPIFreeBuffer** does nothing.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="9c119-116">������������ ��������</span><span class="sxs-lookup"><span data-stu-id="9c119-116">Return value</span></span>

<span data-ttu-id="9c119-117">ЗНАЧЕНИЕ S_OK</span><span class="sxs-lookup"><span data-stu-id="9c119-117">S_OK</span></span> 
  
> <span data-ttu-id="9c119-118">Вызов успешно и освобождается память запрошено.</span><span class="sxs-lookup"><span data-stu-id="9c119-118">The call succeeded and freed the memory requested.</span></span> <span data-ttu-id="9c119-119">**MAPIFreeBuffer** может также возвращать значение S_OK на уже освобожденное расположения или если блок памяти не выделяется с **MAPIAllocateBuffer** и **MAPIAllocateMore**.</span><span class="sxs-lookup"><span data-stu-id="9c119-119">**MAPIFreeBuffer** can also return S_OK on already freed locations or if memory block is not allocated with **MAPIAllocateBuffer** and **MAPIAllocateMore**.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="9c119-120">Замечания</span><span class="sxs-lookup"><span data-stu-id="9c119-120">Remarks</span></span>

<span data-ttu-id="9c119-121">Как правило, когда клиентского приложения или поставщика услуг вызывает метод [MAPIAllocateBuffer](mapiallocatebuffer.md) или [MAPIAllocateMore](mapiallocatemore.md), конструкции операционной системы в одной непрерывной памяти буфера один или несколько сложных структур с несколькими уровнями указатели.</span><span class="sxs-lookup"><span data-stu-id="9c119-121">Usually, when a client application or service provider calls [MAPIAllocateBuffer](mapiallocatebuffer.md) or [MAPIAllocateMore](mapiallocatemore.md), the operating system constructs in one contiguous memory buffer one or more complex structures with multiple levels of pointers.</span></span> <span data-ttu-id="9c119-122">Когда функция MAPI или метод создает буфер с таким содержимым, клиента более поздней версии можно освободить все структуры, содержащихся в буфере, передав **MAPIFreeBuffer** указатель на буфер, возвращаемого функцией MAPI, которые созданы буфер.</span><span class="sxs-lookup"><span data-stu-id="9c119-122">When a MAPI function or method creates a buffer with such contents, a client can later free all the structures contained in the buffer by passing to **MAPIFreeBuffer** the pointer to the buffer returned by the MAPI function that created the buffer.</span></span> <span data-ttu-id="9c119-123">Для поставщика услуг освободить память буфера, используя **MAPIFreeBuffer**его необходимо передать указатель буфером, возвращаемых в объект поддержки поставщика.</span><span class="sxs-lookup"><span data-stu-id="9c119-123">For a service provider to free a memory buffer using **MAPIFreeBuffer**, it must pass the pointer to that buffer returned with the provider's support object.</span></span> 
  
<span data-ttu-id="9c119-124">Вызов **MAPIFreeBuffer** для освобождения определенного буфера должна состоять как можно скорее клиента или поставщика по завершении работы с помощью этого буфера.</span><span class="sxs-lookup"><span data-stu-id="9c119-124">The call to **MAPIFreeBuffer** to free a particular buffer must be made as soon as a client or provider is finished using this buffer.</span></span> <span data-ttu-id="9c119-125">Просто вызов метода [IMAPISession::Logoff](imapisession-logoff.md) в конце сеанса MAPI не освобождает автоматически буферов памяти.</span><span class="sxs-lookup"><span data-stu-id="9c119-125">Simply calling the [IMAPISession::Logoff](imapisession-logoff.md) method at the end of a MAPI session does not automatically release memory buffers.</span></span> 
  
<span data-ttu-id="9c119-126">Предварительное условие, указатель, переданный _lpBuffer_ является недопустимым после успешного возвращения из **MAPIFreeBuffer**следует работать клиента или поставщика.</span><span class="sxs-lookup"><span data-stu-id="9c119-126">A client or service provider should operate on the assumption that the pointer passed in  _lpBuffer_ is invalid after a successful return from **MAPIFreeBuffer**.</span></span> <span data-ttu-id="9c119-127">Если указатель мыши указывает блок памяти, не выделяются системой обмена сообщениями через **MAPIAllocateBuffer** или **MAPIAllocateMore** или блок свободной памяти, поведение **MAPIFreeBuffer** не определено.</span><span class="sxs-lookup"><span data-stu-id="9c119-127">If the pointer indicates either a memory block not allocated by the messaging system through **MAPIAllocateBuffer** or **MAPIAllocateMore** or a free memory block, the behavior of **MAPIFreeBuffer** is undefined.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="9c119-128">Передача указатель на значение null, в **MAPIFreeBuffer** делает код очистки приложения проще и меньшего размера так, как можно инициализировать указатели на значение NULL и освободить их код очистки без необходимости их необходимо протестировать сначала **MAPIFreeBuffer** .</span><span class="sxs-lookup"><span data-stu-id="9c119-128">Passing a null pointer to **MAPIFreeBuffer** makes application cleanup code simpler and smaller because **MAPIFreeBuffer** can initialize pointers to NULL and then free them in the cleanup code without having to test them first.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="9c119-129">См. также</span><span class="sxs-lookup"><span data-stu-id="9c119-129">See also</span></span>



[<span data-ttu-id="9c119-130">IMAPISupport::GetMemAllocRoutines</span><span class="sxs-lookup"><span data-stu-id="9c119-130">IMAPISupport::GetMemAllocRoutines</span></span>](imapisupport-getmemallocroutines.md)

