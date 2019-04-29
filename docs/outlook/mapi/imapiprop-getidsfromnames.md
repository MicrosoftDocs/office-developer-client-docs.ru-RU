---
title: Имапипропжетидсфромнамес
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
# <a name="imapipropgetidsfromnames"></a><span data-ttu-id="8d117-103">IMAPIProp::GetIDsFromNames</span><span class="sxs-lookup"><span data-stu-id="8d117-103">IMAPIProp::GetIDsFromNames</span></span>

  
  
<span data-ttu-id="8d117-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8d117-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8d117-105">Предоставляет идентификаторы свойств, соответствующие одному или нескольким именам свойств.</span><span class="sxs-lookup"><span data-stu-id="8d117-105">Provides the property identifiers that correspond to one or more property names.</span></span>
  
```cpp
HRESULT GetIDsFromNames(
  ULONG cPropNames,
  LPMAPINAMEID FAR * lppPropNames,
  ULONG ulFlags,
  LPSPropTagArray FAR * lppPropTags
);
```

## <a name="parameters"></a><span data-ttu-id="8d117-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="8d117-106">Parameters</span></span>

 <span data-ttu-id="8d117-107">_Кпропнамес_</span><span class="sxs-lookup"><span data-stu-id="8d117-107">_cPropNames_</span></span>
  
> <span data-ttu-id="8d117-108">возврата Количество имен свойств, на которые указывает параметр _лпппропнамес_ .</span><span class="sxs-lookup"><span data-stu-id="8d117-108">[in] The count of property names pointed to by the  _lppPropNames_ parameter.</span></span> <span data-ttu-id="8d117-109">Если _лпппропнамес_ имеет значение null, параметр _КПРОПНАМЕС_ должен иметь значение 0.</span><span class="sxs-lookup"><span data-stu-id="8d117-109">If  _lppPropNames_ is NULL, the  _cPropNames_ parameter must be 0.</span></span> 
    
 <span data-ttu-id="8d117-110">_Лпппропнамес_</span><span class="sxs-lookup"><span data-stu-id="8d117-110">_lppPropNames_</span></span>
  
> <span data-ttu-id="8d117-111">возврата Указатель на массив имен свойств или значение NULL.</span><span class="sxs-lookup"><span data-stu-id="8d117-111">[in] A pointer to an array of property names, or NULL.</span></span> <span data-ttu-id="8d117-112">Передача идентификаторов свойств NULL для всех имен свойств во всех наборах свойств, сведения о котором имеются у объекта.</span><span class="sxs-lookup"><span data-stu-id="8d117-112">Passing NULL requests property identifiers for all property names in all property sets about which the object has information.</span></span> <span data-ttu-id="8d117-113">Параметр _лпппропнамес_ не может иметь значение null, если установлен флаг мапи_креате в параметре _ulFlags_ .</span><span class="sxs-lookup"><span data-stu-id="8d117-113">The  _lppPropNames_ parameter must not be NULL if the MAPI_CREATE flag is set in the  _ulFlags_ parameter.</span></span> 
    
 <span data-ttu-id="8d117-114">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="8d117-114">_ulFlags_</span></span>
  
> <span data-ttu-id="8d117-115">возврата Битовая маска флагов, указывающая, как должны возвращаться идентификаторы свойств.</span><span class="sxs-lookup"><span data-stu-id="8d117-115">[in] A bitmask of flags that indicates how the property identifiers should be returned.</span></span> <span data-ttu-id="8d117-116">Можно задать следующий флаг:</span><span class="sxs-lookup"><span data-stu-id="8d117-116">The following flag can be set:</span></span>
    
<span data-ttu-id="8d117-117">МАПИ_КРЕАТЕ</span><span class="sxs-lookup"><span data-stu-id="8d117-117">MAPI_CREATE</span></span> 
  
