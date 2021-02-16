---
title: IMAPIPropDeleteProps
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIProp.DeleteProps
api_type:
- COM
ms.assetid: 5cc642de-21f0-4826-bf21-aac4bcfc1328
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 5bfef87baa2dffa4605f9a7afa3833024f514430
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409239"
---
# <a name="imapipropdeleteprops"></a><span data-ttu-id="9ff78-103">IMAPIProp::DeleteProps</span><span class="sxs-lookup"><span data-stu-id="9ff78-103">IMAPIProp::DeleteProps</span></span>

  
  
<span data-ttu-id="9ff78-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9ff78-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9ff78-105">Удаляет одно или несколько свойств объекта.</span><span class="sxs-lookup"><span data-stu-id="9ff78-105">Deletes one or more properties from an object.</span></span> 
  
```cpp
HRESULT DeleteProps(
  LPSPropTagArray lpPropTagArray,
  LPSPropProblemArray FAR * lppProblems
);
```

## <a name="parameters"></a><span data-ttu-id="9ff78-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="9ff78-106">Parameters</span></span>

 <span data-ttu-id="9ff78-107">_lpPropTagArray_</span><span class="sxs-lookup"><span data-stu-id="9ff78-107">_lpPropTagArray_</span></span>
  
> <span data-ttu-id="9ff78-108">[in] Указатель на массив тегов свойств, которые указывают удаляемые свойства.</span><span class="sxs-lookup"><span data-stu-id="9ff78-108">[in] A pointer to an array of property tags that indicate the properties to delete.</span></span> <span data-ttu-id="9ff78-109">Член **cValues** структуры [SPropTagArray,](sproptagarray.md) на который указывает  _lpPropTagArray,_ не должен быть нулем, а сам параметр  _lpPropTagArray_ не должен иметь значение NULL.</span><span class="sxs-lookup"><span data-stu-id="9ff78-109">The **cValues** member of the [SPropTagArray](sproptagarray.md) structure pointed to by  _lpPropTagArray_ must not be zero, and the  _lpPropTagArray_ parameter itself must not be NULL.</span></span> 
    
 <span data-ttu-id="9ff78-110">_lppProblems_</span><span class="sxs-lookup"><span data-stu-id="9ff78-110">_lppProblems_</span></span>
  
> <span data-ttu-id="9ff78-111">[in, out] При вводе указатель на указатель на [структуру SPropProblemArray;](spropproblemarray.md) в противном случае — NULL, что указывает на отсутствие необходимости в сведениях об ошибках.</span><span class="sxs-lookup"><span data-stu-id="9ff78-111">[in, out] On input, a pointer to a pointer to an [SPropProblemArray](spropproblemarray.md) structure; otherwise, NULL, which indicates that there is no need for error information.</span></span> <span data-ttu-id="9ff78-112">Если  _lppProblems_ является допустимым указателем при вводе, **DeleteProps** возвращает подробные сведения об ошибках при удалении одного или более свойств.</span><span class="sxs-lookup"><span data-stu-id="9ff78-112">If  _lppProblems_ is a valid pointer on input, **DeleteProps** returns detailed information about errors in deleting one or more properties.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="9ff78-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="9ff78-113">Return value</span></span>

<span data-ttu-id="9ff78-114">S_OK</span><span class="sxs-lookup"><span data-stu-id="9ff78-114">S_OK</span></span> 
  
> <span data-ttu-id="9ff78-115">Свойства были успешно удалены.</span><span class="sxs-lookup"><span data-stu-id="9ff78-115">Properties were successfully deleted.</span></span>
    
<span data-ttu-id="9ff78-116">MAPI_E_NO_ACCESS</span><span class="sxs-lookup"><span data-stu-id="9ff78-116">MAPI_E_NO_ACCESS</span></span> 
  
> <span data-ttu-id="9ff78-117">У вызываемого объекта недостаточно разрешений на удаление свойств.</span><span class="sxs-lookup"><span data-stu-id="9ff78-117">The caller has insufficient permissions to delete properties.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="9ff78-118">Примечания</span><span class="sxs-lookup"><span data-stu-id="9ff78-118">Remarks</span></span>

