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
description: '���� ���������� ���������: 9 ����� 2015 �.'
ms.openlocfilehash: 33351235db2a9a3f9d9b67f59e8356a0fa8abfa8
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19809033"
---
# <a name="imapipropgetprops"></a><span data-ttu-id="f7a2a-103">IMAPIProp::GetProps</span><span class="sxs-lookup"><span data-stu-id="f7a2a-103">IMAPIProp::GetProps</span></span>

  
  
<span data-ttu-id="f7a2a-104">**Применимо к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="f7a2a-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="f7a2a-105">Получает значение свойства из одного или нескольких свойств объекта.</span><span class="sxs-lookup"><span data-stu-id="f7a2a-105">Retrieves the property value of one or more properties of an object.</span></span>
  
```cpp
HRESULT GetProps(
  LPSPropTagArray lpPropTagArray,
  ULONG ulFlags,
  ULONG FAR * lpcValues,
  LPSPropValue FAR * lppPropArray
);
```

## <a name="parameters"></a><span data-ttu-id="f7a2a-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="f7a2a-106">Parameters</span></span>

 <span data-ttu-id="f7a2a-107">_lpPropTagArray_</span><span class="sxs-lookup"><span data-stu-id="f7a2a-107">_lpPropTagArray_</span></span>
  
> <span data-ttu-id="f7a2a-108">[in] Указатель на массив тегов свойств, чтобы указать свойства, значения которых нужно вернуть.</span><span class="sxs-lookup"><span data-stu-id="f7a2a-108">[in] A pointer to an array of property tags that identify the properties whose values are to be retrieved.</span></span> <span data-ttu-id="f7a2a-109">Параметр _lpPropTagArray_ должен иметь значение NULL, указывающее, что значения всех свойств объекта должны быть возвращены, укажите на структуру [SPropTagArray](sproptagarray.md) , содержит один или несколько тегов свойств.</span><span class="sxs-lookup"><span data-stu-id="f7a2a-109">The  _lpPropTagArray_ parameter must be either NULL, indicating that values for all properties of the object should be returned, or point to an [SPropTagArray](sproptagarray.md) structure that contains one or more property tags.</span></span> 
    
 <span data-ttu-id="f7a2a-110">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="f7a2a-110">_ulFlags_</span></span>
  
> <span data-ttu-id="f7a2a-111">[in] Битовая маска флаги, которое указывает формат для свойства, имеющие тип PT_UNSPECIFIED.</span><span class="sxs-lookup"><span data-stu-id="f7a2a-111">[in] A bitmask of flags that indicates the format for properties that have the type PT_UNSPECIFIED.</span></span> <span data-ttu-id="f7a2a-112">Можно задать следующий флаг:</span><span class="sxs-lookup"><span data-stu-id="f7a2a-112">The following flag can be set:</span></span>
    
<span data-ttu-id="f7a2a-113">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="f7a2a-113">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="f7a2a-114">Строковые значения для этих свойств должны возвращаться в формате Юникод.</span><span class="sxs-lookup"><span data-stu-id="f7a2a-114">The string values for these properties should be returned in the Unicode format.</span></span> <span data-ttu-id="f7a2a-115">Если флаг MAPI_UNICODE не установлен, строковые значения должны возвращаться в формате ANSI.</span><span class="sxs-lookup"><span data-stu-id="f7a2a-115">If the MAPI_UNICODE flag is not set, the string values should be returned in the ANSI format.</span></span>
    
 <span data-ttu-id="f7a2a-116">_lpcValues_</span><span class="sxs-lookup"><span data-stu-id="f7a2a-116">_lpcValues_</span></span>
  
> <span data-ttu-id="f7a2a-117">[out] Указатель на количество значений свойств, на который указывает параметр _lppPropArray_ .</span><span class="sxs-lookup"><span data-stu-id="f7a2a-117">[out] A pointer to a count of property values pointed to by the  _lppPropArray_ parameter.</span></span> <span data-ttu-id="f7a2a-118">Если _lppPropArray_ имеет значение NULL, содержимое параметра _lpcValues_ равно нулю.</span><span class="sxs-lookup"><span data-stu-id="f7a2a-118">If  _lppPropArray_ is NULL, the content of the  _lpcValues_ parameter is zero.</span></span> 
    
 <span data-ttu-id="f7a2a-119">_lppPropArray_</span><span class="sxs-lookup"><span data-stu-id="f7a2a-119">_lppPropArray_</span></span>
  
