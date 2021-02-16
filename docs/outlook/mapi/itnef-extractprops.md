---
title: ITnefExtractProps
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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407503"
---
# <a name="itnefextractprops"></a><span data-ttu-id="5676e-103">ITnef::ExtractProps</span><span class="sxs-lookup"><span data-stu-id="5676e-103">ITnef::ExtractProps</span></span>

  
  
<span data-ttu-id="5676e-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5676e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5676e-105">Извлекает свойства из инкапсуляции TNEF.</span><span class="sxs-lookup"><span data-stu-id="5676e-105">Extracts the properties from a TNEF encapsulation.</span></span> 
  
```cpp
HRESULT ExtractProps(
  ULONG ulFlags,
  LPSPropTagArray lpPropList,
  LPSTnefProblemArray FAR * lpProblems
);
```

## <a name="parameters"></a><span data-ttu-id="5676e-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="5676e-106">Parameters</span></span>

 <span data-ttu-id="5676e-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="5676e-107">_ulFlags_</span></span>
  
> <span data-ttu-id="5676e-108">[in] Битоваяmas флагов, которая управляет декодирования свойств.</span><span class="sxs-lookup"><span data-stu-id="5676e-108">[in] A bitmask of flags that controls how properties are decoded.</span></span> <span data-ttu-id="5676e-109">Можно установить следующие флаги:</span><span class="sxs-lookup"><span data-stu-id="5676e-109">The following flags can be set:</span></span>
    
<span data-ttu-id="5676e-110">TNEF_PROP_EXCLUDE</span><span class="sxs-lookup"><span data-stu-id="5676e-110">TNEF_PROP_EXCLUDE</span></span> 
  
> <span data-ttu-id="5676e-111">Декодирует все свойства, не указанные в параметре _lpPropList._</span><span class="sxs-lookup"><span data-stu-id="5676e-111">Decodes all properties not specified in the  _lpPropList_ parameter.</span></span> 
    
<span data-ttu-id="5676e-112">TNEF_PROP_INCLUDE</span><span class="sxs-lookup"><span data-stu-id="5676e-112">TNEF_PROP_INCLUDE</span></span> 
  
> <span data-ttu-id="5676e-113">Декодирует все свойства, указанные в _lpPropList._</span><span class="sxs-lookup"><span data-stu-id="5676e-113">Decodes all properties specified in  _lpPropList_.</span></span>
    
 <span data-ttu-id="5676e-114">_lpPropList_</span><span class="sxs-lookup"><span data-stu-id="5676e-114">_lpPropList_</span></span>
  
> <span data-ttu-id="5676e-115">[in] Указатель на список свойств, которые необходимо включить в операцию декодирования или исключить из нее.</span><span class="sxs-lookup"><span data-stu-id="5676e-115">[in] A pointer to the list of properties to include in or exclude from the decoding operation.</span></span>
    
 <span data-ttu-id="5676e-116">_lpProblems_</span><span class="sxs-lookup"><span data-stu-id="5676e-116">_lpProblems_</span></span>
  
> <span data-ttu-id="5676e-117">[out] Указатель на указатель на возвращенную [структуру STnefProblemArray.](stnefproblemarray.md)</span><span class="sxs-lookup"><span data-stu-id="5676e-117">[out] A pointer to a pointer to a returned [STnefProblemArray](stnefproblemarray.md) structure.</span></span> <span data-ttu-id="5676e-118">Структура **STnefProblemArray** указывает, какие свойства ,если таковые имеются, не были закодированы должным образом.</span><span class="sxs-lookup"><span data-stu-id="5676e-118">The **STnefProblemArray** structure indicates which properties, if any, were not encoded properly.</span></span> <span data-ttu-id="5676e-119">Если в параметре  _lpProblems_ передается NULL, массив проблем свойств не возвращается.</span><span class="sxs-lookup"><span data-stu-id="5676e-119">If NULL is passed in the  _lpProblems_ parameter, no property problem array is returned.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="5676e-120">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="5676e-120">Return value</span></span>

<span data-ttu-id="5676e-121">S_OK</span><span class="sxs-lookup"><span data-stu-id="5676e-121">S_OK</span></span> 
  
> <span data-ttu-id="5676e-122">Вызов был успешным и возвратил ожидаемое значение или значения.</span><span class="sxs-lookup"><span data-stu-id="5676e-122">The call succeeded and returned the expected value or values.</span></span>
    
<span data-ttu-id="5676e-123">MAPI_E_CORRUPT_DATA</span><span class="sxs-lookup"><span data-stu-id="5676e-123">MAPI_E_CORRUPT_DATA</span></span> 
  
> <span data-ttu-id="5676e-124">Данные, декодироваться в потоке, повреждены.</span><span class="sxs-lookup"><span data-stu-id="5676e-124">Data being decoded into a stream is corrupted.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="5676e-125">Примечания</span><span class="sxs-lookup"><span data-stu-id="5676e-125">Remarks</span></span>

