---
title: имапипропжетпроплист
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
ms.openlocfilehash: f089fa2c608fb9fcb7deba2e061c5cf5886aa02f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33414790"
---
# <a name="imapipropgetproplist"></a><span data-ttu-id="aa39b-103">IMAPIProp::GetPropList</span><span class="sxs-lookup"><span data-stu-id="aa39b-103">IMAPIProp::GetPropList</span></span>

  
  
<span data-ttu-id="aa39b-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="aa39b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="aa39b-105">Возвращает теги свойств для всех свойств.</span><span class="sxs-lookup"><span data-stu-id="aa39b-105">Returns property tags for all properties.</span></span> 
  
```cpp
HRESULT GetPropList(
  ULONG ulFlags,
  LPSPropTagArray FAR * lppPropTagArray
);
```

## <a name="parameters"></a><span data-ttu-id="aa39b-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="aa39b-106">Parameters</span></span>

 <span data-ttu-id="aa39b-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="aa39b-107">_ulFlags_</span></span>
  
> <span data-ttu-id="aa39b-108">возврата Битовая маска флагов, которая управляет форматом строк в возвращенных тегах свойств.</span><span class="sxs-lookup"><span data-stu-id="aa39b-108">[in] A bitmask of flags that controls the format for the strings in the returned property tags.</span></span> <span data-ttu-id="aa39b-109">Можно задать следующий флаг:</span><span class="sxs-lookup"><span data-stu-id="aa39b-109">The following flag can be set:</span></span>
    
<span data-ttu-id="aa39b-110">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="aa39b-110">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="aa39b-111">Возвращаемые строки представлены в формате Юникод.</span><span class="sxs-lookup"><span data-stu-id="aa39b-111">The returned strings are in Unicode format.</span></span> <span data-ttu-id="aa39b-112">Если флаг MAPI_UNICODE не установлен, строки представлены в формате ANSI.</span><span class="sxs-lookup"><span data-stu-id="aa39b-112">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span>
    
 <span data-ttu-id="aa39b-113">_лпппроптагаррай_</span><span class="sxs-lookup"><span data-stu-id="aa39b-113">_lppPropTagArray_</span></span>
  
> <span data-ttu-id="aa39b-114">вышли Указатель на указатель на массив тегов свойств, который содержит теги для всех свойств объекта.</span><span class="sxs-lookup"><span data-stu-id="aa39b-114">[out] A pointer to a pointer to the property tag array that contains tags for all of the object's properties.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="aa39b-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="aa39b-115">Return value</span></span>

<span data-ttu-id="aa39b-116">S_OK</span><span class="sxs-lookup"><span data-stu-id="aa39b-116">S_OK</span></span> 
  
> <span data-ttu-id="aa39b-117">Все теги свойств успешно возвращены.</span><span class="sxs-lookup"><span data-stu-id="aa39b-117">All of the property tags were returned successfully.</span></span>
    
<span data-ttu-id="aa39b-118">MAPI_E_BAD_CHARWIDTH</span><span class="sxs-lookup"><span data-stu-id="aa39b-118">MAPI_E_BAD_CHARWIDTH</span></span> 
  
> <span data-ttu-id="aa39b-119">Установлен флаг MAPI_UNICODE, а реализация не поддерживает Юникод, или MAPI_UNICODE не задано, а реализация поддерживает только Юникод.</span><span class="sxs-lookup"><span data-stu-id="aa39b-119">Either the MAPI_UNICODE flag was set and the implementation does not support Unicode, or MAPI_UNICODE was not set and the implementation supports only Unicode.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="aa39b-120">Примечания</span><span class="sxs-lookup"><span data-stu-id="aa39b-120">Remarks</span></span>

<span data-ttu-id="aa39b-121">Метод **IMAPIProp:: жетпроплист** извлекает тег свойства для каждого свойства, которое в настоящее время поддерживается объектом.</span><span class="sxs-lookup"><span data-stu-id="aa39b-121">The **IMAPIProp::GetPropList** method retrieves the property tag for each property currently supported by an object.</span></span> <span data-ttu-id="aa39b-122">Если объект в настоящее время не поддерживает какие бы то ни было свойства, **жетпроплист** возвращает массив тегов свойств с набором элементов **квалуес** , равным 0.</span><span class="sxs-lookup"><span data-stu-id="aa39b-122">If the object does not currently support any properties, **GetPropList** returns a property tag array with the **cValues** member set to 0.</span></span> 
  