> <span data-ttu-id="f7a2a-120">[out] Указатель на указатель на извлеченное свойство значения.</span><span class="sxs-lookup"><span data-stu-id="f7a2a-120">[out] A pointer to a pointer to the retrieved property values.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="f7a2a-121">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="1">Return value</span></span>

<span data-ttu-id="f7a2a-122">ЗНАЧЕНИЕ S_OK</span><span class="sxs-lookup"><span data-stu-id="f7a2a-122">S_OK</span></span> 
  
> <span data-ttu-id="f7a2a-123">Значения свойств были успешно извлечен.</span><span class="sxs-lookup"><span data-stu-id="f7a2a-123">The property values were successfully retrieved.</span></span>
    
<span data-ttu-id="f7a2a-124">MAPI_W_ERRORS_RETURNED</span><span class="sxs-lookup"><span data-stu-id="f7a2a-124">MAPI_W_ERRORS_RETURNED</span></span> 
  
> <span data-ttu-id="f7a2a-125">Вызов завершился успешно в целом, но не удается получить доступ к одного или нескольких свойств.</span><span class="sxs-lookup"><span data-stu-id="f7a2a-125">The call succeeded overall, but one or more properties could not be accessed.</span></span> <span data-ttu-id="f7a2a-126">Член **aulPropTag** значение свойства для каждого свойства, недоступен имеет тип свойства PT_ERROR и идентификатора нулю.</span><span class="sxs-lookup"><span data-stu-id="f7a2a-126">The **aulPropTag** member of the property value for each unavailable property has a property type of PT_ERROR and an identifier of zero.</span></span> <span data-ttu-id="f7a2a-127">При возвращении этого предупреждения вызова необходимо обрабатывать об успешном завершении.</span><span class="sxs-lookup"><span data-stu-id="f7a2a-127">When this warning is returned, the call should be handled as successful.</span></span> <span data-ttu-id="f7a2a-128">Чтобы проверить это предупреждение, используйте **HR_FAILED** макрос.</span><span class="sxs-lookup"><span data-stu-id="f7a2a-128">To test for this warning, use the **HR_FAILED** macro.</span></span> <span data-ttu-id="f7a2a-129">Дополнительные сведения можно [С помощью макросов для обработки ошибок](using-macros-for-error-handling.md).</span><span class="sxs-lookup"><span data-stu-id="f7a2a-129">For more information, see [Using Macros for Error Handling](using-macros-for-error-handling.md).</span></span>
    
<span data-ttu-id="f7a2a-130">MAPI_E_INVALID_PARAMETER</span><span class="sxs-lookup"><span data-stu-id="f7a2a-130">MAPI_E_INVALID_PARAMETER</span></span> 
  
> <span data-ttu-id="f7a2a-131">Член **cValues** структуры **SPropTagArray** , на который указывает _lpPropTagArray_был передан нулю.</span><span class="sxs-lookup"><span data-stu-id="f7a2a-131">Zero was passed in the **cValues** member of the **SPropTagArray** structure pointed to by  _lpPropTagArray_.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="f7a2a-132">Замечания</span><span class="sxs-lookup"><span data-stu-id="f7a2a-132">Remarks</span></span>

<span data-ttu-id="f7a2a-133">Метод **IMAPIProp::GetProps** получает значения свойств из одного или нескольких свойств объекта.</span><span class="sxs-lookup"><span data-stu-id="f7a2a-133">The **IMAPIProp::GetProps** method obtains the property values of one or more properties of an object.</span></span> 
  
<span data-ttu-id="f7a2a-134">Значения свойств возвращаются в том же порядке, как они были запрошено (то есть, порядок свойств в массиве свойство tag указывает соответствия _lpPropTagArray_ порядке в массиве структур значение свойства указывает _lppPropArray _).</span><span class="sxs-lookup"><span data-stu-id="f7a2a-134">The property values are returned in the same order as they were requested (that is, the order of properties in the property tag array pointed to by  _lpPropTagArray_ matches the order in the array of property value structures pointed to by  _lppPropArray_).</span></span> 
  
