---
title: Имапипропжетпропс
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIProp.GetProps
api_type:
- COM
ms.assetid: 1c7a9cd2-d765-4218-9aee-52df1a2aae6c
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 9b03775d495f7d1f51142eb0ed06fc9ecdf6d1a3
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412459"
---
# <a name="imapipropgetprops"></a><span data-ttu-id="cdc87-103">IMAPIProp::GetProps</span><span class="sxs-lookup"><span data-stu-id="cdc87-103">IMAPIProp::GetProps</span></span>

  
  
<span data-ttu-id="cdc87-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="cdc87-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="cdc87-105">Получает значение свойства одного или нескольких свойств объекта.</span><span class="sxs-lookup"><span data-stu-id="cdc87-105">Retrieves the property value of one or more properties of an object.</span></span>
  
```cpp
HRESULT GetProps(
  LPSPropTagArray lpPropTagArray,
  ULONG ulFlags,
  ULONG FAR * lpcValues,
  LPSPropValue FAR * lppPropArray
);
```

## <a name="parameters"></a><span data-ttu-id="cdc87-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="cdc87-106">Parameters</span></span>

 <span data-ttu-id="cdc87-107">_Лппроптагаррай_</span><span class="sxs-lookup"><span data-stu-id="cdc87-107">_lpPropTagArray_</span></span>
  
> <span data-ttu-id="cdc87-108">возврата Указатель на массив тегов свойств, определяющий свойства, значения которых требуется получить.</span><span class="sxs-lookup"><span data-stu-id="cdc87-108">[in] A pointer to an array of property tags that identify the properties whose values are to be retrieved.</span></span> <span data-ttu-id="cdc87-109">Параметр _лппроптагаррай_ должен иметь значение null, указывая, что необходимо возвратить значения всех свойств объекта, или указать структуру [спроптагаррай](sproptagarray.md) , содержащую один или несколько тегов свойств.</span><span class="sxs-lookup"><span data-stu-id="cdc87-109">The  _lpPropTagArray_ parameter must be either NULL, indicating that values for all properties of the object should be returned, or point to an [SPropTagArray](sproptagarray.md) structure that contains one or more property tags.</span></span> 
    
 <span data-ttu-id="cdc87-110">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="cdc87-110">_ulFlags_</span></span>
  
> <span data-ttu-id="cdc87-111">возврата Битовая маска флагов, указывающая формат для свойств с типом ПТ_УНСПЕЦИФИЕД.</span><span class="sxs-lookup"><span data-stu-id="cdc87-111">[in] A bitmask of flags that indicates the format for properties that have the type PT_UNSPECIFIED.</span></span> <span data-ttu-id="cdc87-112">Можно задать следующий флаг:</span><span class="sxs-lookup"><span data-stu-id="cdc87-112">The following flag can be set:</span></span>
    
<span data-ttu-id="cdc87-113">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="cdc87-113">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="cdc87-114">Строковые значения для этих свойств должны быть возвращены в формате Юникод.</span><span class="sxs-lookup"><span data-stu-id="cdc87-114">The string values for these properties should be returned in the Unicode format.</span></span> <span data-ttu-id="cdc87-115">Если флаг МАПИ_УНИКОДЕ не установлен, строковые значения должны быть возвращены в формате ANSI.</span><span class="sxs-lookup"><span data-stu-id="cdc87-115">If the MAPI_UNICODE flag is not set, the string values should be returned in the ANSI format.</span></span>
    
 <span data-ttu-id="cdc87-116">_Лпквалуес_</span><span class="sxs-lookup"><span data-stu-id="cdc87-116">_lpcValues_</span></span>
  
> <span data-ttu-id="cdc87-117">вышли Указатель на число значений свойств, на которые указывает параметр _лпппропаррай_ .</span><span class="sxs-lookup"><span data-stu-id="cdc87-117">[out] A pointer to a count of property values pointed to by the  _lppPropArray_ parameter.</span></span> <span data-ttu-id="cdc87-118">Если _лпппропаррай_ имеет значение null, то содержимое параметра _лпквалуес_ равно нулю.</span><span class="sxs-lookup"><span data-stu-id="cdc87-118">If  _lppPropArray_ is NULL, the content of the  _lpcValues_ parameter is zero.</span></span> 
    
 <span data-ttu-id="cdc87-119">_Лпппропаррай_</span><span class="sxs-lookup"><span data-stu-id="cdc87-119">_lppPropArray_</span></span>
  
