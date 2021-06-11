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
# <a name="imapipropgetprops"></a><span data-ttu-id="1c089-103">IMAPIProp::GetProps</span><span class="sxs-lookup"><span data-stu-id="1c089-103">IMAPIProp::GetProps</span></span>

  
  
<span data-ttu-id="1c089-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1c089-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1c089-105">Извлекает значение свойства одного или более свойств объекта.</span><span class="sxs-lookup"><span data-stu-id="1c089-105">Retrieves the property value of one or more properties of an object.</span></span>
  
```cpp
HRESULT GetProps(
  LPSPropTagArray lpPropTagArray,
  ULONG ulFlags,
  ULONG FAR * lpcValues,
  LPSPropValue FAR * lppPropArray
);
```

## <a name="parameters"></a><span data-ttu-id="1c089-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="1c089-106">Parameters</span></span>

 <span data-ttu-id="1c089-107">_lpPropTagArray_</span><span class="sxs-lookup"><span data-stu-id="1c089-107">_lpPropTagArray_</span></span>
  
> <span data-ttu-id="1c089-108">[in] Указатель на массив тегов свойств, которые определяют свойства, значения которых должны быть извлечены.</span><span class="sxs-lookup"><span data-stu-id="1c089-108">[in] A pointer to an array of property tags that identify the properties whose values are to be retrieved.</span></span> <span data-ttu-id="1c089-109">Параметр  _lpPropTagArray_ должен быть либо NULL, указывающее, что значения для всех свойств объекта должны быть возвращены, либо указать на структуру [SPropTagArray,](sproptagarray.md) которая содержит один или несколько тегов свойств.</span><span class="sxs-lookup"><span data-stu-id="1c089-109">The  _lpPropTagArray_ parameter must be either NULL, indicating that values for all properties of the object should be returned, or point to an [SPropTagArray](sproptagarray.md) structure that contains one or more property tags.</span></span> 
    
 <span data-ttu-id="1c089-110">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="1c089-110">_ulFlags_</span></span>
  
> <span data-ttu-id="1c089-111">[in] Битмаска флагов, которая указывает формат свойств, которые имеют тип PT_UNSPECIFIED.</span><span class="sxs-lookup"><span data-stu-id="1c089-111">[in] A bitmask of flags that indicates the format for properties that have the type PT_UNSPECIFIED.</span></span> <span data-ttu-id="1c089-112">Можно установить следующий флаг:</span><span class="sxs-lookup"><span data-stu-id="1c089-112">The following flag can be set:</span></span>
    
<span data-ttu-id="1c089-113">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="1c089-113">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="1c089-114">Значения строк для этих свойств должны быть возвращены в формате Unicode.</span><span class="sxs-lookup"><span data-stu-id="1c089-114">The string values for these properties should be returned in the Unicode format.</span></span> <span data-ttu-id="1c089-115">Если флаг MAPI_UNICODE не установлен, строки должны быть возвращены в формате ANSI.</span><span class="sxs-lookup"><span data-stu-id="1c089-115">If the MAPI_UNICODE flag is not set, the string values should be returned in the ANSI format.</span></span>
    
 <span data-ttu-id="1c089-116">_lpcValues_</span><span class="sxs-lookup"><span data-stu-id="1c089-116">_lpcValues_</span></span>
  
> <span data-ttu-id="1c089-117">[вышел] Указатель на количество значений свойств, на которые указывает параметр _lppPropArray._</span><span class="sxs-lookup"><span data-stu-id="1c089-117">[out] A pointer to a count of property values pointed to by the  _lppPropArray_ parameter.</span></span> <span data-ttu-id="1c089-118">Если  _lppPropArray_ является NULL, содержимое  _параметра lpcValues_ нулевое.</span><span class="sxs-lookup"><span data-stu-id="1c089-118">If  _lppPropArray_ is NULL, the content of the  _lpcValues_ parameter is zero.</span></span> 
    
 <span data-ttu-id="1c089-119">_lppPropArray_</span><span class="sxs-lookup"><span data-stu-id="1c089-119">_lppPropArray_</span></span>
  
