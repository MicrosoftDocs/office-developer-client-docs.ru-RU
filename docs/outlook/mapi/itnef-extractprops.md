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
ms.openlocfilehash: 0765e46a6f0545682b16e484d08d296ea13e2136
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22571348"
---
# <a name="itnefextractprops"></a><span data-ttu-id="2fd09-103">ITnef::ExtractProps</span><span class="sxs-lookup"><span data-stu-id="2fd09-103">ITnef::ExtractProps</span></span>

  
  
<span data-ttu-id="2fd09-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2fd09-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="2fd09-105">Извлекает свойства из инкапсуляция TNEF.</span><span class="sxs-lookup"><span data-stu-id="2fd09-105">Extracts the properties from a TNEF encapsulation.</span></span> 
  
```cpp
HRESULT ExtractProps(
  ULONG ulFlags,
  LPSPropTagArray lpPropList,
  LPSTnefProblemArray FAR * lpProblems
);
```

## <a name="parameters"></a><span data-ttu-id="2fd09-106">���������</span><span class="sxs-lookup"><span data-stu-id="2fd09-106">Parameters</span></span>

 <span data-ttu-id="2fd09-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="2fd09-107">_ulFlags_</span></span>
  
> <span data-ttu-id="2fd09-108">[in] Битовая маска флаги, который определяет, как декодировать свойства.</span><span class="sxs-lookup"><span data-stu-id="2fd09-108">[in] A bitmask of flags that controls how properties are decoded.</span></span> <span data-ttu-id="2fd09-109">Можно задать следующие флажки:</span><span class="sxs-lookup"><span data-stu-id="2fd09-109">The following flags can be set:</span></span>
    
<span data-ttu-id="2fd09-110">TNEF_PROP_EXCLUDE</span><span class="sxs-lookup"><span data-stu-id="2fd09-110">TNEF_PROP_EXCLUDE</span></span> 
  
> <span data-ttu-id="2fd09-111">Декодирует все свойства не указан в параметре _lpPropList_ .</span><span class="sxs-lookup"><span data-stu-id="2fd09-111">Decodes all properties not specified in the  _lpPropList_ parameter.</span></span> 
    
<span data-ttu-id="2fd09-112">TNEF_PROP_INCLUDE</span><span class="sxs-lookup"><span data-stu-id="2fd09-112">TNEF_PROP_INCLUDE</span></span> 
  
> <span data-ttu-id="2fd09-113">Декодирует всех свойств, указанных в _lpPropList_.</span><span class="sxs-lookup"><span data-stu-id="2fd09-113">Decodes all properties specified in  _lpPropList_.</span></span>
    
 <span data-ttu-id="2fd09-114">_lpPropList_</span><span class="sxs-lookup"><span data-stu-id="2fd09-114">_lpPropList_</span></span>
  
> <span data-ttu-id="2fd09-115">[in] Указатель на список свойств, включаемых в или исключить из операции декодирования.</span><span class="sxs-lookup"><span data-stu-id="2fd09-115">[in] A pointer to the list of properties to include in or exclude from the decoding operation.</span></span>
    
 <span data-ttu-id="2fd09-116">_lpProblems_</span><span class="sxs-lookup"><span data-stu-id="2fd09-116">_lpProblems_</span></span>
  
> <span data-ttu-id="2fd09-117">[out] Указатель на указатель на структуру возвращенные [STnefProblemArray](stnefproblemarray.md) .</span><span class="sxs-lookup"><span data-stu-id="2fd09-117">[out] A pointer to a pointer to a returned [STnefProblemArray](stnefproblemarray.md) structure.</span></span> <span data-ttu-id="2fd09-118">Структура **STnefProblemArray** указывает, какие свойства при их наличии, были не кодируются должным образом.</span><span class="sxs-lookup"><span data-stu-id="2fd09-118">The **STnefProblemArray** structure indicates which properties, if any, were not encoded properly.</span></span> <span data-ttu-id="2fd09-119">Если NULL передается в параметре _lpProblems_ , возвращается массив проблема не свойство.</span><span class="sxs-lookup"><span data-stu-id="2fd09-119">If NULL is passed in the  _lpProblems_ parameter, no property problem array is returned.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="2fd09-120">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="2fd09-120">Return value</span></span>

