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
# <a name="xpproviderinit"></a><span data-ttu-id="879b2-103">XPProviderInit</span><span class="sxs-lookup"><span data-stu-id="879b2-103">XPProviderInit</span></span>

  
  
<span data-ttu-id="879b2-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="879b2-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="879b2-105">Инициализирует поставщик транспорта для операции.</span><span class="sxs-lookup"><span data-stu-id="879b2-105">Initializes a transport provider for operation.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="879b2-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="879b2-106">Header file:</span></span>  <br/> |<span data-ttu-id="879b2-107">Маписпи. h</span><span class="sxs-lookup"><span data-stu-id="879b2-107">Mapispi.h</span></span>  <br/> |
|<span data-ttu-id="879b2-108">Реализовано в:</span><span class="sxs-lookup"><span data-stu-id="879b2-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="879b2-109">Поставщики транспорта</span><span class="sxs-lookup"><span data-stu-id="879b2-109">Transport providers</span></span>  <br/> |
|<span data-ttu-id="879b2-110">Вызывающая сторона:</span><span class="sxs-lookup"><span data-stu-id="879b2-110">Called by:</span></span>  <br/> |<span data-ttu-id="879b2-111">MAPI</span><span class="sxs-lookup"><span data-stu-id="879b2-111">MAPI</span></span>  <br/> |
   
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

## <a name="parameters"></a><span data-ttu-id="879b2-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="879b2-112">Parameters</span></span>

 <span data-ttu-id="879b2-113">_hInstance_</span><span class="sxs-lookup"><span data-stu-id="879b2-113">_hInstance_</span></span>
  
> <span data-ttu-id="879b2-114">возврата Экземпляр библиотеки динамической компоновки (DLL) поставщика транспорта, используемой MAPI при загрузке библиотеки DLL.</span><span class="sxs-lookup"><span data-stu-id="879b2-114">[in] The instance of the transport provider's dynamic-link library (DLL) that MAPI used when it loaded the DLL.</span></span>
    
 <span data-ttu-id="879b2-115">_Лпмаллок_</span><span class="sxs-lookup"><span data-stu-id="879b2-115">_lpMalloc_</span></span>
  
> <span data-ttu-id="879b2-116">возврата Указатель на объект распределителя памяти, который предоставляет интерфейс для **выделения** OLE.</span><span class="sxs-lookup"><span data-stu-id="879b2-116">[in] Pointer to a memory allocator object exposing the OLE **IMalloc** interface.</span></span> <span data-ttu-id="879b2-117">Поставщику транспорта может потребоваться использовать этот метод распределения при работе с определенными интерфейсами, такими как **IStream**.</span><span class="sxs-lookup"><span data-stu-id="879b2-117">The transport provider may need to use this allocation method when working with certain interfaces such as **IStream**.</span></span> 
    
 <span data-ttu-id="879b2-118">_Лпаллокатебуффер_</span><span class="sxs-lookup"><span data-stu-id="879b2-118">_lpAllocateBuffer_</span></span>
  
> <span data-ttu-id="879b2-119">возврата Указатель на функцию [мапиаллокатебуффер](mapiallocatebuffer.md) , которая будет использоваться для выделения памяти.</span><span class="sxs-lookup"><span data-stu-id="879b2-119">[in] Pointer to the [MAPIAllocateBuffer](mapiallocatebuffer.md) function, to be used to allocate memory.</span></span> 
    
 <span data-ttu-id="879b2-120">_Лпаллокатеморе_</span><span class="sxs-lookup"><span data-stu-id="879b2-120">_lpAllocateMore_</span></span>
  
> <span data-ttu-id="879b2-121">возврата Указатель на функцию [мапиаллокатеморе](mapiallocatemore.md) , которая будет использоваться для выделения дополнительной памяти.</span><span class="sxs-lookup"><span data-stu-id="879b2-121">[in] Pointer to the [MAPIAllocateMore](mapiallocatemore.md) function, to be used to allocate additional memory.</span></span> 
    
 <span data-ttu-id="879b2-122">_Лпфрибуффер_</span><span class="sxs-lookup"><span data-stu-id="879b2-122">_lpFreeBuffer_</span></span>
  
> <span data-ttu-id="879b2-123">возврата Указатель на функцию [мапифрибуффер](mapifreebuffer.md) , который будет использоваться для освобождения памяти.</span><span class="sxs-lookup"><span data-stu-id="879b2-123">[in] Pointer to the [MAPIFreeBuffer](mapifreebuffer.md) function, to be used to free memory.</span></span> 
    
 <span data-ttu-id="879b2-124">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="879b2-124">_ulFlags_</span></span>
  
> <span data-ttu-id="879b2-125">возврата Битовая маска флагов.</span><span class="sxs-lookup"><span data-stu-id="879b2-125">[in] Bitmask of flags.</span></span> <span data-ttu-id="879b2-126">Можно задать следующий флаг:</span><span class="sxs-lookup"><span data-stu-id="879b2-126">The following flag can be set:</span></span>
    
