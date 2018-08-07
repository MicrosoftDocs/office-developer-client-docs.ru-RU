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
ms.openlocfilehash: 0415e782a98102314ce732f744c0d29590f646c2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19812622"
---
# <a name="xpproviderinit"></a><span data-ttu-id="697fa-103">XPProviderInit</span><span class="sxs-lookup"><span data-stu-id="697fa-103">XPProviderInit</span></span>

  
  
<span data-ttu-id="697fa-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="697fa-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="697fa-105">Инициализирует поставщика транспорта для операции.</span><span class="sxs-lookup"><span data-stu-id="697fa-105">Initializes a transport provider for operation.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="697fa-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="697fa-106">Header file:</span></span>  <br/> |<span data-ttu-id="697fa-107">Mapispi.h</span><span class="sxs-lookup"><span data-stu-id="697fa-107">Mapispi.h</span></span>  <br/> |
|<span data-ttu-id="697fa-108">Реализованный:</span><span class="sxs-lookup"><span data-stu-id="697fa-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="697fa-109">Поставщиками транспорта</span><span class="sxs-lookup"><span data-stu-id="697fa-109">Transport providers</span></span>  <br/> |
|<span data-ttu-id="697fa-110">Вызывается:</span><span class="sxs-lookup"><span data-stu-id="697fa-110">Called by:</span></span>  <br/> |<span data-ttu-id="697fa-111">MAPI</span><span class="sxs-lookup"><span data-stu-id="697fa-111">MAPI</span></span>  <br/> |
   
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

## <a name="parameters"></a><span data-ttu-id="697fa-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="697fa-112">Parameters</span></span>

 <span data-ttu-id="697fa-113">_hInstance_</span><span class="sxs-lookup"><span data-stu-id="697fa-113">_hInstance_</span></span>
  
> <span data-ttu-id="697fa-114">[in] Экземпляр поставщика транспорта динамической библиотеки (DLL), MAPI, используемой при загрузке DLL.</span><span class="sxs-lookup"><span data-stu-id="697fa-114">[in] The instance of the transport provider's dynamic-link library (DLL) that MAPI used when it loaded the DLL.</span></span>
    
 <span data-ttu-id="697fa-115">_lpMalloc_</span><span class="sxs-lookup"><span data-stu-id="697fa-115">_lpMalloc_</span></span>
  
> <span data-ttu-id="697fa-116">[in] Указатель на объект распределителя памяти, предоставление интерфейса OLE **IMalloc** .</span><span class="sxs-lookup"><span data-stu-id="697fa-116">[in] Pointer to a memory allocator object exposing the OLE **IMalloc** interface.</span></span> <span data-ttu-id="697fa-117">Поставщика транспорта может потребоваться использовать этот метод для распределения при работе с определенных интерфейсов, таких как **IStream**.</span><span class="sxs-lookup"><span data-stu-id="697fa-117">The transport provider may need to use this allocation method when working with certain interfaces such as **IStream**.</span></span> 
    
 <span data-ttu-id="697fa-118">_lpAllocateBuffer_</span><span class="sxs-lookup"><span data-stu-id="697fa-118">_lpAllocateBuffer_</span></span>
  
> <span data-ttu-id="697fa-119">[in] Указатель на функцию [MAPIAllocateBuffer](mapiallocatebuffer.md) , которые будут использоваться для выделения памяти.</span><span class="sxs-lookup"><span data-stu-id="697fa-119">[in] Pointer to the [MAPIAllocateBuffer](mapiallocatebuffer.md) function, to be used to allocate memory.</span></span> 
    
 <span data-ttu-id="697fa-120">_lpAllocateMore_</span><span class="sxs-lookup"><span data-stu-id="697fa-120">_lpAllocateMore_</span></span>
  
> <span data-ttu-id="697fa-121">[in] Указатель на функцию [MAPIAllocateMore](mapiallocatemore.md) , которые будут использоваться для выделения дополнительной памяти.</span><span class="sxs-lookup"><span data-stu-id="697fa-121">[in] Pointer to the [MAPIAllocateMore](mapiallocatemore.md) function, to be used to allocate additional memory.</span></span> 
    
 <span data-ttu-id="697fa-122">_lpFreeBuffer_</span><span class="sxs-lookup"><span data-stu-id="697fa-122">_lpFreeBuffer_</span></span>
  
> <span data-ttu-id="697fa-123">[in] Указатель на функцию [MAPIFreeBuffer](mapifreebuffer.md) , которые будут использоваться для свободного использования памяти.</span><span class="sxs-lookup"><span data-stu-id="697fa-123">[in] Pointer to the [MAPIFreeBuffer](mapifreebuffer.md) function, to be used to free memory.</span></span> 
    
 <span data-ttu-id="697fa-124">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="697fa-124">_ulFlags_</span></span>
  