<span data-ttu-id="2fd09-121">S_OK</span><span class="sxs-lookup"><span data-stu-id="2fd09-121">S_OK</span></span> 
  
> <span data-ttu-id="2fd09-122">Вызов успешно и возвращается ожидаемым значением или значения.</span><span class="sxs-lookup"><span data-stu-id="2fd09-122">The call succeeded and returned the expected value or values.</span></span>
    
<span data-ttu-id="2fd09-123">MAPI_E_CORRUPT_DATA</span><span class="sxs-lookup"><span data-stu-id="2fd09-123">MAPI_E_CORRUPT_DATA</span></span> 
  
> <span data-ttu-id="2fd09-124">Поврежден декодированных в поток данных.</span><span class="sxs-lookup"><span data-stu-id="2fd09-124">Data being decoded into a stream is corrupted.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="2fd09-125">Примечания</span><span class="sxs-lookup"><span data-stu-id="2fd09-125">Remarks</span></span>

<span data-ttu-id="2fd09-126">Поставщики транспорта, поставщиков хранилища сообщений и шлюзов вызовите метод **ITnef::ExtractProps** для извлечения (, который является, декодирования) свойства из инкапсуляция сообщения или вложения, переданный в функцию [OpenTnefStream](opentnefstream.md) .</span><span class="sxs-lookup"><span data-stu-id="2fd09-126">Transport providers, message store providers, and gateways call the **ITnef::ExtractProps** method to extract (that is, decode) properties from the encapsulation of a message or an attachment that was passed to the [OpenTnefStream](opentnefstream.md) function.</span></span> <span data-ttu-id="2fd09-127">Вызывающий поставщика или шлюз можно указать список свойств для декодирования.</span><span class="sxs-lookup"><span data-stu-id="2fd09-127">The calling provider or gateway can specify a list of properties to decode.</span></span> <span data-ttu-id="2fd09-128">Поставщики и шлюзов можно также использовать **ExtractProps** для предоставления сведений о любой специальная обработка вложений.</span><span class="sxs-lookup"><span data-stu-id="2fd09-128">Providers and gateways can also use **ExtractProps** to provide information about any special handling for attachments.</span></span> 
  
 <span data-ttu-id="2fd09-129">**ExtractProps** заполняет был передан в **OpenTnefStream** со свойствами декодированное исходного сообщения.</span><span class="sxs-lookup"><span data-stu-id="2fd09-129">**ExtractProps** populates the original message passed into **OpenTnefStream** with the decoded properties.</span></span> <span data-ttu-id="2fd09-130">Последующие вызовы **ExtractProps** вернуться к сообщению и извлеките новый список свойств.</span><span class="sxs-lookup"><span data-stu-id="2fd09-130">Subsequent **ExtractProps** calls go back to the message and extract the new list of properties.</span></span> 
  
