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
# <a name="imapipropgetnamesfromids"></a><span data-ttu-id="62c8b-103">IMAPIProp::GetNamesFromIDs</span><span class="sxs-lookup"><span data-stu-id="62c8b-103">IMAPIProp::GetNamesFromIDs</span></span>

  
  
<span data-ttu-id="62c8b-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="62c8b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="62c8b-105">Предоставляет имена свойств, соответствующие одному или более идентификаторам свойств.</span><span class="sxs-lookup"><span data-stu-id="62c8b-105">Provides the property names that correspond to one or more property identifiers.</span></span>
  
```cpp
HRESULT GetNamesFromIDs(
  LPSPropTagArray FAR * lppPropTags,
  LPGUID lpPropSetGuid,
  ULONG ulFlags,
  ULONG FAR * lpcPropNames,
  LPMAPINAMEID FAR * FAR * lpppPropNames
);
```

## <a name="parameters"></a><span data-ttu-id="62c8b-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="62c8b-106">Parameters</span></span>

 <span data-ttu-id="62c8b-107">_lppPropTags_</span><span class="sxs-lookup"><span data-stu-id="62c8b-107">_lppPropTags_</span></span>
  
> <span data-ttu-id="62c8b-108">[in, out] На входе указатель на [структуру SPropTagArray,](sproptagarray.md) содержаную массив тегов свойств; в противном случае NULL указывает, что все имена должны быть возвращены.</span><span class="sxs-lookup"><span data-stu-id="62c8b-108">[in, out] On input, a pointer to an [SPropTagArray](sproptagarray.md) structure that contains an array of property tags; otherwise, NULL, indicating that all names should be returned.</span></span> <span data-ttu-id="62c8b-109">Член **cValues для** массива тегов свойств не может быть 0.</span><span class="sxs-lookup"><span data-stu-id="62c8b-109">The **cValues** member for the property tag array cannot be 0.</span></span> <span data-ttu-id="62c8b-110">Если  _lppPropTags_ является допустимым указателем на входе, **GetNamesFromID возвращает** имена для каждого идентификатора свойства, включенного в массив.</span><span class="sxs-lookup"><span data-stu-id="62c8b-110">If  _lppPropTags_ is a valid pointer on input, **GetNamesFromIDs** returns names for each property identifier included in the array.</span></span> 
    
 <span data-ttu-id="62c8b-111">_lpPropSetGuid_</span><span class="sxs-lookup"><span data-stu-id="62c8b-111">_lpPropSetGuid_</span></span>
  
> <span data-ttu-id="62c8b-112">[in] Указатель на структуру GUID или [GUID,](guid.md) которая определяет набор свойств.</span><span class="sxs-lookup"><span data-stu-id="62c8b-112">[in] A pointer to a GUID, or [GUID](guid.md) structure, that identifies a property set.</span></span> <span data-ttu-id="62c8b-113">Параметр  _lpPropSetGuid может_ указать на допустимый набор свойств или может быть NULL.</span><span class="sxs-lookup"><span data-stu-id="62c8b-113">The  _lpPropSetGuid_ parameter can point to a valid property set or can be NULL.</span></span> 
    
 <span data-ttu-id="62c8b-114">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="62c8b-114">_ulFlags_</span></span>
  
> <span data-ttu-id="62c8b-115">[in] Битмашка флагов, которая указывает тип имен, которые должны быть возвращены.</span><span class="sxs-lookup"><span data-stu-id="62c8b-115">[in] A bitmask of flags that indicates the type of names to be returned.</span></span> <span data-ttu-id="62c8b-116">Можно использовать следующие флаги (если оба флага установлены, имена не возвращаются):</span><span class="sxs-lookup"><span data-stu-id="62c8b-116">The following flags can be used (if both flags are set, no names will be returned):</span></span>
    
<span data-ttu-id="62c8b-117">MAPI_NO_IDS</span><span class="sxs-lookup"><span data-stu-id="62c8b-117">MAPI_NO_IDS</span></span> 
  
