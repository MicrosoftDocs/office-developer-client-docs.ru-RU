---
title: IMAPIPropSetProps
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIProp.SetProps
api_type:
- COM
ms.assetid: 49f007c9-42e5-4391-8b83-988c9b0ebdba
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 87709f8a77471637d7652982669bcba93ca2e1dd
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412620"
---
# <a name="imapipropsetprops"></a><span data-ttu-id="7cdf9-103">IMAPIProp::SetProps</span><span class="sxs-lookup"><span data-stu-id="7cdf9-103">IMAPIProp::SetProps</span></span>

  
  
<span data-ttu-id="7cdf9-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7cdf9-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7cdf9-105">Обновляет одно или несколько свойств.</span><span class="sxs-lookup"><span data-stu-id="7cdf9-105">Updates one or more properties.</span></span>
  
```cpp
HRESULT SetProps(
  ULONG cValues,
  LPSPropValue lpPropArray,
  LPSPropProblemArray FAR * lppProblems
);
```

## <a name="parameters"></a><span data-ttu-id="7cdf9-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="7cdf9-106">Parameters</span></span>

 <span data-ttu-id="7cdf9-107">_cValues_</span><span class="sxs-lookup"><span data-stu-id="7cdf9-107">_cValues_</span></span>
  
> <span data-ttu-id="7cdf9-108">[in] Количество значений свойств, на которые указывает _параметр lpPropArray._</span><span class="sxs-lookup"><span data-stu-id="7cdf9-108">[in] The count of property values pointed to by the  _lpPropArray_ parameter.</span></span> <span data-ttu-id="7cdf9-109">Параметр  _cValues_ не должен быть 0.</span><span class="sxs-lookup"><span data-stu-id="7cdf9-109">The  _cValues_ parameter must not be 0.</span></span> 
    
 <span data-ttu-id="7cdf9-110">_lpPropArray_</span><span class="sxs-lookup"><span data-stu-id="7cdf9-110">_lpPropArray_</span></span>
  
> <span data-ttu-id="7cdf9-111">[in] Указатель на массив [структур SPropValue,](spropvalue.md) содержащих обновляемые значения свойств.</span><span class="sxs-lookup"><span data-stu-id="7cdf9-111">[in] A pointer to an array of [SPropValue](spropvalue.md) structures that contain property values to be updated.</span></span> 
    
 <span data-ttu-id="7cdf9-112">_lppProblems_</span><span class="sxs-lookup"><span data-stu-id="7cdf9-112">_lppProblems_</span></span>
  
> <span data-ttu-id="7cdf9-113">[in, out] На входе указатель на указатель на [структуру SPropProblemArray;](spropproblemarray.md) в противном случае NULL, указывающая на отсутствие необходимости в сведениях об ошибках.</span><span class="sxs-lookup"><span data-stu-id="7cdf9-113">[in, out] On input, a pointer to a pointer to an [SPropProblemArray](spropproblemarray.md) structure; otherwise, NULL, indicating no need for error information.</span></span> <span data-ttu-id="7cdf9-114">Если  _lppProblems_ является допустимым указателем ввода, **SetProps** возвращает подробные сведения об ошибках при обновлении одного или более свойств.</span><span class="sxs-lookup"><span data-stu-id="7cdf9-114">If  _lppProblems_ is a valid pointer on input, **SetProps** returns detailed information about errors in updating one or more properties.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="7cdf9-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="7cdf9-115">Return value</span></span>

<span data-ttu-id="7cdf9-116">S_OK</span><span class="sxs-lookup"><span data-stu-id="7cdf9-116">S_OK</span></span> 
  
> <span data-ttu-id="7cdf9-117">Свойства были успешно обновлены.</span><span class="sxs-lookup"><span data-stu-id="7cdf9-117">The properties were successfully updated.</span></span>
    
<span data-ttu-id="7cdf9-118">Следующие значения могут быть возвращены в **структуре SPropProblemArray,** но не в качестве значений возврата **для SetProps:**</span><span class="sxs-lookup"><span data-stu-id="7cdf9-118">The following values can be returned in the **SPropProblemArray** structure, but not as return values for **SetProps**:</span></span>
  
<span data-ttu-id="7cdf9-119">MAPI_E_BAD_CHARWIDTH</span><span class="sxs-lookup"><span data-stu-id="7cdf9-119">MAPI_E_BAD_CHARWIDTH</span></span> 
  
