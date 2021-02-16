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
# <a name="imapipropsetprops"></a><span data-ttu-id="db06e-103">IMAPIProp::SetProps</span><span class="sxs-lookup"><span data-stu-id="db06e-103">IMAPIProp::SetProps</span></span>

  
  
<span data-ttu-id="db06e-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="db06e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="db06e-105">Обновляет одно или несколько свойств.</span><span class="sxs-lookup"><span data-stu-id="db06e-105">Updates one or more properties.</span></span>
  
```cpp
HRESULT SetProps(
  ULONG cValues,
  LPSPropValue lpPropArray,
  LPSPropProblemArray FAR * lppProblems
);
```

## <a name="parameters"></a><span data-ttu-id="db06e-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="db06e-106">Parameters</span></span>

 <span data-ttu-id="db06e-107">_cValues_</span><span class="sxs-lookup"><span data-stu-id="db06e-107">_cValues_</span></span>
  
> <span data-ttu-id="db06e-108">[in] Количество значений свойств, на которые указывает параметр _lpPropArray._</span><span class="sxs-lookup"><span data-stu-id="db06e-108">[in] The count of property values pointed to by the  _lpPropArray_ parameter.</span></span> <span data-ttu-id="db06e-109">Параметр  _cValues не_ должен быть 0.</span><span class="sxs-lookup"><span data-stu-id="db06e-109">The  _cValues_ parameter must not be 0.</span></span> 
    
 <span data-ttu-id="db06e-110">_lpPropArray_</span><span class="sxs-lookup"><span data-stu-id="db06e-110">_lpPropArray_</span></span>
  
> <span data-ttu-id="db06e-111">[in] Указатель на массив структур [SPropValue,](spropvalue.md) содержащих значения свойств для обновления.</span><span class="sxs-lookup"><span data-stu-id="db06e-111">[in] A pointer to an array of [SPropValue](spropvalue.md) structures that contain property values to be updated.</span></span> 
    
 <span data-ttu-id="db06e-112">_lppProblems_</span><span class="sxs-lookup"><span data-stu-id="db06e-112">_lppProblems_</span></span>
  
> <span data-ttu-id="db06e-113">[in, out] При вводе указатель на указатель на [структуру SPropProblemArray;](spropproblemarray.md) в противном случае NULL, указывающее на отсутствие необходимости в сведениях об ошибках.</span><span class="sxs-lookup"><span data-stu-id="db06e-113">[in, out] On input, a pointer to a pointer to an [SPropProblemArray](spropproblemarray.md) structure; otherwise, NULL, indicating no need for error information.</span></span> <span data-ttu-id="db06e-114">Если  _lppProblems_ является допустимым указателем при вводе, **SetProps** возвращает подробные сведения об ошибках при обновлении одного или более свойств.</span><span class="sxs-lookup"><span data-stu-id="db06e-114">If  _lppProblems_ is a valid pointer on input, **SetProps** returns detailed information about errors in updating one or more properties.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="db06e-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="db06e-115">Return value</span></span>

<span data-ttu-id="db06e-116">S_OK</span><span class="sxs-lookup"><span data-stu-id="db06e-116">S_OK</span></span> 
  
> <span data-ttu-id="db06e-117">Свойства были успешно обновлены.</span><span class="sxs-lookup"><span data-stu-id="db06e-117">The properties were successfully updated.</span></span>
    
<span data-ttu-id="db06e-118">Следующие значения могут быть возвращены в структуре **SPropProblemArray,** но не в качестве возвращаемой величины **для SetProps:**</span><span class="sxs-lookup"><span data-stu-id="db06e-118">The following values can be returned in the **SPropProblemArray** structure, but not as return values for **SetProps**:</span></span>
  
<span data-ttu-id="db06e-119">MAPI_E_BAD_CHARWIDTH</span><span class="sxs-lookup"><span data-stu-id="db06e-119">MAPI_E_BAD_CHARWIDTH</span></span> 
  
> <span data-ttu-id="db06e-120">Либо флаг MAPI_UNICODE установлен, а реализация не поддерживает Юникод, либо MAPI_UNICODE не установлен, а реализация поддерживает только Юникод.</span><span class="sxs-lookup"><span data-stu-id="db06e-120">Either the MAPI_UNICODE flag was set and the implementation does not support Unicode, or MAPI_UNICODE was not set and the implementation supports only Unicode.</span></span>
    
