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
ms.openlocfilehash: 28880b818bc80e31cae0c695d4aac92eb9555cac
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33433586"
---
# <a name="imapipropgetidsfromnames"></a><span data-ttu-id="00331-103">IMAPIProp::GetIDsFromNames</span><span class="sxs-lookup"><span data-stu-id="00331-103">IMAPIProp::GetIDsFromNames</span></span>

  
  
<span data-ttu-id="00331-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="00331-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="00331-105">Предоставляет идентификаторы свойств, соответствующие одному или более имени свойств.</span><span class="sxs-lookup"><span data-stu-id="00331-105">Provides the property identifiers that correspond to one or more property names.</span></span>
  
```cpp
HRESULT GetIDsFromNames(
  ULONG cPropNames,
  LPMAPINAMEID FAR * lppPropNames,
  ULONG ulFlags,
  LPSPropTagArray FAR * lppPropTags
);
```

## <a name="parameters"></a><span data-ttu-id="00331-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="00331-106">Parameters</span></span>

 <span data-ttu-id="00331-107">_cPropNames_</span><span class="sxs-lookup"><span data-stu-id="00331-107">_cPropNames_</span></span>
  
> <span data-ttu-id="00331-108">[in] Количество имен свойств, на которые указывает параметр _lppPropNames._</span><span class="sxs-lookup"><span data-stu-id="00331-108">[in] The count of property names pointed to by the  _lppPropNames_ parameter.</span></span> <span data-ttu-id="00331-109">Если  _lppPropNames_ является NULL, параметр  _cPropNames_ должен быть 0.</span><span class="sxs-lookup"><span data-stu-id="00331-109">If  _lppPropNames_ is NULL, the  _cPropNames_ parameter must be 0.</span></span> 
    
 <span data-ttu-id="00331-110">_lppPropNames_</span><span class="sxs-lookup"><span data-stu-id="00331-110">_lppPropNames_</span></span>
  
> <span data-ttu-id="00331-111">[in] Указатель на массив имен свойств или NULL.</span><span class="sxs-lookup"><span data-stu-id="00331-111">[in] A pointer to an array of property names, or NULL.</span></span> <span data-ttu-id="00331-112">Передача NULL запрашивает идентификаторы свойств для всех имен свойств во всех наборах свойств, о которых объект имеет сведения.</span><span class="sxs-lookup"><span data-stu-id="00331-112">Passing NULL requests property identifiers for all property names in all property sets about which the object has information.</span></span> <span data-ttu-id="00331-113">Параметр _lppPropNames_ не должен быть NULL, если флаг MAPI_CREATE в _параметре ulFlags._</span><span class="sxs-lookup"><span data-stu-id="00331-113">The  _lppPropNames_ parameter must not be NULL if the MAPI_CREATE flag is set in the  _ulFlags_ parameter.</span></span> 
    
 <span data-ttu-id="00331-114">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="00331-114">_ulFlags_</span></span>
  
> <span data-ttu-id="00331-115">[in] Битмашка флагов, которая указывает, как должны быть возвращены идентификаторы свойств.</span><span class="sxs-lookup"><span data-stu-id="00331-115">[in] A bitmask of flags that indicates how the property identifiers should be returned.</span></span> <span data-ttu-id="00331-116">Можно установить следующий флаг:</span><span class="sxs-lookup"><span data-stu-id="00331-116">The following flag can be set:</span></span>
    
<span data-ttu-id="00331-117">MAPI_CREATE</span><span class="sxs-lookup"><span data-stu-id="00331-117">MAPI_CREATE</span></span> 
  