> <span data-ttu-id="1c089-120">[вышел] Указатель на указатель на извлеченные значения свойства.</span><span class="sxs-lookup"><span data-stu-id="1c089-120">[out] A pointer to a pointer to the retrieved property values.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="1c089-121">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="1c089-121">Return value</span></span>

<span data-ttu-id="1c089-122">S_OK</span><span class="sxs-lookup"><span data-stu-id="1c089-122">S_OK</span></span> 
  
> <span data-ttu-id="1c089-123">Значения свойств были успешно извлечены.</span><span class="sxs-lookup"><span data-stu-id="1c089-123">The property values were successfully retrieved.</span></span>
    
<span data-ttu-id="1c089-124">MAPI_W_ERRORS_RETURNED</span><span class="sxs-lookup"><span data-stu-id="1c089-124">MAPI_W_ERRORS_RETURNED</span></span> 
  
> <span data-ttu-id="1c089-125">Вызов удался в целом, но не удалось получить доступ к одному или более свойствам.</span><span class="sxs-lookup"><span data-stu-id="1c089-125">The call succeeded overall, but one or more properties could not be accessed.</span></span> <span data-ttu-id="1c089-126">Член **aulPropTag** значения свойства для каждого недоступного свойства имеет тип свойства PT_ERROR и идентификатор нуля.</span><span class="sxs-lookup"><span data-stu-id="1c089-126">The **aulPropTag** member of the property value for each unavailable property has a property type of PT_ERROR and an identifier of zero.</span></span> <span data-ttu-id="1c089-127">Когда это предупреждение возвращается, вызов должен быть обработан как успешный.</span><span class="sxs-lookup"><span data-stu-id="1c089-127">When this warning is returned, the call should be handled as successful.</span></span> <span data-ttu-id="1c089-128">Чтобы проверить это предупреждение, используйте **HR_FAILED** макрос.</span><span class="sxs-lookup"><span data-stu-id="1c089-128">To test for this warning, use the **HR_FAILED** macro.</span></span> <span data-ttu-id="1c089-129">Дополнительные сведения см. в [дополнительных сведениях Об использовании макроса для обработки ошибок.](using-macros-for-error-handling.md)</span><span class="sxs-lookup"><span data-stu-id="1c089-129">For more information, see [Using Macros for Error Handling](using-macros-for-error-handling.md).</span></span>
    
<span data-ttu-id="1c089-130">MAPI_E_INVALID_PARAMETER</span><span class="sxs-lookup"><span data-stu-id="1c089-130">MAPI_E_INVALID_PARAMETER</span></span> 
  
> <span data-ttu-id="1c089-131">Zero передается в **члене cValues** структуры **SPropTagArray,** на который указывает _lpPropTagArray._</span><span class="sxs-lookup"><span data-stu-id="1c089-131">Zero was passed in the **cValues** member of the **SPropTagArray** structure pointed to by  _lpPropTagArray_.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="1c089-132">Примечания</span><span class="sxs-lookup"><span data-stu-id="1c089-132">Remarks</span></span>

<span data-ttu-id="1c089-133">Метод **IMAPIProp::GetProps** получает значения свойств одного или более свойств объекта.</span><span class="sxs-lookup"><span data-stu-id="1c089-133">The **IMAPIProp::GetProps** method obtains the property values of one or more properties of an object.</span></span> 
  
<span data-ttu-id="1c089-134">Значения свойств возвращаются в том же порядке, что и запрашивалось (то есть порядок свойств в массиве тегов свойств, на которые указывает _lpPropTagArray,_ соответствует порядку в массиве структур значений свойств, на которые указывает _lppPropArray)._</span><span class="sxs-lookup"><span data-stu-id="1c089-134">The property values are returned in the same order as they were requested (that is, the order of properties in the property tag array pointed to by  _lpPropTagArray_ matches the order in the array of property value structures pointed to by  _lppPropArray_).</span></span> 
  
