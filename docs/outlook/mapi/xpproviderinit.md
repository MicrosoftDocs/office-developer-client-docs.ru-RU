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
ms.openlocfilehash: 38b60180ae7c417bf34998e72f96b353ace02859
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22592537"
---
# <a name="xpproviderinit"></a><span data-ttu-id="5bc66-103">XPProviderInit</span><span class="sxs-lookup"><span data-stu-id="5bc66-103">XPProviderInit</span></span>

  
  
<span data-ttu-id="5bc66-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5bc66-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5bc66-105">Инициализирует поставщика транспорта для операции.</span><span class="sxs-lookup"><span data-stu-id="5bc66-105">Initializes a transport provider for operation.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="5bc66-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="5bc66-106">Header file:</span></span>  <br/> |<span data-ttu-id="5bc66-107">Mapispi.h</span><span class="sxs-lookup"><span data-stu-id="5bc66-107">Mapispi.h</span></span>  <br/> |
|<span data-ttu-id="5bc66-108">Реализованный:</span><span class="sxs-lookup"><span data-stu-id="5bc66-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="5bc66-109">Поставщиками транспорта</span><span class="sxs-lookup"><span data-stu-id="5bc66-109">Transport providers</span></span>  <br/> |
|<span data-ttu-id="5bc66-110">Вызывается:</span><span class="sxs-lookup"><span data-stu-id="5bc66-110">Called by:</span></span>  <br/> |<span data-ttu-id="5bc66-111">MAPI</span><span class="sxs-lookup"><span data-stu-id="5bc66-111">MAPI</span></span>  <br/> |
   
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

## <a name="parameters"></a><span data-ttu-id="5bc66-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="5bc66-112">Parameters</span></span>

 <span data-ttu-id="5bc66-113">_hInstance_</span><span class="sxs-lookup"><span data-stu-id="5bc66-113">_hInstance_</span></span>
  
> <span data-ttu-id="5bc66-114">[in] Экземпляр поставщика транспорта динамической библиотеки (DLL), MAPI, используемой при загрузке DLL.</span><span class="sxs-lookup"><span data-stu-id="5bc66-114">[in] The instance of the transport provider's dynamic-link library (DLL) that MAPI used when it loaded the DLL.</span></span>
    
 <span data-ttu-id="5bc66-115">_lpMalloc_</span><span class="sxs-lookup"><span data-stu-id="5bc66-115">_lpMalloc_</span></span>
  
> <span data-ttu-id="5bc66-116">[in] Указатель на объект распределителя памяти, предоставление интерфейса OLE **IMalloc** .</span><span class="sxs-lookup"><span data-stu-id="5bc66-116">[in] Pointer to a memory allocator object exposing the OLE **IMalloc** interface.</span></span> <span data-ttu-id="5bc66-117">Поставщика транспорта может потребоваться использовать этот метод для распределения при работе с определенных интерфейсов, таких как **IStream**.</span><span class="sxs-lookup"><span data-stu-id="5bc66-117">The transport provider may need to use this allocation method when working with certain interfaces such as **IStream**.</span></span> 
    
 <span data-ttu-id="5bc66-118">_lpAllocateBuffer_</span><span class="sxs-lookup"><span data-stu-id="5bc66-118">_lpAllocateBuffer_</span></span>
  
> <span data-ttu-id="5bc66-119">[in] Указатель на функцию [MAPIAllocateBuffer](mapiallocatebuffer.md) , которые будут использоваться для выделения памяти.</span><span class="sxs-lookup"><span data-stu-id="5bc66-119">[in] Pointer to the [MAPIAllocateBuffer](mapiallocatebuffer.md) function, to be used to allocate memory.</span></span> 
    
 <span data-ttu-id="5bc66-120">_lpAllocateMore_</span><span class="sxs-lookup"><span data-stu-id="5bc66-120">_lpAllocateMore_</span></span>
  
> <span data-ttu-id="5bc66-121">[in] Указатель на функцию [MAPIAllocateMore](mapiallocatemore.md) , которые будут использоваться для выделения дополнительной памяти.</span><span class="sxs-lookup"><span data-stu-id="5bc66-121">[in] Pointer to the [MAPIAllocateMore](mapiallocatemore.md) function, to be used to allocate additional memory.</span></span> 
    
 <span data-ttu-id="5bc66-122">_lpFreeBuffer_</span><span class="sxs-lookup"><span data-stu-id="5bc66-122">_lpFreeBuffer_</span></span>
  
> <span data-ttu-id="5bc66-123">[in] Указатель на функцию [MAPIFreeBuffer](mapifreebuffer.md) , которые будут использоваться для свободного использования памяти.</span><span class="sxs-lookup"><span data-stu-id="5bc66-123">[in] Pointer to the [MAPIFreeBuffer](mapifreebuffer.md) function, to be used to free memory.</span></span> 
    
 <span data-ttu-id="5bc66-124">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="5bc66-124">_ulFlags_</span></span>
  
