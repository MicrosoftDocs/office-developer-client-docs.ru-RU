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
ms.openlocfilehash: cf1febe89c49b29cdfaf8d27760c4fb27b4c4990
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19810032"
---
# <a name="msproviderinit"></a><span data-ttu-id="d8482-103">MSProviderInit</span><span class="sxs-lookup"><span data-stu-id="d8482-103">MSProviderInit</span></span>

  
  
<span data-ttu-id="d8482-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="d8482-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="d8482-105">Инициализирует поставщика хранилища сообщений для операции.</span><span class="sxs-lookup"><span data-stu-id="d8482-105">Initializes a message store provider for operation.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="d8482-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="d8482-106">Header file:</span></span>  <br/> |<span data-ttu-id="d8482-107">Mapispi.h</span><span class="sxs-lookup"><span data-stu-id="d8482-107">Mapispi.h</span></span>  <br/> |
|<span data-ttu-id="d8482-108">Реализованный:</span><span class="sxs-lookup"><span data-stu-id="d8482-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="d8482-109">Поставщики хранилища сообщений</span><span class="sxs-lookup"><span data-stu-id="d8482-109">Message store providers</span></span>  <br/> |
|<span data-ttu-id="d8482-110">Вызывается:</span><span class="sxs-lookup"><span data-stu-id="d8482-110">Called by:</span></span>  <br/> |<span data-ttu-id="d8482-111">MAPI</span><span class="sxs-lookup"><span data-stu-id="d8482-111">MAPI</span></span>  <br/> |
   
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

## <a name="parameters"></a><span data-ttu-id="d8482-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="d8482-112">Parameters</span></span>

 <span data-ttu-id="d8482-113">_hInstance_</span><span class="sxs-lookup"><span data-stu-id="d8482-113">_hInstance_</span></span>
  
> <span data-ttu-id="d8482-114">[in] Экземпляр сообщения хранилища поставщика динамической библиотеки (DLL), который используется MAPI, когда она связана.</span><span class="sxs-lookup"><span data-stu-id="d8482-114">[in] The instance of the message store provider's dynamic-link library (DLL) that MAPI used when it linked.</span></span> 
    
 <span data-ttu-id="d8482-115">_lpMalloc_</span><span class="sxs-lookup"><span data-stu-id="d8482-115">_lpMalloc_</span></span>
  
> <span data-ttu-id="d8482-116">[in] Указатель на объект распределителя памяти, предоставление интерфейса OLE **IMalloc** .</span><span class="sxs-lookup"><span data-stu-id="d8482-116">[in] Pointer to a memory allocator object exposing the OLE **IMalloc** interface.</span></span> <span data-ttu-id="d8482-117">Поставщик хранения сообщений может потребоваться использовать этот метод для распределения при работе с определенных интерфейсов, таких как **IStream**.</span><span class="sxs-lookup"><span data-stu-id="d8482-117">The message store provider may need to use this allocation method when working with certain interfaces such as **IStream**.</span></span> 
    
 <span data-ttu-id="d8482-118">_lpAllocateBuffer_</span><span class="sxs-lookup"><span data-stu-id="d8482-118">_lpAllocateBuffer_</span></span>
  
> <span data-ttu-id="d8482-119">[in] Указатель на функцию [MAPIAllocateBuffer](mapiallocatebuffer.md) , которые будут использоваться для выделения памяти.</span><span class="sxs-lookup"><span data-stu-id="d8482-119">[in] Pointer to the [MAPIAllocateBuffer](mapiallocatebuffer.md) function, to be used to allocate memory.</span></span> 
    
 <span data-ttu-id="d8482-120">_lpAllocateMore_</span><span class="sxs-lookup"><span data-stu-id="d8482-120">_lpAllocateMore_</span></span>
  
> <span data-ttu-id="d8482-121">[in] Указатель на функцию [MAPIAllocateMore](mapiallocatemore.md) , которые будут использоваться для выделения дополнительной памяти.</span><span class="sxs-lookup"><span data-stu-id="d8482-121">[in] Pointer to the [MAPIAllocateMore](mapiallocatemore.md) function, to be used to allocate additional memory.</span></span> 
    
 <span data-ttu-id="d8482-122">_lpFreeBuffer_</span><span class="sxs-lookup"><span data-stu-id="d8482-122">_lpFreeBuffer_</span></span>
  
> <span data-ttu-id="d8482-123">[in] Указатель на функцию [MAPIFreeBuffer](mapifreebuffer.md) , которые будут использоваться для свободного использования памяти.</span><span class="sxs-lookup"><span data-stu-id="d8482-123">[in] Pointer to the [MAPIFreeBuffer](mapifreebuffer.md) function, to be used to free memory.</span></span> 
    
 <span data-ttu-id="d8482-124">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="d8482-124">_ulFlags_</span></span>
  
