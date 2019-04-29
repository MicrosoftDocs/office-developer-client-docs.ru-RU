---
title: Имапипропделетепропс
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
# <a name="imapipropdeleteprops"></a><span data-ttu-id="888e6-103">IMAPIProp::DeleteProps</span><span class="sxs-lookup"><span data-stu-id="888e6-103">IMAPIProp::DeleteProps</span></span>

  
  
<span data-ttu-id="888e6-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="888e6-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="888e6-105">Удаляет одно или несколько свойств объекта.</span><span class="sxs-lookup"><span data-stu-id="888e6-105">Deletes one or more properties from an object.</span></span> 
  
```cpp
HRESULT DeleteProps(
  LPSPropTagArray lpPropTagArray,
  LPSPropProblemArray FAR * lppProblems
);
```

## <a name="parameters"></a><span data-ttu-id="888e6-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="888e6-106">Parameters</span></span>

 <span data-ttu-id="888e6-107">_Лппроптагаррай_</span><span class="sxs-lookup"><span data-stu-id="888e6-107">_lpPropTagArray_</span></span>
  
> <span data-ttu-id="888e6-108">возврата Указатель на массив тегов свойств, указывающий свойства, которые требуется удалить.</span><span class="sxs-lookup"><span data-stu-id="888e6-108">[in] A pointer to an array of property tags that indicate the properties to delete.</span></span> <span data-ttu-id="888e6-109">Элемент **квалуес** структуры [спроптагаррай](sproptagarray.md) , на который указывает _лппроптагаррай_ , не должен иметь значение 0, а сам параметр _лппроптагаррай_ не должен иметь значение null.</span><span class="sxs-lookup"><span data-stu-id="888e6-109">The **cValues** member of the [SPropTagArray](sproptagarray.md) structure pointed to by  _lpPropTagArray_ must not be zero, and the  _lpPropTagArray_ parameter itself must not be NULL.</span></span> 
    
 <span data-ttu-id="888e6-110">_Лпппроблемс_</span><span class="sxs-lookup"><span data-stu-id="888e6-110">_lppProblems_</span></span>
  
> <span data-ttu-id="888e6-111">[вход, выход] На входе указатель на указатель на структуру [спроппроблемаррай](spropproblemarray.md) ; в противном случае — значение NULL, которое указывает, что нет необходимости в сведениях об ошибке.</span><span class="sxs-lookup"><span data-stu-id="888e6-111">[in, out] On input, a pointer to a pointer to an [SPropProblemArray](spropproblemarray.md) structure; otherwise, NULL, which indicates that there is no need for error information.</span></span> <span data-ttu-id="888e6-112">Если _лпппроблемс_ является допустимым указателем на входе, **делетепропс** возвращает подробные сведения об ошибках при удалении одного или нескольких свойств.</span><span class="sxs-lookup"><span data-stu-id="888e6-112">If  _lppProblems_ is a valid pointer on input, **DeleteProps** returns detailed information about errors in deleting one or more properties.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="888e6-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="888e6-113">Return value</span></span>

<span data-ttu-id="888e6-114">S_OK</span><span class="sxs-lookup"><span data-stu-id="888e6-114">S_OK</span></span> 
  
> <span data-ttu-id="888e6-115">Свойства были успешно удалены.</span><span class="sxs-lookup"><span data-stu-id="888e6-115">Properties were successfully deleted.</span></span>
    
<span data-ttu-id="888e6-116">МАПИ_Е_НО_АКЦЕСС</span><span class="sxs-lookup"><span data-stu-id="888e6-116">MAPI_E_NO_ACCESS</span></span> 
  
> <span data-ttu-id="888e6-117">Вызывающий не имеет достаточных разрешений на удаление свойств.</span><span class="sxs-lookup"><span data-stu-id="888e6-117">The caller has insufficient permissions to delete properties.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="888e6-118">Примечания</span><span class="sxs-lookup"><span data-stu-id="888e6-118">Remarks</span></span>

