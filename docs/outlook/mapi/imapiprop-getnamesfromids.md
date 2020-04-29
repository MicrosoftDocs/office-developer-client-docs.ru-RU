---
title: имапипропжетнамесфромидс
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
# <a name="imapipropgetnamesfromids"></a><span data-ttu-id="24476-103">IMAPIProp::GetNamesFromIDs</span><span class="sxs-lookup"><span data-stu-id="24476-103">IMAPIProp::GetNamesFromIDs</span></span>

  
  
<span data-ttu-id="24476-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="24476-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="24476-105">Предоставляет имена свойств, которые соответствуют одному или нескольким идентификаторам свойств.</span><span class="sxs-lookup"><span data-stu-id="24476-105">Provides the property names that correspond to one or more property identifiers.</span></span>
  
```cpp
HRESULT GetNamesFromIDs(
  LPSPropTagArray FAR * lppPropTags,
  LPGUID lpPropSetGuid,
  ULONG ulFlags,
  ULONG FAR * lpcPropNames,
  LPMAPINAMEID FAR * FAR * lpppPropNames
);
```

## <a name="parameters"></a><span data-ttu-id="24476-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="24476-106">Parameters</span></span>

 <span data-ttu-id="24476-107">_лпппроптагс_</span><span class="sxs-lookup"><span data-stu-id="24476-107">_lppPropTags_</span></span>
  
> <span data-ttu-id="24476-108">[вход, выход] На входе указатель на структуру [спроптагаррай](sproptagarray.md) , содержащую массив тегов свойств; в противном случае — значение NULL, указывающее, что должны возвращаться все имена.</span><span class="sxs-lookup"><span data-stu-id="24476-108">[in, out] On input, a pointer to an [SPropTagArray](sproptagarray.md) structure that contains an array of property tags; otherwise, NULL, indicating that all names should be returned.</span></span> <span data-ttu-id="24476-109">Элемент **квалуес** для массива тегов свойств не может иметь значение 0.</span><span class="sxs-lookup"><span data-stu-id="24476-109">The **cValues** member for the property tag array cannot be 0.</span></span> <span data-ttu-id="24476-110">Если _лпппроптагс_ является допустимым указателем на входе, **жетнамесфромидс** возвращает имена для каждого идентификатора свойства, включенного в массив.</span><span class="sxs-lookup"><span data-stu-id="24476-110">If  _lppPropTags_ is a valid pointer on input, **GetNamesFromIDs** returns names for each property identifier included in the array.</span></span> 
    
 <span data-ttu-id="24476-111">_лппропсетгуид_</span><span class="sxs-lookup"><span data-stu-id="24476-111">_lpPropSetGuid_</span></span>
  
> <span data-ttu-id="24476-112">возврата Указатель на GUID или структуру [GUID](guid.md) , определяющую набор свойств.</span><span class="sxs-lookup"><span data-stu-id="24476-112">[in] A pointer to a GUID, or [GUID](guid.md) structure, that identifies a property set.</span></span> <span data-ttu-id="24476-113">Параметр _лппропсетгуид_ может указывать на допустимый набор свойств или может иметь значение null.</span><span class="sxs-lookup"><span data-stu-id="24476-113">The  _lpPropSetGuid_ parameter can point to a valid property set or can be NULL.</span></span> 
    
 <span data-ttu-id="24476-114">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="24476-114">_ulFlags_</span></span>
  
> <span data-ttu-id="24476-115">возврата Битовая маска флагов, указывающая тип возвращаемых имен.</span><span class="sxs-lookup"><span data-stu-id="24476-115">[in] A bitmask of flags that indicates the type of names to be returned.</span></span> <span data-ttu-id="24476-116">Можно использовать следующие флаги (если установлены оба флага, имена не возвращаются):</span><span class="sxs-lookup"><span data-stu-id="24476-116">The following flags can be used (if both flags are set, no names will be returned):</span></span>
    
