---
title: Имапипропопенпроперти
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIProp.OpenProperty
api_type:
- COM
ms.assetid: e400e6cc-4e36-43fc-9304-b688a0a7fd77
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 7bf1d6912e44319c36e288cd3870218e8c4e45ff
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32319812"
---
# <a name="imapipropopenproperty"></a><span data-ttu-id="12312-103">IMAPIProp::OpenProperty</span><span class="sxs-lookup"><span data-stu-id="12312-103">IMAPIProp::OpenProperty</span></span>

<span data-ttu-id="12312-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="12312-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="12312-105">Возвращает указатель на интерфейс, который можно использовать для доступа к свойству.</span><span class="sxs-lookup"><span data-stu-id="12312-105">Returns a pointer to an interface that can be used to access a property.</span></span>
  
```cpp
HRESULT OpenProperty(
  ULONG ulPropTag,
  LPCIID lpiid,
  ULONG ulInterfaceOptions,
  ULONG ulFlags,
  LPUNKNOWN FAR * lppUnk
);
```

## <a name="parameters"></a><span data-ttu-id="12312-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="12312-106">Parameters</span></span>

 <span data-ttu-id="12312-107">_Улпроптаг_</span><span class="sxs-lookup"><span data-stu-id="12312-107">_ulPropTag_</span></span>
  
> <span data-ttu-id="12312-108">возврата Тег свойства для свойства, к которому необходимо получить доступ.</span><span class="sxs-lookup"><span data-stu-id="12312-108">[in] The property tag for the property to be accessed.</span></span> <span data-ttu-id="12312-109">Идентификатор и тип должны быть включены в тег Property.</span><span class="sxs-lookup"><span data-stu-id="12312-109">Both the identifier and the type must be included in the property tag.</span></span>
    
 <span data-ttu-id="12312-110">_лпиид_</span><span class="sxs-lookup"><span data-stu-id="12312-110">_lpiid_</span></span>
  
> <span data-ttu-id="12312-111">возврата Указатель на идентификатор интерфейса, который будет использоваться для доступа к свойству.</span><span class="sxs-lookup"><span data-stu-id="12312-111">[in] A pointer to the identifier for the interface to be used to access the property.</span></span> <span data-ttu-id="12312-112">Параметр _лпиид_ не должен иметь **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="12312-112">The  _lpiid_ parameter must not be **null**.</span></span>
    
 <span data-ttu-id="12312-113">_Улинтерфацеоптионс_</span><span class="sxs-lookup"><span data-stu-id="12312-113">_ulInterfaceOptions_</span></span>
  
> <span data-ttu-id="12312-114">возврата Данные, связанные с интерфейсом, определяемым параметром _лпиид_ .</span><span class="sxs-lookup"><span data-stu-id="12312-114">[in] Data that relates to the interface identified by the  _lpiid_ parameter.</span></span> 
    
 <span data-ttu-id="12312-115">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="12312-115">_ulFlags_</span></span>
  
> <span data-ttu-id="12312-116">возврата Битовая маска флагов, которые управляют доступом к свойству.</span><span class="sxs-lookup"><span data-stu-id="12312-116">[in] A bitmask of flags that controls access to the property.</span></span> <span data-ttu-id="12312-117">Можно задать следующие флаги:</span><span class="sxs-lookup"><span data-stu-id="12312-117">The following flags can be set:</span></span>
    
<span data-ttu-id="12312-118">МАПИ_КРЕАТЕ</span><span class="sxs-lookup"><span data-stu-id="12312-118">MAPI_CREATE</span></span> 
  
> <span data-ttu-id="12312-119">Если свойство не существует, оно должно быть создано.</span><span class="sxs-lookup"><span data-stu-id="12312-119">If the property does not exist, it should be created.</span></span> <span data-ttu-id="12312-120">Если свойство существует, текущее значение свойства должно быть отменено.</span><span class="sxs-lookup"><span data-stu-id="12312-120">If the property does exist, the current value of the property should be discarded.</span></span> <span data-ttu-id="12312-121">Когда вызывающий абонент устанавливает флаг МАПИ_КРЕАТЕ, он также должен установить флаг МАПИ_МОДИФИ.</span><span class="sxs-lookup"><span data-stu-id="12312-121">When a caller sets the MAPI_CREATE flag, it should also set the MAPI_MODIFY flag.</span></span>
    
