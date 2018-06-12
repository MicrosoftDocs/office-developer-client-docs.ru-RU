---
title: ABProviderInit
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ABProviderInit
api_type:
- HeaderDef
ms.assetid: c3dcd0d4-018a-47b0-b040-227034ed59d8
description: '���� ���������� ���������: 9 ����� 2015 �.'
ms.openlocfilehash: 03375a11be3f6f128db5f6147c5fbe901d0a0fa9
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19807990"
---
# <a name="abproviderinit"></a><span data-ttu-id="e13f1-103">ABProviderInit</span><span class="sxs-lookup"><span data-stu-id="e13f1-103">ABProviderInit</span></span>
 
<span data-ttu-id="e13f1-104">**Применимо к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="e13f1-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="e13f1-105">Инициализирует поставщика адресных книг для операции.</span><span class="sxs-lookup"><span data-stu-id="e13f1-105">Initializes an address book provider for operation.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="e13f1-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="e13f1-106">Header file:</span></span>  <br/> |<span data-ttu-id="e13f1-107">Mapispi.h</span><span class="sxs-lookup"><span data-stu-id="e13f1-107">Mapispi.h</span></span>  <br/> |
|<span data-ttu-id="e13f1-108">Реализованный:</span><span class="sxs-lookup"><span data-stu-id="e13f1-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="e13f1-109">Поставщиками адресных книг</span><span class="sxs-lookup"><span data-stu-id="e13f1-109">Address book providers</span></span>  <br/> |
|<span data-ttu-id="e13f1-110">Вызывается:</span><span class="sxs-lookup"><span data-stu-id="e13f1-110">Called by:</span></span>  <br/> |<span data-ttu-id="e13f1-111">MAPI</span><span class="sxs-lookup"><span data-stu-id="e13f1-111">MAPI</span></span>  <br/> |
   
```cpp
HRESULT ABProviderInit(
  HINSTANCE hInstance,
  LPMALLOC lpMalloc,
  LPALLOCATEBUFFER lpAllocateBuffer,
  LPALLOCATEMORE lpAllocateMore,
  LPFREEBUFFER lpFreeBuffer,
  ULONG ulFlags,
  ULONG ulMAPIVer,
  ULONG FAR * lpulProviderVer,
  LPABPROVIDER FAR * lppABProvider
);
```

## <a name="parameters"></a><span data-ttu-id="e13f1-112">Parameters</span><span class="sxs-lookup"><span data-stu-id="e13f1-112">Parameters</span></span>

 <span data-ttu-id="e13f1-113">_hInstance_</span><span class="sxs-lookup"><span data-stu-id="e13f1-113">_hInstance_</span></span>
  
> <span data-ttu-id="e13f1-114">[in] Экземпляр поставщик адресной книги динамической библиотеки (DLL), который используется MAPI, когда она связана.</span><span class="sxs-lookup"><span data-stu-id="e13f1-114">[in] The instance of the address book provider's dynamic-link library (DLL) that MAPI used when it linked.</span></span> 
    
 <span data-ttu-id="e13f1-115">_lpMalloc_</span><span class="sxs-lookup"><span data-stu-id="e13f1-115">_lpMalloc_</span></span>
  
> <span data-ttu-id="e13f1-116">[in] Указатель на объект распределителя памяти, предоставление интерфейса OLE **IMalloc** .</span><span class="sxs-lookup"><span data-stu-id="e13f1-116">[in] Pointer to a memory allocator object exposing the OLE **IMalloc** interface.</span></span> <span data-ttu-id="e13f1-117">Поставщик адресной книги может потребоваться использовать этот метод для распределения при работе с определенных интерфейсов, таких как **IStream**.</span><span class="sxs-lookup"><span data-stu-id="e13f1-117">The address book provider may need to use this allocation method when working with certain interfaces such as **IStream**.</span></span> 
    
 <span data-ttu-id="e13f1-118">_lpAllocateBuffer_</span><span class="sxs-lookup"><span data-stu-id="e13f1-118">_lpAllocateBuffer_</span></span>
  
> <span data-ttu-id="e13f1-119">[in] Указатель на функцию [MAPIAllocateBuffer](mapiallocatebuffer.md) для использования где по MAPI требуется выделить память.</span><span class="sxs-lookup"><span data-stu-id="e13f1-119">[in] Pointer to the [MAPIAllocateBuffer](mapiallocatebuffer.md) function, to be used where required by MAPI to allocate memory.</span></span> 
    
 <span data-ttu-id="e13f1-120">_lpAllocateMore_</span><span class="sxs-lookup"><span data-stu-id="e13f1-120">_lpAllocateMore_</span></span>
  
> <span data-ttu-id="e13f1-121">[in] Указатель на функцию [MAPIAllocateMore](mapiallocatemore.md) для использования где по MAPI требуется для выделения дополнительной памяти.</span><span class="sxs-lookup"><span data-stu-id="e13f1-121">[in] Pointer to the [MAPIAllocateMore](mapiallocatemore.md) function, to be used where required by MAPI to allocate additional memory.</span></span> 
    
 <span data-ttu-id="e13f1-122">_lpFreeBuffer_</span><span class="sxs-lookup"><span data-stu-id="e13f1-122">_lpFreeBuffer_</span></span>
  
