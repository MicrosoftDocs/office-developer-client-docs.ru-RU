---
title: IMAPIPropGetProps
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
# <a name="imapipropgetprops"></a><span data-ttu-id="a4465-103">IMAPIProp::GetProps</span><span class="sxs-lookup"><span data-stu-id="a4465-103">IMAPIProp::GetProps</span></span>

  
  
<span data-ttu-id="a4465-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a4465-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a4465-105">Извлекает значение свойства одного или более свойств объекта.</span><span class="sxs-lookup"><span data-stu-id="a4465-105">Retrieves the property value of one or more properties of an object.</span></span>
  
```cpp
HRESULT GetProps(
  LPSPropTagArray lpPropTagArray,
  ULONG ulFlags,
  ULONG FAR * lpcValues,
  LPSPropValue FAR * lppPropArray
);
```

## <a name="parameters"></a><span data-ttu-id="a4465-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="a4465-106">Parameters</span></span>

 <span data-ttu-id="a4465-107">_lpPropTagArray_</span><span class="sxs-lookup"><span data-stu-id="a4465-107">_lpPropTagArray_</span></span>
  
> <span data-ttu-id="a4465-108">[in] Указатель на массив тегов свойств, которые определяют свойства, значения которых необходимо получить.</span><span class="sxs-lookup"><span data-stu-id="a4465-108">[in] A pointer to an array of property tags that identify the properties whose values are to be retrieved.</span></span> <span data-ttu-id="a4465-109">Параметр  _lpPropTagArray_ должен иметь значение NULL, указывающее на то, что должны быть возвращены значения для всех свойств объекта, или указать структуру [SPropTagArray,](sproptagarray.md) которая содержит один или несколько тегов свойств.</span><span class="sxs-lookup"><span data-stu-id="a4465-109">The  _lpPropTagArray_ parameter must be either NULL, indicating that values for all properties of the object should be returned, or point to an [SPropTagArray](sproptagarray.md) structure that contains one or more property tags.</span></span> 
    
 <span data-ttu-id="a4465-110">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="a4465-110">_ulFlags_</span></span>
  
> <span data-ttu-id="a4465-111">[in] Битоваяmas флагов, которая указывает формат для свойств с типом PT_UNSPECIFIED.</span><span class="sxs-lookup"><span data-stu-id="a4465-111">[in] A bitmask of flags that indicates the format for properties that have the type PT_UNSPECIFIED.</span></span> <span data-ttu-id="a4465-112">Можно установить следующий флаг:</span><span class="sxs-lookup"><span data-stu-id="a4465-112">The following flag can be set:</span></span>
    
<span data-ttu-id="a4465-113">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="a4465-113">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="a4465-114">Строки этих свойств должны возвращаться в формате Юникод.</span><span class="sxs-lookup"><span data-stu-id="a4465-114">The string values for these properties should be returned in the Unicode format.</span></span> <span data-ttu-id="a4465-115">Если флаг MAPI_UNICODE не установлен, строки должны возвращаться в формате ANSI.</span><span class="sxs-lookup"><span data-stu-id="a4465-115">If the MAPI_UNICODE flag is not set, the string values should be returned in the ANSI format.</span></span>
    
 <span data-ttu-id="a4465-116">_lpcValues_</span><span class="sxs-lookup"><span data-stu-id="a4465-116">_lpcValues_</span></span>
  
> <span data-ttu-id="a4465-117">[out] Указатель на количество значений свойств, на которые указывает параметр _lppPropArray._</span><span class="sxs-lookup"><span data-stu-id="a4465-117">[out] A pointer to a count of property values pointed to by the  _lppPropArray_ parameter.</span></span> <span data-ttu-id="a4465-118">Если  _lppPropArray_ имеет значение NULL, содержимое параметра  _lpcValues_ — ноль.</span><span class="sxs-lookup"><span data-stu-id="a4465-118">If  _lppPropArray_ is NULL, the content of the  _lpcValues_ parameter is zero.</span></span> 
    
 <span data-ttu-id="a4465-119">_lppPropArray_</span><span class="sxs-lookup"><span data-stu-id="a4465-119">_lppPropArray_</span></span>
  
