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
ms.openlocfilehash: 8eb19f9a2d3458e153b0758b56c502ce612be0cc
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19809044"
---
# <a name="imapipropdeleteprops"></a><span data-ttu-id="c7251-103">IMAPIProp::DeleteProps</span><span class="sxs-lookup"><span data-stu-id="c7251-103">IMAPIProp::DeleteProps</span></span>

  
  
<span data-ttu-id="c7251-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="c7251-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="c7251-105">Удаляет одно или несколько свойств объекта.</span><span class="sxs-lookup"><span data-stu-id="c7251-105">Deletes one or more properties from an object.</span></span> 
  
```cpp
HRESULT DeleteProps(
  LPSPropTagArray lpPropTagArray,
  LPSPropProblemArray FAR * lppProblems
);
```

## <a name="parameters"></a><span data-ttu-id="c7251-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="c7251-106">Parameters</span></span>

 <span data-ttu-id="c7251-107">_lpPropTagArray_</span><span class="sxs-lookup"><span data-stu-id="c7251-107">_lpPropTagArray_</span></span>
  
> <span data-ttu-id="c7251-108">[in] Указатель на массив тегов свойств, которые указывают свойства, которые нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="c7251-108">[in] A pointer to an array of property tags that indicate the properties to delete.</span></span> <span data-ttu-id="c7251-109">Член **cValues** структуры [SPropTagArray](sproptagarray.md) , на который указывает _lpPropTagArray_ не должна быть нулевой и сам параметр _lpPropTagArray_ не должна быть NULL.</span><span class="sxs-lookup"><span data-stu-id="c7251-109">The **cValues** member of the [SPropTagArray](sproptagarray.md) structure pointed to by  _lpPropTagArray_ must not be zero, and the  _lpPropTagArray_ parameter itself must not be NULL.</span></span> 
    
 <span data-ttu-id="c7251-110">_lppProblems_</span><span class="sxs-lookup"><span data-stu-id="c7251-110">_lppProblems_</span></span>
  
> <span data-ttu-id="c7251-111">[in, out] На входе указатель указатель на структуру [SPropProblemArray](spropproblemarray.md) ; в противном случае — значение NULL, который означает, что нет необходимости для получения сведений об ошибках.</span><span class="sxs-lookup"><span data-stu-id="c7251-111">[in, out] On input, a pointer to a pointer to an [SPropProblemArray](spropproblemarray.md) structure; otherwise, NULL, which indicates that there is no need for error information.</span></span> <span data-ttu-id="c7251-112">Если _lppProblems_ допустимый указатель на входные данные, **DeleteProps** возвращает подробные сведения об ошибках в удаления одного или нескольких свойств.</span><span class="sxs-lookup"><span data-stu-id="c7251-112">If  _lppProblems_ is a valid pointer on input, **DeleteProps** returns detailed information about errors in deleting one or more properties.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="c7251-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="3">Return value</span></span>

<span data-ttu-id="c7251-114">ЗНАЧЕНИЕ S_OK</span><span class="sxs-lookup"><span data-stu-id="c7251-114">S_OK</span></span> 
  
> <span data-ttu-id="c7251-115">Свойства были успешно удалены.</span><span class="sxs-lookup"><span data-stu-id="c7251-115">Properties were successfully deleted.</span></span>
    
<span data-ttu-id="c7251-116">MAPI_E_NO_ACCESS</span><span class="sxs-lookup"><span data-stu-id="c7251-116">MAPI_E_NO_ACCESS</span></span> 
  
> <span data-ttu-id="c7251-117">Вызывающий не имеет разрешений на удаление свойства.</span><span class="sxs-lookup"><span data-stu-id="c7251-117">The caller has insufficient permissions to delete properties.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="c7251-118">Замечания</span><span class="sxs-lookup"><span data-stu-id="c7251-118">Remarks</span></span>