<span data-ttu-id="5676e-126">Поставщики транспорта, поставщики store сообщений и шлюзы вызывают метод **ITnef::ExtractProps** для извлечения (т. е. декодирования) свойств из инкапсуляции сообщения или вложения, переданного функции [OpenTnefStream.](opentnefstream.md)</span><span class="sxs-lookup"><span data-stu-id="5676e-126">Transport providers, message store providers, and gateways call the **ITnef::ExtractProps** method to extract (that is, decode) properties from the encapsulation of a message or an attachment that was passed to the [OpenTnefStream](opentnefstream.md) function.</span></span> <span data-ttu-id="5676e-127">Поставщик или шлюз звонков может указать список свойств для декодирования.</span><span class="sxs-lookup"><span data-stu-id="5676e-127">The calling provider or gateway can specify a list of properties to decode.</span></span> <span data-ttu-id="5676e-128">Поставщики и шлюзы также могут использовать **ExtractProps** для предоставления сведений о любой специальной обработке вложений.</span><span class="sxs-lookup"><span data-stu-id="5676e-128">Providers and gateways can also use **ExtractProps** to provide information about any special handling for attachments.</span></span> 
  
 <span data-ttu-id="5676e-129">**ExtractProps** заполняет исходное сообщение, переданное **в OpenTnefStream,** расшифровки свойств.</span><span class="sxs-lookup"><span data-stu-id="5676e-129">**ExtractProps** populates the original message passed into **OpenTnefStream** with the decoded properties.</span></span> <span data-ttu-id="5676e-130">Последующие **вызовы ExtractProps** будут возвращаться к сообщению и извлекать новый список свойств.</span><span class="sxs-lookup"><span data-stu-id="5676e-130">Subsequent **ExtractProps** calls go back to the message and extract the new list of properties.</span></span> 
  
<span data-ttu-id="5676e-131">В отличие от метода [ITnef::AddProps,](itnef-addprops.md) который добавляет в очередь запрашиваемую информацию о действиях до тех пор, пока не будет вызван метод **ITnef::Finish,** метод **ExtractProps** декодирует инкапсулированные свойства сразу же при его вызвании.</span><span class="sxs-lookup"><span data-stu-id="5676e-131">Unlike the [ITnef::AddProps](itnef-addprops.md) method, which queues requested actions until the **ITnef::Finish** method is called, the **ExtractProps** method decodes the encapsulated properties immediately when it is called.</span></span> <span data-ttu-id="5676e-132">По этой причине целевое сообщение для инкапсуляции должно быть относительно пустым.</span><span class="sxs-lookup"><span data-stu-id="5676e-132">For that reason, the target message for encapsulation decoding should be relatively empty.</span></span> <span data-ttu-id="5676e-133">Существующие свойства в целевом сообщении перезаписываются инкапсулированных свойствами.</span><span class="sxs-lookup"><span data-stu-id="5676e-133">Existing properties in the target message are overwritten by encapsulated properties.</span></span> 
  
 <span data-ttu-id="5676e-134">**ExtractProps** поддерживается только для объектов, которые открываются с TNEF_DECODE флагом для **функции OpenTnefStream** или [OpenTnefStreamEx.](opentnefstreamex.md)</span><span class="sxs-lookup"><span data-stu-id="5676e-134">**ExtractProps** is supported only for objects that are opened with the TNEF_DECODE flag for the **OpenTnefStream** or [OpenTnefStreamEx](opentnefstreamex.md) function.</span></span> 
  
<span data-ttu-id="5676e-135">Реализация TNEF сообщает о проблемах кодиации потока TNEF без остановки процесса **ExtractProps.**</span><span class="sxs-lookup"><span data-stu-id="5676e-135">The TNEF implementation reports TNEF stream encoding problems without stopping the **ExtractProps** process.</span></span> <span data-ttu-id="5676e-136">Структура [STnefProblemArray,](stnefproblemarray.md) возвращаемая  _в lpProblems,_ указывает, какие атрибуты TNEF или свойства MAPI (если таковые имеются) не удалось обработать.</span><span class="sxs-lookup"><span data-stu-id="5676e-136">The [STnefProblemArray](stnefproblemarray.md) structure returned in  _lpProblems_ indicates which TNEF attributes or MAPI properties, if any, could not be processed.</span></span> <span data-ttu-id="5676e-137">Значение, возвращаемого в члене **scode** одной из структур **STnefProblem,** содержащихся в **STnefProblemArray,** указывает на конкретную проблему.</span><span class="sxs-lookup"><span data-stu-id="5676e-137">The value returned in the **scode** member of the one of the **STnefProblem** structures contained in **STnefProblemArray** indicates the specific problem.</span></span> <span data-ttu-id="5676e-138">Поставщик или шлюз может работать при предположении, что все свойства или атрибуты, для которых **ExtractProps** не возвращает отчет о проблеме, были успешно обработаны.</span><span class="sxs-lookup"><span data-stu-id="5676e-138">The provider or gateway can work on the assumption that all properties or attributes for which **ExtractProps** does not return a problem report were processed successfully.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="5676e-139">Если свойство в блоке инкапсуляции MAPI не может быть обработано и поток остается ненадежным во время декодирования потока TNEF, декодирования блока инкапсуляции останавливается и сообщается о проблеме.</span><span class="sxs-lookup"><span data-stu-id="5676e-139">If a property in the MAPI encapsulation block cannot be processed and leaves the stream unreliable during the decoding of a TNEF stream, decoding of the encapsulation block is stopped and a problem is reported.</span></span> <span data-ttu-id="5676e-140">Массив проблем для этого типа проблемы содержит 0L для члена **ulPropTag** или для члена `attMAPIProps` `attAttachment` **ulAttribute** и MAPI_E_UNABLE_TO_COMPLETE для члена **scode.**</span><span class="sxs-lookup"><span data-stu-id="5676e-140">The problem array for this type of problem contains 0L for the **ulPropTag** member,  `attMAPIProps` or  `attAttachment` for the **ulAttribute** member, and MAPI_E_UNABLE_TO_COMPLETE for the **scode** member.</span></span> <span data-ttu-id="5676e-141">Обратите внимание, что декодирования потока не остановить, просто декодирования блока инкапсуляции MAPI.</span><span class="sxs-lookup"><span data-stu-id="5676e-141">Note that the decoding of the stream is not halted, just the decoding of the MAPI encapsulation block.</span></span> <span data-ttu-id="5676e-142">Декодирования потока продолжается с помощью следующего блока атрибутов.</span><span class="sxs-lookup"><span data-stu-id="5676e-142">The stream decoding continues with the next attribute block.</span></span> 
  
