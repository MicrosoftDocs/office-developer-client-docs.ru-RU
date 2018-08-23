---
title: IMAPIPropOpenProperty
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
ms.openlocfilehash: e5f35474910f2257e18bcdc3b6b1dc661e2dc63a
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22563977"
---
# <a name="imapipropopenproperty"></a><span data-ttu-id="20d8a-103">IMAPIProp::OpenProperty</span><span class="sxs-lookup"><span data-stu-id="20d8a-103">IMAPIProp::OpenProperty</span></span>

<span data-ttu-id="20d8a-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="20d8a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="20d8a-105">Возвращает указатель на интерфейс, который можно использовать для доступа к свойству.</span><span class="sxs-lookup"><span data-stu-id="20d8a-105">Returns a pointer to an interface that can be used to access a property.</span></span>
  
```cpp
HRESULT OpenProperty(
  ULONG ulPropTag,
  LPCIID lpiid,
  ULONG ulInterfaceOptions,
  ULONG ulFlags,
  LPUNKNOWN FAR * lppUnk
);
```

## <a name="parameters"></a><span data-ttu-id="20d8a-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="20d8a-106">Parameters</span></span>

 <span data-ttu-id="20d8a-107">_ulPropTag_</span><span class="sxs-lookup"><span data-stu-id="20d8a-107">_ulPropTag_</span></span>
  
> <span data-ttu-id="20d8a-108">[in] Тег свойства для свойства, которое должно осуществляться.</span><span class="sxs-lookup"><span data-stu-id="20d8a-108">[in] The property tag for the property to be accessed.</span></span> <span data-ttu-id="20d8a-109">Идентификатор и типом должны быть включены в тег свойства.</span><span class="sxs-lookup"><span data-stu-id="20d8a-109">Both the identifier and the type must be included in the property tag.</span></span>
    
 <span data-ttu-id="20d8a-110">_lpiid_</span><span class="sxs-lookup"><span data-stu-id="20d8a-110">_lpiid_</span></span>
  
> <span data-ttu-id="20d8a-111">[in] Указатель на идентификатор для интерфейса, которые будут использоваться для доступа к свойству.</span><span class="sxs-lookup"><span data-stu-id="20d8a-111">[in] A pointer to the identifier for the interface to be used to access the property.</span></span> <span data-ttu-id="20d8a-112">Параметр _lpiid_ не должно быть **значение null**.</span><span class="sxs-lookup"><span data-stu-id="20d8a-112">The  _lpiid_ parameter must not be **null**.</span></span>
    
 <span data-ttu-id="20d8a-113">_ulInterfaceOptions_</span><span class="sxs-lookup"><span data-stu-id="20d8a-113">_ulInterfaceOptions_</span></span>
  
> <span data-ttu-id="20d8a-114">[in] Данные, связанные с интерфейсом, определенного параметром _lpiid_ .</span><span class="sxs-lookup"><span data-stu-id="20d8a-114">[in] Data that relates to the interface identified by the  _lpiid_ parameter.</span></span> 
    
 <span data-ttu-id="20d8a-115">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="20d8a-115">_ulFlags_</span></span>
  
> <span data-ttu-id="20d8a-116">[in] Битовая маска, элементы управления доступом к свойству флагов.</span><span class="sxs-lookup"><span data-stu-id="20d8a-116">[in] A bitmask of flags that controls access to the property.</span></span> <span data-ttu-id="20d8a-117">Можно задать следующие флажки:</span><span class="sxs-lookup"><span data-stu-id="20d8a-117">The following flags can be set:</span></span>
    
<span data-ttu-id="20d8a-118">MAPI_CREATE</span><span class="sxs-lookup"><span data-stu-id="20d8a-118">MAPI_CREATE</span></span> 
  
> <span data-ttu-id="20d8a-119">Если свойство не существует, он должен быть создан.</span><span class="sxs-lookup"><span data-stu-id="20d8a-119">If the property does not exist, it should be created.</span></span> <span data-ttu-id="20d8a-120">Если свойство существует, следует ли удалить текущее значение свойства.</span><span class="sxs-lookup"><span data-stu-id="20d8a-120">If the property does exist, the current value of the property should be discarded.</span></span> <span data-ttu-id="20d8a-121">Если вызывающий объект задает флаг MAPI_CREATE, он должен установить флаг MAPI_MODIFY.</span><span class="sxs-lookup"><span data-stu-id="20d8a-121">When a caller sets the MAPI_CREATE flag, it should also set the MAPI_MODIFY flag.</span></span>
    