> <span data-ttu-id="7cdf9-120">Либо был MAPI_UNICODE флаг, а реализация не поддерживает Юникод, либо MAPI_UNICODE не установлена, а реализация поддерживает только Юникод.</span><span class="sxs-lookup"><span data-stu-id="7cdf9-120">Either the MAPI_UNICODE flag was set and the implementation does not support Unicode, or MAPI_UNICODE was not set and the implementation supports only Unicode.</span></span>
    
<span data-ttu-id="7cdf9-121">MAPI_E_COMPUTED</span><span class="sxs-lookup"><span data-stu-id="7cdf9-121">MAPI_E_COMPUTED</span></span> 
  
> <span data-ttu-id="7cdf9-122">Свойство не может быть обновлено, так как оно только для чтения, вычисляется поставщиком услуг, отвечающим за объект.</span><span class="sxs-lookup"><span data-stu-id="7cdf9-122">The property cannot be updated because it is read-only, computed by the service provider that is responsible for the object.</span></span>
    
<span data-ttu-id="7cdf9-123">MAPI_E_INVALID_TYPE</span><span class="sxs-lookup"><span data-stu-id="7cdf9-123">MAPI_E_INVALID_TYPE</span></span> 
  
> <span data-ttu-id="7cdf9-124">Тип свойства недействителен.</span><span class="sxs-lookup"><span data-stu-id="7cdf9-124">The property type is invalid.</span></span>
    
<span data-ttu-id="7cdf9-125">MAPI_E_NO_ACCESS</span><span class="sxs-lookup"><span data-stu-id="7cdf9-125">MAPI_E_NO_ACCESS</span></span> 
  
> <span data-ttu-id="7cdf9-126">Была предпринята попытка изменить объект только для чтения или получить доступ к объекту, для которого у пользователя недостаточно разрешений.</span><span class="sxs-lookup"><span data-stu-id="7cdf9-126">An attempt was made to modify a read-only object or to access an object for which the user has insufficient permissions.</span></span>
    
<span data-ttu-id="7cdf9-127">MAPI_E_NOT_ENOUGH_MEMORY</span><span class="sxs-lookup"><span data-stu-id="7cdf9-127">MAPI_E_NOT_ENOUGH_MEMORY</span></span> 
  
> <span data-ttu-id="7cdf9-128">Свойство не может быть обновлено, так как оно больше размера буфера удаленного вызова процедуры (RPC).</span><span class="sxs-lookup"><span data-stu-id="7cdf9-128">The property cannot be updated because it is larger than the remote procedure call (RPC) buffer size.</span></span>
    
<span data-ttu-id="7cdf9-129">MAPI_E_UNEXPECTED_TYPE</span><span class="sxs-lookup"><span data-stu-id="7cdf9-129">MAPI_E_UNEXPECTED_TYPE</span></span> 
  
> <span data-ttu-id="7cdf9-130">Тип свойства не является типом, ожидаемым реализацией вызова.</span><span class="sxs-lookup"><span data-stu-id="7cdf9-130">The property type is not the type expected by the calling implementation.</span></span>
    
## <a name="notes-to-implementers"></a><span data-ttu-id="7cdf9-131">Примечания для исполнителей</span><span class="sxs-lookup"><span data-stu-id="7cdf9-131">Notes to implementers</span></span>

<span data-ttu-id="7cdf9-132">Игнорировать тег **свойства PR_NULL** [(PidTagNull)](pidtagnull-canonical-property.md)и все свойства с **типом PT_ERROR**.</span><span class="sxs-lookup"><span data-stu-id="7cdf9-132">Ignore the **PR_NULL** ([PidTagNull](pidtagnull-canonical-property.md)) property tag and all properties with a type of **PT_ERROR**.</span></span> <span data-ttu-id="7cdf9-133">Не внося изменений или отчетов о проблемах в **структуре SPropProblemArray.**</span><span class="sxs-lookup"><span data-stu-id="7cdf9-133">Do not make changes or report problems in the **SPropProblemArray** structure.</span></span> 
  
<span data-ttu-id="7cdf9-134">Возврат MAPI_E_INVALID_PARAMETER, если свойство **типа** PT_OBJECT включено в массив значений свойства.</span><span class="sxs-lookup"><span data-stu-id="7cdf9-134">Return MAPI_E_INVALID_PARAMETER if a property of type **PT_OBJECT** is included in the property value array.</span></span> <span data-ttu-id="7cdf9-135">Также возвращаем эту ошибку, если свойство с несколькими значениями включено в массив и его **член cValues** задает значение 0.</span><span class="sxs-lookup"><span data-stu-id="7cdf9-135">Also return this error if a multiple-value property is included in the array and its **cValues** member is set to 0.</span></span> 
  
