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
ms.openlocfilehash: 186afd6a80d0ae3ae0a767456e60b2ebaaa579b9
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22574386"
---
# <a name="imapipropgetnamesfromids"></a><span data-ttu-id="675df-103">IMAPIProp::GetNamesFromIDs</span><span class="sxs-lookup"><span data-stu-id="675df-103">IMAPIProp::GetNamesFromIDs</span></span>

  
  
<span data-ttu-id="675df-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="675df-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="675df-105">Содержит имена свойств, которые соответствуют один или несколько идентификаторов свойств.</span><span class="sxs-lookup"><span data-stu-id="675df-105">Provides the property names that correspond to one or more property identifiers.</span></span>
  
```cpp
HRESULT GetNamesFromIDs(
  LPSPropTagArray FAR * lppPropTags,
  LPGUID lpPropSetGuid,
  ULONG ulFlags,
  ULONG FAR * lpcPropNames,
  LPMAPINAMEID FAR * FAR * lpppPropNames
);
```

## <a name="parameters"></a><span data-ttu-id="675df-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="675df-106">Parameters</span></span>

 <span data-ttu-id="675df-107">_lppPropTags_</span><span class="sxs-lookup"><span data-stu-id="675df-107">_lppPropTags_</span></span>
  
> <span data-ttu-id="675df-108">[in, out] На входе указатель на структуру [SPropTagArray](sproptagarray.md) , который содержит массив теги свойства; в противном случае — значение NULL, указывающего на то, что все имена должны быть возвращены.</span><span class="sxs-lookup"><span data-stu-id="675df-108">[in, out] On input, a pointer to an [SPropTagArray](sproptagarray.md) structure that contains an array of property tags; otherwise, NULL, indicating that all names should be returned.</span></span> <span data-ttu-id="675df-109">Элемент **cValues** для массива тега свойства не может быть 0.</span><span class="sxs-lookup"><span data-stu-id="675df-109">The **cValues** member for the property tag array cannot be 0.</span></span> <span data-ttu-id="675df-110">Если _lppPropTags_ допустимый указатель на входные данные, **GetNamesFromIDs** возвращает имена для каждого свойства идентификатора, включенные в массиве.</span><span class="sxs-lookup"><span data-stu-id="675df-110">If  _lppPropTags_ is a valid pointer on input, **GetNamesFromIDs** returns names for each property identifier included in the array.</span></span> 
    
 <span data-ttu-id="675df-111">_lpPropSetGuid_</span><span class="sxs-lookup"><span data-stu-id="675df-111">_lpPropSetGuid_</span></span>
  
> <span data-ttu-id="675df-112">[in] Указатель на идентификатор GUID, или [идентификатор GUID](guid.md) структуры, определяющий набор свойств.</span><span class="sxs-lookup"><span data-stu-id="675df-112">[in] A pointer to a GUID, or [GUID](guid.md) structure, that identifies a property set.</span></span> <span data-ttu-id="675df-113">Параметр _lpPropSetGuid_ можно сопоставить с набором свойство или может быть NULL.</span><span class="sxs-lookup"><span data-stu-id="675df-113">The  _lpPropSetGuid_ parameter can point to a valid property set or can be NULL.</span></span> 
    
 <span data-ttu-id="675df-114">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="675df-114">_ulFlags_</span></span>
  
> <span data-ttu-id="675df-115">[in] Битовая маска флаги, указывающую тип имена которого требуется получить.</span><span class="sxs-lookup"><span data-stu-id="675df-115">[in] A bitmask of flags that indicates the type of names to be returned.</span></span> <span data-ttu-id="675df-116">Можно использовать следующие флаги (если заданы оба флаги, имена не будут возвращены):</span><span class="sxs-lookup"><span data-stu-id="675df-116">The following flags can be used (if both flags are set, no names will be returned):</span></span>
    
<span data-ttu-id="675df-117">MAPI_NO_IDS</span><span class="sxs-lookup"><span data-stu-id="675df-117">MAPI_NO_IDS</span></span> 
  
> <span data-ttu-id="675df-118">Запросы, которые возвращены только имена, сохраненной в качестве строки Юникод.</span><span class="sxs-lookup"><span data-stu-id="675df-118">Requests that only names stored as Unicode strings be returned.</span></span> 
    
<span data-ttu-id="675df-119">MAPI_NO_STRINGS</span><span class="sxs-lookup"><span data-stu-id="675df-119">MAPI_NO_STRINGS</span></span> 
  