<span data-ttu-id="f7a2a-135">Типы свойств, указанных в **aulPropTag** элементы массива тега свойства указывают тип значение, которое должны быть возвращены в элемент **значения** структуры значение каждого свойства.</span><span class="sxs-lookup"><span data-stu-id="f7a2a-135">The property types specified in the **aulPropTag** members of the property tag array indicate the type of value that should be returned in the **Value** member of each property value structure.</span></span> <span data-ttu-id="f7a2a-136">Тем не менее если вызывающий не имеет тип свойства, типа в элемент **aulPropTag** может быть присвоено вместо PT_UNSPECIFIED.</span><span class="sxs-lookup"><span data-stu-id="f7a2a-136">However, if the caller does not know the type of a property, the type in the **aulPropTag** member can be set instead to PT_UNSPECIFIED.</span></span> <span data-ttu-id="f7a2a-137">При получении значение **GetProps** задает правильный тип в член **aulPropTag** структуры значение свойства для свойства.</span><span class="sxs-lookup"><span data-stu-id="f7a2a-137">In retrieving the value, **GetProps** sets the correct type in the **aulPropTag** member of the property value structure for the property.</span></span> 
  
<span data-ttu-id="f7a2a-138">Если типы свойств заданы в **SPropTagArray** в _lpPropTagArray_, значения свойств в **SPropValue** , возвращаемых в _lppPropArray_ типами, точно соответствовать запрошенных типов, если не возвращаемое значение ошибки Вместо этого.</span><span class="sxs-lookup"><span data-stu-id="f7a2a-138">If property types are specified in the **SPropTagArray** in  _lpPropTagArray_, the property values in the **SPropValue** returned in  _lppPropArray_ have types that exactly match the requested types, unless an error value is returned instead.</span></span> 
  
<span data-ttu-id="f7a2a-139">Свойства строка может иметь одно из двух типов свойств: PT_UNICODE для представления формата Юникод и PT_STRING8 для представления формата ANSI.</span><span class="sxs-lookup"><span data-stu-id="f7a2a-139">String properties can have one of two property types: PT_UNICODE to represent the Unicode format and PT_STRING8 to represent the ANSI format.</span></span> <span data-ttu-id="f7a2a-140">Если флаг MAPI_UNICODE установлен в параметре _ulFlags_ каждый раз, когда **GetProps** не может определить соответствующий формат для свойства строки, возвращается его значение в формате Юникод.</span><span class="sxs-lookup"><span data-stu-id="f7a2a-140">If the MAPI_UNICODE flag is set in the  _ulFlags_ parameter, whenever **GetProps** cannot determine the appropriate format for a string property, it returns its value in the Unicode format.</span></span> <span data-ttu-id="f7a2a-141">**GetProps** не может определить тип свойства точной строки в следующих ситуациях:</span><span class="sxs-lookup"><span data-stu-id="f7a2a-141">**GetProps** cannot determine an exact string property type in the following situations:</span></span> 
  
- <span data-ttu-id="f7a2a-142">Параметр _lpPropTagArray_ задано значение NULL, чтобы запросить все свойства.</span><span class="sxs-lookup"><span data-stu-id="f7a2a-142">The  _lpPropTagArray_ parameter is set to NULL to request all properties.</span></span> 
    
- <span data-ttu-id="f7a2a-143">Член **aulPropTag** содержит значение PT_UNSPECIFIED в качестве свойства типа в массиве тега свойства.</span><span class="sxs-lookup"><span data-stu-id="f7a2a-143">The **aulPropTag** member includes the value PT_UNSPECIFIED as its property type in the property tag array.</span></span> 
    
<span data-ttu-id="f7a2a-144">Если параметр _lpPropTagArray_ задано значение NULL для извлечения всех свойств объекта, а свойства не существует, **GetProps** выполняет следующие действия.</span><span class="sxs-lookup"><span data-stu-id="f7a2a-144">If the  _lpPropTagArray_ parameter is set to NULL to retrieve all of the properties of the object and no properties exist, **GetProps** does the following:</span></span> 
  
- <span data-ttu-id="f7a2a-145">Возвращает значение S_OK.</span><span class="sxs-lookup"><span data-stu-id="f7a2a-145">Returns S_OK.</span></span>
    
