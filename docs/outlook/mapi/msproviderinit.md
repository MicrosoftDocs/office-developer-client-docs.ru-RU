---
title: MSProviderInit
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MSProviderInit
api_type:
- HeaderDef
ms.assetid: 230c66c4-ab04-4fa6-946f-9f4b704f2842
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 9a5f8b44f9d795282ccfd61fd32a306c5478ed21
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33416239"
---
# <a name="msproviderinit"></a><span data-ttu-id="d1d15-103">MSProviderInit</span><span class="sxs-lookup"><span data-stu-id="d1d15-103">MSProviderInit</span></span>

  
  
<span data-ttu-id="d1d15-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d1d15-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d1d15-105">Инициализирует поставщика для работы с хранилищем сообщений.</span><span class="sxs-lookup"><span data-stu-id="d1d15-105">Initializes a message store provider for operation.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="d1d15-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="d1d15-106">Header file:</span></span>  <br/> |<span data-ttu-id="d1d15-107">Mapispi.h</span><span class="sxs-lookup"><span data-stu-id="d1d15-107">Mapispi.h</span></span>  <br/> |
|<span data-ttu-id="d1d15-108">Реализовано в:</span><span class="sxs-lookup"><span data-stu-id="d1d15-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="d1d15-109">Поставщики store сообщений</span><span class="sxs-lookup"><span data-stu-id="d1d15-109">Message store providers</span></span>  <br/> |
|<span data-ttu-id="d1d15-110">Вызывающая сторона:</span><span class="sxs-lookup"><span data-stu-id="d1d15-110">Called by:</span></span>  <br/> |<span data-ttu-id="d1d15-111">MAPI</span><span class="sxs-lookup"><span data-stu-id="d1d15-111">MAPI</span></span>  <br/> |
   
```cpp
HRESULT MSProviderInit(
  HINSTANCE hInstance,
  LPMALLOC lpMalloc,
  LPALLOCATEBUFFER lpAllocateBuffer,
  LPALLOCATEMORE lpAllocateMore,
  LPFREEBUFFER lpFreeBuffer,
  ULONG ulFlags,
  ULONG ulMAPIVer,
  ULONG FAR * lpulProviderVer,
  LPMSPROVIDER FAR * lppMSProvider
);
```

## <a name="parameters"></a><span data-ttu-id="d1d15-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="d1d15-112">Parameters</span></span>

 <span data-ttu-id="d1d15-113">_hInstance_</span><span class="sxs-lookup"><span data-stu-id="d1d15-113">_hInstance_</span></span>
  
> <span data-ttu-id="d1d15-114">[in] Экземпляр библиотеки динамической ссылки поставщика хранения сообщений (DLL), используемой MAPI при его связи.</span><span class="sxs-lookup"><span data-stu-id="d1d15-114">[in] The instance of the message store provider's dynamic-link library (DLL) that MAPI used when it linked.</span></span> 
    
 <span data-ttu-id="d1d15-115">_lpMalloc_</span><span class="sxs-lookup"><span data-stu-id="d1d15-115">_lpMalloc_</span></span>
  
> <span data-ttu-id="d1d15-116">[in] Указатель на объект-память для размещения интерфейса OLE **IMalloc.**</span><span class="sxs-lookup"><span data-stu-id="d1d15-116">[in] Pointer to a memory allocator object exposing the OLE **IMalloc** interface.</span></span> <span data-ttu-id="d1d15-117">Поставщику хранилище сообщений может потребоваться использовать этот метод выделения при работе с определенными интерфейсами, такими как **IStream.**</span><span class="sxs-lookup"><span data-stu-id="d1d15-117">The message store provider may need to use this allocation method when working with certain interfaces such as **IStream**.</span></span> 
    
 <span data-ttu-id="d1d15-118">_lpAllocateBuffer_</span><span class="sxs-lookup"><span data-stu-id="d1d15-118">_lpAllocateBuffer_</span></span>
  
