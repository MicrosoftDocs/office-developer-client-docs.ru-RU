---
title: IMAPIPropGetIDsFromNames
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIProp.GetIDsFromNames
api_type:
- COM
ms.assetid: e3f501a4-a8ee-43d7-bd83-c94e7980c398
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 7f7c243995c633389ab8fa80a26dddd152347276
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22565363"
---
# <a name="imapipropgetidsfromnames"></a><span data-ttu-id="0eebb-103">IMAPIProp::GetIDsFromNames</span><span class="sxs-lookup"><span data-stu-id="0eebb-103">IMAPIProp::GetIDsFromNames</span></span>

  
  
<span data-ttu-id="0eebb-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0eebb-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0eebb-105">Предоставляет свойство идентификаторы, соответствующие имена одного или нескольких свойств.</span><span class="sxs-lookup"><span data-stu-id="0eebb-105">Provides the property identifiers that correspond to one or more property names.</span></span>
  
```cpp
HRESULT GetIDsFromNames(
  ULONG cPropNames,
  LPMAPINAMEID FAR * lppPropNames,
  ULONG ulFlags,
  LPSPropTagArray FAR * lppPropTags
);
```

## <a name="parameters"></a><span data-ttu-id="0eebb-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="0eebb-106">Parameters</span></span>

 <span data-ttu-id="0eebb-107">_cPropNames_</span><span class="sxs-lookup"><span data-stu-id="0eebb-107">_cPropNames_</span></span>
  
> <span data-ttu-id="0eebb-108">[in] Count имена свойств, на который указывает параметр _lppPropNames_ .</span><span class="sxs-lookup"><span data-stu-id="0eebb-108">[in] The count of property names pointed to by the  _lppPropNames_ parameter.</span></span> <span data-ttu-id="0eebb-109">Если _lppPropNames_ имеет значение NULL, параметр _cPropNames_ должен иметь значение 0.</span><span class="sxs-lookup"><span data-stu-id="0eebb-109">If  _lppPropNames_ is NULL, the  _cPropNames_ parameter must be 0.</span></span> 
    
 <span data-ttu-id="0eebb-110">_lppPropNames_</span><span class="sxs-lookup"><span data-stu-id="0eebb-110">_lppPropNames_</span></span>
  
> <span data-ttu-id="0eebb-111">[in] Указатель на массив имена свойств, или значение NULL.</span><span class="sxs-lookup"><span data-stu-id="0eebb-111">[in] A pointer to an array of property names, or NULL.</span></span> <span data-ttu-id="0eebb-112">Передача значение NULL, запрашивает идентификаторы свойств в все наборы свойств о том, какие объект содержит сведения о всех имен свойств.</span><span class="sxs-lookup"><span data-stu-id="0eebb-112">Passing NULL requests property identifiers for all property names in all property sets about which the object has information.</span></span> <span data-ttu-id="0eebb-113">Параметр _lppPropNames_ не должна быть NULL, если флаг MAPI_CREATE установлен в параметре _ulFlags_ .</span><span class="sxs-lookup"><span data-stu-id="0eebb-113">The  _lppPropNames_ parameter must not be NULL if the MAPI_CREATE flag is set in the  _ulFlags_ parameter.</span></span> 
    
 <span data-ttu-id="0eebb-114">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="0eebb-114">_ulFlags_</span></span>
  
> <span data-ttu-id="0eebb-115">[in] Битовая маска флаги, которое указывает, как должны быть возвращены идентификаторы свойств.</span><span class="sxs-lookup"><span data-stu-id="0eebb-115">[in] A bitmask of flags that indicates how the property identifiers should be returned.</span></span> <span data-ttu-id="0eebb-116">Можно задать следующий флаг:</span><span class="sxs-lookup"><span data-stu-id="0eebb-116">The following flag can be set:</span></span>
    
<span data-ttu-id="0eebb-117">MAPI_CREATE</span><span class="sxs-lookup"><span data-stu-id="0eebb-117">MAPI_CREATE</span></span> 
  
