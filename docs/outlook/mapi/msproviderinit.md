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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32342793"
---
# <a name="msproviderinit"></a><span data-ttu-id="9239e-103">MSProviderInit</span><span class="sxs-lookup"><span data-stu-id="9239e-103">MSProviderInit</span></span>

  
  
<span data-ttu-id="9239e-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9239e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9239e-105">Инициализирует поставщик хранилища сообщений для операции.</span><span class="sxs-lookup"><span data-stu-id="9239e-105">Initializes a message store provider for operation.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="9239e-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="9239e-106">Header file:</span></span>  <br/> |<span data-ttu-id="9239e-107">Маписпи. h</span><span class="sxs-lookup"><span data-stu-id="9239e-107">Mapispi.h</span></span>  <br/> |
|<span data-ttu-id="9239e-108">Реализовано в:</span><span class="sxs-lookup"><span data-stu-id="9239e-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="9239e-109">Поставщики хранилища сообщений</span><span class="sxs-lookup"><span data-stu-id="9239e-109">Message store providers</span></span>  <br/> |
|<span data-ttu-id="9239e-110">Вызывающая сторона:</span><span class="sxs-lookup"><span data-stu-id="9239e-110">Called by:</span></span>  <br/> |<span data-ttu-id="9239e-111">MAPI</span><span class="sxs-lookup"><span data-stu-id="9239e-111">MAPI</span></span>  <br/> |
   
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

## <a name="parameters"></a><span data-ttu-id="9239e-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="9239e-112">Parameters</span></span>

 <span data-ttu-id="9239e-113">_hInstance_</span><span class="sxs-lookup"><span data-stu-id="9239e-113">_hInstance_</span></span>
  
> <span data-ttu-id="9239e-114">возврата Экземпляр библиотеки динамической компоновки (DLL) поставщика хранилища сообщений, которая используется MAPI при связывании.</span><span class="sxs-lookup"><span data-stu-id="9239e-114">[in] The instance of the message store provider's dynamic-link library (DLL) that MAPI used when it linked.</span></span> 
    
 <span data-ttu-id="9239e-115">_Лпмаллок_</span><span class="sxs-lookup"><span data-stu-id="9239e-115">_lpMalloc_</span></span>
  
> <span data-ttu-id="9239e-116">возврата Указатель на объект распределителя памяти, который предоставляет интерфейс для **выделения** OLE.</span><span class="sxs-lookup"><span data-stu-id="9239e-116">[in] Pointer to a memory allocator object exposing the OLE **IMalloc** interface.</span></span> <span data-ttu-id="9239e-117">Поставщику хранилища сообщений может потребоваться использовать этот метод распределения при работе с определенными интерфейсами, такими как **IStream**.</span><span class="sxs-lookup"><span data-stu-id="9239e-117">The message store provider may need to use this allocation method when working with certain interfaces such as **IStream**.</span></span> 
    
 <span data-ttu-id="9239e-118">_Лпаллокатебуффер_</span><span class="sxs-lookup"><span data-stu-id="9239e-118">_lpAllocateBuffer_</span></span>
  
> <span data-ttu-id="9239e-119">возврата Указатель на функцию [мапиаллокатебуффер](mapiallocatebuffer.md) , которая будет использоваться для выделения памяти.</span><span class="sxs-lookup"><span data-stu-id="9239e-119">[in] Pointer to the [MAPIAllocateBuffer](mapiallocatebuffer.md) function, to be used to allocate memory.</span></span> 
    
 <span data-ttu-id="9239e-120">_Лпаллокатеморе_</span><span class="sxs-lookup"><span data-stu-id="9239e-120">_lpAllocateMore_</span></span>
  
> <span data-ttu-id="9239e-121">возврата Указатель на функцию [мапиаллокатеморе](mapiallocatemore.md) , которая будет использоваться для выделения дополнительной памяти.</span><span class="sxs-lookup"><span data-stu-id="9239e-121">[in] Pointer to the [MAPIAllocateMore](mapiallocatemore.md) function, to be used to allocate additional memory.</span></span> 
    
 <span data-ttu-id="9239e-122">_Лпфрибуффер_</span><span class="sxs-lookup"><span data-stu-id="9239e-122">_lpFreeBuffer_</span></span>
  
> <span data-ttu-id="9239e-123">возврата Указатель на функцию [мапифрибуффер](mapifreebuffer.md) , который будет использоваться для освобождения памяти.</span><span class="sxs-lookup"><span data-stu-id="9239e-123">[in] Pointer to the [MAPIFreeBuffer](mapifreebuffer.md) function, to be used to free memory.</span></span> 
    
 <span data-ttu-id="9239e-124">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="9239e-124">_ulFlags_</span></span>
  
> <span data-ttu-id="9239e-125">возврата Битовая маска флагов.</span><span class="sxs-lookup"><span data-stu-id="9239e-125">[in] Bitmask of flags.</span></span> <span data-ttu-id="9239e-126">Можно задать следующий флаг:</span><span class="sxs-lookup"><span data-stu-id="9239e-126">The following flag can be set:</span></span>
    
