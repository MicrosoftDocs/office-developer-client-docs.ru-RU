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
ms.openlocfilehash: 93bfcce9c45a4c6fd4d57be8c1222be286e0a945
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22592033"
---
# <a name="imapipropsetprops"></a><span data-ttu-id="0e19f-103">IMAPIProp::SetProps</span><span class="sxs-lookup"><span data-stu-id="0e19f-103">IMAPIProp::SetProps</span></span>

  
  
<span data-ttu-id="0e19f-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0e19f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0e19f-105">Обновление одного или нескольких свойств.</span><span class="sxs-lookup"><span data-stu-id="0e19f-105">Updates one or more properties.</span></span>
  
```cpp
HRESULT SetProps(
  ULONG cValues,
  LPSPropValue lpPropArray,
  LPSPropProblemArray FAR * lppProblems
);
```

## <a name="parameters"></a><span data-ttu-id="0e19f-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="0e19f-106">Parameters</span></span>

 <span data-ttu-id="0e19f-107">_cValues_</span><span class="sxs-lookup"><span data-stu-id="0e19f-107">_cValues_</span></span>
  
> <span data-ttu-id="0e19f-108">[in] Количество значений свойств, на который указывает параметр _lpPropArray_ .</span><span class="sxs-lookup"><span data-stu-id="0e19f-108">[in] The count of property values pointed to by the  _lpPropArray_ parameter.</span></span> <span data-ttu-id="0e19f-109">Параметр _cValues_ не должен иметь значение 0.</span><span class="sxs-lookup"><span data-stu-id="0e19f-109">The  _cValues_ parameter must not be 0.</span></span> 
    
 <span data-ttu-id="0e19f-110">_lpPropArray_</span><span class="sxs-lookup"><span data-stu-id="0e19f-110">_lpPropArray_</span></span>
  
> <span data-ttu-id="0e19f-111">[in] Указатель на массив структур [SPropValue](spropvalue.md) , которые содержат значения свойств, который требуется обновить.</span><span class="sxs-lookup"><span data-stu-id="0e19f-111">[in] A pointer to an array of [SPropValue](spropvalue.md) structures that contain property values to be updated.</span></span> 
    
 <span data-ttu-id="0e19f-112">_lppProblems_</span><span class="sxs-lookup"><span data-stu-id="0e19f-112">_lppProblems_</span></span>
  
> <span data-ttu-id="0e19f-113">[in, out] На входе указатель указатель на структуру [SPropProblemArray](spropproblemarray.md) ; в противном случае — значение NULL, указывающее, не требуется выполнять сведения об ошибке.</span><span class="sxs-lookup"><span data-stu-id="0e19f-113">[in, out] On input, a pointer to a pointer to an [SPropProblemArray](spropproblemarray.md) structure; otherwise, NULL, indicating no need for error information.</span></span> <span data-ttu-id="0e19f-114">Если _lppProblems_ допустимый указатель на входные данные, **SetProps** возвращает подробные сведения об ошибках при обновлении одного или нескольких свойств.</span><span class="sxs-lookup"><span data-stu-id="0e19f-114">If  _lppProblems_ is a valid pointer on input, **SetProps** returns detailed information about errors in updating one or more properties.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="0e19f-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="0e19f-115">Return value</span></span>

<span data-ttu-id="0e19f-116">S_OK</span><span class="sxs-lookup"><span data-stu-id="0e19f-116">S_OK</span></span> 
  
> <span data-ttu-id="0e19f-117">Свойства были успешно обновлены.</span><span class="sxs-lookup"><span data-stu-id="0e19f-117">The properties were successfully updated.</span></span>
    
<span data-ttu-id="0e19f-118">Возможные значения могут быть возвращены в структуре **SPropProblemArray** , но не как возвращаемые значения для **SetProps**:</span><span class="sxs-lookup"><span data-stu-id="0e19f-118">The following values can be returned in the **SPropProblemArray** structure, but not as return values for **SetProps**:</span></span>
  
<span data-ttu-id="0e19f-119">MAPI_E_BAD_CHARWIDTH</span><span class="sxs-lookup"><span data-stu-id="0e19f-119">MAPI_E_BAD_CHARWIDTH</span></span> 
  
