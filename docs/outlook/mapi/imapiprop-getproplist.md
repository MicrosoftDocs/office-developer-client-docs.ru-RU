---
title: IMAPIPropGetPropList
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIProp.GetPropList
api_type:
- COM
ms.assetid: 0069c223-32bb-4286-b763-39fd45dc263b
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 5417853dbb1fa87d2beead2f73ca57329e17b044
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22571124"
---
# <a name="imapipropgetproplist"></a><span data-ttu-id="16077-103">IMAPIProp::GetPropList</span><span class="sxs-lookup"><span data-stu-id="16077-103">IMAPIProp::GetPropList</span></span>

  
  
<span data-ttu-id="16077-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="16077-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="16077-105">Возвращает свойство теги для всех свойств.</span><span class="sxs-lookup"><span data-stu-id="16077-105">Returns property tags for all properties.</span></span> 
  
```cpp
HRESULT GetPropList(
  ULONG ulFlags,
  LPSPropTagArray FAR * lppPropTagArray
);
```

## <a name="parameters"></a><span data-ttu-id="16077-106">���������</span><span class="sxs-lookup"><span data-stu-id="16077-106">Parameters</span></span>

 <span data-ttu-id="16077-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="16077-107">_ulFlags_</span></span>
  
> <span data-ttu-id="16077-108">[in] Битовая маска флаги, который управляет формата для строк в тегах возвращаемого свойства.</span><span class="sxs-lookup"><span data-stu-id="16077-108">[in] A bitmask of flags that controls the format for the strings in the returned property tags.</span></span> <span data-ttu-id="16077-109">Можно задать следующий флаг:</span><span class="sxs-lookup"><span data-stu-id="16077-109">The following flag can be set:</span></span>
    
<span data-ttu-id="16077-110">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="16077-110">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="16077-111">В формате Юникод, возвращенных строк.</span><span class="sxs-lookup"><span data-stu-id="16077-111">The returned strings are in Unicode format.</span></span> <span data-ttu-id="16077-112">Если флаг MAPI_UNICODE не установлен, они в формате ANSI.</span><span class="sxs-lookup"><span data-stu-id="16077-112">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span>
    
 <span data-ttu-id="16077-113">_lppPropTagArray_</span><span class="sxs-lookup"><span data-stu-id="16077-113">_lppPropTagArray_</span></span>
  
> <span data-ttu-id="16077-114">[out] Указатель на указатель массив тег свойство, которое содержит теги для всех свойств объекта.</span><span class="sxs-lookup"><span data-stu-id="16077-114">[out] A pointer to a pointer to the property tag array that contains tags for all of the object's properties.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="16077-115">������������ ��������</span><span class="sxs-lookup"><span data-stu-id="16077-115">Return value</span></span>

<span data-ttu-id="16077-116">ЗНАЧЕНИЕ S_OK</span><span class="sxs-lookup"><span data-stu-id="16077-116">S_OK</span></span> 
  
> <span data-ttu-id="16077-117">Все теги свойство были успешно возвращен.</span><span class="sxs-lookup"><span data-stu-id="16077-117">All of the property tags were returned successfully.</span></span>
    
<span data-ttu-id="16077-118">MAPI_E_BAD_CHARWIDTH</span><span class="sxs-lookup"><span data-stu-id="16077-118">MAPI_E_BAD_CHARWIDTH</span></span> 
  
> <span data-ttu-id="16077-119">Либо был установлен флажок MAPI_UNICODE и реализация не поддерживает Юникод, или MAPI_UNICODE не было установлено и реализация поддерживает только Юникод.</span><span class="sxs-lookup"><span data-stu-id="16077-119">Either the MAPI_UNICODE flag was set and the implementation does not support Unicode, or MAPI_UNICODE was not set and the implementation supports only Unicode.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="16077-120">Замечания</span><span class="sxs-lookup"><span data-stu-id="16077-120">Remarks</span></span>

<span data-ttu-id="16077-121">Метод **IMAPIProp::GetPropList** получает тега свойства для каждого свойства, в настоящее время поддерживается объектом.</span><span class="sxs-lookup"><span data-stu-id="16077-121">The **IMAPIProp::GetPropList** method retrieves the property tag for each property currently supported by an object.</span></span> <span data-ttu-id="16077-122">Если объект не поддерживает все свойства, **GetPropList** возвращает массив свойство тег с элементом **cValues** значение 0.</span><span class="sxs-lookup"><span data-stu-id="16077-122">If the object does not currently support any properties, **GetPropList** returns a property tag array with the **cValues** member set to 0.</span></span> 
  