<span data-ttu-id="1c089-135">Типы свойств, указанные в **aulPropTag** в массиве тегов свойств, указывают тип значения, которое должно быть возвращено в члене **значения** каждой структуры значения свойства.</span><span class="sxs-lookup"><span data-stu-id="1c089-135">The property types specified in the **aulPropTag** members of the property tag array indicate the type of value that should be returned in the **Value** member of each property value structure.</span></span> <span data-ttu-id="1c089-136">Однако если вызываемая не знает тип свойства, тип в **члене aulPropTag** можно установить вместо PT_UNSPECIFIED.</span><span class="sxs-lookup"><span data-stu-id="1c089-136">However, if the caller does not know the type of a property, the type in the **aulPropTag** member can be set instead to PT_UNSPECIFIED.</span></span> <span data-ttu-id="1c089-137">При ирисовке значения **GetProps** задает правильный тип в **члене aulPropTag** структуры значения свойства для свойства.</span><span class="sxs-lookup"><span data-stu-id="1c089-137">In retrieving the value, **GetProps** sets the correct type in the **aulPropTag** member of the property value structure for the property.</span></span> 
  
<span data-ttu-id="1c089-138">Если типы свойств указаны в **SPropTagArray** в  _lpPropTagArray,_ значения свойств в **SPropValue,** возвращаемом  _в lppPropArray,_ имеют типы, которые точно соответствуют запрашиваемым типам, если вместо этого не будет возвращено значение ошибки.</span><span class="sxs-lookup"><span data-stu-id="1c089-138">If property types are specified in the **SPropTagArray** in  _lpPropTagArray_, the property values in the **SPropValue** returned in  _lppPropArray_ have types that exactly match the requested types, unless an error value is returned instead.</span></span> 
  
<span data-ttu-id="1c089-139">Свойства string могут иметь один из двух типов свойств: PT_UNICODE для представления формата Юникод и PT_STRING8 для представления формата ANSI.</span><span class="sxs-lookup"><span data-stu-id="1c089-139">String properties can have one of two property types: PT_UNICODE to represent the Unicode format and PT_STRING8 to represent the ANSI format.</span></span> <span data-ttu-id="1c089-140">Если флаг MAPI_UNICODE задан в параметре  _ulFlags,_ каждый раз, когда **GetProps** не может определить подходящий формат для свойства строки, он возвращает его значение в формате Unicode.</span><span class="sxs-lookup"><span data-stu-id="1c089-140">If the MAPI_UNICODE flag is set in the  _ulFlags_ parameter, whenever **GetProps** cannot determine the appropriate format for a string property, it returns its value in the Unicode format.</span></span> <span data-ttu-id="1c089-141">**GetProps** не может определить точный тип свойства строки в следующих ситуациях:</span><span class="sxs-lookup"><span data-stu-id="1c089-141">**GetProps** cannot determine an exact string property type in the following situations:</span></span> 
  
- <span data-ttu-id="1c089-142">Параметр  _lpPropTagArray_ задан nULL для запроса всех свойств.</span><span class="sxs-lookup"><span data-stu-id="1c089-142">The  _lpPropTagArray_ parameter is set to NULL to request all properties.</span></span> 
    
- <span data-ttu-id="1c089-143">Член **aulPropTag** включает значение PT_UNSPECIFIED как тип свойства в массиве тегов свойств.</span><span class="sxs-lookup"><span data-stu-id="1c089-143">The **aulPropTag** member includes the value PT_UNSPECIFIED as its property type in the property tag array.</span></span> 
    
<span data-ttu-id="1c089-144">Если параметр  _lpPropTagArray_ задан nULL для получения всех свойств объекта и не существует свойств, **GetProps** делает следующее:</span><span class="sxs-lookup"><span data-stu-id="1c089-144">If the  _lpPropTagArray_ parameter is set to NULL to retrieve all of the properties of the object and no properties exist, **GetProps** does the following:</span></span> 
  
- <span data-ttu-id="1c089-145">Возвращает S_OK.</span><span class="sxs-lookup"><span data-stu-id="1c089-145">Returns S_OK.</span></span>
    
- <span data-ttu-id="1c089-146">Задает значение отсчета в **члене cValues** структуры значения свойства до 0.</span><span class="sxs-lookup"><span data-stu-id="1c089-146">Sets the count value in the **cValues** member of the property value structure to 0.</span></span> 
    
