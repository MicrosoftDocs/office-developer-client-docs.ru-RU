---
title: Имапипропсетпропс
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIProp.SetProps
api_type:
- COM
ms.assetid: 49f007c9-42e5-4391-8b83-988c9b0ebdba
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 87709f8a77471637d7652982669bcba93ca2e1dd
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412620"
---
# <a name="imapipropsetprops"></a><span data-ttu-id="9bce1-103">IMAPIProp::SetProps</span><span class="sxs-lookup"><span data-stu-id="9bce1-103">IMAPIProp::SetProps</span></span>

  
  
<span data-ttu-id="9bce1-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9bce1-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9bce1-105">Обновляет одно или несколько свойств.</span><span class="sxs-lookup"><span data-stu-id="9bce1-105">Updates one or more properties.</span></span>
  
```cpp
HRESULT SetProps(
  ULONG cValues,
  LPSPropValue lpPropArray,
  LPSPropProblemArray FAR * lppProblems
);
```

## <a name="parameters"></a><span data-ttu-id="9bce1-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="9bce1-106">Parameters</span></span>

 <span data-ttu-id="9bce1-107">_Квалуес_</span><span class="sxs-lookup"><span data-stu-id="9bce1-107">_cValues_</span></span>
  
> <span data-ttu-id="9bce1-108">возврата Количество значений свойств, на которые указывает параметр _лппропаррай_ .</span><span class="sxs-lookup"><span data-stu-id="9bce1-108">[in] The count of property values pointed to by the  _lpPropArray_ parameter.</span></span> <span data-ttu-id="9bce1-109">Значение параметра _квалуес_ не должно быть равно 0.</span><span class="sxs-lookup"><span data-stu-id="9bce1-109">The  _cValues_ parameter must not be 0.</span></span> 
    
 <span data-ttu-id="9bce1-110">_Лппропаррай_</span><span class="sxs-lookup"><span data-stu-id="9bce1-110">_lpPropArray_</span></span>
  
> <span data-ttu-id="9bce1-111">возврата Указатель на массив структур [спропвалуе](spropvalue.md) , содержащих значения свойств, которые необходимо обновить.</span><span class="sxs-lookup"><span data-stu-id="9bce1-111">[in] A pointer to an array of [SPropValue](spropvalue.md) structures that contain property values to be updated.</span></span> 
    
 <span data-ttu-id="9bce1-112">_Лпппроблемс_</span><span class="sxs-lookup"><span data-stu-id="9bce1-112">_lppProblems_</span></span>
  
> <span data-ttu-id="9bce1-113">[вход, выход] На входе указатель на указатель на структуру [спроппроблемаррай](spropproblemarray.md) ; в противном случае — значение NULL, которое указывает на отсутствие необходимости в сведениях об ошибке.</span><span class="sxs-lookup"><span data-stu-id="9bce1-113">[in, out] On input, a pointer to a pointer to an [SPropProblemArray](spropproblemarray.md) structure; otherwise, NULL, indicating no need for error information.</span></span> <span data-ttu-id="9bce1-114">Если _лпппроблемс_ является допустимым указателем на входе, **SetProps** возвращает подробные сведения об ошибках при обновлении одного или нескольких свойств.</span><span class="sxs-lookup"><span data-stu-id="9bce1-114">If  _lppProblems_ is a valid pointer on input, **SetProps** returns detailed information about errors in updating one or more properties.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="9bce1-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="9bce1-115">Return value</span></span>

<span data-ttu-id="9bce1-116">S_OK</span><span class="sxs-lookup"><span data-stu-id="9bce1-116">S_OK</span></span> 
  
> <span data-ttu-id="9bce1-117">Свойства успешно обновлены.</span><span class="sxs-lookup"><span data-stu-id="9bce1-117">The properties were successfully updated.</span></span>
    
<span data-ttu-id="9bce1-118">Следующие значения могут возвращаться в структуре **спроппроблемаррай** , но не в качестве возвращаемых значений для **SetProps**:</span><span class="sxs-lookup"><span data-stu-id="9bce1-118">The following values can be returned in the **SPropProblemArray** structure, but not as return values for **SetProps**:</span></span>
  
<span data-ttu-id="9bce1-119">МАПИ_Е_БАД_ЧАРВИДС</span><span class="sxs-lookup"><span data-stu-id="9bce1-119">MAPI_E_BAD_CHARWIDTH</span></span> 
  
