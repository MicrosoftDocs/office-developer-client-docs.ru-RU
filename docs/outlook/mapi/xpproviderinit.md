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
# <a name="xpproviderinit"></a><span data-ttu-id="d071c-103">XPProviderInit</span><span class="sxs-lookup"><span data-stu-id="d071c-103">XPProviderInit</span></span>

  
  
<span data-ttu-id="d071c-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d071c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d071c-105">Инициализирует поставщика транспорта для операции.</span><span class="sxs-lookup"><span data-stu-id="d071c-105">Initializes a transport provider for operation.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="d071c-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="d071c-106">Header file:</span></span>  <br/> |<span data-ttu-id="d071c-107">Mapispi.h</span><span class="sxs-lookup"><span data-stu-id="d071c-107">Mapispi.h</span></span>  <br/> |
|<span data-ttu-id="d071c-108">Реализовано в:</span><span class="sxs-lookup"><span data-stu-id="d071c-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="d071c-109">Поставщики транспорта</span><span class="sxs-lookup"><span data-stu-id="d071c-109">Transport providers</span></span>  <br/> |
|<span data-ttu-id="d071c-110">Вызывающая сторона:</span><span class="sxs-lookup"><span data-stu-id="d071c-110">Called by:</span></span>  <br/> |<span data-ttu-id="d071c-111">MAPI</span><span class="sxs-lookup"><span data-stu-id="d071c-111">MAPI</span></span>  <br/> |
   
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

## <a name="parameters"></a><span data-ttu-id="d071c-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="d071c-112">Parameters</span></span>

 <span data-ttu-id="d071c-113">_hInstance_</span><span class="sxs-lookup"><span data-stu-id="d071c-113">_hInstance_</span></span>
  
> <span data-ttu-id="d071c-114">[in] Экземпляр библиотеки динамической ссылки поставщика транспорта (DLL), используемой MAPI при загрузке библиотеки DLL.</span><span class="sxs-lookup"><span data-stu-id="d071c-114">[in] The instance of the transport provider's dynamic-link library (DLL) that MAPI used when it loaded the DLL.</span></span>
    
 <span data-ttu-id="d071c-115">_lpMalloc_</span><span class="sxs-lookup"><span data-stu-id="d071c-115">_lpMalloc_</span></span>
  
> <span data-ttu-id="d071c-116">[in] Указатель на объект-память для размещения интерфейса OLE **IMalloc.**</span><span class="sxs-lookup"><span data-stu-id="d071c-116">[in] Pointer to a memory allocator object exposing the OLE **IMalloc** interface.</span></span> <span data-ttu-id="d071c-117">Поставщику транспорта может потребоваться использовать этот метод выделения при работе с определенными интерфейсами, такими как **IStream.**</span><span class="sxs-lookup"><span data-stu-id="d071c-117">The transport provider may need to use this allocation method when working with certain interfaces such as **IStream**.</span></span> 
    
 <span data-ttu-id="d071c-118">_lpAllocateBuffer_</span><span class="sxs-lookup"><span data-stu-id="d071c-118">_lpAllocateBuffer_</span></span>
  
> <span data-ttu-id="d071c-119">[in] Указатель на [функцию MAPIAllocateBuffer,](mapiallocatebuffer.md) которая используется для выделения памяти.</span><span class="sxs-lookup"><span data-stu-id="d071c-119">[in] Pointer to the [MAPIAllocateBuffer](mapiallocatebuffer.md) function, to be used to allocate memory.</span></span> 
    
 <span data-ttu-id="d071c-120">_lpAllocateMore_</span><span class="sxs-lookup"><span data-stu-id="d071c-120">_lpAllocateMore_</span></span>
  
> <span data-ttu-id="d071c-121">[in] Указатель на [функцию MAPIAllocateMore,](mapiallocatemore.md) которая используется для выделения дополнительной памяти.</span><span class="sxs-lookup"><span data-stu-id="d071c-121">[in] Pointer to the [MAPIAllocateMore](mapiallocatemore.md) function, to be used to allocate additional memory.</span></span> 
    
 <span data-ttu-id="d071c-122">_lpFreeBuffer_</span><span class="sxs-lookup"><span data-stu-id="d071c-122">_lpFreeBuffer_</span></span>
  
> <span data-ttu-id="d071c-123">[in] Указатель на [функцию MAPIFreeBuffer,](mapifreebuffer.md) которая используется для освободить память.</span><span class="sxs-lookup"><span data-stu-id="d071c-123">[in] Pointer to the [MAPIFreeBuffer](mapifreebuffer.md) function, to be used to free memory.</span></span> 
    
 <span data-ttu-id="d071c-124">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="d071c-124">_ulFlags_</span></span>
  