> <span data-ttu-id="8d117-118">Присваивает идентификатор свойства, если он еще не назначен, одному или нескольким именам, включенным в массив имен свойств, на который указывает _лпппропнамес_.</span><span class="sxs-lookup"><span data-stu-id="8d117-118">Assigns a property identifier, if one has not yet been assigned, to one or more of the names included in the property name array pointed to by  _lppPropNames_.</span></span> <span data-ttu-id="8d117-119">Этот флаг регистрирует идентификатор в таблице сопоставлений "имя — идентификатор".</span><span class="sxs-lookup"><span data-stu-id="8d117-119">This flag internally registers the identifier in the name-to-identifier mapping table.</span></span>
    
 <span data-ttu-id="8d117-120">_Лпппроптагс_</span><span class="sxs-lookup"><span data-stu-id="8d117-120">_lppPropTags_</span></span>
  
> <span data-ttu-id="8d117-121">вышли Указатель на указатель на массив тегов свойств, который содержит существующие или новые назначенные идентификаторы свойств.</span><span class="sxs-lookup"><span data-stu-id="8d117-121">[out] A pointer to a pointer to an array of property tags that contains existing or newly assigned property identifiers.</span></span> <span data-ttu-id="8d117-122">Для типов свойств для тегов свойств в этом массиве задано значение **пт_унспеЦифиед**.</span><span class="sxs-lookup"><span data-stu-id="8d117-122">The property types for the property tags in this array are set to **PT_UNSPECIFIED**.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="8d117-123">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="8d117-123">Return value</span></span>

<span data-ttu-id="8d117-124">S_OK</span><span class="sxs-lookup"><span data-stu-id="8d117-124">S_OK</span></span> 
  
> <span data-ttu-id="8d117-125">Идентификаторы для указанных имен свойств успешно возвращены.</span><span class="sxs-lookup"><span data-stu-id="8d117-125">The identifiers for the specified property names were successfully returned.</span></span>
    
<span data-ttu-id="8d117-126">МАПИ_Е_НО_СУППОРТ</span><span class="sxs-lookup"><span data-stu-id="8d117-126">MAPI_E_NO_SUPPORT</span></span> 
  
> <span data-ttu-id="8d117-127">Объект не поддерживает именованные свойства.</span><span class="sxs-lookup"><span data-stu-id="8d117-127">The object does not support named properties.</span></span>
    
<span data-ttu-id="8d117-128">МАПИ_Е_НОТ_ЕНАУГХ_МЕМОРИ</span><span class="sxs-lookup"><span data-stu-id="8d117-128">MAPI_E_NOT_ENOUGH_MEMORY</span></span> 
  
> <span data-ttu-id="8d117-129">Недостаточно памяти для получения идентификаторов.</span><span class="sxs-lookup"><span data-stu-id="8d117-129">Insufficient memory was available to retrieve the identifiers.</span></span>
    
<span data-ttu-id="8d117-130">МАПИ_Е_ТУ_БИГ</span><span class="sxs-lookup"><span data-stu-id="8d117-130">MAPI_E_TOO_BIG</span></span> 
  
> <span data-ttu-id="8d117-131">Операция не может быть выполнена, так как ей требуется слишком много тегов свойств, которые необходимо вернуть.</span><span class="sxs-lookup"><span data-stu-id="8d117-131">The operation cannot be performed because it requires too many property tags to be returned.</span></span>
    
<span data-ttu-id="8d117-132">МАПИ_В_ЕРРОРС_РЕТУРНЕД</span><span class="sxs-lookup"><span data-stu-id="8d117-132">MAPI_W_ERRORS_RETURNED</span></span> 
  
> <span data-ttu-id="8d117-133">Вызов выполнен в целом, но не удалось вернуть один или несколько идентификаторов свойств.</span><span class="sxs-lookup"><span data-stu-id="8d117-133">The call succeeded overall, but one or more property identifiers could not be returned.</span></span> <span data-ttu-id="8d117-134">Соответствующему типу свойства для каждого недоступного свойства задается значение **пт_еррор** , а для идентификатора — ноль.</span><span class="sxs-lookup"><span data-stu-id="8d117-134">The corresponding property type for each unavailable property is set to **PT_ERROR** and its identifier to zero.</span></span> <span data-ttu-id="8d117-135">При возвращении этого предупреждения обработайте вызов как успешный.</span><span class="sxs-lookup"><span data-stu-id="8d117-135">When this warning is returned, handle the call as successful.</span></span> <span data-ttu-id="8d117-136">Чтобы проверить это предупреждение, используйте макрос **хр_фаилед** .</span><span class="sxs-lookup"><span data-stu-id="8d117-136">To test for this warning, use the **HR_FAILED** macro.</span></span> <span data-ttu-id="8d117-137">Просмотр и [Использование макросов для обработки ошибок](using-macros-for-error-handling.md).</span><span class="sxs-lookup"><span data-stu-id="8d117-137">See [Using Macros for Error Handling](using-macros-for-error-handling.md).</span></span>
    