> <span data-ttu-id="cdc87-120">вышли Указатель на указатель на извлеченные значения свойства.</span><span class="sxs-lookup"><span data-stu-id="cdc87-120">[out] A pointer to a pointer to the retrieved property values.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="cdc87-121">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="cdc87-121">Return value</span></span>

<span data-ttu-id="cdc87-122">S_OK</span><span class="sxs-lookup"><span data-stu-id="cdc87-122">S_OK</span></span> 
  
> <span data-ttu-id="cdc87-123">Значения свойств успешно получены.</span><span class="sxs-lookup"><span data-stu-id="cdc87-123">The property values were successfully retrieved.</span></span>
    
<span data-ttu-id="cdc87-124">МАПИ_В_ЕРРОРС_РЕТУРНЕД</span><span class="sxs-lookup"><span data-stu-id="cdc87-124">MAPI_W_ERRORS_RETURNED</span></span> 
  
> <span data-ttu-id="cdc87-125">Вызов выполнен успешно, но не удалось получить доступ к одному или нескольким свойствам.</span><span class="sxs-lookup"><span data-stu-id="cdc87-125">The call succeeded overall, but one or more properties could not be accessed.</span></span> <span data-ttu-id="cdc87-126">Элемент **аулпроптаг** значения свойства для каждого недоступного свойства имеет тип свойства пт_еррор и нулевой идентификатор.</span><span class="sxs-lookup"><span data-stu-id="cdc87-126">The **aulPropTag** member of the property value for each unavailable property has a property type of PT_ERROR and an identifier of zero.</span></span> <span data-ttu-id="cdc87-127">При возвращении этого предупреждения вызов должен обрабатываться как успешный.</span><span class="sxs-lookup"><span data-stu-id="cdc87-127">When this warning is returned, the call should be handled as successful.</span></span> <span data-ttu-id="cdc87-128">Чтобы проверить это предупреждение, используйте макрос **хр_фаилед** .</span><span class="sxs-lookup"><span data-stu-id="cdc87-128">To test for this warning, use the **HR_FAILED** macro.</span></span> <span data-ttu-id="cdc87-129">Дополнительные сведения см. [в разделе Использование макросов для обработки ошибок](using-macros-for-error-handling.md).</span><span class="sxs-lookup"><span data-stu-id="cdc87-129">For more information, see [Using Macros for Error Handling](using-macros-for-error-handling.md).</span></span>
    
<span data-ttu-id="cdc87-130">МАПИ_Е_ИНВАЛИД_ПАРАМЕТЕР</span><span class="sxs-lookup"><span data-stu-id="cdc87-130">MAPI_E_INVALID_PARAMETER</span></span> 
  
> <span data-ttu-id="cdc87-131">Нулевое значение передано в элемент **квалуес** структуры **спроптагаррай** , на который указывает _лппроптагаррай_.</span><span class="sxs-lookup"><span data-stu-id="cdc87-131">Zero was passed in the **cValues** member of the **SPropTagArray** structure pointed to by  _lpPropTagArray_.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="cdc87-132">Примечания</span><span class="sxs-lookup"><span data-stu-id="cdc87-132">Remarks</span></span>

<span data-ttu-id="cdc87-133">Метод **IMAPIProp::** /PROPS получает значения свойств одного или нескольких свойств объекта.</span><span class="sxs-lookup"><span data-stu-id="cdc87-133">The **IMAPIProp::GetProps** method obtains the property values of one or more properties of an object.</span></span> 
  
<span data-ttu-id="cdc87-134">Значения свойств возвращаются в том же порядке, в котором они были запрошены (то есть порядок свойств в массиве тегов свойств, на который указывает _лппроптагаррай_ , совпадает с порядком в массиве структур значений свойств, на который указывает _лпппропаррай _).</span><span class="sxs-lookup"><span data-stu-id="cdc87-134">The property values are returned in the same order as they were requested (that is, the order of properties in the property tag array pointed to by  _lpPropTagArray_ matches the order in the array of property value structures pointed to by  _lppPropArray_).</span></span> 
  