<span data-ttu-id="aa39b-123">Область действия свойств, возвращаемых **жетпроплист** , отличается от поставщика к поставщику.</span><span class="sxs-lookup"><span data-stu-id="aa39b-123">The scope of properties returned by **GetPropList** varies from provider to provider.</span></span> <span data-ttu-id="aa39b-124">Некоторые поставщики услуг исключают те свойства, для которых у вызывающего абонента нет доступа.</span><span class="sxs-lookup"><span data-stu-id="aa39b-124">Some service providers exclude those properties for which the caller does not have access.</span></span> <span data-ttu-id="aa39b-125">Все поставщики возвращают свойства типа **PT_OBJECT**.</span><span class="sxs-lookup"><span data-stu-id="aa39b-125">All providers return properties of type **PT_OBJECT**.</span></span>
  
<span data-ttu-id="aa39b-126">Если объект не поддерживает Юникод, **жетпроплист** возвращает MAPI_E_BAD_CHARWIDTH, даже если для объекта не определено строковые свойства.</span><span class="sxs-lookup"><span data-stu-id="aa39b-126">If the object does not support Unicode, **GetPropList** returns MAPI_E_BAD_CHARWIDTH, even if there are no string properties defined for the object.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="aa39b-127">Примечания для исполнителей</span><span class="sxs-lookup"><span data-stu-id="aa39b-127">Notes to implementers</span></span>

<span data-ttu-id="aa39b-128">Удаленные поставщики транспорта реализуют **жетпроплист** точно так, как указано здесь.</span><span class="sxs-lookup"><span data-stu-id="aa39b-128">Remote transport providers implement **GetPropList** exactly as specified here.</span></span> <span data-ttu-id="aa39b-129">Нет особых вопросов.</span><span class="sxs-lookup"><span data-stu-id="aa39b-129">There are no special concerns.</span></span> <span data-ttu-id="aa39b-130">Реализация должна, конечно же, возвращать тот же список свойств, который поддерживается методом [IMAPIProp::/PROPS](imapiprop-getprops.md) .</span><span class="sxs-lookup"><span data-stu-id="aa39b-130">Your implementation should, of course, return the same list of properties as supported by the [IMAPIProp::GetProps](imapiprop-getprops.md) method.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="aa39b-131">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="aa39b-131">Notes to callers</span></span>

<span data-ttu-id="aa39b-132">Вызовите функцию [мапифрибуффер](mapifreebuffer.md) , чтобы освободить массив тегов свойств, на который указывает _лпппроптагаррай_.</span><span class="sxs-lookup"><span data-stu-id="aa39b-132">Call the [MAPIFreeBuffer](mapifreebuffer.md) function to free the property tag array pointed to by  _lppPropTagArray_.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="aa39b-133">Справочные материалы по MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="aa39b-133">MFCMAPI reference</span></span>

<span data-ttu-id="aa39b-134">Пример кода MFCMAPI указан в приведенной ниже таблице.</span><span class="sxs-lookup"><span data-stu-id="aa39b-134">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="aa39b-135">**Файл**</span><span class="sxs-lookup"><span data-stu-id="aa39b-135">**File**</span></span>|<span data-ttu-id="aa39b-136">**Функция**</span><span class="sxs-lookup"><span data-stu-id="aa39b-136">**Function**</span></span>|<span data-ttu-id="aa39b-137">**Примечание**</span><span class="sxs-lookup"><span data-stu-id="aa39b-137">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="aa39b-138">Мапифунктионс. cpp</span><span class="sxs-lookup"><span data-stu-id="aa39b-138">MAPIFunctions.cpp</span></span>  <br/> |<span data-ttu-id="aa39b-139">жетпропснулл</span><span class="sxs-lookup"><span data-stu-id="aa39b-139">GetPropsNULL</span></span>  <br/> |<span data-ttu-id="aa39b-140">MFCMAPI использует метод **IMAPIProp:: жетпроплист** для получения списка свойств, который передается в методе **PROPS**.</span><span class="sxs-lookup"><span data-stu-id="aa39b-140">MFCMAPI uses the **IMAPIProp::GetPropList** method to get a property list to pass to **GetProps**.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="aa39b-141">См. также</span><span class="sxs-lookup"><span data-stu-id="aa39b-141">See also</span></span>



[<span data-ttu-id="aa39b-142">IMAPIProp::GetProps</span><span class="sxs-lookup"><span data-stu-id="aa39b-142">IMAPIProp::GetProps</span></span>](imapiprop-getprops.md)
  
[<span data-ttu-id="aa39b-143">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="aa39b-143">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="aa39b-144">IMAPIProp : IUnknown</span><span class="sxs-lookup"><span data-stu-id="aa39b-144">IMAPIProp : IUnknown</span></span>](imapipropiunknown.md)


[<span data-ttu-id="aa39b-145">Mfcmapi (en) � �������� ������� ����</span><span class="sxs-lookup"><span data-stu-id="aa39b-145">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