> <span data-ttu-id="9bce1-120">Установлен либо флаг МАПИ_УНИКОДЕ, либо реализация не поддерживает Юникод, или МАПИ_УНИКОДЕ не задано, а реализация поддерживает только Юникод.</span><span class="sxs-lookup"><span data-stu-id="9bce1-120">Either the MAPI_UNICODE flag was set and the implementation does not support Unicode, or MAPI_UNICODE was not set and the implementation supports only Unicode.</span></span>
    
<span data-ttu-id="9bce1-121">МАПИ_Е_КОМПУТЕД</span><span class="sxs-lookup"><span data-stu-id="9bce1-121">MAPI_E_COMPUTED</span></span> 
  
> <span data-ttu-id="9bce1-122">Свойство не может быть Обновлено, так как оно доступно только для чтения, которое вычисляется поставщиком службы, который отвечает за объект.</span><span class="sxs-lookup"><span data-stu-id="9bce1-122">The property cannot be updated because it is read-only, computed by the service provider that is responsible for the object.</span></span>
    
<span data-ttu-id="9bce1-123">МАПИ_Е_ИНВАЛИД_ТИПЕ</span><span class="sxs-lookup"><span data-stu-id="9bce1-123">MAPI_E_INVALID_TYPE</span></span> 
  
> <span data-ttu-id="9bce1-124">Недопустимый тип свойства.</span><span class="sxs-lookup"><span data-stu-id="9bce1-124">The property type is invalid.</span></span>
    
<span data-ttu-id="9bce1-125">МАПИ_Е_НО_АКЦЕСС</span><span class="sxs-lookup"><span data-stu-id="9bce1-125">MAPI_E_NO_ACCESS</span></span> 
  
> <span data-ttu-id="9bce1-126">Предпринята попытка изменить объект, предназначенный только для чтения, или доступ к объекту, для которого у пользователя недостаточно разрешений.</span><span class="sxs-lookup"><span data-stu-id="9bce1-126">An attempt was made to modify a read-only object or to access an object for which the user has insufficient permissions.</span></span>
    
<span data-ttu-id="9bce1-127">МАПИ_Е_НОТ_ЕНАУГХ_МЕМОРИ</span><span class="sxs-lookup"><span data-stu-id="9bce1-127">MAPI_E_NOT_ENOUGH_MEMORY</span></span> 
  
> <span data-ttu-id="9bce1-128">Свойство не может быть Обновлено, так как оно больше размера буфера удаленного вызова процедур (RPC).</span><span class="sxs-lookup"><span data-stu-id="9bce1-128">The property cannot be updated because it is larger than the remote procedure call (RPC) buffer size.</span></span>
    
<span data-ttu-id="9bce1-129">МАПИ_Е_УНЕКСПЕКТЕД_ТИПЕ</span><span class="sxs-lookup"><span data-stu-id="9bce1-129">MAPI_E_UNEXPECTED_TYPE</span></span> 
  
> <span data-ttu-id="9bce1-130">Тип свойства не является типом, ожидаемым реализацией вызова.</span><span class="sxs-lookup"><span data-stu-id="9bce1-130">The property type is not the type expected by the calling implementation.</span></span>
    
## <a name="notes-to-implementers"></a><span data-ttu-id="9bce1-131">Примечания для исполнителей</span><span class="sxs-lookup"><span data-stu-id="9bce1-131">Notes to implementers</span></span>

<span data-ttu-id="9bce1-132">Игнорировать тег свойства **пр_нулл** ([PidTagNull](pidtagnull-canonical-property.md)) и все свойства с типом **пт_еррор**.</span><span class="sxs-lookup"><span data-stu-id="9bce1-132">Ignore the **PR_NULL** ([PidTagNull](pidtagnull-canonical-property.md)) property tag and all properties with a type of **PT_ERROR**.</span></span> <span data-ttu-id="9bce1-133">Не вносите изменения или сообщайте о проблемах в структуре **спроппроблемаррай** .</span><span class="sxs-lookup"><span data-stu-id="9bce1-133">Do not make changes or report problems in the **SPropProblemArray** structure.</span></span> 
  
<span data-ttu-id="9bce1-134">Возвращает МАПИ_Е_ИНВАЛИД_ПАРАМЕТЕР, если свойство типа \*\*пт_обжект\*\* включено в массив значений свойства.</span><span class="sxs-lookup"><span data-stu-id="9bce1-134">Return MAPI_E_INVALID_PARAMETER if a property of type **PT_OBJECT** is included in the property value array.</span></span> <span data-ttu-id="9bce1-135">Также возвращайте эту ошибку, если в массив включено свойство с несколькими значениями, а его элемент **квалуес** имеет значение 0.</span><span class="sxs-lookup"><span data-stu-id="9bce1-135">Also return this error if a multiple-value property is included in the array and its **cValues** member is set to 0.</span></span> 
  