- <span data-ttu-id="f7a2a-146">Задает значение числа в член **cValues** структуры свойство значение 0.</span><span class="sxs-lookup"><span data-stu-id="f7a2a-146">Sets the count value in the **cValues** member of the property value structure to 0.</span></span> 
    
- <span data-ttu-id="f7a2a-147">Задает содержимое _lpcValues_ 0.</span><span class="sxs-lookup"><span data-stu-id="f7a2a-147">Sets the contents of  _lpcValues_ to 0.</span></span> 
    
- <span data-ttu-id="f7a2a-148">Задает _lppPropArray_ значение NULL.</span><span class="sxs-lookup"><span data-stu-id="f7a2a-148">Sets  _lppPropArray_ to NULL.</span></span> 
    
 <span data-ttu-id="f7a2a-149">**GetProps** не должен возвращать, что свойства с несколькими значениями с **cValues** значение 0.</span><span class="sxs-lookup"><span data-stu-id="f7a2a-149">**GetProps** must not return multiple-value properties with **cValues** set to 0.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="f7a2a-150">Примечания для исполнителей</span><span class="sxs-lookup"><span data-stu-id="f7a2a-150">Notes to implementers</span></span>

<span data-ttu-id="f7a2a-151">Вызовите функцию [MAPIAllocateBuffer](mapiallocatebuffer.md) изначально выделить память для структуры [SPropValue](spropvalue.md) , на который указывает _lpPropTagArray_; вызов [MAPIAllocateMore](mapiallocatemore.md) распределения любой дополнительной памяти, необходимый для членов структуры.</span><span class="sxs-lookup"><span data-stu-id="f7a2a-151">Call the [MAPIAllocateBuffer](mapiallocatebuffer.md) function to allocate memory initially for the [SPropValue](spropvalue.md) structure pointed to by  _lpPropTagArray_; call [MAPIAllocateMore](mapiallocatemore.md) to allocate any additional memory needed for the structure's members.</span></span> 
  
<span data-ttu-id="f7a2a-152">Возвращает MAPI_W_ERRORS_RETURNED, если вы не сможете получить значение для одного или нескольких запрошенных свойств.</span><span class="sxs-lookup"><span data-stu-id="f7a2a-152">Return MAPI_W_ERRORS_RETURNED if you cannot retrieve the value for one or more of the requested properties.</span></span> <span data-ttu-id="f7a2a-153">В структуре значение свойства установите тип в **aulPropTag** к PT_ERROR, а **значение** код состояния, с описанием ошибки.</span><span class="sxs-lookup"><span data-stu-id="f7a2a-153">In the property value structure, set the type in the **aulPropTag** member to PT_ERROR and the **Value** member to a status code that describes the error.</span></span> <span data-ttu-id="f7a2a-154">Например если для преобразования строки Юникод и не поддерживает Юникод, установите **значение** равным MAPI_E_BAD_CHARWIDTH.</span><span class="sxs-lookup"><span data-stu-id="f7a2a-154">For example, if you have to convert a string to Unicode and do not support Unicode, set the **Value** member to MAPI_E_BAD_CHARWIDTH.</span></span> <span data-ttu-id="f7a2a-155">Если свойство имеет слишком большой, задайте значение MAPI_E_NOT_ENOUGH_MEMORY.</span><span class="sxs-lookup"><span data-stu-id="f7a2a-155">If the property is too large, set it to MAPI_E_NOT_ENOUGH_MEMORY.</span></span> <span data-ttu-id="f7a2a-156">Если объект не поддерживает свойство, присвойте этому параметру MAPI_E_NOT_FOUND.</span><span class="sxs-lookup"><span data-stu-id="f7a2a-156">If the object does not support the property, set it to MAPI_E_NOT_FOUND.</span></span> 
  
<span data-ttu-id="f7a2a-157">Реализация поставщика транспорта удаленного метода **GetProps** должен возвращать значения свойств папки для запрошенного вызывающим абонентом.</span><span class="sxs-lookup"><span data-stu-id="f7a2a-157">A remote transport provider's implementation of the **GetProps** method must return the folder's property values for properties requested by the caller.</span></span> <span data-ttu-id="f7a2a-158">Внедрения необходимо выполнить следующие действия.</span><span class="sxs-lookup"><span data-stu-id="f7a2a-158">Your implementation must do the following:</span></span> 
  