> <span data-ttu-id="0e19f-120">Либо был установлен флажок MAPI_UNICODE и реализация не поддерживает Юникод, или MAPI_UNICODE не было установлено и реализация поддерживает только Юникод.</span><span class="sxs-lookup"><span data-stu-id="0e19f-120">Either the MAPI_UNICODE flag was set and the implementation does not support Unicode, or MAPI_UNICODE was not set and the implementation supports only Unicode.</span></span>
    
<span data-ttu-id="0e19f-121">MAPI_E_COMPUTED</span><span class="sxs-lookup"><span data-stu-id="0e19f-121">MAPI_E_COMPUTED</span></span> 
  
> <span data-ttu-id="0e19f-122">Свойство не может быть обновлен, поскольку он доступен только для чтения, вычисленный с поставщиком, который несет ответственность за объект.</span><span class="sxs-lookup"><span data-stu-id="0e19f-122">The property cannot be updated because it is read-only, computed by the service provider that is responsible for the object.</span></span>
    
<span data-ttu-id="0e19f-123">MAPI_E_INVALID_TYPE</span><span class="sxs-lookup"><span data-stu-id="0e19f-123">MAPI_E_INVALID_TYPE</span></span> 
  
> <span data-ttu-id="0e19f-124">Недопустимый тип свойства.</span><span class="sxs-lookup"><span data-stu-id="0e19f-124">The property type is invalid.</span></span>
    
<span data-ttu-id="0e19f-125">MAPI_E_NO_ACCESS</span><span class="sxs-lookup"><span data-stu-id="0e19f-125">MAPI_E_NO_ACCESS</span></span> 
  
> <span data-ttu-id="0e19f-126">Предпринята попытка изменения объекта только для чтения или для доступа к объекту, для которого пользователь имеет недостаточно разрешений.</span><span class="sxs-lookup"><span data-stu-id="0e19f-126">An attempt was made to modify a read-only object or to access an object for which the user has insufficient permissions.</span></span>
    
<span data-ttu-id="0e19f-127">MAPI_E_NOT_ENOUGH_MEMORY</span><span class="sxs-lookup"><span data-stu-id="0e19f-127">MAPI_E_NOT_ENOUGH_MEMORY</span></span> 
  
> <span data-ttu-id="0e19f-128">Не удается обновить свойство, так как они больше, чем размер буфера удаленного вызова (RPC).</span><span class="sxs-lookup"><span data-stu-id="0e19f-128">The property cannot be updated because it is larger than the remote procedure call (RPC) buffer size.</span></span>
    
<span data-ttu-id="0e19f-129">MAPI_E_UNEXPECTED_TYPE</span><span class="sxs-lookup"><span data-stu-id="0e19f-129">MAPI_E_UNEXPECTED_TYPE</span></span> 
  
> <span data-ttu-id="0e19f-130">Тип свойства не типа, вызывающий реализации.</span><span class="sxs-lookup"><span data-stu-id="0e19f-130">The property type is not the type expected by the calling implementation.</span></span>
    
## <a name="notes-to-implementers"></a><span data-ttu-id="0e19f-131">Примечания для реализующих</span><span class="sxs-lookup"><span data-stu-id="0e19f-131">Notes to implementers</span></span>