<span data-ttu-id="9239e-127">МАПИ_НТ_СЕРВИЦЕ</span><span class="sxs-lookup"><span data-stu-id="9239e-127">MAPI_NT_SERVICE</span></span> 
  
> <span data-ttu-id="9239e-128">Поставщик загружается в контексте службы Windows — особого типа процесса без доступа к любому пользовательскому интерфейсу.</span><span class="sxs-lookup"><span data-stu-id="9239e-128">The provider is being loaded in the context of a Windows service, a special type of process without access to any user interface.</span></span> 
    
 <span data-ttu-id="9239e-129">_Улмапивер_</span><span class="sxs-lookup"><span data-stu-id="9239e-129">_ulMAPIVer_</span></span>
  
> <span data-ttu-id="9239e-130">возврата Номер версии интерфейса поставщика услуг (SPI), который использует MAPI.</span><span class="sxs-lookup"><span data-stu-id="9239e-130">[in] Version number of the service provider interface (SPI) that MAPI uses.</span></span> <span data-ttu-id="9239e-131">Текущий номер версии представлен в файле заголовка Маписпи. h.</span><span class="sxs-lookup"><span data-stu-id="9239e-131">For the current version number, see the Mapispi.h header file.</span></span> 
    
 <span data-ttu-id="9239e-132">_Лпулпровидервер_</span><span class="sxs-lookup"><span data-stu-id="9239e-132">_lpulProviderVer_</span></span>
  
> <span data-ttu-id="9239e-133">вышли Указатель на номер версии SPI, который использует этот поставщик хранилища сообщений.</span><span class="sxs-lookup"><span data-stu-id="9239e-133">[out] Pointer to the version number of the SPI that this message store provider uses.</span></span> 
    
 <span data-ttu-id="9239e-134">_Лппмспровидер_</span><span class="sxs-lookup"><span data-stu-id="9239e-134">_lppMSProvider_</span></span>
  
> <span data-ttu-id="9239e-135">вышли Указатель на указатель инициализированного объекта поставщика хранилища сообщений.</span><span class="sxs-lookup"><span data-stu-id="9239e-135">[out] Pointer to a pointer to the initialized message store provider object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="9239e-136">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="9239e-136">Return value</span></span>

<span data-ttu-id="9239e-137">S_OK</span><span class="sxs-lookup"><span data-stu-id="9239e-137">S_OK</span></span> 
  
> <span data-ttu-id="9239e-138">����� ������� � ������ ��������� ��������� ��� ��������.</span><span class="sxs-lookup"><span data-stu-id="9239e-138">The call succeeded and has returned the expected value or values.</span></span> 
    
<span data-ttu-id="9239e-139">МАПИ_Е_ВЕРСИОН</span><span class="sxs-lookup"><span data-stu-id="9239e-139">MAPI_E_VERSION</span></span> 
  
> <span data-ttu-id="9239e-140">Версия SPI, используемая MAPI, несовместима с SPI, используемым этим поставщиком.</span><span class="sxs-lookup"><span data-stu-id="9239e-140">The SPI version being used by MAPI is not compatible with the SPI being used by this provider.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="9239e-141">Комментарии</span><span class="sxs-lookup"><span data-stu-id="9239e-141">Remarks</span></span>

<span data-ttu-id="9239e-142">MAPI вызывает функцию точки входа **мспровидеринит** для инициализации поставщика хранилища сообщений после входа клиента.</span><span class="sxs-lookup"><span data-stu-id="9239e-142">MAPI calls the entry point function **MSProviderInit** to initialize a message store provider following a client logon.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="9239e-143">Примечания для исполнителей</span><span class="sxs-lookup"><span data-stu-id="9239e-143">Notes to implementers</span></span>

<span data-ttu-id="9239e-144">Поставщик хранилища сообщений должен реализовать **мспровидеринит** в качестве функции точки входа в DLL поставщика.</span><span class="sxs-lookup"><span data-stu-id="9239e-144">A message store provider must implement **MSProviderInit** as an entry point function in the provider's DLL.</span></span> <span data-ttu-id="9239e-145">Реализация должна основываться на прототипе функции **мспровидеринит** , также указанном в маписпи. Высоты.</span><span class="sxs-lookup"><span data-stu-id="9239e-145">The implementation must be based on the **MSPROVIDERINIT** function prototype, also specified in MAPISPI.H.</span></span> <span data-ttu-id="9239e-146">MAPI определяет **мспровидеринит** для использования стандартного типа вызова инициализации MAPI, стдмапииниткаллтипе, что заставляет **мспровидеринит** следовать соглашению о вызовах кдекл.</span><span class="sxs-lookup"><span data-stu-id="9239e-146">MAPI defines **MSPROVIDERINIT** to use the standard MAPI initialization call type, STDMAPIINITCALLTYPE, which causes **MSProviderInit** to follow the CDECL calling convention.</span></span> <span data-ttu-id="9239e-147">Преимуществом КДЕКЛ является то, что можно предпринимать попытки вызовов, даже если количество параметров вызовов не равно числу определенных параметров.</span><span class="sxs-lookup"><span data-stu-id="9239e-147">An advantage of CDECL is that calls can be attempted even if the number of calling parameters does not match the number of defined parameters.</span></span> 
  
