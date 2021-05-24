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
ms.openlocfilehash: 95273bf6025d6ef995d7c21c0e44bdbbf59072f6
ms.sourcegitcommit: fb521c23df785c9c3aefa5062272b2630a32e587
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/20/2021
ms.locfileid: "52589175"
---
# <a name="hrgetoneprop"></a><span data-ttu-id="93237-103">HrGetOneProp</span><span class="sxs-lookup"><span data-stu-id="93237-103">HrGetOneProp</span></span>

  
  
<span data-ttu-id="93237-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="93237-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="93237-105">Извлекает значение одного свойства из интерфейса свойства, то есть интерфейса, полученного из [IMAPIProp.](imapipropiunknown.md)</span><span class="sxs-lookup"><span data-stu-id="93237-105">Retrieves the value of a single property from a property interface, that is, an interface derived from [IMAPIProp](imapipropiunknown.md).</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="93237-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="93237-106">Header file:</span></span>  <br/> |<span data-ttu-id="93237-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="93237-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="93237-108">Реализовано в:</span><span class="sxs-lookup"><span data-stu-id="93237-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="93237-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="93237-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="93237-110">Вызывающая сторона:</span><span class="sxs-lookup"><span data-stu-id="93237-110">Called by:</span></span>  <br/> |<span data-ttu-id="93237-111">Клиентские приложения и поставщики услуг</span><span class="sxs-lookup"><span data-stu-id="93237-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
HRESULT HrGetOneProp(
  LPMAPIPROP pmp,
  ULONG ulPropTag,
  LPSPropValue FAR * ppprop
);
```

## <a name="parameters"></a><span data-ttu-id="93237-112">Parameters</span><span class="sxs-lookup"><span data-stu-id="93237-112">Parameters</span></span>

 <span data-ttu-id="93237-113">_pmp_</span><span class="sxs-lookup"><span data-stu-id="93237-113">_pmp_</span></span>
  
> <span data-ttu-id="93237-114">[in] Указатель на [интерфейс IMAPIProp,](imapipropiunknown.md) из которого должно быть извлечено значение свойства.</span><span class="sxs-lookup"><span data-stu-id="93237-114">[in] Pointer to the [IMAPIProp](imapipropiunknown.md) interface from which the property value is to be retrieved.</span></span> 
    
 <span data-ttu-id="93237-115">_ulPropTag_</span><span class="sxs-lookup"><span data-stu-id="93237-115">_ulPropTag_</span></span>
  
> <span data-ttu-id="93237-116">[in] Тег свойства извлекаемого свойства.</span><span class="sxs-lookup"><span data-stu-id="93237-116">[in] Property tag of the property to be retrieved.</span></span> 
    
 <span data-ttu-id="93237-117">_ppprop_</span><span class="sxs-lookup"><span data-stu-id="93237-117">_ppprop_</span></span>
  
> <span data-ttu-id="93237-118">[вышел] Указатель на указатель на возвращенную [структуру SPropValue,](spropvalue.md) определяющий извлеченное значение свойства.</span><span class="sxs-lookup"><span data-stu-id="93237-118">[out] Pointer to a pointer to the returned [SPropValue](spropvalue.md) structure defining the retrieved property value.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="93237-119">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="93237-119">Return value</span></span>

<span data-ttu-id="93237-120">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="93237-120">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="93237-121">Запрашиваемая свойство недоступна из указанного интерфейса.</span><span class="sxs-lookup"><span data-stu-id="93237-121">The requested property is not available from the specified interface.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="93237-122">Примечания</span><span class="sxs-lookup"><span data-stu-id="93237-122">Remarks</span></span>

<span data-ttu-id="93237-123">В отличие [от метода IMAPIProp::GetProps,](imapiprop-getprops.md) функция **HrGetOneProp** никогда не возвращает никаких предупреждений.</span><span class="sxs-lookup"><span data-stu-id="93237-123">Unlike the [IMAPIProp::GetProps](imapiprop-getprops.md) method, the **HrGetOneProp** function never returns any warning.</span></span> <span data-ttu-id="93237-124">Так как оно извлекает только одно свойство, оно просто успешно или не удается.</span><span class="sxs-lookup"><span data-stu-id="93237-124">Because it retrieves only one property, it simply either succeeds or fails.</span></span> <span data-ttu-id="93237-125">Для получения нескольких свойств **GetProps быстрее.**</span><span class="sxs-lookup"><span data-stu-id="93237-125">For retrieving multiple properties, **GetProps** is faster.</span></span> 
  
<span data-ttu-id="93237-126">Можно установить или изменить одно свойство с помощью [функции HrSetOneProp.](hrsetoneprop.md)</span><span class="sxs-lookup"><span data-stu-id="93237-126">You can set or change a single property with the [HrSetOneProp](hrsetoneprop.md) function.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="93237-127">Справочные материалы по MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="93237-127">MFCMAPI reference</span></span>

<span data-ttu-id="93237-128">Пример кода MFCMAPI указан в приведенной ниже таблице.</span><span class="sxs-lookup"><span data-stu-id="93237-128">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="93237-129">**Файл**</span><span class="sxs-lookup"><span data-stu-id="93237-129">**File**</span></span>|<span data-ttu-id="93237-130">**Функция**</span><span class="sxs-lookup"><span data-stu-id="93237-130">**Function**</span></span>|<span data-ttu-id="93237-131">**Примечание**</span><span class="sxs-lookup"><span data-stu-id="93237-131">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="93237-132">MAPIFunctions.cpp</span><span class="sxs-lookup"><span data-stu-id="93237-132">MAPIFunctions.cpp</span></span>  <br/> |<span data-ttu-id="93237-133">GetMAPIObjectType</span><span class="sxs-lookup"><span data-stu-id="93237-133">GetMAPIObjectType</span></span>  <br/> |<span data-ttu-id="93237-134">MFCMAPI использует метод **HrGetOneProp** для получения типа объекта.</span><span class="sxs-lookup"><span data-stu-id="93237-134">MFCMAPI uses the **HrGetOneProp** method to retrieve the type of an object.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="93237-135">См. также</span><span class="sxs-lookup"><span data-stu-id="93237-135">See also</span></span>



[<span data-ttu-id="93237-136">Mfcmapi (en) � �������� ������� ����</span><span class="sxs-lookup"><span data-stu-id="93237-136">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