> <span data-ttu-id="0eebb-118">Если один не еще не присвоен, к одному или нескольким имена, включенные в массиве имя свойства, на который указывает _lppPropNames_, назначает идентификатор свойства.</span><span class="sxs-lookup"><span data-stu-id="0eebb-118">Assigns a property identifier, if one has not yet been assigned, to one or more of the names included in the property name array pointed to by  _lppPropNames_.</span></span> <span data-ttu-id="0eebb-119">Этот флаг не зарегистрирует идентификатор в таблице сопоставления идентификатор имени.</span><span class="sxs-lookup"><span data-stu-id="0eebb-119">This flag internally registers the identifier in the name-to-identifier mapping table.</span></span>
    
 <span data-ttu-id="0eebb-120">_lppPropTags_</span><span class="sxs-lookup"><span data-stu-id="0eebb-120">_lppPropTags_</span></span>
  
> <span data-ttu-id="0eebb-121">[out] Указатель на указатель на массив тегов свойств, содержащий существующие или новые назначенные идентификаторы свойств.</span><span class="sxs-lookup"><span data-stu-id="0eebb-121">[out] A pointer to a pointer to an array of property tags that contains existing or newly assigned property identifiers.</span></span> <span data-ttu-id="0eebb-122">Типы свойств для тегов свойств этого массива устанавливаются **PT_UNSPECIFIED**.</span><span class="sxs-lookup"><span data-stu-id="0eebb-122">The property types for the property tags in this array are set to **PT_UNSPECIFIED**.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="0eebb-123">������������ ��������</span><span class="sxs-lookup"><span data-stu-id="0eebb-123">Return value</span></span>

<span data-ttu-id="0eebb-124">ЗНАЧЕНИЕ S_OK</span><span class="sxs-lookup"><span data-stu-id="0eebb-124">S_OK</span></span> 
  
> <span data-ttu-id="0eebb-125">Идентификаторы для указанного свойства имена были успешно возвращен.</span><span class="sxs-lookup"><span data-stu-id="0eebb-125">The identifiers for the specified property names were successfully returned.</span></span>
    
<span data-ttu-id="0eebb-126">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="0eebb-126">MAPI_E_NO_SUPPORT</span></span> 
  
> <span data-ttu-id="0eebb-127">Объект не поддерживает именованные свойства.</span><span class="sxs-lookup"><span data-stu-id="0eebb-127">The object does not support named properties.</span></span>
    
<span data-ttu-id="0eebb-128">MAPI_E_NOT_ENOUGH_MEMORY</span><span class="sxs-lookup"><span data-stu-id="0eebb-128">MAPI_E_NOT_ENOUGH_MEMORY</span></span> 
  
> <span data-ttu-id="0eebb-129">Недостаточно памяти была доступна для получения идентификаторов.</span><span class="sxs-lookup"><span data-stu-id="0eebb-129">Insufficient memory was available to retrieve the identifiers.</span></span>
    
<span data-ttu-id="0eebb-130">MAPI_E_TOO_BIG</span><span class="sxs-lookup"><span data-stu-id="0eebb-130">MAPI_E_TOO_BIG</span></span> 
  
> <span data-ttu-id="0eebb-131">Операцию не удается выполнить из-за слишком большого числа тегов свойства которого требуется получить.</span><span class="sxs-lookup"><span data-stu-id="0eebb-131">The operation cannot be performed because it requires too many property tags to be returned.</span></span>
    
<span data-ttu-id="0eebb-132">MAPI_W_ERRORS_RETURNED</span><span class="sxs-lookup"><span data-stu-id="0eebb-132">MAPI_W_ERRORS_RETURNED</span></span> 
  
> <span data-ttu-id="0eebb-133">Вызов завершился успешно в целом, но не должны возвращаться один или несколько идентификаторов свойств.</span><span class="sxs-lookup"><span data-stu-id="0eebb-133">The call succeeded overall, but one or more property identifiers could not be returned.</span></span> <span data-ttu-id="0eebb-134">Соответствующий тип свойства для каждого свойства, недоступен — это значение **PT_ERROR** и его идентификатор нулевое значение.</span><span class="sxs-lookup"><span data-stu-id="0eebb-134">The corresponding property type for each unavailable property is set to **PT_ERROR** and its identifier to zero.</span></span> <span data-ttu-id="0eebb-135">При возвращении этого предупреждения обработки вызова как успешно.</span><span class="sxs-lookup"><span data-stu-id="0eebb-135">When this warning is returned, handle the call as successful.</span></span> <span data-ttu-id="0eebb-136">Чтобы проверить это предупреждение, используйте **HR_FAILED** макрос.</span><span class="sxs-lookup"><span data-stu-id="0eebb-136">To test for this warning, use the **HR_FAILED** macro.</span></span> <span data-ttu-id="0eebb-137">В разделе [Использование макросов для обработки ошибок](using-macros-for-error-handling.md).</span><span class="sxs-lookup"><span data-stu-id="0eebb-137">See [Using Macros for Error Handling](using-macros-for-error-handling.md).</span></span>
    