> <span data-ttu-id="5bc66-125">[in] Битовая маска флаги.</span><span class="sxs-lookup"><span data-stu-id="5bc66-125">[in] Bitmask of flags.</span></span> <span data-ttu-id="5bc66-126">Можно задать следующий флаг:</span><span class="sxs-lookup"><span data-stu-id="5bc66-126">The following flag can be set:</span></span>
    
<span data-ttu-id="5bc66-127">MAPI_NT_SERVICE</span><span class="sxs-lookup"><span data-stu-id="5bc66-127">MAPI_NT_SERVICE</span></span> 
  
> <span data-ttu-id="5bc66-128">Поставщик загружается в контексте службы Windows, особый тип процесса без доступа к любой пользовательский интерфейс.</span><span class="sxs-lookup"><span data-stu-id="5bc66-128">The provider is being loaded in the context of a Windows service, a special type of process without access to any user interface.</span></span> 
    
 <span data-ttu-id="5bc66-129">_ulMAPIVer_</span><span class="sxs-lookup"><span data-stu-id="5bc66-129">_ulMAPIVer_</span></span>
  
> <span data-ttu-id="5bc66-130">[in] Номер версии поставщика службы интерфейса (SPI), который использует Mapi.dll.</span><span class="sxs-lookup"><span data-stu-id="5bc66-130">[in] Version number of the service provider interface (SPI) that Mapi.dll uses.</span></span> <span data-ttu-id="5bc66-131">Файл заголовка Mapispi.h текущий номер версии, см.</span><span class="sxs-lookup"><span data-stu-id="5bc66-131">For the current version number, see the Mapispi.h header file.</span></span> 
    
 <span data-ttu-id="5bc66-132">_lpulProviderVer_</span><span class="sxs-lookup"><span data-stu-id="5bc66-132">_lpulProviderVer_</span></span>
  
> <span data-ttu-id="5bc66-133">[out] Указатель на номер версии индекс параметров безопасности, которая использует этот поставщик транспорта.</span><span class="sxs-lookup"><span data-stu-id="5bc66-133">[out] Pointer to the version number of the SPI that this transport provider uses.</span></span> 
    
 <span data-ttu-id="5bc66-134">_lppXPProvider_</span><span class="sxs-lookup"><span data-stu-id="5bc66-134">_lppXPProvider_</span></span>
  
> <span data-ttu-id="5bc66-135">[out] Указатель на указатель на объект поставщика инициализированную транспорта.</span><span class="sxs-lookup"><span data-stu-id="5bc66-135">[out] Pointer to a pointer to the initialized transport provider object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="5bc66-136">������������ ��������</span><span class="sxs-lookup"><span data-stu-id="5bc66-136">Return value</span></span>

<span data-ttu-id="5bc66-137">ЗНАЧЕНИЕ S_OK</span><span class="sxs-lookup"><span data-stu-id="5bc66-137">S_OK</span></span> 
  
> <span data-ttu-id="5bc66-138">����� ������� � ������ ��������� ��������� ��� ��������.</span><span class="sxs-lookup"><span data-stu-id="5bc66-138">The call succeeded and has returned the expected value or values.</span></span> 
    
<span data-ttu-id="5bc66-139">MAPI_E_VERSION</span><span class="sxs-lookup"><span data-stu-id="5bc66-139">MAPI_E_VERSION</span></span> 
  
> <span data-ttu-id="5bc66-140">Версия SPI, используемые MAPI не совместимый с индекс параметров безопасности, используемые этим поставщиком.</span><span class="sxs-lookup"><span data-stu-id="5bc66-140">The SPI version being used by MAPI is not compatible with the SPI being used by this provider.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="5bc66-141">Замечания</span><span class="sxs-lookup"><span data-stu-id="5bc66-141">Remarks</span></span>

<span data-ttu-id="5bc66-142">MAPI вызывает функцию точки входа **XPProviderInit** для инициализации поставщика транспорта после входа клиента.</span><span class="sxs-lookup"><span data-stu-id="5bc66-142">MAPI calls the entry point function **XPProviderInit** to initialize a transport provider following a client logon.</span></span> <span data-ttu-id="5bc66-143">**XPProviderInit** вызывается один раз для каждого поставщика транспорта, указанного в профиле клиента.</span><span class="sxs-lookup"><span data-stu-id="5bc66-143">**XPProviderInit** is called once for each transport provider specified in the client's profile.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="5bc66-144">Примечания для исполнителей</span><span class="sxs-lookup"><span data-stu-id="5bc66-144">Notes to implementers</span></span>