<span data-ttu-id="7cdf9-136">Если вызов удается в целом, но есть проблемы с установкой некоторых свойств, верните S_OK и поместите сведения о проблемах в соответствующую запись **структуры SPropProblemArray,** на которую указывает параметр _lppProblems._</span><span class="sxs-lookup"><span data-stu-id="7cdf9-136">If the call succeeds overall but there are problems with setting some of the properties, return S_OK and put information about the problems in the appropriate entry of the **SPropProblemArray** structure that the  _lppProblems_ parameter points to.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="7cdf9-137">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="7cdf9-137">Notes to callers</span></span>

<span data-ttu-id="7cdf9-138">В зависимости от поставщика услуг вы также можете изменить тип свойства, передав тег свойства, содержащий другой тип, чем был ранее использован с заданным идентификатором свойства.</span><span class="sxs-lookup"><span data-stu-id="7cdf9-138">Depending on the service provider, you might also be able to change the property type by passing a property tag that contains a different type than was previously used with a given property identifier.</span></span>
  
<span data-ttu-id="7cdf9-139">Если вы включаете тег свойства для свойства, которое неподтверчено объекту, а реализация **SetProps** позволяет создавать новые свойства, свойство добавляется к объекту.</span><span class="sxs-lookup"><span data-stu-id="7cdf9-139">If you include a property tag for a property that is unsupported by the object and the implementation of **SetProps** allows the creation of new properties, the property is added to the object.</span></span> <span data-ttu-id="7cdf9-140">Любое предыдущее значение, сохраненное с идентификатором свойства, которое использовалось для нового свойства, удаляется.</span><span class="sxs-lookup"><span data-stu-id="7cdf9-140">Any previous value stored with the property identifier that was used for the new property is discarded.</span></span> 
  
<span data-ttu-id="7cdf9-141">Обратите внимание, S_OK значение возврата не гарантирует успешное обновление всех свойств.</span><span class="sxs-lookup"><span data-stu-id="7cdf9-141">Note that the S_OK return value does not guarantee that all of the properties were successfully updated.</span></span> <span data-ttu-id="7cdf9-142">Некоторые поставщики кэша **Вызовы SetProps,** пока они не получат вызов, который требует вмешательства поставщика, такие как [IMAPIProp::SaveChanges](imapiprop-savechanges.md) или [IMAPIProp::GetProps](imapiprop-getprops.md).</span><span class="sxs-lookup"><span data-stu-id="7cdf9-142">Some providers cache **SetProps** calls until they receive a call that requires provider intervention, such as [IMAPIProp::SaveChanges](imapiprop-savechanges.md) or [IMAPIProp::GetProps](imapiprop-getprops.md).</span></span> <span data-ttu-id="7cdf9-143">Таким образом, можно получать значения ошибок, которые относятся к **вызову SetProps** с последующими вызовами.</span><span class="sxs-lookup"><span data-stu-id="7cdf9-143">Therefore, it is possible to receive error values that relate to the **SetProps** call with the later calls.</span></span> 
  
<span data-ttu-id="7cdf9-144">Если **SetProps** возвращается S_OK, проверьте структуру **SPropProblemArray,** на которые указывает  _lppProblems,_ на проблемы с обновлением отдельных свойств.</span><span class="sxs-lookup"><span data-stu-id="7cdf9-144">If **SetProps** returns S_OK, check the **SPropProblemArray** structure pointed to by  _lppProblems_ for problems updating individual properties.</span></span> <span data-ttu-id="7cdf9-145">Если **SetProps** возвращает ошибку, не проверяйте массив проблем свойств.</span><span class="sxs-lookup"><span data-stu-id="7cdf9-145">If **SetProps** returns an error, do not check the property problem array.</span></span> <span data-ttu-id="7cdf9-146">Вместо этого позвоните по методу [IMAPIProp::GetLastError.](imapiprop-getlasterror.md)</span><span class="sxs-lookup"><span data-stu-id="7cdf9-146">Instead, call the object's [IMAPIProp::GetLastError](imapiprop-getlasterror.md) method.</span></span> 
  
