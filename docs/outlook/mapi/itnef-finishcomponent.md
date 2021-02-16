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
ms.openlocfilehash: c8dc10bdb8bcde15dccf7bab4d9e10d2481cef11
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33416442"
---
# <a name="itneffinishcomponent"></a><span data-ttu-id="4260f-103">ITnef::FinishComponent</span><span class="sxs-lookup"><span data-stu-id="4260f-103">ITnef::FinishComponent</span></span>

  
  
<span data-ttu-id="4260f-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4260f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4260f-105">Обрабатывает отдельные компоненты из сообщения по одному в поток Transport-Neutral формата инкапсуляции (TNEF).</span><span class="sxs-lookup"><span data-stu-id="4260f-105">Processes individual components from a message one at a time into a Transport-Neutral Encapsulation Format (TNEF) stream.</span></span>
  
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

## <a name="parameters"></a><span data-ttu-id="4260f-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="4260f-106">Parameters</span></span>

 <span data-ttu-id="4260f-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="4260f-107">_ulFlags_</span></span>
  
> <span data-ttu-id="4260f-108">[in] Битоваяmas флагов, которая управляет тем, какой компонент будет завершен.</span><span class="sxs-lookup"><span data-stu-id="4260f-108">[in] A bitmask of flags that controls which component will be finished.</span></span> <span data-ttu-id="4260f-109">Должен быть установлен один или несколько следующих флагов:</span><span class="sxs-lookup"><span data-stu-id="4260f-109">One or the other of the following flags must be set:</span></span>
    
<span data-ttu-id="4260f-110">TNEF_COMPONENT_ATTACHMENT</span><span class="sxs-lookup"><span data-stu-id="4260f-110">TNEF_COMPONENT_ATTACHMENT</span></span> 
  
> <span data-ttu-id="4260f-111">Обработка для объекта вложения будет завершена; Параметр  _ulComponentID_ **содержит** PR_ATTACH_NUM ([PidTagAttachNumber)](pidtagattachnumber-canonical-property.md)вложения.</span><span class="sxs-lookup"><span data-stu-id="4260f-111">Processing will be finished for an attachment object; the  _ulComponentID_ parameter contains the **PR_ATTACH_NUM** ([PidTagAttachNumber](pidtagattachnumber-canonical-property.md)) property of the attachment.</span></span> 
    
<span data-ttu-id="4260f-112">TNEF_COMPONENT_MESSAGE</span><span class="sxs-lookup"><span data-stu-id="4260f-112">TNEF_COMPONENT_MESSAGE</span></span> 
  
> <span data-ttu-id="4260f-113">Обработка для объекта сообщения будет завершена.</span><span class="sxs-lookup"><span data-stu-id="4260f-113">Processing will be finished for a message object.</span></span> 
    
 <span data-ttu-id="4260f-114">_ulComponentID_</span><span class="sxs-lookup"><span data-stu-id="4260f-114">_ulComponentID_</span></span>
  
> <span data-ttu-id="4260f-115">[in] 0, чтобы указать обработку сообщения или PR_ATTACH_NUM вложения для обработки. </span><span class="sxs-lookup"><span data-stu-id="4260f-115">[in] 0 to indicate processing for a message, or the **PR_ATTACH_NUM** property of an attachment to be processed.</span></span> <span data-ttu-id="4260f-116">Если в TNEF_COMPONENT_MESSAGE  _ulFlags_ задан флаг,  _ulComponentID_ должен иметь 0.</span><span class="sxs-lookup"><span data-stu-id="4260f-116">If the TNEF_COMPONENT_MESSAGE flag is set in the  _ulFlags_ parameter,  _ulComponentID_ must be 0.</span></span> 
    
 <span data-ttu-id="4260f-117">_lpCustomPropList_</span><span class="sxs-lookup"><span data-stu-id="4260f-117">_lpCustomPropList_</span></span>
  
> <span data-ttu-id="4260f-118">[in] Указатель на структуру [SPropTagArray,](sproptagarray.md) которая содержит теги свойств, которые определяют свойства, переданные в _параметре lpCustomProps._</span><span class="sxs-lookup"><span data-stu-id="4260f-118">[in] A pointer to an [SPropTagArray](sproptagarray.md) structure that contains property tags that identify the properties passed in the  _lpCustomProps_ parameter.</span></span> <span data-ttu-id="4260f-119">Между каждым значением свойства в  _lpCustomProps_ и тегом свойства в параметре  _lpCustomPropList_ должно быть соответствие "один к одному".</span><span class="sxs-lookup"><span data-stu-id="4260f-119">There must be a one-to-one correspondence between each property value in  _lpCustomProps_ and a property tag in the  _lpCustomPropList_ parameter.</span></span> 
    
 <span data-ttu-id="4260f-120">_lpCustomProps_</span><span class="sxs-lookup"><span data-stu-id="4260f-120">_lpCustomProps_</span></span>
  
