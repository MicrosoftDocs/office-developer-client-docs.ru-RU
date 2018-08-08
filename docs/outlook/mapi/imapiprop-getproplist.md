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
ms.openlocfilehash: 0457007334ad8cc69dade3abd5859dd0d5f7af7f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19809029"
---
# <a name="imapipropgetproplist"></a><span data-ttu-id="95009-103">IMAPIProp::GetPropList</span><span class="sxs-lookup"><span data-stu-id="95009-103">IMAPIProp::GetPropList</span></span>

  
  
<span data-ttu-id="95009-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="95009-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="95009-105">Возвращает свойство теги для всех свойств.</span><span class="sxs-lookup"><span data-stu-id="95009-105">Returns property tags for all properties.</span></span> 
  
```cpp
HRESULT GetPropList(
  ULONG ulFlags,
  LPSPropTagArray FAR * lppPropTagArray
);
```

## <a name="parameters"></a><span data-ttu-id="95009-106">���������</span><span class="sxs-lookup"><span data-stu-id="95009-106">Parameters</span></span>

 <span data-ttu-id="95009-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="95009-107">_ulFlags_</span></span>
  
> <span data-ttu-id="95009-108">[in] Битовая маска флаги, который управляет формата для строк в тегах возвращаемого свойства.</span><span class="sxs-lookup"><span data-stu-id="95009-108">[in] A bitmask of flags that controls the format for the strings in the returned property tags.</span></span> <span data-ttu-id="95009-109">Можно задать следующий флаг:</span><span class="sxs-lookup"><span data-stu-id="95009-109">The following flag can be set:</span></span>
    
<span data-ttu-id="95009-110">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="95009-110">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="95009-111">В формате Юникод, возвращенных строк.</span><span class="sxs-lookup"><span data-stu-id="95009-111">The returned strings are in Unicode format.</span></span> <span data-ttu-id="95009-112">Если флаг MAPI_UNICODE не установлен, они в формате ANSI.</span><span class="sxs-lookup"><span data-stu-id="95009-112">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span>
    
 <span data-ttu-id="95009-113">_lppPropTagArray_</span><span class="sxs-lookup"><span data-stu-id="95009-113">_lppPropTagArray_</span></span>
  
> <span data-ttu-id="95009-114">[out] Указатель на указатель массив тег свойство, которое содержит теги для всех свойств объекта.</span><span class="sxs-lookup"><span data-stu-id="95009-114">[out] A pointer to a pointer to the property tag array that contains tags for all of the object's properties.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="95009-115">������������ ��������</span><span class="sxs-lookup"><span data-stu-id="95009-115">Return value</span></span>

<span data-ttu-id="95009-116">ЗНАЧЕНИЕ S_OK</span><span class="sxs-lookup"><span data-stu-id="95009-116">S_OK</span></span> 
  
> <span data-ttu-id="95009-117">Все теги свойство были успешно возвращен.</span><span class="sxs-lookup"><span data-stu-id="95009-117">All of the property tags were returned successfully.</span></span>
    
<span data-ttu-id="95009-118">MAPI_E_BAD_CHARWIDTH</span><span class="sxs-lookup"><span data-stu-id="95009-118">MAPI_E_BAD_CHARWIDTH</span></span> 
  
> <span data-ttu-id="95009-119">Либо был установлен флажок MAPI_UNICODE и реализация не поддерживает Юникод, или MAPI_UNICODE не было установлено и реализация поддерживает только Юникод.</span><span class="sxs-lookup"><span data-stu-id="95009-119">Either the MAPI_UNICODE flag was set and the implementation does not support Unicode, or MAPI_UNICODE was not set and the implementation supports only Unicode.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="95009-120">Замечания</span><span class="sxs-lookup"><span data-stu-id="95009-120">Remarks</span></span>

<span data-ttu-id="95009-121">Метод **IMAPIProp::GetPropList** получает тега свойства для каждого свойства, в настоящее время поддерживается объектом.</span><span class="sxs-lookup"><span data-stu-id="95009-121">The **IMAPIProp::GetPropList** method retrieves the property tag for each property currently supported by an object.</span></span> <span data-ttu-id="95009-122">Если объект не поддерживает все свойства, **GetPropList** возвращает массив свойство тег с элементом **cValues** значение 0.</span><span class="sxs-lookup"><span data-stu-id="95009-122">If the object does not currently support any properties, **GetPropList** returns a property tag array with the **cValues** member set to 0.</span></span> 
  