> <span data-ttu-id="d071c-125">[in] Битоваяmas флагов.</span><span class="sxs-lookup"><span data-stu-id="d071c-125">[in] Bitmask of flags.</span></span> <span data-ttu-id="d071c-126">Можно установить следующий флаг:</span><span class="sxs-lookup"><span data-stu-id="d071c-126">The following flag can be set:</span></span>
    
<span data-ttu-id="d071c-127">MAPI_NT_SERVICE</span><span class="sxs-lookup"><span data-stu-id="d071c-127">MAPI_NT_SERVICE</span></span> 
  
> <span data-ttu-id="d071c-128">Поставщик загружается в контексте службы Windows — особого типа процесса без доступа к пользовательскому интерфейсу.</span><span class="sxs-lookup"><span data-stu-id="d071c-128">The provider is being loaded in the context of a Windows service, a special type of process without access to any user interface.</span></span> 
    
 <span data-ttu-id="d071c-129">_ulMAPIVer_</span><span class="sxs-lookup"><span data-stu-id="d071c-129">_ulMAPIVer_</span></span>
  
> <span data-ttu-id="d071c-130">[in] Номер версии интерфейса поставщика услуг (SPI), который Mapi.dll.</span><span class="sxs-lookup"><span data-stu-id="d071c-130">[in] Version number of the service provider interface (SPI) that Mapi.dll uses.</span></span> <span data-ttu-id="d071c-131">Номер текущей версии см. в файле заголовок Mapispi.h.</span><span class="sxs-lookup"><span data-stu-id="d071c-131">For the current version number, see the Mapispi.h header file.</span></span> 
    
 <span data-ttu-id="d071c-132">_lpulProviderVer_</span><span class="sxs-lookup"><span data-stu-id="d071c-132">_lpulProviderVer_</span></span>
  
> <span data-ttu-id="d071c-133">[out] Указатель на номер версии SPI, который использует этот поставщик транспорта.</span><span class="sxs-lookup"><span data-stu-id="d071c-133">[out] Pointer to the version number of the SPI that this transport provider uses.</span></span> 
    
 <span data-ttu-id="d071c-134">_lppXPProvider_</span><span class="sxs-lookup"><span data-stu-id="d071c-134">_lppXPProvider_</span></span>
  
> <span data-ttu-id="d071c-135">[out] Указатель на указатель на инициализированный объект поставщика транспорта.</span><span class="sxs-lookup"><span data-stu-id="d071c-135">[out] Pointer to a pointer to the initialized transport provider object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="d071c-136">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="d071c-136">Return value</span></span>

<span data-ttu-id="d071c-137">S_OK</span><span class="sxs-lookup"><span data-stu-id="d071c-137">S_OK</span></span> 
  
> <span data-ttu-id="d071c-138">����� ������� � ������ ��������� ��������� ��� ��������.</span><span class="sxs-lookup"><span data-stu-id="d071c-138">The call succeeded and has returned the expected value or values.</span></span> 
    
<span data-ttu-id="d071c-139">MAPI_E_VERSION</span><span class="sxs-lookup"><span data-stu-id="d071c-139">MAPI_E_VERSION</span></span> 
  
> <span data-ttu-id="d071c-140">Версия SPI, используемая MAPI, несовместима с SPI, используемым этим поставщиком.</span><span class="sxs-lookup"><span data-stu-id="d071c-140">The SPI version being used by MAPI is not compatible with the SPI being used by this provider.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="d071c-141">Примечания</span><span class="sxs-lookup"><span data-stu-id="d071c-141">Remarks</span></span>

<span data-ttu-id="d071c-142">MAPI вызывает функцию точки входа **XPProviderInit** для инициализации поставщика транспорта после входа клиента.</span><span class="sxs-lookup"><span data-stu-id="d071c-142">MAPI calls the entry point function **XPProviderInit** to initialize a transport provider following a client logon.</span></span> <span data-ttu-id="d071c-143">**XPProviderInit** будет вызван один раз для каждого поставщика транспорта, указанного в профиле клиента.</span><span class="sxs-lookup"><span data-stu-id="d071c-143">**XPProviderInit** is called once for each transport provider specified in the client's profile.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="d071c-144">Примечания для исполнителей</span><span class="sxs-lookup"><span data-stu-id="d071c-144">Notes to implementers</span></span>