## <a name="remarks"></a><span data-ttu-id="8d117-138">Примечания</span><span class="sxs-lookup"><span data-stu-id="8d117-138">Remarks</span></span>

<span data-ttu-id="8d117-139">Метод **IMAPIProp:: жетидсфромнамес** извлекает массив тегов свойств, которые содержат идентификаторы свойств для одного или нескольких именованных свойств.</span><span class="sxs-lookup"><span data-stu-id="8d117-139">The **IMAPIProp::GetIDsFromNames** method retrieves an array of property tags that hold the property identifiers for one or more named properties.</span></span> <span data-ttu-id="8d117-140">**IMAPIProp:: жетидсфромнамес** может вызываться для выполнения следующих действий:</span><span class="sxs-lookup"><span data-stu-id="8d117-140">**IMAPIProp::GetIDsFromNames** can be called to do the following:</span></span> 
  
- <span data-ttu-id="8d117-141">Создание идентификаторов для новых имен.</span><span class="sxs-lookup"><span data-stu-id="8d117-141">Create identifiers for new names.</span></span>
    
- <span data-ttu-id="8d117-142">Получение идентификаторов для определенных имен.</span><span class="sxs-lookup"><span data-stu-id="8d117-142">Retrieve identifiers for specific names.</span></span>
    
- <span data-ttu-id="8d117-143">Получение идентификаторов для всех именованных свойств, включенных в сопоставление объекта.</span><span class="sxs-lookup"><span data-stu-id="8d117-143">Retrieve identifiers for all named properties that are included in the object's mapping.</span></span>
    
<span data-ttu-id="8d117-144">Именованные свойства обычно используются поставщиками хранилищ сообщений для папок и сообщений.</span><span class="sxs-lookup"><span data-stu-id="8d117-144">Named properties are typically used by message store providers for folders and messages.</span></span> <span data-ttu-id="8d117-145">Другие объекты, такие как пользователи обмена сообщениями и разделы профилей, могут не поддерживать связь имен с идентификаторами свойств и могут возвращать МАПИ_Е_НО_СУППОРТ из **жетидсфромнамес**.</span><span class="sxs-lookup"><span data-stu-id="8d117-145">Other objects, such as messaging users and profile sections, might not support the association of names to property identifiers and might return MAPI_E_NO_SUPPORT from **GetIDsFromNames**.</span></span>
  
<span data-ttu-id="8d117-146">Если возникает ошибка, возвращающая идентификатор для определенного имени, **жетидсфромнамес** возвращает мапи_в_еррорс_ретурнед и задает тип свойства в записи массива тегов свойства, соответствующей имени \*\*пт_еррор\*\* , и идентификатору, равным нулю.</span><span class="sxs-lookup"><span data-stu-id="8d117-146">If there is an error that returns an identifier for a particular name, **GetIDsFromNames** returns MAPI_W_ERRORS_RETURNED and sets the property type in the property tag array entry that corresponds to the name to **PT_ERROR** and the identifier to zero.</span></span> 
  