<span data-ttu-id="9ff78-119">Метод **IMAPIProp::D eleteProps** удаляет одно или несколько свойств из текущего объекта.</span><span class="sxs-lookup"><span data-stu-id="9ff78-119">The **IMAPIProp::DeleteProps** method removes one or more properties from the current object.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="9ff78-120">Примечания для исполнителей</span><span class="sxs-lookup"><span data-stu-id="9ff78-120">Notes to implementers</span></span>

<span data-ttu-id="9ff78-121">Удалять свойства из всех объектов не нужно.</span><span class="sxs-lookup"><span data-stu-id="9ff78-121">You do not have to allow properties to be deleted from all objects.</span></span> <span data-ttu-id="9ff78-122">Если объект не может быть модификабельным, MAPI_E_NO_ACCESS из **метода DeleteProps.**</span><span class="sxs-lookup"><span data-stu-id="9ff78-122">If the object is not modifiable, return MAPI_E_NO_ACCESS from the **DeleteProps** method.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="9ff78-123">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="9ff78-123">Notes to callers</span></span>

<span data-ttu-id="9ff78-124">Не нужно устанавливать тип свойства для каждого тега свойства в массиве тегов свойств, на который указывает параметр _lpPropTagArray._</span><span class="sxs-lookup"><span data-stu-id="9ff78-124">You do not have to set the property type for each property tag in the property tag array pointed to by the  _lpPropTagArray_ parameter.</span></span> <span data-ttu-id="9ff78-125">Типы свойств игнорируются; используются только идентификаторы свойств.</span><span class="sxs-lookup"><span data-stu-id="9ff78-125">Property types are ignored; only the property identifiers are used.</span></span> 
  
<span data-ttu-id="9ff78-126">Следует помнить, что некоторые объекты не позволяют вносить изменения и MAPI_E_NO_ACCESS из метода **DeleteProps.**</span><span class="sxs-lookup"><span data-stu-id="9ff78-126">Be aware that some objects do not allow modification and that these objects return MAPI_E_NO_ACCESS from the **DeleteProps** method.</span></span> <span data-ttu-id="9ff78-127">Другие объекты позволяют удалять некоторые свойства, но не другие.</span><span class="sxs-lookup"><span data-stu-id="9ff78-127">Other objects allow some properties to be deleted, but not others.</span></span> <span data-ttu-id="9ff78-128">Если возникает проблема с удалением только некоторых свойств, **DeleteProps** возвращает S_OK.</span><span class="sxs-lookup"><span data-stu-id="9ff78-128">When there is a problem deleting only some of the properties, **DeleteProps** returns S_OK.</span></span> <span data-ttu-id="9ff78-129">Если вы передали допустимый указатель в  _параметре lppProblems,_ **DeleteProps** настроит указатель на структуру **SPropProblemArray,** которая содержит подробные сведения о проблемах с каждым свойством.</span><span class="sxs-lookup"><span data-stu-id="9ff78-129">If you have passed a valid pointer in the  _lppProblems_ parameter, **DeleteProps** will set the pointer to an **SPropProblemArray** structure that contains detailed information about the problems with each property.</span></span> <span data-ttu-id="9ff78-130">Например, если удалить все свойства сообщения и возникла проблема с одним или более его вложениями, структура **SPropProblemArray** будет содержать запись для свойства **PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments).](pidtagmessageattachments-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="9ff78-130">For example, if you are deleting all of the properties of a message and there is a problem with one or more of its attachments, the **SPropProblemArray** structure will contain an entry for the **PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md)) property.</span></span> 
  