> <span data-ttu-id="675df-120">Запросы, которые возвращены только имена, сохраненной в качестве числовых идентификаторов.</span><span class="sxs-lookup"><span data-stu-id="675df-120">Requests that only names stored as numeric identifiers be returned.</span></span> 
    
 <span data-ttu-id="675df-121">_lpcPropNames_</span><span class="sxs-lookup"><span data-stu-id="675df-121">_lpcPropNames_</span></span>
  
> <span data-ttu-id="675df-122">[out] Указатель на число указатели имя свойства в массиве указывает параметр _lppPropNames_ .</span><span class="sxs-lookup"><span data-stu-id="675df-122">[out] A pointer to a count of the property name pointers in the array pointed to by the  _lppPropNames_ parameter.</span></span> 
    
 <span data-ttu-id="675df-123">_lpppPropNames_</span><span class="sxs-lookup"><span data-stu-id="675df-123">_lpppPropNames_</span></span>
  
> <span data-ttu-id="675df-124">[out] Указатель на массив указатели на [MAPINAMEID](mapinameid.md) структуры, содержащий имена свойств.</span><span class="sxs-lookup"><span data-stu-id="675df-124">[out] A pointer to an array of pointers to [MAPINAMEID](mapinameid.md) structures that contains property names.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="675df-125">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="675df-125">Return value</span></span>

<span data-ttu-id="675df-126">S_OK</span><span class="sxs-lookup"><span data-stu-id="675df-126">S_OK</span></span> 
  
> <span data-ttu-id="675df-127">Имена свойств были успешно возвращен.</span><span class="sxs-lookup"><span data-stu-id="675df-127">The property names were successfully returned.</span></span> 
    
<span data-ttu-id="675df-128">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="675df-128">MAPI_E_NO_SUPPORT</span></span> 
  
> <span data-ttu-id="675df-129">Объект не поддерживает именованные свойства.</span><span class="sxs-lookup"><span data-stu-id="675df-129">The object does not support named properties.</span></span> 
    
<span data-ttu-id="675df-130">MAPI_W_ERRORS_RETURNED</span><span class="sxs-lookup"><span data-stu-id="675df-130">MAPI_W_ERRORS_RETURNED</span></span> 
  
> <span data-ttu-id="675df-131">Вызов завершился успешно в целом, но не будут получены имена для одного или нескольких свойств.</span><span class="sxs-lookup"><span data-stu-id="675df-131">The call succeeded overall, but names for one or more properties could not be returned.</span></span> <span data-ttu-id="675df-132">Свойство теги для свойств со сбоями имеют типа свойства **PT_ERROR**.</span><span class="sxs-lookup"><span data-stu-id="675df-132">The property tags for the failing properties have a property type of **PT_ERROR**.</span></span> <span data-ttu-id="675df-133">При возвращении этого предупреждения вызова необходимо обрабатывать об успешном завершении.</span><span class="sxs-lookup"><span data-stu-id="675df-133">When this warning is returned, the call should be handled as successful.</span></span> <span data-ttu-id="675df-134">Чтобы проверить это предупреждение, используйте **HR_FAILED** макрос.</span><span class="sxs-lookup"><span data-stu-id="675df-134">To test for this warning, use the **HR_FAILED** macro.</span></span> <span data-ttu-id="675df-135">Дополнительные сведения можно [С помощью макросов для обработки ошибок](using-macros-for-error-handling.md).</span><span class="sxs-lookup"><span data-stu-id="675df-135">For more information, see [Using Macros for Error Handling](using-macros-for-error-handling.md).</span></span> 
    
<span data-ttu-id="675df-136">MAPI_E_INVALID_PARAMETER</span><span class="sxs-lookup"><span data-stu-id="675df-136">MAPI_E_INVALID_PARAMETER</span></span> 
  
> <span data-ttu-id="675df-137">Член **cValues** одной или нескольких записей в массиве тег свойства, на который указывает _lppPropTags_ имеет значение 0.</span><span class="sxs-lookup"><span data-stu-id="675df-137">The **cValues** member of one or more of the entries in the property tag array pointed to by  _lppPropTags_ is set to 0.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="675df-138">Замечания</span><span class="sxs-lookup"><span data-stu-id="675df-138">Remarks</span></span>

<span data-ttu-id="675df-139">Во время доступа к большинство свойств по идентификатору свойство некоторые свойства может осуществляться по имени.</span><span class="sxs-lookup"><span data-stu-id="675df-139">While access to most properties is by property identifier, some properties can be accessed by name.</span></span> <span data-ttu-id="675df-140">Метод **IMAPIProp::GetNamesFromIDs** может вызываться для выполнения следующих:</span><span class="sxs-lookup"><span data-stu-id="675df-140">The **IMAPIProp::GetNamesFromIDs** method can be called to do the following:</span></span> 
  