<span data-ttu-id="cdc87-135">Типы свойств, указанные в элементах **аулпроптаг** в массиве тегов свойств, указывают тип значения, которое должно возвращаться в элементе **value** каждой структуры значения свойства.</span><span class="sxs-lookup"><span data-stu-id="cdc87-135">The property types specified in the **aulPropTag** members of the property tag array indicate the type of value that should be returned in the **Value** member of each property value structure.</span></span> <span data-ttu-id="cdc87-136">Тем не менее, если вызывающему объекту не известен тип свойства, для типа в элементе **аулпроптаг** можно задать значение пт_унспеЦифиед.</span><span class="sxs-lookup"><span data-stu-id="cdc87-136">However, if the caller does not know the type of a property, the type in the **aulPropTag** member can be set instead to PT_UNSPECIFIED.</span></span> <span data-ttu-id="cdc87-137">При получении значения параметру **PROPS** присваивается правильный тип в элементе **аулпроптаг** структуры значений свойств для свойства.</span><span class="sxs-lookup"><span data-stu-id="cdc87-137">In retrieving the value, **GetProps** sets the correct type in the **aulPropTag** member of the property value structure for the property.</span></span> 
  
<span data-ttu-id="cdc87-138">Если типы свойств указаны в **спроптагаррай** в _лппроптагаррай_, то значения свойств в **Спропвалуе** , возвращенные в _лпппропаррай_ , имеют типы, которые точно соответствуют запрашиваемым типам, если не будет возвращено значение ошибки Вместо.</span><span class="sxs-lookup"><span data-stu-id="cdc87-138">If property types are specified in the **SPropTagArray** in  _lpPropTagArray_, the property values in the **SPropValue** returned in  _lppPropArray_ have types that exactly match the requested types, unless an error value is returned instead.</span></span> 
  
<span data-ttu-id="cdc87-139">Строковые свойства могут иметь один из двух типов свойств: ПТ_УНИКОДЕ для представления формата Юникода и PT_STRING8 для представления формата ANSI.</span><span class="sxs-lookup"><span data-stu-id="cdc87-139">String properties can have one of two property types: PT_UNICODE to represent the Unicode format and PT_STRING8 to represent the ANSI format.</span></span> <span data-ttu-id="cdc87-140">Если в параметре _ulFlags_ ЗАДАН флаг мапи_уникоде, то при невозможности определить соответствующий формат для свойства String он возвращает его значение в формате Юникод. \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="cdc87-140">If the MAPI_UNICODE flag is set in the  _ulFlags_ parameter, whenever **GetProps** cannot determine the appropriate format for a string property, it returns its value in the Unicode format.</span></span> <span data-ttu-id="cdc87-141">\*\*\*\* Свойства PROPS не могут определять точный тип свойства String в следующих ситуациях:</span><span class="sxs-lookup"><span data-stu-id="cdc87-141">**GetProps** cannot determine an exact string property type in the following situations:</span></span> 
  
- <span data-ttu-id="cdc87-142">Параметр _лппроптагаррай_ имеет значение null, чтобы запросить все свойства.</span><span class="sxs-lookup"><span data-stu-id="cdc87-142">The  _lpPropTagArray_ parameter is set to NULL to request all properties.</span></span> 
    
- <span data-ttu-id="cdc87-143">Элемент **аулпроптаг** включает значение пт_унспеЦифиед в качестве типа свойства в массиве тегов свойств.</span><span class="sxs-lookup"><span data-stu-id="cdc87-143">The **aulPropTag** member includes the value PT_UNSPECIFIED as its property type in the property tag array.</span></span> 
    
<span data-ttu-id="cdc87-144">Если для параметра _лппроптагаррай_ ЗАДАНО значение null, в результате которого извлекаются все свойства объекта без свойств, свойство- **PROPS** выполняет следующие действия:</span><span class="sxs-lookup"><span data-stu-id="cdc87-144">If the  _lpPropTagArray_ parameter is set to NULL to retrieve all of the properties of the object and no properties exist, **GetProps** does the following:</span></span> 
  
- <span data-ttu-id="cdc87-145">Возвращает значение S_OK.</span><span class="sxs-lookup"><span data-stu-id="cdc87-145">Returns S_OK.</span></span>
    
