---
title: XPProviderInit
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.XPProviderInit
api_type:
- COM
ms.assetid: df6eacf4-1cf9-4c25-806f-f87c38dad597
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: ee0ff8d32436f71020be2cdc91d6677bd4ec8e43
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428538"
---
# <a name="xpproviderinit"></a><span data-ttu-id="83b2e-103">XPProviderInit</span><span class="sxs-lookup"><span data-stu-id="83b2e-103">XPProviderInit</span></span>

  
  
<span data-ttu-id="83b2e-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="83b2e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="83b2e-105">Инициализирует поставщика транспорта для работы.</span><span class="sxs-lookup"><span data-stu-id="83b2e-105">Initializes a transport provider for operation.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="83b2e-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="83b2e-106">Header file:</span></span>  <br/> |<span data-ttu-id="83b2e-107">Mapispi.h</span><span class="sxs-lookup"><span data-stu-id="83b2e-107">Mapispi.h</span></span>  <br/> |
|<span data-ttu-id="83b2e-108">Реализовано в:</span><span class="sxs-lookup"><span data-stu-id="83b2e-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="83b2e-109">Поставщики транспорта</span><span class="sxs-lookup"><span data-stu-id="83b2e-109">Transport providers</span></span>  <br/> |
|<span data-ttu-id="83b2e-110">Вызывающая сторона:</span><span class="sxs-lookup"><span data-stu-id="83b2e-110">Called by:</span></span>  <br/> |<span data-ttu-id="83b2e-111">MAPI</span><span class="sxs-lookup"><span data-stu-id="83b2e-111">MAPI</span></span>  <br/> |
   
```cpp
HRESULT XPProviderInit(
  HINSTANCE hInstance,
  LPMALLOC lpMalloc,
  LPALLOCATEBUFFER lpAllocateBuffer,
  LPALLOCATEMORE lpAllocateMore,
  LPFREEBUFFER lpFreeBuffer,
  ULONG ulFlags,
  ULONG ulMAPIVer,
  ULONG FAR * lpulProviderVer,
  LPXPPROVIDER FAR * lppXPProvider
);
```

## <a name="parameters"></a><span data-ttu-id="83b2e-112">Parameters</span><span class="sxs-lookup"><span data-stu-id="83b2e-112">Parameters</span></span>

 <span data-ttu-id="83b2e-113">_hInstance_</span><span class="sxs-lookup"><span data-stu-id="83b2e-113">_hInstance_</span></span>
  
> <span data-ttu-id="83b2e-114">[in] Экземпляр библиотеки динамических ссылок поставщика транспорта (DLL), используемой MAPI при загрузке DLL.</span><span class="sxs-lookup"><span data-stu-id="83b2e-114">[in] The instance of the transport provider's dynamic-link library (DLL) that MAPI used when it loaded the DLL.</span></span>
    
 <span data-ttu-id="83b2e-115">_lpMalloc_</span><span class="sxs-lookup"><span data-stu-id="83b2e-115">_lpMalloc_</span></span>
  
> <span data-ttu-id="83b2e-116">[in] Указатель на объект-аллигатор памяти, подвергая обнажает интерфейс OLE **IMalloc.**</span><span class="sxs-lookup"><span data-stu-id="83b2e-116">[in] Pointer to a memory allocator object exposing the OLE **IMalloc** interface.</span></span> <span data-ttu-id="83b2e-117">Поставщику транспорта может потребоваться использовать этот метод выделения при работе с определенными интерфейсами, такими как **IStream.**</span><span class="sxs-lookup"><span data-stu-id="83b2e-117">The transport provider may need to use this allocation method when working with certain interfaces such as **IStream**.</span></span> 
    
 <span data-ttu-id="83b2e-118">_lpAllocateBuffer_</span><span class="sxs-lookup"><span data-stu-id="83b2e-118">_lpAllocateBuffer_</span></span>
  