<span data-ttu-id="c7251-119">Метод **IMAPIProp::DeleteProps** удаляет одного или нескольких свойств из текущего объекта.</span><span class="sxs-lookup"><span data-stu-id="c7251-119">The **IMAPIProp::DeleteProps** method removes one or more properties from the current object.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="c7251-120">Примечания для исполнителей</span><span class="sxs-lookup"><span data-stu-id="c7251-120">Notes to implementers</span></span>

<span data-ttu-id="c7251-121">Необходимо разрешить свойства к удалению из всех объектов.</span><span class="sxs-lookup"><span data-stu-id="c7251-121">You do not have to allow properties to be deleted from all objects.</span></span> <span data-ttu-id="c7251-122">Если объект не является изменяемым, возвратите MAPI_E_NO_ACCESS из метода **DeleteProps** .</span><span class="sxs-lookup"><span data-stu-id="c7251-122">If the object is not modifiable, return MAPI_E_NO_ACCESS from the **DeleteProps** method.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="c7251-123">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="c7251-123">Notes to callers</span></span>

<span data-ttu-id="c7251-124">Задать тип свойства для каждого свойства тега в массиве тег свойство указывает параметр _lpPropTagArray_ не нужно.</span><span class="sxs-lookup"><span data-stu-id="c7251-124">You do not have to set the property type for each property tag in the property tag array pointed to by the  _lpPropTagArray_ parameter.</span></span> <span data-ttu-id="c7251-125">Типы свойств игнорируются; используются только идентификаторы свойств.</span><span class="sxs-lookup"><span data-stu-id="c7251-125">Property types are ignored; only the property identifiers are used.</span></span> 
  
<span data-ttu-id="c7251-126">Обратите внимание, что некоторые объекты не разрешать изменений и возврата, что эти объекты MAPI_E_NO_ACCESS из метода **DeleteProps** .</span><span class="sxs-lookup"><span data-stu-id="c7251-126">Be aware that some objects do not allow modification and that these objects return MAPI_E_NO_ACCESS from the **DeleteProps** method.</span></span> <span data-ttu-id="c7251-127">Другие объекты разрешить некоторые свойства к удалению, но не для других пользователей.</span><span class="sxs-lookup"><span data-stu-id="c7251-127">Other objects allow some properties to be deleted, but not others.</span></span> <span data-ttu-id="c7251-128">При наличии проблем удаление только некоторые свойства, **DeleteProps** возвращает значение S_OK.</span><span class="sxs-lookup"><span data-stu-id="c7251-128">When there is a problem deleting only some of the properties, **DeleteProps** returns S_OK.</span></span> <span data-ttu-id="c7251-129">Если допустимый указатель выполнены в параметре _lppProblems_ , **DeleteProps** установит указатель на структуру **SPropProblemArray** , который содержит подробные сведения о проблемах, связанных с каждого свойства.</span><span class="sxs-lookup"><span data-stu-id="c7251-129">If you have passed a valid pointer in the  _lppProblems_ parameter, **DeleteProps** will set the pointer to an **SPropProblemArray** structure that contains detailed information about the problems with each property.</span></span> <span data-ttu-id="c7251-130">Например при удалении все свойства сообщения и проблемы с одним или несколькими его вложения, структура **SPropProblemArray** будет содержать запись для **PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments ](pidtagmessageattachments-canonical-property.md)) свойство.</span><span class="sxs-lookup"><span data-stu-id="c7251-130">For example, if you are deleting all of the properties of a message and there is a problem with one or more of its attachments, the **SPropProblemArray** structure will contain an entry for the **PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md)) property.</span></span> 
  