> <span data-ttu-id="a4465-120">[out] Указатель на указатель на полученные значения свойств.</span><span class="sxs-lookup"><span data-stu-id="a4465-120">[out] A pointer to a pointer to the retrieved property values.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="a4465-121">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="a4465-121">Return value</span></span>

<span data-ttu-id="a4465-122">S_OK</span><span class="sxs-lookup"><span data-stu-id="a4465-122">S_OK</span></span> 
  
> <span data-ttu-id="a4465-123">Значения свойств были успешно извлечены.</span><span class="sxs-lookup"><span data-stu-id="a4465-123">The property values were successfully retrieved.</span></span>
    
<span data-ttu-id="a4465-124">MAPI_W_ERRORS_RETURNED</span><span class="sxs-lookup"><span data-stu-id="a4465-124">MAPI_W_ERRORS_RETURNED</span></span> 
  
> <span data-ttu-id="a4465-125">Вызов в целом был успешным, но не удалось получить доступ к одному или более свойствам.</span><span class="sxs-lookup"><span data-stu-id="a4465-125">The call succeeded overall, but one or more properties could not be accessed.</span></span> <span data-ttu-id="a4465-126">Член **aulPropTag** значения свойства для каждого недоступного свойства имеет тип свойства PT_ERROR идентификатора 0.</span><span class="sxs-lookup"><span data-stu-id="a4465-126">The **aulPropTag** member of the property value for each unavailable property has a property type of PT_ERROR and an identifier of zero.</span></span> <span data-ttu-id="a4465-127">При возвращении этого предупреждения вызов должен быть обработан как успешный.</span><span class="sxs-lookup"><span data-stu-id="a4465-127">When this warning is returned, the call should be handled as successful.</span></span> <span data-ttu-id="a4465-128">Чтобы проверить это предупреждение, используйте **макрос** HR_FAILED.</span><span class="sxs-lookup"><span data-stu-id="a4465-128">To test for this warning, use the **HR_FAILED** macro.</span></span> <span data-ttu-id="a4465-129">Дополнительные сведения см. в [теме "Использование макроса для обработки ошибок".](using-macros-for-error-handling.md)</span><span class="sxs-lookup"><span data-stu-id="a4465-129">For more information, see [Using Macros for Error Handling](using-macros-for-error-handling.md).</span></span>
    
<span data-ttu-id="a4465-130">MAPI_E_INVALID_PARAMETER</span><span class="sxs-lookup"><span data-stu-id="a4465-130">MAPI_E_INVALID_PARAMETER</span></span> 
  
> <span data-ttu-id="a4465-131">Ноль был передан в **члене cValues** структуры **SPropTagArray,** на который указывает _lpPropTagArray._</span><span class="sxs-lookup"><span data-stu-id="a4465-131">Zero was passed in the **cValues** member of the **SPropTagArray** structure pointed to by  _lpPropTagArray_.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="a4465-132">Примечания</span><span class="sxs-lookup"><span data-stu-id="a4465-132">Remarks</span></span>

<span data-ttu-id="a4465-133">Метод **IMAPIProp::GetProps** получает значения свойств одного или более свойств объекта.</span><span class="sxs-lookup"><span data-stu-id="a4465-133">The **IMAPIProp::GetProps** method obtains the property values of one or more properties of an object.</span></span> 
  
<span data-ttu-id="a4465-134">Значения свойств возвращаются в том же порядке, в который они были запрощены (то есть порядок свойств в массиве тегов свойств, на который указывает _lpPropTagArray,_ соответствует порядку в массиве структур значений свойств, на которые указывает _lppPropArray)._</span><span class="sxs-lookup"><span data-stu-id="a4465-134">The property values are returned in the same order as they were requested (that is, the order of properties in the property tag array pointed to by  _lpPropTagArray_ matches the order in the array of property value structures pointed to by  _lppPropArray_).</span></span> 
  