> <span data-ttu-id="83b2e-119">[in] Указатель на [функцию MAPIAllocateBuffer,](mapiallocatebuffer.md) которая будет использоваться для выделения памяти.</span><span class="sxs-lookup"><span data-stu-id="83b2e-119">[in] Pointer to the [MAPIAllocateBuffer](mapiallocatebuffer.md) function, to be used to allocate memory.</span></span> 
    
 <span data-ttu-id="83b2e-120">_lpAllocateMore_</span><span class="sxs-lookup"><span data-stu-id="83b2e-120">_lpAllocateMore_</span></span>
  
> <span data-ttu-id="83b2e-121">[in] Указатель на функцию [MAPIAllocateMore,](mapiallocatemore.md) которая будет использоваться для выделения дополнительной памяти.</span><span class="sxs-lookup"><span data-stu-id="83b2e-121">[in] Pointer to the [MAPIAllocateMore](mapiallocatemore.md) function, to be used to allocate additional memory.</span></span> 
    
 <span data-ttu-id="83b2e-122">_lpFreeBuffer_</span><span class="sxs-lookup"><span data-stu-id="83b2e-122">_lpFreeBuffer_</span></span>
  
> <span data-ttu-id="83b2e-123">[in] Указатель на функцию [MAPIFreeBuffer,](mapifreebuffer.md) которая будет использоваться для бесплатной памяти.</span><span class="sxs-lookup"><span data-stu-id="83b2e-123">[in] Pointer to the [MAPIFreeBuffer](mapifreebuffer.md) function, to be used to free memory.</span></span> 
    
 <span data-ttu-id="83b2e-124">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="83b2e-124">_ulFlags_</span></span>
  
> <span data-ttu-id="83b2e-125">[in] Bitmask флагов.</span><span class="sxs-lookup"><span data-stu-id="83b2e-125">[in] Bitmask of flags.</span></span> <span data-ttu-id="83b2e-126">Можно установить следующий флаг:</span><span class="sxs-lookup"><span data-stu-id="83b2e-126">The following flag can be set:</span></span>
    
<span data-ttu-id="83b2e-127">MAPI_NT_SERVICE</span><span class="sxs-lookup"><span data-stu-id="83b2e-127">MAPI_NT_SERVICE</span></span> 
  
> <span data-ttu-id="83b2e-128">Поставщик загружается в контексте службы Windows, особого типа процесса без доступа к любому пользовательскому интерфейсу.</span><span class="sxs-lookup"><span data-stu-id="83b2e-128">The provider is being loaded in the context of a Windows service, a special type of process without access to any user interface.</span></span> 
    
 <span data-ttu-id="83b2e-129">_ulMAPIVer_</span><span class="sxs-lookup"><span data-stu-id="83b2e-129">_ulMAPIVer_</span></span>
  
> <span data-ttu-id="83b2e-130">[in] Номер версии интерфейса поставщика услуг (SPI), который Mapi.dll использует.</span><span class="sxs-lookup"><span data-stu-id="83b2e-130">[in] Version number of the service provider interface (SPI) that Mapi.dll uses.</span></span> <span data-ttu-id="83b2e-131">Для текущего номера версии см. файл заголовки Mapispi.h.</span><span class="sxs-lookup"><span data-stu-id="83b2e-131">For the current version number, see the Mapispi.h header file.</span></span> 
    
 <span data-ttu-id="83b2e-132">_lpulProviderVer_</span><span class="sxs-lookup"><span data-stu-id="83b2e-132">_lpulProviderVer_</span></span>
  
> <span data-ttu-id="83b2e-133">[вышел] Указатель на номер версии SPI, который использует этот поставщик транспорта.</span><span class="sxs-lookup"><span data-stu-id="83b2e-133">[out] Pointer to the version number of the SPI that this transport provider uses.</span></span> 
    
 <span data-ttu-id="83b2e-134">_lppXPProvider_</span><span class="sxs-lookup"><span data-stu-id="83b2e-134">_lppXPProvider_</span></span>
  