- <span data-ttu-id="cdc87-146">Задает значение 0 в качестве значения счетчика в элементе **квалуес** в структуре значения свойства.</span><span class="sxs-lookup"><span data-stu-id="cdc87-146">Sets the count value in the **cValues** member of the property value structure to 0.</span></span> 
    
- <span data-ttu-id="cdc87-147">Задает значение 0 для содержимого _лпквалуес_ .</span><span class="sxs-lookup"><span data-stu-id="cdc87-147">Sets the contents of  _lpcValues_ to 0.</span></span> 
    
- <span data-ttu-id="cdc87-148">Задает для _ЛПППРОПАРРАЙ_ значение null.</span><span class="sxs-lookup"><span data-stu-id="cdc87-148">Sets  _lppPropArray_ to NULL.</span></span> 
    
 <span data-ttu-id="cdc87-149">\*\*\*\* Свойства PROPS не должны возвращать свойства с несколькими значениями, для **квалуес** задано значение 0.</span><span class="sxs-lookup"><span data-stu-id="cdc87-149">**GetProps** must not return multiple-value properties with **cValues** set to 0.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="cdc87-150">Примечания для исполнителей</span><span class="sxs-lookup"><span data-stu-id="cdc87-150">Notes to implementers</span></span>

<span data-ttu-id="cdc87-151">ВыЗовите функцию [мапиаллокатебуффер](mapiallocatebuffer.md) , чтобы сначала выделить память для структуры [спропвалуе](spropvalue.md) , на которую указывает _лппроптагаррай_; Вызовите [мапиаллокатеморе](mapiallocatemore.md) , чтобы выделить дополнительную память, необходимую для членов структуры.</span><span class="sxs-lookup"><span data-stu-id="cdc87-151">Call the [MAPIAllocateBuffer](mapiallocatebuffer.md) function to allocate memory initially for the [SPropValue](spropvalue.md) structure pointed to by  _lpPropTagArray_; call [MAPIAllocateMore](mapiallocatemore.md) to allocate any additional memory needed for the structure's members.</span></span> 
  
<span data-ttu-id="cdc87-152">Возвращает МАПИ_В_ЕРРОРС_РЕТУРНЕД, если не удается получить значение для одного или нескольких запрошенных свойств.</span><span class="sxs-lookup"><span data-stu-id="cdc87-152">Return MAPI_W_ERRORS_RETURNED if you cannot retrieve the value for one or more of the requested properties.</span></span> <span data-ttu-id="cdc87-153">В структуре значение свойства задайте для параметра Тип элемента **аулпроптаг** значение пт_еррор и элемент **значение** — код состояния, описывающий ошибку.</span><span class="sxs-lookup"><span data-stu-id="cdc87-153">In the property value structure, set the type in the **aulPropTag** member to PT_ERROR and the **Value** member to a status code that describes the error.</span></span> <span data-ttu-id="cdc87-154">Например, если необходимо преобразовать строку в Юникод и не поддерживает Юникод, установите для элемента **value значение** мапи_е_бад_чарвидс.</span><span class="sxs-lookup"><span data-stu-id="cdc87-154">For example, if you have to convert a string to Unicode and do not support Unicode, set the **Value** member to MAPI_E_BAD_CHARWIDTH.</span></span> <span data-ttu-id="cdc87-155">Если свойство слишком велико, задайте для него значение МАПИ_Е_НОТ_ЕНАУГХ_МЕМОРИ.</span><span class="sxs-lookup"><span data-stu-id="cdc87-155">If the property is too large, set it to MAPI_E_NOT_ENOUGH_MEMORY.</span></span> <span data-ttu-id="cdc87-156">Если объект не поддерживает это свойство, задайте для него значение МАПИ_Е_НОТ_ФАУНД.</span><span class="sxs-lookup"><span data-stu-id="cdc87-156">If the object does not support the property, set it to MAPI_E_NOT_FOUND.</span></span> 
  
<span data-ttu-id="cdc87-157">Реализация метода props в поставщике удаленного \*\*\*\* транспорта должна возвращать значения свойств папки для свойств, запрашиваемых вызывающим абонентом.</span><span class="sxs-lookup"><span data-stu-id="cdc87-157">A remote transport provider's implementation of the **GetProps** method must return the folder's property values for properties requested by the caller.</span></span> <span data-ttu-id="cdc87-158">Ваша реализация должна выполнять следующие действия:</span><span class="sxs-lookup"><span data-stu-id="cdc87-158">Your implementation must do the following:</span></span> 
  
