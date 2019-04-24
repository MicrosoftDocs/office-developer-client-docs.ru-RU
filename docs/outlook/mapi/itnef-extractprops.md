---
title: Итнефекстрактпропс
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ITnef.ExtractProps
api_type:
- COM
ms.assetid: 9169a5be-21dd-4938-8db3-522bea165c92
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 5a01c65bbec061248537558257c66d1a90128b5e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32348652"
---
# <a name="itnefextractprops"></a><span data-ttu-id="4053e-103">ITnef::ExtractProps</span><span class="sxs-lookup"><span data-stu-id="4053e-103">ITnef::ExtractProps</span></span>

  
  
<span data-ttu-id="4053e-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4053e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4053e-105">Извлекает свойства из инкапсуляции TNEF.</span><span class="sxs-lookup"><span data-stu-id="4053e-105">Extracts the properties from a TNEF encapsulation.</span></span> 
  
```cpp
HRESULT ExtractProps(
  ULONG ulFlags,
  LPSPropTagArray lpPropList,
  LPSTnefProblemArray FAR * lpProblems
);
```

## <a name="parameters"></a><span data-ttu-id="4053e-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="4053e-106">Parameters</span></span>

 <span data-ttu-id="4053e-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="4053e-107">_ulFlags_</span></span>
  
> <span data-ttu-id="4053e-108">возврата Битовая маска флагов, определяющих способ декодирования свойств.</span><span class="sxs-lookup"><span data-stu-id="4053e-108">[in] A bitmask of flags that controls how properties are decoded.</span></span> <span data-ttu-id="4053e-109">Можно задать следующие флаги:</span><span class="sxs-lookup"><span data-stu-id="4053e-109">The following flags can be set:</span></span>
    
<span data-ttu-id="4053e-110">ТНЕФ_ПРОП_ЕКСКЛУДЕ</span><span class="sxs-lookup"><span data-stu-id="4053e-110">TNEF_PROP_EXCLUDE</span></span> 
  
> <span data-ttu-id="4053e-111">Декодирует все свойства, которые не указаны в параметре _лппроплист_ .</span><span class="sxs-lookup"><span data-stu-id="4053e-111">Decodes all properties not specified in the  _lpPropList_ parameter.</span></span> 
    
<span data-ttu-id="4053e-112">ТНЕФ_ПРОП_ИНКЛУДЕ</span><span class="sxs-lookup"><span data-stu-id="4053e-112">TNEF_PROP_INCLUDE</span></span> 
  
> <span data-ttu-id="4053e-113">Декодирует все свойства, указанные в _лппроплист_.</span><span class="sxs-lookup"><span data-stu-id="4053e-113">Decodes all properties specified in  _lpPropList_.</span></span>
    
 <span data-ttu-id="4053e-114">_Лппроплист_</span><span class="sxs-lookup"><span data-stu-id="4053e-114">_lpPropList_</span></span>
  
> <span data-ttu-id="4053e-115">возврата Указатель на список свойств, которые необходимо включить в операцию декодирования или исключить из нее.</span><span class="sxs-lookup"><span data-stu-id="4053e-115">[in] A pointer to the list of properties to include in or exclude from the decoding operation.</span></span>
    
 <span data-ttu-id="4053e-116">_Лппроблемс_</span><span class="sxs-lookup"><span data-stu-id="4053e-116">_lpProblems_</span></span>
  
> <span data-ttu-id="4053e-117">вышли Указатель на указатель на возвращаемую структуру [стнефпроблемаррай](stnefproblemarray.md) .</span><span class="sxs-lookup"><span data-stu-id="4053e-117">[out] A pointer to a pointer to a returned [STnefProblemArray](stnefproblemarray.md) structure.</span></span> <span data-ttu-id="4053e-118">Структура **стнефпроблемаррай** указывает, какие свойства не кодируются должным образом.</span><span class="sxs-lookup"><span data-stu-id="4053e-118">The **STnefProblemArray** structure indicates which properties, if any, were not encoded properly.</span></span> <span data-ttu-id="4053e-119">Если параметр _лппроблемс_ переДАЕТСЯ значение null, массив проблем свойств не возвращается.</span><span class="sxs-lookup"><span data-stu-id="4053e-119">If NULL is passed in the  _lpProblems_ parameter, no property problem array is returned.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="4053e-120">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="4053e-120">Return value</span></span>