<span data-ttu-id="a4465-135">Типы свойств, указанные в членах **aulPropTag** массива тегов свойств, указывают тип значения, которое должно быть возвращено в члене **Value** каждой структуры значений свойств.</span><span class="sxs-lookup"><span data-stu-id="a4465-135">The property types specified in the **aulPropTag** members of the property tag array indicate the type of value that should be returned in the **Value** member of each property value structure.</span></span> <span data-ttu-id="a4465-136">Однако если вызываемая часть не знает тип свойства, вместо этого можно установить тип в члене **aulPropTag** PT_UNSPECIFIED.</span><span class="sxs-lookup"><span data-stu-id="a4465-136">However, if the caller does not know the type of a property, the type in the **aulPropTag** member can be set instead to PT_UNSPECIFIED.</span></span> <span data-ttu-id="a4465-137">При искомом значении **GetProps** задает правильный тип в члене **aulPropTag** структуры значения свойства.</span><span class="sxs-lookup"><span data-stu-id="a4465-137">In retrieving the value, **GetProps** sets the correct type in the **aulPropTag** member of the property value structure for the property.</span></span> 
  
<span data-ttu-id="a4465-138">Если типы свойств указаны в **объекте SPropTagArray** в  _lpPropTagArray,_ значения свойств **в объекте SPropValue,** возвращаемом  _в lppPropArray,_ имеют типы, которые точно соответствуют запрашиваемым типам, если только не возвращается значение ошибки.</span><span class="sxs-lookup"><span data-stu-id="a4465-138">If property types are specified in the **SPropTagArray** in  _lpPropTagArray_, the property values in the **SPropValue** returned in  _lppPropArray_ have types that exactly match the requested types, unless an error value is returned instead.</span></span> 
  
<span data-ttu-id="a4465-139">Строковые свойства могут иметь один из двух типов свойств: PT_UNICODE для представления формата Юникод и PT_STRING8 для представления формата ANSI.</span><span class="sxs-lookup"><span data-stu-id="a4465-139">String properties can have one of two property types: PT_UNICODE to represent the Unicode format and PT_STRING8 to represent the ANSI format.</span></span> <span data-ttu-id="a4465-140">Если флаг MAPI_UNICODE задан в параметре  _ulFlags,_ каждый раз, когда **GetProps** не удается определить подходящий формат для строки свойства, он возвращает его значение в формате Юникод.</span><span class="sxs-lookup"><span data-stu-id="a4465-140">If the MAPI_UNICODE flag is set in the  _ulFlags_ parameter, whenever **GetProps** cannot determine the appropriate format for a string property, it returns its value in the Unicode format.</span></span> <span data-ttu-id="a4465-141">**GetProps** не может определить точный тип строки свойства в следующих ситуациях:</span><span class="sxs-lookup"><span data-stu-id="a4465-141">**GetProps** cannot determine an exact string property type in the following situations:</span></span> 
  
- <span data-ttu-id="a4465-142">Для  _параметра lpPropTagArray_ задано NULL для запроса всех свойств.</span><span class="sxs-lookup"><span data-stu-id="a4465-142">The  _lpPropTagArray_ parameter is set to NULL to request all properties.</span></span> 
    
- <span data-ttu-id="a4465-143">Член **aulPropTag** включает значение, PT_UNSPECIFIED в виде типа свойства в массиве тегов свойств.</span><span class="sxs-lookup"><span data-stu-id="a4465-143">The **aulPropTag** member includes the value PT_UNSPECIFIED as its property type in the property tag array.</span></span> 
    
<span data-ttu-id="a4465-144">Если для  _параметра lpPropTagArray_ задано NULL для получения всех свойств объекта, а свойства не существуют, **GetProps** делает следующее:</span><span class="sxs-lookup"><span data-stu-id="a4465-144">If the  _lpPropTagArray_ parameter is set to NULL to retrieve all of the properties of the object and no properties exist, **GetProps** does the following:</span></span> 
  
- <span data-ttu-id="a4465-145">Возвращает S_OK.</span><span class="sxs-lookup"><span data-stu-id="a4465-145">Returns S_OK.</span></span>
    
- <span data-ttu-id="a4465-146">Задает для значения подсчета в **члене cValues** структуры значений свойства значение 0.</span><span class="sxs-lookup"><span data-stu-id="a4465-146">Sets the count value in the **cValues** member of the property value structure to 0.</span></span> 
    
