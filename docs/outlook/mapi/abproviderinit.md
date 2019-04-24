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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328114"
---
# <a name="abproviderinit"></a><span data-ttu-id="3db7c-103">ABProviderInit</span><span class="sxs-lookup"><span data-stu-id="3db7c-103">ABProviderInit</span></span>
 
<span data-ttu-id="3db7c-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3db7c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3db7c-105">Инициализирует поставщик адресных книг для операции.</span><span class="sxs-lookup"><span data-stu-id="3db7c-105">Initializes an address book provider for operation.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="3db7c-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="3db7c-106">Header file:</span></span>  <br/> |<span data-ttu-id="3db7c-107">Маписпи. h</span><span class="sxs-lookup"><span data-stu-id="3db7c-107">Mapispi.h</span></span>  <br/> |
|<span data-ttu-id="3db7c-108">Реализовано в:</span><span class="sxs-lookup"><span data-stu-id="3db7c-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="3db7c-109">Поставщики адресных книг</span><span class="sxs-lookup"><span data-stu-id="3db7c-109">Address book providers</span></span>  <br/> |
|<span data-ttu-id="3db7c-110">Вызывающая сторона:</span><span class="sxs-lookup"><span data-stu-id="3db7c-110">Called by:</span></span>  <br/> |<span data-ttu-id="3db7c-111">MAPI</span><span class="sxs-lookup"><span data-stu-id="3db7c-111">MAPI</span></span>  <br/> |
   
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

## <a name="parameters"></a><span data-ttu-id="3db7c-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="3db7c-112">Parameters</span></span>

 <span data-ttu-id="3db7c-113">_hInstance_</span><span class="sxs-lookup"><span data-stu-id="3db7c-113">_hInstance_</span></span>
  
> <span data-ttu-id="3db7c-114">возврата Экземпляр библиотеки динамической компоновки (DLL) поставщика адресных книг, которая используется MAPI при связывании.</span><span class="sxs-lookup"><span data-stu-id="3db7c-114">[in] The instance of the address book provider's dynamic-link library (DLL) that MAPI used when it linked.</span></span> 
    
 <span data-ttu-id="3db7c-115">_Лпмаллок_</span><span class="sxs-lookup"><span data-stu-id="3db7c-115">_lpMalloc_</span></span>
  
> <span data-ttu-id="3db7c-116">возврата Указатель на объект распределителя памяти, который предоставляет интерфейс для **выделения** OLE.</span><span class="sxs-lookup"><span data-stu-id="3db7c-116">[in] Pointer to a memory allocator object exposing the OLE **IMalloc** interface.</span></span> <span data-ttu-id="3db7c-117">Для работы с определенными интерфейсами, такими как **IStream**, поставщику адресной книги может потребоваться использовать этот метод распределения.</span><span class="sxs-lookup"><span data-stu-id="3db7c-117">The address book provider may need to use this allocation method when working with certain interfaces such as **IStream**.</span></span> 
    
 <span data-ttu-id="3db7c-118">_Лпаллокатебуффер_</span><span class="sxs-lookup"><span data-stu-id="3db7c-118">_lpAllocateBuffer_</span></span>
  
> <span data-ttu-id="3db7c-119">возврата Указатель на функцию [мапиаллокатебуффер](mapiallocatebuffer.md) , которая будет использоваться, когда интерфейс MAPI требует выделить память.</span><span class="sxs-lookup"><span data-stu-id="3db7c-119">[in] Pointer to the [MAPIAllocateBuffer](mapiallocatebuffer.md) function, to be used where required by MAPI to allocate memory.</span></span> 
    
 <span data-ttu-id="3db7c-120">_Лпаллокатеморе_</span><span class="sxs-lookup"><span data-stu-id="3db7c-120">_lpAllocateMore_</span></span>
  
> <span data-ttu-id="3db7c-121">возврата Указатель на функцию [мапиаллокатеморе](mapiallocatemore.md) , которая будет использоваться, когда интерфейс MAPI требует выделить дополнительную память.</span><span class="sxs-lookup"><span data-stu-id="3db7c-121">[in] Pointer to the [MAPIAllocateMore](mapiallocatemore.md) function, to be used where required by MAPI to allocate additional memory.</span></span> 
    
 <span data-ttu-id="3db7c-122">_Лпфрибуффер_</span><span class="sxs-lookup"><span data-stu-id="3db7c-122">_lpFreeBuffer_</span></span>
  
> <span data-ttu-id="3db7c-123">возврата Указатель на функцию [мапифрибуффер](mapifreebuffer.md) , которая будет использоваться, когда требуется для освобождения памяти MAPI.</span><span class="sxs-lookup"><span data-stu-id="3db7c-123">[in] Pointer to the [MAPIFreeBuffer](mapifreebuffer.md) function, to be used where required by MAPI to free memory.</span></span> 
    
 <span data-ttu-id="3db7c-124">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="3db7c-124">_ulFlags_</span></span>
  