<span data-ttu-id="db06e-121">MAPI_E_COMPUTED</span><span class="sxs-lookup"><span data-stu-id="db06e-121">MAPI_E_COMPUTED</span></span> 
  
> <span data-ttu-id="db06e-122">Свойство не может быть обновлено, так как оно является "только чтением", вычисляется поставщиком услуг, отвечающим за объект.</span><span class="sxs-lookup"><span data-stu-id="db06e-122">The property cannot be updated because it is read-only, computed by the service provider that is responsible for the object.</span></span>
    
<span data-ttu-id="db06e-123">MAPI_E_INVALID_TYPE</span><span class="sxs-lookup"><span data-stu-id="db06e-123">MAPI_E_INVALID_TYPE</span></span> 
  
> <span data-ttu-id="db06e-124">Недопустимый тип свойства.</span><span class="sxs-lookup"><span data-stu-id="db06e-124">The property type is invalid.</span></span>
    
<span data-ttu-id="db06e-125">MAPI_E_NO_ACCESS</span><span class="sxs-lookup"><span data-stu-id="db06e-125">MAPI_E_NO_ACCESS</span></span> 
  
> <span data-ttu-id="db06e-126">Предпринята попытка изменить объект, доступный только для чтения, или получить доступ к объекту, у которого у пользователя недостаточно разрешений.</span><span class="sxs-lookup"><span data-stu-id="db06e-126">An attempt was made to modify a read-only object or to access an object for which the user has insufficient permissions.</span></span>
    
<span data-ttu-id="db06e-127">MAPI_E_NOT_ENOUGH_MEMORY</span><span class="sxs-lookup"><span data-stu-id="db06e-127">MAPI_E_NOT_ENOUGH_MEMORY</span></span> 
  
> <span data-ttu-id="db06e-128">Свойство не может быть обновлено, так как оно больше размера буфера удаленного вызова процедур (RPC).</span><span class="sxs-lookup"><span data-stu-id="db06e-128">The property cannot be updated because it is larger than the remote procedure call (RPC) buffer size.</span></span>
    
<span data-ttu-id="db06e-129">MAPI_E_UNEXPECTED_TYPE</span><span class="sxs-lookup"><span data-stu-id="db06e-129">MAPI_E_UNEXPECTED_TYPE</span></span> 
  
> <span data-ttu-id="db06e-130">Тип свойства не является типом, ожидаемым реализацией вызова.</span><span class="sxs-lookup"><span data-stu-id="db06e-130">The property type is not the type expected by the calling implementation.</span></span>
    
## <a name="notes-to-implementers"></a><span data-ttu-id="db06e-131">Примечания для исполнителей</span><span class="sxs-lookup"><span data-stu-id="db06e-131">Notes to implementers</span></span>

<span data-ttu-id="db06e-132">Игнорируйте **тег PR_NULL** ([PidTagNull)](pidtagnull-canonical-property.md)и все свойства с типом PT_ERROR **.**</span><span class="sxs-lookup"><span data-stu-id="db06e-132">Ignore the **PR_NULL** ([PidTagNull](pidtagnull-canonical-property.md)) property tag and all properties with a type of **PT_ERROR**.</span></span> <span data-ttu-id="db06e-133">Не внося изменений и не сообщая о проблемах в **структуре SPropProblemArray.**</span><span class="sxs-lookup"><span data-stu-id="db06e-133">Do not make changes or report problems in the **SPropProblemArray** structure.</span></span> 
  
<span data-ttu-id="db06e-134">Возвращает MAPI_E_INVALID_PARAMETER, если свойство типа **PT_OBJECT** включено в массив значений свойств.</span><span class="sxs-lookup"><span data-stu-id="db06e-134">Return MAPI_E_INVALID_PARAMETER if a property of type **PT_OBJECT** is included in the property value array.</span></span> <span data-ttu-id="db06e-135">Также возвращает эту ошибку, если свойство с несколькими значениями включено в массив и его член **cValues** имеет значение 0.</span><span class="sxs-lookup"><span data-stu-id="db06e-135">Also return this error if a multiple-value property is included in the array and its **cValues** member is set to 0.</span></span> 
  