## <a name="remarks"></a><span data-ttu-id="0eebb-138">Замечания</span><span class="sxs-lookup"><span data-stu-id="0eebb-138">Remarks</span></span>

<span data-ttu-id="0eebb-139">Метод **IMAPIProp::GetIDsFromNames** получает массив теги свойства, в которых содержатся идентификаторы свойств для одного или нескольких именованных свойств.</span><span class="sxs-lookup"><span data-stu-id="0eebb-139">The **IMAPIProp::GetIDsFromNames** method retrieves an array of property tags that hold the property identifiers for one or more named properties.</span></span> <span data-ttu-id="0eebb-140">**IMAPIProp::GetIDsFromNames** могут вызываться для выполнения следующих:</span><span class="sxs-lookup"><span data-stu-id="0eebb-140">**IMAPIProp::GetIDsFromNames** can be called to do the following:</span></span> 
  
- <span data-ttu-id="0eebb-141">Создайте идентификаторы для новых имен.</span><span class="sxs-lookup"><span data-stu-id="0eebb-141">Create identifiers for new names.</span></span>
    
- <span data-ttu-id="0eebb-142">Получите идентификаторы для определенных имен.</span><span class="sxs-lookup"><span data-stu-id="0eebb-142">Retrieve identifiers for specific names.</span></span>
    
- <span data-ttu-id="0eebb-143">Получите идентификаторы для всех именованных свойств, которые включены в объект сопоставления.</span><span class="sxs-lookup"><span data-stu-id="0eebb-143">Retrieve identifiers for all named properties that are included in the object's mapping.</span></span>
    
<span data-ttu-id="0eebb-144">Именованные свойства обычно используются поставщиками хранилища сообщений для сообщений и папок.</span><span class="sxs-lookup"><span data-stu-id="0eebb-144">Named properties are typically used by message store providers for folders and messages.</span></span> <span data-ttu-id="0eebb-145">Другие объекты, таких как системы обмена сообщениями разделах профилей и пользователи могут не поддерживать связь имена идентификаторов свойств и может возвращать MAPI_E_NO_SUPPORT из **GetIDsFromNames**.</span><span class="sxs-lookup"><span data-stu-id="0eebb-145">Other objects, such as messaging users and profile sections, might not support the association of names to property identifiers and might return MAPI_E_NO_SUPPORT from **GetIDsFromNames**.</span></span>
  
<span data-ttu-id="0eebb-146">Если ошибка, которая возвращает идентификатор для определенного имени, **GetIDsFromNames** MAPI_W_ERRORS_RETURNED возвращает и задает тип свойства в строке массива свойства tag, соответствующий имени **PT_ERROR** и идентификатор нулевое значение.</span><span class="sxs-lookup"><span data-stu-id="0eebb-146">If there is an error that returns an identifier for a particular name, **GetIDsFromNames** returns MAPI_W_ERRORS_RETURNED and sets the property type in the property tag array entry that corresponds to the name to **PT_ERROR** and the identifier to zero.</span></span> 
  