- <span data-ttu-id="675df-141">Извлечение имен идентификаторов определенное свойство в наборе определенное свойство.</span><span class="sxs-lookup"><span data-stu-id="675df-141">Retrieve names for specific property identifiers in a specific property set.</span></span>
    
- <span data-ttu-id="675df-142">Извлечение имен идентификаторов определенное свойство в любой набор свойств.</span><span class="sxs-lookup"><span data-stu-id="675df-142">Retrieve names for specific property identifiers in any property set.</span></span>
    
- <span data-ttu-id="675df-143">Извлечение имен для всех именованных свойств, которые включены в объект сопоставления.</span><span class="sxs-lookup"><span data-stu-id="675df-143">Retrieve names for all named properties that are included in the object's mapping.</span></span>
    
<span data-ttu-id="675df-144">Если значение _lppPropTags_ указывает на это свойство тег массив с один или несколько идентификаторов свойств, а _lpPropSetGuid_ указывает свойство, **GetNamesFromIDs** игнорирует набор свойств и типы свойств и возвращает все имена которые сопоставляются с идентификаторами указанного.</span><span class="sxs-lookup"><span data-stu-id="675df-144">If  _lppPropTags_ points to a valid property tag array with one or more property identifiers, and  _lpPropSetGuid_ points to a valid property set, **GetNamesFromIDs** ignores the property set and the property types and returns all of the names that map to the specified identifiers.</span></span> 
  
<span data-ttu-id="675df-145">При _lppPropTags_ указывает на массива тег допустимого свойства с помощью одного или нескольких идентификаторов свойств и _lpPropSetGuid_ значение NULL, **GetNamesFromIDs** возвращает все имена, которые сопоставляют указанного идентификаторами.</span><span class="sxs-lookup"><span data-stu-id="675df-145">If  _lppPropTags_ points to a valid property tag array with one or more property identifiers and  _lpPropSetGuid_ is NULL, **GetNamesFromIDs** returns all of the names that map to the specified identifiers.</span></span> 
  
<span data-ttu-id="675df-146">Если указанный идентификатор не имеет имя, **GetNamesFromIDs** возвращает NULL на месте этот идентификатор в структуре, возвращаемых в _lpppPropNames_ и возвращает MAPI_W_ERRORS_RETURNED.</span><span class="sxs-lookup"><span data-stu-id="675df-146">If a specified identifier does not have a name, **GetNamesFromIDs** returns NULL in that identifier's place in the structure returned in  _lpppPropNames_ and also returns MAPI_W_ERRORS_RETURNED.</span></span> 
  
<span data-ttu-id="675df-147">Если _lpPropSetGuid_ и _lppPropTags_ значение NULL, **GetNamesFromIDs** выделяет новый массив свойство tag и возвращает все имена для всех именованных свойств для объекта.</span><span class="sxs-lookup"><span data-stu-id="675df-147">If both  _lpPropSetGuid_ and  _lppPropTags_ are NULL, **GetNamesFromIDs** allocates a new property tag array and returns all of the names for all of the named properties for the object.</span></span> 
  
<span data-ttu-id="675df-148">При наличии имена, не должно быть возвращено, возможно, так как нет свойств в наборе запрошенное свойство или все свойства, типа, исключены с флаги **GetNamesFromIDs** выполняет следующее.</span><span class="sxs-lookup"><span data-stu-id="675df-148">When there are no names to be returned, perhaps because there are no properties in the requested property set or all of the properties are of a type excluded by the flags, **GetNamesFromIDs** does the following:</span></span> 
  
- <span data-ttu-id="675df-149">Возвращает значение S_OK.</span><span class="sxs-lookup"><span data-stu-id="675df-149">Returns S_OK.</span></span>
    
- <span data-ttu-id="675df-150">Выделяет новые структуры **SPropTagArray** , **cValues** члену задается значение 0.</span><span class="sxs-lookup"><span data-stu-id="675df-150">Allocates a new **SPropTagArray** structure, setting the **cValues** member to 0.</span></span> 
    
- <span data-ttu-id="675df-151">Задает содержимое _lpcPropNames_ 0.</span><span class="sxs-lookup"><span data-stu-id="675df-151">Sets the contents of  _lpcPropNames_ to 0.</span></span> 
    
- <span data-ttu-id="675df-152">Задает содержимое _lpppPropNames_ значение NULL.</span><span class="sxs-lookup"><span data-stu-id="675df-152">Sets the contents of  _lpppPropNames_ to NULL.</span></span> 
    
