---
title: ITnefFinishComponent
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ITnef.FinishComponent
api_type:
- COM
ms.assetid: bcdd0688-0897-47d7-9601-f592ba453b39
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 0242015680f11e5be6ae8ea9987e5778dc7cdf05
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22594364"
---
# <a name="itneffinishcomponent"></a><span data-ttu-id="1f34d-103">ITnef::FinishComponent</span><span class="sxs-lookup"><span data-stu-id="1f34d-103">ITnef::FinishComponent</span></span>

  
  
<span data-ttu-id="1f34d-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1f34d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1f34d-105">Обрабатывает отдельные компоненты из сообщения одно за раз в поток Transport-Neutral Encapsulation формата TNEF ().</span><span class="sxs-lookup"><span data-stu-id="1f34d-105">Processes individual components from a message one at a time into a Transport-Neutral Encapsulation Format (TNEF) stream.</span></span>
  
```cpp
HRESULT FinishComponent(
  ULONG ulFlags,
  ULONG ulComponentID,
  LPSPropTagArray lpCustomPropList,
  LPSPropValue lpCustomProps,
  LPSPropTagArray lpPropList,
  LPSTnefProblemArray FAR * lppProblems
);
```

## <a name="parameters"></a><span data-ttu-id="1f34d-106">���������</span><span class="sxs-lookup"><span data-stu-id="1f34d-106">Parameters</span></span>

 <span data-ttu-id="1f34d-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="1f34d-107">_ulFlags_</span></span>
  
> <span data-ttu-id="1f34d-108">[in] Битовая маска флаги, который определяет, какой компонент будет завершено.</span><span class="sxs-lookup"><span data-stu-id="1f34d-108">[in] A bitmask of flags that controls which component will be finished.</span></span> <span data-ttu-id="1f34d-109">Необходимо задать одно или другое следующих флагов:</span><span class="sxs-lookup"><span data-stu-id="1f34d-109">One or the other of the following flags must be set:</span></span>
    
<span data-ttu-id="1f34d-110">TNEF_COMPONENT_ATTACHMENT</span><span class="sxs-lookup"><span data-stu-id="1f34d-110">TNEF_COMPONENT_ATTACHMENT</span></span> 
  
> <span data-ttu-id="1f34d-111">Обработка будет завершено для объекта вложений; параметр _ulComponentID_ содержит свойство **PR_ATTACH_NUM** ([PidTagAttachNumber](pidtagattachnumber-canonical-property.md)) вложения.</span><span class="sxs-lookup"><span data-stu-id="1f34d-111">Processing will be finished for an attachment object; the  _ulComponentID_ parameter contains the **PR_ATTACH_NUM** ([PidTagAttachNumber](pidtagattachnumber-canonical-property.md)) property of the attachment.</span></span> 
    
<span data-ttu-id="1f34d-112">TNEF_COMPONENT_MESSAGE</span><span class="sxs-lookup"><span data-stu-id="1f34d-112">TNEF_COMPONENT_MESSAGE</span></span> 
  
> <span data-ttu-id="1f34d-113">Обработка будет завершено для объекта message.</span><span class="sxs-lookup"><span data-stu-id="1f34d-113">Processing will be finished for a message object.</span></span> 
    
 <span data-ttu-id="1f34d-114">_ulComponentID_</span><span class="sxs-lookup"><span data-stu-id="1f34d-114">_ulComponentID_</span></span>
  
> <span data-ttu-id="1f34d-115">[in] 0 для указания обработки для сообщения или свойство **PR_ATTACH_NUM** вложения для обработки.</span><span class="sxs-lookup"><span data-stu-id="1f34d-115">[in] 0 to indicate processing for a message, or the **PR_ATTACH_NUM** property of an attachment to be processed.</span></span> <span data-ttu-id="1f34d-116">Если в параметре _ulFlags_ флаг TNEF_COMPONENT_MESSAGE, _ulComponentID_ должен иметь значение 0.</span><span class="sxs-lookup"><span data-stu-id="1f34d-116">If the TNEF_COMPONENT_MESSAGE flag is set in the  _ulFlags_ parameter,  _ulComponentID_ must be 0.</span></span> 
    
 <span data-ttu-id="1f34d-117">_lpCustomPropList_</span><span class="sxs-lookup"><span data-stu-id="1f34d-117">_lpCustomPropList_</span></span>
  