> <span data-ttu-id="d8482-125">[in] Битовая маска флаги.</span><span class="sxs-lookup"><span data-stu-id="d8482-125">[in] Bitmask of flags.</span></span> <span data-ttu-id="d8482-126">Можно задать следующий флаг:</span><span class="sxs-lookup"><span data-stu-id="d8482-126">The following flag can be set:</span></span>
    
<span data-ttu-id="d8482-127">MAPI_NT_SERVICE</span><span class="sxs-lookup"><span data-stu-id="d8482-127">MAPI_NT_SERVICE</span></span> 
  
> <span data-ttu-id="d8482-128">Поставщик загружается в контексте службы Windows, особый тип процесса без доступа к любой пользовательский интерфейс.</span><span class="sxs-lookup"><span data-stu-id="d8482-128">The provider is being loaded in the context of a Windows service, a special type of process without access to any user interface.</span></span> 
    
 <span data-ttu-id="d8482-129">_ulMAPIVer_</span><span class="sxs-lookup"><span data-stu-id="d8482-129">_ulMAPIVer_</span></span>
  
> <span data-ttu-id="d8482-130">[in] Номер версии поставщика службы интерфейса (SPI), который использует MAPI.</span><span class="sxs-lookup"><span data-stu-id="d8482-130">[in] Version number of the service provider interface (SPI) that MAPI uses.</span></span> <span data-ttu-id="d8482-131">Файл заголовка Mapispi.h текущий номер версии, см.</span><span class="sxs-lookup"><span data-stu-id="d8482-131">For the current version number, see the Mapispi.h header file.</span></span> 
    
 <span data-ttu-id="d8482-132">_lpulProviderVer_</span><span class="sxs-lookup"><span data-stu-id="d8482-132">_lpulProviderVer_</span></span>
  
> <span data-ttu-id="d8482-133">[out] Указатель на номер версии индекс параметров безопасности, которая использует этот поставщик хранения сообщений.</span><span class="sxs-lookup"><span data-stu-id="d8482-133">[out] Pointer to the version number of the SPI that this message store provider uses.</span></span> 
    
 <span data-ttu-id="d8482-134">_lppMSProvider_</span><span class="sxs-lookup"><span data-stu-id="d8482-134">_lppMSProvider_</span></span>
  
> <span data-ttu-id="d8482-135">[out] Указатель на указатель на объект поставщика хранилища инициализированную сообщения.</span><span class="sxs-lookup"><span data-stu-id="d8482-135">[out] Pointer to a pointer to the initialized message store provider object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="d8482-136">������������ ��������</span><span class="sxs-lookup"><span data-stu-id="d8482-136">Return value</span></span>

<span data-ttu-id="d8482-137">ЗНАЧЕНИЕ S_OK</span><span class="sxs-lookup"><span data-stu-id="d8482-137">S_OK</span></span> 
  
> <span data-ttu-id="d8482-138">����� ������� � ������ ��������� ��������� ��� ��������.</span><span class="sxs-lookup"><span data-stu-id="d8482-138">The call succeeded and has returned the expected value or values.</span></span> 
    
<span data-ttu-id="d8482-139">MAPI_E_VERSION</span><span class="sxs-lookup"><span data-stu-id="d8482-139">MAPI_E_VERSION</span></span> 
  
> <span data-ttu-id="d8482-140">Версия SPI, используемые MAPI не совместимый с индекс параметров безопасности, используемые этим поставщиком.</span><span class="sxs-lookup"><span data-stu-id="d8482-140">The SPI version being used by MAPI is not compatible with the SPI being used by this provider.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="d8482-141">Замечания</span><span class="sxs-lookup"><span data-stu-id="d8482-141">Remarks</span></span>

<span data-ttu-id="d8482-142">MAPI вызывает функцию точки входа **MSProviderInit** для инициализации поставщика хранилища сообщений после входа клиента.</span><span class="sxs-lookup"><span data-stu-id="d8482-142">MAPI calls the entry point function **MSProviderInit** to initialize a message store provider following a client logon.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="d8482-143">Примечания для исполнителей</span><span class="sxs-lookup"><span data-stu-id="d8482-143">Notes to implementers</span></span>

<span data-ttu-id="d8482-144">Поставщик хранения сообщений необходимо реализовать **MSProviderInit** как функцию точки входа в DLL поставщика.</span><span class="sxs-lookup"><span data-stu-id="d8482-144">A message store provider must implement **MSProviderInit** as an entry point function in the provider's DLL.</span></span> <span data-ttu-id="d8482-145">Реализация должны быть основаны на прототип функции **MSPROVIDERINIT** также указано в MAPISPI. З.</span><span class="sxs-lookup"><span data-stu-id="d8482-145">The implementation must be based on the **MSPROVIDERINIT** function prototype, also specified in MAPISPI.H.</span></span> <span data-ttu-id="d8482-146">MAPI определяет **MSPROVIDERINIT** для использования типа стандартный вызова инициализации MAPI, STDMAPIINITCALLTYPE, что активирует **MSProviderInit** необходимо выполнить соглашение о вызовах CDECL.</span><span class="sxs-lookup"><span data-stu-id="d8482-146">MAPI defines **MSPROVIDERINIT** to use the standard MAPI initialization call type, STDMAPIINITCALLTYPE, which causes **MSProviderInit** to follow the CDECL calling convention.</span></span> <span data-ttu-id="d8482-147">Преимуществом CDECL — даже в том случае, если число вызовов параметров не соответствует количество определенных параметров может выполняться звонки.</span><span class="sxs-lookup"><span data-stu-id="d8482-147">An advantage of CDECL is that calls can be attempted even if the number of calling parameters does not match the number of defined parameters.</span></span> 
  