> <span data-ttu-id="e13f1-123">[in] Указатель на функцию [MAPIFreeBuffer](mapifreebuffer.md) для использования где по MAPI требуется свободной памяти.</span><span class="sxs-lookup"><span data-stu-id="e13f1-123">[in] Pointer to the [MAPIFreeBuffer](mapifreebuffer.md) function, to be used where required by MAPI to free memory.</span></span> 
    
 <span data-ttu-id="e13f1-124">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="e13f1-124">_ulFlags_</span></span>
  
> <span data-ttu-id="e13f1-125">[in] Битовая маска флаги.</span><span class="sxs-lookup"><span data-stu-id="e13f1-125">[in] Bitmask of flags.</span></span> <span data-ttu-id="e13f1-126">Можно задать следующий флаг:</span><span class="sxs-lookup"><span data-stu-id="e13f1-126">The following flag can be set:</span></span>
    
<span data-ttu-id="e13f1-127">MAPI_NT_SERVICE</span><span class="sxs-lookup"><span data-stu-id="e13f1-127">MAPI_NT_SERVICE</span></span> 
  
> <span data-ttu-id="e13f1-128">Поставщик загружается в контексте службы Windows, особый тип процесса без доступа к любой пользовательский интерфейс.</span><span class="sxs-lookup"><span data-stu-id="e13f1-128">The provider is being loaded in the context of a Windows service, a special type of process without access to any user interface.</span></span> 
    
 <span data-ttu-id="e13f1-129">_ulMAPIVer_</span><span class="sxs-lookup"><span data-stu-id="e13f1-129">_ulMAPIVer_</span></span>
  
> <span data-ttu-id="e13f1-130">[in] Номер версии интерфейса поставщика службы (SPI), MAPI. Использует библиотеку DLL.</span><span class="sxs-lookup"><span data-stu-id="e13f1-130">[in] Version number of the service provider interface (SPI) that MAPI.DLL uses.</span></span> <span data-ttu-id="e13f1-131">Текущий номер версии в разделе MAPISPI. Файл заголовка.</span><span class="sxs-lookup"><span data-stu-id="e13f1-131">For the current version number, see the MAPISPI.H header file.</span></span> 
    
 <span data-ttu-id="e13f1-132">_lpulProviderVer_</span><span class="sxs-lookup"><span data-stu-id="e13f1-132">_lpulProviderVer_</span></span>
  
> <span data-ttu-id="e13f1-133">[out] Указатель на номер версии индекс параметров безопасности, которая использует этот поставщик адресной книги.</span><span class="sxs-lookup"><span data-stu-id="e13f1-133">[out] Pointer to the version number of the SPI that this address book provider uses.</span></span> 
    
 <span data-ttu-id="e13f1-134">_lppABProvider_</span><span class="sxs-lookup"><span data-stu-id="e13f1-134">_lppABProvider_</span></span>
  
> <span data-ttu-id="e13f1-135">[out] Указатель на указатель на объект поставщика инициализированную адресной книги.</span><span class="sxs-lookup"><span data-stu-id="e13f1-135">[out] Pointer to a pointer to the initialized address book provider object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="e13f1-136">������������ ��������</span><span class="sxs-lookup"><span data-stu-id="e13f1-136">Return value</span></span>

<span data-ttu-id="e13f1-137">ЗНАЧЕНИЕ S_OK</span><span class="sxs-lookup"><span data-stu-id="e13f1-137">S_OK</span></span> 
  
> <span data-ttu-id="e13f1-138">����� ������� � ������ ��������� ��������� ��� ��������.</span><span class="sxs-lookup"><span data-stu-id="e13f1-138">The call succeeded and has returned the expected value or values.</span></span> 
    
<span data-ttu-id="e13f1-139">MAPI_E_VERSION</span><span class="sxs-lookup"><span data-stu-id="e13f1-139">MAPI_E_VERSION</span></span> 
  
> <span data-ttu-id="e13f1-140">Версия SPI, используемые MAPI не совместимый с индекс параметров безопасности, используемые этим поставщиком.</span><span class="sxs-lookup"><span data-stu-id="e13f1-140">The SPI version being used by MAPI is not compatible with the SPI being used by this provider.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="e13f1-141">Замечания</span><span class="sxs-lookup"><span data-stu-id="e13f1-141">Remarks</span></span>

<span data-ttu-id="e13f1-142">MAPI вызывает функцию точки входа **ABProviderInit** для инициализации поставщика адресных книг после входа клиента.</span><span class="sxs-lookup"><span data-stu-id="e13f1-142">MAPI calls the entry point function **ABProviderInit** to initialize an address book provider following a client logon.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="e13f1-143">Примечания для исполнителей</span><span class="sxs-lookup"><span data-stu-id="e13f1-143">Notes to implementers</span></span>