> <span data-ttu-id="62c8b-118">Возвращаются запросы, в которых возвращаются только имена, хранимые как строки Юникод.</span><span class="sxs-lookup"><span data-stu-id="62c8b-118">Requests that only names stored as Unicode strings be returned.</span></span> 
    
<span data-ttu-id="62c8b-119">MAPI_NO_STRINGS</span><span class="sxs-lookup"><span data-stu-id="62c8b-119">MAPI_NO_STRINGS</span></span> 
  
> <span data-ttu-id="62c8b-120">Возвращаются запросы, в которых возвращаются только имена, хранимые в качестве числимые идентификаторы.</span><span class="sxs-lookup"><span data-stu-id="62c8b-120">Requests that only names stored as numeric identifiers be returned.</span></span> 
    
 <span data-ttu-id="62c8b-121">_lpcPropNames_</span><span class="sxs-lookup"><span data-stu-id="62c8b-121">_lpcPropNames_</span></span>
  
> <span data-ttu-id="62c8b-122">[вышел] Указатель на количество указателей имен свойств в массиве, на который указывает параметр _lppPropNames._</span><span class="sxs-lookup"><span data-stu-id="62c8b-122">[out] A pointer to a count of the property name pointers in the array pointed to by the  _lppPropNames_ parameter.</span></span> 
    
 <span data-ttu-id="62c8b-123">_lpppPropNames_</span><span class="sxs-lookup"><span data-stu-id="62c8b-123">_lpppPropNames_</span></span>
  
> <span data-ttu-id="62c8b-124">[вышел] Указатель на массив указателей для [структур MAPINAMEID,](mapinameid.md) которые содержат имена свойств.</span><span class="sxs-lookup"><span data-stu-id="62c8b-124">[out] A pointer to an array of pointers to [MAPINAMEID](mapinameid.md) structures that contains property names.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="62c8b-125">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="62c8b-125">Return value</span></span>

<span data-ttu-id="62c8b-126">S_OK</span><span class="sxs-lookup"><span data-stu-id="62c8b-126">S_OK</span></span> 
  
> <span data-ttu-id="62c8b-127">Имена свойств были успешно возвращены.</span><span class="sxs-lookup"><span data-stu-id="62c8b-127">The property names were successfully returned.</span></span> 
    
<span data-ttu-id="62c8b-128">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="62c8b-128">MAPI_E_NO_SUPPORT</span></span> 
  
> <span data-ttu-id="62c8b-129">Объект не поддерживает именимые свойства.</span><span class="sxs-lookup"><span data-stu-id="62c8b-129">The object does not support named properties.</span></span> 
    
<span data-ttu-id="62c8b-130">MAPI_W_ERRORS_RETURNED</span><span class="sxs-lookup"><span data-stu-id="62c8b-130">MAPI_W_ERRORS_RETURNED</span></span> 
  
> <span data-ttu-id="62c8b-131">Вызов удался в целом, но имена одного или более свойств не удалось вернуть.</span><span class="sxs-lookup"><span data-stu-id="62c8b-131">The call succeeded overall, but names for one or more properties could not be returned.</span></span> <span data-ttu-id="62c8b-132">Теги свойств для сбоя свойств имеют тип **свойства PT_ERROR**.</span><span class="sxs-lookup"><span data-stu-id="62c8b-132">The property tags for the failing properties have a property type of **PT_ERROR**.</span></span> <span data-ttu-id="62c8b-133">Когда это предупреждение возвращается, вызов должен быть обработан как успешный.</span><span class="sxs-lookup"><span data-stu-id="62c8b-133">When this warning is returned, the call should be handled as successful.</span></span> <span data-ttu-id="62c8b-134">Чтобы проверить это предупреждение, используйте **HR_FAILED** макрос.</span><span class="sxs-lookup"><span data-stu-id="62c8b-134">To test for this warning, use the **HR_FAILED** macro.</span></span> <span data-ttu-id="62c8b-135">Дополнительные сведения см. в [дополнительных сведениях Об использовании макроса для обработки ошибок.](using-macros-for-error-handling.md)</span><span class="sxs-lookup"><span data-stu-id="62c8b-135">For more information, see [Using Macros for Error Handling](using-macros-for-error-handling.md).</span></span> 
    