<span data-ttu-id="d071c-145">Поставщик транспорта должен реализовать **XPProviderInit** в качестве функции точки входа в DLL поставщика.</span><span class="sxs-lookup"><span data-stu-id="d071c-145">A transport provider must implement **XPProviderInit** as an entry point function in the provider's DLL.</span></span> <span data-ttu-id="d071c-146">Реализация должна быть основана на прототипе **функции XPPROVIDERINIT,** который также указан в mapispi.h.</span><span class="sxs-lookup"><span data-stu-id="d071c-146">The implementation must be based on the **XPPROVIDERINIT** function prototype, also specified in Mapispi.h.</span></span> <span data-ttu-id="d071c-147">MAPI определяет **XPPROVIDERINIT** для использования стандартного типа вызова инициализации MAPI, STDMAPIINITCALLTYPE, что приводит к следуют соглашению о вызовах **XPProviderInit** CDECL.</span><span class="sxs-lookup"><span data-stu-id="d071c-147">MAPI defines **XPPROVIDERINIT** to use the standard MAPI initialization call type, STDMAPIINITCALLTYPE, which causes **XPProviderInit** to follow the CDECL calling convention.</span></span> <span data-ttu-id="d071c-148">Преимуществом CDECL является возможность попытки вызова, даже если количество параметров вызова не соответствует числу заданных параметров.</span><span class="sxs-lookup"><span data-stu-id="d071c-148">An advantage of CDECL is that calls can be attempted even if the number of calling parameters does not match the number of defined parameters.</span></span> 
  
<span data-ttu-id="d071c-149">Поставщик может быть инициализирован несколько раз в результате появления в нескольких профилях одновременного использования или появления более одного раза в одном профиле.</span><span class="sxs-lookup"><span data-stu-id="d071c-149">A provider can be initialized multiple times as a result of appearing in several profiles in simultaneous use or of appearing more than once in the same profile.</span></span> <span data-ttu-id="d071c-150">Так как объект поставщика содержит контекст, **XPProviderInit** должен возвращать другой объект поставщика в  _lppXPProvider_ для каждой инициализации даже для нескольких инициализации в одном процессе.</span><span class="sxs-lookup"><span data-stu-id="d071c-150">Because the provider object contains context, **XPProviderInit** must return a different provider object in  _lppXPProvider_ for each initialization, even for multiple initializations in the same process.</span></span> 
  
<span data-ttu-id="d071c-151">Поставщик транспорта должен использовать функции, на которые указывают  _lpAllocateBuffer,_  _lpAllocateMore_ и  _lpFreeBuffer_ для выделения и распределения памяти.</span><span class="sxs-lookup"><span data-stu-id="d071c-151">The transport provider should use the functions pointed to by  _lpAllocateBuffer_,  _lpAllocateMore_, and  _lpFreeBuffer_ for most memory allocation and deallocation.</span></span> <span data-ttu-id="d071c-152">В частности, поставщик должен использовать эти функции для выделения памяти для использования клиентских приложений при вызове интерфейсов объектов, таких как [IMAPIProp::GetProps](imapiprop-getprops.md) и [IMAPITable::QueryRows](imapitable-queryrows.md).</span><span class="sxs-lookup"><span data-stu-id="d071c-152">In particular, the provider must use these functions to allocate memory for use by client applications when calling object interfaces such as [IMAPIProp::GetProps](imapiprop-getprops.md) and [IMAPITable::QueryRows](imapitable-queryrows.md).</span></span> <span data-ttu-id="d071c-153">Если поставщик также ожидает использовать память OLE, он должен вызвать метод **IUnknown::AddRef** объекта allocator, на который указывает параметр _lpMalloc._</span><span class="sxs-lookup"><span data-stu-id="d071c-153">If the provider also expects to use the OLE memory allocator, it should call the **IUnknown::AddRef** method of the allocator object pointed to by the  _lpMalloc_ parameter.</span></span> 
  
<span data-ttu-id="d071c-154">Дополнительные сведения о **написании XPProviderInit** см. в [инициализации поставщика транспорта.](initializing-the-transport-provider.md)</span><span class="sxs-lookup"><span data-stu-id="d071c-154">For more information about writing **XPProviderInit**, see [Initializing the Transport Provider](initializing-the-transport-provider.md).</span></span> <span data-ttu-id="d071c-155">Дополнительные сведения о функциях точек входа см. в [реализации функции](implementing-a-service-provider-entry-point-function.md)точки входа поставщика услуг.</span><span class="sxs-lookup"><span data-stu-id="d071c-155">For more information about entry point functions, see [Implementing a Service Provider Entry Point Function](implementing-a-service-provider-entry-point-function.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="d071c-156">См. также</span><span class="sxs-lookup"><span data-stu-id="d071c-156">See also</span></span>



[<span data-ttu-id="d071c-157">ABProviderInit</span><span class="sxs-lookup"><span data-stu-id="d071c-157">ABProviderInit</span></span>](abproviderinit.md)
  
[<span data-ttu-id="d071c-158">IXPProvider : IUnknown</span><span class="sxs-lookup"><span data-stu-id="d071c-158">IXPProvider : IUnknown</span></span>](ixpprovideriunknown.md)
  
[<span data-ttu-id="d071c-159">MSProviderInit</span><span class="sxs-lookup"><span data-stu-id="d071c-159">MSProviderInit</span></span>](msproviderinit.md)

