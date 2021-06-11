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
# <a name="itneffinishcomponent"></a><span data-ttu-id="dab4c-103">ITnef::FinishComponent</span><span class="sxs-lookup"><span data-stu-id="dab4c-103">ITnef::FinishComponent</span></span>

  
  
<span data-ttu-id="dab4c-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="dab4c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="dab4c-105">Обрабатывает отдельные компоненты из сообщения по одному в поток Transport-Neutral формата Инкапсуляции (TNEF).</span><span class="sxs-lookup"><span data-stu-id="dab4c-105">Processes individual components from a message one at a time into a Transport-Neutral Encapsulation Format (TNEF) stream.</span></span>
  
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

## <a name="parameters"></a><span data-ttu-id="dab4c-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="dab4c-106">Parameters</span></span>

 <span data-ttu-id="dab4c-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="dab4c-107">_ulFlags_</span></span>
  
> <span data-ttu-id="dab4c-108">[in] Битмаска флагов, которые контролируют, какой компонент будет завершен.</span><span class="sxs-lookup"><span data-stu-id="dab4c-108">[in] A bitmask of flags that controls which component will be finished.</span></span> <span data-ttu-id="dab4c-109">Необходимо установить один или другой из следующих флагов:</span><span class="sxs-lookup"><span data-stu-id="dab4c-109">One or the other of the following flags must be set:</span></span>
    
<span data-ttu-id="dab4c-110">TNEF_COMPONENT_ATTACHMENT</span><span class="sxs-lookup"><span data-stu-id="dab4c-110">TNEF_COMPONENT_ATTACHMENT</span></span> 
  