<span data-ttu-id="62c8b-136">MAPI_E_INVALID_PARAMETER</span><span class="sxs-lookup"><span data-stu-id="62c8b-136">MAPI_E_INVALID_PARAMETER</span></span> 
  
> <span data-ttu-id="62c8b-137">Для **члена cValues** одного или более записей в массиве тегов свойств, на которые указывает  _lppPropTags,_ установлено 0.</span><span class="sxs-lookup"><span data-stu-id="62c8b-137">The **cValues** member of one or more of the entries in the property tag array pointed to by  _lppPropTags_ is set to 0.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="62c8b-138">Примечания</span><span class="sxs-lookup"><span data-stu-id="62c8b-138">Remarks</span></span>

<span data-ttu-id="62c8b-139">Хотя доступ к большинству свойств определяется идентификатором свойств, некоторые свойства можно получить по имени.</span><span class="sxs-lookup"><span data-stu-id="62c8b-139">While access to most properties is by property identifier, some properties can be accessed by name.</span></span> <span data-ttu-id="62c8b-140">Метод **IMAPIProp::GetNamesFromIDs** можно назвать следующим образом:</span><span class="sxs-lookup"><span data-stu-id="62c8b-140">The **IMAPIProp::GetNamesFromIDs** method can be called to do the following:</span></span> 
  
- <span data-ttu-id="62c8b-141">Извлечение имен для определенных идентификаторов свойств в определенном наборе свойств.</span><span class="sxs-lookup"><span data-stu-id="62c8b-141">Retrieve names for specific property identifiers in a specific property set.</span></span>
    
- <span data-ttu-id="62c8b-142">Извлечение имен для определенных идентификаторов свойств в любом наборе свойств.</span><span class="sxs-lookup"><span data-stu-id="62c8b-142">Retrieve names for specific property identifiers in any property set.</span></span>
    
- <span data-ttu-id="62c8b-143">Извлечение имен для всех названных свойств, включенных в сопоставление объекта.</span><span class="sxs-lookup"><span data-stu-id="62c8b-143">Retrieve names for all named properties that are included in the object's mapping.</span></span>
    
<span data-ttu-id="62c8b-144">Если  _lppPropTags_ указывает на допустимый массив тегов свойств с одним или более идентификаторами свойств, а  _lpPropSetGuid_ указывает на допустимый набор свойств, **getNamesFromIDs** игнорирует набор свойств и типы свойств и возвращает все имена, которые намечают указанные идентификаторы.</span><span class="sxs-lookup"><span data-stu-id="62c8b-144">If  _lppPropTags_ points to a valid property tag array with one or more property identifiers, and  _lpPropSetGuid_ points to a valid property set, **GetNamesFromIDs** ignores the property set and the property types and returns all of the names that map to the specified identifiers.</span></span> 
  
<span data-ttu-id="62c8b-145">Если  _lppPropTags_ указывает на допустимый массив тегов свойств с одним или более идентификаторами свойств, а  _lpPropSetGuid_ — NULL, **GetNamesFromIDs** возвращает все имена, которые отбираются в указанные идентификаторы.</span><span class="sxs-lookup"><span data-stu-id="62c8b-145">If  _lppPropTags_ points to a valid property tag array with one or more property identifiers and  _lpPropSetGuid_ is NULL, **GetNamesFromIDs** returns all of the names that map to the specified identifiers.</span></span> 
  
<span data-ttu-id="62c8b-146">Если у указанного идентификатора нет имени, **GetNamesFromIDs** возвращает NULL в месте этого идентификатора в структуре, возвращаемой в  _lpppPropNames,_ а также возвращает MAPI_W_ERRORS_RETURNED.</span><span class="sxs-lookup"><span data-stu-id="62c8b-146">If a specified identifier does not have a name, **GetNamesFromIDs** returns NULL in that identifier's place in the structure returned in  _lpppPropNames_ and also returns MAPI_W_ERRORS_RETURNED.</span></span> 
  
