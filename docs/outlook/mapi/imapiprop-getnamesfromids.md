---
title: IMAPIPropGetNamesFromIDs
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIProp.GetNamesFromIDs
api_type:
- COM
ms.assetid: 3efa4731-cf32-4a6c-9ba8-d059e58b0d98
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: f6688afde9b36a7722eaaf768f091481c15b7308
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33423575"
---
# <a name="imapipropgetnamesfromids"></a><span data-ttu-id="a7691-103">IMAPIProp::GetNamesFromIDs</span><span class="sxs-lookup"><span data-stu-id="a7691-103">IMAPIProp::GetNamesFromIDs</span></span>

  
  
<span data-ttu-id="a7691-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a7691-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a7691-105">Предоставляет имена свойств, соответствующие одному или более идентификаторам свойств.</span><span class="sxs-lookup"><span data-stu-id="a7691-105">Provides the property names that correspond to one or more property identifiers.</span></span>
  
```cpp
HRESULT GetNamesFromIDs(
  LPSPropTagArray FAR * lppPropTags,
  LPGUID lpPropSetGuid,
  ULONG ulFlags,
  ULONG FAR * lpcPropNames,
  LPMAPINAMEID FAR * FAR * lpppPropNames
);
```

## <a name="parameters"></a><span data-ttu-id="a7691-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="a7691-106">Parameters</span></span>

 <span data-ttu-id="a7691-107">_lppPropTags_</span><span class="sxs-lookup"><span data-stu-id="a7691-107">_lppPropTags_</span></span>
  
> <span data-ttu-id="a7691-108">[in, out] При вводе указатель на [структуру SPropTagArray,](sproptagarray.md) которая содержит массив тегов свойств; в противном случае NULL, указывающее, что должны быть возвращены все имена.</span><span class="sxs-lookup"><span data-stu-id="a7691-108">[in, out] On input, a pointer to an [SPropTagArray](sproptagarray.md) structure that contains an array of property tags; otherwise, NULL, indicating that all names should be returned.</span></span> <span data-ttu-id="a7691-109">Для массива тегов свойств член **cValues** не может быть 0.</span><span class="sxs-lookup"><span data-stu-id="a7691-109">The **cValues** member for the property tag array cannot be 0.</span></span> <span data-ttu-id="a7691-110">Если  _lppPropTags_ является допустимым указателем при вводе, **GetNamesFromIDs** возвращает имена для каждого идентификатора свойства, включенного в массив.</span><span class="sxs-lookup"><span data-stu-id="a7691-110">If  _lppPropTags_ is a valid pointer on input, **GetNamesFromIDs** returns names for each property identifier included in the array.</span></span> 
    
 <span data-ttu-id="a7691-111">_lpPropSetGuid_</span><span class="sxs-lookup"><span data-stu-id="a7691-111">_lpPropSetGuid_</span></span>
  
> <span data-ttu-id="a7691-112">[in] Указатель на guID или структуру [GUID,](guid.md) определяя набор свойств.</span><span class="sxs-lookup"><span data-stu-id="a7691-112">[in] A pointer to a GUID, or [GUID](guid.md) structure, that identifies a property set.</span></span> <span data-ttu-id="a7691-113">Параметр  _lpPropSetGuid_ может указать допустимый набор свойств или иметь NULL.</span><span class="sxs-lookup"><span data-stu-id="a7691-113">The  _lpPropSetGuid_ parameter can point to a valid property set or can be NULL.</span></span> 
    
 <span data-ttu-id="a7691-114">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="a7691-114">_ulFlags_</span></span>
  
> <span data-ttu-id="a7691-115">[in] Битоваяmas флагов, которая указывает тип возвращаемого имени.</span><span class="sxs-lookup"><span data-stu-id="a7691-115">[in] A bitmask of flags that indicates the type of names to be returned.</span></span> <span data-ttu-id="a7691-116">Можно использовать следующие флаги (если установлены оба флага, имена не возвращаются):</span><span class="sxs-lookup"><span data-stu-id="a7691-116">The following flags can be used (if both flags are set, no names will be returned):</span></span>
    