> <span data-ttu-id="4260f-121">[in] Указатель на структуру [SPropValue,](spropvalue.md) которая содержит значения свойств для кодируемых свойств.</span><span class="sxs-lookup"><span data-stu-id="4260f-121">[in] A pointer to an [SPropValue](spropvalue.md) structure that contains property values for the properties to encode.</span></span> 
    
 <span data-ttu-id="4260f-122">_lpPropList_</span><span class="sxs-lookup"><span data-stu-id="4260f-122">_lpPropList_</span></span>
  
> <span data-ttu-id="4260f-123">[in] Указатель на структуру **SPropTagArray,** которая содержит теги свойств для кодируемых свойств.</span><span class="sxs-lookup"><span data-stu-id="4260f-123">[in] A pointer to an **SPropTagArray** structure that contains property tags for the properties to encode.</span></span> 
    
 <span data-ttu-id="4260f-124">_lppProblems_</span><span class="sxs-lookup"><span data-stu-id="4260f-124">_lppProblems_</span></span>
  
> <span data-ttu-id="4260f-125">[out] Указатель на указатель на возвращенную [структуру STnefProblemArray.](stnefproblemarray.md)</span><span class="sxs-lookup"><span data-stu-id="4260f-125">[out] A pointer to a pointer to a returned [STnefProblemArray](stnefproblemarray.md) structure.</span></span> <span data-ttu-id="4260f-126">Структура **STnefProblemArray** указывает, какие свойства ,если таковые имеются, не были закодированы должным образом.</span><span class="sxs-lookup"><span data-stu-id="4260f-126">The **STnefProblemArray** structure indicates which properties, if any, were not encoded properly.</span></span> <span data-ttu-id="4260f-127">Если в параметре  _lppProblems_ передается NULL, массив проблем свойств не возвращается.</span><span class="sxs-lookup"><span data-stu-id="4260f-127">If NULL is passed in the  _lppProblems_ parameter, no property problem array is returned.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="4260f-128">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="4260f-128">Return value</span></span>

<span data-ttu-id="4260f-129">S_OK</span><span class="sxs-lookup"><span data-stu-id="4260f-129">S_OK</span></span> 
  
> <span data-ttu-id="4260f-130">����� ������� � ������ ��������� ��������� ��� ��������.</span><span class="sxs-lookup"><span data-stu-id="4260f-130">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="4260f-131">Примечания</span><span class="sxs-lookup"><span data-stu-id="4260f-131">Remarks</span></span>

<span data-ttu-id="4260f-132">Поставщики транспорта, поставщики параметров хранения сообщений и шлюзы звонят **методу ITnef::FinishComponent** для выполнения обработки TNEF для одного компонента, сообщения или вложения, как указано флагом, установленным в параметре _ulFlags._</span><span class="sxs-lookup"><span data-stu-id="4260f-132">Transport providers, message store providers, and gateways call the **ITnef::FinishComponent** method to perform TNEF processing for one component, either a message or an attachment, as indicated by the flag set in the  _ulFlags_ parameter.</span></span> 
  
<span data-ttu-id="4260f-133">Чтобы включить обработку компонентов, поставщик вызовов или шлюз передают флаг TNEF_COMPONENT_ENCODING в  _ulFlags_ для функции [OpenTnefStream](opentnefstream.md) или [OpenTnefStreamEx,](opentnefstreamex.md) которая открывает объект для получения кодив.</span><span class="sxs-lookup"><span data-stu-id="4260f-133">For component processing to be enabled, the calling provider or gateway pass the TNEF_COMPONENT_ENCODING flag in  _ulFlags_ for the [OpenTnefStream](opentnefstream.md) or [OpenTnefStreamEx](opentnefstreamex.md) function that opened the object to receive encoding.</span></span> 
  
<span data-ttu-id="4260f-134">Передача значений в _параметрах lpCustomPropList_ и _lpCustomProps_ выполняет коду компонента, эквивалентную коде, выполняемой методом [ITnef::SetProps.](itnef-setprops.md)</span><span class="sxs-lookup"><span data-stu-id="4260f-134">Passing values in the  _lpCustomPropList_ and  _lpCustomProps_ parameters performs component encoding equivalent to that done by the [ITnef::SetProps](itnef-setprops.md) method.</span></span> <span data-ttu-id="4260f-135">Передача значения в _параметре lpPropList_ выполняет коду компонента, эквивалентную коде, выполняемой методом [ITnef::AddProps](itnef-addprops.md) с флагом TNEF_PROP_INCLUDE, установленным в _ulFlags._</span><span class="sxs-lookup"><span data-stu-id="4260f-135">Passing a value in the  _lpPropList_ parameter performs component encoding equivalent to that done by the [ITnef::AddProps](itnef-addprops.md) method with the TNEF_PROP_INCLUDE flag set in  _ulFlags_.</span></span> <span data-ttu-id="4260f-136">Передача этих значений позволяет выполнять кодилеты с помощью одного вызова, а не нескольких вызовов.</span><span class="sxs-lookup"><span data-stu-id="4260f-136">Passing these values enables you to perform encodings with a single call instead of multiple calls.</span></span>
  
