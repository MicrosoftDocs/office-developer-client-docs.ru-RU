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
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: acec07df0b72685cf9ec6b21499c730b72f58c59
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428286"
---
# <a name="abproviderinit"></a><span data-ttu-id="6deb7-103">ABProviderInit</span><span class="sxs-lookup"><span data-stu-id="6deb7-103">ABProviderInit</span></span>
 
<span data-ttu-id="6deb7-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6deb7-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6deb7-105">Инициализирует поставщика адресной книги для работы.</span><span class="sxs-lookup"><span data-stu-id="6deb7-105">Initializes an address book provider for operation.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="6deb7-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="6deb7-106">Header file:</span></span>  <br/> |<span data-ttu-id="6deb7-107">Mapispi.h</span><span class="sxs-lookup"><span data-stu-id="6deb7-107">Mapispi.h</span></span>  <br/> |
|<span data-ttu-id="6deb7-108">Реализовано в:</span><span class="sxs-lookup"><span data-stu-id="6deb7-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="6deb7-109">Поставщики адресных книг</span><span class="sxs-lookup"><span data-stu-id="6deb7-109">Address book providers</span></span>  <br/> |
|<span data-ttu-id="6deb7-110">Вызывающая сторона:</span><span class="sxs-lookup"><span data-stu-id="6deb7-110">Called by:</span></span>  <br/> |<span data-ttu-id="6deb7-111">MAPI</span><span class="sxs-lookup"><span data-stu-id="6deb7-111">MAPI</span></span>  <br/> |
   
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

## <a name="parameters"></a><span data-ttu-id="6deb7-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="6deb7-112">Parameters</span></span>

 <span data-ttu-id="6deb7-113">_hInstance_</span><span class="sxs-lookup"><span data-stu-id="6deb7-113">_hInstance_</span></span>
  
> <span data-ttu-id="6deb7-114">[in] Экземпляр библиотеки динамической ссылки (DLL) поставщика адресной книги, используемой MAPI при его связи.</span><span class="sxs-lookup"><span data-stu-id="6deb7-114">[in] The instance of the address book provider's dynamic-link library (DLL) that MAPI used when it linked.</span></span> 
    
 <span data-ttu-id="6deb7-115">_lpMalloc_</span><span class="sxs-lookup"><span data-stu-id="6deb7-115">_lpMalloc_</span></span>
  
> <span data-ttu-id="6deb7-116">[in] Указатель на объект-память для размещения интерфейса OLE **IMalloc.**</span><span class="sxs-lookup"><span data-stu-id="6deb7-116">[in] Pointer to a memory allocator object exposing the OLE **IMalloc** interface.</span></span> <span data-ttu-id="6deb7-117">Поставщику адресной книги может потребоваться использовать этот метод выделения при работе с определенными интерфейсами, такими как **IStream.**</span><span class="sxs-lookup"><span data-stu-id="6deb7-117">The address book provider may need to use this allocation method when working with certain interfaces such as **IStream**.</span></span> 
    
 <span data-ttu-id="6deb7-118">_lpAllocateBuffer_</span><span class="sxs-lookup"><span data-stu-id="6deb7-118">_lpAllocateBuffer_</span></span>
  
> <span data-ttu-id="6deb7-119">[in] Указатель на функцию [MAPIAllocateBuffer,](mapiallocatebuffer.md) которая будет использоваться при необходимости MAPI для выделения памяти.</span><span class="sxs-lookup"><span data-stu-id="6deb7-119">[in] Pointer to the [MAPIAllocateBuffer](mapiallocatebuffer.md) function, to be used where required by MAPI to allocate memory.</span></span> 
    
 <span data-ttu-id="6deb7-120">_lpAllocateMore_</span><span class="sxs-lookup"><span data-stu-id="6deb7-120">_lpAllocateMore_</span></span>
  
> <span data-ttu-id="6deb7-121">[in] Указатель на функцию [MAPIAllocateMore,](mapiallocatemore.md) которая будет использоваться при необходимости MAPI для выделения дополнительной памяти.</span><span class="sxs-lookup"><span data-stu-id="6deb7-121">[in] Pointer to the [MAPIAllocateMore](mapiallocatemore.md) function, to be used where required by MAPI to allocate additional memory.</span></span> 
    
 <span data-ttu-id="6deb7-122">_lpFreeBuffer_</span><span class="sxs-lookup"><span data-stu-id="6deb7-122">_lpFreeBuffer_</span></span>
  
> <span data-ttu-id="6deb7-123">[in] Указатель на [функцию MAPIFreeBuffer,](mapifreebuffer.md) которая будет использоваться при необходимости MAPI для освободить память.</span><span class="sxs-lookup"><span data-stu-id="6deb7-123">[in] Pointer to the [MAPIFreeBuffer](mapifreebuffer.md) function, to be used where required by MAPI to free memory.</span></span> 
    
 <span data-ttu-id="6deb7-124">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="6deb7-124">_ulFlags_</span></span>
  