<span data-ttu-id="a7691-117">MAPI_NO_IDS</span><span class="sxs-lookup"><span data-stu-id="a7691-117">MAPI_NO_IDS</span></span> 
  
> <span data-ttu-id="a7691-118">Запросы на возврат только имен, хранимые в строках Юникода.</span><span class="sxs-lookup"><span data-stu-id="a7691-118">Requests that only names stored as Unicode strings be returned.</span></span> 
    
<span data-ttu-id="a7691-119">MAPI_NO_STRINGS</span><span class="sxs-lookup"><span data-stu-id="a7691-119">MAPI_NO_STRINGS</span></span> 
  
> <span data-ttu-id="a7691-120">Запросы, которые возвращаются только имена, хранимые как числимые идентификаторы.</span><span class="sxs-lookup"><span data-stu-id="a7691-120">Requests that only names stored as numeric identifiers be returned.</span></span> 
    
 <span data-ttu-id="a7691-121">_lpcPropNames_</span><span class="sxs-lookup"><span data-stu-id="a7691-121">_lpcPropNames_</span></span>
  
> <span data-ttu-id="a7691-122">[out] Указатель на количество указателей имен свойств в массиве, на которые указывает параметр _lppPropNames._</span><span class="sxs-lookup"><span data-stu-id="a7691-122">[out] A pointer to a count of the property name pointers in the array pointed to by the  _lppPropNames_ parameter.</span></span> 
    
 <span data-ttu-id="a7691-123">_lpppPropNames_</span><span class="sxs-lookup"><span data-stu-id="a7691-123">_lpppPropNames_</span></span>
  
> <span data-ttu-id="a7691-124">[out] Указатель на массив указателей на структуры [MAPINAMEID,](mapinameid.md) содержащий имена свойств.</span><span class="sxs-lookup"><span data-stu-id="a7691-124">[out] A pointer to an array of pointers to [MAPINAMEID](mapinameid.md) structures that contains property names.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="a7691-125">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="a7691-125">Return value</span></span>

<span data-ttu-id="a7691-126">S_OK</span><span class="sxs-lookup"><span data-stu-id="a7691-126">S_OK</span></span> 
  
> <span data-ttu-id="a7691-127">Имена свойств были успешно возвращены.</span><span class="sxs-lookup"><span data-stu-id="a7691-127">The property names were successfully returned.</span></span> 
    
<span data-ttu-id="a7691-128">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="a7691-128">MAPI_E_NO_SUPPORT</span></span> 
  
> <span data-ttu-id="a7691-129">Объект не поддерживает именуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="a7691-129">The object does not support named properties.</span></span> 
    
<span data-ttu-id="a7691-130">MAPI_W_ERRORS_RETURNED</span><span class="sxs-lookup"><span data-stu-id="a7691-130">MAPI_W_ERRORS_RETURNED</span></span> 
  
> <span data-ttu-id="a7691-131">Вызов в целом был успешным, но не удалось вернуть имена одного или более свойств.</span><span class="sxs-lookup"><span data-stu-id="a7691-131">The call succeeded overall, but names for one or more properties could not be returned.</span></span> <span data-ttu-id="a7691-132">Теги свойств для сбойных свойств имеют тип свойства **PT_ERROR**.</span><span class="sxs-lookup"><span data-stu-id="a7691-132">The property tags for the failing properties have a property type of **PT_ERROR**.</span></span> <span data-ttu-id="a7691-133">При возврате этого предупреждения вызов должен быть обработан как успешный.</span><span class="sxs-lookup"><span data-stu-id="a7691-133">When this warning is returned, the call should be handled as successful.</span></span> <span data-ttu-id="a7691-134">Чтобы проверить это предупреждение, используйте **макрос HR_FAILED.**</span><span class="sxs-lookup"><span data-stu-id="a7691-134">To test for this warning, use the **HR_FAILED** macro.</span></span> <span data-ttu-id="a7691-135">Дополнительные сведения см. в [теме "Использование макроса для обработки ошибок".](using-macros-for-error-handling.md)</span><span class="sxs-lookup"><span data-stu-id="a7691-135">For more information, see [Using Macros for Error Handling](using-macros-for-error-handling.md).</span></span> 
    