## <a name="notes-to-implementers"></a><span data-ttu-id="675df-153">Примечания для реализующих</span><span class="sxs-lookup"><span data-stu-id="675df-153">Notes to implementers</span></span>

<span data-ttu-id="675df-154">Если _lpPropSetGuid_ указывает на свойство набора и _lppPropTags_ имеет значение NULL, результат является неопределенным.</span><span class="sxs-lookup"><span data-stu-id="675df-154">If  _lpPropSetGuid_ points to a valid property set and  _lppPropTags_ is NULL, the result is undefined.</span></span> <span data-ttu-id="675df-155">Можно использовать один из следующих стратегий:</span><span class="sxs-lookup"><span data-stu-id="675df-155">You can use one of the following strategies:</span></span> 
  
- <span data-ttu-id="675df-156">Пропуск набор свойств и возвращают имена для идентификаторов в массиве тега свойства.</span><span class="sxs-lookup"><span data-stu-id="675df-156">Ignore the property set and return the names for the identifiers in the property tag array.</span></span>
    
- <span data-ttu-id="675df-157">Возвращает имена только идентификаторов в массиве тег свойств, относящихся к указанным набором свойств.</span><span class="sxs-lookup"><span data-stu-id="675df-157">Return the names for only the identifiers in the property tag array that belong to the specified property set.</span></span>
    
- <span data-ttu-id="675df-158">Сбой вызова, возвращая MAPI_E_INVALID_PARAMETER.</span><span class="sxs-lookup"><span data-stu-id="675df-158">Fail the call, returning MAPI_E_INVALID_PARAMETER.</span></span> 
    
## <a name="notes-to-callers"></a><span data-ttu-id="675df-159">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="675df-159">Notes to callers</span></span>

<span data-ttu-id="675df-160">Чтобы получить все именованные свойства для объекта, необходимо вызвать метод [IMAPIProp::GetPropList](imapiprop-getproplist.md) объекта и затем передайте возвращенные идентификаторы, над 0x8000 диапазона **GetNamesFromIDs**.</span><span class="sxs-lookup"><span data-stu-id="675df-160">To retrieve all of the named properties for an object, you must first call the object's [IMAPIProp::GetPropList](imapiprop-getproplist.md) method and then pass the returned identifiers that are above the 0x8000 range to **GetNamesFromIDs**.</span></span>
  
<span data-ttu-id="675df-161">Если передать свойство набор, но не свойство tag массива быть подготовлено к непредсказуемым последствиям.</span><span class="sxs-lookup"><span data-stu-id="675df-161">If you pass a valid property set but not a valid property tag array, be prepared for unpredictable results.</span></span> <span data-ttu-id="675df-162">Некоторые реализации **GetNamesFromIDs** игнорировать набор свойств и возвращает имена для идентификаторов в массиве тега свойства.</span><span class="sxs-lookup"><span data-stu-id="675df-162">Some implementations of **GetNamesFromIDs** ignore the property set and return the names for the identifiers in the property tag array.</span></span> <span data-ttu-id="675df-163">Некоторые реализации возвращают MAPI_E_INVALID_PARAMETER.</span><span class="sxs-lookup"><span data-stu-id="675df-163">Some implementations return MAPI_E_INVALID_PARAMETER.</span></span> <span data-ttu-id="675df-164">По-прежнему другими реализациями возвращать имена идентификаторов всех свойств в набор свойств.</span><span class="sxs-lookup"><span data-stu-id="675df-164">Still other implementations return names for identifiers of all properties in the property set.</span></span> <span data-ttu-id="675df-165">Если набор свойств PS_PUBLIC_STRINGS, **GetNamesFromIDs** может вернуть все имена, которые никогда не были созданы.</span><span class="sxs-lookup"><span data-stu-id="675df-165">If the property set is PS_PUBLIC_STRINGS, **GetNamesFromIDs** can return all names that were ever created.</span></span> <span data-ttu-id="675df-166">Является ли поставщик услуг сохраняет свойства в разделе идентификаторы, связанные с общей строки несущественно.</span><span class="sxs-lookup"><span data-stu-id="675df-166">Whether the service provider stores a property under the identifiers associated with the public strings is immaterial.</span></span> 
  