- <span data-ttu-id="cdc87-159">Выделите массив значений свойства, чтобы вернуться к вызывающему объекту, и сохраните его адрес в параметре указателя значения свойства, переданном для этой цели.</span><span class="sxs-lookup"><span data-stu-id="cdc87-159">Allocate a property value array to return to the caller and store its address in the property value pointer parameter passed in for that purpose.</span></span>
    
- <span data-ttu-id="cdc87-160">Скопируйте теги свойств из свойств папки в теги свойств в массиве значений свойства в соответствии с массивом тегов свойств, передаваемых в свойства **PROPS**.</span><span class="sxs-lookup"><span data-stu-id="cdc87-160">Copy the property tags from the folder's properties into the property tags in the property value array according to the array of property tags passed to **GetProps**.</span></span>
    
- <span data-ttu-id="cdc87-161">Убедитесь, что тип свойства задан для всех тегов свойств, которые передаются в свойствах **PROPS**.</span><span class="sxs-lookup"><span data-stu-id="cdc87-161">Ensure that the property type is set for all property tags passed to **GetProps**.</span></span> <span data-ttu-id="cdc87-162">Вызывающий абонент может передавать тип свойства ПТ_УНСПЕЦИФИЕД, в этом случае параметру \*\*\*\* GetProperty необходимо задать правильный тип свойства для тега этого свойства.</span><span class="sxs-lookup"><span data-stu-id="cdc87-162">The caller can pass in a property type of PT_UNSPECIFIED, in which case **GetProps** must set the correct property type for that property tag.</span></span> 
    
- <span data-ttu-id="cdc87-163">Задайте значение каждого свойства в массиве значений свойства в соответствии с его тегом.</span><span class="sxs-lookup"><span data-stu-id="cdc87-163">Set the value of each property in the property value array according to its tag.</span></span> <span data-ttu-id="cdc87-164">Например, если в качестве тега свойства, запрошенного вызывающим абонентом, задано значение **пр_обжект_типе** ([PidTagObjectType](pidtagobjecttype-canonical-property.md)), то параметру- **PROPS** можно присвоить значение мапи_фолдер.</span><span class="sxs-lookup"><span data-stu-id="cdc87-164">For example, if the property tag requested by the caller is **PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md)), **GetProps** can set the value to MAPI_FOLDER.</span></span> 
    
- <span data-ttu-id="cdc87-165">Если вызывающий абонент передает все теги свойств, которые не обрабатываются в вашей реализации, можно установить для тега свойства значение ПТ_ЕРРОР для этих свойств и задать для свойства значение МАПИ_Е_НОТ_ФАУНД.</span><span class="sxs-lookup"><span data-stu-id="cdc87-165">If the caller passes in any property tags that your implementation does not handle, you can set the property tag to PT_ERROR for those properties, and set the property value to MAPI_E_NOT_FOUND.</span></span>
    
- <span data-ttu-id="cdc87-166">Возвращает значение S_OK при отсутствии ошибок или МАПИ_В_ЕРРОРС_РЕТУРНЕД при возникновении ошибок.</span><span class="sxs-lookup"><span data-stu-id="cdc87-166">Return S_OK if no errors occurred or MAPI_W_ERRORS_RETURNED if there were errors.</span></span>
    
<span data-ttu-id="cdc87-167">Реализация метода props в поставщике удаленного \*\*\*\* транспорта должна поддерживать следующие свойства по крайней мере:</span><span class="sxs-lookup"><span data-stu-id="cdc87-167">A remote transport provider's implementation of the **GetProps** method must support the following properties at a minimum:</span></span> 
  