- <span data-ttu-id="a4465-147">Устанавливает для содержимого  _lpcValues_ 0.</span><span class="sxs-lookup"><span data-stu-id="a4465-147">Sets the contents of  _lpcValues_ to 0.</span></span> 
    
- <span data-ttu-id="a4465-148">Устанавливает _для lppPropArray nULL._</span><span class="sxs-lookup"><span data-stu-id="a4465-148">Sets  _lppPropArray_ to NULL.</span></span> 
    
 <span data-ttu-id="a4465-149">**GetProps** не должен возвращать свойства с несколькими значениями, для **значений cValue установлено** значение 0.</span><span class="sxs-lookup"><span data-stu-id="a4465-149">**GetProps** must not return multiple-value properties with **cValues** set to 0.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="a4465-150">Примечания для исполнителей</span><span class="sxs-lookup"><span data-stu-id="a4465-150">Notes to implementers</span></span>

<span data-ttu-id="a4465-151">Вызовите [функцию MAPIAllocateBuffer,](mapiallocatebuffer.md) чтобы изначально выделить память для [структуры SPropValue,](spropvalue.md) на который указывает  _lpPropTagArray;_ вызовите [MAPIAllocateMore,](mapiallocatemore.md) чтобы выделить дополнительную память, необходимую для членов структуры.</span><span class="sxs-lookup"><span data-stu-id="a4465-151">Call the [MAPIAllocateBuffer](mapiallocatebuffer.md) function to allocate memory initially for the [SPropValue](spropvalue.md) structure pointed to by  _lpPropTagArray_; call [MAPIAllocateMore](mapiallocatemore.md) to allocate any additional memory needed for the structure's members.</span></span> 
  
<span data-ttu-id="a4465-152">Возвращает MAPI_W_ERRORS_RETURNED, если не удается получить значение одного или более из запрашиваемого свойства.</span><span class="sxs-lookup"><span data-stu-id="a4465-152">Return MAPI_W_ERRORS_RETURNED if you cannot retrieve the value for one or more of the requested properties.</span></span> <span data-ttu-id="a4465-153">В структуре значений свойства установите для типа в члене **aulPropTag** значение PT_ERROR и значение в код состояния, описывая ошибку. </span><span class="sxs-lookup"><span data-stu-id="a4465-153">In the property value structure, set the type in the **aulPropTag** member to PT_ERROR and the **Value** member to a status code that describes the error.</span></span> <span data-ttu-id="a4465-154">Например, если необходимо преобразовать строку в Юникод и не  поддерживать Юникод, установите для MAPI_E_BAD_CHARWIDTH.</span><span class="sxs-lookup"><span data-stu-id="a4465-154">For example, if you have to convert a string to Unicode and do not support Unicode, set the **Value** member to MAPI_E_BAD_CHARWIDTH.</span></span> <span data-ttu-id="a4465-155">Если свойство слишком большое, установите для него MAPI_E_NOT_ENOUGH_MEMORY.</span><span class="sxs-lookup"><span data-stu-id="a4465-155">If the property is too large, set it to MAPI_E_NOT_ENOUGH_MEMORY.</span></span> <span data-ttu-id="a4465-156">Если объект не поддерживает свойство, установите для него MAPI_E_NOT_FOUND.</span><span class="sxs-lookup"><span data-stu-id="a4465-156">If the object does not support the property, set it to MAPI_E_NOT_FOUND.</span></span> 
  
<span data-ttu-id="a4465-157">Реализация метода **GetProps** удаленного поставщика транспорта должна возвращать значения свойств папки для свойств, запрашиваемого вызываемой программой.</span><span class="sxs-lookup"><span data-stu-id="a4465-157">A remote transport provider's implementation of the **GetProps** method must return the folder's property values for properties requested by the caller.</span></span> <span data-ttu-id="a4465-158">Реализация должна сделать следующее:</span><span class="sxs-lookup"><span data-stu-id="a4465-158">Your implementation must do the following:</span></span> 
  