<span data-ttu-id="879b2-127">МАПИ_НТ_СЕРВИЦЕ</span><span class="sxs-lookup"><span data-stu-id="879b2-127">MAPI_NT_SERVICE</span></span> 
  
> <span data-ttu-id="879b2-128">Поставщик загружается в контексте службы Windows — особого типа процесса без доступа к любому пользовательскому интерфейсу.</span><span class="sxs-lookup"><span data-stu-id="879b2-128">The provider is being loaded in the context of a Windows service, a special type of process without access to any user interface.</span></span> 
    
 <span data-ttu-id="879b2-129">_Улмапивер_</span><span class="sxs-lookup"><span data-stu-id="879b2-129">_ulMAPIVer_</span></span>
  
> <span data-ttu-id="879b2-130">возврата Номер версии интерфейса поставщика услуг (SPI), который использует MAPI. dll.</span><span class="sxs-lookup"><span data-stu-id="879b2-130">[in] Version number of the service provider interface (SPI) that Mapi.dll uses.</span></span> <span data-ttu-id="879b2-131">Текущий номер версии представлен в файле заголовка Маписпи. h.</span><span class="sxs-lookup"><span data-stu-id="879b2-131">For the current version number, see the Mapispi.h header file.</span></span> 
    
 <span data-ttu-id="879b2-132">_Лпулпровидервер_</span><span class="sxs-lookup"><span data-stu-id="879b2-132">_lpulProviderVer_</span></span>
  
> <span data-ttu-id="879b2-133">вышли Указатель на номер версии SPI, который использует этот поставщик транспорта.</span><span class="sxs-lookup"><span data-stu-id="879b2-133">[out] Pointer to the version number of the SPI that this transport provider uses.</span></span> 
    
 <span data-ttu-id="879b2-134">_Лппксппровидер_</span><span class="sxs-lookup"><span data-stu-id="879b2-134">_lppXPProvider_</span></span>
  
> <span data-ttu-id="879b2-135">вышли Указатель на указатель на инициализированный объект поставщика транспорта.</span><span class="sxs-lookup"><span data-stu-id="879b2-135">[out] Pointer to a pointer to the initialized transport provider object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="879b2-136">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="879b2-136">Return value</span></span>

<span data-ttu-id="879b2-137">S_OK</span><span class="sxs-lookup"><span data-stu-id="879b2-137">S_OK</span></span> 
  
> <span data-ttu-id="879b2-138">����� ������� � ������ ��������� ��������� ��� ��������.</span><span class="sxs-lookup"><span data-stu-id="879b2-138">The call succeeded and has returned the expected value or values.</span></span> 
    
<span data-ttu-id="879b2-139">МАПИ_Е_ВЕРСИОН</span><span class="sxs-lookup"><span data-stu-id="879b2-139">MAPI_E_VERSION</span></span> 
  
> <span data-ttu-id="879b2-140">Версия SPI, используемая MAPI, несовместима с SPI, используемым этим поставщиком.</span><span class="sxs-lookup"><span data-stu-id="879b2-140">The SPI version being used by MAPI is not compatible with the SPI being used by this provider.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="879b2-141">Примечания</span><span class="sxs-lookup"><span data-stu-id="879b2-141">Remarks</span></span>

<span data-ttu-id="879b2-142">MAPI вызывает функцию точки входа **ксппровидеринит** для инициализации поставщика транспорта после входа клиента.</span><span class="sxs-lookup"><span data-stu-id="879b2-142">MAPI calls the entry point function **XPProviderInit** to initialize a transport provider following a client logon.</span></span> <span data-ttu-id="879b2-143">**Ксппровидеринит** вызывается один раз для каждого поставщика транспорта, указанного в профиле клиента.</span><span class="sxs-lookup"><span data-stu-id="879b2-143">**XPProviderInit** is called once for each transport provider specified in the client's profile.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="879b2-144">Примечания для исполнителей</span><span class="sxs-lookup"><span data-stu-id="879b2-144">Notes to implementers</span></span>