- <span data-ttu-id="cdc87-168">**Пр_акцесс** ([PidTagAccess](pidtagaccess-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="cdc87-168">**PR_ACCESS** ([PidTagAccess](pidtagaccess-canonical-property.md))</span></span>
    
- <span data-ttu-id="cdc87-169">**Пр_акцесс_левел** ([PidTagAccessLevel](pidtagaccesslevel-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="cdc87-169">**PR_ACCESS_LEVEL** ([PidTagAccessLevel](pidtagaccesslevel-canonical-property.md))</span></span>
    
- <span data-ttu-id="cdc87-170">**Пр_ассок_контент_каунт** ([PidTagAssociatedContentCount](pidtagassociatedcontentcount-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="cdc87-170">**PR_ASSOC_CONTENT_COUNT** ([PidTagAssociatedContentCount](pidtagassociatedcontentcount-canonical-property.md))</span></span>
    
- <span data-ttu-id="cdc87-171">**Пр_контент_каунт** ([PidTagContentCount](pidtagcontentcount-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="cdc87-171">**PR_CONTENT_COUNT** ([PidTagContentCount](pidtagcontentcount-canonical-property.md))</span></span>
    
- <span data-ttu-id="cdc87-172">**Пр_креатион_тиме** ([PidTagCreationTime](pidtagcreationtime-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="cdc87-172">**PR_CREATION_TIME** ([PidTagCreationTime](pidtagcreationtime-canonical-property.md))</span></span>
    
- <span data-ttu-id="cdc87-173">**Пр_дисплай_наме** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="cdc87-173">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span></span>
    
- <span data-ttu-id="cdc87-174">**Пр_дисплай_типе** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="cdc87-174">**PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md))</span></span>
    
- <span data-ttu-id="cdc87-175">**Пр_фолдер_типе** ([PidTagFolderType](pidtagfoldertype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="cdc87-175">**PR_FOLDER_TYPE** ([PidTagFolderType](pidtagfoldertype-canonical-property.md))</span></span>
    
- <span data-ttu-id="cdc87-176">**ПР_ОБЖЕКТ_ТИПЕ**</span><span class="sxs-lookup"><span data-stu-id="cdc87-176">**PR_OBJECT_TYPE**</span></span>
    
- <span data-ttu-id="cdc87-177">**Пр_субфолдерс** ([PidTagSubfolders](pidtagsubfolders-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="cdc87-177">**PR_SUBFOLDERS** ([PidTagSubfolders](pidtagsubfolders-canonical-property.md))</span></span>
    
## <a name="notes-to-callers"></a><span data-ttu-id="cdc87-178">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="cdc87-178">Notes to callers</span></span>

<span data-ttu-id="cdc87-179">Для свойств типа ПТ_ОБЖЕКТ вызовите метод [IMAPIProp:: опенпроперти](imapiprop-openproperty.md) вместо PROPS. \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="cdc87-179">For properties of type PT_OBJECT, call the [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method instead of **GetProps**.</span></span> 
  
<span data-ttu-id="cdc87-180">Для защищенных свойств не рекомендуется извлекать их с помощью вызова \*\*\*\* метода лпппроптагаррай, если для параметра __ задано значение null.</span><span class="sxs-lookup"><span data-stu-id="cdc87-180">For secure properties, do not expect to retrieve them by calling **GetProps** with the  _lppPropTagArray_ parameter set to NULL.</span></span> <span data-ttu-id="cdc87-181">При вызове метода PROPS необходимо явно задать идентификатор безопасного свойства в элементе **аулпроптаг** в массиве тегов свойств. \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="cdc87-181">You must explicitly set a secure property's identifier in the **aulPropTag** member of its property tag array when you call **GetProps**.</span></span> <span data-ttu-id="cdc87-182">Когда и как доступно безопасное свойство, у поставщика услуг.</span><span class="sxs-lookup"><span data-stu-id="cdc87-182">When and how a secure property is available is up to the service provider.</span></span> 
  
<span data-ttu-id="cdc87-183">Освободите возвращаемую структуру **спропвалуе** , вызвав функцию [мапифрибуффер](mapifreebuffer.md) только в том случае, если метод **PROPS** возвращает значение S_OK или мапи_в_еррорс_ретурнед.</span><span class="sxs-lookup"><span data-stu-id="cdc87-183">Free the returned **SPropValue** structure by calling the [MAPIFreeBuffer](mapifreebuffer.md) function only if **GetProps** returns S_OK or MAPI_W_ERRORS_RETURNED.</span></span> 
  
<span data-ttu-id="cdc87-184">Если **PROPS** возвращает мапи_в_еррорс_ретурнед, так как ему не удалось получить доступ к одному или нескольким свойствам, проверьте теги свойств возвращаемых свойств.</span><span class="sxs-lookup"><span data-stu-id="cdc87-184">If **GetProps** returns MAPI_W_ERRORS_RETURNED because it could not access one or more properties, check the property tags of the returned properties.</span></span> <span data-ttu-id="cdc87-185">Свойства Failed будут иметь следующие значения в структуре значений свойств:</span><span class="sxs-lookup"><span data-stu-id="cdc87-185">The failed properties will have the following values set in their property value structure:</span></span> 
  
- <span data-ttu-id="cdc87-186">Тип свойства в элементе **аулпроптаг** в наборе пт_еррор.</span><span class="sxs-lookup"><span data-stu-id="cdc87-186">The property type in the **aulPropTag** member set to PT_ERROR.</span></span> 
    
- <span data-ttu-id="cdc87-187">Значение свойства в элементе **value** устанавливается равным коду состояния ошибки, например мапи_е_нот_фаунд.</span><span class="sxs-lookup"><span data-stu-id="cdc87-187">The property value in the **Value** member set to a status code for the error, such as MAPI_E_NOT_FOUND.</span></span> 
    
<span data-ttu-id="cdc87-188">Свойства, которые не удалось получить из-за слишком большого размера для удобного возврата в структуре значений свойств, имеют **значение** мапи_е_нот_енаугх_мемори.</span><span class="sxs-lookup"><span data-stu-id="cdc87-188">Properties that fail because they are too large to conveniently be returned in the property value structure have their **Value** member set to MAPI_E_NOT_ENOUGH_MEMORY.</span></span> <span data-ttu-id="cdc87-189">Обычно это происходит со строковыми или двоичными свойствами типа PT_STRING8, ПТ_УНИКОДЕ или ПТ_БИНАРИ, когда значение свойства равно 4 КБ или больше.</span><span class="sxs-lookup"><span data-stu-id="cdc87-189">Typically, this occurs with string or binary properties of type PT_STRING8, PT_UNICODE, or PT_BINARY when the value of the property is 4 KB or larger.</span></span> <span data-ttu-id="cdc87-190">Call **IMAPIProp:: опенпроперти** для получения больших свойств.</span><span class="sxs-lookup"><span data-stu-id="cdc87-190">Call **IMAPIProp::OpenProperty** to retrieve large properties.</span></span> 
  
<span data-ttu-id="cdc87-191">Не все реализации методов **PROPS** поддерживают как формат Юникод, так и формат ANSI для символьных строк.</span><span class="sxs-lookup"><span data-stu-id="cdc87-191">Not all implementations of **GetProps** support both the Unicode and ANSI formats for character strings.</span></span> <span data-ttu-id="cdc87-192">Если конкретному свойству требуется преобразование строкового \*\*\*\* формата, а PROPS не поддерживают его, элементу Value для этого свойства присваивается **значение** мапи_е_бад_чарвидс.</span><span class="sxs-lookup"><span data-stu-id="cdc87-192">When a particular property requires string format conversion and **GetProps** cannot support it, the **Value** member for the property is set to MAPI_E_BAD_CHARWIDTH.</span></span> 
  
<span data-ttu-id="cdc87-193">Чтобы проверить, является ли PST-файл PST SharePoint, подключите PST-файл с помощью [IMAPISession:: опенмсгсторе](imapisession-openmsgstore.md), а затем вызовите команду GetProperty для объекта хранилища сообщений, запрашивающего это свойство. \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="cdc87-193">To check if a PST is a SharePoint PST, mount the PST using [IMAPISession::OpenMsgStore](imapisession-openmsgstore.md), then call **GetProps** on the message store object requesting this property.</span></span> <span data-ttu-id="cdc87-194">Если он существует, можно предположить, что PST-файл настроен для SharePoint; в противном случае PST-файл не был настроен как PST-файл SharePoint.</span><span class="sxs-lookup"><span data-stu-id="cdc87-194">If it exists, you can assume the PST has been configured for SharePoint; if not, the PST has not been configured as a SharePoint PST.</span></span> 
  
<span data-ttu-id="cdc87-195">Дополнительные сведения о том, как использовать \*\*\*\* свойства, чтобы получить доступ к свойствам, можно узнать в статье [Получение свойств MAPI](retrieving-mapi-properties.md).</span><span class="sxs-lookup"><span data-stu-id="cdc87-195">For more information about how to use **GetProps** to access properties, see [Retrieving MAPI Properties](retrieving-mapi-properties.md).</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="cdc87-196">Справочные материалы по MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="cdc87-196">MFCMAPI reference</span></span>

<span data-ttu-id="cdc87-197">Пример кода MFCMAPI указан в приведенной ниже таблице.</span><span class="sxs-lookup"><span data-stu-id="cdc87-197">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="cdc87-198">**Файл**</span><span class="sxs-lookup"><span data-stu-id="cdc87-198">**File**</span></span>|<span data-ttu-id="cdc87-199">**Функция**</span><span class="sxs-lookup"><span data-stu-id="cdc87-199">**Function**</span></span>|<span data-ttu-id="cdc87-200">**Примечание**</span><span class="sxs-lookup"><span data-stu-id="cdc87-200">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="cdc87-201">Мапифунктионс. cpp</span><span class="sxs-lookup"><span data-stu-id="cdc87-201">MAPIFunctions.cpp</span></span>  <br/> |<span data-ttu-id="cdc87-202">Жетпропснулл</span><span class="sxs-lookup"><span data-stu-id="cdc87-202">GetPropsNULL</span></span>  <br/> |<span data-ttu-id="cdc87-203">MFCMAPI использует метод **IMAPIProp::** , чтобы получить все свойства объекта, ПЕРЕДАВ значение null или массив, возвращенный методом [IMAPIProp:: жетпроплист](imapiprop-getproplist.md) в параметре _лппроптагаррай_ .</span><span class="sxs-lookup"><span data-stu-id="cdc87-203">MFCMAPI uses the **IMAPIProp::GetProps** method to obtain all properties for an object by passing either NULL or the array returned by the [IMAPIProp::GetPropList](imapiprop-getproplist.md) method in the  _lpPropTagArray_ parameter.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="cdc87-204">См. также</span><span class="sxs-lookup"><span data-stu-id="cdc87-204">See also</span></span>



[<span data-ttu-id="cdc87-205">IMAPIProp::GetPropList</span><span class="sxs-lookup"><span data-stu-id="cdc87-205">IMAPIProp::GetPropList</span></span>](imapiprop-getproplist.md)
  
[<span data-ttu-id="cdc87-206">IMAPIProp::OpenProperty</span><span class="sxs-lookup"><span data-stu-id="cdc87-206">IMAPIProp::OpenProperty</span></span>](imapiprop-openproperty.md)
  
[<span data-ttu-id="cdc87-207">MAPIAllocateBuffer</span><span class="sxs-lookup"><span data-stu-id="cdc87-207">MAPIAllocateBuffer</span></span>](mapiallocatebuffer.md)
  
[<span data-ttu-id="cdc87-208">MAPIAllocateMore</span><span class="sxs-lookup"><span data-stu-id="cdc87-208">MAPIAllocateMore</span></span>](mapiallocatemore.md)
  
[<span data-ttu-id="cdc87-209">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="cdc87-209">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="cdc87-210">SPropTagArray</span><span class="sxs-lookup"><span data-stu-id="cdc87-210">SPropTagArray</span></span>](sproptagarray.md)
  
[<span data-ttu-id="cdc87-211">SPropValue</span><span class="sxs-lookup"><span data-stu-id="cdc87-211">SPropValue</span></span>](spropvalue.md)
  
[<span data-ttu-id="cdc87-212">IMAPIProp : IUnknown</span><span class="sxs-lookup"><span data-stu-id="cdc87-212">IMAPIProp : IUnknown</span></span>](imapipropiunknown.md)


[<span data-ttu-id="cdc87-213">MFCMAPI как пример кода</span><span class="sxs-lookup"><span data-stu-id="cdc87-213">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)
  
[<span data-ttu-id="cdc87-214">Получение свойств MAPI</span><span class="sxs-lookup"><span data-stu-id="cdc87-214">Retrieving MAPI Properties</span></span>](retrieving-mapi-properties.md)
  
[<span data-ttu-id="cdc87-215">Использование макросов для обработки ошибок</span><span class="sxs-lookup"><span data-stu-id="cdc87-215">Using Macros for Error Handling</span></span>](using-macros-for-error-handling.md)