<span data-ttu-id="888e6-119">Метод **IMAPIProp::D елетепропс** удаляет одно или несколько свойств из текущего объекта.</span><span class="sxs-lookup"><span data-stu-id="888e6-119">The **IMAPIProp::DeleteProps** method removes one or more properties from the current object.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="888e6-120">Примечания для исполнителей</span><span class="sxs-lookup"><span data-stu-id="888e6-120">Notes to implementers</span></span>

<span data-ttu-id="888e6-121">Не нужно разрешать удаление свойств из всех объектов.</span><span class="sxs-lookup"><span data-stu-id="888e6-121">You do not have to allow properties to be deleted from all objects.</span></span> <span data-ttu-id="888e6-122">Если объект не является изменяемым, возвращайте МАПИ_Е_НО_АКЦЕСС из метода **делетепропс** .</span><span class="sxs-lookup"><span data-stu-id="888e6-122">If the object is not modifiable, return MAPI_E_NO_ACCESS from the **DeleteProps** method.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="888e6-123">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="888e6-123">Notes to callers</span></span>

<span data-ttu-id="888e6-124">Нет необходимости задавать тип свойства для каждого тега свойства в массиве тегов свойств, на который указывает параметр _лппроптагаррай_ .</span><span class="sxs-lookup"><span data-stu-id="888e6-124">You do not have to set the property type for each property tag in the property tag array pointed to by the  _lpPropTagArray_ parameter.</span></span> <span data-ttu-id="888e6-125">Типы свойств игнорируются; используются только идентификаторы свойств.</span><span class="sxs-lookup"><span data-stu-id="888e6-125">Property types are ignored; only the property identifiers are used.</span></span> 
  
<span data-ttu-id="888e6-126">Обратите внимание, что некоторые объекты не допускают изменения и что эти объекты возвращают МАПИ_Е_НО_АКЦЕСС из метода **делетепропс** .</span><span class="sxs-lookup"><span data-stu-id="888e6-126">Be aware that some objects do not allow modification and that these objects return MAPI_E_NO_ACCESS from the **DeleteProps** method.</span></span> <span data-ttu-id="888e6-127">Другие объекты позволяют удалять некоторые свойства, но не другие.</span><span class="sxs-lookup"><span data-stu-id="888e6-127">Other objects allow some properties to be deleted, but not others.</span></span> <span data-ttu-id="888e6-128">При возникновении проблем с удалением только некоторых свойств **делетепропс** ВОЗВРАЩАЕТ значение S_OK.</span><span class="sxs-lookup"><span data-stu-id="888e6-128">When there is a problem deleting only some of the properties, **DeleteProps** returns S_OK.</span></span> <span data-ttu-id="888e6-129">Если вы передали допустимый указатель в параметре _лпппроблемс_ , **делетепропс** установит указатель на структуру **спроппроблемаррай** , содержащую подробные сведения о проблемах с каждым свойством.</span><span class="sxs-lookup"><span data-stu-id="888e6-129">If you have passed a valid pointer in the  _lppProblems_ parameter, **DeleteProps** will set the pointer to an **SPropProblemArray** structure that contains detailed information about the problems with each property.</span></span> <span data-ttu-id="888e6-130">Например, если удаляются все свойства сообщения и возникла проблема с одним или несколькими вложениями, структура **спроппроблемаррай** будет содержать запись для **пр_мессаже_аттачментс** ([PidTagMessageAttachments ](pidtagmessageattachments-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="888e6-130">For example, if you are deleting all of the properties of a message and there is a problem with one or more of its attachments, the **SPropProblemArray** structure will contain an entry for the **PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md)) property.</span></span> 
  