> <span data-ttu-id="6deb7-125">[in] Битоваяmas флагов.</span><span class="sxs-lookup"><span data-stu-id="6deb7-125">[in] Bitmask of flags.</span></span> <span data-ttu-id="6deb7-126">Можно установить следующий флаг:</span><span class="sxs-lookup"><span data-stu-id="6deb7-126">The following flag can be set:</span></span>
    
<span data-ttu-id="6deb7-127">MAPI_NT_SERVICE</span><span class="sxs-lookup"><span data-stu-id="6deb7-127">MAPI_NT_SERVICE</span></span> 
  
> <span data-ttu-id="6deb7-128">Поставщик загружается в контексте службы Windows— особого типа процесса без доступа к пользовательскому интерфейсу.</span><span class="sxs-lookup"><span data-stu-id="6deb7-128">The provider is being loaded in the context of a Windows service, a special type of process without access to any user interface.</span></span> 
    
 <span data-ttu-id="6deb7-129">_ulMAPIVer_</span><span class="sxs-lookup"><span data-stu-id="6deb7-129">_ulMAPIVer_</span></span>
  
> <span data-ttu-id="6deb7-130">[in] Номер версии интерфейса поставщика услуг (SPI), который MAPI.DLL.</span><span class="sxs-lookup"><span data-stu-id="6deb7-130">[in] Version number of the service provider interface (SPI) that MAPI.DLL uses.</span></span> <span data-ttu-id="6deb7-131">Номер текущей версии см. в MAPISPI. Файл h-загона.</span><span class="sxs-lookup"><span data-stu-id="6deb7-131">For the current version number, see the MAPISPI.H header file.</span></span> 
    
 <span data-ttu-id="6deb7-132">_lpulProviderVer_</span><span class="sxs-lookup"><span data-stu-id="6deb7-132">_lpulProviderVer_</span></span>
  
> <span data-ttu-id="6deb7-133">[out] Указатель на номер версии SPI, который использует этот поставщик адресной книги.</span><span class="sxs-lookup"><span data-stu-id="6deb7-133">[out] Pointer to the version number of the SPI that this address book provider uses.</span></span> 
    
 <span data-ttu-id="6deb7-134">_lppABProvider_</span><span class="sxs-lookup"><span data-stu-id="6deb7-134">_lppABProvider_</span></span>
  
> <span data-ttu-id="6deb7-135">[out] Указатель на указатель на инициализированный объект поставщика адресной книги.</span><span class="sxs-lookup"><span data-stu-id="6deb7-135">[out] Pointer to a pointer to the initialized address book provider object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="6deb7-136">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="6deb7-136">Return value</span></span>

<span data-ttu-id="6deb7-137">S_OK</span><span class="sxs-lookup"><span data-stu-id="6deb7-137">S_OK</span></span> 
  
> <span data-ttu-id="6deb7-138">����� ������� � ������ ��������� ��������� ��� ��������.</span><span class="sxs-lookup"><span data-stu-id="6deb7-138">The call succeeded and has returned the expected value or values.</span></span> 
    
<span data-ttu-id="6deb7-139">MAPI_E_VERSION</span><span class="sxs-lookup"><span data-stu-id="6deb7-139">MAPI_E_VERSION</span></span> 
  
> <span data-ttu-id="6deb7-140">Версия SPI, используемая MAPI, несовместима с SPI, используемым этим поставщиком.</span><span class="sxs-lookup"><span data-stu-id="6deb7-140">The SPI version being used by MAPI is not compatible with the SPI being used by this provider.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="6deb7-141">Примечания</span><span class="sxs-lookup"><span data-stu-id="6deb7-141">Remarks</span></span>

<span data-ttu-id="6deb7-142">MAPI вызывает функцию точки входа **ABProviderInit** для инициализации поставщика адресной книги после входа клиента.</span><span class="sxs-lookup"><span data-stu-id="6deb7-142">MAPI calls the entry point function **ABProviderInit** to initialize an address book provider following a client logon.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="6deb7-143">Примечания для исполнителей</span><span class="sxs-lookup"><span data-stu-id="6deb7-143">Notes to implementers</span></span>