<span data-ttu-id="e13f1-144">Поставщик адресной книги необходимо реализовать **ABProviderInit** как функцию точки входа в DLL поставщика.</span><span class="sxs-lookup"><span data-stu-id="e13f1-144">An address book provider must implement **ABProviderInit** as an entry point function in the provider's DLL.</span></span> <span data-ttu-id="e13f1-145">Реализация должны быть основаны на прототип функции **ABPROVIDERINIT** также указано в MAPISPI. З.</span><span class="sxs-lookup"><span data-stu-id="e13f1-145">The implementation must be based on the **ABPROVIDERINIT** function prototype, also specified in MAPISPI.H.</span></span> <span data-ttu-id="e13f1-146">MAPI определяет **ABPROVIDERINIT** для использования типа стандартный вызова инициализации MAPI, STDMAPIINITCALLTYPE, что активирует **ABProviderInit** необходимо выполнить соглашение о вызовах CDECL.</span><span class="sxs-lookup"><span data-stu-id="e13f1-146">MAPI defines **ABPROVIDERINIT** to use the standard MAPI initialization call type, STDMAPIINITCALLTYPE, which causes **ABProviderInit** to follow the CDECL calling convention.</span></span> 
  
<span data-ttu-id="e13f1-147">Поставщик может быть инициализирован несколько раз, из-за изображения которых появляются в несколько профилей в одновременное использование или отображение более одного раза в одном профиле.</span><span class="sxs-lookup"><span data-stu-id="e13f1-147">A provider can be initialized multiple times, as a result of appearing in several profiles in simultaneous use or of appearing more than once in the same profile.</span></span> <span data-ttu-id="e13f1-148">Поскольку объект поставщика содержит контекста, **ABProviderInit** необходимо возвратить объект другого поставщика в _lppABProvider_ для каждой инициализации, даже для нескольких инициализации в одном процессе.</span><span class="sxs-lookup"><span data-stu-id="e13f1-148">Because the provider object contains context, **ABProviderInit** must return a different provider object in  _lppABProvider_ for each initialization, even for multiple initializations in the same process.</span></span> 
  
<span data-ttu-id="e13f1-149">Поставщик адресной книги следует использовать функции, на который указывает _lpAllocateBuffer_, _lpAllocateMore_и _lpFreeBuffer_ для большинства выделение и освобождение памяти.</span><span class="sxs-lookup"><span data-stu-id="e13f1-149">The address book provider should use the functions pointed to by  _lpAllocateBuffer_,  _lpAllocateMore_, and  _lpFreeBuffer_ for most memory allocation and deallocation.</span></span> <span data-ttu-id="e13f1-150">В частности поставщик должен использовать эти функции для выделения памяти для использования с клиентскими приложениями при вызове интерфейсы объекта, такие как [IMAPIProp::GetProps](imapiprop-getprops.md) и [IMAPITable::QueryRows](imapitable-queryrows.md).</span><span class="sxs-lookup"><span data-stu-id="e13f1-150">In particular, the provider must use these functions to allocate memory for use by client applications when calling object interfaces such as [IMAPIProp::GetProps](imapiprop-getprops.md) and [IMAPITable::QueryRows](imapitable-queryrows.md).</span></span> <span data-ttu-id="e13f1-151">Если поставщик также требуется для использования распределителя памяти OLE, он должен вызвать метод **IUnknown::AddRef** распределителя объект, указанный в параметре _lpMalloc_ .</span><span class="sxs-lookup"><span data-stu-id="e13f1-151">If the provider also expects to use the OLE memory allocator, it should call the **IUnknown::AddRef** method of the allocator object pointed to by the  _lpMalloc_ parameter.</span></span> 
  
<span data-ttu-id="e13f1-152">Дополнительные сведения о создании **ABProviderInit** [Функцию адресной книги поставщика](implementing-an-address-book-provider-entry-point-function.md)см.</span><span class="sxs-lookup"><span data-stu-id="e13f1-152">For more information on writing **ABProviderInit**, see [Implementing an Address Book Provider Entry Point Function](implementing-an-address-book-provider-entry-point-function.md).</span></span> <span data-ttu-id="e13f1-153">Дополнительные сведения о функциях точки входа [реализации функции выберите запись службы поставщика](implementing-a-service-provider-entry-point-function.md)см.</span><span class="sxs-lookup"><span data-stu-id="e13f1-153">For more information on entry point functions, see [Implementing a Service Provider Entry Point Function](implementing-a-service-provider-entry-point-function.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="e13f1-154">См. также</span><span class="sxs-lookup"><span data-stu-id="e13f1-154">See also</span></span>

- [<span data-ttu-id="e13f1-155">IABProvider: IUnknown</span><span class="sxs-lookup"><span data-stu-id="e13f1-155">IABProvider : IUnknown</span></span>](iabprovideriunknown.md) 
- [<span data-ttu-id="e13f1-156">MSProviderInit</span><span class="sxs-lookup"><span data-stu-id="e13f1-156">MSProviderInit</span></span>](msproviderinit.md)
- [<span data-ttu-id="e13f1-157">XPProviderInit</span><span class="sxs-lookup"><span data-stu-id="e13f1-157">XPProviderInit</span></span>](xpproviderinit.md)

