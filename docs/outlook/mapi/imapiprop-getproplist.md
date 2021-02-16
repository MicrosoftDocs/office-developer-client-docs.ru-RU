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
ms.openlocfilehash: f089fa2c608fb9fcb7deba2e061c5cf5886aa02f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33414790"
---
# <a name="imapipropgetproplist"></a><span data-ttu-id="bab1e-103">IMAPIProp::GetPropList</span><span class="sxs-lookup"><span data-stu-id="bab1e-103">IMAPIProp::GetPropList</span></span>

  
  
<span data-ttu-id="bab1e-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="bab1e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="bab1e-105">Возвращает теги свойств для всех свойств.</span><span class="sxs-lookup"><span data-stu-id="bab1e-105">Returns property tags for all properties.</span></span> 
  
```cpp
HRESULT GetPropList(
  ULONG ulFlags,
  LPSPropTagArray FAR * lppPropTagArray
);
```

## <a name="parameters"></a><span data-ttu-id="bab1e-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="bab1e-106">Parameters</span></span>

 <span data-ttu-id="bab1e-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="bab1e-107">_ulFlags_</span></span>
  
> <span data-ttu-id="bab1e-108">[in] Битовая метка флагов, которая управляет форматом строк в возвращаемом теге свойства.</span><span class="sxs-lookup"><span data-stu-id="bab1e-108">[in] A bitmask of flags that controls the format for the strings in the returned property tags.</span></span> <span data-ttu-id="bab1e-109">Можно установить следующий флаг:</span><span class="sxs-lookup"><span data-stu-id="bab1e-109">The following flag can be set:</span></span>
    
<span data-ttu-id="bab1e-110">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="bab1e-110">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="bab1e-111">Возвращенные строки имеют формат Юникод.</span><span class="sxs-lookup"><span data-stu-id="bab1e-111">The returned strings are in Unicode format.</span></span> <span data-ttu-id="bab1e-112">Если флаг MAPI_UNICODE не установлен, строки будут в формате ANSI.</span><span class="sxs-lookup"><span data-stu-id="bab1e-112">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span>
    
 <span data-ttu-id="bab1e-113">_lppPropTagArray_</span><span class="sxs-lookup"><span data-stu-id="bab1e-113">_lppPropTagArray_</span></span>
  
> <span data-ttu-id="bab1e-114">[out] Указатель на указатель на массив тегов свойств, содержащий теги для всех свойств объекта.</span><span class="sxs-lookup"><span data-stu-id="bab1e-114">[out] A pointer to a pointer to the property tag array that contains tags for all of the object's properties.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="bab1e-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="bab1e-115">Return value</span></span>

<span data-ttu-id="bab1e-116">S_OK</span><span class="sxs-lookup"><span data-stu-id="bab1e-116">S_OK</span></span> 
  
> <span data-ttu-id="bab1e-117">Все теги свойств были возвращены успешно.</span><span class="sxs-lookup"><span data-stu-id="bab1e-117">All of the property tags were returned successfully.</span></span>
    
<span data-ttu-id="bab1e-118">MAPI_E_BAD_CHARWIDTH</span><span class="sxs-lookup"><span data-stu-id="bab1e-118">MAPI_E_BAD_CHARWIDTH</span></span> 
  
> <span data-ttu-id="bab1e-119">Либо флаг MAPI_UNICODE установлен, а реализация не поддерживает Юникод, либо MAPI_UNICODE не установлен, а реализация поддерживает только Юникод.</span><span class="sxs-lookup"><span data-stu-id="bab1e-119">Either the MAPI_UNICODE flag was set and the implementation does not support Unicode, or MAPI_UNICODE was not set and the implementation supports only Unicode.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="bab1e-120">Примечания</span><span class="sxs-lookup"><span data-stu-id="bab1e-120">Remarks</span></span>

<span data-ttu-id="bab1e-121">Метод **IMAPIProp::GetPropList** извлекает тег свойства для каждого свойства, поддерживаемого объектом.</span><span class="sxs-lookup"><span data-stu-id="bab1e-121">The **IMAPIProp::GetPropList** method retrieves the property tag for each property currently supported by an object.</span></span> <span data-ttu-id="bab1e-122">Если в настоящее время объект не поддерживает какие-либо свойства, **GetPropList** возвращает массив тегов свойств, для члена **cValues** установлено 0.</span><span class="sxs-lookup"><span data-stu-id="bab1e-122">If the object does not currently support any properties, **GetPropList** returns a property tag array with the **cValues** member set to 0.</span></span> 
  