> <span data-ttu-id="1f34d-118">[in] Указатель на структуру [SPropTagArray](sproptagarray.md) , содержащий тегов свойств, чтобы указать свойства, переданной в параметре _lpCustomProps_ .</span><span class="sxs-lookup"><span data-stu-id="1f34d-118">[in] A pointer to an [SPropTagArray](sproptagarray.md) structure that contains property tags that identify the properties passed in the  _lpCustomProps_ parameter.</span></span> <span data-ttu-id="1f34d-119">Должен быть однозначного соответствия между каждое значение свойства в _lpCustomProps_ и тег свойства с помощью параметра _lpCustomPropList_ .</span><span class="sxs-lookup"><span data-stu-id="1f34d-119">There must be a one-to-one correspondence between each property value in  _lpCustomProps_ and a property tag in the  _lpCustomPropList_ parameter.</span></span> 
    
 <span data-ttu-id="1f34d-120">_lpCustomProps_</span><span class="sxs-lookup"><span data-stu-id="1f34d-120">_lpCustomProps_</span></span>
  
> <span data-ttu-id="1f34d-121">[in] Указатель на структуру [SPropValue](spropvalue.md) , который содержит значения для свойств для кодирования.</span><span class="sxs-lookup"><span data-stu-id="1f34d-121">[in] A pointer to an [SPropValue](spropvalue.md) structure that contains property values for the properties to encode.</span></span> 
    
 <span data-ttu-id="1f34d-122">_lpPropList_</span><span class="sxs-lookup"><span data-stu-id="1f34d-122">_lpPropList_</span></span>
  
> <span data-ttu-id="1f34d-123">[in] Указатель на структуру **SPropTagArray** , содержащий теги свойства для свойства, которые нужно кодировать.</span><span class="sxs-lookup"><span data-stu-id="1f34d-123">[in] A pointer to an **SPropTagArray** structure that contains property tags for the properties to encode.</span></span> 
    
 <span data-ttu-id="1f34d-124">_lppProblems_</span><span class="sxs-lookup"><span data-stu-id="1f34d-124">_lppProblems_</span></span>
  
> <span data-ttu-id="1f34d-125">[out] Указатель на указатель на структуру возвращенные [STnefProblemArray](stnefproblemarray.md) .</span><span class="sxs-lookup"><span data-stu-id="1f34d-125">[out] A pointer to a pointer to a returned [STnefProblemArray](stnefproblemarray.md) structure.</span></span> <span data-ttu-id="1f34d-126">Структура **STnefProblemArray** указывает, какие свойства при их наличии, были не кодируются должным образом.</span><span class="sxs-lookup"><span data-stu-id="1f34d-126">The **STnefProblemArray** structure indicates which properties, if any, were not encoded properly.</span></span> <span data-ttu-id="1f34d-127">Если NULL передается в параметре _lppProblems_ , возвращается массив проблема не свойство.</span><span class="sxs-lookup"><span data-stu-id="1f34d-127">If NULL is passed in the  _lppProblems_ parameter, no property problem array is returned.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="1f34d-128">������������ ��������</span><span class="sxs-lookup"><span data-stu-id="1f34d-128">Return value</span></span>

<span data-ttu-id="1f34d-129">ЗНАЧЕНИЕ S_OK</span><span class="sxs-lookup"><span data-stu-id="1f34d-129">S_OK</span></span> 
  
> <span data-ttu-id="1f34d-130">����� ������� � ������ ��������� ��������� ��� ��������.</span><span class="sxs-lookup"><span data-stu-id="1f34d-130">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="1f34d-131">���������</span><span class="sxs-lookup"><span data-stu-id="1f34d-131">Remarks</span></span>