<span data-ttu-id="62c8b-147">Если  _оба lpPropSetGuid_ и  _lppPropTags_ являются NULL, **GetNamesFromIDs** выделяет новый массив тегов свойств и возвращает все имена для всех названных свойств объекта.</span><span class="sxs-lookup"><span data-stu-id="62c8b-147">If both  _lpPropSetGuid_ and  _lppPropTags_ are NULL, **GetNamesFromIDs** allocates a new property tag array and returns all of the names for all of the named properties for the object.</span></span> 
  
<span data-ttu-id="62c8b-148">Если в наборе запрашиваемого свойства нет имен, возможно, из-за того, что в запрашиваемом наборе свойств нет свойств или все свойства имеют тип, исключаемый флагами, **GetNamesFromIDs** делает следующее:</span><span class="sxs-lookup"><span data-stu-id="62c8b-148">When there are no names to be returned, perhaps because there are no properties in the requested property set or all of the properties are of a type excluded by the flags, **GetNamesFromIDs** does the following:</span></span> 
  
- <span data-ttu-id="62c8b-149">Возвращает S_OK.</span><span class="sxs-lookup"><span data-stu-id="62c8b-149">Returns S_OK.</span></span>
    
- <span data-ttu-id="62c8b-150">Выделяет новую **структуру SPropTagArray,** установив для **члена cValues** 0.</span><span class="sxs-lookup"><span data-stu-id="62c8b-150">Allocates a new **SPropTagArray** structure, setting the **cValues** member to 0.</span></span> 
    
- <span data-ttu-id="62c8b-151">Задает содержимое  _lpcPropNames_ до 0.</span><span class="sxs-lookup"><span data-stu-id="62c8b-151">Sets the contents of  _lpcPropNames_ to 0.</span></span> 
    
- <span data-ttu-id="62c8b-152">Задает содержимое  _lpppPropNames_ nULL.</span><span class="sxs-lookup"><span data-stu-id="62c8b-152">Sets the contents of  _lpppPropNames_ to NULL.</span></span> 
    
## <a name="notes-to-implementers"></a><span data-ttu-id="62c8b-153">Примечания для исполнителей</span><span class="sxs-lookup"><span data-stu-id="62c8b-153">Notes to implementers</span></span>

<span data-ttu-id="62c8b-154">Если  _lpPropSetGuid_ указывает на допустимый набор свойств,  _а lppPropTags_ — NULL, результат неопределяется.</span><span class="sxs-lookup"><span data-stu-id="62c8b-154">If  _lpPropSetGuid_ points to a valid property set and  _lppPropTags_ is NULL, the result is undefined.</span></span> <span data-ttu-id="62c8b-155">Можно использовать одну из следующих стратегий:</span><span class="sxs-lookup"><span data-stu-id="62c8b-155">You can use one of the following strategies:</span></span> 
  
- <span data-ttu-id="62c8b-156">Игнорируйте набор свойств и возвращайте имена идентификаторов в массиве тегов свойств.</span><span class="sxs-lookup"><span data-stu-id="62c8b-156">Ignore the property set and return the names for the identifiers in the property tag array.</span></span>
    
- <span data-ttu-id="62c8b-157">Возвращаем имена только для идентификаторов в массиве тегов свойств, которые относятся к указанному набору свойств.</span><span class="sxs-lookup"><span data-stu-id="62c8b-157">Return the names for only the identifiers in the property tag array that belong to the specified property set.</span></span>
    
- <span data-ttu-id="62c8b-158">Не удается вызвать, возвращая MAPI_E_INVALID_PARAMETER.</span><span class="sxs-lookup"><span data-stu-id="62c8b-158">Fail the call, returning MAPI_E_INVALID_PARAMETER.</span></span> 
    