> <span data-ttu-id="d1d15-119">[in] Указатель на [функцию MAPIAllocateBuffer,](mapiallocatebuffer.md) которая используется для выделения памяти.</span><span class="sxs-lookup"><span data-stu-id="d1d15-119">[in] Pointer to the [MAPIAllocateBuffer](mapiallocatebuffer.md) function, to be used to allocate memory.</span></span> 
    
 <span data-ttu-id="d1d15-120">_lpAllocateMore_</span><span class="sxs-lookup"><span data-stu-id="d1d15-120">_lpAllocateMore_</span></span>
  
> <span data-ttu-id="d1d15-121">[in] Указатель на [функцию MAPIAllocateMore,](mapiallocatemore.md) которая используется для выделения дополнительной памяти.</span><span class="sxs-lookup"><span data-stu-id="d1d15-121">[in] Pointer to the [MAPIAllocateMore](mapiallocatemore.md) function, to be used to allocate additional memory.</span></span> 
    
 <span data-ttu-id="d1d15-122">_lpFreeBuffer_</span><span class="sxs-lookup"><span data-stu-id="d1d15-122">_lpFreeBuffer_</span></span>
  
> <span data-ttu-id="d1d15-123">[in] Указатель на [функцию MAPIFreeBuffer,](mapifreebuffer.md) которая используется для освободить память.</span><span class="sxs-lookup"><span data-stu-id="d1d15-123">[in] Pointer to the [MAPIFreeBuffer](mapifreebuffer.md) function, to be used to free memory.</span></span> 
    
 <span data-ttu-id="d1d15-124">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="d1d15-124">_ulFlags_</span></span>
  
> <span data-ttu-id="d1d15-125">[in] Битоваяmas флагов.</span><span class="sxs-lookup"><span data-stu-id="d1d15-125">[in] Bitmask of flags.</span></span> <span data-ttu-id="d1d15-126">Можно установить следующий флаг:</span><span class="sxs-lookup"><span data-stu-id="d1d15-126">The following flag can be set:</span></span>
    
<span data-ttu-id="d1d15-127">MAPI_NT_SERVICE</span><span class="sxs-lookup"><span data-stu-id="d1d15-127">MAPI_NT_SERVICE</span></span> 
  
> <span data-ttu-id="d1d15-128">Поставщик загружается в контексте службы Windows— особого типа процесса без доступа к пользовательскому интерфейсу.</span><span class="sxs-lookup"><span data-stu-id="d1d15-128">The provider is being loaded in the context of a Windows service, a special type of process without access to any user interface.</span></span> 
    
 <span data-ttu-id="d1d15-129">_ulMAPIVer_</span><span class="sxs-lookup"><span data-stu-id="d1d15-129">_ulMAPIVer_</span></span>
  
> <span data-ttu-id="d1d15-130">[in] Номер версии интерфейса поставщика услуг (SPI), который использует MAPI.</span><span class="sxs-lookup"><span data-stu-id="d1d15-130">[in] Version number of the service provider interface (SPI) that MAPI uses.</span></span> <span data-ttu-id="d1d15-131">Номер текущей версии см. в файле заголовок Mapispi.h.</span><span class="sxs-lookup"><span data-stu-id="d1d15-131">For the current version number, see the Mapispi.h header file.</span></span> 
    
 <span data-ttu-id="d1d15-132">_lpulProviderVer_</span><span class="sxs-lookup"><span data-stu-id="d1d15-132">_lpulProviderVer_</span></span>
  
> <span data-ttu-id="d1d15-133">[out] Указатель на номер версии SPI, который использует этот поставщик хранилище сообщений.</span><span class="sxs-lookup"><span data-stu-id="d1d15-133">[out] Pointer to the version number of the SPI that this message store provider uses.</span></span> 
    
 <span data-ttu-id="d1d15-134">_lppMSProvider_</span><span class="sxs-lookup"><span data-stu-id="d1d15-134">_lppMSProvider_</span></span>
  