<span data-ttu-id="6deb7-144">Поставщик адресной книги должен реализовать **ABProviderInit** в качестве функции точки входа в DLL поставщика.</span><span class="sxs-lookup"><span data-stu-id="6deb7-144">An address book provider must implement **ABProviderInit** as an entry point function in the provider's DLL.</span></span> <span data-ttu-id="6deb7-145">Реализация должна быть основана на прототипе **функции ABPROVIDERINIT,** также указанном в MAPISPI.H.</span><span class="sxs-lookup"><span data-stu-id="6deb7-145">The implementation must be based on the **ABPROVIDERINIT** function prototype, also specified in MAPISPI.H.</span></span> <span data-ttu-id="6deb7-146">MAPI определяет **ABPROVIDERINIT** для использования стандартного типа вызова инициализации MAPI STDMAPIINITCALLTYPE, что приводит к следуют соглашению о вызовах CDECL для **ABProviderInit.**</span><span class="sxs-lookup"><span data-stu-id="6deb7-146">MAPI defines **ABPROVIDERINIT** to use the standard MAPI initialization call type, STDMAPIINITCALLTYPE, which causes **ABProviderInit** to follow the CDECL calling convention.</span></span> 
  
<span data-ttu-id="6deb7-147">Поставщик может быть инициализирован несколько раз в результате одновременного использования нескольких профилей или появления в одном профиле более одного раза.</span><span class="sxs-lookup"><span data-stu-id="6deb7-147">A provider can be initialized multiple times, as a result of appearing in several profiles in simultaneous use or of appearing more than once in the same profile.</span></span> <span data-ttu-id="6deb7-148">Так как объект поставщика содержит контекст, **ABProviderInit** должен возвращать разные объекты поставщика в  _lppABProvider_ для каждой инициализации даже для нескольких инициализации в одном процессе.</span><span class="sxs-lookup"><span data-stu-id="6deb7-148">Because the provider object contains context, **ABProviderInit** must return a different provider object in  _lppABProvider_ for each initialization, even for multiple initializations in the same process.</span></span> 
  
<span data-ttu-id="6deb7-149">Поставщик адресной книги должен использовать функции, на которые указывают  _lpAllocateBuffer,_  _lpAllocateMore_ и  _lpFreeBuffer_ для выделения и распределения памяти.</span><span class="sxs-lookup"><span data-stu-id="6deb7-149">The address book provider should use the functions pointed to by  _lpAllocateBuffer_,  _lpAllocateMore_, and  _lpFreeBuffer_ for most memory allocation and deallocation.</span></span> <span data-ttu-id="6deb7-150">В частности, поставщик должен использовать эти функции для выделения памяти для использования клиентских приложений при вызове интерфейсов объектов, таких как [IMAPIProp::GetProps](imapiprop-getprops.md) и [IMAPITable::QueryRows](imapitable-queryrows.md).</span><span class="sxs-lookup"><span data-stu-id="6deb7-150">In particular, the provider must use these functions to allocate memory for use by client applications when calling object interfaces such as [IMAPIProp::GetProps](imapiprop-getprops.md) and [IMAPITable::QueryRows](imapitable-queryrows.md).</span></span> <span data-ttu-id="6deb7-151">Если поставщик также ожидает использовать память OLE, он должен вызвать метод **IUnknown::AddRef** объекта allocator, на который указывает параметр _lpMalloc._</span><span class="sxs-lookup"><span data-stu-id="6deb7-151">If the provider also expects to use the OLE memory allocator, it should call the **IUnknown::AddRef** method of the allocator object pointed to by the  _lpMalloc_ parameter.</span></span> 
  
<span data-ttu-id="6deb7-152">Дополнительные сведения о написании **ABProviderInit** см. в реализации функции точки входа поставщика [адресной книги.](implementing-an-address-book-provider-entry-point-function.md)</span><span class="sxs-lookup"><span data-stu-id="6deb7-152">For more information on writing **ABProviderInit**, see [Implementing an Address Book Provider Entry Point Function](implementing-an-address-book-provider-entry-point-function.md).</span></span> <span data-ttu-id="6deb7-153">Дополнительные сведения о функциях точек входа см. в [реализации функции](implementing-a-service-provider-entry-point-function.md)точки входа поставщика услуг.</span><span class="sxs-lookup"><span data-stu-id="6deb7-153">For more information on entry point functions, see [Implementing a Service Provider Entry Point Function](implementing-a-service-provider-entry-point-function.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="6deb7-154">См. также</span><span class="sxs-lookup"><span data-stu-id="6deb7-154">See also</span></span>

- [<span data-ttu-id="6deb7-155">IABProvider : IUnknown</span><span class="sxs-lookup"><span data-stu-id="6deb7-155">IABProvider : IUnknown</span></span>](iabprovideriunknown.md) 
- [<span data-ttu-id="6deb7-156">MSProviderInit</span><span class="sxs-lookup"><span data-stu-id="6deb7-156">MSProviderInit</span></span>](msproviderinit.md)
- [<span data-ttu-id="6deb7-157">XPProviderInit</span><span class="sxs-lookup"><span data-stu-id="6deb7-157">XPProviderInit</span></span>](xpproviderinit.md)