<span data-ttu-id="8d117-147">Сопоставление имен с идентификатором представлено свойством объекта **пр_маппинг_сигнатуре** ([PidTagMappingSignature](pidtagmappingsignature-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="8d117-147">Name-to-identifier mapping is represented by an object's **PR_MAPPING_SIGNATURE** ([PidTagMappingSignature](pidtagmappingsignature-canonical-property.md)) property.</span></span> <span data-ttu-id="8d117-148">**Пр_маппинг_сигнатуре** содержит структуру [мапиуид](mapiuid.md) , указывающую поставщика услуг, ответственного за объект.</span><span class="sxs-lookup"><span data-stu-id="8d117-148">**PR_MAPPING_SIGNATURE** contains a [MAPIUID](mapiuid.md) structure that indicates the service provider responsible for the object.</span></span> <span data-ttu-id="8d117-149">Если свойство **пр_маппинг_сигнатуре** одинаково для двух объектов, предполагается, что эти объекты используют одно и то же сопоставление имен и идентификаторов.</span><span class="sxs-lookup"><span data-stu-id="8d117-149">If the **PR_MAPPING_SIGNATURE** property is the same for two objects, assume that these objects use the same name-to-identifier mapping.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="8d117-150">Примечания для исполнителей</span><span class="sxs-lookup"><span data-stu-id="8d117-150">Notes to implementers</span></span>

<span data-ttu-id="8d117-151">Идентификаторы, которые вы передаете в массиве тегов свойств, на который указывает параметр _лпппропнамес_ , должны находиться в диапазоне от 0x8000 до 0xFFFE.</span><span class="sxs-lookup"><span data-stu-id="8d117-151">The identifiers that you pass back in the property tag array pointed to by the  _lppPropNames_ parameter must be in the 0x8000 to 0xFFFE range.</span></span> <span data-ttu-id="8d117-152">Записи в этом массиве должны находиться в том же порядке, что и имена, переданные в массиве имен свойств, на который указывает _лпппропнамес_.</span><span class="sxs-lookup"><span data-stu-id="8d117-152">The entries in this array must be in the same order as the names passed in the property name array pointed to by  _lppPropNames_.</span></span> 
  
<span data-ttu-id="8d117-153">Если вы поддерживаете именованные свойства в контейнере, используйте одинаковое сопоставление имен и идентификаторов для всех объектов в вашем контейнере (то есть не используйте для каждой папки в хранилище сообщений или каждого сообщения в папке другое сопоставление).</span><span class="sxs-lookup"><span data-stu-id="8d117-153">If you support named properties on a container, use the same name-to-identifier mapping for all objects in your container (that is, do not use a different mapping for each folder in your message store or each message in your folder).</span></span>
  
## <a name="notes-to-callers"></a><span data-ttu-id="8d117-154">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="8d117-154">Notes to callers</span></span>

<span data-ttu-id="8d117-155">Так как типы свойств для возвращенных идентификаторов в массиве тегов свойств, на который указывает _лпппроптагс_ , имеют значение **пт_унспеЦифиед**, необходимо вызвать метод [IMAPIProp:: SetProps](imapiprop-setprops.md) для получения точных типов.</span><span class="sxs-lookup"><span data-stu-id="8d117-155">Because the property types for the returned identifiers in the property tag array pointed to by  _lppPropTags_ are set to **PT_UNSPECIFIED**, you will have to call the [IMAPIProp::SetProps](imapiprop-setprops.md) method to retrieve the accurate types.</span></span> 
  
<span data-ttu-id="8d117-156">Если вы перемещаете или копируете объекты с именованными свойствами, а исходный и конечный объекты имеют разные подписи сопоставления, как указано значениями их свойств **пр_маппинг_сигнатуре** , необходимо сохранить имена во время этих операций.</span><span class="sxs-lookup"><span data-stu-id="8d117-156">If you move or copy objects with named properties, and the source and destination objects have different mapping signatures as indicated by the values of their **PR_MAPPING_SIGNATURE** properties, you must preserve the names during these operations.</span></span> <span data-ttu-id="8d117-157">Чтобы сохранить имена свойств, измените соответствующие идентификаторы свойств в соответствии с сопоставлением имен с идентификатором целевого объекта.</span><span class="sxs-lookup"><span data-stu-id="8d117-157">To preserve property names, adjust the corresponding property identifiers to match the name-to-identifier mapping of the destination object.</span></span> 
  
<span data-ttu-id="8d117-158">Некоторые объекты имеют ограничения на количество идентификаторов свойств, которые могут иметь имена.</span><span class="sxs-lookup"><span data-stu-id="8d117-158">Some objects have a limit as to the number of property identifiers they can name.</span></span> <span data-ttu-id="8d117-159">Если вызов **жетидсфромнамес** приводит к превышению этого ограничения, метод возвращает мапи_е_ту_биг.</span><span class="sxs-lookup"><span data-stu-id="8d117-159">If a call to **GetIDsFromNames** causes this limit to be exceeded, the method returns MAPI_E_TOO_BIG.</span></span> <span data-ttu-id="8d117-160">В этом случае запрос выполняется по идентификатору.</span><span class="sxs-lookup"><span data-stu-id="8d117-160">In this case, query by identifier.</span></span> 
  
<span data-ttu-id="8d117-161">Дополнительные сведения см. [](mapi-named-properties.md)</span><span class="sxs-lookup"><span data-stu-id="8d117-161">For more information, see [MAPI Named Properties](mapi-named-properties.md).</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="8d117-162">Справочные материалы по MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="8d117-162">MFCMAPI reference</span></span>

<span data-ttu-id="8d117-163">Пример кода MFCMAPI указан в приведенной ниже таблице.</span><span class="sxs-lookup"><span data-stu-id="8d117-163">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="8d117-164">**Файл**</span><span class="sxs-lookup"><span data-stu-id="8d117-164">**File**</span></span>|<span data-ttu-id="8d117-165">**Функция**</span><span class="sxs-lookup"><span data-stu-id="8d117-165">**Function**</span></span>|<span data-ttu-id="8d117-166">**Примечание**</span><span class="sxs-lookup"><span data-stu-id="8d117-166">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="8d117-167">Синглемапипроплистктрл. cpp</span><span class="sxs-lookup"><span data-stu-id="8d117-167">SingleMAPIPropListCtrl.cpp</span></span>  <br/> |<span data-ttu-id="8d117-168">Ксинглемапипроплистктрл:: Финдаллнамедпропсусед</span><span class="sxs-lookup"><span data-stu-id="8d117-168">CSingleMAPIPropListCtrl::FindAllNamedPropsUsed</span></span>  <br/> |<span data-ttu-id="8d117-169">MFCMAPI использует метод **IMAPIProp:: жетидсфромнамес** для получения тегов свойств для всех сопоставленных именованных свойств.</span><span class="sxs-lookup"><span data-stu-id="8d117-169">MFCMAPI uses the **IMAPIProp::GetIDsFromNames** method to obtain property tags for all named properties that have been mapped.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="8d117-170">См. также</span><span class="sxs-lookup"><span data-stu-id="8d117-170">See also</span></span>



[<span data-ttu-id="8d117-171">IMAPIProp::GetNamesFromIDs</span><span class="sxs-lookup"><span data-stu-id="8d117-171">IMAPIProp::GetNamesFromIDs</span></span>](imapiprop-getnamesfromids.md)
  
[<span data-ttu-id="8d117-172">IMAPIProp::SetProps</span><span class="sxs-lookup"><span data-stu-id="8d117-172">IMAPIProp::SetProps</span></span>](imapiprop-setprops.md)
  
[<span data-ttu-id="8d117-173">MAPINAMEID</span><span class="sxs-lookup"><span data-stu-id="8d117-173">MAPINAMEID</span></span>](mapinameid.md)
  
[<span data-ttu-id="8d117-174">MAPIUID</span><span class="sxs-lookup"><span data-stu-id="8d117-174">MAPIUID</span></span>](mapiuid.md)
  
[<span data-ttu-id="8d117-175">IMAPIProp : IUnknown</span><span class="sxs-lookup"><span data-stu-id="8d117-175">IMAPIProp : IUnknown</span></span>](imapipropiunknown.md)


[<span data-ttu-id="8d117-176">MFCMAPI как пример кода</span><span class="sxs-lookup"><span data-stu-id="8d117-176">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)
  
[<span data-ttu-id="8d117-177">Именованные свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="8d117-177">MAPI Named Properties</span></span>](mapi-named-properties.md)
  
[<span data-ttu-id="8d117-178">Использование макросов для обработки ошибок</span><span class="sxs-lookup"><span data-stu-id="8d117-178">Using Macros for Error Handling</span></span>](using-macros-for-error-handling.md)