<span data-ttu-id="a7691-136">MAPI_E_INVALID_PARAMETER</span><span class="sxs-lookup"><span data-stu-id="a7691-136">MAPI_E_INVALID_PARAMETER</span></span> 
  
> <span data-ttu-id="a7691-137">Для **члена cValues** одной или более записей в массиве тегов свойств, на которые указывает  _lppPropTags,_ установлено 0.</span><span class="sxs-lookup"><span data-stu-id="a7691-137">The **cValues** member of one or more of the entries in the property tag array pointed to by  _lppPropTags_ is set to 0.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="a7691-138">Примечания</span><span class="sxs-lookup"><span data-stu-id="a7691-138">Remarks</span></span>

<span data-ttu-id="a7691-139">Хотя доступ к большинству свойств можно получить по идентификатору свойства, некоторые свойства можно получить по имени.</span><span class="sxs-lookup"><span data-stu-id="a7691-139">While access to most properties is by property identifier, some properties can be accessed by name.</span></span> <span data-ttu-id="a7691-140">Метод **IMAPIProp::GetNamesFromIDs** можно использовать для следующего:</span><span class="sxs-lookup"><span data-stu-id="a7691-140">The **IMAPIProp::GetNamesFromIDs** method can be called to do the following:</span></span> 
  
- <span data-ttu-id="a7691-141">Извлечение имен для определенных идентификаторов свойств в определенном наборе свойств.</span><span class="sxs-lookup"><span data-stu-id="a7691-141">Retrieve names for specific property identifiers in a specific property set.</span></span>
    
- <span data-ttu-id="a7691-142">Извлечение имен для определенных идентификаторов свойств в любом наборе свойств.</span><span class="sxs-lookup"><span data-stu-id="a7691-142">Retrieve names for specific property identifiers in any property set.</span></span>
    
- <span data-ttu-id="a7691-143">Извлекает имена всех именуемой свойства, включенных в сопоставление объекта.</span><span class="sxs-lookup"><span data-stu-id="a7691-143">Retrieve names for all named properties that are included in the object's mapping.</span></span>
    
<span data-ttu-id="a7691-144">Если  _lppPropTags_ указывает на допустимый массив тегов свойств с одним или более идентификаторами свойств, а  _lpPropSetGuid_ указывает на допустимый набор свойств, **GetNamesFromIDs** игнорирует набор свойств и типы свойств и возвращает все имена, которые сопоказают указанным идентификаторам.</span><span class="sxs-lookup"><span data-stu-id="a7691-144">If  _lppPropTags_ points to a valid property tag array with one or more property identifiers, and  _lpPropSetGuid_ points to a valid property set, **GetNamesFromIDs** ignores the property set and the property types and returns all of the names that map to the specified identifiers.</span></span> 
  
<span data-ttu-id="a7691-145">Если  _lppPropTags_ указывает на допустимый массив тегов свойств с одним или более идентификаторами свойств, а  _lpPropSetGuid_ — NULL, **GetNamesFromIDs** возвращает все имена, которые сопоставляются с указанными идентификаторами.</span><span class="sxs-lookup"><span data-stu-id="a7691-145">If  _lppPropTags_ points to a valid property tag array with one or more property identifiers and  _lpPropSetGuid_ is NULL, **GetNamesFromIDs** returns all of the names that map to the specified identifiers.</span></span> 
  