> <span data-ttu-id="dab4c-111">Обработка будет завершена для объекта вложения; параметр _ulComponentID_ **содержит свойство PR_ATTACH_NUM** [(PidTagAttachNumber).](pidtagattachnumber-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="dab4c-111">Processing will be finished for an attachment object; the  _ulComponentID_ parameter contains the **PR_ATTACH_NUM** ([PidTagAttachNumber](pidtagattachnumber-canonical-property.md)) property of the attachment.</span></span> 
    
<span data-ttu-id="dab4c-112">TNEF_COMPONENT_MESSAGE</span><span class="sxs-lookup"><span data-stu-id="dab4c-112">TNEF_COMPONENT_MESSAGE</span></span> 
  
> <span data-ttu-id="dab4c-113">Обработка будет завершена для объекта сообщения.</span><span class="sxs-lookup"><span data-stu-id="dab4c-113">Processing will be finished for a message object.</span></span> 
    
 <span data-ttu-id="dab4c-114">_ulComponentID_</span><span class="sxs-lookup"><span data-stu-id="dab4c-114">_ulComponentID_</span></span>
  
> <span data-ttu-id="dab4c-115">[в] 0, чтобы указать обработку сообщения или PR_ATTACH_NUM свойства вложения, которое будет обработано. </span><span class="sxs-lookup"><span data-stu-id="dab4c-115">[in] 0 to indicate processing for a message, or the **PR_ATTACH_NUM** property of an attachment to be processed.</span></span> <span data-ttu-id="dab4c-116">Если флаг TNEF_COMPONENT_MESSAGE установлен в параметре  _ulFlags,_  _ulComponentID_ должен быть 0.</span><span class="sxs-lookup"><span data-stu-id="dab4c-116">If the TNEF_COMPONENT_MESSAGE flag is set in the  _ulFlags_ parameter,  _ulComponentID_ must be 0.</span></span> 
    
 <span data-ttu-id="dab4c-117">_lpCustomPropList_</span><span class="sxs-lookup"><span data-stu-id="dab4c-117">_lpCustomPropList_</span></span>
  
> <span data-ttu-id="dab4c-118">[in] Указатель на структуру [SPropTagArray,](sproptagarray.md) которая содержит теги свойств, определяя свойства, переданные в _параметре lpCustomProps._</span><span class="sxs-lookup"><span data-stu-id="dab4c-118">[in] A pointer to an [SPropTagArray](sproptagarray.md) structure that contains property tags that identify the properties passed in the  _lpCustomProps_ parameter.</span></span> <span data-ttu-id="dab4c-119">Между каждым значением свойства  _в lpCustomProps_ и тегом свойства в  _параметре lpCustomPropList_ должна быть корреспонденция по одному.</span><span class="sxs-lookup"><span data-stu-id="dab4c-119">There must be a one-to-one correspondence between each property value in  _lpCustomProps_ and a property tag in the  _lpCustomPropList_ parameter.</span></span> 
    
 <span data-ttu-id="dab4c-120">_lpCustomProps_</span><span class="sxs-lookup"><span data-stu-id="dab4c-120">_lpCustomProps_</span></span>
  
> <span data-ttu-id="dab4c-121">[in] Указатель на [структуру SPropValue,](spropvalue.md) которая содержит значения свойств для кодируемых свойств.</span><span class="sxs-lookup"><span data-stu-id="dab4c-121">[in] A pointer to an [SPropValue](spropvalue.md) structure that contains property values for the properties to encode.</span></span> 
    
 <span data-ttu-id="dab4c-122">_lpPropList_</span><span class="sxs-lookup"><span data-stu-id="dab4c-122">_lpPropList_</span></span>
  
> <span data-ttu-id="dab4c-123">[in] Указатель на структуру **SPropTagArray,** которая содержит теги свойств для кодируемых свойств.</span><span class="sxs-lookup"><span data-stu-id="dab4c-123">[in] A pointer to an **SPropTagArray** structure that contains property tags for the properties to encode.</span></span> 
    
 <span data-ttu-id="dab4c-124">_lppProblems_</span><span class="sxs-lookup"><span data-stu-id="dab4c-124">_lppProblems_</span></span>
  
> <span data-ttu-id="dab4c-125">[вышел] Указатель на указатель на возвращенную [структуру STnefProblemArray.](stnefproblemarray.md)</span><span class="sxs-lookup"><span data-stu-id="dab4c-125">[out] A pointer to a pointer to a returned [STnefProblemArray](stnefproblemarray.md) structure.</span></span> <span data-ttu-id="dab4c-126">Структура **STnefProblemArray** указывает, какие свойства, если таковые имеются, были неправильно закодированы.</span><span class="sxs-lookup"><span data-stu-id="dab4c-126">The **STnefProblemArray** structure indicates which properties, if any, were not encoded properly.</span></span> <span data-ttu-id="dab4c-127">Если NULL передается в  _параметре lppProblems,_ массив проблем свойств не возвращается.</span><span class="sxs-lookup"><span data-stu-id="dab4c-127">If NULL is passed in the  _lppProblems_ parameter, no property problem array is returned.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="dab4c-128">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="dab4c-128">Return value</span></span>

<span data-ttu-id="dab4c-129">S_OK</span><span class="sxs-lookup"><span data-stu-id="dab4c-129">S_OK</span></span> 
  
> <span data-ttu-id="dab4c-130">����� ������� � ������ ��������� ��������� ��� ��������.</span><span class="sxs-lookup"><span data-stu-id="dab4c-130">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="dab4c-131">Примечания</span><span class="sxs-lookup"><span data-stu-id="dab4c-131">Remarks</span></span>

<span data-ttu-id="dab4c-132">Поставщики транспорта, поставщики магазинов сообщений и шлюзы звонят **методу ITnef::FinishComponent** для выполнения обработки TNEF для одного компонента, сообщения или вложения, как указано в флаге, заданном в параметре _ulFlags._</span><span class="sxs-lookup"><span data-stu-id="dab4c-132">Transport providers, message store providers, and gateways call the **ITnef::FinishComponent** method to perform TNEF processing for one component, either a message or an attachment, as indicated by the flag set in the  _ulFlags_ parameter.</span></span> 
  
<span data-ttu-id="dab4c-133">Чтобы включить обработку компонентов, поставщик вызовов или шлюз передают флаг TNEF_COMPONENT_ENCODING  _в ulFlags_ для функции [OpenTnefStream](opentnefstream.md) или [OpenTnefStreamEx,](opentnefstreamex.md) открывающей объект для получения кодиляции.</span><span class="sxs-lookup"><span data-stu-id="dab4c-133">For component processing to be enabled, the calling provider or gateway pass the TNEF_COMPONENT_ENCODING flag in  _ulFlags_ for the [OpenTnefStream](opentnefstream.md) or [OpenTnefStreamEx](opentnefstreamex.md) function that opened the object to receive encoding.</span></span> 
  
<span data-ttu-id="dab4c-134">Передача значений в _параметрах lpCustomPropList_ и _lpCustomProps_ выполняет кодинг компонентов, эквивалентный значениям, выполняемым методом [ITnef::SetProps.](itnef-setprops.md)</span><span class="sxs-lookup"><span data-stu-id="dab4c-134">Passing values in the  _lpCustomPropList_ and  _lpCustomProps_ parameters performs component encoding equivalent to that done by the [ITnef::SetProps](itnef-setprops.md) method.</span></span> <span data-ttu-id="dab4c-135">Передача значения в  _параметре lpPropList_ выполняет кодинг компонентов, эквивалентный методу [ITnef::AddProps](itnef-addprops.md) с флагом TNEF_PROP_INCLUDE в  _ulFlags_.</span><span class="sxs-lookup"><span data-stu-id="dab4c-135">Passing a value in the  _lpPropList_ parameter performs component encoding equivalent to that done by the [ITnef::AddProps](itnef-addprops.md) method with the TNEF_PROP_INCLUDE flag set in  _ulFlags_.</span></span> <span data-ttu-id="dab4c-136">Передача этих значений позволяет выполнять кодиры одним вызовом, а не несколькими вызовами.</span><span class="sxs-lookup"><span data-stu-id="dab4c-136">Passing these values enables you to perform encodings with a single call instead of multiple calls.</span></span>
  
<span data-ttu-id="dab4c-137">Реализация TNEF сообщает о проблемах кодации потока TNEF без остановки процесса **FinishComponent.**</span><span class="sxs-lookup"><span data-stu-id="dab4c-137">The TNEF implementation reports TNEF stream encoding problems without stopping the **FinishComponent** process.</span></span> <span data-ttu-id="dab4c-138">Структура **STnefProblemArray,** возвращаемая  _в lppProblems,_ указывает, какие атрибуты TNEF или свойства MAPI, если таковые имеются, не удалось обрабатывать.</span><span class="sxs-lookup"><span data-stu-id="dab4c-138">The **STnefProblemArray** structure returned in  _lppProblems_ indicates which TNEF attributes or MAPI properties, if any, could not be processed.</span></span> <span data-ttu-id="dab4c-139">Значение, возвращаемого  в члене кода одной из структур **STnefProblem,** содержащихся в **STnefProblemArray,** указывает на конкретную проблему.</span><span class="sxs-lookup"><span data-stu-id="dab4c-139">The value returned in the **scode** member of the one of the **STnefProblem** structures contained in **STnefProblemArray** indicates the specific problem.</span></span> <span data-ttu-id="dab4c-140">Поставщик или шлюз могут работать с предположением, что все свойства или атрибуты, для которых **FinishComponent** не возвращает отчет о проблеме, были успешно обработаны.</span><span class="sxs-lookup"><span data-stu-id="dab4c-140">The provider or gateway can work on the assumption that all properties or attributes for which **FinishComponent** does not return a problem report were processed successfully.</span></span> 
  
<span data-ttu-id="dab4c-141">Если поставщик или шлюз не работает с массивами проблем, он может передавать NULL  _в lppProblems;_ В этом случае массив проблем не возвращается.</span><span class="sxs-lookup"><span data-stu-id="dab4c-141">If a provider or gateway does not work with problem arrays, it can pass NULL in  _lppProblems_; in this case, no problem array is returned.</span></span>
  
<span data-ttu-id="dab4c-142">Возвращаемая в  _lppProblems_ величина действительна только в том случае, если вызов возвращается S_OK.</span><span class="sxs-lookup"><span data-stu-id="dab4c-142">The value returned in  _lppProblems_ is valid only if the call returns S_OK.</span></span> <span data-ttu-id="dab4c-143">Когда S_OK возвращается, поставщик или шлюз должны проверить значения, возвращенные в [структуре STnefProblemArray.](stnefproblemarray.md)</span><span class="sxs-lookup"><span data-stu-id="dab4c-143">When S_OK is returned, the provider or gateway should check the values returned in the [STnefProblemArray](stnefproblemarray.md) structure.</span></span> <span data-ttu-id="dab4c-144">Если при вызове возникает ошибка, структура **STnefProblemArray** не заполняется, и поставщик вызовов или шлюз не должны использовать или освободить структуру.</span><span class="sxs-lookup"><span data-stu-id="dab4c-144">If an error occurs on the call, the **STnefProblemArray** structure is not filled in, and the calling provider or gateway should not use or free the structure.</span></span> <span data-ttu-id="dab4c-145">Если при вызове не возникает ошибки, поставщик вызовов или шлюз должен освободить память **для STnefProblemArray,** позвонив в [функцию MAPIFreeBuffer.](mapifreebuffer.md)</span><span class="sxs-lookup"><span data-stu-id="dab4c-145">If no error occurs on the call, the calling provider or gateway must release the memory for the **STnefProblemArray** by calling the [MAPIFreeBuffer](mapifreebuffer.md) function.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="dab4c-146">См. также</span><span class="sxs-lookup"><span data-stu-id="dab4c-146">See also</span></span>



[<span data-ttu-id="dab4c-147">ITnef::AddProps</span><span class="sxs-lookup"><span data-stu-id="dab4c-147">ITnef::AddProps</span></span>](itnef-addprops.md)
  
[<span data-ttu-id="dab4c-148">ITnef::SetProps</span><span class="sxs-lookup"><span data-stu-id="dab4c-148">ITnef::SetProps</span></span>](itnef-setprops.md)
  
[<span data-ttu-id="dab4c-149">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="dab4c-149">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="dab4c-150">OpenTnefStream</span><span class="sxs-lookup"><span data-stu-id="dab4c-150">OpenTnefStream</span></span>](opentnefstream.md)
  
[<span data-ttu-id="dab4c-151">OpenTnefStreamEx</span><span class="sxs-lookup"><span data-stu-id="dab4c-151">OpenTnefStreamEx</span></span>](opentnefstreamex.md)
  
[<span data-ttu-id="dab4c-152">SPropTagArray</span><span class="sxs-lookup"><span data-stu-id="dab4c-152">SPropTagArray</span></span>](sproptagarray.md)
  
[<span data-ttu-id="dab4c-153">STnefProblemArray</span><span class="sxs-lookup"><span data-stu-id="dab4c-153">STnefProblemArray</span></span>](stnefproblemarray.md)
  
[<span data-ttu-id="dab4c-154">ITnef : IUnknown</span><span class="sxs-lookup"><span data-stu-id="dab4c-154">ITnef : IUnknown</span></span>](itnefiunknown.md)