<span data-ttu-id="5bc66-145">Поставщика транспорта необходимо реализовать **XPProviderInit** как функцию точки входа в DLL поставщика.</span><span class="sxs-lookup"><span data-stu-id="5bc66-145">A transport provider must implement **XPProviderInit** as an entry point function in the provider's DLL.</span></span> <span data-ttu-id="5bc66-146">Реализация должны быть основаны на прототип функции **XPPROVIDERINIT** также указано в Mapispi.h.</span><span class="sxs-lookup"><span data-stu-id="5bc66-146">The implementation must be based on the **XPPROVIDERINIT** function prototype, also specified in Mapispi.h.</span></span> <span data-ttu-id="5bc66-147">MAPI определяет **XPPROVIDERINIT** для использования типа стандартный вызова инициализации MAPI, STDMAPIINITCALLTYPE, что активирует **XPProviderInit** необходимо выполнить соглашение о вызовах CDECL.</span><span class="sxs-lookup"><span data-stu-id="5bc66-147">MAPI defines **XPPROVIDERINIT** to use the standard MAPI initialization call type, STDMAPIINITCALLTYPE, which causes **XPProviderInit** to follow the CDECL calling convention.</span></span> <span data-ttu-id="5bc66-148">Преимуществом CDECL — даже в том случае, если число вызовов параметров не соответствует количество определенных параметров может выполняться звонки.</span><span class="sxs-lookup"><span data-stu-id="5bc66-148">An advantage of CDECL is that calls can be attempted even if the number of calling parameters does not match the number of defined parameters.</span></span> 
  
<span data-ttu-id="5bc66-149">Поставщик может быть инициализирован несколько раз из-за изображения которых появляются в несколько профилей в одновременное использование или отображение более одного раза в одном профиле.</span><span class="sxs-lookup"><span data-stu-id="5bc66-149">A provider can be initialized multiple times as a result of appearing in several profiles in simultaneous use or of appearing more than once in the same profile.</span></span> <span data-ttu-id="5bc66-150">Поскольку объект поставщика содержит контекста, **XPProviderInit** необходимо возвратить объект другого поставщика в _lppXPProvider_ для каждой инициализации, даже для нескольких инициализации в одном процессе.</span><span class="sxs-lookup"><span data-stu-id="5bc66-150">Because the provider object contains context, **XPProviderInit** must return a different provider object in  _lppXPProvider_ for each initialization, even for multiple initializations in the same process.</span></span> 
  
<span data-ttu-id="5bc66-151">Поставщика транспорта должно использовать функции, на который указывает _lpAllocateBuffer_, _lpAllocateMore_и _lpFreeBuffer_ для большинства выделение и освобождение памяти.</span><span class="sxs-lookup"><span data-stu-id="5bc66-151">The transport provider should use the functions pointed to by  _lpAllocateBuffer_,  _lpAllocateMore_, and  _lpFreeBuffer_ for most memory allocation and deallocation.</span></span> <span data-ttu-id="5bc66-152">В частности поставщик должен использовать эти функции для выделения памяти для использования с клиентскими приложениями при вызове интерфейсы объекта, такие как [IMAPIProp::GetProps](imapiprop-getprops.md) и [IMAPITable::QueryRows](imapitable-queryrows.md).</span><span class="sxs-lookup"><span data-stu-id="5bc66-152">In particular, the provider must use these functions to allocate memory for use by client applications when calling object interfaces such as [IMAPIProp::GetProps](imapiprop-getprops.md) and [IMAPITable::QueryRows](imapitable-queryrows.md).</span></span> <span data-ttu-id="5bc66-153">Если поставщик также требуется для использования распределителя памяти OLE, он должен вызвать метод **IUnknown::AddRef** распределителя объект, указанный в параметре _lpMalloc_ .</span><span class="sxs-lookup"><span data-stu-id="5bc66-153">If the provider also expects to use the OLE memory allocator, it should call the **IUnknown::AddRef** method of the allocator object pointed to by the  _lpMalloc_ parameter.</span></span> 
  
<span data-ttu-id="5bc66-154">Дополнительные сведения о создании **XPProviderInit**можно [инициализации поставщика транспорта](initializing-the-transport-provider.md).</span><span class="sxs-lookup"><span data-stu-id="5bc66-154">For more information about writing **XPProviderInit**, see [Initializing the Transport Provider](initializing-the-transport-provider.md).</span></span> <span data-ttu-id="5bc66-155">Дополнительные сведения о функциях точки входа [реализации функции выберите запись службы поставщика](implementing-a-service-provider-entry-point-function.md)см.</span><span class="sxs-lookup"><span data-stu-id="5bc66-155">For more information about entry point functions, see [Implementing a Service Provider Entry Point Function](implementing-a-service-provider-entry-point-function.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="5bc66-156">См. также</span><span class="sxs-lookup"><span data-stu-id="5bc66-156">See also</span></span>



[<span data-ttu-id="5bc66-157">ABProviderInit</span><span class="sxs-lookup"><span data-stu-id="5bc66-157">ABProviderInit</span></span>](abproviderinit.md)
  
[<span data-ttu-id="5bc66-158">IXPProvider : IUnknown</span><span class="sxs-lookup"><span data-stu-id="5bc66-158">IXPProvider : IUnknown</span></span>](ixpprovideriunknown.md)
  
[<span data-ttu-id="5bc66-159">MSProviderInit</span><span class="sxs-lookup"><span data-stu-id="5bc66-159">MSProviderInit</span></span>](msproviderinit.md)