<span data-ttu-id="a7691-146">Если у указанного идентификатора нет имени, **GetNamesFromIDs** возвращает NULL в месте этого идентификатора в структуре, возвращаемой  _в lpppPropNames,_ а также возвращает MAPI_W_ERRORS_RETURNED.</span><span class="sxs-lookup"><span data-stu-id="a7691-146">If a specified identifier does not have a name, **GetNamesFromIDs** returns NULL in that identifier's place in the structure returned in  _lpppPropNames_ and also returns MAPI_W_ERRORS_RETURNED.</span></span> 
  
<span data-ttu-id="a7691-147">Если  _и lpPropSetGuid,_ и  _lppPropTags_ имеют NULL, **GetNamesFromIDs** выделяет новый массив тегов свойств и возвращает все имена всех именовых свойств объекта.</span><span class="sxs-lookup"><span data-stu-id="a7691-147">If both  _lpPropSetGuid_ and  _lppPropTags_ are NULL, **GetNamesFromIDs** allocates a new property tag array and returns all of the names for all of the named properties for the object.</span></span> 
  
<span data-ttu-id="a7691-148">Если имена не возвращаются, например из-за того, что в запрашиваемом наборе свойств нет свойств или все свойства имеют тип, исключенный флагами, **GetNamesFromIDs** делает следующее:</span><span class="sxs-lookup"><span data-stu-id="a7691-148">When there are no names to be returned, perhaps because there are no properties in the requested property set or all of the properties are of a type excluded by the flags, **GetNamesFromIDs** does the following:</span></span> 
  
- <span data-ttu-id="a7691-149">Возвращает S_OK.</span><span class="sxs-lookup"><span data-stu-id="a7691-149">Returns S_OK.</span></span>
    
- <span data-ttu-id="a7691-150">Выделяет новую **структуру SPropTagArray,** устанавливая для члена **cValues** 0.</span><span class="sxs-lookup"><span data-stu-id="a7691-150">Allocates a new **SPropTagArray** structure, setting the **cValues** member to 0.</span></span> 
    
- <span data-ttu-id="a7691-151">Задает для содержимого  _lpcPropNames_ 0.</span><span class="sxs-lookup"><span data-stu-id="a7691-151">Sets the contents of  _lpcPropNames_ to 0.</span></span> 
    
- <span data-ttu-id="a7691-152">Задает для  _содержимого lpppPropNames_ nULL.</span><span class="sxs-lookup"><span data-stu-id="a7691-152">Sets the contents of  _lpppPropNames_ to NULL.</span></span> 
    
## <a name="notes-to-implementers"></a><span data-ttu-id="a7691-153">Примечания для исполнителей</span><span class="sxs-lookup"><span data-stu-id="a7691-153">Notes to implementers</span></span>

<span data-ttu-id="a7691-154">Если  _lpPropSetGuid_ указывает на допустимый набор свойств, а  _lppPropTags_ — на NULL, результат будет неопределенным.</span><span class="sxs-lookup"><span data-stu-id="a7691-154">If  _lpPropSetGuid_ points to a valid property set and  _lppPropTags_ is NULL, the result is undefined.</span></span> <span data-ttu-id="a7691-155">Можно использовать одну из следующих стратегий:</span><span class="sxs-lookup"><span data-stu-id="a7691-155">You can use one of the following strategies:</span></span> 
  
- <span data-ttu-id="a7691-156">Игнорируйте набор свойств и возвращайте имена идентификаторов в массиве тегов свойств.</span><span class="sxs-lookup"><span data-stu-id="a7691-156">Ignore the property set and return the names for the identifiers in the property tag array.</span></span>
    
- <span data-ttu-id="a7691-157">Возвращает имена только идентификаторов в массиве тегов свойств, принадлежащих указанному набору свойств.</span><span class="sxs-lookup"><span data-stu-id="a7691-157">Return the names for only the identifiers in the property tag array that belong to the specified property set.</span></span>
    
- <span data-ttu-id="a7691-158">Сбой вызова, возвращающий MAPI_E_INVALID_PARAMETER.</span><span class="sxs-lookup"><span data-stu-id="a7691-158">Fail the call, returning MAPI_E_INVALID_PARAMETER.</span></span> 
    