<span data-ttu-id="24476-117">MAPI_NO_IDS</span><span class="sxs-lookup"><span data-stu-id="24476-117">MAPI_NO_IDS</span></span> 
  
> <span data-ttu-id="24476-118">Возвращаются только те запросы, для которых возвращаются только имена, хранящиеся в виде строк Юникода.</span><span class="sxs-lookup"><span data-stu-id="24476-118">Requests that only names stored as Unicode strings be returned.</span></span> 
    
<span data-ttu-id="24476-119">MAPI_NO_STRINGS</span><span class="sxs-lookup"><span data-stu-id="24476-119">MAPI_NO_STRINGS</span></span> 
  
> <span data-ttu-id="24476-120">Запросы, которые возвращаются только имена, хранящиеся как числовые идентификаторы.</span><span class="sxs-lookup"><span data-stu-id="24476-120">Requests that only names stored as numeric identifiers be returned.</span></span> 
    
 <span data-ttu-id="24476-121">_лпкпропнамес_</span><span class="sxs-lookup"><span data-stu-id="24476-121">_lpcPropNames_</span></span>
  
> <span data-ttu-id="24476-122">вышли Указатель на число указателей имени свойства в массиве, на которое указывает параметр _лпппропнамес_ .</span><span class="sxs-lookup"><span data-stu-id="24476-122">[out] A pointer to a count of the property name pointers in the array pointed to by the  _lppPropNames_ parameter.</span></span> 
    
 <span data-ttu-id="24476-123">_лппппропнамес_</span><span class="sxs-lookup"><span data-stu-id="24476-123">_lpppPropNames_</span></span>
  
> <span data-ttu-id="24476-124">вышли Указатель на массив указателей на структуры [мапинамеид](mapinameid.md) , которые содержат имена свойств.</span><span class="sxs-lookup"><span data-stu-id="24476-124">[out] A pointer to an array of pointers to [MAPINAMEID](mapinameid.md) structures that contains property names.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="24476-125">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="24476-125">Return value</span></span>

<span data-ttu-id="24476-126">S_OK</span><span class="sxs-lookup"><span data-stu-id="24476-126">S_OK</span></span> 
  
> <span data-ttu-id="24476-127">Имена свойств успешно возвращены.</span><span class="sxs-lookup"><span data-stu-id="24476-127">The property names were successfully returned.</span></span> 
    
<span data-ttu-id="24476-128">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="24476-128">MAPI_E_NO_SUPPORT</span></span> 
  
> <span data-ttu-id="24476-129">Объект не поддерживает именованные свойства.</span><span class="sxs-lookup"><span data-stu-id="24476-129">The object does not support named properties.</span></span> 
    
<span data-ttu-id="24476-130">MAPI_W_ERRORS_RETURNED</span><span class="sxs-lookup"><span data-stu-id="24476-130">MAPI_W_ERRORS_RETURNED</span></span> 
  
> <span data-ttu-id="24476-131">Вызов выполнен в целом, но имена одного или нескольких свойств не могут быть возвращены.</span><span class="sxs-lookup"><span data-stu-id="24476-131">The call succeeded overall, but names for one or more properties could not be returned.</span></span> <span data-ttu-id="24476-132">Теги свойств для неисправного свойства имеют тип свойства **PT_ERROR**.</span><span class="sxs-lookup"><span data-stu-id="24476-132">The property tags for the failing properties have a property type of **PT_ERROR**.</span></span> <span data-ttu-id="24476-133">При возвращении этого предупреждения вызов должен обрабатываться как успешный.</span><span class="sxs-lookup"><span data-stu-id="24476-133">When this warning is returned, the call should be handled as successful.</span></span> <span data-ttu-id="24476-134">Чтобы проверить это предупреждение, используйте макрос **HR_FAILED** .</span><span class="sxs-lookup"><span data-stu-id="24476-134">To test for this warning, use the **HR_FAILED** macro.</span></span> <span data-ttu-id="24476-135">Дополнительные сведения см. [в разделе Использование макросов для обработки ошибок](using-macros-for-error-handling.md).</span><span class="sxs-lookup"><span data-stu-id="24476-135">For more information, see [Using Macros for Error Handling](using-macros-for-error-handling.md).</span></span> 
    