<span data-ttu-id="12312-122">МАПИ_ДЕФЕРРЕД_ЕРРОРС</span><span class="sxs-lookup"><span data-stu-id="12312-122">MAPI_DEFERRED_ERRORS</span></span> 
  
> <span data-ttu-id="12312-123">Разрешает успешное возвращение **опенпроперти** , возможно, перед тем, как объект будет полностью доступен вызывающему абоненту.</span><span class="sxs-lookup"><span data-stu-id="12312-123">Allows **OpenProperty** to return successfully, possibly before the object is fully available to the caller.</span></span> <span data-ttu-id="12312-124">Если объект недоступен, то выполнение следующего вызова объекта может вызвать ошибку.</span><span class="sxs-lookup"><span data-stu-id="12312-124">If the object is not available, making a subsequent object call can raise an error.</span></span> 
    
<span data-ttu-id="12312-125">МАПИ_МОДИФИ</span><span class="sxs-lookup"><span data-stu-id="12312-125">MAPI_MODIFY</span></span> 
  
> <span data-ttu-id="12312-126">МАПИ_МОДИФИ является обязательным в следующих ситуациях:</span><span class="sxs-lookup"><span data-stu-id="12312-126">MAPI_MODIFY is required in these situations:</span></span>
    
  - <span data-ttu-id="12312-127">При открытии свойства потока, например **иид_истреам**, для его изменения.</span><span class="sxs-lookup"><span data-stu-id="12312-127">When opening a stream property, such as **IID_IStream**, to modify it.</span></span>
    
  - <span data-ttu-id="12312-128">При открытии вложения внедренного сообщения, например [пр_аттач_дата_обж](pidtagattachdataobject-canonical-property.md) , открытого с помощью **иид_имессаже**, для его изменения.</span><span class="sxs-lookup"><span data-stu-id="12312-128">When opening an embedded message attachment, such as [PR_ATTACH_DATA_OBJ](pidtagattachdataobject-canonical-property.md) opened with **IID_IMessage**, to modify it.</span></span>
    
 <span data-ttu-id="12312-129">_Лппунк_</span><span class="sxs-lookup"><span data-stu-id="12312-129">_lppUnk_</span></span>
  
> <span data-ttu-id="12312-130">вышли Указатель на запрашиваемый интерфейс, который будет использоваться для доступа к свойству.</span><span class="sxs-lookup"><span data-stu-id="12312-130">[out] A pointer to the requested interface to be used for property access.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="12312-131">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="12312-131">Return value</span></span>

<span data-ttu-id="12312-132">S_OK</span><span class="sxs-lookup"><span data-stu-id="12312-132">S_OK</span></span> 
  
> <span data-ttu-id="12312-133">Запрошенный указатель интерфейса успешно возвращен.</span><span class="sxs-lookup"><span data-stu-id="12312-133">The requested interface pointer was successfully returned.</span></span>
    
<span data-ttu-id="12312-134">МАПИ_Е_ИНТЕРФАЦЕ_НОТ_СУППОРТЕД</span><span class="sxs-lookup"><span data-stu-id="12312-134">MAPI_E_INTERFACE_NOT_SUPPORTED</span></span> 
  
> <span data-ttu-id="12312-135">Запрошенный интерфейс не поддерживается для этого свойства.</span><span class="sxs-lookup"><span data-stu-id="12312-135">The requested interface is not supported for this property.</span></span>
    
<span data-ttu-id="12312-136">МАПИ_Е_НО_АКЦЕСС</span><span class="sxs-lookup"><span data-stu-id="12312-136">MAPI_E_NO_ACCESS</span></span> 
  
> <span data-ttu-id="12312-137">Вызывающий не имеет достаточных разрешений для доступа к свойству.</span><span class="sxs-lookup"><span data-stu-id="12312-137">The caller has insufficient permissions to access the property.</span></span>
    
<span data-ttu-id="12312-138">МАПИ_Е_НО_СУППОРТ</span><span class="sxs-lookup"><span data-stu-id="12312-138">MAPI_E_NO_SUPPORT</span></span> 
  