- <span data-ttu-id="f7a2a-159">Выделите массив значений свойство вернуться к вызывающему и сохранить его адрес с помощью параметра указатель значение свойства переданную для этой цели.</span><span class="sxs-lookup"><span data-stu-id="f7a2a-159">Allocate a property value array to return to the caller and store its address in the property value pointer parameter passed in for that purpose.</span></span>
    
- <span data-ttu-id="f7a2a-160">Копирование свойств папки тегов свойств в свойство теги в массиве значение свойства в соответствии с массива тегов свойств, переданной в **GetProps**.</span><span class="sxs-lookup"><span data-stu-id="f7a2a-160">Copy the property tags from the folder's properties into the property tags in the property value array according to the array of property tags passed to **GetProps**.</span></span>
    
- <span data-ttu-id="f7a2a-161">Убедитесь, что тип свойства для всех свойств тегов, переданной в **GetProps**.</span><span class="sxs-lookup"><span data-stu-id="f7a2a-161">Ensure that the property type is set for all property tags passed to **GetProps**.</span></span> <span data-ttu-id="f7a2a-162">В свойство типа PT_UNSPECIFIED, в котором case **GetProps** необходимо установить правильный тип для этого свойства тега должно пройти вызывающего абонента.</span><span class="sxs-lookup"><span data-stu-id="f7a2a-162">The caller can pass in a property type of PT_UNSPECIFIED, in which case **GetProps** must set the correct property type for that property tag.</span></span> 
    
- <span data-ttu-id="f7a2a-163">Задайте значение каждого свойства в массиве значение свойства в соответствии с его тег.</span><span class="sxs-lookup"><span data-stu-id="f7a2a-163">Set the value of each property in the property value array according to its tag.</span></span> <span data-ttu-id="f7a2a-164">Например если свойство тег, запрошенную вызывающим **PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md)), **GetProps** можно задать значение MAPI_FOLDER.</span><span class="sxs-lookup"><span data-stu-id="f7a2a-164">For example, if the property tag requested by the caller is **PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md)), **GetProps** can set the value to MAPI_FOLDER.</span></span> 
    
- <span data-ttu-id="f7a2a-165">Вызывающего абонента передает все теги свойства, которые не работают внедрения, можно установите свойство tag PT_ERROR для этих свойств и задайте для свойства значение MAPI_E_NOT_FOUND.</span><span class="sxs-lookup"><span data-stu-id="f7a2a-165">If the caller passes in any property tags that your implementation does not handle, you can set the property tag to PT_ERROR for those properties, and set the property value to MAPI_E_NOT_FOUND.</span></span>
    
- <span data-ttu-id="f7a2a-166">Возвращает значение S_OK, если ошибок не или MAPI_W_ERRORS_RETURNED при наличии ошибок.</span><span class="sxs-lookup"><span data-stu-id="f7a2a-166">Return S_OK if no errors occurred or MAPI_W_ERRORS_RETURNED if there were errors.</span></span>
    
<span data-ttu-id="f7a2a-167">Реализация поставщика транспорта удаленного метода **GetProps** должен поддерживать по крайней мере следующие свойства:</span><span class="sxs-lookup"><span data-stu-id="f7a2a-167">A remote transport provider's implementation of the **GetProps** method must support the following properties at a minimum:</span></span> 
  