> <span data-ttu-id="d1d15-135">[out] Указатель на указатель на инициализированный объект поставщика хранения сообщений.</span><span class="sxs-lookup"><span data-stu-id="d1d15-135">[out] Pointer to a pointer to the initialized message store provider object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="d1d15-136">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="d1d15-136">Return value</span></span>

<span data-ttu-id="d1d15-137">S_OK</span><span class="sxs-lookup"><span data-stu-id="d1d15-137">S_OK</span></span> 
  
> <span data-ttu-id="d1d15-138">����� ������� � ������ ��������� ��������� ��� ��������.</span><span class="sxs-lookup"><span data-stu-id="d1d15-138">The call succeeded and has returned the expected value or values.</span></span> 
    
<span data-ttu-id="d1d15-139">MAPI_E_VERSION</span><span class="sxs-lookup"><span data-stu-id="d1d15-139">MAPI_E_VERSION</span></span> 
  
> <span data-ttu-id="d1d15-140">Версия SPI, используемая MAPI, несовместима с SPI, используемым этим поставщиком.</span><span class="sxs-lookup"><span data-stu-id="d1d15-140">The SPI version being used by MAPI is not compatible with the SPI being used by this provider.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="d1d15-141">Примечания</span><span class="sxs-lookup"><span data-stu-id="d1d15-141">Remarks</span></span>

<span data-ttu-id="d1d15-142">MAPI вызывает функцию точки входа **MSProviderInit** для инициализации поставщика магазина сообщений после входа клиента.</span><span class="sxs-lookup"><span data-stu-id="d1d15-142">MAPI calls the entry point function **MSProviderInit** to initialize a message store provider following a client logon.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="d1d15-143">Примечания для исполнителей</span><span class="sxs-lookup"><span data-stu-id="d1d15-143">Notes to implementers</span></span>

<span data-ttu-id="d1d15-144">Поставщик точки входа должен реализовать **MSProviderInit** в DLL поставщика.</span><span class="sxs-lookup"><span data-stu-id="d1d15-144">A message store provider must implement **MSProviderInit** as an entry point function in the provider's DLL.</span></span> <span data-ttu-id="d1d15-145">Реализация должна быть основана на прототипе функции **MSPROVIDERINIT,** также указанном в MAPISPI.H.</span><span class="sxs-lookup"><span data-stu-id="d1d15-145">The implementation must be based on the **MSPROVIDERINIT** function prototype, also specified in MAPISPI.H.</span></span> <span data-ttu-id="d1d15-146">MAPI определяет **MSPROVIDERINIT** для использования стандартного типа вызова инициализации MAPI STDMAPIINITCALLTYPE, что приводит к следуют соглашению о вызовах CDECL **msProviderInit.**</span><span class="sxs-lookup"><span data-stu-id="d1d15-146">MAPI defines **MSPROVIDERINIT** to use the standard MAPI initialization call type, STDMAPIINITCALLTYPE, which causes **MSProviderInit** to follow the CDECL calling convention.</span></span> <span data-ttu-id="d1d15-147">Преимуществом CDECL является возможность попытки вызова, даже если количество параметров вызова не соответствует числу заданных параметров.</span><span class="sxs-lookup"><span data-stu-id="d1d15-147">An advantage of CDECL is that calls can be attempted even if the number of calling parameters does not match the number of defined parameters.</span></span> 
  
<span data-ttu-id="d1d15-148">Поставщик может быть инициализирован несколько раз в результате одновременного использования нескольких профилей или появления в одном профиле более одного раза.</span><span class="sxs-lookup"><span data-stu-id="d1d15-148">A provider can be initialized multiple times, as a result of appearing in several profiles in simultaneous use or of appearing more than once in the same profile.</span></span> <span data-ttu-id="d1d15-149">Поскольку объект поставщика содержит контекст, **MSProviderInit** должен возвращать разные объекты поставщика в  _lppMSProvider_ для каждой инициализации даже для нескольких инициализации в одном процессе.</span><span class="sxs-lookup"><span data-stu-id="d1d15-149">Because the provider object contains context, **MSProviderInit** must return a different provider object in  _lppMSProvider_ for each initialization, even for multiple initializations in the same process.</span></span> 
  