<span data-ttu-id="db06e-136">Если вызов в целом был успешным, но при этом возникли проблемы с настройкой некоторых свойств, верните S_OK и поместите сведения о проблемах в соответствующую запись структуры **SPropProblemArray,** на которую указывает параметр _lppProblems._</span><span class="sxs-lookup"><span data-stu-id="db06e-136">If the call succeeds overall but there are problems with setting some of the properties, return S_OK and put information about the problems in the appropriate entry of the **SPropProblemArray** structure that the  _lppProblems_ parameter points to.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="db06e-137">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="db06e-137">Notes to callers</span></span>

<span data-ttu-id="db06e-138">В зависимости от поставщика службы можно также изменить тип свойства, передав тег свойства, содержащий тип, отличающийся от ранее использованного с заданным идентификатором свойства.</span><span class="sxs-lookup"><span data-stu-id="db06e-138">Depending on the service provider, you might also be able to change the property type by passing a property tag that contains a different type than was previously used with a given property identifier.</span></span>
  
<span data-ttu-id="db06e-139">Если вы включаете тег свойства, неподключенный объектом, и реализация **SetProps** позволяет создавать новые свойства, свойство добавляется в объект.</span><span class="sxs-lookup"><span data-stu-id="db06e-139">If you include a property tag for a property that is unsupported by the object and the implementation of **SetProps** allows the creation of new properties, the property is added to the object.</span></span> <span data-ttu-id="db06e-140">Любое предыдущее значение, сохраненное с идентификатором свойства, которое использовалось для нового свойства, удаляется.</span><span class="sxs-lookup"><span data-stu-id="db06e-140">Any previous value stored with the property identifier that was used for the new property is discarded.</span></span> 
  
<span data-ttu-id="db06e-141">Обратите внимание S_OK возвращаемого значения не гарантирует, что все свойства были успешно обновлены.</span><span class="sxs-lookup"><span data-stu-id="db06e-141">Note that the S_OK return value does not guarantee that all of the properties were successfully updated.</span></span> <span data-ttu-id="db06e-142">Некоторые поставщики кэшют вызовы **SetProps,** пока не получат вызов, требуя вмешательства поставщика, например [IMAPIProp::SaveChanges](imapiprop-savechanges.md) или [IMAPIProp::GetProps.](imapiprop-getprops.md)</span><span class="sxs-lookup"><span data-stu-id="db06e-142">Some providers cache **SetProps** calls until they receive a call that requires provider intervention, such as [IMAPIProp::SaveChanges](imapiprop-savechanges.md) or [IMAPIProp::GetProps](imapiprop-getprops.md).</span></span> <span data-ttu-id="db06e-143">Таким образом, можно получить значения ошибок, которые относятся к **вызову SetProps** с последующими вызовами.</span><span class="sxs-lookup"><span data-stu-id="db06e-143">Therefore, it is possible to receive error values that relate to the **SetProps** call with the later calls.</span></span> 
  
<span data-ttu-id="db06e-144">Если **SetProps** возвращает S_OK, проверьте структуру **SPropProblemArray,** на которая указывает  _lppProblems,_ на проблемы при обновлении отдельных свойств.</span><span class="sxs-lookup"><span data-stu-id="db06e-144">If **SetProps** returns S_OK, check the **SPropProblemArray** structure pointed to by  _lppProblems_ for problems updating individual properties.</span></span> <span data-ttu-id="db06e-145">Если **SetProps** возвращает ошибку, не проверяйте массив проблем свойств.</span><span class="sxs-lookup"><span data-stu-id="db06e-145">If **SetProps** returns an error, do not check the property problem array.</span></span> <span data-ttu-id="db06e-146">Вместо этого вызовите метод [IMAPIProp::GetLastError](imapiprop-getlasterror.md) объекта.</span><span class="sxs-lookup"><span data-stu-id="db06e-146">Instead, call the object's [IMAPIProp::GetLastError](imapiprop-getlasterror.md) method.</span></span> 
  