> <span data-ttu-id="12312-139">Объект не может предоставлять доступ к этому свойству через запрошенный интерфейс.</span><span class="sxs-lookup"><span data-stu-id="12312-139">The object cannot provide access to this property through the requested interface.</span></span>
    
<span data-ttu-id="12312-140">МАПИ_Е_НОТ_ФАУНД</span><span class="sxs-lookup"><span data-stu-id="12312-140">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="12312-141">Запрошенное свойство не существует, а МАПИ_КРЕАТЕ не задано в параметре _ulFlags_ .</span><span class="sxs-lookup"><span data-stu-id="12312-141">The requested property does not exist and MAPI_CREATE was not set in the  _ulFlags_ parameter.</span></span> 
    
<span data-ttu-id="12312-142">МАПИ_Е_ИНВАЛИД_ПАРАМЕТЕР</span><span class="sxs-lookup"><span data-stu-id="12312-142">MAPI_E_INVALID_PARAMETER</span></span> 
  
> <span data-ttu-id="12312-143">Для типа свойства в теге задано значение ПТ_УНСПЕЦИФИЕД.</span><span class="sxs-lookup"><span data-stu-id="12312-143">The property type in the tag is set to PT_UNSPECIFIED.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="12312-144">Комментарии</span><span class="sxs-lookup"><span data-stu-id="12312-144">Remarks</span></span>

<span data-ttu-id="12312-145">Метод **IMAPIProp:: опенпроперти** предоставляет доступ к свойству через определенный интерфейс.</span><span class="sxs-lookup"><span data-stu-id="12312-145">The **IMAPIProp::OpenProperty** method provides access to a property through a particular interface.</span></span> <span data-ttu-id="12312-146">**Опенпроперти** является альтернативой методам [IMAPIProp::](imapiprop-getprops.md) -PROPS и [IMAPIProp:: SetProps](imapiprop-setprops.md) .</span><span class="sxs-lookup"><span data-stu-id="12312-146">**OpenProperty** is an alternative to the [IMAPIProp::GetProps](imapiprop-getprops.md) and [IMAPIProp::SetProps](imapiprop-setprops.md) methods.</span></span> <span data-ttu-id="12312-147">Если свойства \*\*\*\* -PROPS или **SetProps** не выполняются из-за того, что свойство слишком велико или слишком сложное, вызовите **опенпроперти**.</span><span class="sxs-lookup"><span data-stu-id="12312-147">When either **GetProps** or **SetProps** fails because the property is too large or too complex, call **OpenProperty**.</span></span> <span data-ttu-id="12312-148">**Опенпроперти** обычно используется для доступа к свойствам типа пт_обжект.</span><span class="sxs-lookup"><span data-stu-id="12312-148">**OpenProperty** is typically used to access properties of type PT_OBJECT.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="12312-149">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="12312-149">Notes to callers</span></span>

<span data-ttu-id="12312-150">Чтобы получить доступ к вложениям сообщений, откройте свойство **пр_аттач_дата_обж** ([PidTagAttachDataObject](pidtagattachdataobject-canonical-property.md)) с другим идентификатором интерфейса в зависимости от типа вложения.</span><span class="sxs-lookup"><span data-stu-id="12312-150">To access message attachments, open the **PR_ATTACH_DATA_OBJ** ([PidTagAttachDataObject](pidtagattachdataobject-canonical-property.md)) property with a different interface identifier, depending on the type of attachment.</span></span> <span data-ttu-id="12312-151">В следующей таблице описано, как вызывать **опенпроперти** для различных типов вложений:</span><span class="sxs-lookup"><span data-stu-id="12312-151">The following table describes how to call **OpenProperty** for the different types of attachments:</span></span> 
  