<span data-ttu-id="4260f-137">Реализация TNEF сообщает о проблемах кодиации потока TNEF без остановки процесса **FinishComponent.**</span><span class="sxs-lookup"><span data-stu-id="4260f-137">The TNEF implementation reports TNEF stream encoding problems without stopping the **FinishComponent** process.</span></span> <span data-ttu-id="4260f-138">Структура **STnefProblemArray,** возвращаемая  _в lppProblems,_ указывает, какие атрибуты TNEF или свойства MAPI (если таковые имеются) не удалось обработать.</span><span class="sxs-lookup"><span data-stu-id="4260f-138">The **STnefProblemArray** structure returned in  _lppProblems_ indicates which TNEF attributes or MAPI properties, if any, could not be processed.</span></span> <span data-ttu-id="4260f-139">Значение, возвращаемого в члене **scode** одной из структур **STnefProblem,** содержащихся в **STnefProblemArray,** указывает на конкретную проблему.</span><span class="sxs-lookup"><span data-stu-id="4260f-139">The value returned in the **scode** member of the one of the **STnefProblem** structures contained in **STnefProblemArray** indicates the specific problem.</span></span> <span data-ttu-id="4260f-140">Поставщик или шлюз может работать при предположении, что все свойства или атрибуты, для которых **FinishComponent** не возвращает отчет о проблеме, были успешно обработаны.</span><span class="sxs-lookup"><span data-stu-id="4260f-140">The provider or gateway can work on the assumption that all properties or attributes for which **FinishComponent** does not return a problem report were processed successfully.</span></span> 
  
<span data-ttu-id="4260f-141">Если поставщик или шлюз не работает с массивами проблем, он может передавать NULL в  _lppProblems;_ в этом случае массив проблем не возвращается.</span><span class="sxs-lookup"><span data-stu-id="4260f-141">If a provider or gateway does not work with problem arrays, it can pass NULL in  _lppProblems_; in this case, no problem array is returned.</span></span>
  
<span data-ttu-id="4260f-142">Возвращаемая в  _lppProblems_ значение допустимо, только если вызов возвращает S_OK.</span><span class="sxs-lookup"><span data-stu-id="4260f-142">The value returned in  _lppProblems_ is valid only if the call returns S_OK.</span></span> <span data-ttu-id="4260f-143">Когда S_OK возвращается, поставщик или шлюз должен проверить значения, возвращенные в [структуре STnefProblemArray.](stnefproblemarray.md)</span><span class="sxs-lookup"><span data-stu-id="4260f-143">When S_OK is returned, the provider or gateway should check the values returned in the [STnefProblemArray](stnefproblemarray.md) structure.</span></span> <span data-ttu-id="4260f-144">Если при вызове возникает ошибка, структура **STnefProblemArray** не заполняется, и поставщик или шлюз вызовов не должны использовать или освободить структуру.</span><span class="sxs-lookup"><span data-stu-id="4260f-144">If an error occurs on the call, the **STnefProblemArray** structure is not filled in, and the calling provider or gateway should not use or free the structure.</span></span> <span data-ttu-id="4260f-145">Если ошибка при вызове не возникает, поставщик или шлюз вызовов должен освободить память **для STnefProblemArray,** вызывая функцию [MAPIFreeBuffer.](mapifreebuffer.md)</span><span class="sxs-lookup"><span data-stu-id="4260f-145">If no error occurs on the call, the calling provider or gateway must release the memory for the **STnefProblemArray** by calling the [MAPIFreeBuffer](mapifreebuffer.md) function.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="4260f-146">См. также</span><span class="sxs-lookup"><span data-stu-id="4260f-146">See also</span></span>



[<span data-ttu-id="4260f-147">ITnef::AddProps</span><span class="sxs-lookup"><span data-stu-id="4260f-147">ITnef::AddProps</span></span>](itnef-addprops.md)
  
[<span data-ttu-id="4260f-148">ITnef::SetProps</span><span class="sxs-lookup"><span data-stu-id="4260f-148">ITnef::SetProps</span></span>](itnef-setprops.md)
  
[<span data-ttu-id="4260f-149">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="4260f-149">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="4260f-150">OpenTnefStream</span><span class="sxs-lookup"><span data-stu-id="4260f-150">OpenTnefStream</span></span>](opentnefstream.md)
  
[<span data-ttu-id="4260f-151">OpenTnefStreamEx</span><span class="sxs-lookup"><span data-stu-id="4260f-151">OpenTnefStreamEx</span></span>](opentnefstreamex.md)
  
[<span data-ttu-id="4260f-152">SPropTagArray</span><span class="sxs-lookup"><span data-stu-id="4260f-152">SPropTagArray</span></span>](sproptagarray.md)
  
[<span data-ttu-id="4260f-153">STnefProblemArray</span><span class="sxs-lookup"><span data-stu-id="4260f-153">STnefProblemArray</span></span>](stnefproblemarray.md)
  
[<span data-ttu-id="4260f-154">ITnef : IUnknown</span><span class="sxs-lookup"><span data-stu-id="4260f-154">ITnef : IUnknown</span></span>](itnefiunknown.md)