> <span data-ttu-id="3db7c-125">возврата Битовая маска флагов.</span><span class="sxs-lookup"><span data-stu-id="3db7c-125">[in] Bitmask of flags.</span></span> <span data-ttu-id="3db7c-126">Можно задать следующий флаг:</span><span class="sxs-lookup"><span data-stu-id="3db7c-126">The following flag can be set:</span></span>
    
<span data-ttu-id="3db7c-127">МАПИ_НТ_СЕРВИЦЕ</span><span class="sxs-lookup"><span data-stu-id="3db7c-127">MAPI_NT_SERVICE</span></span> 
  
> <span data-ttu-id="3db7c-128">Поставщик загружается в контексте службы Windows — особого типа процесса без доступа к любому пользовательскому интерфейсу.</span><span class="sxs-lookup"><span data-stu-id="3db7c-128">The provider is being loaded in the context of a Windows service, a special type of process without access to any user interface.</span></span> 
    
 <span data-ttu-id="3db7c-129">_Улмапивер_</span><span class="sxs-lookup"><span data-stu-id="3db7c-129">_ulMAPIVer_</span></span>
  
> <span data-ttu-id="3db7c-130">возврата Номер версии интерфейса поставщика услуг (SPI), который является MAPI. Библиотека DLL использует.</span><span class="sxs-lookup"><span data-stu-id="3db7c-130">[in] Version number of the service provider interface (SPI) that MAPI.DLL uses.</span></span> <span data-ttu-id="3db7c-131">Текущий номер версии приведен в разделе МАПИСПИ. H файл заголовка.</span><span class="sxs-lookup"><span data-stu-id="3db7c-131">For the current version number, see the MAPISPI.H header file.</span></span> 
    
 <span data-ttu-id="3db7c-132">_Лпулпровидервер_</span><span class="sxs-lookup"><span data-stu-id="3db7c-132">_lpulProviderVer_</span></span>
  
> <span data-ttu-id="3db7c-133">вышли Указатель на номер версии SPI, который использует этот поставщик адресных книг.</span><span class="sxs-lookup"><span data-stu-id="3db7c-133">[out] Pointer to the version number of the SPI that this address book provider uses.</span></span> 
    
 <span data-ttu-id="3db7c-134">_Лппабпровидер_</span><span class="sxs-lookup"><span data-stu-id="3db7c-134">_lppABProvider_</span></span>
  
> <span data-ttu-id="3db7c-135">вышли Указатель на указатель инициализированного объекта поставщика адресных книг.</span><span class="sxs-lookup"><span data-stu-id="3db7c-135">[out] Pointer to a pointer to the initialized address book provider object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="3db7c-136">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="3db7c-136">Return value</span></span>

<span data-ttu-id="3db7c-137">S_OK</span><span class="sxs-lookup"><span data-stu-id="3db7c-137">S_OK</span></span> 
  
> <span data-ttu-id="3db7c-138">����� ������� � ������ ��������� ��������� ��� ��������.</span><span class="sxs-lookup"><span data-stu-id="3db7c-138">The call succeeded and has returned the expected value or values.</span></span> 
    
<span data-ttu-id="3db7c-139">МАПИ_Е_ВЕРСИОН</span><span class="sxs-lookup"><span data-stu-id="3db7c-139">MAPI_E_VERSION</span></span> 
  
> <span data-ttu-id="3db7c-140">Версия SPI, используемая MAPI, несовместима с SPI, используемым этим поставщиком.</span><span class="sxs-lookup"><span data-stu-id="3db7c-140">The SPI version being used by MAPI is not compatible with the SPI being used by this provider.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="3db7c-141">Комментарии</span><span class="sxs-lookup"><span data-stu-id="3db7c-141">Remarks</span></span>

<span data-ttu-id="3db7c-142">MAPI вызывает функцию точки входа **абпровидеринит** для инициализации поставщика адресных книг после входа клиента.</span><span class="sxs-lookup"><span data-stu-id="3db7c-142">MAPI calls the entry point function **ABProviderInit** to initialize an address book provider following a client logon.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="3db7c-143">Примечания для исполнителей</span><span class="sxs-lookup"><span data-stu-id="3db7c-143">Notes to implementers</span></span>