<span data-ttu-id="9239e-148">Поставщик может быть инициализирован несколько раз в результате того, что в одном и том же профиле появлялось несколько профилей в одновременном использовании или несколько раз.</span><span class="sxs-lookup"><span data-stu-id="9239e-148">A provider can be initialized multiple times, as a result of appearing in several profiles in simultaneous use or of appearing more than once in the same profile.</span></span> <span data-ttu-id="9239e-149">Так как объект provider содержит Context, **мспровидеринит** должен возвратить другой объект поставщика в _лппмспровидер_ для каждой инициализации, даже для нескольких инициализаций в одном процессе.</span><span class="sxs-lookup"><span data-stu-id="9239e-149">Because the provider object contains context, **MSProviderInit** must return a different provider object in  _lppMSProvider_ for each initialization, even for multiple initializations in the same process.</span></span> 
  
<span data-ttu-id="9239e-150">Библиотека DLL поставщика не должна быть связана с Мапикс. dll.</span><span class="sxs-lookup"><span data-stu-id="9239e-150">The provider DLL should not be linked with Mapix.dll.</span></span> <span data-ttu-id="9239e-151">Вместо этого он должен использовать эти указатели для выделения или освобождения памяти.</span><span class="sxs-lookup"><span data-stu-id="9239e-151">Instead, it should use these pointers for memory allocation or deallocation.</span></span> 
  
<span data-ttu-id="9239e-152">Поставщик хранилища сообщений должен использовать функции, на которые указывает _лпаллокатебуффер_, _лпаллокатеморе_и _лпфрибуффер_ для большинства выделений и освобождений памяти.</span><span class="sxs-lookup"><span data-stu-id="9239e-152">The message store provider should use the functions pointed to by  _lpAllocateBuffer_,  _lpAllocateMore_, and  _lpFreeBuffer_ for most memory allocation and deallocation.</span></span> <span data-ttu-id="9239e-153">В частности, поставщик должен использовать эти функции для выделения памяти, которая будет использоваться клиентскими приложениями при вызове интерфейсов объектов, таких как [IMAPIProp::](imapiprop-getprops.md) /PROPS и [IMAPITable:: QueryRows](imapitable-queryrows.md).</span><span class="sxs-lookup"><span data-stu-id="9239e-153">In particular, the provider must use these functions to allocate memory for use by client applications when calling object interfaces such as [IMAPIProp::GetProps](imapiprop-getprops.md) and [IMAPITable::QueryRows](imapitable-queryrows.md).</span></span> <span data-ttu-id="9239e-154">Если поставщик также ожидает использования распределителя памяти OLE, он должен вызывать метод **IUnknown:: AddRef** объекта распределителя, на который указывает параметр _лпмаллок_ .</span><span class="sxs-lookup"><span data-stu-id="9239e-154">If the provider also expects to use the OLE memory allocator, it should call the **IUnknown::AddRef** method of the allocator object pointed to by the  _lpMalloc_ parameter.</span></span> 
  
<span data-ttu-id="9239e-155">Более подробную информацию о создании **мспровидеринит**можно узнать в статье [Загрузка поставщиков хранилища сообщений](loading-message-store-providers.md).</span><span class="sxs-lookup"><span data-stu-id="9239e-155">For more information about writing **MSProviderInit**, see [Loading Message Store Providers](loading-message-store-providers.md).</span></span> <span data-ttu-id="9239e-156">Дополнительные сведения о функциях точки входа можно найти [в статье реализация функции точки входа поставщика услуг](implementing-a-service-provider-entry-point-function.md).</span><span class="sxs-lookup"><span data-stu-id="9239e-156">For more information about entry point functions, see [Implementing a Service Provider Entry Point Function](implementing-a-service-provider-entry-point-function.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="9239e-157">См. также</span><span class="sxs-lookup"><span data-stu-id="9239e-157">See also</span></span>



[<span data-ttu-id="9239e-158">ABProviderInit</span><span class="sxs-lookup"><span data-stu-id="9239e-158">ABProviderInit</span></span>](abproviderinit.md)
  
[<span data-ttu-id="9239e-159">IMSProvider : IUnknown</span><span class="sxs-lookup"><span data-stu-id="9239e-159">IMSProvider : IUnknown</span></span>](imsprovideriunknown.md)
  
[<span data-ttu-id="9239e-160">XPProviderInit</span><span class="sxs-lookup"><span data-stu-id="9239e-160">XPProviderInit</span></span>](xpproviderinit.md)

