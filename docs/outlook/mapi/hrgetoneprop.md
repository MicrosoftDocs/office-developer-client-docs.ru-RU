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
ms.openlocfilehash: 4dcdce72781669988a0cb15eb9b3a7cd73494bfb
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19808692"
---
# <a name="hrgetoneprop"></a><span data-ttu-id="0ce01-103">HrGetOneProp</span><span class="sxs-lookup"><span data-stu-id="0ce01-103">HrGetOneProp</span></span>

  
  
<span data-ttu-id="0ce01-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="0ce01-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="0ce01-105">Извлекает значения одного свойства из интерфейса свойство, то есть, производные от [IMAPIProp](imapipropiunknown.md)интерфейс.</span><span class="sxs-lookup"><span data-stu-id="0ce01-105">Retrieves the value of a single property from a property interface, that is, an interface derived from [IMAPIProp](imapipropiunknown.md).</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="0ce01-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="0ce01-106">Header file:</span></span>  <br/> |<span data-ttu-id="0ce01-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="0ce01-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="0ce01-108">Реализованный:</span><span class="sxs-lookup"><span data-stu-id="0ce01-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="0ce01-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="0ce01-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="0ce01-110">Вызывается:</span><span class="sxs-lookup"><span data-stu-id="0ce01-110">Called by:</span></span>  <br/> |<span data-ttu-id="0ce01-111">Клиентские приложения и поставщиков услуг</span><span class="sxs-lookup"><span data-stu-id="0ce01-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
HrGetOneProp(
  LPMAPIPROP pmp,
  ULONG ulPropTag,
  LPSPropValue FAR * ppprop
);
```

## <a name="parameters"></a><span data-ttu-id="0ce01-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="0ce01-112">Parameters</span></span>

 <span data-ttu-id="0ce01-113">_pmp_</span><span class="sxs-lookup"><span data-stu-id="0ce01-113">_pmp_</span></span>
  
> <span data-ttu-id="0ce01-114">[in] Указатель на интерфейс [IMAPIProp](imapipropiunknown.md) , из которого выполняется получение значения свойства.</span><span class="sxs-lookup"><span data-stu-id="0ce01-114">[in] Pointer to the [IMAPIProp](imapipropiunknown.md) interface from which the property value is to be retrieved.</span></span> 
    
 <span data-ttu-id="0ce01-115">_ulPropTag_</span><span class="sxs-lookup"><span data-stu-id="0ce01-115">_ulPropTag_</span></span>
  
> <span data-ttu-id="0ce01-116">[in] Свойство tag свойства нужно вернуть.</span><span class="sxs-lookup"><span data-stu-id="0ce01-116">[in] Property tag of the property to be retrieved.</span></span> 
    
 <span data-ttu-id="0ce01-117">_ppprop_</span><span class="sxs-lookup"><span data-stu-id="0ce01-117">_ppprop_</span></span>
  
> <span data-ttu-id="0ce01-118">[out] Указатель на указатель на структуру возвращенные [SPropValue](spropvalue.md) , определяющий значение извлеченное свойство.</span><span class="sxs-lookup"><span data-stu-id="0ce01-118">[out] Pointer to a pointer to the returned [SPropValue](spropvalue.md) structure defining the retrieved property value.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="0ce01-119">������������ ��������</span><span class="sxs-lookup"><span data-stu-id="0ce01-119">Return value</span></span>

<span data-ttu-id="0ce01-120">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="0ce01-120">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="0ce01-121">Свойство недоступен из указанного интерфейса.</span><span class="sxs-lookup"><span data-stu-id="0ce01-121">The requested property is not available from the specified interface.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="0ce01-122">Замечания</span><span class="sxs-lookup"><span data-stu-id="0ce01-122">Remarks</span></span>

<span data-ttu-id="0ce01-123">В отличие от метода [IMAPIProp::GetProps](imapiprop-getprops.md) функция **HrGetOneProp** никогда не возвращает все предупреждения.</span><span class="sxs-lookup"><span data-stu-id="0ce01-123">Unlike the [IMAPIProp::GetProps](imapiprop-getprops.md) method, the **HrGetOneProp** function never returns any warning.</span></span> <span data-ttu-id="0ce01-124">Так как он получает только одно свойство, он просто либо успешного или неудачного завершения.</span><span class="sxs-lookup"><span data-stu-id="0ce01-124">Because it retrieves only one property, it simply either succeeds or fails.</span></span> <span data-ttu-id="0ce01-125">Для получения значений нескольких свойств, **GetProps** выполняется быстрее.</span><span class="sxs-lookup"><span data-stu-id="0ce01-125">For retrieving multiple properties, **GetProps** is faster.</span></span> 
  
<span data-ttu-id="0ce01-126">Можно установить или изменить отдельное свойство с помощью функции [HrSetOneProp](hrsetoneprop.md) .</span><span class="sxs-lookup"><span data-stu-id="0ce01-126">You can set or change a single property with the [HrSetOneProp](hrsetoneprop.md) function.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="0ce01-127">Справочник по mfcmapi (en)</span><span class="sxs-lookup"><span data-stu-id="0ce01-127">MFCMAPI reference</span></span>

<span data-ttu-id="0ce01-128">������ ���� mfcmapi (en) ���������� � ������� ����.</span><span class="sxs-lookup"><span data-stu-id="0ce01-128">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="0ce01-129">**����**</span><span class="sxs-lookup"><span data-stu-id="0ce01-129">**File**</span></span>|<span data-ttu-id="0ce01-130">**�������**</span><span class="sxs-lookup"><span data-stu-id="0ce01-130">**Function**</span></span>|<span data-ttu-id="0ce01-131">**�����������**</span><span class="sxs-lookup"><span data-stu-id="0ce01-131">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="0ce01-132">MAPIFunctions.cpp</span><span class="sxs-lookup"><span data-stu-id="0ce01-132">MAPIFunctions.cpp</span></span>  <br/> |<span data-ttu-id="0ce01-133">GetMAPIObjectType</span><span class="sxs-lookup"><span data-stu-id="0ce01-133">GetMAPIObjectType</span></span>  <br/> |<span data-ttu-id="0ce01-134">Mfcmapi (en) используется метод **HrGetOneProp** для получения типа объекта.</span><span class="sxs-lookup"><span data-stu-id="0ce01-134">MFCMAPI uses the **HrGetOneProp** method to retrieve the type of an object.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="0ce01-135">См. также</span><span class="sxs-lookup"><span data-stu-id="0ce01-135">See also</span></span>



[<span data-ttu-id="0ce01-136">Mfcmapi (en) � �������� ������� ����</span><span class="sxs-lookup"><span data-stu-id="0ce01-136">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