<span data-ttu-id="24476-136">MAPI_E_INVALID_PARAMETER</span><span class="sxs-lookup"><span data-stu-id="24476-136">MAPI_E_INVALID_PARAMETER</span></span> 
  
> <span data-ttu-id="24476-137">Элемент **квалуес** одной или нескольких записей в массиве тегов свойств, на который указывает _лпппроптагс_ , имеет значение 0.</span><span class="sxs-lookup"><span data-stu-id="24476-137">The **cValues** member of one or more of the entries in the property tag array pointed to by  _lppPropTags_ is set to 0.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="24476-138">Примечания</span><span class="sxs-lookup"><span data-stu-id="24476-138">Remarks</span></span>

<span data-ttu-id="24476-139">Несмотря на то, что доступ к большинству свойств осуществляется с помощью идентификатора свойства, к некоторым свойствам можно получить доступ по имени.</span><span class="sxs-lookup"><span data-stu-id="24476-139">While access to most properties is by property identifier, some properties can be accessed by name.</span></span> <span data-ttu-id="24476-140">Метод **IMAPIProp:: жетнамесфромидс** может быть вызван для выполнения следующих действий:</span><span class="sxs-lookup"><span data-stu-id="24476-140">The **IMAPIProp::GetNamesFromIDs** method can be called to do the following:</span></span> 
  
- <span data-ttu-id="24476-141">Получение имен для определенных идентификаторов свойств в определенном наборе свойств.</span><span class="sxs-lookup"><span data-stu-id="24476-141">Retrieve names for specific property identifiers in a specific property set.</span></span>
    
- <span data-ttu-id="24476-142">Получение имен для определенных идентификаторов свойств в любом наборе свойств.</span><span class="sxs-lookup"><span data-stu-id="24476-142">Retrieve names for specific property identifiers in any property set.</span></span>
    
- <span data-ttu-id="24476-143">Получение имен для всех именованных свойств, включенных в сопоставление объекта.</span><span class="sxs-lookup"><span data-stu-id="24476-143">Retrieve names for all named properties that are included in the object's mapping.</span></span>
    
<span data-ttu-id="24476-144">Если _лпппроптагс_ указывает на допустимый массив тегов свойств с одним или несколькими идентификаторами свойств, а _лппропсетгуид_ указывает на допустимый набор свойств, **жетнамесфромидс** игнорирует набор свойств и типы свойств и возвращает все имена, сопоставляемые с указанными идентификаторами.</span><span class="sxs-lookup"><span data-stu-id="24476-144">If  _lppPropTags_ points to a valid property tag array with one or more property identifiers, and  _lpPropSetGuid_ points to a valid property set, **GetNamesFromIDs** ignores the property set and the property types and returns all of the names that map to the specified identifiers.</span></span> 
  
<span data-ttu-id="24476-145">Если _лпппроптагс_ указывает на допустимый массив тегов свойств с одним или несколькими идентификаторами свойств, а _лппропсетгуид_ имеет значение null, **жетнамесфромидс** возвращает все имена, сопоставляемые с указанными идентификаторами.</span><span class="sxs-lookup"><span data-stu-id="24476-145">If  _lppPropTags_ points to a valid property tag array with one or more property identifiers and  _lpPropSetGuid_ is NULL, **GetNamesFromIDs** returns all of the names that map to the specified identifiers.</span></span> 
  