- <span data-ttu-id="1c089-147">Задает содержимое  _lpcValues_ до 0.</span><span class="sxs-lookup"><span data-stu-id="1c089-147">Sets the contents of  _lpcValues_ to 0.</span></span> 
    
- <span data-ttu-id="1c089-148">Задает  _lppPropArray_ в NULL.</span><span class="sxs-lookup"><span data-stu-id="1c089-148">Sets  _lppPropArray_ to NULL.</span></span> 
    
 <span data-ttu-id="1c089-149">**GetProps** не должен возвращать свойства с несколькими значениями **с набором cValues** до 0.</span><span class="sxs-lookup"><span data-stu-id="1c089-149">**GetProps** must not return multiple-value properties with **cValues** set to 0.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="1c089-150">Примечания для исполнителей</span><span class="sxs-lookup"><span data-stu-id="1c089-150">Notes to implementers</span></span>

<span data-ttu-id="1c089-151">Вызов [функции MAPIAllocateBuffer](mapiallocatebuffer.md) для выделения памяти изначально для [структуры SPropValue,](spropvalue.md) на которые указывает  _lpPropTagArray;_ вызов [MAPIAllocateMore,](mapiallocatemore.md) чтобы выделить дополнительную память, необходимую для членов структуры.</span><span class="sxs-lookup"><span data-stu-id="1c089-151">Call the [MAPIAllocateBuffer](mapiallocatebuffer.md) function to allocate memory initially for the [SPropValue](spropvalue.md) structure pointed to by  _lpPropTagArray_; call [MAPIAllocateMore](mapiallocatemore.md) to allocate any additional memory needed for the structure's members.</span></span> 
  
<span data-ttu-id="1c089-152">Возврат MAPI_W_ERRORS_RETURNED, если вы не можете получить значение для одного или более запрашиваемого свойства.</span><span class="sxs-lookup"><span data-stu-id="1c089-152">Return MAPI_W_ERRORS_RETURNED if you cannot retrieve the value for one or more of the requested properties.</span></span> <span data-ttu-id="1c089-153">В структуре значения свойства установите тип в члене **aulPropTag** для PT_ERROR и участника **Value** к коду состояния, который описывает ошибку.</span><span class="sxs-lookup"><span data-stu-id="1c089-153">In the property value structure, set the type in the **aulPropTag** member to PT_ERROR and the **Value** member to a status code that describes the error.</span></span> <span data-ttu-id="1c089-154">Например, если вам необходимо преобразовать строку в Unicode и не поддерживать Юникод, установите для участника **Value** значение MAPI_E_BAD_CHARWIDTH.</span><span class="sxs-lookup"><span data-stu-id="1c089-154">For example, if you have to convert a string to Unicode and do not support Unicode, set the **Value** member to MAPI_E_BAD_CHARWIDTH.</span></span> <span data-ttu-id="1c089-155">Если свойство слишком большое, установите его MAPI_E_NOT_ENOUGH_MEMORY.</span><span class="sxs-lookup"><span data-stu-id="1c089-155">If the property is too large, set it to MAPI_E_NOT_ENOUGH_MEMORY.</span></span> <span data-ttu-id="1c089-156">Если объект не поддерживает свойство, установите его MAPI_E_NOT_FOUND.</span><span class="sxs-lookup"><span data-stu-id="1c089-156">If the object does not support the property, set it to MAPI_E_NOT_FOUND.</span></span> 
  
<span data-ttu-id="1c089-157">Реализация методом **GetProps** удаленного поставщика транспорта должна вернуть значения свойств папки для свойств, запрашиваемого вызываемой вызываемой.</span><span class="sxs-lookup"><span data-stu-id="1c089-157">A remote transport provider's implementation of the **GetProps** method must return the folder's property values for properties requested by the caller.</span></span> <span data-ttu-id="1c089-158">Реализация должна сделать следующее:</span><span class="sxs-lookup"><span data-stu-id="1c089-158">Your implementation must do the following:</span></span> 
  