<span data-ttu-id="2fd09-131">В отличие от метода [ITnef::AddProps](itnef-addprops.md) очередей запрошенного действия, пока не будет вызван метод **ITnef::Finish** , метод **ExtractProps** декодирует инкапсулированное свойства сразу же после вызова.</span><span class="sxs-lookup"><span data-stu-id="2fd09-131">Unlike the [ITnef::AddProps](itnef-addprops.md) method, which queues requested actions until the **ITnef::Finish** method is called, the **ExtractProps** method decodes the encapsulated properties immediately when it is called.</span></span> <span data-ttu-id="2fd09-132">По этой причине сообщение целевой для декодирования инкапсуляция должно быть относительно пустой.</span><span class="sxs-lookup"><span data-stu-id="2fd09-132">For that reason, the target message for encapsulation decoding should be relatively empty.</span></span> <span data-ttu-id="2fd09-133">Существующие свойства в сообщении конечного перезаписываются инкапсулированное свойства.</span><span class="sxs-lookup"><span data-stu-id="2fd09-133">Existing properties in the target message are overwritten by encapsulated properties.</span></span> 
  
 <span data-ttu-id="2fd09-134">**ExtractProps** поддерживается только для объектов, которые открываются с флагом TNEF_DECODE для функции **OpenTnefStream** или [OpenTnefStreamEx](opentnefstreamex.md) .</span><span class="sxs-lookup"><span data-stu-id="2fd09-134">**ExtractProps** is supported only for objects that are opened with the TNEF_DECODE flag for the **OpenTnefStream** or [OpenTnefStreamEx](opentnefstreamex.md) function.</span></span> 
  
<span data-ttu-id="2fd09-135">Реализация TNEF отчетов проблем кодировки TNEF потока без остановки процесса **ExtractProps** .</span><span class="sxs-lookup"><span data-stu-id="2fd09-135">The TNEF implementation reports TNEF stream encoding problems without stopping the **ExtractProps** process.</span></span> <span data-ttu-id="2fd09-136">Структура [STnefProblemArray](stnefproblemarray.md) , возвращаемых в _lpProblems_ указывает, какие атрибуты TNEF или свойства MAPI, если не удается обработать.</span><span class="sxs-lookup"><span data-stu-id="2fd09-136">The [STnefProblemArray](stnefproblemarray.md) structure returned in  _lpProblems_ indicates which TNEF attributes or MAPI properties, if any, could not be processed.</span></span> <span data-ttu-id="2fd09-137">Значение, возвращаемое в **scode** членом одного из структур **STnefProblem** , содержащихся в **STnefProblemArray** Указывает конкретную проблему.</span><span class="sxs-lookup"><span data-stu-id="2fd09-137">The value returned in the **scode** member of the one of the **STnefProblem** structures contained in **STnefProblemArray** indicates the specific problem.</span></span> <span data-ttu-id="2fd09-138">Поставщик или шлюз может работать предполагается, что все свойства или атрибуты, для которых **ExtractProps** не возвращает отчет о проблеме обработаны успешно.</span><span class="sxs-lookup"><span data-stu-id="2fd09-138">The provider or gateway can work on the assumption that all properties or attributes for which **ExtractProps** does not return a problem report were processed successfully.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="2fd09-139">Если свойство в блоке инкапсуляция MAPI не может обработать и оставляет потока ненадежный во время декодирования TNEF потока, декодирование инкапсуляция блокировки остановлена, обнаруженных проблем.</span><span class="sxs-lookup"><span data-stu-id="2fd09-139">If a property in the MAPI encapsulation block cannot be processed and leaves the stream unreliable during the decoding of a TNEF stream, decoding of the encapsulation block is stopped and a problem is reported.</span></span> <span data-ttu-id="2fd09-140">Массив проблемы для проблемы такого типа содержит 0L для элемента **ulPropTag** `attMAPIProps` или `attAttachment` для члена **ulAttribute** и MAPI_E_UNABLE_TO_COMPLETE для элемента **scode** .</span><span class="sxs-lookup"><span data-stu-id="2fd09-140">The problem array for this type of problem contains 0L for the **ulPropTag** member,  `attMAPIProps` or  `attAttachment` for the **ulAttribute** member, and MAPI_E_UNABLE_TO_COMPLETE for the **scode** member.</span></span> <span data-ttu-id="2fd09-141">Обратите внимание, что декодирование в потоке не прервать этот процесс и декодирования блокировки инкапсуляция MAPI.</span><span class="sxs-lookup"><span data-stu-id="2fd09-141">Note that the decoding of the stream is not halted, just the decoding of the MAPI encapsulation block.</span></span> <span data-ttu-id="2fd09-142">Декодирование потока продолжается в следующем блоке атрибута.</span><span class="sxs-lookup"><span data-stu-id="2fd09-142">The stream decoding continues with the next attribute block.</span></span> 
  