<span data-ttu-id="3db7c-144">Поставщик адресных книг должен реализовать **абпровидеринит** в качестве функции точки входа в DLL поставщика.</span><span class="sxs-lookup"><span data-stu-id="3db7c-144">An address book provider must implement **ABProviderInit** as an entry point function in the provider's DLL.</span></span> <span data-ttu-id="3db7c-145">Реализация должна основываться на прототипе функции **абпровидеринит** , также указанном в маписпи. Высоты.</span><span class="sxs-lookup"><span data-stu-id="3db7c-145">The implementation must be based on the **ABPROVIDERINIT** function prototype, also specified in MAPISPI.H.</span></span> <span data-ttu-id="3db7c-146">MAPI определяет **абпровидеринит** для использования стандартного типа вызова инициализации MAPI, стдмапииниткаллтипе, что заставляет **абпровидеринит** следовать соглашению о вызовах кдекл.</span><span class="sxs-lookup"><span data-stu-id="3db7c-146">MAPI defines **ABPROVIDERINIT** to use the standard MAPI initialization call type, STDMAPIINITCALLTYPE, which causes **ABProviderInit** to follow the CDECL calling convention.</span></span> 
  
<span data-ttu-id="3db7c-147">Поставщик может быть инициализирован несколько раз в результате того, что в одном и том же профиле появлялось несколько профилей в одновременном использовании или несколько раз.</span><span class="sxs-lookup"><span data-stu-id="3db7c-147">A provider can be initialized multiple times, as a result of appearing in several profiles in simultaneous use or of appearing more than once in the same profile.</span></span> <span data-ttu-id="3db7c-148">Так как объект provider содержит Context, **абпровидеринит** должен возвратить другой объект поставщика в _лппабпровидер_ для каждой инициализации, даже для нескольких инициализаций в одном процессе.</span><span class="sxs-lookup"><span data-stu-id="3db7c-148">Because the provider object contains context, **ABProviderInit** must return a different provider object in  _lppABProvider_ for each initialization, even for multiple initializations in the same process.</span></span> 
  
<span data-ttu-id="3db7c-149">Поставщик адресных книг должен использовать функции, на которые указывает _лпаллокатебуффер_, _лпаллокатеморе_и _лпфрибуффер_ для большинства выделений и освобождений памяти.</span><span class="sxs-lookup"><span data-stu-id="3db7c-149">The address book provider should use the functions pointed to by  _lpAllocateBuffer_,  _lpAllocateMore_, and  _lpFreeBuffer_ for most memory allocation and deallocation.</span></span> <span data-ttu-id="3db7c-150">В частности, поставщик должен использовать эти функции для выделения памяти, которая будет использоваться клиентскими приложениями при вызове интерфейсов объектов, таких как [IMAPIProp::](imapiprop-getprops.md) /PROPS и [IMAPITable:: QueryRows](imapitable-queryrows.md).</span><span class="sxs-lookup"><span data-stu-id="3db7c-150">In particular, the provider must use these functions to allocate memory for use by client applications when calling object interfaces such as [IMAPIProp::GetProps](imapiprop-getprops.md) and [IMAPITable::QueryRows](imapitable-queryrows.md).</span></span> <span data-ttu-id="3db7c-151">Если поставщик также ожидает использования распределителя памяти OLE, он должен вызывать метод **IUnknown:: AddRef** объекта распределителя, на который указывает параметр _лпмаллок_ .</span><span class="sxs-lookup"><span data-stu-id="3db7c-151">If the provider also expects to use the OLE memory allocator, it should call the **IUnknown::AddRef** method of the allocator object pointed to by the  _lpMalloc_ parameter.</span></span> 
  
<span data-ttu-id="3db7c-152">Дополнительные сведения о создании **абпровидеринит**можно найти в статье [Реализация функции точки входа поставщика адресных книг](implementing-an-address-book-provider-entry-point-function.md).</span><span class="sxs-lookup"><span data-stu-id="3db7c-152">For more information on writing **ABProviderInit**, see [Implementing an Address Book Provider Entry Point Function](implementing-an-address-book-provider-entry-point-function.md).</span></span> <span data-ttu-id="3db7c-153">Дополнительные сведения о функциях точки входа можно найти в статье [Реализация функции точки входа поставщика услуг](implementing-a-service-provider-entry-point-function.md).</span><span class="sxs-lookup"><span data-stu-id="3db7c-153">For more information on entry point functions, see [Implementing a Service Provider Entry Point Function](implementing-a-service-provider-entry-point-function.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="3db7c-154">См. также</span><span class="sxs-lookup"><span data-stu-id="3db7c-154">See also</span></span>

- [<span data-ttu-id="3db7c-155">IABProvider : IUnknown</span><span class="sxs-lookup"><span data-stu-id="3db7c-155">IABProvider : IUnknown</span></span>](iabprovideriunknown.md) 
- [<span data-ttu-id="3db7c-156">MSProviderInit</span><span class="sxs-lookup"><span data-stu-id="3db7c-156">MSProviderInit</span></span>](msproviderinit.md)
- [<span data-ttu-id="3db7c-157">XPProviderInit</span><span class="sxs-lookup"><span data-stu-id="3db7c-157">XPProviderInit</span></span>](xpproviderinit.md)