- <span data-ttu-id="1c089-159">Выделим массив значений свойств, чтобы вернуться к вызываемой и сохранить его адрес в параметре указателя значения свойства, переданного для этой цели.</span><span class="sxs-lookup"><span data-stu-id="1c089-159">Allocate a property value array to return to the caller and store its address in the property value pointer parameter passed in for that purpose.</span></span>
    
- <span data-ttu-id="1c089-160">Скопируйте теги свойств из свойств папки в теги свойств в массиве значений свойства в соответствии с массивом тегов свойств, переданных **GetProps.**</span><span class="sxs-lookup"><span data-stu-id="1c089-160">Copy the property tags from the folder's properties into the property tags in the property value array according to the array of property tags passed to **GetProps**.</span></span>
    
- <span data-ttu-id="1c089-161">Убедитесь, что тип свойства установлен для всех тегов свойств, переданных **GetProps.**</span><span class="sxs-lookup"><span data-stu-id="1c089-161">Ensure that the property type is set for all property tags passed to **GetProps**.</span></span> <span data-ttu-id="1c089-162">Вызываемая может передаваться в типе свойства PT_UNSPECIFIED, в этом случае **GetProps** должен задать правильный тип свойства для этого тега свойства.</span><span class="sxs-lookup"><span data-stu-id="1c089-162">The caller can pass in a property type of PT_UNSPECIFIED, in which case **GetProps** must set the correct property type for that property tag.</span></span> 
    
- <span data-ttu-id="1c089-163">Установите значение каждого свойства в массиве значений свойства в соответствии с его тегом.</span><span class="sxs-lookup"><span data-stu-id="1c089-163">Set the value of each property in the property value array according to its tag.</span></span> <span data-ttu-id="1c089-164">Например, если тег свойства, запрашиваемого  звонивцом, PR_OBJECT_TYPE [(PidTagObjectType),](pidtagobjecttype-canonical-property.md) **GetProps** может задать значение MAPI_FOLDER.</span><span class="sxs-lookup"><span data-stu-id="1c089-164">For example, if the property tag requested by the caller is **PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md)), **GetProps** can set the value to MAPI_FOLDER.</span></span> 
    
- <span data-ttu-id="1c089-165">Если звонивка передает в теги свойств, которые не обрабатываются реализацией, можно установить тег свойства PT_ERROR для этих свойств и установить значение свойства MAPI_E_NOT_FOUND.</span><span class="sxs-lookup"><span data-stu-id="1c089-165">If the caller passes in any property tags that your implementation does not handle, you can set the property tag to PT_ERROR for those properties, and set the property value to MAPI_E_NOT_FOUND.</span></span>
    
- <span data-ttu-id="1c089-166">Возврат S_OK, если ошибки не произошли или MAPI_W_ERRORS_RETURNED если были ошибки.</span><span class="sxs-lookup"><span data-stu-id="1c089-166">Return S_OK if no errors occurred or MAPI_W_ERRORS_RETURNED if there were errors.</span></span>
    
<span data-ttu-id="1c089-167">Реализация метода **GetProps** для удаленного поставщика транспорта должна как минимум поддерживать следующие свойства:</span><span class="sxs-lookup"><span data-stu-id="1c089-167">A remote transport provider's implementation of the **GetProps** method must support the following properties at a minimum:</span></span> 
  