|<span data-ttu-id="12312-152">**Тип вложения**</span><span class="sxs-lookup"><span data-stu-id="12312-152">**Type of attachment**</span></span>|<span data-ttu-id="12312-153">**Используемый идентификатор интерфейса**</span><span class="sxs-lookup"><span data-stu-id="12312-153">**Interface identifier to use**</span></span>|
|:-----|:-----|
|<span data-ttu-id="12312-154">Binary</span><span class="sxs-lookup"><span data-stu-id="12312-154">Binary</span></span>  <br/> |<span data-ttu-id="12312-155">Иид_истреам</span><span class="sxs-lookup"><span data-stu-id="12312-155">IID_IStream</span></span>  <br/> |
|<span data-ttu-id="12312-156">Строка</span><span class="sxs-lookup"><span data-stu-id="12312-156">String</span></span>  <br/> |<span data-ttu-id="12312-157">Иид_истреам</span><span class="sxs-lookup"><span data-stu-id="12312-157">IID_IStream</span></span>  <br/> |
|<span data-ttu-id="12312-158">Сообщение</span><span class="sxs-lookup"><span data-stu-id="12312-158">Message</span></span>  <br/> |<span data-ttu-id="12312-159">Иид_имессаже</span><span class="sxs-lookup"><span data-stu-id="12312-159">IID_IMessage</span></span>  <br/> |
|<span data-ttu-id="12312-160">OLE 2,0</span><span class="sxs-lookup"><span data-stu-id="12312-160">OLE 2.0</span></span>  <br/> |<span data-ttu-id="12312-161">Иид_истреамдокфиле</span><span class="sxs-lookup"><span data-stu-id="12312-161">IID_IStreamDocfile</span></span>  <br/> |
   