## <a name="notes-to-callers"></a><span data-ttu-id="62c8b-159">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="62c8b-159">Notes to callers</span></span>

<span data-ttu-id="62c8b-160">Чтобы получить все названные свойства объекта, сначала необходимо вызвать метод [IMAPIProp::GetPropList](imapiprop-getproplist.md) объекта, а затем передать возвращенные идентификаторы, которые находятся выше 0x8000 диапазона, в **GetNamesFromIDs**.</span><span class="sxs-lookup"><span data-stu-id="62c8b-160">To retrieve all of the named properties for an object, you must first call the object's [IMAPIProp::GetPropList](imapiprop-getproplist.md) method and then pass the returned identifiers that are above the 0x8000 range to **GetNamesFromIDs**.</span></span>
  
<span data-ttu-id="62c8b-161">Если вы передаете допустимый набор свойств, но не допустимый массив тегов свойств, будьте готовы к непредсказуемым результатам.</span><span class="sxs-lookup"><span data-stu-id="62c8b-161">If you pass a valid property set but not a valid property tag array, be prepared for unpredictable results.</span></span> <span data-ttu-id="62c8b-162">Некоторые реализации **GetNamesFromID игнорируют** набор свойств и возвращают имена идентификаторов в массиве тегов свойств.</span><span class="sxs-lookup"><span data-stu-id="62c8b-162">Some implementations of **GetNamesFromIDs** ignore the property set and return the names for the identifiers in the property tag array.</span></span> <span data-ttu-id="62c8b-163">Некоторые реализации возвращают MAPI_E_INVALID_PARAMETER.</span><span class="sxs-lookup"><span data-stu-id="62c8b-163">Some implementations return MAPI_E_INVALID_PARAMETER.</span></span> <span data-ttu-id="62c8b-164">Другие реализации возвращают имена для идентификаторов всех свойств в наборе свойств.</span><span class="sxs-lookup"><span data-stu-id="62c8b-164">Still other implementations return names for identifiers of all properties in the property set.</span></span> <span data-ttu-id="62c8b-165">Если набор свойств PS_PUBLIC_STRINGS, **getNamesFromIDs** может вернуть все созданные имена.</span><span class="sxs-lookup"><span data-stu-id="62c8b-165">If the property set is PS_PUBLIC_STRINGS, **GetNamesFromIDs** can return all names that were ever created.</span></span> <span data-ttu-id="62c8b-166">Сохраняет ли поставщик служб свойство под идентификаторами, связанными с общедоступными строками, несущественно.</span><span class="sxs-lookup"><span data-stu-id="62c8b-166">Whether the service provider stores a property under the identifiers associated with the public strings is immaterial.</span></span> 
  
<span data-ttu-id="62c8b-167">Когда вы закончите с именами свойств, проверьте содержимое параметра  _lpcPropNames,_ чтобы определить, были ли возвращены какие-либо имена.</span><span class="sxs-lookup"><span data-stu-id="62c8b-167">When you are finished with the property names, check the contents of the  _lpcPropNames_ parameter to determine whether any names were returned.</span></span> <span data-ttu-id="62c8b-168">Если это так, позвоните в [функцию MAPIFreeBuffer,](mapifreebuffer.md) чтобы освободить память, на что указывают  _lppPropTags_ и  _lpppPropNames_ при возвращении успешного результата.</span><span class="sxs-lookup"><span data-stu-id="62c8b-168">If so, call the [MAPIFreeBuffer](mapifreebuffer.md) function to free the memory pointed to by  _lppPropTags_ and  _lpppPropNames_ when a successful result is returned.</span></span> <span data-ttu-id="62c8b-169">Для каждого параметра достаточно одного вызова **в MAPIFreeBuffer;** вам не нужно пересекать массив указателей и освободить каждую **структуру MAPINAMEID** по отдельности.</span><span class="sxs-lookup"><span data-stu-id="62c8b-169">One call to **MAPIFreeBuffer** is sufficient for each parameter; you do not have to traverse the array of pointers and free each **MAPINAMEID** structure individually.</span></span> 
  
