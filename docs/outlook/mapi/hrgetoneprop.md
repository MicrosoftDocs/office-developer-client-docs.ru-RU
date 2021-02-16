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
ms.openlocfilehash: e5adc7d0c317d8b803645d78227777998d7d241f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33416057"
---
# <a name="hrgetoneprop"></a><span data-ttu-id="3e8f9-103">HrGetOneProp</span><span class="sxs-lookup"><span data-stu-id="3e8f9-103">HrGetOneProp</span></span>

  
  
<span data-ttu-id="3e8f9-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3e8f9-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3e8f9-105">Извлекает значение одного свойства из интерфейса свойства, то есть интерфейса, производного от [IMAPIProp.](imapipropiunknown.md)</span><span class="sxs-lookup"><span data-stu-id="3e8f9-105">Retrieves the value of a single property from a property interface, that is, an interface derived from [IMAPIProp](imapipropiunknown.md).</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="3e8f9-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="3e8f9-106">Header file:</span></span>  <br/> |<span data-ttu-id="3e8f9-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="3e8f9-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="3e8f9-108">Реализовано в:</span><span class="sxs-lookup"><span data-stu-id="3e8f9-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="3e8f9-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="3e8f9-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="3e8f9-110">Вызывающая сторона:</span><span class="sxs-lookup"><span data-stu-id="3e8f9-110">Called by:</span></span>  <br/> |<span data-ttu-id="3e8f9-111">Клиентские приложения и поставщики услуг</span><span class="sxs-lookup"><span data-stu-id="3e8f9-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
HrGetOneProp(
  LPMAPIPROP pmp,
  ULONG ulPropTag,
  LPSPropValue FAR * ppprop
);
```

## <a name="parameters"></a><span data-ttu-id="3e8f9-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="3e8f9-112">Parameters</span></span>

 <span data-ttu-id="3e8f9-113">_pmp_</span><span class="sxs-lookup"><span data-stu-id="3e8f9-113">_pmp_</span></span>
  
> <span data-ttu-id="3e8f9-114">[in] Указатель на интерфейс [IMAPIProp,](imapipropiunknown.md) из которого требуется получить значение свойства.</span><span class="sxs-lookup"><span data-stu-id="3e8f9-114">[in] Pointer to the [IMAPIProp](imapipropiunknown.md) interface from which the property value is to be retrieved.</span></span> 
    
 <span data-ttu-id="3e8f9-115">_ulPropTag_</span><span class="sxs-lookup"><span data-stu-id="3e8f9-115">_ulPropTag_</span></span>
  
> <span data-ttu-id="3e8f9-116">[in] Тег свойства извлекаемого свойства.</span><span class="sxs-lookup"><span data-stu-id="3e8f9-116">[in] Property tag of the property to be retrieved.</span></span> 
    
 <span data-ttu-id="3e8f9-117">_ppprop_</span><span class="sxs-lookup"><span data-stu-id="3e8f9-117">_ppprop_</span></span>
  
> <span data-ttu-id="3e8f9-118">[out] Указатель на указатель на возвращенную [структуру SPropValue,](spropvalue.md) определяющий извлеченное значение свойства.</span><span class="sxs-lookup"><span data-stu-id="3e8f9-118">[out] Pointer to a pointer to the returned [SPropValue](spropvalue.md) structure defining the retrieved property value.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="3e8f9-119">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="3e8f9-119">Return value</span></span>

<span data-ttu-id="3e8f9-120">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="3e8f9-120">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="3e8f9-121">Запрашиваемая свойство недоступна из указанного интерфейса.</span><span class="sxs-lookup"><span data-stu-id="3e8f9-121">The requested property is not available from the specified interface.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="3e8f9-122">Примечания</span><span class="sxs-lookup"><span data-stu-id="3e8f9-122">Remarks</span></span>

<span data-ttu-id="3e8f9-123">В отличие [от метода IMAPIProp::GetProps](imapiprop-getprops.md) функция **HrGetOneProp** никогда не возвращает никаких предупреждений.</span><span class="sxs-lookup"><span data-stu-id="3e8f9-123">Unlike the [IMAPIProp::GetProps](imapiprop-getprops.md) method, the **HrGetOneProp** function never returns any warning.</span></span> <span data-ttu-id="3e8f9-124">Так как он получает только одно свойство, он просто успешно или неудачно.</span><span class="sxs-lookup"><span data-stu-id="3e8f9-124">Because it retrieves only one property, it simply either succeeds or fails.</span></span> <span data-ttu-id="3e8f9-125">Для получения нескольких свойств **getProps** быстрее.</span><span class="sxs-lookup"><span data-stu-id="3e8f9-125">For retrieving multiple properties, **GetProps** is faster.</span></span> 
  
<span data-ttu-id="3e8f9-126">Можно установить или изменить одно свойство с помощью функции [HrSetOneProp.](hrsetoneprop.md)</span><span class="sxs-lookup"><span data-stu-id="3e8f9-126">You can set or change a single property with the [HrSetOneProp](hrsetoneprop.md) function.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="3e8f9-127">Справочные материалы по MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="3e8f9-127">MFCMAPI reference</span></span>

<span data-ttu-id="3e8f9-128">Пример кода MFCMAPI указан в приведенной ниже таблице.</span><span class="sxs-lookup"><span data-stu-id="3e8f9-128">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="3e8f9-129">**Файл**</span><span class="sxs-lookup"><span data-stu-id="3e8f9-129">**File**</span></span>|<span data-ttu-id="3e8f9-130">**Функция**</span><span class="sxs-lookup"><span data-stu-id="3e8f9-130">**Function**</span></span>|<span data-ttu-id="3e8f9-131">**Примечание**</span><span class="sxs-lookup"><span data-stu-id="3e8f9-131">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="3e8f9-132">MAPIFunctions.cpp</span><span class="sxs-lookup"><span data-stu-id="3e8f9-132">MAPIFunctions.cpp</span></span>  <br/> |<span data-ttu-id="3e8f9-133">GetMAPIObjectType</span><span class="sxs-lookup"><span data-stu-id="3e8f9-133">GetMAPIObjectType</span></span>  <br/> |<span data-ttu-id="3e8f9-134">MFCMAPI использует метод **HrGetOneProp** для получения типа объекта.</span><span class="sxs-lookup"><span data-stu-id="3e8f9-134">MFCMAPI uses the **HrGetOneProp** method to retrieve the type of an object.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="3e8f9-135">См. также</span><span class="sxs-lookup"><span data-stu-id="3e8f9-135">See also</span></span>



[<span data-ttu-id="3e8f9-136">Mfcmapi (en) � �������� ������� ����</span><span class="sxs-lookup"><span data-stu-id="3e8f9-136">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