> <span data-ttu-id="00331-118">Назначает идентификатор свойства, если он еще не назначен, одному или несколько имен, включенных в массив имен свойств, на которые указывает _lppPropNames._</span><span class="sxs-lookup"><span data-stu-id="00331-118">Assigns a property identifier, if one has not yet been assigned, to one or more of the names included in the property name array pointed to by  _lppPropNames_.</span></span> <span data-ttu-id="00331-119">Этот флаг регистрирует идентификатор в таблице сопоставления от имени к идентификатору.</span><span class="sxs-lookup"><span data-stu-id="00331-119">This flag internally registers the identifier in the name-to-identifier mapping table.</span></span>
    
 <span data-ttu-id="00331-120">_lppPropTags_</span><span class="sxs-lookup"><span data-stu-id="00331-120">_lppPropTags_</span></span>
  
> <span data-ttu-id="00331-121">[вышел] Указатель на указатель на массив тегов свойств, содержащий существующие или недавно назначенные идентификаторы свойств.</span><span class="sxs-lookup"><span data-stu-id="00331-121">[out] A pointer to a pointer to an array of property tags that contains existing or newly assigned property identifiers.</span></span> <span data-ttu-id="00331-122">Типы свойств тегов свойств в этом массиве заданной для **PT_UNSPECIFIED.**</span><span class="sxs-lookup"><span data-stu-id="00331-122">The property types for the property tags in this array are set to **PT_UNSPECIFIED**.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="00331-123">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="00331-123">Return value</span></span>

<span data-ttu-id="00331-124">S_OK</span><span class="sxs-lookup"><span data-stu-id="00331-124">S_OK</span></span> 
  
> <span data-ttu-id="00331-125">Идентификаторы для указанных имен свойств были успешно возвращены.</span><span class="sxs-lookup"><span data-stu-id="00331-125">The identifiers for the specified property names were successfully returned.</span></span>
    
<span data-ttu-id="00331-126">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="00331-126">MAPI_E_NO_SUPPORT</span></span> 
  
> <span data-ttu-id="00331-127">Объект не поддерживает именимые свойства.</span><span class="sxs-lookup"><span data-stu-id="00331-127">The object does not support named properties.</span></span>
    
<span data-ttu-id="00331-128">MAPI_E_NOT_ENOUGH_MEMORY</span><span class="sxs-lookup"><span data-stu-id="00331-128">MAPI_E_NOT_ENOUGH_MEMORY</span></span> 
  
> <span data-ttu-id="00331-129">Недостаточная память была доступна для получения идентификаторов.</span><span class="sxs-lookup"><span data-stu-id="00331-129">Insufficient memory was available to retrieve the identifiers.</span></span>
    
<span data-ttu-id="00331-130">MAPI_E_TOO_BIG</span><span class="sxs-lookup"><span data-stu-id="00331-130">MAPI_E_TOO_BIG</span></span> 
  
> <span data-ttu-id="00331-131">Операция не может быть выполнена, так как для ее возврата требуется слишком много тегов свойств.</span><span class="sxs-lookup"><span data-stu-id="00331-131">The operation cannot be performed because it requires too many property tags to be returned.</span></span>
    
<span data-ttu-id="00331-132">MAPI_W_ERRORS_RETURNED</span><span class="sxs-lookup"><span data-stu-id="00331-132">MAPI_W_ERRORS_RETURNED</span></span> 
  
> <span data-ttu-id="00331-133">Вызов удался в целом, но один или несколько идентификаторов свойств не удалось вернуть.</span><span class="sxs-lookup"><span data-stu-id="00331-133">The call succeeded overall, but one or more property identifiers could not be returned.</span></span> <span data-ttu-id="00331-134">Соответствующий тип свойства для каждого недоступного свойства PT_ERROR и его идентификатор до нуля. </span><span class="sxs-lookup"><span data-stu-id="00331-134">The corresponding property type for each unavailable property is set to **PT_ERROR** and its identifier to zero.</span></span> <span data-ttu-id="00331-135">Когда это предупреждение возвращается, обработать вызов как успешный.</span><span class="sxs-lookup"><span data-stu-id="00331-135">When this warning is returned, handle the call as successful.</span></span> <span data-ttu-id="00331-136">Чтобы проверить это предупреждение, используйте **HR_FAILED** макрос.</span><span class="sxs-lookup"><span data-stu-id="00331-136">To test for this warning, use the **HR_FAILED** macro.</span></span> <span data-ttu-id="00331-137">См. в руб. Использование [макроса для обработки ошибок.](using-macros-for-error-handling.md)</span><span class="sxs-lookup"><span data-stu-id="00331-137">See [Using Macros for Error Handling](using-macros-for-error-handling.md).</span></span>
    