<span data-ttu-id="95009-123">Область свойств, возвращаемых **GetPropList** зависит от поставщика для поставщика.</span><span class="sxs-lookup"><span data-stu-id="95009-123">The scope of properties returned by **GetPropList** varies from provider to provider.</span></span> <span data-ttu-id="95009-124">Некоторые поставщики услуг исключать эти свойства, для которых вызывающий не имеет доступа.</span><span class="sxs-lookup"><span data-stu-id="95009-124">Some service providers exclude those properties for which the caller does not have access.</span></span> <span data-ttu-id="95009-125">Все поставщики возврата свойств типа **PT_OBJECT**.</span><span class="sxs-lookup"><span data-stu-id="95009-125">All providers return properties of type **PT_OBJECT**.</span></span>
  
<span data-ttu-id="95009-126">Если объект не поддерживает Юникод, **GetPropList** возвращает MAPI_E_BAD_CHARWIDTH, даже в том случае, если нет строки свойств, определенных для объекта.</span><span class="sxs-lookup"><span data-stu-id="95009-126">If the object does not support Unicode, **GetPropList** returns MAPI_E_BAD_CHARWIDTH, even if there are no string properties defined for the object.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="95009-127">Примечания для исполнителей</span><span class="sxs-lookup"><span data-stu-id="95009-127">Notes to implementers</span></span>

<span data-ttu-id="95009-128">Поставщики удаленного транспорта реализовать **GetPropList** именно то, как указано здесь.</span><span class="sxs-lookup"><span data-stu-id="95009-128">Remote transport providers implement **GetPropList** exactly as specified here.</span></span> <span data-ttu-id="95009-129">Существуют нет специальных проблемы.</span><span class="sxs-lookup"><span data-stu-id="95009-129">There are no special concerns.</span></span> <span data-ttu-id="95009-130">Реализация Конечно, вернет тот же список свойства, как поддерживаемый метод [IMAPIProp::GetProps](imapiprop-getprops.md) .</span><span class="sxs-lookup"><span data-stu-id="95009-130">Your implementation should, of course, return the same list of properties as supported by the [IMAPIProp::GetProps](imapiprop-getprops.md) method.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="95009-131">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="95009-131">Notes to callers</span></span>

<span data-ttu-id="95009-132">Вызовите функцию [MAPIFreeBuffer](mapifreebuffer.md) , чтобы освободить место на массива тега свойства, на который указывает _lppPropTagArray_.</span><span class="sxs-lookup"><span data-stu-id="95009-132">Call the [MAPIFreeBuffer](mapifreebuffer.md) function to free the property tag array pointed to by  _lppPropTagArray_.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="95009-133">Справочник по mfcmapi (en)</span><span class="sxs-lookup"><span data-stu-id="95009-133">MFCMAPI reference</span></span>

<span data-ttu-id="95009-134">������ ���� mfcmapi (en) ���������� � ������� ����.</span><span class="sxs-lookup"><span data-stu-id="95009-134">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="95009-135">**����**</span><span class="sxs-lookup"><span data-stu-id="95009-135">**File**</span></span>|<span data-ttu-id="95009-136">**�������**</span><span class="sxs-lookup"><span data-stu-id="95009-136">**Function**</span></span>|<span data-ttu-id="95009-137">**�����������**</span><span class="sxs-lookup"><span data-stu-id="95009-137">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="95009-138">MAPIFunctions.cpp</span><span class="sxs-lookup"><span data-stu-id="95009-138">MAPIFunctions.cpp</span></span>  <br/> |<span data-ttu-id="95009-139">GetPropsNULL</span><span class="sxs-lookup"><span data-stu-id="95009-139">GetPropsNULL</span></span>  <br/> |<span data-ttu-id="95009-140">Mfcmapi (en) использует метод **IMAPIProp::GetPropList** , чтобы получить список свойств для передачи **GetProps**.</span><span class="sxs-lookup"><span data-stu-id="95009-140">MFCMAPI uses the **IMAPIProp::GetPropList** method to get a property list to pass to **GetProps**.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="95009-141">См. также</span><span class="sxs-lookup"><span data-stu-id="95009-141">See also</span></span>



[<span data-ttu-id="95009-142">IMAPIProp::GetProps</span><span class="sxs-lookup"><span data-stu-id="95009-142">IMAPIProp::GetProps</span></span>](imapiprop-getprops.md)
  
[<span data-ttu-id="95009-143">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="95009-143">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="95009-144">IMAPIProp : IUnknown</span><span class="sxs-lookup"><span data-stu-id="95009-144">IMAPIProp : IUnknown</span></span>](imapipropiunknown.md)


[<span data-ttu-id="95009-145">Mfcmapi (en) � �������� ������� ����</span><span class="sxs-lookup"><span data-stu-id="95009-145">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