<span data-ttu-id="24476-146">Если у указанного идентификатора нет имени, **жетнамесфромидс** возвращает значение NULL в этом идентификаторе в структуре, возвращаемой в _лппппропнамес_ , а также возвращает MAPI_W_ERRORS_RETURNED.</span><span class="sxs-lookup"><span data-stu-id="24476-146">If a specified identifier does not have a name, **GetNamesFromIDs** returns NULL in that identifier's place in the structure returned in  _lpppPropNames_ and also returns MAPI_W_ERRORS_RETURNED.</span></span> 
  
<span data-ttu-id="24476-147">Если для обоих свойств _лппропсетгуид_ и _лпппроптагс_ задано значение null, **жетнамесфромидс** выделяет новый массив тегов свойств и возвращает все имена всех именованных свойств объекта.</span><span class="sxs-lookup"><span data-stu-id="24476-147">If both  _lpPropSetGuid_ and  _lppPropTags_ are NULL, **GetNamesFromIDs** allocates a new property tag array and returns all of the names for all of the named properties for the object.</span></span> 
  
<span data-ttu-id="24476-148">Если нет возвращаемых имен, вероятно, из-за того, что в запрошенном наборе свойств нет свойств или все свойства имеют тип, исключенный с помощью флагов, **жетнамесфромидс** выполняет следующие действия:</span><span class="sxs-lookup"><span data-stu-id="24476-148">When there are no names to be returned, perhaps because there are no properties in the requested property set or all of the properties are of a type excluded by the flags, **GetNamesFromIDs** does the following:</span></span> 
  
- <span data-ttu-id="24476-149">Возвращает S_OK.</span><span class="sxs-lookup"><span data-stu-id="24476-149">Returns S_OK.</span></span>
    
- <span data-ttu-id="24476-150">Выделяет новую структуру **спроптагаррай** , устанавливая для члена **квалуес** значение 0.</span><span class="sxs-lookup"><span data-stu-id="24476-150">Allocates a new **SPropTagArray** structure, setting the **cValues** member to 0.</span></span> 
    
- <span data-ttu-id="24476-151">Задает значение 0 для содержимого _лпкпропнамес_ .</span><span class="sxs-lookup"><span data-stu-id="24476-151">Sets the contents of  _lpcPropNames_ to 0.</span></span> 
    
- <span data-ttu-id="24476-152">Задает для содержимого _лппппропнамес_ значение null.</span><span class="sxs-lookup"><span data-stu-id="24476-152">Sets the contents of  _lpppPropNames_ to NULL.</span></span> 
    
## <a name="notes-to-implementers"></a><span data-ttu-id="24476-153">Примечания для исполнителей</span><span class="sxs-lookup"><span data-stu-id="24476-153">Notes to implementers</span></span>

<span data-ttu-id="24476-154">Если _лппропсетгуид_ указывает на допустимый набор свойств, а _лпппроптагс_ имеет значение null, результат не определен.</span><span class="sxs-lookup"><span data-stu-id="24476-154">If  _lpPropSetGuid_ points to a valid property set and  _lppPropTags_ is NULL, the result is undefined.</span></span> <span data-ttu-id="24476-155">Можно использовать одну из следующих стратегий:</span><span class="sxs-lookup"><span data-stu-id="24476-155">You can use one of the following strategies:</span></span> 
  
- <span data-ttu-id="24476-156">Игнорировать набор свойств и возвращать имена идентификаторов в массиве тегов свойств.</span><span class="sxs-lookup"><span data-stu-id="24476-156">Ignore the property set and return the names for the identifiers in the property tag array.</span></span>
    
- <span data-ttu-id="24476-157">Возвращает имена только для идентификаторов в массиве тегов свойств, принадлежащих указанному набору свойств.</span><span class="sxs-lookup"><span data-stu-id="24476-157">Return the names for only the identifiers in the property tag array that belong to the specified property set.</span></span>
    
- <span data-ttu-id="24476-158">Произошел отказ вызова, возвращая MAPI_E_INVALID_PARAMETER.</span><span class="sxs-lookup"><span data-stu-id="24476-158">Fail the call, returning MAPI_E_INVALID_PARAMETER.</span></span> 
    