<span data-ttu-id="9bce1-136">Если вызов выполнен в целом, но возникли проблемы с настройкой некоторых свойств, возвращайте значение S_OK и поместите сведения о проблемах в соответствующую запись структуры **спроппроблемаррай** , на которую указывает параметр _лпппроблемс_ .</span><span class="sxs-lookup"><span data-stu-id="9bce1-136">If the call succeeds overall but there are problems with setting some of the properties, return S_OK and put information about the problems in the appropriate entry of the **SPropProblemArray** structure that the  _lppProblems_ parameter points to.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="9bce1-137">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="9bce1-137">Notes to callers</span></span>

<span data-ttu-id="9bce1-138">В зависимости от поставщика услуг Вы также можете изменить тип свойства, передав тег свойства, который содержит другой тип, чем ранее использовался с заданным идентификатором свойства.</span><span class="sxs-lookup"><span data-stu-id="9bce1-138">Depending on the service provider, you might also be able to change the property type by passing a property tag that contains a different type than was previously used with a given property identifier.</span></span>
  
<span data-ttu-id="9bce1-139">Если вы включили тег свойства для свойства, которое не поддерживается объектом, а реализация **SetProps** позволяет создавать новые свойства, свойство добавляется в объект.</span><span class="sxs-lookup"><span data-stu-id="9bce1-139">If you include a property tag for a property that is unsupported by the object and the implementation of **SetProps** allows the creation of new properties, the property is added to the object.</span></span> <span data-ttu-id="9bce1-140">Все предыдущие значения, хранящиеся в идентификаторе свойства, использованном для нового свойства, отбрасываются.</span><span class="sxs-lookup"><span data-stu-id="9bce1-140">Any previous value stored with the property identifier that was used for the new property is discarded.</span></span> 
  
<span data-ttu-id="9bce1-141">Обратите внимание, что возвращаемое значение S_OK не гарантирует, что все свойства были успешно обновлены.</span><span class="sxs-lookup"><span data-stu-id="9bce1-141">Note that the S_OK return value does not guarantee that all of the properties were successfully updated.</span></span> <span data-ttu-id="9bce1-142">Некоторые поставщики кэшируют вызовы **SetProps** до тех пор, пока не будут получены вызовы, требующие вмешательства поставщика, такие как [IMAPIProp:: SaveChanges](imapiprop-savechanges.md) или [IMAPIProp:: PROPS](imapiprop-getprops.md).</span><span class="sxs-lookup"><span data-stu-id="9bce1-142">Some providers cache **SetProps** calls until they receive a call that requires provider intervention, such as [IMAPIProp::SaveChanges](imapiprop-savechanges.md) or [IMAPIProp::GetProps](imapiprop-getprops.md).</span></span> <span data-ttu-id="9bce1-143">Таким образом, можно получить значения ошибок, которые относятся к вызову **SetProps** с помощью последующих вызовов.</span><span class="sxs-lookup"><span data-stu-id="9bce1-143">Therefore, it is possible to receive error values that relate to the **SetProps** call with the later calls.</span></span> 
  
<span data-ttu-id="9bce1-144">Если **SetProps** ВОЗВРАЩАЕТ значение S_OK, проверьте структуру **спроппроблемаррай** , на которую указывает _лпппроблемс_ , для проблем, связанных с обновлением отдельных свойств.</span><span class="sxs-lookup"><span data-stu-id="9bce1-144">If **SetProps** returns S_OK, check the **SPropProblemArray** structure pointed to by  _lppProblems_ for problems updating individual properties.</span></span> <span data-ttu-id="9bce1-145">Если **SetProps** возвращает ошибку, не проверяйте массив проблем свойств.</span><span class="sxs-lookup"><span data-stu-id="9bce1-145">If **SetProps** returns an error, do not check the property problem array.</span></span> <span data-ttu-id="9bce1-146">Вместо этого вызовите метод объекта [IMAPIProp:: GetLastError](imapiprop-getlasterror.md) .</span><span class="sxs-lookup"><span data-stu-id="9bce1-146">Instead, call the object's [IMAPIProp::GetLastError](imapiprop-getlasterror.md) method.</span></span> 
  