<span data-ttu-id="bab1e-123">Область свойств, возвращаемая **GetPropList,** зависит от поставщика.</span><span class="sxs-lookup"><span data-stu-id="bab1e-123">The scope of properties returned by **GetPropList** varies from provider to provider.</span></span> <span data-ttu-id="bab1e-124">Некоторые поставщики услуг исключают те свойства, к которым у вызываемой связи нет доступа.</span><span class="sxs-lookup"><span data-stu-id="bab1e-124">Some service providers exclude those properties for which the caller does not have access.</span></span> <span data-ttu-id="bab1e-125">Все поставщики возвращают свойства **типа** PT_OBJECT.</span><span class="sxs-lookup"><span data-stu-id="bab1e-125">All providers return properties of type **PT_OBJECT**.</span></span>
  
<span data-ttu-id="bab1e-126">Если объект не поддерживает Юникод, **GetPropList** возвращает MAPI_E_BAD_CHARWIDTH, даже если для объекта не определены свойства строки.</span><span class="sxs-lookup"><span data-stu-id="bab1e-126">If the object does not support Unicode, **GetPropList** returns MAPI_E_BAD_CHARWIDTH, even if there are no string properties defined for the object.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="bab1e-127">Примечания для исполнителей</span><span class="sxs-lookup"><span data-stu-id="bab1e-127">Notes to implementers</span></span>

<span data-ttu-id="bab1e-128">Поставщики удаленных транспортных услуг **реализуют GetPropList в** точности так, как указано здесь.</span><span class="sxs-lookup"><span data-stu-id="bab1e-128">Remote transport providers implement **GetPropList** exactly as specified here.</span></span> <span data-ttu-id="bab1e-129">Особых проблем нет.</span><span class="sxs-lookup"><span data-stu-id="bab1e-129">There are no special concerns.</span></span> <span data-ttu-id="bab1e-130">Конечно, реализация должна возвращать тот же список свойств, что и метод [IMAPIProp::GetProps.](imapiprop-getprops.md)</span><span class="sxs-lookup"><span data-stu-id="bab1e-130">Your implementation should, of course, return the same list of properties as supported by the [IMAPIProp::GetProps](imapiprop-getprops.md) method.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="bab1e-131">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="bab1e-131">Notes to callers</span></span>

<span data-ttu-id="bab1e-132">Вызовите [функцию MAPIFreeBuffer,](mapifreebuffer.md) чтобы освободить массив тегов свойств, на который указывает _lppPropTagArray._</span><span class="sxs-lookup"><span data-stu-id="bab1e-132">Call the [MAPIFreeBuffer](mapifreebuffer.md) function to free the property tag array pointed to by  _lppPropTagArray_.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="bab1e-133">Справочные материалы по MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="bab1e-133">MFCMAPI reference</span></span>

<span data-ttu-id="bab1e-134">Пример кода MFCMAPI указан в приведенной ниже таблице.</span><span class="sxs-lookup"><span data-stu-id="bab1e-134">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="bab1e-135">**Файл**</span><span class="sxs-lookup"><span data-stu-id="bab1e-135">**File**</span></span>|<span data-ttu-id="bab1e-136">**Функция**</span><span class="sxs-lookup"><span data-stu-id="bab1e-136">**Function**</span></span>|<span data-ttu-id="bab1e-137">**Примечание**</span><span class="sxs-lookup"><span data-stu-id="bab1e-137">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="bab1e-138">MAPIFunctions.cpp</span><span class="sxs-lookup"><span data-stu-id="bab1e-138">MAPIFunctions.cpp</span></span>  <br/> |<span data-ttu-id="bab1e-139">GetPropsNULL</span><span class="sxs-lookup"><span data-stu-id="bab1e-139">GetPropsNULL</span></span>  <br/> |<span data-ttu-id="bab1e-140">MFCMAPI использует метод **IMAPIProp::GetPropList** для получения списка свойств, передав его **в GetProps.**</span><span class="sxs-lookup"><span data-stu-id="bab1e-140">MFCMAPI uses the **IMAPIProp::GetPropList** method to get a property list to pass to **GetProps**.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="bab1e-141">См. также</span><span class="sxs-lookup"><span data-stu-id="bab1e-141">See also</span></span>



[<span data-ttu-id="bab1e-142">IMAPIProp::GetProps</span><span class="sxs-lookup"><span data-stu-id="bab1e-142">IMAPIProp::GetProps</span></span>](imapiprop-getprops.md)
  
[<span data-ttu-id="bab1e-143">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="bab1e-143">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="bab1e-144">IMAPIProp : IUnknown</span><span class="sxs-lookup"><span data-stu-id="bab1e-144">IMAPIProp : IUnknown</span></span>](imapipropiunknown.md)


[<span data-ttu-id="bab1e-145">Mfcmapi (en) � �������� ������� ����</span><span class="sxs-lookup"><span data-stu-id="bab1e-145">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