## <a name="notes-to-callers"></a><span data-ttu-id="24476-159">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="24476-159">Notes to callers</span></span>

<span data-ttu-id="24476-160">Чтобы получить все именованные свойства объекта, сначала необходимо вызвать метод объекта [IMAPIProp:: жетпроплист](imapiprop-getproplist.md) , а затем передать возвращенные идентификаторы, находящиеся выше диапазона 0x8000, в **жетнамесфромидс**.</span><span class="sxs-lookup"><span data-stu-id="24476-160">To retrieve all of the named properties for an object, you must first call the object's [IMAPIProp::GetPropList](imapiprop-getproplist.md) method and then pass the returned identifiers that are above the 0x8000 range to **GetNamesFromIDs**.</span></span>
  
<span data-ttu-id="24476-161">Если вы передаете допустимый набор свойств, но не является допустимым массивом тегов свойств, будьте готовы к непредсказуемым результатам.</span><span class="sxs-lookup"><span data-stu-id="24476-161">If you pass a valid property set but not a valid property tag array, be prepared for unpredictable results.</span></span> <span data-ttu-id="24476-162">Некоторые реализации **жетнамесфромидс** игнорируют набор свойств и возвращают имена идентификаторов в массиве тегов свойств.</span><span class="sxs-lookup"><span data-stu-id="24476-162">Some implementations of **GetNamesFromIDs** ignore the property set and return the names for the identifiers in the property tag array.</span></span> <span data-ttu-id="24476-163">Некоторые реализации возвращают MAPI_E_INVALID_PARAMETER.</span><span class="sxs-lookup"><span data-stu-id="24476-163">Some implementations return MAPI_E_INVALID_PARAMETER.</span></span> <span data-ttu-id="24476-164">Остальные реализации возвращают имена для идентификаторов всех свойств в наборе свойств.</span><span class="sxs-lookup"><span data-stu-id="24476-164">Still other implementations return names for identifiers of all properties in the property set.</span></span> <span data-ttu-id="24476-165">Если свойство имеет значение PS_PUBLIC_STRINGS, **жетнамесфромидс** может возвращать все ранее созданные имена.</span><span class="sxs-lookup"><span data-stu-id="24476-165">If the property set is PS_PUBLIC_STRINGS, **GetNamesFromIDs** can return all names that were ever created.</span></span> <span data-ttu-id="24476-166">Хранит ли поставщик услуг свойство под идентификаторами, связанными с общедоступными строками, является нематериальным.</span><span class="sxs-lookup"><span data-stu-id="24476-166">Whether the service provider stores a property under the identifiers associated with the public strings is immaterial.</span></span> 
  
<span data-ttu-id="24476-167">По завершении работы с именами свойств проверьте содержимое параметра _лпкпропнамес_ , чтобы определить, были ли возвращены какие бы то ни было имена.</span><span class="sxs-lookup"><span data-stu-id="24476-167">When you are finished with the property names, check the contents of the  _lpcPropNames_ parameter to determine whether any names were returned.</span></span> <span data-ttu-id="24476-168">В этом случае вызовите функцию [мапифрибуффер](mapifreebuffer.md) , чтобы освободить память, на которую указывает _Лпппроптагс_ , и _лппппропнамес_ , когда возвращается успешный результат.</span><span class="sxs-lookup"><span data-stu-id="24476-168">If so, call the [MAPIFreeBuffer](mapifreebuffer.md) function to free the memory pointed to by  _lppPropTags_ and  _lpppPropNames_ when a successful result is returned.</span></span> <span data-ttu-id="24476-169">Для каждого параметра достаточно одного вызова **мапифрибуффер** ; нет необходимости проходить по массиву указателей и освобождать каждую структуру **мапинамеид** по отдельности.</span><span class="sxs-lookup"><span data-stu-id="24476-169">One call to **MAPIFreeBuffer** is sufficient for each parameter; you do not have to traverse the array of pointers and free each **MAPINAMEID** structure individually.</span></span> 
  