> <span data-ttu-id="83b2e-135">[вышел] Указатель на указатель на инициализированный объект поставщика транспорта.</span><span class="sxs-lookup"><span data-stu-id="83b2e-135">[out] Pointer to a pointer to the initialized transport provider object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="83b2e-136">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="83b2e-136">Return value</span></span>

<span data-ttu-id="83b2e-137">S_OK</span><span class="sxs-lookup"><span data-stu-id="83b2e-137">S_OK</span></span> 
  
> <span data-ttu-id="83b2e-138">����� ������� � ������ ��������� ��������� ��� ��������.</span><span class="sxs-lookup"><span data-stu-id="83b2e-138">The call succeeded and has returned the expected value or values.</span></span> 
    
<span data-ttu-id="83b2e-139">MAPI_E_VERSION</span><span class="sxs-lookup"><span data-stu-id="83b2e-139">MAPI_E_VERSION</span></span> 
  
> <span data-ttu-id="83b2e-140">Версия SPI, используемая MAPI, не совместима с spi, используемым этим поставщиком.</span><span class="sxs-lookup"><span data-stu-id="83b2e-140">The SPI version being used by MAPI is not compatible with the SPI being used by this provider.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="83b2e-141">Примечания</span><span class="sxs-lookup"><span data-stu-id="83b2e-141">Remarks</span></span>

<span data-ttu-id="83b2e-142">MAPI вызывает функцию точки входа **XPProviderInit** для инициализации поставщика транспорта после логотипа клиента.</span><span class="sxs-lookup"><span data-stu-id="83b2e-142">MAPI calls the entry point function **XPProviderInit** to initialize a transport provider following a client logon.</span></span> <span data-ttu-id="83b2e-143">**XPProviderInit** вызван один раз для каждого поставщика транспорта, указанного в профиле клиента.</span><span class="sxs-lookup"><span data-stu-id="83b2e-143">**XPProviderInit** is called once for each transport provider specified in the client's profile.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="83b2e-144">Примечания для исполнителей</span><span class="sxs-lookup"><span data-stu-id="83b2e-144">Notes to implementers</span></span>

<span data-ttu-id="83b2e-145">Поставщик транспорта должен реализовать **XPProviderInit** в качестве функции точки входа в DLL поставщика.</span><span class="sxs-lookup"><span data-stu-id="83b2e-145">A transport provider must implement **XPProviderInit** as an entry point function in the provider's DLL.</span></span> <span data-ttu-id="83b2e-146">Реализация должна основываться на прототипе **функции XPPROVIDERINIT,** также указанном в Mapispi.h.</span><span class="sxs-lookup"><span data-stu-id="83b2e-146">The implementation must be based on the **XPPROVIDERINIT** function prototype, also specified in Mapispi.h.</span></span> <span data-ttu-id="83b2e-147">MAPI определяет **XPPROVIDERINIT** для использования стандартного типа вызовов инициализации MAPI STDMAPIINITCALLTYPE, из-за чего **XPProviderInit** следует конвенции вызова CDECL.</span><span class="sxs-lookup"><span data-stu-id="83b2e-147">MAPI defines **XPPROVIDERINIT** to use the standard MAPI initialization call type, STDMAPIINITCALLTYPE, which causes **XPProviderInit** to follow the CDECL calling convention.</span></span> <span data-ttu-id="83b2e-148">ПреимуществоМ CDECL является то, что вызовы можно предпринять даже в том случае, если количество параметров вызова не соответствует количеству заданных параметров.</span><span class="sxs-lookup"><span data-stu-id="83b2e-148">An advantage of CDECL is that calls can be attempted even if the number of calling parameters does not match the number of defined parameters.</span></span> 
  
