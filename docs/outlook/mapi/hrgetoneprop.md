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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32347840"
---
# <a name="hrgetoneprop"></a><span data-ttu-id="1bfd2-103">HrGetOneProp</span><span class="sxs-lookup"><span data-stu-id="1bfd2-103">HrGetOneProp</span></span>

  
  
<span data-ttu-id="1bfd2-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1bfd2-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1bfd2-105">Извлекает значение одного свойства из интерфейса свойства, то есть интерфейс, производный от [IMAPIProp](imapipropiunknown.md).</span><span class="sxs-lookup"><span data-stu-id="1bfd2-105">Retrieves the value of a single property from a property interface, that is, an interface derived from [IMAPIProp](imapipropiunknown.md).</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="1bfd2-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="1bfd2-106">Header file:</span></span>  <br/> |<span data-ttu-id="1bfd2-107">Мапиутил. h</span><span class="sxs-lookup"><span data-stu-id="1bfd2-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="1bfd2-108">Реализовано в:</span><span class="sxs-lookup"><span data-stu-id="1bfd2-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="1bfd2-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="1bfd2-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="1bfd2-110">Вызывающая сторона:</span><span class="sxs-lookup"><span data-stu-id="1bfd2-110">Called by:</span></span>  <br/> |<span data-ttu-id="1bfd2-111">Клиентские приложения и поставщики услуг</span><span class="sxs-lookup"><span data-stu-id="1bfd2-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
HrGetOneProp(
  LPMAPIPROP pmp,
  ULONG ulPropTag,
  LPSPropValue FAR * ppprop
);
```

## <a name="parameters"></a><span data-ttu-id="1bfd2-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="1bfd2-112">Parameters</span></span>

 <span data-ttu-id="1bfd2-113">_ПМП_</span><span class="sxs-lookup"><span data-stu-id="1bfd2-113">_pmp_</span></span>
  
> <span data-ttu-id="1bfd2-114">возврата Указатель на интерфейс [IMAPIProp](imapipropiunknown.md) , из которого извлекается значение свойства.</span><span class="sxs-lookup"><span data-stu-id="1bfd2-114">[in] Pointer to the [IMAPIProp](imapipropiunknown.md) interface from which the property value is to be retrieved.</span></span> 
    
 <span data-ttu-id="1bfd2-115">_Улпроптаг_</span><span class="sxs-lookup"><span data-stu-id="1bfd2-115">_ulPropTag_</span></span>
  
> <span data-ttu-id="1bfd2-116">возврата Тег свойства для извлекаемого свойства.</span><span class="sxs-lookup"><span data-stu-id="1bfd2-116">[in] Property tag of the property to be retrieved.</span></span> 
    
 <span data-ttu-id="1bfd2-117">_пппроп_</span><span class="sxs-lookup"><span data-stu-id="1bfd2-117">_ppprop_</span></span>
  
> <span data-ttu-id="1bfd2-118">вышли Указатель на указатель на возвращенную структуру [спропвалуе](spropvalue.md) , определяющую полученное значение свойства.</span><span class="sxs-lookup"><span data-stu-id="1bfd2-118">[out] Pointer to a pointer to the returned [SPropValue](spropvalue.md) structure defining the retrieved property value.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="1bfd2-119">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="1bfd2-119">Return value</span></span>

<span data-ttu-id="1bfd2-120">МАПИ_Е_НОТ_ФАУНД</span><span class="sxs-lookup"><span data-stu-id="1bfd2-120">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="1bfd2-121">Запрошенное свойство недоступно для указанного интерфейса.</span><span class="sxs-lookup"><span data-stu-id="1bfd2-121">The requested property is not available from the specified interface.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="1bfd2-122">Примечания</span><span class="sxs-lookup"><span data-stu-id="1bfd2-122">Remarks</span></span>

<span data-ttu-id="1bfd2-123">В отличие от метода [IMAPIProp::](imapiprop-getprops.md) /Props, функция **хржетонепроп** никогда не возвращает какое бы то ни было предупреждение.</span><span class="sxs-lookup"><span data-stu-id="1bfd2-123">Unlike the [IMAPIProp::GetProps](imapiprop-getprops.md) method, the **HrGetOneProp** function never returns any warning.</span></span> <span data-ttu-id="1bfd2-124">Так как извлекает только одно свойство, оно просто завершается или завершается с ошибкой.</span><span class="sxs-lookup"><span data-stu-id="1bfd2-124">Because it retrieves only one property, it simply either succeeds or fails.</span></span> <span data-ttu-id="1bfd2-125">Для получения нескольких свойств выполняется быстрее \*\*\*\* .</span><span class="sxs-lookup"><span data-stu-id="1bfd2-125">For retrieving multiple properties, **GetProps** is faster.</span></span> 
  
<span data-ttu-id="1bfd2-126">Вы можете задать или изменить одно свойство с помощью функции [хрсетонепроп](hrsetoneprop.md) .</span><span class="sxs-lookup"><span data-stu-id="1bfd2-126">You can set or change a single property with the [HrSetOneProp](hrsetoneprop.md) function.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="1bfd2-127">Справочные материалы по MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="1bfd2-127">MFCMAPI reference</span></span>

<span data-ttu-id="1bfd2-128">Пример кода MFCMAPI указан в приведенной ниже таблице.</span><span class="sxs-lookup"><span data-stu-id="1bfd2-128">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="1bfd2-129">**Файл**</span><span class="sxs-lookup"><span data-stu-id="1bfd2-129">**File**</span></span>|<span data-ttu-id="1bfd2-130">**Функция**</span><span class="sxs-lookup"><span data-stu-id="1bfd2-130">**Function**</span></span>|<span data-ttu-id="1bfd2-131">**Примечание**</span><span class="sxs-lookup"><span data-stu-id="1bfd2-131">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="1bfd2-132">Мапифунктионс. cpp</span><span class="sxs-lookup"><span data-stu-id="1bfd2-132">MAPIFunctions.cpp</span></span>  <br/> |<span data-ttu-id="1bfd2-133">Жетмапиобжекттипе</span><span class="sxs-lookup"><span data-stu-id="1bfd2-133">GetMAPIObjectType</span></span>  <br/> |<span data-ttu-id="1bfd2-134">MFCMAPI использует метод **хржетонепроп** для получения типа объекта.</span><span class="sxs-lookup"><span data-stu-id="1bfd2-134">MFCMAPI uses the **HrGetOneProp** method to retrieve the type of an object.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="1bfd2-135">См. также</span><span class="sxs-lookup"><span data-stu-id="1bfd2-135">See also</span></span>



[<span data-ttu-id="1bfd2-136">Mfcmapi (en) � �������� ������� ����</span><span class="sxs-lookup"><span data-stu-id="1bfd2-136">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

