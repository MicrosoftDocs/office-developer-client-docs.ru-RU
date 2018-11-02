---
title: HrGetOneProp
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- HrGetOneProp
api_type:
- HeaderDef
ms.assetid: 8d0a381a-e714-4663-9a57-b0e1cdbd6ba7
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 99b63e7b0b31a603bf372b1d52e83af39784b628
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22564159"
---
# <a name="hrgetoneprop"></a><span data-ttu-id="b5d7e-103">HrGetOneProp</span><span class="sxs-lookup"><span data-stu-id="b5d7e-103">HrGetOneProp</span></span>

  
  
<span data-ttu-id="b5d7e-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b5d7e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b5d7e-105">Извлекает значения одного свойства из интерфейса свойство, то есть, производные от [IMAPIProp](imapipropiunknown.md)интерфейс.</span><span class="sxs-lookup"><span data-stu-id="b5d7e-105">Retrieves the value of a single property from a property interface, that is, an interface derived from [IMAPIProp](imapipropiunknown.md).</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="b5d7e-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="b5d7e-106">Header file:</span></span>  <br/> |<span data-ttu-id="b5d7e-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="b5d7e-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="b5d7e-108">Реализовано в:</span><span class="sxs-lookup"><span data-stu-id="b5d7e-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="b5d7e-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="b5d7e-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="b5d7e-110">Вызывающая сторона:</span><span class="sxs-lookup"><span data-stu-id="b5d7e-110">Called by:</span></span>  <br/> |<span data-ttu-id="b5d7e-111">Клиентские приложения и поставщиков услуг</span><span class="sxs-lookup"><span data-stu-id="b5d7e-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
HrGetOneProp(
  LPMAPIPROP pmp,
  ULONG ulPropTag,
  LPSPropValue FAR * ppprop
);
```

## <a name="parameters"></a><span data-ttu-id="b5d7e-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="b5d7e-112">Parameters</span></span>

 <span data-ttu-id="b5d7e-113">_pmp_</span><span class="sxs-lookup"><span data-stu-id="b5d7e-113">_pmp_</span></span>
  
> <span data-ttu-id="b5d7e-114">[in] Указатель на интерфейс [IMAPIProp](imapipropiunknown.md) , из которого выполняется получение значения свойства.</span><span class="sxs-lookup"><span data-stu-id="b5d7e-114">[in] Pointer to the [IMAPIProp](imapipropiunknown.md) interface from which the property value is to be retrieved.</span></span> 
    
 <span data-ttu-id="b5d7e-115">_ulPropTag_</span><span class="sxs-lookup"><span data-stu-id="b5d7e-115">_ulPropTag_</span></span>
  
> <span data-ttu-id="b5d7e-116">[in] Свойство tag свойства нужно вернуть.</span><span class="sxs-lookup"><span data-stu-id="b5d7e-116">[in] Property tag of the property to be retrieved.</span></span> 
    
 <span data-ttu-id="b5d7e-117">_ppprop_</span><span class="sxs-lookup"><span data-stu-id="b5d7e-117">_ppprop_</span></span>
  
> <span data-ttu-id="b5d7e-118">[out] Указатель на указатель на структуру возвращенные [SPropValue](spropvalue.md) , определяющий значение извлеченное свойство.</span><span class="sxs-lookup"><span data-stu-id="b5d7e-118">[out] Pointer to a pointer to the returned [SPropValue](spropvalue.md) structure defining the retrieved property value.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="b5d7e-119">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="b5d7e-119">Return value</span></span>

<span data-ttu-id="b5d7e-120">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="b5d7e-120">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="b5d7e-121">Свойство недоступен из указанного интерфейса.</span><span class="sxs-lookup"><span data-stu-id="b5d7e-121">The requested property is not available from the specified interface.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="b5d7e-122">Примечания</span><span class="sxs-lookup"><span data-stu-id="b5d7e-122">Remarks</span></span>

<span data-ttu-id="b5d7e-123">В отличие от метода [IMAPIProp::GetProps](imapiprop-getprops.md) функция **HrGetOneProp** никогда не возвращает все предупреждения.</span><span class="sxs-lookup"><span data-stu-id="b5d7e-123">Unlike the [IMAPIProp::GetProps](imapiprop-getprops.md) method, the **HrGetOneProp** function never returns any warning.</span></span> <span data-ttu-id="b5d7e-124">Так как он получает только одно свойство, он просто либо успешного или неудачного завершения.</span><span class="sxs-lookup"><span data-stu-id="b5d7e-124">Because it retrieves only one property, it simply either succeeds or fails.</span></span> <span data-ttu-id="b5d7e-125">Для получения значений нескольких свойств, **GetProps** выполняется быстрее.</span><span class="sxs-lookup"><span data-stu-id="b5d7e-125">For retrieving multiple properties, **GetProps** is faster.</span></span> 
  
<span data-ttu-id="b5d7e-126">Можно установить или изменить отдельное свойство с помощью функции [HrSetOneProp](hrsetoneprop.md) .</span><span class="sxs-lookup"><span data-stu-id="b5d7e-126">You can set or change a single property with the [HrSetOneProp](hrsetoneprop.md) function.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="b5d7e-127">Справочные материалы по MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="b5d7e-127">MFCMAPI reference</span></span>

<span data-ttu-id="b5d7e-128">Пример кода MFCMAPI указан в приведенной ниже таблице.</span><span class="sxs-lookup"><span data-stu-id="b5d7e-128">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="b5d7e-129">**Файл**</span><span class="sxs-lookup"><span data-stu-id="b5d7e-129">**File**</span></span>|<span data-ttu-id="b5d7e-130">**Функция**</span><span class="sxs-lookup"><span data-stu-id="b5d7e-130">**Function**</span></span>|<span data-ttu-id="b5d7e-131">**Примечание**</span><span class="sxs-lookup"><span data-stu-id="b5d7e-131">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="b5d7e-132">MAPIFunctions.cpp</span><span class="sxs-lookup"><span data-stu-id="b5d7e-132">MAPIFunctions.cpp</span></span>  <br/> |<span data-ttu-id="b5d7e-133">GetMAPIObjectType</span><span class="sxs-lookup"><span data-stu-id="b5d7e-133">GetMAPIObjectType</span></span>  <br/> |<span data-ttu-id="b5d7e-134">Mfcmapi (en) используется метод **HrGetOneProp** для получения типа объекта.</span><span class="sxs-lookup"><span data-stu-id="b5d7e-134">MFCMAPI uses the **HrGetOneProp** method to retrieve the type of an object.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="b5d7e-135">См. также</span><span class="sxs-lookup"><span data-stu-id="b5d7e-135">See also</span></span>



[<span data-ttu-id="b5d7e-136">Mfcmapi (en) � �������� ������� ����</span><span class="sxs-lookup"><span data-stu-id="b5d7e-136">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