- <span data-ttu-id="f7a2a-168">**PR_ACCESS** ([PidTagAccess](pidtagaccess-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="f7a2a-168">**PR_ACCESS** ([PidTagAccess](pidtagaccess-canonical-property.md))</span></span>
    
- <span data-ttu-id="f7a2a-169">**PR_ACCESS_LEVEL** ([PidTagAccessLevel](pidtagaccesslevel-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="f7a2a-169">**PR_ACCESS_LEVEL** ([PidTagAccessLevel](pidtagaccesslevel-canonical-property.md))</span></span>
    
- <span data-ttu-id="f7a2a-170">**PR_ASSOC_CONTENT_COUNT** ([PidTagAssociatedContentCount](pidtagassociatedcontentcount-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="f7a2a-170">**PR_ASSOC_CONTENT_COUNT** ([PidTagAssociatedContentCount](pidtagassociatedcontentcount-canonical-property.md))</span></span>
    
- <span data-ttu-id="f7a2a-171">**PR_CONTENT_COUNT** ([PidTagContentCount](pidtagcontentcount-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="f7a2a-171">**PR_CONTENT_COUNT** ([PidTagContentCount](pidtagcontentcount-canonical-property.md))</span></span>
    
- <span data-ttu-id="f7a2a-172">**PR_CREATION_TIME** ([PidTagCreationTime](pidtagcreationtime-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="f7a2a-172">**PR_CREATION_TIME** ([PidTagCreationTime](pidtagcreationtime-canonical-property.md))</span></span>
    
- <span data-ttu-id="f7a2a-173">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="f7a2a-173">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span></span>
    
- <span data-ttu-id="f7a2a-174">**PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="f7a2a-174">**PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md))</span></span>
    
- <span data-ttu-id="f7a2a-175">**PR_FOLDER_TYPE** ([PidTagFolderType](pidtagfoldertype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="f7a2a-175">**PR_FOLDER_TYPE** ([PidTagFolderType](pidtagfoldertype-canonical-property.md))</span></span>
    
- <span data-ttu-id="f7a2a-176">**PR_OBJECT_TYPE**</span><span class="sxs-lookup"><span data-stu-id="f7a2a-176">**PR_OBJECT_TYPE**</span></span>
    
- <span data-ttu-id="f7a2a-177">**PR_SUBFOLDERS** ([PidTagSubfolders](pidtagsubfolders-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="f7a2a-177">**PR_SUBFOLDERS** ([PidTagSubfolders](pidtagsubfolders-canonical-property.md))</span></span>
    
## <a name="notes-to-callers"></a><span data-ttu-id="f7a2a-178">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="f7a2a-178">Notes to callers</span></span>

<span data-ttu-id="f7a2a-179">Для свойства типа PT_OBJECT вызовите метод [IMAPIProp::OpenProperty](imapiprop-openproperty.md) вместо **GetProps**.</span><span class="sxs-lookup"><span data-stu-id="f7a2a-179">For properties of type PT_OBJECT, call the [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method instead of **GetProps**.</span></span> 
  
<span data-ttu-id="f7a2a-180">Для свойства безопасности не ожидается их извлечь путем вызова **GetProps** с параметром _lppPropTagArray_ задано значение NULL.</span><span class="sxs-lookup"><span data-stu-id="f7a2a-180">For secure properties, do not expect to retrieve them by calling **GetProps** with the  _lppPropTagArray_ parameter set to NULL.</span></span> <span data-ttu-id="f7a2a-181">Явным образом, необходимо установить идентификатор secure свойства в **aulPropTag** членом массива тег его свойства при вызове **GetProps**.</span><span class="sxs-lookup"><span data-stu-id="f7a2a-181">You must explicitly set a secure property's identifier in the **aulPropTag** member of its property tag array when you call **GetProps**.</span></span> <span data-ttu-id="f7a2a-182">Когда и как безопасной свойство доступно зависит от поставщика услуг.</span><span class="sxs-lookup"><span data-stu-id="f7a2a-182">When and how a secure property is available is up to the service provider.</span></span> 
  
<span data-ttu-id="f7a2a-183">Бесплатная загрузка возвращенные структура **SPropValue** путем вызова функции [MAPIFreeBuffer](mapifreebuffer.md) только в том случае, если **GetProps** возвращает значение S_OK или MAPI_W_ERRORS_RETURNED.</span><span class="sxs-lookup"><span data-stu-id="f7a2a-183">Free the returned **SPropValue** structure by calling the [MAPIFreeBuffer](mapifreebuffer.md) function only if **GetProps** returns S_OK or MAPI_W_ERRORS_RETURNED.</span></span> 
  
<span data-ttu-id="f7a2a-184">Если **GetProps** возвращает MAPI_W_ERRORS_RETURNED, так как он не удалось получить доступ к одной или нескольких свойств, проверьте свойство теги возвращаемых свойств.</span><span class="sxs-lookup"><span data-stu-id="f7a2a-184">If **GetProps** returns MAPI_W_ERRORS_RETURNED because it could not access one or more properties, check the property tags of the returned properties.</span></span> <span data-ttu-id="f7a2a-185">Сбой свойств будет иметь следующие значения, заданные в их структуру значение свойства:</span><span class="sxs-lookup"><span data-stu-id="f7a2a-185">The failed properties will have the following values set in their property value structure:</span></span> 
  
- <span data-ttu-id="f7a2a-186">Тип свойства в **aulPropTag** набор элементов для PT_ERROR.</span><span class="sxs-lookup"><span data-stu-id="f7a2a-186">The property type in the **aulPropTag** member set to PT_ERROR.</span></span> 
    
- <span data-ttu-id="f7a2a-187">Код состояния для ошибки, такие как MAPI_E_NOT_FOUND принимает значение свойства в элемент **значения** .</span><span class="sxs-lookup"><span data-stu-id="f7a2a-187">The property value in the **Value** member set to a status code for the error, such as MAPI_E_NOT_FOUND.</span></span> 
    
<span data-ttu-id="f7a2a-188">Свойства, завершившихся неудачно из-за слишком большого легко создавать будут возвращаться в структуре значение свойства имеют их **значение** набор элементов в MAPI_E_NOT_ENOUGH_MEMORY.</span><span class="sxs-lookup"><span data-stu-id="f7a2a-188">Properties that fail because they are too large to conveniently be returned in the property value structure have their **Value** member set to MAPI_E_NOT_ENOUGH_MEMORY.</span></span> <span data-ttu-id="f7a2a-189">Обычно это происходит с строку или двоичный свойств типа PT_STRING8, PT_UNICODE или PT_BINARY Если значение свойства 4 КБ или больше.</span><span class="sxs-lookup"><span data-stu-id="f7a2a-189">Typically, this occurs with string or binary properties of type PT_STRING8, PT_UNICODE, or PT_BINARY when the value of the property is 4 KB or larger.</span></span> <span data-ttu-id="f7a2a-190">Вызов **IMAPIProp::OpenProperty** для извлечения больших свойства.</span><span class="sxs-lookup"><span data-stu-id="f7a2a-190">Call **IMAPIProp::OpenProperty** to retrieve large properties.</span></span> 
  
<span data-ttu-id="f7a2a-191">Не все реализации **GetProps** поддерживает форматы ANSI и Юникод для строк.</span><span class="sxs-lookup"><span data-stu-id="f7a2a-191">Not all implementations of **GetProps** support both the Unicode and ANSI formats for character strings.</span></span> <span data-ttu-id="f7a2a-192">Когда определенное свойство требует преобразования формата строки и **GetProps** не поддерживает ее, элемент **значение** для свойства имеет значение MAPI_E_BAD_CHARWIDTH.</span><span class="sxs-lookup"><span data-stu-id="f7a2a-192">When a particular property requires string format conversion and **GetProps** cannot support it, the **Value** member for the property is set to MAPI_E_BAD_CHARWIDTH.</span></span> 
  
<span data-ttu-id="f7a2a-193">Чтобы проверить, является ли файл личных ПАПОК SharePoint PST, подключите PST-файлов с помощью [IMAPISession::OpenMsgStore](imapisession-openmsgstore.md), затем вызвать **GetProps** объекта хранилища сообщений, запрашивающего это свойство.</span><span class="sxs-lookup"><span data-stu-id="f7a2a-193">To check if a PST is a SharePoint PST, mount the PST using [IMAPISession::OpenMsgStore](imapisession-openmsgstore.md), then call **GetProps** on the message store object requesting this property.</span></span> <span data-ttu-id="f7a2a-194">Если он существует, можно предположить, что PST-файлов будет настроен для SharePoint; в противном случае PST не был настроен как SharePoint PST.</span><span class="sxs-lookup"><span data-stu-id="f7a2a-194">If it exists, you can assume the PST has been configured for SharePoint; if not, the PST has not been configured as a SharePoint PST.</span></span> 
  
<span data-ttu-id="f7a2a-195">Дополнительные сведения об использовании **GetProps** для доступа к свойствам можно [Извлечение свойств MAPI](retrieving-mapi-properties.md).</span><span class="sxs-lookup"><span data-stu-id="f7a2a-195">For more information about how to use **GetProps** to access properties, see [Retrieving MAPI Properties](retrieving-mapi-properties.md).</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="f7a2a-196">Справочник по mfcmapi (en)</span><span class="sxs-lookup"><span data-stu-id="f7a2a-196">MFCMAPI reference</span></span>

<span data-ttu-id="f7a2a-197">������ ���� mfcmapi (en) ���������� � ������� ����.</span><span class="sxs-lookup"><span data-stu-id="f7a2a-197">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="f7a2a-198">**����**</span><span class="sxs-lookup"><span data-stu-id="f7a2a-198">**File**</span></span>|<span data-ttu-id="f7a2a-199">**�������**</span><span class="sxs-lookup"><span data-stu-id="f7a2a-199">**Function**</span></span>|<span data-ttu-id="f7a2a-200">**�����������**</span><span class="sxs-lookup"><span data-stu-id="f7a2a-200">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="f7a2a-201">MAPIFunctions.cpp</span><span class="sxs-lookup"><span data-stu-id="f7a2a-201">MAPIFunctions.cpp</span></span>  <br/> |<span data-ttu-id="f7a2a-202">GetPropsNULL</span><span class="sxs-lookup"><span data-stu-id="f7a2a-202">GetPropsNULL</span></span>  <br/> |<span data-ttu-id="f7a2a-203">Mfcmapi (en) использует метод **IMAPIProp::GetProps** для получения всех свойств для объекта, передавая NULL или массива, возвращенных методом [IMAPIProp::GetPropList](imapiprop-getproplist.md) с помощью параметра _lpPropTagArray_ .</span><span class="sxs-lookup"><span data-stu-id="f7a2a-203">MFCMAPI uses the **IMAPIProp::GetProps** method to obtain all properties for an object by passing either NULL or the array returned by the [IMAPIProp::GetPropList](imapiprop-getproplist.md) method in the  _lpPropTagArray_ parameter.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="f7a2a-204">См. также</span><span class="sxs-lookup"><span data-stu-id="f7a2a-204">See also</span></span>



[<span data-ttu-id="f7a2a-205">IMAPIProp::GetPropList</span><span class="sxs-lookup"><span data-stu-id="f7a2a-205">IMAPIProp::GetPropList</span></span>](imapiprop-getproplist.md)
  
[<span data-ttu-id="f7a2a-206">IMAPIProp::OpenProperty</span><span class="sxs-lookup"><span data-stu-id="f7a2a-206">IMAPIProp::OpenProperty</span></span>](imapiprop-openproperty.md)
  
[<span data-ttu-id="f7a2a-207">MAPIAllocateBuffer</span><span class="sxs-lookup"><span data-stu-id="f7a2a-207">MAPIAllocateBuffer</span></span>](mapiallocatebuffer.md)
  
[<span data-ttu-id="f7a2a-208">MAPIAllocateMore</span><span class="sxs-lookup"><span data-stu-id="f7a2a-208">MAPIAllocateMore</span></span>](mapiallocatemore.md)
  
[<span data-ttu-id="f7a2a-209">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="f7a2a-209">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="f7a2a-210">SPropTagArray</span><span class="sxs-lookup"><span data-stu-id="f7a2a-210">SPropTagArray</span></span>](sproptagarray.md)
  
[<span data-ttu-id="f7a2a-211">SPropValue</span><span class="sxs-lookup"><span data-stu-id="f7a2a-211">SPropValue</span></span>](spropvalue.md)
  
[<span data-ttu-id="f7a2a-212">IMAPIProp: IUnknown</span><span class="sxs-lookup"><span data-stu-id="f7a2a-212">IMAPIProp : IUnknown</span></span>](imapipropiunknown.md)


[<span data-ttu-id="f7a2a-213">Mfcmapi (en) � �������� ������� ����</span><span class="sxs-lookup"><span data-stu-id="f7a2a-213">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)
  
[<span data-ttu-id="f7a2a-214">Извлечение свойств MAPI</span><span class="sxs-lookup"><span data-stu-id="f7a2a-214">Retrieving MAPI Properties</span></span>](retrieving-mapi-properties.md)
  
[<span data-ttu-id="f7a2a-215">Использование макросов для обработки ошибок</span><span class="sxs-lookup"><span data-stu-id="f7a2a-215">Using Macros for Error Handling</span></span>](using-macros-for-error-handling.md)