<span data-ttu-id="4053e-121">S_OK</span><span class="sxs-lookup"><span data-stu-id="4053e-121">S_OK</span></span> 
  
> <span data-ttu-id="4053e-122">Вызов выполнен успешно и вернул ожидаемое значение или значения.</span><span class="sxs-lookup"><span data-stu-id="4053e-122">The call succeeded and returned the expected value or values.</span></span>
    
<span data-ttu-id="4053e-123">МАПИ_Е_КОРРУПТ_ДАТА</span><span class="sxs-lookup"><span data-stu-id="4053e-123">MAPI_E_CORRUPT_DATA</span></span> 
  
> <span data-ttu-id="4053e-124">Данные, декодированные в поток, повреждены.</span><span class="sxs-lookup"><span data-stu-id="4053e-124">Data being decoded into a stream is corrupted.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="4053e-125">Примечания</span><span class="sxs-lookup"><span data-stu-id="4053e-125">Remarks</span></span>

<span data-ttu-id="4053e-126">Поставщики транспорта, поставщики хранилищ сообщений и шлюзы вызывают метод Итнеф:: Екстрактпропс для извлечения свойств из инкапсуляции сообщения или вложения, переданного в функцию [опентнефстреам](opentnefstream.md) , в методе **::** .</span><span class="sxs-lookup"><span data-stu-id="4053e-126">Transport providers, message store providers, and gateways call the **ITnef::ExtractProps** method to extract (that is, decode) properties from the encapsulation of a message or an attachment that was passed to the [OpenTnefStream](opentnefstream.md) function.</span></span> <span data-ttu-id="4053e-127">Поставщик или шлюз вызова может указать список свойств для декодирования.</span><span class="sxs-lookup"><span data-stu-id="4053e-127">The calling provider or gateway can specify a list of properties to decode.</span></span> <span data-ttu-id="4053e-128">Поставщики и шлюзы также могут использовать **екстрактпропс** для предоставления сведений о специальной обработке вложений.</span><span class="sxs-lookup"><span data-stu-id="4053e-128">Providers and gateways can also use **ExtractProps** to provide information about any special handling for attachments.</span></span> 
  
 <span data-ttu-id="4053e-129">**Екстрактпропс** заполняет исходное сообщение, переданное в **опентнефстреам** , с помощью раскодированных свойств.</span><span class="sxs-lookup"><span data-stu-id="4053e-129">**ExtractProps** populates the original message passed into **OpenTnefStream** with the decoded properties.</span></span> <span data-ttu-id="4053e-130">Последующие вызовы **екстрактпропс** вернитесь к сообщению и извлеките новый список свойств.</span><span class="sxs-lookup"><span data-stu-id="4053e-130">Subsequent **ExtractProps** calls go back to the message and extract the new list of properties.</span></span> 
  