<span data-ttu-id="9ff78-131">Структура, на которая указывает  _lppProblems,_ действительна, только если **DeleteProps** возвращает S_OK.</span><span class="sxs-lookup"><span data-stu-id="9ff78-131">The structure pointed to by  _lppProblems_ is only valid if **DeleteProps** returns S_OK.</span></span> <span data-ttu-id="9ff78-132">Если **DeleteProps** возвращает ошибку, не пытайтесь использовать **структуру SPropProblemArray.**</span><span class="sxs-lookup"><span data-stu-id="9ff78-132">If **DeleteProps** returns an error, do not attempt to use the **SPropProblemArray** structure.</span></span> <span data-ttu-id="9ff78-133">Вместо этого вызовите метод [IMAPIProp::GetLastError](imapiprop-getlasterror.md) объекта, чтобы получить дополнительные сведения об ошибке.</span><span class="sxs-lookup"><span data-stu-id="9ff78-133">Instead, call the object's [IMAPIProp::GetLastError](imapiprop-getlasterror.md) method to obtain more information about the error.</span></span> 
  
<span data-ttu-id="9ff78-134">Освободите возвращенную **структуру SPropProblemArray,** вызывая [функцию MAPIFreeBuffer.](mapifreebuffer.md)</span><span class="sxs-lookup"><span data-stu-id="9ff78-134">Free the returned **SPropProblemArray** structure by calling the [MAPIFreeBuffer](mapifreebuffer.md) function.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="9ff78-135">Справочные материалы по MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="9ff78-135">MFCMAPI reference</span></span>

<span data-ttu-id="9ff78-136">Пример кода MFCMAPI указан в приведенной ниже таблице.</span><span class="sxs-lookup"><span data-stu-id="9ff78-136">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="9ff78-137">**Файл**</span><span class="sxs-lookup"><span data-stu-id="9ff78-137">**File**</span></span>|<span data-ttu-id="9ff78-138">**Функция**</span><span class="sxs-lookup"><span data-stu-id="9ff78-138">**Function**</span></span>|<span data-ttu-id="9ff78-139">**Примечание**</span><span class="sxs-lookup"><span data-stu-id="9ff78-139">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="9ff78-140">MAPIFunctions.cpp</span><span class="sxs-lookup"><span data-stu-id="9ff78-140">MAPIFunctions.cpp</span></span>  <br/> |<span data-ttu-id="9ff78-141">DeleteProperty</span><span class="sxs-lookup"><span data-stu-id="9ff78-141">DeleteProperty</span></span>  <br/> |<span data-ttu-id="9ff78-142">MFCMAPI использует метод **IMAPIProp::D eleteProps** для удаления свойства из объекта.</span><span class="sxs-lookup"><span data-stu-id="9ff78-142">MFCMAPI uses the **IMAPIProp::DeleteProps** method to delete a property from an object.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="9ff78-143">См. также</span><span class="sxs-lookup"><span data-stu-id="9ff78-143">See also</span></span>



[<span data-ttu-id="9ff78-144">IMAPIProp::GetLastError</span><span class="sxs-lookup"><span data-stu-id="9ff78-144">IMAPIProp::GetLastError</span></span>](imapiprop-getlasterror.md)
  
[<span data-ttu-id="9ff78-145">IMAPIProp::GetProps</span><span class="sxs-lookup"><span data-stu-id="9ff78-145">IMAPIProp::GetProps</span></span>](imapiprop-getprops.md)
  
[<span data-ttu-id="9ff78-146">IMAPIProp::SaveChanges</span><span class="sxs-lookup"><span data-stu-id="9ff78-146">IMAPIProp::SaveChanges</span></span>](imapiprop-savechanges.md)
  
[<span data-ttu-id="9ff78-147">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="9ff78-147">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="9ff78-148">SPropProblemArray</span><span class="sxs-lookup"><span data-stu-id="9ff78-148">SPropProblemArray</span></span>](spropproblemarray.md)
  
[<span data-ttu-id="9ff78-149">SPropTagArray</span><span class="sxs-lookup"><span data-stu-id="9ff78-149">SPropTagArray</span></span>](sproptagarray.md)
  
[<span data-ttu-id="9ff78-150">IMAPIProp : IUnknown</span><span class="sxs-lookup"><span data-stu-id="9ff78-150">IMAPIProp : IUnknown</span></span>](imapipropiunknown.md)


[<span data-ttu-id="9ff78-151">Mfcmapi (en) � �������� ������� ����</span><span class="sxs-lookup"><span data-stu-id="9ff78-151">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