## <a name="notes-to-callers"></a><span data-ttu-id="a7691-159">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="a7691-159">Notes to callers</span></span>

<span data-ttu-id="a7691-160">Чтобы получить все именовые свойства объекта, необходимо сначала вызвать метод [IMAPIProp::GetPropList](imapiprop-getproplist.md) объекта, а затем передать возвращенные идентификаторы над диапазоном 0x8000 **getNamesFromIDs**.</span><span class="sxs-lookup"><span data-stu-id="a7691-160">To retrieve all of the named properties for an object, you must first call the object's [IMAPIProp::GetPropList](imapiprop-getproplist.md) method and then pass the returned identifiers that are above the 0x8000 range to **GetNamesFromIDs**.</span></span>
  
<span data-ttu-id="a7691-161">Если вы передаете допустимый набор свойств, но не допустимый массив тегов свойств, будьте готовы к непредсказуемым результатам.</span><span class="sxs-lookup"><span data-stu-id="a7691-161">If you pass a valid property set but not a valid property tag array, be prepared for unpredictable results.</span></span> <span data-ttu-id="a7691-162">Некоторые реализации **GetNamesFromID игнорируют** набор свойств и возвращают имена идентификаторов в массиве тегов свойств.</span><span class="sxs-lookup"><span data-stu-id="a7691-162">Some implementations of **GetNamesFromIDs** ignore the property set and return the names for the identifiers in the property tag array.</span></span> <span data-ttu-id="a7691-163">Некоторые реализации возвращают MAPI_E_INVALID_PARAMETER.</span><span class="sxs-lookup"><span data-stu-id="a7691-163">Some implementations return MAPI_E_INVALID_PARAMETER.</span></span> <span data-ttu-id="a7691-164">Другие реализации возвращают имена идентификаторов всех свойств в наборе свойств.</span><span class="sxs-lookup"><span data-stu-id="a7691-164">Still other implementations return names for identifiers of all properties in the property set.</span></span> <span data-ttu-id="a7691-165">Если набор свойств имеет PS_PUBLIC_STRINGS, **GetNamesFromIDs** может возвращать все имена, которые когда-либо были созданы.</span><span class="sxs-lookup"><span data-stu-id="a7691-165">If the property set is PS_PUBLIC_STRINGS, **GetNamesFromIDs** can return all names that were ever created.</span></span> <span data-ttu-id="a7691-166">Указывает, хранит ли поставщик услуг свойство в идентификаторах, связанных с общедоступными строками, как iдиатериальное.</span><span class="sxs-lookup"><span data-stu-id="a7691-166">Whether the service provider stores a property under the identifiers associated with the public strings is immaterial.</span></span> 
  
<span data-ttu-id="a7691-167">После завершения работы с именами свойств проверьте содержимое параметра  _lpcPropNames,_ чтобы определить, были ли возвращены какие-либо имена.</span><span class="sxs-lookup"><span data-stu-id="a7691-167">When you are finished with the property names, check the contents of the  _lpcPropNames_ parameter to determine whether any names were returned.</span></span> <span data-ttu-id="a7691-168">В этом случае вызовите функцию [MAPIFreeBuffer,](mapifreebuffer.md) чтобы освободить память, на которая указывают  _lppPropTags_ и  _lpppPropNames,_ когда возвращается успешный результат.</span><span class="sxs-lookup"><span data-stu-id="a7691-168">If so, call the [MAPIFreeBuffer](mapifreebuffer.md) function to free the memory pointed to by  _lppPropTags_ and  _lpppPropNames_ when a successful result is returned.</span></span> <span data-ttu-id="a7691-169">Для каждого параметра достаточно одного вызова **MAPIFreeBuffer;** Вам не нужно обходить массив указателей и освободить каждую структуру **MAPINAMEID** по отдельности.</span><span class="sxs-lookup"><span data-stu-id="a7691-169">One call to **MAPIFreeBuffer** is sufficient for each parameter; you do not have to traverse the array of pointers and free each **MAPINAMEID** structure individually.</span></span> 
  