<span data-ttu-id="675df-167">По окончании имена свойств, проверьте содержимое параметра _lpcPropNames_ , чтобы определить, были ли возвращены имена.</span><span class="sxs-lookup"><span data-stu-id="675df-167">When you are finished with the property names, check the contents of the  _lpcPropNames_ parameter to determine whether any names were returned.</span></span> <span data-ttu-id="675df-168">Если Да, вызовите функцию [MAPIFreeBuffer](mapifreebuffer.md) , чтобы освободить память, на который указывает _lppPropTags_ и _lpppPropNames_ при возвращении успешный результат.</span><span class="sxs-lookup"><span data-stu-id="675df-168">If so, call the [MAPIFreeBuffer](mapifreebuffer.md) function to free the memory pointed to by  _lppPropTags_ and  _lpppPropNames_ when a successful result is returned.</span></span> <span data-ttu-id="675df-169">Один вызов **MAPIFreeBuffer** является достаточным для каждого параметра; Нет необходимости проходят через массив указателей и сведениям каждой структуры **MAPINAMEID** по отдельности.</span><span class="sxs-lookup"><span data-stu-id="675df-169">One call to **MAPIFreeBuffer** is sufficient for each parameter; you do not have to traverse the array of pointers and free each **MAPINAMEID** structure individually.</span></span> 
  
<span data-ttu-id="675df-170">Дополнительные сведения об именованных свойств в разделе [Свойства с именем MAPI](mapi-named-properties.md).</span><span class="sxs-lookup"><span data-stu-id="675df-170">For more information about named properties, see [MAPI Named Properties](mapi-named-properties.md).</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="675df-171">Справочные материалы по MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="675df-171">MFCMAPI reference</span></span>

<span data-ttu-id="675df-172">Пример кода MFCMAPI указан в приведенной ниже таблице.</span><span class="sxs-lookup"><span data-stu-id="675df-172">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="675df-173">**Файл**</span><span class="sxs-lookup"><span data-stu-id="675df-173">**File**</span></span>|<span data-ttu-id="675df-174">**Функция**</span><span class="sxs-lookup"><span data-stu-id="675df-174">**Function**</span></span>|<span data-ttu-id="675df-175">**Примечание**</span><span class="sxs-lookup"><span data-stu-id="675df-175">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="675df-176">SingleMAPIPropListCtrl.cpp</span><span class="sxs-lookup"><span data-stu-id="675df-176">SingleMAPIPropListCtrl.cpp</span></span>  <br/> |<span data-ttu-id="675df-177">CSingleMAPIPropListCtrl::FindAllNamedProps</span><span class="sxs-lookup"><span data-stu-id="675df-177">CSingleMAPIPropListCtrl::FindAllNamedProps</span></span>  <br/> |<span data-ttu-id="675df-178">Mfcmapi (en) использует метод **IMAPIProp::GetNamesFromIDs** для поиска именованных свойств, которые ранее были сопоставлены.</span><span class="sxs-lookup"><span data-stu-id="675df-178">MFCMAPI uses the **IMAPIProp::GetNamesFromIDs** method to look up named properties that have previously been mapped.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="675df-179">См. также</span><span class="sxs-lookup"><span data-stu-id="675df-179">See also</span></span>



[<span data-ttu-id="675df-180">GUID</span><span class="sxs-lookup"><span data-stu-id="675df-180">GUID</span></span>](guid.md)
  
[<span data-ttu-id="675df-181">IMAPIProp::GetIDsFromNames</span><span class="sxs-lookup"><span data-stu-id="675df-181">IMAPIProp::GetIDsFromNames</span></span>](imapiprop-getidsfromnames.md)
  
[<span data-ttu-id="675df-182">IMAPIProp::GetPropList</span><span class="sxs-lookup"><span data-stu-id="675df-182">IMAPIProp::GetPropList</span></span>](imapiprop-getproplist.md)
  
[<span data-ttu-id="675df-183">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="675df-183">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="675df-184">MAPINAMEID</span><span class="sxs-lookup"><span data-stu-id="675df-184">MAPINAMEID</span></span>](mapinameid.md)
  
[<span data-ttu-id="675df-185">SPropTagArray</span><span class="sxs-lookup"><span data-stu-id="675df-185">SPropTagArray</span></span>](sproptagarray.md)
  
[<span data-ttu-id="675df-186">IMAPIProp : IUnknown</span><span class="sxs-lookup"><span data-stu-id="675df-186">IMAPIProp : IUnknown</span></span>](imapipropiunknown.md)


[<span data-ttu-id="675df-187">MFCMAPI как пример кода</span><span class="sxs-lookup"><span data-stu-id="675df-187">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)
  
[<span data-ttu-id="675df-188">Именованные свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="675df-188">MAPI Named Properties</span></span>](mapi-named-properties.md)
  
[<span data-ttu-id="675df-189">Использование макросов для обработки ошибок</span><span class="sxs-lookup"><span data-stu-id="675df-189">Using Macros for Error Handling</span></span>](using-macros-for-error-handling.md)