<span data-ttu-id="4053e-131">В отличие от метода [итнеф:: аддпропс](itnef-addprops.md) , который ставит в очередь запрошенные действия до вызова метода **Итнеф:: Finish** , метод **екстрактпропс** декодирует инкапсулированные свойства сразу же после его вызова.</span><span class="sxs-lookup"><span data-stu-id="4053e-131">Unlike the [ITnef::AddProps](itnef-addprops.md) method, which queues requested actions until the **ITnef::Finish** method is called, the **ExtractProps** method decodes the encapsulated properties immediately when it is called.</span></span> <span data-ttu-id="4053e-132">По этой причине конечное сообщение для декодирования инкапсуляции должно быть относительно пустым.</span><span class="sxs-lookup"><span data-stu-id="4053e-132">For that reason, the target message for encapsulation decoding should be relatively empty.</span></span> <span data-ttu-id="4053e-133">Существующие свойства в целевом сообщении перезаписываются инкапсулированными свойствами.</span><span class="sxs-lookup"><span data-stu-id="4053e-133">Existing properties in the target message are overwritten by encapsulated properties.</span></span> 
  
 <span data-ttu-id="4053e-134">**Екстрактпропс** поддерживается только для объектов, открытых с флагом тнеф_декоде для функции **опентнефстреам** или [опентнефстреамекс](opentnefstreamex.md) .</span><span class="sxs-lookup"><span data-stu-id="4053e-134">**ExtractProps** is supported only for objects that are opened with the TNEF_DECODE flag for the **OpenTnefStream** or [OpenTnefStreamEx](opentnefstreamex.md) function.</span></span> 
  
<span data-ttu-id="4053e-135">Реализация TNEF сообщает о неполадках кодирования потока TNEF без остановки процесса **екстрактпропс** .</span><span class="sxs-lookup"><span data-stu-id="4053e-135">The TNEF implementation reports TNEF stream encoding problems without stopping the **ExtractProps** process.</span></span> <span data-ttu-id="4053e-136">Структура [стнефпроблемаррай](stnefproblemarray.md) , возвращаемая в _лппроблемс_ , указывает, какие АТРИБУТЫ TNEF или свойства MAPI, если они есть, не могут быть обработаны.</span><span class="sxs-lookup"><span data-stu-id="4053e-136">The [STnefProblemArray](stnefproblemarray.md) structure returned in  _lpProblems_ indicates which TNEF attributes or MAPI properties, if any, could not be processed.</span></span> <span data-ttu-id="4053e-137">Значение, возвращаемое элементом **SCODE** одной из структур **стнефпроблем** , включенных в **стнефпроблемаррай** , указывает на конкретную проблему.</span><span class="sxs-lookup"><span data-stu-id="4053e-137">The value returned in the **scode** member of the one of the **STnefProblem** structures contained in **STnefProblemArray** indicates the specific problem.</span></span> <span data-ttu-id="4053e-138">Поставщик или шлюз могут работать в предположении, что все свойства или атрибуты, для которых **екстрактпропс** не возвращает отчет о проблеме, были успешно обработаны.</span><span class="sxs-lookup"><span data-stu-id="4053e-138">The provider or gateway can work on the assumption that all properties or attributes for which **ExtractProps** does not return a problem report were processed successfully.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="4053e-139">Если свойство в блоке инкапсуляции MAPI не может быть обработано и оставляет поток ненадежным во время декодирования потока TNEF, декодирование блока инкапсуляции останавливается и сообщает о проблеме.</span><span class="sxs-lookup"><span data-stu-id="4053e-139">If a property in the MAPI encapsulation block cannot be processed and leaves the stream unreliable during the decoding of a TNEF stream, decoding of the encapsulation block is stopped and a problem is reported.</span></span> <span data-ttu-id="4053e-140">Массив проблем для этого типа проблемы содержит 0L для члена **улпроптаг** , `attMAPIProps` или `attAttachment` для члена **улаттрибуте** , и мапи_е_унабле_то_комплете для члена **SCODE** .</span><span class="sxs-lookup"><span data-stu-id="4053e-140">The problem array for this type of problem contains 0L for the **ulPropTag** member,  `attMAPIProps` or  `attAttachment` for the **ulAttribute** member, and MAPI_E_UNABLE_TO_COMPLETE for the **scode** member.</span></span> <span data-ttu-id="4053e-141">Обратите внимание, что декодирование потока не приостанавливается, просто декодированием блока инкапсуляции MAPI.</span><span class="sxs-lookup"><span data-stu-id="4053e-141">Note that the decoding of the stream is not halted, just the decoding of the MAPI encapsulation block.</span></span> <span data-ttu-id="4053e-142">Декодирование потока продолжается с использованием следующего блока атрибута.</span><span class="sxs-lookup"><span data-stu-id="4053e-142">The stream decoding continues with the next attribute block.</span></span> 
  