<span data-ttu-id="83b2e-149">Поставщик может быть инициализирован несколько раз в результате появления в нескольких профилях одновременного использования или более одного раза в одном профиле.</span><span class="sxs-lookup"><span data-stu-id="83b2e-149">A provider can be initialized multiple times as a result of appearing in several profiles in simultaneous use or of appearing more than once in the same profile.</span></span> <span data-ttu-id="83b2e-150">Так как объект поставщика содержит контекст, **XPProviderInit** должен возвращать другой объект поставщика  _в lppXPProvider_ для каждой инициализации даже для нескольких инициализации в одном и том же процессе.</span><span class="sxs-lookup"><span data-stu-id="83b2e-150">Because the provider object contains context, **XPProviderInit** must return a different provider object in  _lppXPProvider_ for each initialization, even for multiple initializations in the same process.</span></span> 
  
<span data-ttu-id="83b2e-151">Поставщик транспорта должен использовать функции, на которые указывает  _lpAllocateBuffer,_  _lpAllocateMore_ и  _lpFreeBuffer_ для большинства распределений памяти и deallocation.</span><span class="sxs-lookup"><span data-stu-id="83b2e-151">The transport provider should use the functions pointed to by  _lpAllocateBuffer_,  _lpAllocateMore_, and  _lpFreeBuffer_ for most memory allocation and deallocation.</span></span> <span data-ttu-id="83b2e-152">В частности, поставщик должен использовать эти функции для выделения памяти для использования в клиентских приложениях при вызове интерфейсов объектов, таких как [IMAPIProp::GetProps](imapiprop-getprops.md) и [IMAPITable::QueryRows](imapitable-queryrows.md).</span><span class="sxs-lookup"><span data-stu-id="83b2e-152">In particular, the provider must use these functions to allocate memory for use by client applications when calling object interfaces such as [IMAPIProp::GetProps](imapiprop-getprops.md) and [IMAPITable::QueryRows](imapitable-queryrows.md).</span></span> <span data-ttu-id="83b2e-153">Если поставщик также рассчитывает использовать аллигатор памяти OLE, он должен вызвать **метод IUnknown::AddRef** объекта-аллигатора, на который указывает параметр _lpMalloc._</span><span class="sxs-lookup"><span data-stu-id="83b2e-153">If the provider also expects to use the OLE memory allocator, it should call the **IUnknown::AddRef** method of the allocator object pointed to by the  _lpMalloc_ parameter.</span></span> 
  
<span data-ttu-id="83b2e-154">Дополнительные сведения о **написании XPProviderInit** см. в [инициализации поставщика транспорта.](initializing-the-transport-provider.md)</span><span class="sxs-lookup"><span data-stu-id="83b2e-154">For more information about writing **XPProviderInit**, see [Initializing the Transport Provider](initializing-the-transport-provider.md).</span></span> <span data-ttu-id="83b2e-155">Дополнительные сведения о функциях точек входа см. в см. в нем [Implementing a Service Provider Entry Point Function.](implementing-a-service-provider-entry-point-function.md)</span><span class="sxs-lookup"><span data-stu-id="83b2e-155">For more information about entry point functions, see [Implementing a Service Provider Entry Point Function](implementing-a-service-provider-entry-point-function.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="83b2e-156">См. также</span><span class="sxs-lookup"><span data-stu-id="83b2e-156">See also</span></span>



[<span data-ttu-id="83b2e-157">ABProviderInit</span><span class="sxs-lookup"><span data-stu-id="83b2e-157">ABProviderInit</span></span>](abproviderinit.md)
  
[<span data-ttu-id="83b2e-158">IXPProvider : IUnknown</span><span class="sxs-lookup"><span data-stu-id="83b2e-158">IXPProvider : IUnknown</span></span>](ixpprovideriunknown.md)
  
[<span data-ttu-id="83b2e-159">MSProviderInit</span><span class="sxs-lookup"><span data-stu-id="83b2e-159">MSProviderInit</span></span>](msproviderinit.md)