<span data-ttu-id="20d8a-122">MAPI_DEFERRED_ERRORS</span><span class="sxs-lookup"><span data-stu-id="20d8a-122">MAPI_DEFERRED_ERRORS</span></span> 
  
> <span data-ttu-id="20d8a-123">Разрешает **OpenProperty** для возврата успешно, возможно перед объект полностью доступен для вызывающего абонента.</span><span class="sxs-lookup"><span data-stu-id="20d8a-123">Allows **OpenProperty** to return successfully, possibly before the object is fully available to the caller.</span></span> <span data-ttu-id="20d8a-124">Если объект недоступен, вызов последующих объектов может вызвать ошибку.</span><span class="sxs-lookup"><span data-stu-id="20d8a-124">If the object is not available, making a subsequent object call can raise an error.</span></span> 
    
<span data-ttu-id="20d8a-125">MAPI_MODIFY</span><span class="sxs-lookup"><span data-stu-id="20d8a-125">MAPI_MODIFY</span></span> 
  
> <span data-ttu-id="20d8a-126">MAPI_MODIFY требуется в следующих ситуациях:</span><span class="sxs-lookup"><span data-stu-id="20d8a-126">MAPI_MODIFY is required in these situations:</span></span>
    
  - <span data-ttu-id="20d8a-127">При открытии свойство потока, такие как **IID_IStream**, чтобы изменить его.</span><span class="sxs-lookup"><span data-stu-id="20d8a-127">When opening a stream property, such as **IID_IStream**, to modify it.</span></span>
    
  - <span data-ttu-id="20d8a-128">При открытии вложения внедренных сообщений, такие как [PR_ATTACH_DATA_OBJ](pidtagattachdataobject-canonical-property.md) , открытый с **IID_IMessage**, чтобы изменить его.</span><span class="sxs-lookup"><span data-stu-id="20d8a-128">When opening an embedded message attachment, such as [PR_ATTACH_DATA_OBJ](pidtagattachdataobject-canonical-property.md) opened with **IID_IMessage**, to modify it.</span></span>
    
 <span data-ttu-id="20d8a-129">_lppUnk_</span><span class="sxs-lookup"><span data-stu-id="20d8a-129">_lppUnk_</span></span>
  
> <span data-ttu-id="20d8a-130">[out] Указатель на запрашиваемый интерфейс, используемый для доступа к свойству.</span><span class="sxs-lookup"><span data-stu-id="20d8a-130">[out] A pointer to the requested interface to be used for property access.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="20d8a-131">������������ ��������</span><span class="sxs-lookup"><span data-stu-id="20d8a-131">Return value</span></span>

<span data-ttu-id="20d8a-132">ЗНАЧЕНИЕ S_OK</span><span class="sxs-lookup"><span data-stu-id="20d8a-132">S_OK</span></span> 
  
> <span data-ttu-id="20d8a-133">Указатель запрошенного интерфейса успешно возвращен.</span><span class="sxs-lookup"><span data-stu-id="20d8a-133">The requested interface pointer was successfully returned.</span></span>
    
<span data-ttu-id="20d8a-134">MAPI_E_INTERFACE_NOT_SUPPORTED</span><span class="sxs-lookup"><span data-stu-id="20d8a-134">MAPI_E_INTERFACE_NOT_SUPPORTED</span></span> 
  
> <span data-ttu-id="20d8a-135">Запрошенный интерфейс не поддерживается для этого свойства.</span><span class="sxs-lookup"><span data-stu-id="20d8a-135">The requested interface is not supported for this property.</span></span>
    
<span data-ttu-id="20d8a-136">MAPI_E_NO_ACCESS</span><span class="sxs-lookup"><span data-stu-id="20d8a-136">MAPI_E_NO_ACCESS</span></span> 
  
> <span data-ttu-id="20d8a-137">Вызывающий не имеет разрешений на доступ к свойству.</span><span class="sxs-lookup"><span data-stu-id="20d8a-137">The caller has insufficient permissions to access the property.</span></span>
    
<span data-ttu-id="20d8a-138">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="20d8a-138">MAPI_E_NO_SUPPORT</span></span> 
  
> <span data-ttu-id="20d8a-139">Объект не может предоставить доступ к этому свойству через интерфейс.</span><span class="sxs-lookup"><span data-stu-id="20d8a-139">The object cannot provide access to this property through the requested interface.</span></span>
    