<span data-ttu-id="879b2-145">Поставщик транспорта должен реализовать **ксппровидеринит** в качестве функции точки входа в DLL поставщика.</span><span class="sxs-lookup"><span data-stu-id="879b2-145">A transport provider must implement **XPProviderInit** as an entry point function in the provider's DLL.</span></span> <span data-ttu-id="879b2-146">Реализация должна основываться на прототипе функции **ксппровидеринит** , также указанном в маписпи. h.</span><span class="sxs-lookup"><span data-stu-id="879b2-146">The implementation must be based on the **XPPROVIDERINIT** function prototype, also specified in Mapispi.h.</span></span> <span data-ttu-id="879b2-147">MAPI определяет **ксппровидеринит** для использования стандартного типа вызова инициализации MAPI, стдмапииниткаллтипе, что заставляет **ксппровидеринит** следовать соглашению о вызовах кдекл.</span><span class="sxs-lookup"><span data-stu-id="879b2-147">MAPI defines **XPPROVIDERINIT** to use the standard MAPI initialization call type, STDMAPIINITCALLTYPE, which causes **XPProviderInit** to follow the CDECL calling convention.</span></span> <span data-ttu-id="879b2-148">Преимуществом КДЕКЛ является то, что можно предпринимать попытки вызовов, даже если количество параметров вызовов не равно числу определенных параметров.</span><span class="sxs-lookup"><span data-stu-id="879b2-148">An advantage of CDECL is that calls can be attempted even if the number of calling parameters does not match the number of defined parameters.</span></span> 
  
<span data-ttu-id="879b2-149">Поставщик может быть инициализирован несколько раз в результате того, что в одном и том же профиле появлялось несколько профилей в одновременном использовании или несколько раз.</span><span class="sxs-lookup"><span data-stu-id="879b2-149">A provider can be initialized multiple times as a result of appearing in several profiles in simultaneous use or of appearing more than once in the same profile.</span></span> <span data-ttu-id="879b2-150">Так как объект provider содержит Context, **ксппровидеринит** должен возвратить другой объект поставщика в _лппксппровидер_ для каждой инициализации, даже для нескольких инициализаций в одном процессе.</span><span class="sxs-lookup"><span data-stu-id="879b2-150">Because the provider object contains context, **XPProviderInit** must return a different provider object in  _lppXPProvider_ for each initialization, even for multiple initializations in the same process.</span></span> 
  
<span data-ttu-id="879b2-151">Поставщик транспорта должен использовать функции, на которые указывает _лпаллокатебуффер_, _лпаллокатеморе_и _лпфрибуффер_ для большинства выделений и освобождений памяти.</span><span class="sxs-lookup"><span data-stu-id="879b2-151">The transport provider should use the functions pointed to by  _lpAllocateBuffer_,  _lpAllocateMore_, and  _lpFreeBuffer_ for most memory allocation and deallocation.</span></span> <span data-ttu-id="879b2-152">В частности, поставщик должен использовать эти функции для выделения памяти, которая будет использоваться клиентскими приложениями при вызове интерфейсов объектов, таких как [IMAPIProp::](imapiprop-getprops.md) /PROPS и [IMAPITable:: QueryRows](imapitable-queryrows.md).</span><span class="sxs-lookup"><span data-stu-id="879b2-152">In particular, the provider must use these functions to allocate memory for use by client applications when calling object interfaces such as [IMAPIProp::GetProps](imapiprop-getprops.md) and [IMAPITable::QueryRows](imapitable-queryrows.md).</span></span> <span data-ttu-id="879b2-153">Если поставщик также ожидает использования распределителя памяти OLE, он должен вызывать метод **IUnknown:: AddRef** объекта распределителя, на который указывает параметр _лпмаллок_ .</span><span class="sxs-lookup"><span data-stu-id="879b2-153">If the provider also expects to use the OLE memory allocator, it should call the **IUnknown::AddRef** method of the allocator object pointed to by the  _lpMalloc_ parameter.</span></span> 
  
<span data-ttu-id="879b2-154">Дополнительные сведения о создании **ксппровидеринит**можно найти [в статье инициализация поставщика транспорта](initializing-the-transport-provider.md).</span><span class="sxs-lookup"><span data-stu-id="879b2-154">For more information about writing **XPProviderInit**, see [Initializing the Transport Provider](initializing-the-transport-provider.md).</span></span> <span data-ttu-id="879b2-155">Дополнительные сведения о функциях точки входа можно найти [в статье реализация функции точки входа поставщика услуг](implementing-a-service-provider-entry-point-function.md).</span><span class="sxs-lookup"><span data-stu-id="879b2-155">For more information about entry point functions, see [Implementing a Service Provider Entry Point Function](implementing-a-service-provider-entry-point-function.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="879b2-156">См. также</span><span class="sxs-lookup"><span data-stu-id="879b2-156">See also</span></span>



[<span data-ttu-id="879b2-157">ABProviderInit</span><span class="sxs-lookup"><span data-stu-id="879b2-157">ABProviderInit</span></span>](abproviderinit.md)
  
[<span data-ttu-id="879b2-158">IXPProvider : IUnknown</span><span class="sxs-lookup"><span data-stu-id="879b2-158">IXPProvider : IUnknown</span></span>](ixpprovideriunknown.md)
  
[<span data-ttu-id="879b2-159">MSProviderInit</span><span class="sxs-lookup"><span data-stu-id="879b2-159">MSProviderInit</span></span>](msproviderinit.md)