<span data-ttu-id="12312-162">**Помощью istreamdocfile** является производным от интерфейса [IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx) , основанного на составном файле OLE 2,0.</span><span class="sxs-lookup"><span data-stu-id="12312-162">**IStreamDocfile** is a derivative of the [IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx) interface that is based on an OLE 2.0 compound file.</span></span> <span data-ttu-id="12312-163">**Помощью istreamdocfile** — лучший выбор для доступа к вложениям OLE 2,0, так как он требует наименьшего объема издержек.</span><span class="sxs-lookup"><span data-stu-id="12312-163">**IStreamDocfile** is the best choice for accessing OLE 2.0 attachments because it involves the least amount of overhead.</span></span> <span data-ttu-id="12312-164">Вы можете использовать Иид_истреамдокфиле для тех свойств, которые содержат данные, хранящиеся в структурированном хранилище, доступном через интерфейс [IStorage](https://msdn.microsoft.com/library/aa380015%28VS.85%29.aspx) .</span><span class="sxs-lookup"><span data-stu-id="12312-164">You can use IID_IStreamDocFile for those properties that contain data stored in structured storage available through the [IStorage](https://msdn.microsoft.com/library/aa380015%28VS.85%29.aspx) interface.</span></span> 
  
<span data-ttu-id="12312-165">Дополнительные сведения о том, как использовать **опенпроперти** с вложениями, можно узнать в свойстве **Пр_аттач_дата_обж** и [открыть вложение](opening-an-attachment.md).</span><span class="sxs-lookup"><span data-stu-id="12312-165">For more information about how to use **OpenProperty** with attachments, see the **PR_ATTACH_DATA_OBJ** property and [Opening an Attachment](opening-an-attachment.md).</span></span>
  
<span data-ttu-id="12312-166">Не используйте указатель **IStream** , который вы получаете для вызова метода [Seek](https://msdn.microsoft.com/library/aa380043%28v=VS.85%29.aspx) или [SetSize](https://msdn.microsoft.com/library/aa380044%28v=VS.85%29.aspx) , если не используется переменная position или size.</span><span class="sxs-lookup"><span data-stu-id="12312-166">Do not use the **IStream** pointer that you receive to call either its [Seek](https://msdn.microsoft.com/library/aa380043%28v=VS.85%29.aspx) or [SetSize](https://msdn.microsoft.com/library/aa380044%28v=VS.85%29.aspx) method unless you use a zero position or size variable.</span></span> <span data-ttu-id="12312-167">Кроме того, не полагайтесь на значение выходного параметра _плибневпоситион_ , возвращенного при вызове **Seek** .</span><span class="sxs-lookup"><span data-stu-id="12312-167">Also, do not rely on the value of the  _plibNewPosition_ output parameter returned from the **Seek** call.</span></span> 
  
<span data-ttu-id="12312-168">При вызове **опенпроперти** для доступа к свойству с помощью интерфейса **IStream** используйте только этот интерфейс для внесения изменений.</span><span class="sxs-lookup"><span data-stu-id="12312-168">If you call **OpenProperty** to access a property with the **IStream** interface, use only that interface to make changes to it.</span></span> <span data-ttu-id="12312-169">Не пытайтесь обновить свойство с любыми другими методами [IMAPIProp: IUnknown](imapipropiunknown.md) , такими как **SetProps** или [IMAPIProp::D елетепропс](imapiprop-deleteprops.md).</span><span class="sxs-lookup"><span data-stu-id="12312-169">Do not attempt to update the property with any of the other [IMAPIProp : IUnknown](imapipropiunknown.md) methods, such as **SetProps** or [IMAPIProp::DeleteProps](imapiprop-deleteprops.md).</span></span> 
  
<span data-ttu-id="12312-170">Не пытайтесь открыть свойство с помощью **опенпроперти** более одного раза.</span><span class="sxs-lookup"><span data-stu-id="12312-170">Do not try to open a property with **OpenProperty** more than once.</span></span> <span data-ttu-id="12312-171">Результаты не определены, так как они могут отличаться от поставщика к поставщику.</span><span class="sxs-lookup"><span data-stu-id="12312-171">The results are undefined because they can vary from provider to provider.</span></span> 
  
<span data-ttu-id="12312-172">Если необходимо изменить свойство, которое должно быть открыто, установите флаг МАПИ_МОДИФИ.</span><span class="sxs-lookup"><span data-stu-id="12312-172">If you need to modify the property to be opened, set the MAPI_MODIFY flag.</span></span> <span data-ttu-id="12312-173">Если вы не знаете, поддерживает ли объект свойство, но считаете, что это необходимо, установите флаги МАПИ_КРЕАТЕ и МАПИ_МОДИФИ.</span><span class="sxs-lookup"><span data-stu-id="12312-173">If you are not sure whether the object supports the property but you think it should, set the MAPI_CREATE and MAPI_MODIFY flags.</span></span> <span data-ttu-id="12312-174">Если задано значение МАПИ_КРЕАТЕ, необходимо также установить МАПИ_МОДИФИ.</span><span class="sxs-lookup"><span data-stu-id="12312-174">Whenever MAPI_CREATE is set, MAPI_MODIFY must also be set.</span></span>
  
<span data-ttu-id="12312-175">Вы несете ответственность за переопределение указателя интерфейса, возвращаемого в параметре _лппунк_ , на тот, который подходит для интерфейса, указанного в параметре _лпиид_ .</span><span class="sxs-lookup"><span data-stu-id="12312-175">You are responsible for recasting the interface pointer returned in the  _lppUnk_ parameter to one that is appropriate for the interface specified in the  _lpiid_ parameter.</span></span> <span data-ttu-id="12312-176">Кроме того, необходимо использовать возвращенный указатель, чтобы вызвать метод [IUnknown:: Release](https://msdn.microsoft.com/library/ms682317%28v=VS.85%29.aspx) после завершения работы с ним.</span><span class="sxs-lookup"><span data-stu-id="12312-176">You must also use the returned pointer to call its [IUnknown::Release](https://msdn.microsoft.com/library/ms682317%28v=VS.85%29.aspx) method when you are finished with it.</span></span> 
  
<span data-ttu-id="12312-177">Иногда установка флагов в параметре _ulFlags_ недостаточно для указания типа доступа к требуемому свойству.</span><span class="sxs-lookup"><span data-stu-id="12312-177">Sometimes setting the flags in the  _ulFlags_ parameter is not enough to indicate the type of access to the property that is required.</span></span> <span data-ttu-id="12312-178">В параметре _улинтерфацеоптионс_ можно добавить дополнительные данные, например флаги.</span><span class="sxs-lookup"><span data-stu-id="12312-178">You can put additional data, such as flags, in the  _ulInterfaceOptions_ parameter.</span></span> <span data-ttu-id="12312-179">Эти данные зависят от интерфейса.</span><span class="sxs-lookup"><span data-stu-id="12312-179">This data is interface dependent.</span></span> <span data-ttu-id="12312-180">Некоторые интерфейсы (например, **IStream**) используют его, а другие — нет.</span><span class="sxs-lookup"><span data-stu-id="12312-180">Some interfaces (such as **IStream**) use it, and others do not.</span></span> <span data-ttu-id="12312-181">Например, при открытии свойства, которое необходимо изменить с помощью **IStream**, установите флаг стгм_врите в параметре _улинтерфацеоптионс_ в дополнение к мапи_модифи.</span><span class="sxs-lookup"><span data-stu-id="12312-181">For example, when you open a property to be modified with **IStream**, set the STGM_WRITE flag in the  _ulInterfaceOptions_ parameter in addition to MAPI_MODIFY.</span></span> <span data-ttu-id="12312-182">При открытии таблицы с помощью интерфейса [IMAPITable](imapitableiunknown.md) можно задать для параметра _улинтерфацеоптионс_ значение мапи_уникоде, чтобы указать, должны ли столбцы таблицы, содержащие строковые свойства, иметь формат Юникод.</span><span class="sxs-lookup"><span data-stu-id="12312-182">When you open a table by using the [IMAPITable](imapitableiunknown.md) interface, you can set  _ulInterfaceOptions_ to MAPI_UNICODE to indicate whether the columns in the table that hold string properties should be in Unicode format.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="12312-183">Справочные материалы по MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="12312-183">MFCMAPI reference</span></span>

<span data-ttu-id="12312-184">Пример кода MFCMAPI указан в приведенной ниже таблице.</span><span class="sxs-lookup"><span data-stu-id="12312-184">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="12312-185">**Файл**</span><span class="sxs-lookup"><span data-stu-id="12312-185">**File**</span></span>|<span data-ttu-id="12312-186">**Функция**</span><span class="sxs-lookup"><span data-stu-id="12312-186">**Function**</span></span>|<span data-ttu-id="12312-187">**Примечание**</span><span class="sxs-lookup"><span data-stu-id="12312-187">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="12312-188">Стреамедитор. cpp</span><span class="sxs-lookup"><span data-stu-id="12312-188">StreamEditor.cpp</span></span>  <br/> |<span data-ttu-id="12312-189">Кстреамедитор:: Реадтекстстреамфромпроперти</span><span class="sxs-lookup"><span data-stu-id="12312-189">CStreamEditor::ReadTextStreamFromProperty</span></span>  <br/> |<span data-ttu-id="12312-190">MFCMAPI использует метод **IMAPIProp:: опенпроперти** для получения потокового интерфейса для больших текстовых и двоичных свойств.</span><span class="sxs-lookup"><span data-stu-id="12312-190">MFCMAPI uses the **IMAPIProp::OpenProperty** method to retrieve a stream interface for large text and binary properties.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="12312-191">См. также</span><span class="sxs-lookup"><span data-stu-id="12312-191">See also</span></span>

- [<span data-ttu-id="12312-192">HrIStorageFromStream</span><span class="sxs-lookup"><span data-stu-id="12312-192">HrIStorageFromStream</span></span>](hristoragefromstream.md) 
- [<span data-ttu-id="12312-193">IMAPIProp::DeleteProps</span><span class="sxs-lookup"><span data-stu-id="12312-193">IMAPIProp::DeleteProps</span></span>](imapiprop-deleteprops.md) 
- [<span data-ttu-id="12312-194">IMAPIProp::GetProps</span><span class="sxs-lookup"><span data-stu-id="12312-194">IMAPIProp::GetProps</span></span>](imapiprop-getprops.md)
- [<span data-ttu-id="12312-195">IMAPIProp::SetProps</span><span class="sxs-lookup"><span data-stu-id="12312-195">IMAPIProp::SetProps</span></span>](imapiprop-setprops.md)
- [<span data-ttu-id="12312-196">IMAPISupport::IStorageFromStream</span><span class="sxs-lookup"><span data-stu-id="12312-196">IMAPISupport::IStorageFromStream</span></span>](imapisupport-istoragefromstream.md)
- [<span data-ttu-id="12312-197">IMAPITable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="12312-197">IMAPITable : IUnknown</span></span>](imapitableiunknown.md)
- [<span data-ttu-id="12312-198">IMAPIProp : IUnknown</span><span class="sxs-lookup"><span data-stu-id="12312-198">IMAPIProp : IUnknown</span></span>](imapipropiunknown.md)
- [<span data-ttu-id="12312-199">MFCMAPI как пример кода</span><span class="sxs-lookup"><span data-stu-id="12312-199">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)
- [<span data-ttu-id="12312-200">Открытие вложения</span><span class="sxs-lookup"><span data-stu-id="12312-200">Opening an Attachment</span></span>](opening-an-attachment.md)