<span data-ttu-id="2fd09-143">Если поставщик или шлюз не работает с массивами проблемы, его можно передать значение NULL в _lppProblems_; в этом случае возвращается массив не проблемы.</span><span class="sxs-lookup"><span data-stu-id="2fd09-143">If a provider or gateway does not work with problem arrays, it can pass NULL in  _lppProblems_; in this case, no problem array is returned.</span></span> 
  
<span data-ttu-id="2fd09-144">Значение, возвращаемое в _lpProblems_ действителен только в том случае, если вызов возвращает значение S_OK.</span><span class="sxs-lookup"><span data-stu-id="2fd09-144">The value returned in  _lpProblems_ is valid only if the call returns S_OK.</span></span> <span data-ttu-id="2fd09-145">Если возвращается значение S_OK, поставщик или шлюз должен проверить, значения, возвращаемые в структуре **STnefProblemArray** .</span><span class="sxs-lookup"><span data-stu-id="2fd09-145">When S_OK is returned, the provider or gateway should check the values returned in the **STnefProblemArray** structure.</span></span> <span data-ttu-id="2fd09-146">При возникновении ошибки на звонок, структура **STnefProblemArray** не заполнено и вызова поставщика или шлюз не использовать или Бесплатная загрузка структуры.</span><span class="sxs-lookup"><span data-stu-id="2fd09-146">If an error occurs on the call, the **STnefProblemArray** structure is not filled in and the calling provider or gateway should not use or free the structure.</span></span> <span data-ttu-id="2fd09-147">Если ошибки не обнаружены на звонок, вызывающей поставщика или шлюз необходимо освободить память для структуры **STnefProblemArray** путем вызова функции [MAPIFreeBuffer](mapifreebuffer.md) .</span><span class="sxs-lookup"><span data-stu-id="2fd09-147">If no error occurs on the call, the calling provider or gateway must release the memory for the **STnefProblemArray** structure by calling the [MAPIFreeBuffer](mapifreebuffer.md) function.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="2fd09-148">См. также</span><span class="sxs-lookup"><span data-stu-id="2fd09-148">See also</span></span>



[<span data-ttu-id="2fd09-149">ITnef::AddProps</span><span class="sxs-lookup"><span data-stu-id="2fd09-149">ITnef::AddProps</span></span>](itnef-addprops.md)
  
[<span data-ttu-id="2fd09-150">ITnef::Finish</span><span class="sxs-lookup"><span data-stu-id="2fd09-150">ITnef::Finish</span></span>](itnef-finish.md)
  
[<span data-ttu-id="2fd09-151">ITnef::SetProps</span><span class="sxs-lookup"><span data-stu-id="2fd09-151">ITnef::SetProps</span></span>](itnef-setprops.md)
  
[<span data-ttu-id="2fd09-152">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="2fd09-152">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="2fd09-153">OpenTnefStream</span><span class="sxs-lookup"><span data-stu-id="2fd09-153">OpenTnefStream</span></span>](opentnefstream.md)
  
[<span data-ttu-id="2fd09-154">OpenTnefStreamEx</span><span class="sxs-lookup"><span data-stu-id="2fd09-154">OpenTnefStreamEx</span></span>](opentnefstreamex.md)
  
[<span data-ttu-id="2fd09-155">STnefProblemArray</span><span class="sxs-lookup"><span data-stu-id="2fd09-155">STnefProblemArray</span></span>](stnefproblemarray.md)
  
[<span data-ttu-id="2fd09-156">ITnef : IUnknown</span><span class="sxs-lookup"><span data-stu-id="2fd09-156">ITnef : IUnknown</span></span>](itnefiunknown.md)