<span data-ttu-id="20d8a-140">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="20d8a-140">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="20d8a-141">Свойство не существует и MAPI_CREATE не было задано с помощью параметра _ulFlags_ .</span><span class="sxs-lookup"><span data-stu-id="20d8a-141">The requested property does not exist and MAPI_CREATE was not set in the  _ulFlags_ parameter.</span></span> 
    
<span data-ttu-id="20d8a-142">MAPI_E_INVALID_PARAMETER</span><span class="sxs-lookup"><span data-stu-id="20d8a-142">MAPI_E_INVALID_PARAMETER</span></span> 
  
> <span data-ttu-id="20d8a-143">Тип свойства в теге задано значение PT_UNSPECIFIED.</span><span class="sxs-lookup"><span data-stu-id="20d8a-143">The property type in the tag is set to PT_UNSPECIFIED.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="20d8a-144">Замечания</span><span class="sxs-lookup"><span data-stu-id="20d8a-144">Remarks</span></span>

<span data-ttu-id="20d8a-145">Метод **IMAPIProp::OpenProperty** предоставляет доступ к свойству через определенный интерфейс.</span><span class="sxs-lookup"><span data-stu-id="20d8a-145">The **IMAPIProp::OpenProperty** method provides access to a property through a particular interface.</span></span> <span data-ttu-id="20d8a-146">**OpenProperty** является альтернативой методы [IMAPIProp::GetProps](imapiprop-getprops.md) и [IMAPIProp::SetProps](imapiprop-setprops.md) .</span><span class="sxs-lookup"><span data-stu-id="20d8a-146">**OpenProperty** is an alternative to the [IMAPIProp::GetProps](imapiprop-getprops.md) and [IMAPIProp::SetProps](imapiprop-setprops.md) methods.</span></span> <span data-ttu-id="20d8a-147">Когда **GetProps** или **SetProps** не удается выполнить из-за слишком большой или слишком сложный вызов **OpenProperty**свойство.</span><span class="sxs-lookup"><span data-stu-id="20d8a-147">When either **GetProps** or **SetProps** fails because the property is too large or too complex, call **OpenProperty**.</span></span> <span data-ttu-id="20d8a-148">**OpenProperty** обычно используется для доступа к свойствам типа PT_OBJECT.</span><span class="sxs-lookup"><span data-stu-id="20d8a-148">**OpenProperty** is typically used to access properties of type PT_OBJECT.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="20d8a-149">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="20d8a-149">Notes to callers</span></span>

<span data-ttu-id="20d8a-150">Для доступа к вложений сообщений, откройте свойства **PR_ATTACH_DATA_OBJ** ([PidTagAttachDataObject](pidtagattachdataobject-canonical-property.md)) с идентификатором другой интерфейс, в зависимости от типа вложения.</span><span class="sxs-lookup"><span data-stu-id="20d8a-150">To access message attachments, open the **PR_ATTACH_DATA_OBJ** ([PidTagAttachDataObject](pidtagattachdataobject-canonical-property.md)) property with a different interface identifier, depending on the type of attachment.</span></span> <span data-ttu-id="20d8a-151">В следующей таблице описываются вызов **OpenProperty** для разных типов вложений:</span><span class="sxs-lookup"><span data-stu-id="20d8a-151">The following table describes how to call **OpenProperty** for the different types of attachments:</span></span> 
  
|<span data-ttu-id="20d8a-152">**Тип вложения**</span><span class="sxs-lookup"><span data-stu-id="20d8a-152">**Type of attachment**</span></span>|<span data-ttu-id="20d8a-153">**Идентификатор для использования интерфейса**</span><span class="sxs-lookup"><span data-stu-id="20d8a-153">**Interface identifier to use**</span></span>|
|:-----|:-----|
|<span data-ttu-id="20d8a-154">Двоичный</span><span class="sxs-lookup"><span data-stu-id="20d8a-154">Binary</span></span>  <br/> |<span data-ttu-id="20d8a-155">IID_IStream</span><span class="sxs-lookup"><span data-stu-id="20d8a-155">IID_IStream</span></span>  <br/> |
|<span data-ttu-id="20d8a-156">String</span><span class="sxs-lookup"><span data-stu-id="20d8a-156">String</span></span>  <br/> |<span data-ttu-id="20d8a-157">IID_IStream</span><span class="sxs-lookup"><span data-stu-id="20d8a-157">IID_IStream</span></span>  <br/> |
|<span data-ttu-id="20d8a-158">Message</span><span class="sxs-lookup"><span data-stu-id="20d8a-158">Message</span></span>  <br/> |<span data-ttu-id="20d8a-159">IID_IMessage</span><span class="sxs-lookup"><span data-stu-id="20d8a-159">IID_IMessage</span></span>  <br/> |
|<span data-ttu-id="20d8a-160">OLE 2.0 (EN)</span><span class="sxs-lookup"><span data-stu-id="20d8a-160">OLE 2.0</span></span>  <br/> |<span data-ttu-id="20d8a-161">IID_IStreamDocfile</span><span class="sxs-lookup"><span data-stu-id="20d8a-161">IID_IStreamDocfile</span></span>  <br/> |
   