- <span data-ttu-id="a4465-159">Вы можете выделить массив значений свойств для возврата вызываемой цели и сохранить его адрес в параметре указателя значения свойства, переданном для этой цели.</span><span class="sxs-lookup"><span data-stu-id="a4465-159">Allocate a property value array to return to the caller and store its address in the property value pointer parameter passed in for that purpose.</span></span>
    
- <span data-ttu-id="a4465-160">Скопируйте теги свойств из свойств папки в теги свойств в массиве значений свойств в соответствии с массивом тегов свойств, переданных **в GetProps.**</span><span class="sxs-lookup"><span data-stu-id="a4465-160">Copy the property tags from the folder's properties into the property tags in the property value array according to the array of property tags passed to **GetProps**.</span></span>
    
- <span data-ttu-id="a4465-161">Убедитесь, что для всех тегов свойств, переданных **в GetProps,** установлен тип свойства.</span><span class="sxs-lookup"><span data-stu-id="a4465-161">Ensure that the property type is set for all property tags passed to **GetProps**.</span></span> <span data-ttu-id="a4465-162">Вызываемая может передать тип свойства PT_UNSPECIFIED, в этом случае **GetProps** должен установить правильный тип свойства для этого тега свойства.</span><span class="sxs-lookup"><span data-stu-id="a4465-162">The caller can pass in a property type of PT_UNSPECIFIED, in which case **GetProps** must set the correct property type for that property tag.</span></span> 
    
- <span data-ttu-id="a4465-163">Установите значение каждого свойства в массиве значений свойств в соответствии с его тегом.</span><span class="sxs-lookup"><span data-stu-id="a4465-163">Set the value of each property in the property value array according to its tag.</span></span> <span data-ttu-id="a4465-164">Например, если запрашивается тег свойства **PR_OBJECT_TYPE** ([PidTagObjectType),](pidtagobjecttype-canonical-property.md) **GetProps** может установить значение MAPI_FOLDER.</span><span class="sxs-lookup"><span data-stu-id="a4465-164">For example, if the property tag requested by the caller is **PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md)), **GetProps** can set the value to MAPI_FOLDER.</span></span> 
    
- <span data-ttu-id="a4465-165">Если вызываемая передает какие-либо теги свойств, которые не обрабатываются реализацией, можно установить для тега свойства значение PT_ERROR для этих свойств и установить значение свойства MAPI_E_NOT_FOUND.</span><span class="sxs-lookup"><span data-stu-id="a4465-165">If the caller passes in any property tags that your implementation does not handle, you can set the property tag to PT_ERROR for those properties, and set the property value to MAPI_E_NOT_FOUND.</span></span>
    
- <span data-ttu-id="a4465-166">Возвращает S_OK, если ошибок не было или MAPI_W_ERRORS_RETURNED ошибки.</span><span class="sxs-lookup"><span data-stu-id="a4465-166">Return S_OK if no errors occurred or MAPI_W_ERRORS_RETURNED if there were errors.</span></span>
    
<span data-ttu-id="a4465-167">Реализация метода **GetProps** удаленного поставщика транспорта должна поддерживать как минимум следующие свойства:</span><span class="sxs-lookup"><span data-stu-id="a4465-167">A remote transport provider's implementation of the **GetProps** method must support the following properties at a minimum:</span></span> 
  