<span data-ttu-id="a7691-170">Дополнительные сведения об именуемом свойстве см. в под названием [MAPI.](mapi-named-properties.md)</span><span class="sxs-lookup"><span data-stu-id="a7691-170">For more information about named properties, see [MAPI Named Properties](mapi-named-properties.md).</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="a7691-171">Справочные материалы по MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="a7691-171">MFCMAPI reference</span></span>

<span data-ttu-id="a7691-172">Пример кода MFCMAPI указан в приведенной ниже таблице.</span><span class="sxs-lookup"><span data-stu-id="a7691-172">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="a7691-173">**Файл**</span><span class="sxs-lookup"><span data-stu-id="a7691-173">**File**</span></span>|<span data-ttu-id="a7691-174">**Функция**</span><span class="sxs-lookup"><span data-stu-id="a7691-174">**Function**</span></span>|<span data-ttu-id="a7691-175">**Примечание**</span><span class="sxs-lookup"><span data-stu-id="a7691-175">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="a7691-176">SingleMAPIPropListCtrl.cpp</span><span class="sxs-lookup"><span data-stu-id="a7691-176">SingleMAPIPropListCtrl.cpp</span></span>  <br/> |<span data-ttu-id="a7691-177">CSingleMAPIPropListCtrl::FindAllNamedProps</span><span class="sxs-lookup"><span data-stu-id="a7691-177">CSingleMAPIPropListCtrl::FindAllNamedProps</span></span>  <br/> |<span data-ttu-id="a7691-178">MFCMAPI использует метод **IMAPIProp::GetNamesFromIDs** для искомого именования свойств, которые были ранее сопощены.</span><span class="sxs-lookup"><span data-stu-id="a7691-178">MFCMAPI uses the **IMAPIProp::GetNamesFromIDs** method to look up named properties that have previously been mapped.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="a7691-179">См. также</span><span class="sxs-lookup"><span data-stu-id="a7691-179">See also</span></span>



[<span data-ttu-id="a7691-180">GUID</span><span class="sxs-lookup"><span data-stu-id="a7691-180">GUID</span></span>](guid.md)
  
[<span data-ttu-id="a7691-181">IMAPIProp::GetIDsFromNames</span><span class="sxs-lookup"><span data-stu-id="a7691-181">IMAPIProp::GetIDsFromNames</span></span>](imapiprop-getidsfromnames.md)
  
[<span data-ttu-id="a7691-182">IMAPIProp::GetPropList</span><span class="sxs-lookup"><span data-stu-id="a7691-182">IMAPIProp::GetPropList</span></span>](imapiprop-getproplist.md)
  
[<span data-ttu-id="a7691-183">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="a7691-183">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="a7691-184">MAPINAMEID</span><span class="sxs-lookup"><span data-stu-id="a7691-184">MAPINAMEID</span></span>](mapinameid.md)
  
[<span data-ttu-id="a7691-185">SPropTagArray</span><span class="sxs-lookup"><span data-stu-id="a7691-185">SPropTagArray</span></span>](sproptagarray.md)
  
[<span data-ttu-id="a7691-186">IMAPIProp : IUnknown</span><span class="sxs-lookup"><span data-stu-id="a7691-186">IMAPIProp : IUnknown</span></span>](imapipropiunknown.md)


[<span data-ttu-id="a7691-187">MFCMAPI как пример кода</span><span class="sxs-lookup"><span data-stu-id="a7691-187">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)
  
[<span data-ttu-id="a7691-188">Именованные свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="a7691-188">MAPI Named Properties</span></span>](mapi-named-properties.md)
  
[<span data-ttu-id="a7691-189">Использование макроса для обработки ошибок</span><span class="sxs-lookup"><span data-stu-id="a7691-189">Using Macros for Error Handling</span></span>](using-macros-for-error-handling.md)