<span data-ttu-id="0eebb-147">Идентификатор имени сопоставление представлено свойством объекта **PR_MAPPING_SIGNATURE** ([PidTagMappingSignature](pidtagmappingsignature-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="0eebb-147">Name-to-identifier mapping is represented by an object's **PR_MAPPING_SIGNATURE** ([PidTagMappingSignature](pidtagmappingsignature-canonical-property.md)) property.</span></span> <span data-ttu-id="0eebb-148">**PR_MAPPING_SIGNATURE** содержит структуру [MAPIUID](mapiuid.md) , которое указывает, ответственного за объект поставщика услуг.</span><span class="sxs-lookup"><span data-stu-id="0eebb-148">**PR_MAPPING_SIGNATURE** contains a [MAPIUID](mapiuid.md) structure that indicates the service provider responsible for the object.</span></span> <span data-ttu-id="0eebb-149">Если свойство **PR_MAPPING_SIGNATURE** является общим для двух объектов, предполагают, что эти объекты используют то же сопоставление идентификатор имени.</span><span class="sxs-lookup"><span data-stu-id="0eebb-149">If the **PR_MAPPING_SIGNATURE** property is the same for two objects, assume that these objects use the same name-to-identifier mapping.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="0eebb-150">Примечания для исполнителей</span><span class="sxs-lookup"><span data-stu-id="0eebb-150">Notes to implementers</span></span>

<span data-ttu-id="0eebb-151">Идентификаторы, передается обратно в массиве тег свойство указывает параметр _lppPropNames_ должен быть в диапазоне 0x8000 для 0xFFFE.</span><span class="sxs-lookup"><span data-stu-id="0eebb-151">The identifiers that you pass back in the property tag array pointed to by the  _lppPropNames_ parameter must be in the 0x8000 to 0xFFFE range.</span></span> <span data-ttu-id="0eebb-152">Записи в этот массив должен быть в том же порядке, как имена, переданные в массиве имя свойства указывает _lppPropNames_.</span><span class="sxs-lookup"><span data-stu-id="0eebb-152">The entries in this array must be in the same order as the names passed in the property name array pointed to by  _lppPropNames_.</span></span> 
  
<span data-ttu-id="0eebb-153">Если вы поддерживаете именованных свойств в контейнере, используйте одно сопоставление идентификатор имени для всех объектов в контейнере (то есть, не используйте разные сопоставления для каждой папке в хранилище сообщений или каждого сообщения в папке).</span><span class="sxs-lookup"><span data-stu-id="0eebb-153">If you support named properties on a container, use the same name-to-identifier mapping for all objects in your container (that is, do not use a different mapping for each folder in your message store or each message in your folder).</span></span>
  
## <a name="notes-to-callers"></a><span data-ttu-id="0eebb-154">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="0eebb-154">Notes to callers</span></span>

<span data-ttu-id="0eebb-155">Так как типы свойств, возвращенный идентификаторов в массиве тег свойства, на который указывает _lppPropTags_ **PT_UNSPECIFIED**, необходимо вызвать метод [IMAPIProp::SetProps](imapiprop-setprops.md) для извлечения точных типов.</span><span class="sxs-lookup"><span data-stu-id="0eebb-155">Because the property types for the returned identifiers in the property tag array pointed to by  _lppPropTags_ are set to **PT_UNSPECIFIED**, you will have to call the [IMAPIProp::SetProps](imapiprop-setprops.md) method to retrieve the accurate types.</span></span> 
  
<span data-ttu-id="0eebb-156">При перемещении или копировать объекты с именованного свойства и объекты источника и назначения имеют различные сопоставления подписи, как указано в значения свойств своих **PR_MAPPING_SIGNATURE** , должны сохранить имена при выполнении этих операций.</span><span class="sxs-lookup"><span data-stu-id="0eebb-156">If you move or copy objects with named properties, and the source and destination objects have different mapping signatures as indicated by the values of their **PR_MAPPING_SIGNATURE** properties, you must preserve the names during these operations.</span></span> <span data-ttu-id="0eebb-157">Чтобы сохранить имена свойств, настройте соответствующие идентификаторы свойства в соответствии с сопоставлением идентификатор имени конечного объекта.</span><span class="sxs-lookup"><span data-stu-id="0eebb-157">To preserve property names, adjust the corresponding property identifiers to match the name-to-identifier mapping of the destination object.</span></span> 
  
<span data-ttu-id="0eebb-158">Некоторые объекты настроено ограничение на число идентификаторов свойств, которые можно присвоить имя.</span><span class="sxs-lookup"><span data-stu-id="0eebb-158">Some objects have a limit as to the number of property identifiers they can name.</span></span> <span data-ttu-id="0eebb-159">Если вызов **GetIDsFromNames** вызывает превышение этого ограничения, метод возвращает MAPI_E_TOO_BIG.</span><span class="sxs-lookup"><span data-stu-id="0eebb-159">If a call to **GetIDsFromNames** causes this limit to be exceeded, the method returns MAPI_E_TOO_BIG.</span></span> <span data-ttu-id="0eebb-160">В этом случае запроса по идентификатору.</span><span class="sxs-lookup"><span data-stu-id="0eebb-160">In this case, query by identifier.</span></span> 
  
<span data-ttu-id="0eebb-161">Для получения дополнительных сведений см [MAPI с именем свойства](mapi-named-properties.md).</span><span class="sxs-lookup"><span data-stu-id="0eebb-161">For more information, see [MAPI Named Properties](mapi-named-properties.md).</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="0eebb-162">Справочник по mfcmapi (en)</span><span class="sxs-lookup"><span data-stu-id="0eebb-162">MFCMAPI reference</span></span>

<span data-ttu-id="0eebb-163">������ ���� mfcmapi (en) ���������� � ������� ����.</span><span class="sxs-lookup"><span data-stu-id="0eebb-163">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="0eebb-164">**����**</span><span class="sxs-lookup"><span data-stu-id="0eebb-164">**File**</span></span>|<span data-ttu-id="0eebb-165">**�������**</span><span class="sxs-lookup"><span data-stu-id="0eebb-165">**Function**</span></span>|<span data-ttu-id="0eebb-166">**�����������**</span><span class="sxs-lookup"><span data-stu-id="0eebb-166">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="0eebb-167">SingleMAPIPropListCtrl.cpp</span><span class="sxs-lookup"><span data-stu-id="0eebb-167">SingleMAPIPropListCtrl.cpp</span></span>  <br/> |<span data-ttu-id="0eebb-168">CSingleMAPIPropListCtrl::FindAllNamedPropsUsed</span><span class="sxs-lookup"><span data-stu-id="0eebb-168">CSingleMAPIPropListCtrl::FindAllNamedPropsUsed</span></span>  <br/> |<span data-ttu-id="0eebb-169">Mfcmapi (en) использует метод **IMAPIProp::GetIDsFromNames** для получения теги свойства для всех именованных свойств, которые были сопоставлены.</span><span class="sxs-lookup"><span data-stu-id="0eebb-169">MFCMAPI uses the **IMAPIProp::GetIDsFromNames** method to obtain property tags for all named properties that have been mapped.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="0eebb-170">См. также</span><span class="sxs-lookup"><span data-stu-id="0eebb-170">See also</span></span>



[<span data-ttu-id="0eebb-171">IMAPIProp::GetNamesFromIDs</span><span class="sxs-lookup"><span data-stu-id="0eebb-171">IMAPIProp::GetNamesFromIDs</span></span>](imapiprop-getnamesfromids.md)
  
[<span data-ttu-id="0eebb-172">IMAPIProp::SetProps</span><span class="sxs-lookup"><span data-stu-id="0eebb-172">IMAPIProp::SetProps</span></span>](imapiprop-setprops.md)
  
[<span data-ttu-id="0eebb-173">MAPINAMEID</span><span class="sxs-lookup"><span data-stu-id="0eebb-173">MAPINAMEID</span></span>](mapinameid.md)
  
[<span data-ttu-id="0eebb-174">MAPIUID</span><span class="sxs-lookup"><span data-stu-id="0eebb-174">MAPIUID</span></span>](mapiuid.md)
  
[<span data-ttu-id="0eebb-175">IMAPIProp : IUnknown</span><span class="sxs-lookup"><span data-stu-id="0eebb-175">IMAPIProp : IUnknown</span></span>](imapipropiunknown.md)


[<span data-ttu-id="0eebb-176">Mfcmapi (en) � �������� ������� ����</span><span class="sxs-lookup"><span data-stu-id="0eebb-176">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)
  
[<span data-ttu-id="0eebb-177">Именованные свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="0eebb-177">MAPI Named Properties</span></span>](mapi-named-properties.md)
  
[<span data-ttu-id="0eebb-178">Обработка ошибок с помощью макросов</span><span class="sxs-lookup"><span data-stu-id="0eebb-178">Using Macros for Error Handling</span></span>](using-macros-for-error-handling.md)