<span data-ttu-id="c7251-131">Структура, на который указывает _lppProblems_ допустимо только в том случае, если **DeleteProps** возвращает значение S_OK.</span><span class="sxs-lookup"><span data-stu-id="c7251-131">The structure pointed to by  _lppProblems_ is only valid if **DeleteProps** returns S_OK.</span></span> <span data-ttu-id="c7251-132">Если **DeleteProps** возвращает ошибку, не следует использовать структуру **SPropProblemArray** .</span><span class="sxs-lookup"><span data-stu-id="c7251-132">If **DeleteProps** returns an error, do not attempt to use the **SPropProblemArray** structure.</span></span> <span data-ttu-id="c7251-133">Вместо этого вызов метода [IMAPIProp::GetLastError](imapiprop-getlasterror.md) объекта для получения дополнительных сведений об ошибке.</span><span class="sxs-lookup"><span data-stu-id="c7251-133">Instead, call the object's [IMAPIProp::GetLastError](imapiprop-getlasterror.md) method to obtain more information about the error.</span></span> 
  
<span data-ttu-id="c7251-134">Бесплатная загрузка возвращенные структура **SPropProblemArray** путем вызова функции [MAPIFreeBuffer](mapifreebuffer.md) .</span><span class="sxs-lookup"><span data-stu-id="c7251-134">Free the returned **SPropProblemArray** structure by calling the [MAPIFreeBuffer](mapifreebuffer.md) function.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="c7251-135">Справочник по mfcmapi (en)</span><span class="sxs-lookup"><span data-stu-id="c7251-135">MFCMAPI reference</span></span>

<span data-ttu-id="c7251-136">������ ���� mfcmapi (en) ���������� � ������� ����.</span><span class="sxs-lookup"><span data-stu-id="c7251-136">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="c7251-137">**����**</span><span class="sxs-lookup"><span data-stu-id="c7251-137">**File**</span></span>|<span data-ttu-id="c7251-138">**�������**</span><span class="sxs-lookup"><span data-stu-id="c7251-138">**Function**</span></span>|<span data-ttu-id="c7251-139">**�����������**</span><span class="sxs-lookup"><span data-stu-id="c7251-139">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="c7251-140">MAPIFunctions.cpp</span><span class="sxs-lookup"><span data-stu-id="c7251-140">MAPIFunctions.cpp</span></span>  <br/> |<span data-ttu-id="c7251-141">DeleteProperty</span><span class="sxs-lookup"><span data-stu-id="c7251-141">DeleteProperty</span></span>  <br/> |<span data-ttu-id="c7251-142">Mfcmapi (en) использует метод **IMAPIProp::DeleteProps** , чтобы удалить свойство из объекта.</span><span class="sxs-lookup"><span data-stu-id="c7251-142">MFCMAPI uses the **IMAPIProp::DeleteProps** method to delete a property from an object.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="c7251-143">См. также</span><span class="sxs-lookup"><span data-stu-id="c7251-143">See also</span></span>



[<span data-ttu-id="c7251-144">IMAPIProp::GetLastError</span><span class="sxs-lookup"><span data-stu-id="c7251-144">IMAPIProp::GetLastError</span></span>](imapiprop-getlasterror.md)
  
[<span data-ttu-id="c7251-145">IMAPIProp::GetProps</span><span class="sxs-lookup"><span data-stu-id="c7251-145">IMAPIProp::GetProps</span></span>](imapiprop-getprops.md)
  
[<span data-ttu-id="c7251-146">IMAPIProp::SaveChanges</span><span class="sxs-lookup"><span data-stu-id="c7251-146">IMAPIProp::SaveChanges</span></span>](imapiprop-savechanges.md)
  
[<span data-ttu-id="c7251-147">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="c7251-147">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="c7251-148">SPropProblemArray</span><span class="sxs-lookup"><span data-stu-id="c7251-148">SPropProblemArray</span></span>](spropproblemarray.md)
  
[<span data-ttu-id="c7251-149">SPropTagArray</span><span class="sxs-lookup"><span data-stu-id="c7251-149">SPropTagArray</span></span>](sproptagarray.md)
  
[<span data-ttu-id="c7251-150">IMAPIProp : IUnknown</span><span class="sxs-lookup"><span data-stu-id="c7251-150">IMAPIProp : IUnknown</span></span>](imapipropiunknown.md)


[<span data-ttu-id="c7251-151">Mfcmapi (en) � �������� ������� ����</span><span class="sxs-lookup"><span data-stu-id="c7251-151">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