> <span data-ttu-id="697fa-125">[in] Битовая маска флаги.</span><span class="sxs-lookup"><span data-stu-id="697fa-125">[in] Bitmask of flags.</span></span> <span data-ttu-id="697fa-126">Можно задать следующий флаг:</span><span class="sxs-lookup"><span data-stu-id="697fa-126">The following flag can be set:</span></span>
    
<span data-ttu-id="697fa-127">MAPI_NT_SERVICE</span><span class="sxs-lookup"><span data-stu-id="697fa-127">MAPI_NT_SERVICE</span></span> 
  
> <span data-ttu-id="697fa-128">Поставщик загружается в контексте службы Windows, особый тип процесса без доступа к любой пользовательский интерфейс.</span><span class="sxs-lookup"><span data-stu-id="697fa-128">The provider is being loaded in the context of a Windows service, a special type of process without access to any user interface.</span></span> 
    
 <span data-ttu-id="697fa-129">_ulMAPIVer_</span><span class="sxs-lookup"><span data-stu-id="697fa-129">_ulMAPIVer_</span></span>
  
> <span data-ttu-id="697fa-130">[in] Номер версии поставщика службы интерфейса (SPI), который использует Mapi.dll.</span><span class="sxs-lookup"><span data-stu-id="697fa-130">[in] Version number of the service provider interface (SPI) that Mapi.dll uses.</span></span> <span data-ttu-id="697fa-131">Файл заголовка Mapispi.h текущий номер версии, см.</span><span class="sxs-lookup"><span data-stu-id="697fa-131">For the current version number, see the Mapispi.h header file.</span></span> 
    
 <span data-ttu-id="697fa-132">_lpulProviderVer_</span><span class="sxs-lookup"><span data-stu-id="697fa-132">_lpulProviderVer_</span></span>
  
> <span data-ttu-id="697fa-133">[out] Указатель на номер версии индекс параметров безопасности, которая использует этот поставщик транспорта.</span><span class="sxs-lookup"><span data-stu-id="697fa-133">[out] Pointer to the version number of the SPI that this transport provider uses.</span></span> 
    
 <span data-ttu-id="697fa-134">_lppXPProvider_</span><span class="sxs-lookup"><span data-stu-id="697fa-134">_lppXPProvider_</span></span>
  
> <span data-ttu-id="697fa-135">[out] Указатель на указатель на объект поставщика инициализированную транспорта.</span><span class="sxs-lookup"><span data-stu-id="697fa-135">[out] Pointer to a pointer to the initialized transport provider object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="697fa-136">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="6">Return value</span></span>

<span data-ttu-id="697fa-137">ЗНАЧЕНИЕ S_OK</span><span class="sxs-lookup"><span data-stu-id="697fa-137">S_OK</span></span> 
  
> <span data-ttu-id="697fa-138">����� ������� � ������ ��������� ��������� ��� ��������.</span><span class="sxs-lookup"><span data-stu-id="697fa-138">The call succeeded and has returned the expected value or values.</span></span> 
    
<span data-ttu-id="697fa-139">MAPI_E_VERSION</span><span class="sxs-lookup"><span data-stu-id="697fa-139">MAPI_E_VERSION</span></span> 
  
> <span data-ttu-id="697fa-140">Версия SPI, используемые MAPI не совместимый с индекс параметров безопасности, используемые этим поставщиком.</span><span class="sxs-lookup"><span data-stu-id="697fa-140">The SPI version being used by MAPI is not compatible with the SPI being used by this provider.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="697fa-141">Замечания</span><span class="sxs-lookup"><span data-stu-id="697fa-141">Remarks</span></span>

<span data-ttu-id="697fa-142">MAPI вызывает функцию точки входа **XPProviderInit** для инициализации поставщика транспорта после входа клиента.</span><span class="sxs-lookup"><span data-stu-id="697fa-142">MAPI calls the entry point function **XPProviderInit** to initialize a transport provider following a client logon.</span></span> <span data-ttu-id="697fa-143">**XPProviderInit** вызывается один раз для каждого поставщика транспорта, указанного в профиле клиента.</span><span class="sxs-lookup"><span data-stu-id="697fa-143">**XPProviderInit** is called once for each transport provider specified in the client's profile.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="697fa-144">Примечания для исполнителей</span><span class="sxs-lookup"><span data-stu-id="697fa-144">Notes to implementers</span></span>