- <span data-ttu-id="1c089-168">**PR_ACCESS** [(PidTagAccess)](pidtagaccess-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="1c089-168">**PR_ACCESS** ([PidTagAccess](pidtagaccess-canonical-property.md))</span></span>
    
- <span data-ttu-id="1c089-169">**PR_ACCESS_LEVEL** [(PidTagAccessLevel](pidtagaccesslevel-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="1c089-169">**PR_ACCESS_LEVEL** ([PidTagAccessLevel](pidtagaccesslevel-canonical-property.md))</span></span>
    
- <span data-ttu-id="1c089-170">**PR_ASSOC_CONTENT_COUNT** [(PidTagAssociatedContentCount)](pidtagassociatedcontentcount-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="1c089-170">**PR_ASSOC_CONTENT_COUNT** ([PidTagAssociatedContentCount](pidtagassociatedcontentcount-canonical-property.md))</span></span>
    
- <span data-ttu-id="1c089-171">**PR_CONTENT_COUNT** [(PidTagContentCount)](pidtagcontentcount-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="1c089-171">**PR_CONTENT_COUNT** ([PidTagContentCount](pidtagcontentcount-canonical-property.md))</span></span>
    
- <span data-ttu-id="1c089-172">**PR_CREATION_TIME** [(PidTagCreationTime)](pidtagcreationtime-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="1c089-172">**PR_CREATION_TIME** ([PidTagCreationTime](pidtagcreationtime-canonical-property.md))</span></span>
    
- <span data-ttu-id="1c089-173">**PR_DISPLAY_NAME** [(PidTagDisplayName)](pidtagdisplayname-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="1c089-173">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span></span>
    
- <span data-ttu-id="1c089-174">**PR_DISPLAY_TYPE** [(PidTagDisplayType)](pidtagdisplaytype-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="1c089-174">**PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md))</span></span>
    
- <span data-ttu-id="1c089-175">**PR_FOLDER_TYPE** [(PidTagFolderType)](pidtagfoldertype-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="1c089-175">**PR_FOLDER_TYPE** ([PidTagFolderType](pidtagfoldertype-canonical-property.md))</span></span>
    
- <span data-ttu-id="1c089-176">**PR_OBJECT_TYPE**</span><span class="sxs-lookup"><span data-stu-id="1c089-176">**PR_OBJECT_TYPE**</span></span>
    
- <span data-ttu-id="1c089-177">**PR_SUBFOLDERS** [(PidTagSubfolders)](pidtagsubfolders-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="1c089-177">**PR_SUBFOLDERS** ([PidTagSubfolders](pidtagsubfolders-canonical-property.md))</span></span>
    
## <a name="notes-to-callers"></a><span data-ttu-id="1c089-178">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="1c089-178">Notes to callers</span></span>

<span data-ttu-id="1c089-179">Для свойств типа PT_OBJECT вызываем [метод IMAPIProp::OpenProperty](imapiprop-openproperty.md) вместо **GetProps.**</span><span class="sxs-lookup"><span data-stu-id="1c089-179">For properties of type PT_OBJECT, call the [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method instead of **GetProps**.</span></span> 
  
<span data-ttu-id="1c089-180">Для безопасных свойств не ожидайте их получения, позвонив **в GetProps** с параметром  _lppPropTagArray,_ заданным nULL.</span><span class="sxs-lookup"><span data-stu-id="1c089-180">For secure properties, do not expect to retrieve them by calling **GetProps** with the  _lppPropTagArray_ parameter set to NULL.</span></span> <span data-ttu-id="1c089-181">При вызове **GetProps** необходимо явно установить идентификатор защищенного свойства в **члене aulPropTag** массива тегов свойств.</span><span class="sxs-lookup"><span data-stu-id="1c089-181">You must explicitly set a secure property's identifier in the **aulPropTag** member of its property tag array when you call **GetProps**.</span></span> <span data-ttu-id="1c089-182">Когда и как доступно безопасное свойство, до поставщика услуг.</span><span class="sxs-lookup"><span data-stu-id="1c089-182">When and how a secure property is available is up to the service provider.</span></span> 
  
<span data-ttu-id="1c089-183">Освободите возвращенную **структуру SPropValue,** позвонив функции [MAPIFreeBuffer](mapifreebuffer.md) только в том случае, если **GetProps** S_OK или MAPI_W_ERRORS_RETURNED.</span><span class="sxs-lookup"><span data-stu-id="1c089-183">Free the returned **SPropValue** structure by calling the [MAPIFreeBuffer](mapifreebuffer.md) function only if **GetProps** returns S_OK or MAPI_W_ERRORS_RETURNED.</span></span> 
  
<span data-ttu-id="1c089-184">Если **GetProps** возвращает MAPI_W_ERRORS_RETURNED из-за того, что он не может получить доступ к одному или более свойствам, проверьте теги свойств возвращенных свойств.</span><span class="sxs-lookup"><span data-stu-id="1c089-184">If **GetProps** returns MAPI_W_ERRORS_RETURNED because it could not access one or more properties, check the property tags of the returned properties.</span></span> <span data-ttu-id="1c089-185">В структуре значения свойства сбойными свойствами будут задатки следующих значений:</span><span class="sxs-lookup"><span data-stu-id="1c089-185">The failed properties will have the following values set in their property value structure:</span></span> 
  
- <span data-ttu-id="1c089-186">Тип свойства в **члене aulPropTag,** замещенный PT_ERROR.</span><span class="sxs-lookup"><span data-stu-id="1c089-186">The property type in the **aulPropTag** member set to PT_ERROR.</span></span> 
    
- <span data-ttu-id="1c089-187">Значение свойства в **члене Value** за набором кода состояния для ошибки, например MAPI_E_NOT_FOUND.</span><span class="sxs-lookup"><span data-stu-id="1c089-187">The property value in the **Value** member set to a status code for the error, such as MAPI_E_NOT_FOUND.</span></span> 
    
<span data-ttu-id="1c089-188">Свойства, которые не удается, так как они слишком большие, чтобы  удобно возвращаться в структуре значения свойства, имеют свой член значения, MAPI_E_NOT_ENOUGH_MEMORY.</span><span class="sxs-lookup"><span data-stu-id="1c089-188">Properties that fail because they are too large to conveniently be returned in the property value structure have their **Value** member set to MAPI_E_NOT_ENOUGH_MEMORY.</span></span> <span data-ttu-id="1c089-189">Как правило, это происходит со строками или двоичными свойствами типа PT_STRING8, PT_UNICODE или PT_BINARY, когда значение свойства 4 КБ или больше.</span><span class="sxs-lookup"><span data-stu-id="1c089-189">Typically, this occurs with string or binary properties of type PT_STRING8, PT_UNICODE, or PT_BINARY when the value of the property is 4 KB or larger.</span></span> <span data-ttu-id="1c089-190">Вызов **IMAPIProp::OpenProperty для** получения больших свойств.</span><span class="sxs-lookup"><span data-stu-id="1c089-190">Call **IMAPIProp::OpenProperty** to retrieve large properties.</span></span> 
  
<span data-ttu-id="1c089-191">Не все реализации **GetProps** поддерживают форматы Unicode и ANSI для строк символов.</span><span class="sxs-lookup"><span data-stu-id="1c089-191">Not all implementations of **GetProps** support both the Unicode and ANSI formats for character strings.</span></span> <span data-ttu-id="1c089-192">Если для определенного свойства требуется преобразование формата строки и **GetProps** не может его поддерживать, значение для свойства заданной MAPI_E_BAD_CHARWIDTH. </span><span class="sxs-lookup"><span data-stu-id="1c089-192">When a particular property requires string format conversion and **GetProps** cannot support it, the **Value** member for the property is set to MAPI_E_BAD_CHARWIDTH.</span></span> 
  
<span data-ttu-id="1c089-193">Чтобы проверить, является ли PST SharePoint PST, смонтировать PST с помощью [IMAPISession::OpenMsgStore,](imapisession-openmsgstore.md)а затем вызвать **GetProps** на объекте магазина сообщений с запросом этого свойства.</span><span class="sxs-lookup"><span data-stu-id="1c089-193">To check if a PST is a SharePoint PST, mount the PST using [IMAPISession::OpenMsgStore](imapisession-openmsgstore.md), then call **GetProps** on the message store object requesting this property.</span></span> <span data-ttu-id="1c089-194">Если он существует, можно предположить, что PST был настроен для SharePoint; если нет, PST не был настроен как SharePoint PST.</span><span class="sxs-lookup"><span data-stu-id="1c089-194">If it exists, you can assume the PST has been configured for SharePoint; if not, the PST has not been configured as a SharePoint PST.</span></span> 
  
<span data-ttu-id="1c089-195">Дополнительные сведения об использовании **GetProps** для доступа к свойствам см. в дополнительных сведениях о том, как получить доступ к [свойствам MAPI.](retrieving-mapi-properties.md)</span><span class="sxs-lookup"><span data-stu-id="1c089-195">For more information about how to use **GetProps** to access properties, see [Retrieving MAPI Properties](retrieving-mapi-properties.md).</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="1c089-196">Справочные материалы по MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="1c089-196">MFCMAPI reference</span></span>

<span data-ttu-id="1c089-197">Пример кода MFCMAPI указан в приведенной ниже таблице.</span><span class="sxs-lookup"><span data-stu-id="1c089-197">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="1c089-198">**Файл**</span><span class="sxs-lookup"><span data-stu-id="1c089-198">**File**</span></span>|<span data-ttu-id="1c089-199">**Функция**</span><span class="sxs-lookup"><span data-stu-id="1c089-199">**Function**</span></span>|<span data-ttu-id="1c089-200">**Примечание**</span><span class="sxs-lookup"><span data-stu-id="1c089-200">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="1c089-201">MAPIFunctions.cpp</span><span class="sxs-lookup"><span data-stu-id="1c089-201">MAPIFunctions.cpp</span></span>  <br/> |<span data-ttu-id="1c089-202">GetPropsNULL</span><span class="sxs-lookup"><span data-stu-id="1c089-202">GetPropsNULL</span></span>  <br/> |<span data-ttu-id="1c089-203">MFCMAPI использует метод **IMAPIProp::GetProps** для получения всех свойств объекта путем передачи NULL или массива, возвращенного методом [IMAPIProp::GetPropList](imapiprop-getproplist.md) в параметре _lpPropTagArray._</span><span class="sxs-lookup"><span data-stu-id="1c089-203">MFCMAPI uses the **IMAPIProp::GetProps** method to obtain all properties for an object by passing either NULL or the array returned by the [IMAPIProp::GetPropList](imapiprop-getproplist.md) method in the  _lpPropTagArray_ parameter.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="1c089-204">См. также</span><span class="sxs-lookup"><span data-stu-id="1c089-204">See also</span></span>



[<span data-ttu-id="1c089-205">IMAPIProp::GetPropList</span><span class="sxs-lookup"><span data-stu-id="1c089-205">IMAPIProp::GetPropList</span></span>](imapiprop-getproplist.md)
  
[<span data-ttu-id="1c089-206">IMAPIProp::OpenProperty</span><span class="sxs-lookup"><span data-stu-id="1c089-206">IMAPIProp::OpenProperty</span></span>](imapiprop-openproperty.md)
  
[<span data-ttu-id="1c089-207">MAPIAllocateBuffer</span><span class="sxs-lookup"><span data-stu-id="1c089-207">MAPIAllocateBuffer</span></span>](mapiallocatebuffer.md)
  
[<span data-ttu-id="1c089-208">MAPIAllocateMore</span><span class="sxs-lookup"><span data-stu-id="1c089-208">MAPIAllocateMore</span></span>](mapiallocatemore.md)
  
[<span data-ttu-id="1c089-209">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="1c089-209">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="1c089-210">SPropTagArray</span><span class="sxs-lookup"><span data-stu-id="1c089-210">SPropTagArray</span></span>](sproptagarray.md)
  
[<span data-ttu-id="1c089-211">SPropValue</span><span class="sxs-lookup"><span data-stu-id="1c089-211">SPropValue</span></span>](spropvalue.md)
  
[<span data-ttu-id="1c089-212">IMAPIProp : IUnknown</span><span class="sxs-lookup"><span data-stu-id="1c089-212">IMAPIProp : IUnknown</span></span>](imapipropiunknown.md)


[<span data-ttu-id="1c089-213">MFCMAPI как пример кода</span><span class="sxs-lookup"><span data-stu-id="1c089-213">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)
  
[<span data-ttu-id="1c089-214">Ирисовка свойств MAPI</span><span class="sxs-lookup"><span data-stu-id="1c089-214">Retrieving MAPI Properties</span></span>](retrieving-mapi-properties.md)
  
[<span data-ttu-id="1c089-215">Использование макроса для обработки ошибок</span><span class="sxs-lookup"><span data-stu-id="1c089-215">Using Macros for Error Handling</span></span>](using-macros-for-error-handling.md)