<span data-ttu-id="16077-123">Область свойств, возвращаемых **GetPropList** зависит от поставщика для поставщика.</span><span class="sxs-lookup"><span data-stu-id="16077-123">The scope of properties returned by **GetPropList** varies from provider to provider.</span></span> <span data-ttu-id="16077-124">Некоторые поставщики услуг исключать эти свойства, для которых вызывающий не имеет доступа.</span><span class="sxs-lookup"><span data-stu-id="16077-124">Some service providers exclude those properties for which the caller does not have access.</span></span> <span data-ttu-id="16077-125">Все поставщики возврата свойств типа **PT_OBJECT**.</span><span class="sxs-lookup"><span data-stu-id="16077-125">All providers return properties of type **PT_OBJECT**.</span></span>
  
<span data-ttu-id="16077-126">Если объект не поддерживает Юникод, **GetPropList** возвращает MAPI_E_BAD_CHARWIDTH, даже в том случае, если нет строки свойств, определенных для объекта.</span><span class="sxs-lookup"><span data-stu-id="16077-126">If the object does not support Unicode, **GetPropList** returns MAPI_E_BAD_CHARWIDTH, even if there are no string properties defined for the object.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="16077-127">Примечания для исполнителей</span><span class="sxs-lookup"><span data-stu-id="16077-127">Notes to implementers</span></span>

<span data-ttu-id="16077-128">Поставщики удаленного транспорта реализовать **GetPropList** именно то, как указано здесь.</span><span class="sxs-lookup"><span data-stu-id="16077-128">Remote transport providers implement **GetPropList** exactly as specified here.</span></span> <span data-ttu-id="16077-129">Существуют нет специальных проблемы.</span><span class="sxs-lookup"><span data-stu-id="16077-129">There are no special concerns.</span></span> <span data-ttu-id="16077-130">Реализация Конечно, вернет тот же список свойства, как поддерживаемый метод [IMAPIProp::GetProps](imapiprop-getprops.md) .</span><span class="sxs-lookup"><span data-stu-id="16077-130">Your implementation should, of course, return the same list of properties as supported by the [IMAPIProp::GetProps](imapiprop-getprops.md) method.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="16077-131">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="16077-131">Notes to callers</span></span>

<span data-ttu-id="16077-132">Вызовите функцию [MAPIFreeBuffer](mapifreebuffer.md) , чтобы освободить место на массива тега свойства, на который указывает _lppPropTagArray_.</span><span class="sxs-lookup"><span data-stu-id="16077-132">Call the [MAPIFreeBuffer](mapifreebuffer.md) function to free the property tag array pointed to by  _lppPropTagArray_.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="16077-133">Справочник по mfcmapi (en)</span><span class="sxs-lookup"><span data-stu-id="16077-133">MFCMAPI reference</span></span>

<span data-ttu-id="16077-134">������ ���� mfcmapi (en) ���������� � ������� ����.</span><span class="sxs-lookup"><span data-stu-id="16077-134">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="16077-135">**����**</span><span class="sxs-lookup"><span data-stu-id="16077-135">**File**</span></span>|<span data-ttu-id="16077-136">**�������**</span><span class="sxs-lookup"><span data-stu-id="16077-136">**Function**</span></span>|<span data-ttu-id="16077-137">**�����������**</span><span class="sxs-lookup"><span data-stu-id="16077-137">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="16077-138">MAPIFunctions.cpp</span><span class="sxs-lookup"><span data-stu-id="16077-138">MAPIFunctions.cpp</span></span>  <br/> |<span data-ttu-id="16077-139">GetPropsNULL</span><span class="sxs-lookup"><span data-stu-id="16077-139">GetPropsNULL</span></span>  <br/> |<span data-ttu-id="16077-140">Mfcmapi (en) использует метод **IMAPIProp::GetPropList** , чтобы получить список свойств для передачи **GetProps**.</span><span class="sxs-lookup"><span data-stu-id="16077-140">MFCMAPI uses the **IMAPIProp::GetPropList** method to get a property list to pass to **GetProps**.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="16077-141">См. также</span><span class="sxs-lookup"><span data-stu-id="16077-141">See also</span></span>



[<span data-ttu-id="16077-142">IMAPIProp::GetProps</span><span class="sxs-lookup"><span data-stu-id="16077-142">IMAPIProp::GetProps</span></span>](imapiprop-getprops.md)
  
[<span data-ttu-id="16077-143">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="16077-143">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="16077-144">IMAPIProp : IUnknown</span><span class="sxs-lookup"><span data-stu-id="16077-144">IMAPIProp : IUnknown</span></span>](imapipropiunknown.md)


[<span data-ttu-id="16077-145">Mfcmapi (en) � �������� ������� ����</span><span class="sxs-lookup"><span data-stu-id="16077-145">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