<span data-ttu-id="d8482-148">Поставщик может быть инициализирован несколько раз, из-за изображения которых появляются в несколько профилей в одновременное использование или отображение более одного раза в одном профиле.</span><span class="sxs-lookup"><span data-stu-id="d8482-148">A provider can be initialized multiple times, as a result of appearing in several profiles in simultaneous use or of appearing more than once in the same profile.</span></span> <span data-ttu-id="d8482-149">Поскольку объект поставщика содержит контекста, **MSProviderInit** необходимо возвратить объект другого поставщика в _lppMSProvider_ для каждой инициализации, даже для нескольких инициализации в одном процессе.</span><span class="sxs-lookup"><span data-stu-id="d8482-149">Because the provider object contains context, **MSProviderInit** must return a different provider object in  _lppMSProvider_ for each initialization, even for multiple initializations in the same process.</span></span> 
  
<span data-ttu-id="d8482-150">Библиотека поставщика не должны быть связаны с Mapix.dll.</span><span class="sxs-lookup"><span data-stu-id="d8482-150">The provider DLL should not be linked with Mapix.dll.</span></span> <span data-ttu-id="d8482-151">Вместо этого следует использовать эти указатели для выделения памяти или освобождение.</span><span class="sxs-lookup"><span data-stu-id="d8482-151">Instead, it should use these pointers for memory allocation or deallocation.</span></span> 
  
<span data-ttu-id="d8482-152">Поставщик хранения сообщений следует использовать функции, на который указывает _lpAllocateBuffer_, _lpAllocateMore_и _lpFreeBuffer_ для большинства выделение и освобождение памяти.</span><span class="sxs-lookup"><span data-stu-id="d8482-152">The message store provider should use the functions pointed to by  _lpAllocateBuffer_,  _lpAllocateMore_, and  _lpFreeBuffer_ for most memory allocation and deallocation.</span></span> <span data-ttu-id="d8482-153">В частности поставщик должен использовать эти функции для выделения памяти для использования с клиентскими приложениями при вызове интерфейсы объекта, такие как [IMAPIProp::GetProps](imapiprop-getprops.md) и [IMAPITable::QueryRows](imapitable-queryrows.md).</span><span class="sxs-lookup"><span data-stu-id="d8482-153">In particular, the provider must use these functions to allocate memory for use by client applications when calling object interfaces such as [IMAPIProp::GetProps](imapiprop-getprops.md) and [IMAPITable::QueryRows](imapitable-queryrows.md).</span></span> <span data-ttu-id="d8482-154">Если поставщик также требуется для использования распределителя памяти OLE, он должен вызвать метод **IUnknown::AddRef** распределителя объект, указанный в параметре _lpMalloc_ .</span><span class="sxs-lookup"><span data-stu-id="d8482-154">If the provider also expects to use the OLE memory allocator, it should call the **IUnknown::AddRef** method of the allocator object pointed to by the  _lpMalloc_ parameter.</span></span> 
  
<span data-ttu-id="d8482-155">Дополнительные сведения о написании **MSProviderInit**можно [Загрузка поставщиков хранилища сообщений](loading-message-store-providers.md).</span><span class="sxs-lookup"><span data-stu-id="d8482-155">For more information about writing **MSProviderInit**, see [Loading Message Store Providers](loading-message-store-providers.md).</span></span> <span data-ttu-id="d8482-156">Дополнительные сведения о функциях точки входа [реализации функции выберите запись службы поставщика](implementing-a-service-provider-entry-point-function.md)см.</span><span class="sxs-lookup"><span data-stu-id="d8482-156">For more information about entry point functions, see [Implementing a Service Provider Entry Point Function](implementing-a-service-provider-entry-point-function.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="d8482-157">См. также</span><span class="sxs-lookup"><span data-stu-id="d8482-157">See also</span></span>



[<span data-ttu-id="d8482-158">ABProviderInit</span><span class="sxs-lookup"><span data-stu-id="d8482-158">ABProviderInit</span></span>](abproviderinit.md)
  
[<span data-ttu-id="d8482-159">IMSProvider : IUnknown</span><span class="sxs-lookup"><span data-stu-id="d8482-159">IMSProvider : IUnknown</span></span>](imsprovideriunknown.md)
  
[<span data-ttu-id="d8482-160">XPProviderInit</span><span class="sxs-lookup"><span data-stu-id="d8482-160">XPProviderInit</span></span>](xpproviderinit.md)