<span data-ttu-id="d1d15-150">DLL поставщика не следует связывать с Mapix.dll.</span><span class="sxs-lookup"><span data-stu-id="d1d15-150">The provider DLL should not be linked with Mapix.dll.</span></span> <span data-ttu-id="d1d15-151">Вместо этого он должен использовать эти указатели для выделения памяти или распределения памяти.</span><span class="sxs-lookup"><span data-stu-id="d1d15-151">Instead, it should use these pointers for memory allocation or deallocation.</span></span> 
  
<span data-ttu-id="d1d15-152">Поставщик store сообщений должен использовать функции, на которые указывают  _lpAllocateBuffer,_  _lpAllocateMore_ и  _lpFreeBuffer_ для выделения и распределения памяти.</span><span class="sxs-lookup"><span data-stu-id="d1d15-152">The message store provider should use the functions pointed to by  _lpAllocateBuffer_,  _lpAllocateMore_, and  _lpFreeBuffer_ for most memory allocation and deallocation.</span></span> <span data-ttu-id="d1d15-153">В частности, поставщик должен использовать эти функции для выделения памяти для использования клиентских приложений при вызове интерфейсов объектов, таких как [IMAPIProp::GetProps](imapiprop-getprops.md) и [IMAPITable::QueryRows](imapitable-queryrows.md).</span><span class="sxs-lookup"><span data-stu-id="d1d15-153">In particular, the provider must use these functions to allocate memory for use by client applications when calling object interfaces such as [IMAPIProp::GetProps](imapiprop-getprops.md) and [IMAPITable::QueryRows](imapitable-queryrows.md).</span></span> <span data-ttu-id="d1d15-154">Если поставщик также ожидает использовать память OLE, он должен вызвать метод **IUnknown::AddRef** объекта allocator, на который указывает параметр _lpMalloc._</span><span class="sxs-lookup"><span data-stu-id="d1d15-154">If the provider also expects to use the OLE memory allocator, it should call the **IUnknown::AddRef** method of the allocator object pointed to by the  _lpMalloc_ parameter.</span></span> 
  
<span data-ttu-id="d1d15-155">Дополнительные сведения о написании **MSProviderInit** см. в подпрограмме ["Загрузка поставщиков store сообщений".](loading-message-store-providers.md)</span><span class="sxs-lookup"><span data-stu-id="d1d15-155">For more information about writing **MSProviderInit**, see [Loading Message Store Providers](loading-message-store-providers.md).</span></span> <span data-ttu-id="d1d15-156">Дополнительные сведения о функциях точек входа см. в [реализации функции](implementing-a-service-provider-entry-point-function.md)точки входа поставщика услуг.</span><span class="sxs-lookup"><span data-stu-id="d1d15-156">For more information about entry point functions, see [Implementing a Service Provider Entry Point Function](implementing-a-service-provider-entry-point-function.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="d1d15-157">См. также</span><span class="sxs-lookup"><span data-stu-id="d1d15-157">See also</span></span>



[<span data-ttu-id="d1d15-158">ABProviderInit</span><span class="sxs-lookup"><span data-stu-id="d1d15-158">ABProviderInit</span></span>](abproviderinit.md)
  
[<span data-ttu-id="d1d15-159">IMSProvider : IUnknown</span><span class="sxs-lookup"><span data-stu-id="d1d15-159">IMSProvider : IUnknown</span></span>](imsprovideriunknown.md)
  
[<span data-ttu-id="d1d15-160">XPProviderInit</span><span class="sxs-lookup"><span data-stu-id="d1d15-160">XPProviderInit</span></span>](xpproviderinit.md)