<span data-ttu-id="7cdf9-147">При обновлении больших свойств **SetProps** может привести к сбойу и возвращению MAPI_E_NOT_ENOUGH_MEMORY.</span><span class="sxs-lookup"><span data-stu-id="7cdf9-147">When updating large properties, **SetProps** can fail and return MAPI_E_NOT_ENOUGH_MEMORY.</span></span> <span data-ttu-id="7cdf9-148">Для свойств не существует максимального размера, а у разных объектов могут быть разные ограничения.</span><span class="sxs-lookup"><span data-stu-id="7cdf9-148">There is no maximum size for properties, and different objects can have different limits.</span></span> <span data-ttu-id="7cdf9-149">Если вы имеете дело с потенциально большими свойствами, будьте готовы вызвать метод [IMAPIProp::OpenProperty](imapiprop-openproperty.md) с IID_IStream в качестве идентификатора интерфейса, если **SetProps** возвращает это значение ошибки.</span><span class="sxs-lookup"><span data-stu-id="7cdf9-149">If you deal with potentially large properties, be prepared to call the [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method with IID_IStream as the interface identifier if **SetProps** returns this error value.</span></span> 
  
<span data-ttu-id="7cdf9-150">Вызов [функции MAPIFreeBuffer,](mapifreebuffer.md) чтобы освободить **структуру SPropProblemArray.**</span><span class="sxs-lookup"><span data-stu-id="7cdf9-150">Call the [MAPIFreeBuffer](mapifreebuffer.md) function to free the **SPropProblemArray** structure.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="7cdf9-151">Справочные материалы по MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="7cdf9-151">MFCMAPI reference</span></span>

<span data-ttu-id="7cdf9-152">Пример кода MFCMAPI указан в приведенной ниже таблице.</span><span class="sxs-lookup"><span data-stu-id="7cdf9-152">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="7cdf9-153">**Файл**</span><span class="sxs-lookup"><span data-stu-id="7cdf9-153">**File**</span></span>|<span data-ttu-id="7cdf9-154">**Функция**</span><span class="sxs-lookup"><span data-stu-id="7cdf9-154">**Function**</span></span>|<span data-ttu-id="7cdf9-155">**Примечание**</span><span class="sxs-lookup"><span data-stu-id="7cdf9-155">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="7cdf9-156">PropertyEditor.cpp</span><span class="sxs-lookup"><span data-stu-id="7cdf9-156">PropertyEditor.cpp</span></span>  <br/> |<span data-ttu-id="7cdf9-157">CPropertyEditor::WriteSPropValueToObject</span><span class="sxs-lookup"><span data-stu-id="7cdf9-157">CPropertyEditor::WriteSPropValueToObject</span></span>  <br/> |<span data-ttu-id="7cdf9-158">MFCMAPI использует метод **IMAPIProp::SetProps** для записи свойства обратно к объекту после редактирования свойства.</span><span class="sxs-lookup"><span data-stu-id="7cdf9-158">MFCMAPI uses the **IMAPIProp::SetProps** method to write a property back to an object after the property has been edited.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="7cdf9-159">См. также</span><span class="sxs-lookup"><span data-stu-id="7cdf9-159">See also</span></span>



[<span data-ttu-id="7cdf9-160">IMAPIProp::GetLastError</span><span class="sxs-lookup"><span data-stu-id="7cdf9-160">IMAPIProp::GetLastError</span></span>](imapiprop-getlasterror.md)
  
[<span data-ttu-id="7cdf9-161">IMAPIProp::GetProps</span><span class="sxs-lookup"><span data-stu-id="7cdf9-161">IMAPIProp::GetProps</span></span>](imapiprop-getprops.md)
  
[<span data-ttu-id="7cdf9-162">IMAPIProp::OpenProperty</span><span class="sxs-lookup"><span data-stu-id="7cdf9-162">IMAPIProp::OpenProperty</span></span>](imapiprop-openproperty.md)
  
[<span data-ttu-id="7cdf9-163">IMAPIProp::SaveChanges</span><span class="sxs-lookup"><span data-stu-id="7cdf9-163">IMAPIProp::SaveChanges</span></span>](imapiprop-savechanges.md)
  
[<span data-ttu-id="7cdf9-164">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="7cdf9-164">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="7cdf9-165">SPropProblemArray</span><span class="sxs-lookup"><span data-stu-id="7cdf9-165">SPropProblemArray</span></span>](spropproblemarray.md)
  
[<span data-ttu-id="7cdf9-166">SPropValue</span><span class="sxs-lookup"><span data-stu-id="7cdf9-166">SPropValue</span></span>](spropvalue.md)
  
[<span data-ttu-id="7cdf9-167">IMAPIProp : IUnknown</span><span class="sxs-lookup"><span data-stu-id="7cdf9-167">IMAPIProp : IUnknown</span></span>](imapipropiunknown.md)