<span data-ttu-id="5676e-143">Если поставщик или шлюз не работает с массивами проблем, он может передавать NULL в  _lppProblems;_ в этом случае массив проблем не возвращается.</span><span class="sxs-lookup"><span data-stu-id="5676e-143">If a provider or gateway does not work with problem arrays, it can pass NULL in  _lppProblems_; in this case, no problem array is returned.</span></span> 
  
<span data-ttu-id="5676e-144">Значение, возвращаемая  _в lpProblems,_ допустимо, только если вызов возвращает S_OK.</span><span class="sxs-lookup"><span data-stu-id="5676e-144">The value returned in  _lpProblems_ is valid only if the call returns S_OK.</span></span> <span data-ttu-id="5676e-145">Когда S_OK возвращается, поставщик или шлюз должен проверить значения, возвращенные в **структуре STnefProblemArray.**</span><span class="sxs-lookup"><span data-stu-id="5676e-145">When S_OK is returned, the provider or gateway should check the values returned in the **STnefProblemArray** structure.</span></span> <span data-ttu-id="5676e-146">Если при вызове возникает ошибка, структура **STnefProblemArray** не заполняется, и поставщик или шлюз вызовов не должны использовать или освободить структуру.</span><span class="sxs-lookup"><span data-stu-id="5676e-146">If an error occurs on the call, the **STnefProblemArray** structure is not filled in and the calling provider or gateway should not use or free the structure.</span></span> <span data-ttu-id="5676e-147">Если ошибка при вызове не возникает, поставщик или шлюз вызовов должен освободить память для структуры **STnefProblemArray,** вызывая функцию [MAPIFreeBuffer.](mapifreebuffer.md)</span><span class="sxs-lookup"><span data-stu-id="5676e-147">If no error occurs on the call, the calling provider or gateway must release the memory for the **STnefProblemArray** structure by calling the [MAPIFreeBuffer](mapifreebuffer.md) function.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="5676e-148">См. также</span><span class="sxs-lookup"><span data-stu-id="5676e-148">See also</span></span>



[<span data-ttu-id="5676e-149">ITnef::AddProps</span><span class="sxs-lookup"><span data-stu-id="5676e-149">ITnef::AddProps</span></span>](itnef-addprops.md)
  
[<span data-ttu-id="5676e-150">ITnef::Finish</span><span class="sxs-lookup"><span data-stu-id="5676e-150">ITnef::Finish</span></span>](itnef-finish.md)
  
[<span data-ttu-id="5676e-151">ITnef::SetProps</span><span class="sxs-lookup"><span data-stu-id="5676e-151">ITnef::SetProps</span></span>](itnef-setprops.md)
  
[<span data-ttu-id="5676e-152">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="5676e-152">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="5676e-153">OpenTnefStream</span><span class="sxs-lookup"><span data-stu-id="5676e-153">OpenTnefStream</span></span>](opentnefstream.md)
  
[<span data-ttu-id="5676e-154">OpenTnefStreamEx</span><span class="sxs-lookup"><span data-stu-id="5676e-154">OpenTnefStreamEx</span></span>](opentnefstreamex.md)
  
[<span data-ttu-id="5676e-155">STnefProblemArray</span><span class="sxs-lookup"><span data-stu-id="5676e-155">STnefProblemArray</span></span>](stnefproblemarray.md)
  
[<span data-ttu-id="5676e-156">ITnef : IUnknown</span><span class="sxs-lookup"><span data-stu-id="5676e-156">ITnef : IUnknown</span></span>](itnefiunknown.md)