## <a name="remarks"></a><span data-ttu-id="00331-138">Примечания</span><span class="sxs-lookup"><span data-stu-id="00331-138">Remarks</span></span>

<span data-ttu-id="00331-139">Метод **IMAPIProp::GetIDsFromNames** извлекает массив тегов свойств, которые удерживают идентификаторы свойств для одного или более именных свойств.</span><span class="sxs-lookup"><span data-stu-id="00331-139">The **IMAPIProp::GetIDsFromNames** method retrieves an array of property tags that hold the property identifiers for one or more named properties.</span></span> <span data-ttu-id="00331-140">**IMAPIProp::GetIDsFromNames** можно назвать следующим образом:</span><span class="sxs-lookup"><span data-stu-id="00331-140">**IMAPIProp::GetIDsFromNames** can be called to do the following:</span></span> 
  
- <span data-ttu-id="00331-141">Создание идентификаторов для новых имен.</span><span class="sxs-lookup"><span data-stu-id="00331-141">Create identifiers for new names.</span></span>
    
- <span data-ttu-id="00331-142">Извлечение идентификаторов для определенных имен.</span><span class="sxs-lookup"><span data-stu-id="00331-142">Retrieve identifiers for specific names.</span></span>
    
- <span data-ttu-id="00331-143">Извлечение идентификаторов для всех именных свойств, включенных в сопоставление объекта.</span><span class="sxs-lookup"><span data-stu-id="00331-143">Retrieve identifiers for all named properties that are included in the object's mapping.</span></span>
    
<span data-ttu-id="00331-144">Свойства имен обычно используются поставщиками магазинов сообщений для папок и сообщений.</span><span class="sxs-lookup"><span data-stu-id="00331-144">Named properties are typically used by message store providers for folders and messages.</span></span> <span data-ttu-id="00331-145">Другие объекты, например пользователи сообщений и разделы профилей, могут не поддерживать связь имен с идентификаторами свойств и могут возвращать MAPI_E_NO_SUPPORT из **GetIDsFromNames.**</span><span class="sxs-lookup"><span data-stu-id="00331-145">Other objects, such as messaging users and profile sections, might not support the association of names to property identifiers and might return MAPI_E_NO_SUPPORT from **GetIDsFromNames**.</span></span>
  
<span data-ttu-id="00331-146">При ошибке, возвращаемой идентификатором для определенного имени, **GetIDsFromNames** возвращает MAPI_W_ERRORS_RETURNED и задает тип свойства в записи массива тегов свойств, соответствующей имени PT_ERROR и идентификатору до нуля. </span><span class="sxs-lookup"><span data-stu-id="00331-146">If there is an error that returns an identifier for a particular name, **GetIDsFromNames** returns MAPI_W_ERRORS_RETURNED and sets the property type in the property tag array entry that corresponds to the name to **PT_ERROR** and the identifier to zero.</span></span> 
  