<span data-ttu-id="1f34d-132">Для передачи поставщиков, поставщиков хранилища сообщений и шлюзов вызова метода **ITnef::FinishComponent** для выполнения TNEF обработки для одного компонента, сообщения или вложения, как указано в параметре _ulFlags_ флаг.</span><span class="sxs-lookup"><span data-stu-id="1f34d-132">Transport providers, message store providers, and gateways call the **ITnef::FinishComponent** method to perform TNEF processing for one component, either a message or an attachment, as indicated by the flag set in the  _ulFlags_ parameter.</span></span> 
  
<span data-ttu-id="1f34d-133">Для обработки компонент необходимо включить, вызывающий поставщика или шлюз передайте флаг TNEF_COMPONENT_ENCODING _ulFlags_ [OpenTnefStream](opentnefstream.md) или [OpenTnefStreamEx](opentnefstreamex.md) функции, которая открыта объект для получения кодировки.</span><span class="sxs-lookup"><span data-stu-id="1f34d-133">For component processing to be enabled, the calling provider or gateway pass the TNEF_COMPONENT_ENCODING flag in  _ulFlags_ for the [OpenTnefStream](opentnefstream.md) or [OpenTnefStreamEx](opentnefstreamex.md) function that opened the object to receive encoding.</span></span> 
  
<span data-ttu-id="1f34d-134">Передача значений в параметры _lpCustomPropList_ и _lpCustomProps_ выполняет компонент кодирования параметру, который выполняется с помощью метода [ITnef::SetProps](itnef-setprops.md) .</span><span class="sxs-lookup"><span data-stu-id="1f34d-134">Passing values in the  _lpCustomPropList_ and  _lpCustomProps_ parameters performs component encoding equivalent to that done by the [ITnef::SetProps](itnef-setprops.md) method.</span></span> <span data-ttu-id="1f34d-135">Передача значения с помощью параметра _lpPropList_ выполняет компонент кодировки эквивалент, который выполняется с помощью метода [ITnef::AddProps](itnef-addprops.md) с флагом TNEF_PROP_INCLUDE в _ulFlags_.</span><span class="sxs-lookup"><span data-stu-id="1f34d-135">Passing a value in the  _lpPropList_ parameter performs component encoding equivalent to that done by the [ITnef::AddProps](itnef-addprops.md) method with the TNEF_PROP_INCLUDE flag set in  _ulFlags_.</span></span> <span data-ttu-id="1f34d-136">Передача этих значений позволяет выполнять кодировки с помощью одного вызова, а не несколько вызовов.</span><span class="sxs-lookup"><span data-stu-id="1f34d-136">Passing these values enables you to perform encodings with a single call instead of multiple calls.</span></span>
  
<span data-ttu-id="1f34d-137">Реализация TNEF отчетов проблем кодировки TNEF потока без остановки процесса **FinishComponent** .</span><span class="sxs-lookup"><span data-stu-id="1f34d-137">The TNEF implementation reports TNEF stream encoding problems without stopping the **FinishComponent** process.</span></span> <span data-ttu-id="1f34d-138">Структура **STnefProblemArray** , возвращаемых в _lppProblems_ указывает, какие атрибуты TNEF или свойства MAPI, если не удается обработать.</span><span class="sxs-lookup"><span data-stu-id="1f34d-138">The **STnefProblemArray** structure returned in  _lppProblems_ indicates which TNEF attributes or MAPI properties, if any, could not be processed.</span></span> <span data-ttu-id="1f34d-139">Значение, возвращаемое в **scode** членом одного из структур **STnefProblem** , содержащихся в **STnefProblemArray** Указывает конкретную проблему.</span><span class="sxs-lookup"><span data-stu-id="1f34d-139">The value returned in the **scode** member of the one of the **STnefProblem** structures contained in **STnefProblemArray** indicates the specific problem.</span></span> <span data-ttu-id="1f34d-140">Поставщик или шлюз может работать предполагается, что все свойства или атрибуты, для которых **FinishComponent** не возвращает отчет о проблеме обработаны успешно.</span><span class="sxs-lookup"><span data-stu-id="1f34d-140">The provider or gateway can work on the assumption that all properties or attributes for which **FinishComponent** does not return a problem report were processed successfully.</span></span> 
  