- <span data-ttu-id="a4465-168">**PR_ACCESS** ([PidTagAccess)](pidtagaccess-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="a4465-168">**PR_ACCESS** ([PidTagAccess](pidtagaccess-canonical-property.md))</span></span>
    
- <span data-ttu-id="a4465-169">**PR_ACCESS_LEVEL** ([PidTagAccessLevel)](pidtagaccesslevel-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="a4465-169">**PR_ACCESS_LEVEL** ([PidTagAccessLevel](pidtagaccesslevel-canonical-property.md))</span></span>
    
- <span data-ttu-id="a4465-170">**PR_ASSOC_CONTENT_COUNT** ([PidTagAssociatedContentCount)](pidtagassociatedcontentcount-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="a4465-170">**PR_ASSOC_CONTENT_COUNT** ([PidTagAssociatedContentCount](pidtagassociatedcontentcount-canonical-property.md))</span></span>
    
- <span data-ttu-id="a4465-171">**PR_CONTENT_COUNT** ([PidTagContentCount)](pidtagcontentcount-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="a4465-171">**PR_CONTENT_COUNT** ([PidTagContentCount](pidtagcontentcount-canonical-property.md))</span></span>
    
- <span data-ttu-id="a4465-172">**PR_CREATION_TIME** ([PidTagCreationTime)](pidtagcreationtime-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="a4465-172">**PR_CREATION_TIME** ([PidTagCreationTime](pidtagcreationtime-canonical-property.md))</span></span>
    
- <span data-ttu-id="a4465-173">**PR_DISPLAY_NAME** ([PidTagDisplayName)](pidtagdisplayname-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="a4465-173">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span></span>
    
- <span data-ttu-id="a4465-174">**PR_DISPLAY_TYPE** ([PidTagDisplayType)](pidtagdisplaytype-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="a4465-174">**PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md))</span></span>
    
- <span data-ttu-id="a4465-175">**PR_FOLDER_TYPE** ([PidTagFolderType)](pidtagfoldertype-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="a4465-175">**PR_FOLDER_TYPE** ([PidTagFolderType](pidtagfoldertype-canonical-property.md))</span></span>
    
- <span data-ttu-id="a4465-176">**PR_OBJECT_TYPE**</span><span class="sxs-lookup"><span data-stu-id="a4465-176">**PR_OBJECT_TYPE**</span></span>
    
- <span data-ttu-id="a4465-177">**PR_SUBFOLDERS** ([PidTagSubfolders)](pidtagsubfolders-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="a4465-177">**PR_SUBFOLDERS** ([PidTagSubfolders](pidtagsubfolders-canonical-property.md))</span></span>
    
## <a name="notes-to-callers"></a><span data-ttu-id="a4465-178">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="a4465-178">Notes to callers</span></span>

<span data-ttu-id="a4465-179">Для свойств типа PT_OBJECT вызвать метод [IMAPIProp::OpenProperty](imapiprop-openproperty.md) вместо **GetProps.**</span><span class="sxs-lookup"><span data-stu-id="a4465-179">For properties of type PT_OBJECT, call the [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method instead of **GetProps**.</span></span> 
  
<span data-ttu-id="a4465-180">Для безопасных свойств не следует рассчитывать на их извлечение путем вызова **GetProps** с параметром  _lppPropTagArray,_ установленным в NULL.</span><span class="sxs-lookup"><span data-stu-id="a4465-180">For secure properties, do not expect to retrieve them by calling **GetProps** with the  _lppPropTagArray_ parameter set to NULL.</span></span> <span data-ttu-id="a4465-181">При вызове **GetProps** необходимо явно установить идентификатор безопасного свойства в члене **aulPropTag** массива тегов свойств.</span><span class="sxs-lookup"><span data-stu-id="a4465-181">You must explicitly set a secure property's identifier in the **aulPropTag** member of its property tag array when you call **GetProps**.</span></span> <span data-ttu-id="a4465-182">Когда и как доступно безопасное свойство, может быть только у поставщика услуг.</span><span class="sxs-lookup"><span data-stu-id="a4465-182">When and how a secure property is available is up to the service provider.</span></span> 
  
<span data-ttu-id="a4465-183">Освободите возвращенную **структуру SPropValue,** вызывая функцию [MAPIFreeBuffer,](mapifreebuffer.md) только если **GetProps** возвращает S_OK или MAPI_W_ERRORS_RETURNED.</span><span class="sxs-lookup"><span data-stu-id="a4465-183">Free the returned **SPropValue** structure by calling the [MAPIFreeBuffer](mapifreebuffer.md) function only if **GetProps** returns S_OK or MAPI_W_ERRORS_RETURNED.</span></span> 
  
<span data-ttu-id="a4465-184">Если **GetProps** возвращает MAPI_W_ERRORS_RETURNED из-за того, что ему не удалось получить доступ к одному или более свойствам, проверьте теги свойств возвращенных свойств.</span><span class="sxs-lookup"><span data-stu-id="a4465-184">If **GetProps** returns MAPI_W_ERRORS_RETURNED because it could not access one or more properties, check the property tags of the returned properties.</span></span> <span data-ttu-id="a4465-185">В структуре значений свойств сбойных свойств будет иметь следующие значения:</span><span class="sxs-lookup"><span data-stu-id="a4465-185">The failed properties will have the following values set in their property value structure:</span></span> 
  
- <span data-ttu-id="a4465-186">Тип свойства в члене **aulPropTag** имеет PT_ERROR.</span><span class="sxs-lookup"><span data-stu-id="a4465-186">The property type in the **aulPropTag** member set to PT_ERROR.</span></span> 
    
- <span data-ttu-id="a4465-187">Значение свойства в члене **Value** имеет код состояния для ошибки, например MAPI_E_NOT_FOUND.</span><span class="sxs-lookup"><span data-stu-id="a4465-187">The property value in the **Value** member set to a status code for the error, such as MAPI_E_NOT_FOUND.</span></span> 
    
<span data-ttu-id="a4465-188">Свойства, которые не удается, так как они слишком большие, чтобы  удобно возвращаться в структуре значения свойства, имеют значение MAPI_E_NOT_ENOUGH_MEMORY.</span><span class="sxs-lookup"><span data-stu-id="a4465-188">Properties that fail because they are too large to conveniently be returned in the property value structure have their **Value** member set to MAPI_E_NOT_ENOUGH_MEMORY.</span></span> <span data-ttu-id="a4465-189">Обычно это происходит со строками или двоичными свойствами типа PT_STRING8, PT_UNICODE или PT_BINARY, если значение свойства составляет 4 КБ или больше.</span><span class="sxs-lookup"><span data-stu-id="a4465-189">Typically, this occurs with string or binary properties of type PT_STRING8, PT_UNICODE, or PT_BINARY when the value of the property is 4 KB or larger.</span></span> <span data-ttu-id="a4465-190">Вызовите **IMAPIProp::OpenProperty,** чтобы получить большие свойства.</span><span class="sxs-lookup"><span data-stu-id="a4465-190">Call **IMAPIProp::OpenProperty** to retrieve large properties.</span></span> 
  
<span data-ttu-id="a4465-191">Не все реализации **GetProps** поддерживают форматы Юникода и ANSI для строк символов.</span><span class="sxs-lookup"><span data-stu-id="a4465-191">Not all implementations of **GetProps** support both the Unicode and ANSI formats for character strings.</span></span> <span data-ttu-id="a4465-192">Если определенному свойству требуется преобразование формата строки  и **GetProps** не может его поддерживать, для значения свойства устанавливается значение MAPI_E_BAD_CHARWIDTH.</span><span class="sxs-lookup"><span data-stu-id="a4465-192">When a particular property requires string format conversion and **GetProps** cannot support it, the **Value** member for the property is set to MAPI_E_BAD_CHARWIDTH.</span></span> 
  
<span data-ttu-id="a4465-193">Чтобы проверить, является ли PST-объектом SharePoint, необходимо установить PST с помощью [IMAPISession::OpenMsgStore,](imapisession-openmsgstore.md)а затем вызвать **GetProps** на объекте хранилищ сообщений, запрашивающих это свойство.</span><span class="sxs-lookup"><span data-stu-id="a4465-193">To check if a PST is a SharePoint PST, mount the PST using [IMAPISession::OpenMsgStore](imapisession-openmsgstore.md), then call **GetProps** on the message store object requesting this property.</span></span> <span data-ttu-id="a4465-194">Если он существует, можно предположить, что PST настроен для SharePoint; В этом случае PST не был настроен в качестве PST-службы SharePoint.</span><span class="sxs-lookup"><span data-stu-id="a4465-194">If it exists, you can assume the PST has been configured for SharePoint; if not, the PST has not been configured as a SharePoint PST.</span></span> 
  
<span data-ttu-id="a4465-195">Дополнительные сведения об использовании **GetProps** для доступа к свойствам см. в подзапуске свойств [MAPI.](retrieving-mapi-properties.md)</span><span class="sxs-lookup"><span data-stu-id="a4465-195">For more information about how to use **GetProps** to access properties, see [Retrieving MAPI Properties](retrieving-mapi-properties.md).</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="a4465-196">Справочные материалы по MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="a4465-196">MFCMAPI reference</span></span>

<span data-ttu-id="a4465-197">Пример кода MFCMAPI указан в приведенной ниже таблице.</span><span class="sxs-lookup"><span data-stu-id="a4465-197">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="a4465-198">**Файл**</span><span class="sxs-lookup"><span data-stu-id="a4465-198">**File**</span></span>|<span data-ttu-id="a4465-199">**Функция**</span><span class="sxs-lookup"><span data-stu-id="a4465-199">**Function**</span></span>|<span data-ttu-id="a4465-200">**Примечание**</span><span class="sxs-lookup"><span data-stu-id="a4465-200">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="a4465-201">MAPIFunctions.cpp</span><span class="sxs-lookup"><span data-stu-id="a4465-201">MAPIFunctions.cpp</span></span>  <br/> |<span data-ttu-id="a4465-202">GetPropsNULL</span><span class="sxs-lookup"><span data-stu-id="a4465-202">GetPropsNULL</span></span>  <br/> |<span data-ttu-id="a4465-203">MFCMAPI использует метод **IMAPIProp::GetProps** для получения всех свойств объекта путем передачи NULL или массива, возвращаемого методом [IMAPIProp::GetPropList](imapiprop-getproplist.md) в параметре _lpPropTagArray._</span><span class="sxs-lookup"><span data-stu-id="a4465-203">MFCMAPI uses the **IMAPIProp::GetProps** method to obtain all properties for an object by passing either NULL or the array returned by the [IMAPIProp::GetPropList](imapiprop-getproplist.md) method in the  _lpPropTagArray_ parameter.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="a4465-204">См. также</span><span class="sxs-lookup"><span data-stu-id="a4465-204">See also</span></span>



[<span data-ttu-id="a4465-205">IMAPIProp::GetPropList</span><span class="sxs-lookup"><span data-stu-id="a4465-205">IMAPIProp::GetPropList</span></span>](imapiprop-getproplist.md)
  
[<span data-ttu-id="a4465-206">IMAPIProp::OpenProperty</span><span class="sxs-lookup"><span data-stu-id="a4465-206">IMAPIProp::OpenProperty</span></span>](imapiprop-openproperty.md)
  
[<span data-ttu-id="a4465-207">MAPIAllocateBuffer</span><span class="sxs-lookup"><span data-stu-id="a4465-207">MAPIAllocateBuffer</span></span>](mapiallocatebuffer.md)
  
[<span data-ttu-id="a4465-208">MAPIAllocateMore</span><span class="sxs-lookup"><span data-stu-id="a4465-208">MAPIAllocateMore</span></span>](mapiallocatemore.md)
  
[<span data-ttu-id="a4465-209">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="a4465-209">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="a4465-210">SPropTagArray</span><span class="sxs-lookup"><span data-stu-id="a4465-210">SPropTagArray</span></span>](sproptagarray.md)
  
[<span data-ttu-id="a4465-211">SPropValue</span><span class="sxs-lookup"><span data-stu-id="a4465-211">SPropValue</span></span>](spropvalue.md)
  
[<span data-ttu-id="a4465-212">IMAPIProp : IUnknown</span><span class="sxs-lookup"><span data-stu-id="a4465-212">IMAPIProp : IUnknown</span></span>](imapipropiunknown.md)


[<span data-ttu-id="a4465-213">MFCMAPI как пример кода</span><span class="sxs-lookup"><span data-stu-id="a4465-213">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)
  
[<span data-ttu-id="a4465-214">Искомые свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="a4465-214">Retrieving MAPI Properties</span></span>](retrieving-mapi-properties.md)
  
[<span data-ttu-id="a4465-215">Использование макроса для обработки ошибок</span><span class="sxs-lookup"><span data-stu-id="a4465-215">Using Macros for Error Handling</span></span>](using-macros-for-error-handling.md)