<span data-ttu-id="00331-147">Сопоставление имен и идентификаторов представлено свойством PR_MAPPING_SIGNATURE **объекта** [(PidTagMappingSignature).](pidtagmappingsignature-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="00331-147">Name-to-identifier mapping is represented by an object's **PR_MAPPING_SIGNATURE** ([PidTagMappingSignature](pidtagmappingsignature-canonical-property.md)) property.</span></span> <span data-ttu-id="00331-148">**PR_MAPPING_SIGNATURE** [содержит структуру MAPIUID,](mapiuid.md) которая указывает поставщика услуг, ответственного за объект.</span><span class="sxs-lookup"><span data-stu-id="00331-148">**PR_MAPPING_SIGNATURE** contains a [MAPIUID](mapiuid.md) structure that indicates the service provider responsible for the object.</span></span> <span data-ttu-id="00331-149">Если **свойство PR_MAPPING_SIGNATURE** одно и то же для двух объектов, предположим, что эти объекты используют одно и то же сопоставление от имени к идентификатору.</span><span class="sxs-lookup"><span data-stu-id="00331-149">If the **PR_MAPPING_SIGNATURE** property is the same for two objects, assume that these objects use the same name-to-identifier mapping.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="00331-150">Примечания для исполнителей</span><span class="sxs-lookup"><span data-stu-id="00331-150">Notes to implementers</span></span>

<span data-ttu-id="00331-151">Идентификаторы, которые передаются в массиве тегов свойств, на которые указывает параметр  _lppPropNames,_ должны быть в диапазоне 0x8000 0xFFFE.</span><span class="sxs-lookup"><span data-stu-id="00331-151">The identifiers that you pass back in the property tag array pointed to by the  _lppPropNames_ parameter must be in the 0x8000 to 0xFFFE range.</span></span> <span data-ttu-id="00331-152">Записи в этом массиве должны быть в том же порядке, что и имена, переданные в массиве имен свойств, на которые указывает _lppPropNames._</span><span class="sxs-lookup"><span data-stu-id="00331-152">The entries in this array must be in the same order as the names passed in the property name array pointed to by  _lppPropNames_.</span></span> 
  
<span data-ttu-id="00331-153">Если вы поддерживаете свойства с именем в контейнере, используйте одно и то же сопоставление от имени к идентификатору для всех объектов в контейнере (то есть не используйте другое сопоставление для каждой папки в хранилище сообщений или каждого сообщения в папке).</span><span class="sxs-lookup"><span data-stu-id="00331-153">If you support named properties on a container, use the same name-to-identifier mapping for all objects in your container (that is, do not use a different mapping for each folder in your message store or each message in your folder).</span></span>
  
## <a name="notes-to-callers"></a><span data-ttu-id="00331-154">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="00331-154">Notes to callers</span></span>

<span data-ttu-id="00331-155">Поскольку типы свойств возвращаемого идентификатора в массиве тегов свойств, на которые указывают _lppPropTags,_ настроены на **PT_UNSPECIFIED,** для получения точных типов необходимо вызвать [метод IMAPIProp::SetProps.](imapiprop-setprops.md)</span><span class="sxs-lookup"><span data-stu-id="00331-155">Because the property types for the returned identifiers in the property tag array pointed to by  _lppPropTags_ are set to **PT_UNSPECIFIED**, you will have to call the [IMAPIProp::SetProps](imapiprop-setprops.md) method to retrieve the accurate types.</span></span> 
  
<span data-ttu-id="00331-156">Если вы перемещаете или **копируете** объекты с указанными свойствами, а объекты источника и назначения имеют различные подписи сопоставления, указанные значениями их свойств PR_MAPPING_SIGNATURE, необходимо сохранить имена во время этих операций.</span><span class="sxs-lookup"><span data-stu-id="00331-156">If you move or copy objects with named properties, and the source and destination objects have different mapping signatures as indicated by the values of their **PR_MAPPING_SIGNATURE** properties, you must preserve the names during these operations.</span></span> <span data-ttu-id="00331-157">Чтобы сохранить имена свойств, настройте соответствующие идентификаторы свойств в соответствие с сопоставлением имени и идентификатора объекта назначения.</span><span class="sxs-lookup"><span data-stu-id="00331-157">To preserve property names, adjust the corresponding property identifiers to match the name-to-identifier mapping of the destination object.</span></span> 
  
<span data-ttu-id="00331-158">Некоторые объекты имеют ограничение на количество идентификаторов свойств, которые они могут назвать.</span><span class="sxs-lookup"><span data-stu-id="00331-158">Some objects have a limit as to the number of property identifiers they can name.</span></span> <span data-ttu-id="00331-159">Если вызов **в GetIDsFromNames** приводит к превышению этого ограничения, метод возвращает MAPI_E_TOO_BIG.</span><span class="sxs-lookup"><span data-stu-id="00331-159">If a call to **GetIDsFromNames** causes this limit to be exceeded, the method returns MAPI_E_TOO_BIG.</span></span> <span data-ttu-id="00331-160">В этом случае запрос по идентификатору.</span><span class="sxs-lookup"><span data-stu-id="00331-160">In this case, query by identifier.</span></span> 
  
<span data-ttu-id="00331-161">Дополнительные сведения см. в [дополнительных сведениях о свойствах MAPI Named Properties.](mapi-named-properties.md)</span><span class="sxs-lookup"><span data-stu-id="00331-161">For more information, see [MAPI Named Properties](mapi-named-properties.md).</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="00331-162">Справочные материалы по MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="00331-162">MFCMAPI reference</span></span>

<span data-ttu-id="00331-163">Пример кода MFCMAPI указан в приведенной ниже таблице.</span><span class="sxs-lookup"><span data-stu-id="00331-163">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="00331-164">**Файл**</span><span class="sxs-lookup"><span data-stu-id="00331-164">**File**</span></span>|<span data-ttu-id="00331-165">**Функция**</span><span class="sxs-lookup"><span data-stu-id="00331-165">**Function**</span></span>|<span data-ttu-id="00331-166">**Примечание**</span><span class="sxs-lookup"><span data-stu-id="00331-166">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="00331-167">SingleMAPIPropListCtrl.cpp</span><span class="sxs-lookup"><span data-stu-id="00331-167">SingleMAPIPropListCtrl.cpp</span></span>  <br/> |<span data-ttu-id="00331-168">CSingleMAPIPropListCtrl::FindAllNamedPropsUsed</span><span class="sxs-lookup"><span data-stu-id="00331-168">CSingleMAPIPropListCtrl::FindAllNamedPropsUsed</span></span>  <br/> |<span data-ttu-id="00331-169">MFCMAPI использует **метод IMAPIProp::GetIDsFromNames** для получения тегов свойств для всех именных свойств, которые были намечаемы.</span><span class="sxs-lookup"><span data-stu-id="00331-169">MFCMAPI uses the **IMAPIProp::GetIDsFromNames** method to obtain property tags for all named properties that have been mapped.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="00331-170">См. также</span><span class="sxs-lookup"><span data-stu-id="00331-170">See also</span></span>



[<span data-ttu-id="00331-171">IMAPIProp::GetNamesFromIDs</span><span class="sxs-lookup"><span data-stu-id="00331-171">IMAPIProp::GetNamesFromIDs</span></span>](imapiprop-getnamesfromids.md)
  
[<span data-ttu-id="00331-172">IMAPIProp::SetProps</span><span class="sxs-lookup"><span data-stu-id="00331-172">IMAPIProp::SetProps</span></span>](imapiprop-setprops.md)
  
[<span data-ttu-id="00331-173">MAPINAMEID</span><span class="sxs-lookup"><span data-stu-id="00331-173">MAPINAMEID</span></span>](mapinameid.md)
  
[<span data-ttu-id="00331-174">MAPIUID</span><span class="sxs-lookup"><span data-stu-id="00331-174">MAPIUID</span></span>](mapiuid.md)
  
[<span data-ttu-id="00331-175">IMAPIProp : IUnknown</span><span class="sxs-lookup"><span data-stu-id="00331-175">IMAPIProp : IUnknown</span></span>](imapipropiunknown.md)


[<span data-ttu-id="00331-176">MFCMAPI как пример кода</span><span class="sxs-lookup"><span data-stu-id="00331-176">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)
  
[<span data-ttu-id="00331-177">Именованные свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="00331-177">MAPI Named Properties</span></span>](mapi-named-properties.md)
  
[<span data-ttu-id="00331-178">Использование макроса для обработки ошибок</span><span class="sxs-lookup"><span data-stu-id="00331-178">Using Macros for Error Handling</span></span>](using-macros-for-error-handling.md)