<span data-ttu-id="888e6-131">Структура, на которую указывает _лпппроблемс_ , допустима только в том случае, если **ДЕЛЕТЕПРОПС** возвращает значение S_OK.</span><span class="sxs-lookup"><span data-stu-id="888e6-131">The structure pointed to by  _lppProblems_ is only valid if **DeleteProps** returns S_OK.</span></span> <span data-ttu-id="888e6-132">Если **делетепропс** возвращает ошибку, не пытайтесь использовать структуру **спроппроблемаррай** .</span><span class="sxs-lookup"><span data-stu-id="888e6-132">If **DeleteProps** returns an error, do not attempt to use the **SPropProblemArray** structure.</span></span> <span data-ttu-id="888e6-133">Вместо этого вызовите метод объекта [IMAPIProp:: GetLastError](imapiprop-getlasterror.md) , чтобы получить дополнительные сведения об ошибке.</span><span class="sxs-lookup"><span data-stu-id="888e6-133">Instead, call the object's [IMAPIProp::GetLastError](imapiprop-getlasterror.md) method to obtain more information about the error.</span></span> 
  
<span data-ttu-id="888e6-134">Освободите возвращаемую структуру **спроппроблемаррай** , вызвав функцию [мапифрибуффер](mapifreebuffer.md) .</span><span class="sxs-lookup"><span data-stu-id="888e6-134">Free the returned **SPropProblemArray** structure by calling the [MAPIFreeBuffer](mapifreebuffer.md) function.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="888e6-135">Справочные материалы по MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="888e6-135">MFCMAPI reference</span></span>

<span data-ttu-id="888e6-136">Пример кода MFCMAPI указан в приведенной ниже таблице.</span><span class="sxs-lookup"><span data-stu-id="888e6-136">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="888e6-137">**Файл**</span><span class="sxs-lookup"><span data-stu-id="888e6-137">**File**</span></span>|<span data-ttu-id="888e6-138">**Функция**</span><span class="sxs-lookup"><span data-stu-id="888e6-138">**Function**</span></span>|<span data-ttu-id="888e6-139">**Примечание**</span><span class="sxs-lookup"><span data-stu-id="888e6-139">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="888e6-140">Мапифунктионс. cpp</span><span class="sxs-lookup"><span data-stu-id="888e6-140">MAPIFunctions.cpp</span></span>  <br/> |<span data-ttu-id="888e6-141">DeleteProperty</span><span class="sxs-lookup"><span data-stu-id="888e6-141">DeleteProperty</span></span>  <br/> |<span data-ttu-id="888e6-142">MFCMAPI использует метод **IMAPIProp::D елетепропс** для удаления свойства из объекта.</span><span class="sxs-lookup"><span data-stu-id="888e6-142">MFCMAPI uses the **IMAPIProp::DeleteProps** method to delete a property from an object.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="888e6-143">См. также</span><span class="sxs-lookup"><span data-stu-id="888e6-143">See also</span></span>



[<span data-ttu-id="888e6-144">IMAPIProp::GetLastError</span><span class="sxs-lookup"><span data-stu-id="888e6-144">IMAPIProp::GetLastError</span></span>](imapiprop-getlasterror.md)
  
[<span data-ttu-id="888e6-145">IMAPIProp::GetProps</span><span class="sxs-lookup"><span data-stu-id="888e6-145">IMAPIProp::GetProps</span></span>](imapiprop-getprops.md)
  
[<span data-ttu-id="888e6-146">IMAPIProp::SaveChanges</span><span class="sxs-lookup"><span data-stu-id="888e6-146">IMAPIProp::SaveChanges</span></span>](imapiprop-savechanges.md)
  
[<span data-ttu-id="888e6-147">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="888e6-147">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="888e6-148">SPropProblemArray</span><span class="sxs-lookup"><span data-stu-id="888e6-148">SPropProblemArray</span></span>](spropproblemarray.md)
  
[<span data-ttu-id="888e6-149">SPropTagArray</span><span class="sxs-lookup"><span data-stu-id="888e6-149">SPropTagArray</span></span>](sproptagarray.md)
  
[<span data-ttu-id="888e6-150">IMAPIProp : IUnknown</span><span class="sxs-lookup"><span data-stu-id="888e6-150">IMAPIProp : IUnknown</span></span>](imapipropiunknown.md)


[<span data-ttu-id="888e6-151">Mfcmapi (en) � �������� ������� ����</span><span class="sxs-lookup"><span data-stu-id="888e6-151">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