<span data-ttu-id="62c8b-170">Дополнительные сведения о свойствах с именем см. в [см. в нем MAPI Named Properties.](mapi-named-properties.md)</span><span class="sxs-lookup"><span data-stu-id="62c8b-170">For more information about named properties, see [MAPI Named Properties](mapi-named-properties.md).</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="62c8b-171">Справочные материалы по MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="62c8b-171">MFCMAPI reference</span></span>

<span data-ttu-id="62c8b-172">Пример кода MFCMAPI указан в приведенной ниже таблице.</span><span class="sxs-lookup"><span data-stu-id="62c8b-172">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="62c8b-173">**Файл**</span><span class="sxs-lookup"><span data-stu-id="62c8b-173">**File**</span></span>|<span data-ttu-id="62c8b-174">**Функция**</span><span class="sxs-lookup"><span data-stu-id="62c8b-174">**Function**</span></span>|<span data-ttu-id="62c8b-175">**Примечание**</span><span class="sxs-lookup"><span data-stu-id="62c8b-175">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="62c8b-176">SingleMAPIPropListCtrl.cpp</span><span class="sxs-lookup"><span data-stu-id="62c8b-176">SingleMAPIPropListCtrl.cpp</span></span>  <br/> |<span data-ttu-id="62c8b-177">CSingleMAPIPropListCtrl::FindAllNamedProps</span><span class="sxs-lookup"><span data-stu-id="62c8b-177">CSingleMAPIPropListCtrl::FindAllNamedProps</span></span>  <br/> |<span data-ttu-id="62c8b-178">MFCMAPI использует метод **IMAPIProp::GetNamesFromIDs** для получения именных свойств, которые ранее были на карту.</span><span class="sxs-lookup"><span data-stu-id="62c8b-178">MFCMAPI uses the **IMAPIProp::GetNamesFromIDs** method to look up named properties that have previously been mapped.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="62c8b-179">См. также</span><span class="sxs-lookup"><span data-stu-id="62c8b-179">See also</span></span>



[<span data-ttu-id="62c8b-180">GUID</span><span class="sxs-lookup"><span data-stu-id="62c8b-180">GUID</span></span>](guid.md)
  
[<span data-ttu-id="62c8b-181">IMAPIProp::GetIDsFromNames</span><span class="sxs-lookup"><span data-stu-id="62c8b-181">IMAPIProp::GetIDsFromNames</span></span>](imapiprop-getidsfromnames.md)
  
[<span data-ttu-id="62c8b-182">IMAPIProp::GetPropList</span><span class="sxs-lookup"><span data-stu-id="62c8b-182">IMAPIProp::GetPropList</span></span>](imapiprop-getproplist.md)
  
[<span data-ttu-id="62c8b-183">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="62c8b-183">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="62c8b-184">MAPINAMEID</span><span class="sxs-lookup"><span data-stu-id="62c8b-184">MAPINAMEID</span></span>](mapinameid.md)
  
[<span data-ttu-id="62c8b-185">SPropTagArray</span><span class="sxs-lookup"><span data-stu-id="62c8b-185">SPropTagArray</span></span>](sproptagarray.md)
  
[<span data-ttu-id="62c8b-186">IMAPIProp : IUnknown</span><span class="sxs-lookup"><span data-stu-id="62c8b-186">IMAPIProp : IUnknown</span></span>](imapipropiunknown.md)


[<span data-ttu-id="62c8b-187">MFCMAPI как пример кода</span><span class="sxs-lookup"><span data-stu-id="62c8b-187">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)
  
[<span data-ttu-id="62c8b-188">Именованные свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="62c8b-188">MAPI Named Properties</span></span>](mapi-named-properties.md)
  
[<span data-ttu-id="62c8b-189">Использование макроса для обработки ошибок</span><span class="sxs-lookup"><span data-stu-id="62c8b-189">Using Macros for Error Handling</span></span>](using-macros-for-error-handling.md)