<span data-ttu-id="4053e-143">Если поставщик или шлюз не работают с неисправной массивом, он может передавать значение NULL в _лпппроблемс_; в этом случае массив проблем не возвращается.</span><span class="sxs-lookup"><span data-stu-id="4053e-143">If a provider or gateway does not work with problem arrays, it can pass NULL in  _lppProblems_; in this case, no problem array is returned.</span></span> 
  
<span data-ttu-id="4053e-144">Значение, возвращаемое в _лппроблемс_ , является допустимым только в том случае, если вызов ВОЗВРАЩАЕТ значение S_OK.</span><span class="sxs-lookup"><span data-stu-id="4053e-144">The value returned in  _lpProblems_ is valid only if the call returns S_OK.</span></span> <span data-ttu-id="4053e-145">Когда возвращается значение S_OK, поставщик или шлюз должны проверить значения, возвращаемые в структуре **стнефпроблемаррай** .</span><span class="sxs-lookup"><span data-stu-id="4053e-145">When S_OK is returned, the provider or gateway should check the values returned in the **STnefProblemArray** structure.</span></span> <span data-ttu-id="4053e-146">Если при вызове возникает ошибка, структура **стнефпроблемаррай** не заполняется, а поставщик или шлюз вызова не должен использовать или освобождать структуру.</span><span class="sxs-lookup"><span data-stu-id="4053e-146">If an error occurs on the call, the **STnefProblemArray** structure is not filled in and the calling provider or gateway should not use or free the structure.</span></span> <span data-ttu-id="4053e-147">Если при вызове не возникнет ошибок, поставщик или шлюз вызова выосвобождают память для структуры **стнефпроблемаррай** , вызвав функцию [мапифрибуффер](mapifreebuffer.md) .</span><span class="sxs-lookup"><span data-stu-id="4053e-147">If no error occurs on the call, the calling provider or gateway must release the memory for the **STnefProblemArray** structure by calling the [MAPIFreeBuffer](mapifreebuffer.md) function.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="4053e-148">См. также</span><span class="sxs-lookup"><span data-stu-id="4053e-148">See also</span></span>



[<span data-ttu-id="4053e-149">ITnef::AddProps</span><span class="sxs-lookup"><span data-stu-id="4053e-149">ITnef::AddProps</span></span>](itnef-addprops.md)
  
[<span data-ttu-id="4053e-150">ITnef::Finish</span><span class="sxs-lookup"><span data-stu-id="4053e-150">ITnef::Finish</span></span>](itnef-finish.md)
  
[<span data-ttu-id="4053e-151">ITnef::SetProps</span><span class="sxs-lookup"><span data-stu-id="4053e-151">ITnef::SetProps</span></span>](itnef-setprops.md)
  
[<span data-ttu-id="4053e-152">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="4053e-152">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="4053e-153">OpenTnefStream</span><span class="sxs-lookup"><span data-stu-id="4053e-153">OpenTnefStream</span></span>](opentnefstream.md)
  
[<span data-ttu-id="4053e-154">OpenTnefStreamEx</span><span class="sxs-lookup"><span data-stu-id="4053e-154">OpenTnefStreamEx</span></span>](opentnefstreamex.md)
  
[<span data-ttu-id="4053e-155">STnefProblemArray</span><span class="sxs-lookup"><span data-stu-id="4053e-155">STnefProblemArray</span></span>](stnefproblemarray.md)
  
[<span data-ttu-id="4053e-156">ITnef : IUnknown</span><span class="sxs-lookup"><span data-stu-id="4053e-156">ITnef : IUnknown</span></span>](itnefiunknown.md)