<span data-ttu-id="20d8a-162">**IStreamDocfile** является производным от интерфейса [IStream](http://msdn.microsoft.com/en-us/library/aa380034%28VS.85%29.aspx) , основанный на составным файлом OLE 2.0.</span><span class="sxs-lookup"><span data-stu-id="20d8a-162">**IStreamDocfile** is a derivative of the [IStream](http://msdn.microsoft.com/en-us/library/aa380034%28VS.85%29.aspx) interface that is based on an OLE 2.0 compound file.</span></span> <span data-ttu-id="20d8a-163">**IStreamDocfile** — это лучший вариант для доступа к OLE 2.0 вложения, так как он содержит меньше всего накладные расходы.</span><span class="sxs-lookup"><span data-stu-id="20d8a-163">**IStreamDocfile** is the best choice for accessing OLE 2.0 attachments because it involves the least amount of overhead.</span></span> <span data-ttu-id="20d8a-164">IID_IStreamDocFile можно использовать для свойств, которые содержат данные, хранящиеся в структурированного хранилища, доступные через интерфейс [IStorage](http://msdn.microsoft.com/en-us/library/aa380015%28VS.85%29.aspx) .</span><span class="sxs-lookup"><span data-stu-id="20d8a-164">You can use IID_IStreamDocFile for those properties that contain data stored in structured storage available through the [IStorage](http://msdn.microsoft.com/en-us/library/aa380015%28VS.85%29.aspx) interface.</span></span> 
  
<span data-ttu-id="20d8a-165">Дополнительные сведения об использовании **OpenProperty** с вложениями можно свойство **PR_ATTACH_DATA_OBJ** и [открытие вложений](opening-an-attachment.md).</span><span class="sxs-lookup"><span data-stu-id="20d8a-165">For more information about how to use **OpenProperty** with attachments, see the **PR_ATTACH_DATA_OBJ** property and [Opening an Attachment](opening-an-attachment.md).</span></span>
  
<span data-ttu-id="20d8a-166">Не используйте указатель **IStream** , который вы получаете для вызова метода его [Seek](http://msdn.microsoft.com/en-us/library/aa380043%28v=VS.85%29.aspx) или [SetSize](http://msdn.microsoft.com/en-us/library/aa380044%28v=VS.85%29.aspx) , если вы не используете ноль положение или размер переменной.</span><span class="sxs-lookup"><span data-stu-id="20d8a-166">Do not use the **IStream** pointer that you receive to call either its [Seek](http://msdn.microsoft.com/en-us/library/aa380043%28v=VS.85%29.aspx) or [SetSize](http://msdn.microsoft.com/en-us/library/aa380044%28v=VS.85%29.aspx) method unless you use a zero position or size variable.</span></span> <span data-ttu-id="20d8a-167">Кроме того не полагайтесь на значение параметра _plibNewPosition_ выходные данные, возвращенные вызова **Seek** .</span><span class="sxs-lookup"><span data-stu-id="20d8a-167">Also, do not rely on the value of the  _plibNewPosition_ output parameter returned from the **Seek** call.</span></span> 
  
<span data-ttu-id="20d8a-168">При вызове **OpenProperty** для доступа к свойству с помощью интерфейса **IStream** используйте только этот интерфейс для внесения изменений.</span><span class="sxs-lookup"><span data-stu-id="20d8a-168">If you call **OpenProperty** to access a property with the **IStream** interface, use only that interface to make changes to it.</span></span> <span data-ttu-id="20d8a-169">Не следует обновить свойство с любыми из другой [IMAPIProp: IUnknown](imapipropiunknown.md) методы, такие как **SetProps** или [IMAPIProp::DeleteProps](imapiprop-deleteprops.md).</span><span class="sxs-lookup"><span data-stu-id="20d8a-169">Do not attempt to update the property with any of the other [IMAPIProp : IUnknown](imapipropiunknown.md) methods, such as **SetProps** or [IMAPIProp::DeleteProps](imapiprop-deleteprops.md).</span></span> 
  
<span data-ttu-id="20d8a-170">Не пытайтесь открыть свойство с **OpenProperty** более одного раза.</span><span class="sxs-lookup"><span data-stu-id="20d8a-170">Do not try to open a property with **OpenProperty** more than once.</span></span> <span data-ttu-id="20d8a-171">Результаты, значение undefined, так как они может меняться в зависимости от поставщика для поставщика.</span><span class="sxs-lookup"><span data-stu-id="20d8a-171">The results are undefined because they can vary from provider to provider.</span></span> 
  
<span data-ttu-id="20d8a-172">Если требуется изменить свойства, которое должно быть открыт, необходимо задайте флаг MAPI_MODIFY.</span><span class="sxs-lookup"><span data-stu-id="20d8a-172">If you need to modify the property to be opened, set the MAPI_MODIFY flag.</span></span> <span data-ttu-id="20d8a-173">Если вы не уверены, поддерживает ли объект свойства, но вы думаете, что оно должно, необходимо задайте флаги MAPI_CREATE и MAPI_MODIFY.</span><span class="sxs-lookup"><span data-stu-id="20d8a-173">If you are not sure whether the object supports the property but you think it should, set the MAPI_CREATE and MAPI_MODIFY flags.</span></span> <span data-ttu-id="20d8a-174">При использовании MAPI_CREATE, необходимо также установить MAPI_MODIFY.</span><span class="sxs-lookup"><span data-stu-id="20d8a-174">Whenever MAPI_CREATE is set, MAPI_MODIFY must also be set.</span></span>
  
<span data-ttu-id="20d8a-175">Вы несете ответственность за преобразование указатель интерфейса, возвращаемых в параметре _lppUnk_ , которая подходит для интерфейса, указанного в параметре _lpiid_ .</span><span class="sxs-lookup"><span data-stu-id="20d8a-175">You are responsible for recasting the interface pointer returned in the  _lppUnk_ parameter to one that is appropriate for the interface specified in the  _lpiid_ parameter.</span></span> <span data-ttu-id="20d8a-176">Возвращенный указатель необходимо также использовать для вызова метода [функции IUnknown::Release](http://msdn.microsoft.com/en-us/library/ms682317%28v=VS.85%29.aspx) после завершения с ним.</span><span class="sxs-lookup"><span data-stu-id="20d8a-176">You must also use the returned pointer to call its [IUnknown::Release](http://msdn.microsoft.com/en-us/library/ms682317%28v=VS.85%29.aspx) method when you are finished with it.</span></span> 
  
<span data-ttu-id="20d8a-177">В некоторых случаях установки флагов с помощью параметра _ulFlags_ не достаточно указать тип доступа к свойству, которое является обязательным.</span><span class="sxs-lookup"><span data-stu-id="20d8a-177">Sometimes setting the flags in the  _ulFlags_ parameter is not enough to indicate the type of access to the property that is required.</span></span> <span data-ttu-id="20d8a-178">Дополнительные данные, такие как флаги, можно размещать в параметре _ulInterfaceOptions_ .</span><span class="sxs-lookup"><span data-stu-id="20d8a-178">You can put additional data, such as flags, in the  _ulInterfaceOptions_ parameter.</span></span> <span data-ttu-id="20d8a-179">Эти данные — интерфейс зависимые.</span><span class="sxs-lookup"><span data-stu-id="20d8a-179">This data is interface dependent.</span></span> <span data-ttu-id="20d8a-180">Некоторые интерфейсы (например, **IStream**) используйте его, а некоторые — нет.</span><span class="sxs-lookup"><span data-stu-id="20d8a-180">Some interfaces (such as **IStream**) use it, and others do not.</span></span> <span data-ttu-id="20d8a-181">Например при открытии свойство так, чтобы изменить с помощью **IStream**, задайте флаг STGM_WRITE с помощью параметра _ulInterfaceOptions_ в дополнение к MAPI_MODIFY.</span><span class="sxs-lookup"><span data-stu-id="20d8a-181">For example, when you open a property to be modified with **IStream**, set the STGM_WRITE flag in the  _ulInterfaceOptions_ parameter in addition to MAPI_MODIFY.</span></span> <span data-ttu-id="20d8a-182">При открытии таблицы с помощью интерфейса [IMAPITable](imapitableiunknown.md) можно включить _ulInterfaceOptions_ MAPI_UNICODE, чтобы указать, следует ли столбцы в таблице, в которых содержатся свойства строки в формате Юникод.</span><span class="sxs-lookup"><span data-stu-id="20d8a-182">When you open a table by using the [IMAPITable](imapitableiunknown.md) interface, you can set  _ulInterfaceOptions_ to MAPI_UNICODE to indicate whether the columns in the table that hold string properties should be in Unicode format.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="20d8a-183">Справочник по mfcmapi (en)</span><span class="sxs-lookup"><span data-stu-id="20d8a-183">MFCMAPI reference</span></span>

<span data-ttu-id="20d8a-184">������ ���� mfcmapi (en) ���������� � ������� ����.</span><span class="sxs-lookup"><span data-stu-id="20d8a-184">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="20d8a-185">**����**</span><span class="sxs-lookup"><span data-stu-id="20d8a-185">**File**</span></span>|<span data-ttu-id="20d8a-186">**�������**</span><span class="sxs-lookup"><span data-stu-id="20d8a-186">**Function**</span></span>|<span data-ttu-id="20d8a-187">**�����������**</span><span class="sxs-lookup"><span data-stu-id="20d8a-187">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="20d8a-188">StreamEditor.cpp</span><span class="sxs-lookup"><span data-stu-id="20d8a-188">StreamEditor.cpp</span></span>  <br/> |<span data-ttu-id="20d8a-189">CStreamEditor::ReadTextStreamFromProperty</span><span class="sxs-lookup"><span data-stu-id="20d8a-189">CStreamEditor::ReadTextStreamFromProperty</span></span>  <br/> |<span data-ttu-id="20d8a-190">Mfcmapi (en) используется метод **IMAPIProp::OpenProperty** для получения интерфейс потока для крупных текст и свойства двоичных файлов.</span><span class="sxs-lookup"><span data-stu-id="20d8a-190">MFCMAPI uses the **IMAPIProp::OpenProperty** method to retrieve a stream interface for large text and binary properties.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="20d8a-191">См. также</span><span class="sxs-lookup"><span data-stu-id="20d8a-191">See also</span></span>

- [<span data-ttu-id="20d8a-192">HrIStorageFromStream</span><span class="sxs-lookup"><span data-stu-id="20d8a-192">HrIStorageFromStream</span></span>](hristoragefromstream.md) 
- [<span data-ttu-id="20d8a-193">IMAPIProp::DeleteProps</span><span class="sxs-lookup"><span data-stu-id="20d8a-193">IMAPIProp::DeleteProps</span></span>](imapiprop-deleteprops.md) 
- [<span data-ttu-id="20d8a-194">IMAPIProp::GetProps</span><span class="sxs-lookup"><span data-stu-id="20d8a-194">IMAPIProp::GetProps</span></span>](imapiprop-getprops.md)
- [<span data-ttu-id="20d8a-195">IMAPIProp::SetProps</span><span class="sxs-lookup"><span data-stu-id="20d8a-195">IMAPIProp::SetProps</span></span>](imapiprop-setprops.md)
- [<span data-ttu-id="20d8a-196">IMAPISupport::IStorageFromStream</span><span class="sxs-lookup"><span data-stu-id="20d8a-196">IMAPISupport::IStorageFromStream</span></span>](imapisupport-istoragefromstream.md)
- [<span data-ttu-id="20d8a-197">IMAPITable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="20d8a-197">IMAPITable : IUnknown</span></span>](imapitableiunknown.md)
- [<span data-ttu-id="20d8a-198">IMAPIProp : IUnknown</span><span class="sxs-lookup"><span data-stu-id="20d8a-198">IMAPIProp : IUnknown</span></span>](imapipropiunknown.md)
- [<span data-ttu-id="20d8a-199">Mfcmapi (en) � �������� ������� ����</span><span class="sxs-lookup"><span data-stu-id="20d8a-199">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)
- [<span data-ttu-id="20d8a-200">Открытие вложения</span><span class="sxs-lookup"><span data-stu-id="20d8a-200">Opening an Attachment</span></span>](opening-an-attachment.md)