<span data-ttu-id="1f34d-141">Если поставщик или шлюз не работает с массивами проблемы, его можно передать значение NULL в _lppProblems_; в этом случае возвращается массив не проблемы.</span><span class="sxs-lookup"><span data-stu-id="1f34d-141">If a provider or gateway does not work with problem arrays, it can pass NULL in  _lppProblems_; in this case, no problem array is returned.</span></span>
  
<span data-ttu-id="1f34d-142">Значение, возвращаемое в _lppProblems_ действителен только в том случае, если вызов возвращает значение S_OK.</span><span class="sxs-lookup"><span data-stu-id="1f34d-142">The value returned in  _lppProblems_ is valid only if the call returns S_OK.</span></span> <span data-ttu-id="1f34d-143">Если возвращается значение S_OK, поставщик или шлюз должен проверить, значения, возвращаемые в структуре [STnefProblemArray](stnefproblemarray.md) .</span><span class="sxs-lookup"><span data-stu-id="1f34d-143">When S_OK is returned, the provider or gateway should check the values returned in the [STnefProblemArray](stnefproblemarray.md) structure.</span></span> <span data-ttu-id="1f34d-144">При возникновении ошибки на звонок, структура **STnefProblemArray** не заполнено, и вызывающему поставщика или шлюз не использовать или Бесплатная загрузка структуры.</span><span class="sxs-lookup"><span data-stu-id="1f34d-144">If an error occurs on the call, the **STnefProblemArray** structure is not filled in, and the calling provider or gateway should not use or free the structure.</span></span> <span data-ttu-id="1f34d-145">Если ошибки не обнаружены на звонок, вызывающий поставщика или шлюз должен высвободить память для **STnefProblemArray** путем вызова функции [MAPIFreeBuffer](mapifreebuffer.md) .</span><span class="sxs-lookup"><span data-stu-id="1f34d-145">If no error occurs on the call, the calling provider or gateway must release the memory for the **STnefProblemArray** by calling the [MAPIFreeBuffer](mapifreebuffer.md) function.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="1f34d-146">См. также</span><span class="sxs-lookup"><span data-stu-id="1f34d-146">See also</span></span>



[<span data-ttu-id="1f34d-147">ITnef::AddProps</span><span class="sxs-lookup"><span data-stu-id="1f34d-147">ITnef::AddProps</span></span>](itnef-addprops.md)
  
[<span data-ttu-id="1f34d-148">ITnef::SetProps</span><span class="sxs-lookup"><span data-stu-id="1f34d-148">ITnef::SetProps</span></span>](itnef-setprops.md)
  
[<span data-ttu-id="1f34d-149">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="1f34d-149">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="1f34d-150">OpenTnefStream</span><span class="sxs-lookup"><span data-stu-id="1f34d-150">OpenTnefStream</span></span>](opentnefstream.md)
  
[<span data-ttu-id="1f34d-151">OpenTnefStreamEx</span><span class="sxs-lookup"><span data-stu-id="1f34d-151">OpenTnefStreamEx</span></span>](opentnefstreamex.md)
  
[<span data-ttu-id="1f34d-152">SPropTagArray</span><span class="sxs-lookup"><span data-stu-id="1f34d-152">SPropTagArray</span></span>](sproptagarray.md)
  
[<span data-ttu-id="1f34d-153">STnefProblemArray</span><span class="sxs-lookup"><span data-stu-id="1f34d-153">STnefProblemArray</span></span>](stnefproblemarray.md)
  
[<span data-ttu-id="1f34d-154">ITnef : IUnknown</span><span class="sxs-lookup"><span data-stu-id="1f34d-154">ITnef : IUnknown</span></span>](itnefiunknown.md)