<span data-ttu-id="697fa-145">Поставщика транспорта необходимо реализовать **XPProviderInit** как функцию точки входа в DLL поставщика.</span><span class="sxs-lookup"><span data-stu-id="697fa-145">A transport provider must implement **XPProviderInit** as an entry point function in the provider's DLL.</span></span> <span data-ttu-id="697fa-146">Реализация должны быть основаны на прототип функции **XPPROVIDERINIT** также указано в Mapispi.h.</span><span class="sxs-lookup"><span data-stu-id="697fa-146">The implementation must be based on the **XPPROVIDERINIT** function prototype, also specified in Mapispi.h.</span></span> <span data-ttu-id="697fa-147">MAPI определяет **XPPROVIDERINIT** для использования типа стандартный вызова инициализации MAPI, STDMAPIINITCALLTYPE, что активирует **XPProviderInit** необходимо выполнить соглашение о вызовах CDECL.</span><span class="sxs-lookup"><span data-stu-id="697fa-147">MAPI defines **XPPROVIDERINIT** to use the standard MAPI initialization call type, STDMAPIINITCALLTYPE, which causes **XPProviderInit** to follow the CDECL calling convention.</span></span> <span data-ttu-id="697fa-148">Преимуществом CDECL — даже в том случае, если число вызовов параметров не соответствует количество определенных параметров может выполняться звонки.</span><span class="sxs-lookup"><span data-stu-id="697fa-148">An advantage of CDECL is that calls can be attempted even if the number of calling parameters does not match the number of defined parameters.</span></span> 
  
<span data-ttu-id="697fa-149">Поставщик может быть инициализирован несколько раз из-за изображения которых появляются в несколько профилей в одновременное использование или отображение более одного раза в одном профиле.</span><span class="sxs-lookup"><span data-stu-id="697fa-149">A provider can be initialized multiple times as a result of appearing in several profiles in simultaneous use or of appearing more than once in the same profile.</span></span> <span data-ttu-id="697fa-150">Поскольку объект поставщика содержит контекста, **XPProviderInit** необходимо возвратить объект другого поставщика в _lppXPProvider_ для каждой инициализации, даже для нескольких инициализации в одном процессе.</span><span class="sxs-lookup"><span data-stu-id="697fa-150">Because the provider object contains context, **XPProviderInit** must return a different provider object in  _lppXPProvider_ for each initialization, even for multiple initializations in the same process.</span></span> 
  
<span data-ttu-id="697fa-151">Поставщика транспорта должно использовать функции, на который указывает _lpAllocateBuffer_, _lpAllocateMore_и _lpFreeBuffer_ для большинства выделение и освобождение памяти.</span><span class="sxs-lookup"><span data-stu-id="697fa-151">The transport provider should use the functions pointed to by  _lpAllocateBuffer_,  _lpAllocateMore_, and  _lpFreeBuffer_ for most memory allocation and deallocation.</span></span> <span data-ttu-id="697fa-152">В частности поставщик должен использовать эти функции для выделения памяти для использования с клиентскими приложениями при вызове интерфейсы объекта, такие как [IMAPIProp::GetProps](imapiprop-getprops.md) и [IMAPITable::QueryRows](imapitable-queryrows.md).</span><span class="sxs-lookup"><span data-stu-id="697fa-152">In particular, the provider must use these functions to allocate memory for use by client applications when calling object interfaces such as [IMAPIProp::GetProps](imapiprop-getprops.md) and [IMAPITable::QueryRows](imapitable-queryrows.md).</span></span> <span data-ttu-id="697fa-153">Если поставщик также требуется для использования распределителя памяти OLE, он должен вызвать метод **IUnknown::AddRef** распределителя объект, указанный в параметре _lpMalloc_ .</span><span class="sxs-lookup"><span data-stu-id="697fa-153">If the provider also expects to use the OLE memory allocator, it should call the **IUnknown::AddRef** method of the allocator object pointed to by the  _lpMalloc_ parameter.</span></span> 
  
<span data-ttu-id="697fa-154">Дополнительные сведения о создании **XPProviderInit**можно [инициализации поставщика транспорта](initializing-the-transport-provider.md).</span><span class="sxs-lookup"><span data-stu-id="697fa-154">For more information about writing **XPProviderInit**, see [Initializing the Transport Provider](initializing-the-transport-provider.md).</span></span> <span data-ttu-id="697fa-155">Дополнительные сведения о функциях точки входа [реализации функции выберите запись службы поставщика](implementing-a-service-provider-entry-point-function.md)см.</span><span class="sxs-lookup"><span data-stu-id="697fa-155">For more information about entry point functions, see [Implementing a Service Provider Entry Point Function](implementing-a-service-provider-entry-point-function.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="697fa-156">См. также</span><span class="sxs-lookup"><span data-stu-id="697fa-156">See also</span></span>



[<span data-ttu-id="697fa-157">ABProviderInit</span><span class="sxs-lookup"><span data-stu-id="697fa-157">ABProviderInit</span></span>](abproviderinit.md)
  
[<span data-ttu-id="697fa-158">IXPProvider : IUnknown</span><span class="sxs-lookup"><span data-stu-id="697fa-158">IXPProvider : IUnknown</span></span>](ixpprovideriunknown.md)
  
[<span data-ttu-id="697fa-159">MSProviderInit</span><span class="sxs-lookup"><span data-stu-id="697fa-159">MSProviderInit</span></span>](msproviderinit.md)