<span data-ttu-id="24476-170">Более подробную информацию об именованных свойствах можно узнать в статье [свойства MAPI с именем](mapi-named-properties.md).</span><span class="sxs-lookup"><span data-stu-id="24476-170">For more information about named properties, see [MAPI Named Properties](mapi-named-properties.md).</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="24476-171">Справочные материалы по MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="24476-171">MFCMAPI reference</span></span>

<span data-ttu-id="24476-172">Пример кода MFCMAPI указан в приведенной ниже таблице.</span><span class="sxs-lookup"><span data-stu-id="24476-172">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="24476-173">**Файл**</span><span class="sxs-lookup"><span data-stu-id="24476-173">**File**</span></span>|<span data-ttu-id="24476-174">**Функция**</span><span class="sxs-lookup"><span data-stu-id="24476-174">**Function**</span></span>|<span data-ttu-id="24476-175">**Примечание**</span><span class="sxs-lookup"><span data-stu-id="24476-175">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="24476-176">Синглемапипроплистктрл. cpp</span><span class="sxs-lookup"><span data-stu-id="24476-176">SingleMAPIPropListCtrl.cpp</span></span>  <br/> |<span data-ttu-id="24476-177">Ксинглемапипроплистктрл:: Финдаллнамедпропс</span><span class="sxs-lookup"><span data-stu-id="24476-177">CSingleMAPIPropListCtrl::FindAllNamedProps</span></span>  <br/> |<span data-ttu-id="24476-178">MFCMAPI использует метод **IMAPIProp:: жетнамесфромидс** для поиска именованных свойств, которые ранее были сопоставлены.</span><span class="sxs-lookup"><span data-stu-id="24476-178">MFCMAPI uses the **IMAPIProp::GetNamesFromIDs** method to look up named properties that have previously been mapped.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="24476-179">См. также</span><span class="sxs-lookup"><span data-stu-id="24476-179">See also</span></span>



[<span data-ttu-id="24476-180">GUID</span><span class="sxs-lookup"><span data-stu-id="24476-180">GUID</span></span>](guid.md)
  
[<span data-ttu-id="24476-181">IMAPIProp::GetIDsFromNames</span><span class="sxs-lookup"><span data-stu-id="24476-181">IMAPIProp::GetIDsFromNames</span></span>](imapiprop-getidsfromnames.md)
  
[<span data-ttu-id="24476-182">IMAPIProp::GetPropList</span><span class="sxs-lookup"><span data-stu-id="24476-182">IMAPIProp::GetPropList</span></span>](imapiprop-getproplist.md)
  
[<span data-ttu-id="24476-183">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="24476-183">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="24476-184">MAPINAMEID</span><span class="sxs-lookup"><span data-stu-id="24476-184">MAPINAMEID</span></span>](mapinameid.md)
  
[<span data-ttu-id="24476-185">SPropTagArray</span><span class="sxs-lookup"><span data-stu-id="24476-185">SPropTagArray</span></span>](sproptagarray.md)
  
[<span data-ttu-id="24476-186">IMAPIProp : IUnknown</span><span class="sxs-lookup"><span data-stu-id="24476-186">IMAPIProp : IUnknown</span></span>](imapipropiunknown.md)


[<span data-ttu-id="24476-187">MFCMAPI как пример кода</span><span class="sxs-lookup"><span data-stu-id="24476-187">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)
  
[<span data-ttu-id="24476-188">Именованные свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="24476-188">MAPI Named Properties</span></span>](mapi-named-properties.md)
  
[<span data-ttu-id="24476-189">Использование макросов для обработки ошибок</span><span class="sxs-lookup"><span data-stu-id="24476-189">Using Macros for Error Handling</span></span>](using-macros-for-error-handling.md)