<span data-ttu-id="9bce1-147">При обновлении больших свойств **SetProps** может не работать и возвращать мапи_е_нот_енаугх_мемори.</span><span class="sxs-lookup"><span data-stu-id="9bce1-147">When updating large properties, **SetProps** can fail and return MAPI_E_NOT_ENOUGH_MEMORY.</span></span> <span data-ttu-id="9bce1-148">Максимальный размер свойств не задан, а различные объекты могут иметь разные ограничения.</span><span class="sxs-lookup"><span data-stu-id="9bce1-148">There is no maximum size for properties, and different objects can have different limits.</span></span> <span data-ttu-id="9bce1-149">Если вы обрабатываете потенциально большие свойства, будьте готовы вызвать метод [IMAPIProp:: опенпроперти](imapiprop-openproperty.md) с иид_истреам в качестве идентификатора интерфейса, если **SetProps** возвращает данное значение ошибки.</span><span class="sxs-lookup"><span data-stu-id="9bce1-149">If you deal with potentially large properties, be prepared to call the [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method with IID_IStream as the interface identifier if **SetProps** returns this error value.</span></span> 
  
<span data-ttu-id="9bce1-150">ВыЗовите функцию [мапифрибуффер](mapifreebuffer.md) , чтобы освободить структуру **спроппроблемаррай** .</span><span class="sxs-lookup"><span data-stu-id="9bce1-150">Call the [MAPIFreeBuffer](mapifreebuffer.md) function to free the **SPropProblemArray** structure.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="9bce1-151">Справочные материалы по MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="9bce1-151">MFCMAPI reference</span></span>

<span data-ttu-id="9bce1-152">Пример кода MFCMAPI указан в приведенной ниже таблице.</span><span class="sxs-lookup"><span data-stu-id="9bce1-152">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="9bce1-153">**Файл**</span><span class="sxs-lookup"><span data-stu-id="9bce1-153">**File**</span></span>|<span data-ttu-id="9bce1-154">**Функция**</span><span class="sxs-lookup"><span data-stu-id="9bce1-154">**Function**</span></span>|<span data-ttu-id="9bce1-155">**Примечание**</span><span class="sxs-lookup"><span data-stu-id="9bce1-155">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="9bce1-156">Редакторсвойств. cpp</span><span class="sxs-lookup"><span data-stu-id="9bce1-156">PropertyEditor.cpp</span></span>  <br/> |<span data-ttu-id="9bce1-157">Кпропертедитор:: Вритеспропвалуетубжект</span><span class="sxs-lookup"><span data-stu-id="9bce1-157">CPropertyEditor::WriteSPropValueToObject</span></span>  <br/> |<span data-ttu-id="9bce1-158">MFCMAPI использует метод **IMAPIProp:: SetProps** для записи свойства обратно в объект после того, как свойство было изменено.</span><span class="sxs-lookup"><span data-stu-id="9bce1-158">MFCMAPI uses the **IMAPIProp::SetProps** method to write a property back to an object after the property has been edited.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="9bce1-159">См. также</span><span class="sxs-lookup"><span data-stu-id="9bce1-159">See also</span></span>



[<span data-ttu-id="9bce1-160">IMAPIProp::GetLastError</span><span class="sxs-lookup"><span data-stu-id="9bce1-160">IMAPIProp::GetLastError</span></span>](imapiprop-getlasterror.md)
  
[<span data-ttu-id="9bce1-161">IMAPIProp::GetProps</span><span class="sxs-lookup"><span data-stu-id="9bce1-161">IMAPIProp::GetProps</span></span>](imapiprop-getprops.md)
  
[<span data-ttu-id="9bce1-162">IMAPIProp::OpenProperty</span><span class="sxs-lookup"><span data-stu-id="9bce1-162">IMAPIProp::OpenProperty</span></span>](imapiprop-openproperty.md)
  
[<span data-ttu-id="9bce1-163">IMAPIProp::SaveChanges</span><span class="sxs-lookup"><span data-stu-id="9bce1-163">IMAPIProp::SaveChanges</span></span>](imapiprop-savechanges.md)
  
[<span data-ttu-id="9bce1-164">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="9bce1-164">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="9bce1-165">SPropProblemArray</span><span class="sxs-lookup"><span data-stu-id="9bce1-165">SPropProblemArray</span></span>](spropproblemarray.md)
  
[<span data-ttu-id="9bce1-166">SPropValue</span><span class="sxs-lookup"><span data-stu-id="9bce1-166">SPropValue</span></span>](spropvalue.md)
  
[<span data-ttu-id="9bce1-167">IMAPIProp : IUnknown</span><span class="sxs-lookup"><span data-stu-id="9bce1-167">IMAPIProp : IUnknown</span></span>](imapipropiunknown.md)