<span data-ttu-id="0e19f-132">Игнорируйте все свойства с типом **PT_ERROR**и тег свойства **PR_NULL** ([PidTagNull](pidtagnull-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="0e19f-132">Ignore the **PR_NULL** ([PidTagNull](pidtagnull-canonical-property.md)) property tag and all properties with a type of **PT_ERROR**.</span></span> <span data-ttu-id="0e19f-133">Не вносить изменения или отправки отчетов о проблемах в структуре **SPropProblemArray** .</span><span class="sxs-lookup"><span data-stu-id="0e19f-133">Do not make changes or report problems in the **SPropProblemArray** structure.</span></span> 
  
<span data-ttu-id="0e19f-134">Возвращает MAPI_E_INVALID_PARAMETER, если свойство типа **PT_OBJECT** включен в массиве значение свойства.</span><span class="sxs-lookup"><span data-stu-id="0e19f-134">Return MAPI_E_INVALID_PARAMETER if a property of type **PT_OBJECT** is included in the property value array.</span></span> <span data-ttu-id="0e19f-135">Также возвращает эту ошибку, если свойство несколько значений входит в массиве и его элементом **cValues** имеет значение 0.</span><span class="sxs-lookup"><span data-stu-id="0e19f-135">Also return this error if a multiple-value property is included in the array and its **cValues** member is set to 0.</span></span> 
  
<span data-ttu-id="0e19f-136">Если звонок успешно в целом, но существуют проблемы с указанием некоторые свойства, возвращает значение S_OK и поместить сведения о проблемах в соответствии структуры **SPropProblemArray** , параметр _lppProblems_ .</span><span class="sxs-lookup"><span data-stu-id="0e19f-136">If the call succeeds overall but there are problems with setting some of the properties, return S_OK and put information about the problems in the appropriate entry of the **SPropProblemArray** structure that the  _lppProblems_ parameter points to.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="0e19f-137">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="0e19f-137">Notes to callers</span></span>

<span data-ttu-id="0e19f-138">В зависимости от поставщика услуг может быть возможность изменить тип свойства, передав свойство тега, содержащего другого типа, не использовался ранее с идентификатором данного свойства.</span><span class="sxs-lookup"><span data-stu-id="0e19f-138">Depending on the service provider, you might also be able to change the property type by passing a property tag that contains a different type than was previously used with a given property identifier.</span></span>
  
<span data-ttu-id="0e19f-139">Если включить тег свойства для свойства, которое не поддерживается объектом и реализации **SetProps** позволяет создавать новые свойства, свойство добавлен в объект.</span><span class="sxs-lookup"><span data-stu-id="0e19f-139">If you include a property tag for a property that is unsupported by the object and the implementation of **SetProps** allows the creation of new properties, the property is added to the object.</span></span> <span data-ttu-id="0e19f-140">Предыдущее значение хранятся с идентификатором свойства, который использовался для нового свойства удаляются.</span><span class="sxs-lookup"><span data-stu-id="0e19f-140">Any previous value stored with the property identifier that was used for the new property is discarded.</span></span> 
  
<span data-ttu-id="0e19f-141">Обратите внимание на то, что значение, возвращаемое значение S_OK не гарантирует, что все свойства были успешно обновлены.</span><span class="sxs-lookup"><span data-stu-id="0e19f-141">Note that the S_OK return value does not guarantee that all of the properties were successfully updated.</span></span> <span data-ttu-id="0e19f-142">Некоторые поставщики кэширование **SetProps** вызовы, пока они получают звонок, который требует вмешательства поставщика, например [IMAPIProp::SaveChanges](imapiprop-savechanges.md) или [IMAPIProp::GetProps](imapiprop-getprops.md).</span><span class="sxs-lookup"><span data-stu-id="0e19f-142">Some providers cache **SetProps** calls until they receive a call that requires provider intervention, such as [IMAPIProp::SaveChanges](imapiprop-savechanges.md) or [IMAPIProp::GetProps](imapiprop-getprops.md).</span></span> <span data-ttu-id="0e19f-143">Таким образом можно получать значения ошибок, имеющих отношение к звонку **SetProps** со звонками более поздней версии.</span><span class="sxs-lookup"><span data-stu-id="0e19f-143">Therefore, it is possible to receive error values that relate to the **SetProps** call with the later calls.</span></span> 
  
<span data-ttu-id="0e19f-144">Если **SetProps** возвращает значение S_OK, проверьте **SPropProblemArray** структуры, на который указывает _lppProblems_ для проблем в процессе обновления отдельных свойств.</span><span class="sxs-lookup"><span data-stu-id="0e19f-144">If **SetProps** returns S_OK, check the **SPropProblemArray** structure pointed to by  _lppProblems_ for problems updating individual properties.</span></span> <span data-ttu-id="0e19f-145">Если **SetProps** возвращает ошибку, не устанавливайте массива свойства проблемы.</span><span class="sxs-lookup"><span data-stu-id="0e19f-145">If **SetProps** returns an error, do not check the property problem array.</span></span> <span data-ttu-id="0e19f-146">Вместо этого вызов метода [IMAPIProp::GetLastError](imapiprop-getlasterror.md) объекта.</span><span class="sxs-lookup"><span data-stu-id="0e19f-146">Instead, call the object's [IMAPIProp::GetLastError](imapiprop-getlasterror.md) method.</span></span> 
  
<span data-ttu-id="0e19f-147">При обновлении большого свойств, **SetProps** может давать сбой и возвращать MAPI_E_NOT_ENOUGH_MEMORY.</span><span class="sxs-lookup"><span data-stu-id="0e19f-147">When updating large properties, **SetProps** can fail and return MAPI_E_NOT_ENOUGH_MEMORY.</span></span> <span data-ttu-id="0e19f-148">Максимальный размер для свойства не и разных объектов могут иметь разные ограничения.</span><span class="sxs-lookup"><span data-stu-id="0e19f-148">There is no maximum size for properties, and different objects can have different limits.</span></span> <span data-ttu-id="0e19f-149">При работе с потенциально большого свойства быть подготовлен для вызова метода [IMAPIProp::OpenProperty](imapiprop-openproperty.md) с IID_IStream идентификатор интерфейса, если **SetProps** возвращает значение этой ошибки.</span><span class="sxs-lookup"><span data-stu-id="0e19f-149">If you deal with potentially large properties, be prepared to call the [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method with IID_IStream as the interface identifier if **SetProps** returns this error value.</span></span> 
  
<span data-ttu-id="0e19f-150">Вызовите функцию [MAPIFreeBuffer](mapifreebuffer.md) , чтобы освободить место на **SPropProblemArray** структуры.</span><span class="sxs-lookup"><span data-stu-id="0e19f-150">Call the [MAPIFreeBuffer](mapifreebuffer.md) function to free the **SPropProblemArray** structure.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="0e19f-151">Справочные материалы по MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="0e19f-151">MFCMAPI reference</span></span>

<span data-ttu-id="0e19f-152">Пример кода MFCMAPI указан в приведенной ниже таблице.</span><span class="sxs-lookup"><span data-stu-id="0e19f-152">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="0e19f-153">**Файл**</span><span class="sxs-lookup"><span data-stu-id="0e19f-153">**File**</span></span>|<span data-ttu-id="0e19f-154">**Функция**</span><span class="sxs-lookup"><span data-stu-id="0e19f-154">**Function**</span></span>|<span data-ttu-id="0e19f-155">**Примечание**</span><span class="sxs-lookup"><span data-stu-id="0e19f-155">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="0e19f-156">PropertyEditor.cpp</span><span class="sxs-lookup"><span data-stu-id="0e19f-156">PropertyEditor.cpp</span></span>  <br/> |<span data-ttu-id="0e19f-157">CPropertyEditor::WriteSPropValueToObject</span><span class="sxs-lookup"><span data-stu-id="0e19f-157">CPropertyEditor::WriteSPropValueToObject</span></span>  <br/> |<span data-ttu-id="0e19f-158">Mfcmapi (en) использует метод **IMAPIProp::SetProps** для обратной записи свойства объекта после изменения свойства.</span><span class="sxs-lookup"><span data-stu-id="0e19f-158">MFCMAPI uses the **IMAPIProp::SetProps** method to write a property back to an object after the property has been edited.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="0e19f-159">См. также</span><span class="sxs-lookup"><span data-stu-id="0e19f-159">See also</span></span>



[<span data-ttu-id="0e19f-160">IMAPIProp::GetLastError</span><span class="sxs-lookup"><span data-stu-id="0e19f-160">IMAPIProp::GetLastError</span></span>](imapiprop-getlasterror.md)
  
[<span data-ttu-id="0e19f-161">IMAPIProp::GetProps</span><span class="sxs-lookup"><span data-stu-id="0e19f-161">IMAPIProp::GetProps</span></span>](imapiprop-getprops.md)
  
[<span data-ttu-id="0e19f-162">IMAPIProp::OpenProperty</span><span class="sxs-lookup"><span data-stu-id="0e19f-162">IMAPIProp::OpenProperty</span></span>](imapiprop-openproperty.md)
  
[<span data-ttu-id="0e19f-163">IMAPIProp::SaveChanges</span><span class="sxs-lookup"><span data-stu-id="0e19f-163">IMAPIProp::SaveChanges</span></span>](imapiprop-savechanges.md)
  
[<span data-ttu-id="0e19f-164">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="0e19f-164">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="0e19f-165">SPropProblemArray</span><span class="sxs-lookup"><span data-stu-id="0e19f-165">SPropProblemArray</span></span>](spropproblemarray.md)
  
[<span data-ttu-id="0e19f-166">SPropValue</span><span class="sxs-lookup"><span data-stu-id="0e19f-166">SPropValue</span></span>](spropvalue.md)
  
[<span data-ttu-id="0e19f-167">IMAPIProp : IUnknown</span><span class="sxs-lookup"><span data-stu-id="0e19f-167">IMAPIProp : IUnknown</span></span>](imapipropiunknown.md)