<span data-ttu-id="db06e-147">При обновлении больших свойств **SetProps** может привести к сбойу и возврату MAPI_E_NOT_ENOUGH_MEMORY.</span><span class="sxs-lookup"><span data-stu-id="db06e-147">When updating large properties, **SetProps** can fail and return MAPI_E_NOT_ENOUGH_MEMORY.</span></span> <span data-ttu-id="db06e-148">Для свойств не существует максимального размера, и разные объекты могут иметь разные ограничения.</span><span class="sxs-lookup"><span data-stu-id="db06e-148">There is no maximum size for properties, and different objects can have different limits.</span></span> <span data-ttu-id="db06e-149">Если вы имеете дело с потенциально большими свойствами, будьте готовы вызвать метод [IMAPIProp::OpenProperty](imapiprop-openproperty.md) с IID_IStream в качестве идентификатора интерфейса, если **SetProps** возвращает это значение ошибки.</span><span class="sxs-lookup"><span data-stu-id="db06e-149">If you deal with potentially large properties, be prepared to call the [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method with IID_IStream as the interface identifier if **SetProps** returns this error value.</span></span> 
  
<span data-ttu-id="db06e-150">Вызовите [функцию MAPIFreeBuffer,](mapifreebuffer.md) чтобы освободить **структуру SPropProblemArray.**</span><span class="sxs-lookup"><span data-stu-id="db06e-150">Call the [MAPIFreeBuffer](mapifreebuffer.md) function to free the **SPropProblemArray** structure.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="db06e-151">Справочные материалы по MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="db06e-151">MFCMAPI reference</span></span>

<span data-ttu-id="db06e-152">Пример кода MFCMAPI указан в приведенной ниже таблице.</span><span class="sxs-lookup"><span data-stu-id="db06e-152">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="db06e-153">**Файл**</span><span class="sxs-lookup"><span data-stu-id="db06e-153">**File**</span></span>|<span data-ttu-id="db06e-154">**Функция**</span><span class="sxs-lookup"><span data-stu-id="db06e-154">**Function**</span></span>|<span data-ttu-id="db06e-155">**Примечание**</span><span class="sxs-lookup"><span data-stu-id="db06e-155">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="db06e-156">PropertyEditor.cpp</span><span class="sxs-lookup"><span data-stu-id="db06e-156">PropertyEditor.cpp</span></span>  <br/> |<span data-ttu-id="db06e-157">CPropertyEditor::WriteSPropValueToObject</span><span class="sxs-lookup"><span data-stu-id="db06e-157">CPropertyEditor::WriteSPropValueToObject</span></span>  <br/> |<span data-ttu-id="db06e-158">MFCMAPI использует метод **IMAPIProp::SetProps** для записи свойства обратно в объект после изменения свойства.</span><span class="sxs-lookup"><span data-stu-id="db06e-158">MFCMAPI uses the **IMAPIProp::SetProps** method to write a property back to an object after the property has been edited.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="db06e-159">См. также</span><span class="sxs-lookup"><span data-stu-id="db06e-159">See also</span></span>



[<span data-ttu-id="db06e-160">IMAPIProp::GetLastError</span><span class="sxs-lookup"><span data-stu-id="db06e-160">IMAPIProp::GetLastError</span></span>](imapiprop-getlasterror.md)
  
[<span data-ttu-id="db06e-161">IMAPIProp::GetProps</span><span class="sxs-lookup"><span data-stu-id="db06e-161">IMAPIProp::GetProps</span></span>](imapiprop-getprops.md)
  
[<span data-ttu-id="db06e-162">IMAPIProp::OpenProperty</span><span class="sxs-lookup"><span data-stu-id="db06e-162">IMAPIProp::OpenProperty</span></span>](imapiprop-openproperty.md)
  
[<span data-ttu-id="db06e-163">IMAPIProp::SaveChanges</span><span class="sxs-lookup"><span data-stu-id="db06e-163">IMAPIProp::SaveChanges</span></span>](imapiprop-savechanges.md)
  
[<span data-ttu-id="db06e-164">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="db06e-164">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="db06e-165">SPropProblemArray</span><span class="sxs-lookup"><span data-stu-id="db06e-165">SPropProblemArray</span></span>](spropproblemarray.md)
  
[<span data-ttu-id="db06e-166">SPropValue</span><span class="sxs-lookup"><span data-stu-id="db06e-166">SPropValue</span></span>](spropvalue.md)
  
[<span data-ttu-id="db06e-167">IMAPIProp : IUnknown</span><span class="sxs-lookup"><span data-stu-id="db06e-167">IMAPIProp : IUnknown</span></span>](imapipropiunknown.md)

