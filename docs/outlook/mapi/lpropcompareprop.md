---
title: LPropCompareProp
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.LPropCompareProp
api_type:
- COM
ms.assetid: f14ad568-fe45-4875-957d-415d39dc6f28
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 7417ddeb814cafb954d5ab80a6dae771fd0f7a79
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33414615"
---
# <a name="lpropcompareprop"></a><span data-ttu-id="432a9-103">LPropCompareProp</span><span class="sxs-lookup"><span data-stu-id="432a9-103">LPropCompareProp</span></span>

  
  
<span data-ttu-id="432a9-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="432a9-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="432a9-105">Сравнивает два значения свойств, чтобы определить, являются ли они равными.</span><span class="sxs-lookup"><span data-stu-id="432a9-105">Compares two property values to determine whether they are equal.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="432a9-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="432a9-106">Header file:</span></span>  <br/> |<span data-ttu-id="432a9-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="432a9-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="432a9-108">Реализовано в:</span><span class="sxs-lookup"><span data-stu-id="432a9-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="432a9-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="432a9-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="432a9-110">Вызывающая сторона:</span><span class="sxs-lookup"><span data-stu-id="432a9-110">Called by:</span></span>  <br/> |<span data-ttu-id="432a9-111">Клиентские приложения и поставщики услуг</span><span class="sxs-lookup"><span data-stu-id="432a9-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
LONG LPropCompareProp(
  LPSPropValue lpSPropValueA,
  LPSPropValue lpSPropValueB
);
```

## <a name="parameters"></a><span data-ttu-id="432a9-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="432a9-112">Parameters</span></span>

 <span data-ttu-id="432a9-113">_lpSPropValueA_</span><span class="sxs-lookup"><span data-stu-id="432a9-113">_lpSPropValueA_</span></span>
  
> <span data-ttu-id="432a9-114">[in] Указатель на [структуру SPropValue,](spropvalue.md) определяющей первое значение свойства, для который необходимо сравнить.</span><span class="sxs-lookup"><span data-stu-id="432a9-114">[in] Pointer to an [SPropValue](spropvalue.md) structure defining the first property value to be compared.</span></span> 
    
 <span data-ttu-id="432a9-115">_lpSPropValueB_</span><span class="sxs-lookup"><span data-stu-id="432a9-115">_lpSPropValueB_</span></span>
  
> <span data-ttu-id="432a9-116">[in] Указатель на **структуру SPropValue,** определяющее второе значение свойства, для который необходимо сравнить.</span><span class="sxs-lookup"><span data-stu-id="432a9-116">[in] Pointer to an **SPropValue** structure defining the second property value to be compared.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="432a9-117">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="432a9-117">Return value</span></span>

 <span data-ttu-id="432a9-118">**LPropCompareProp** возвращает одно из следующих значений для большинства типов свойств:</span><span class="sxs-lookup"><span data-stu-id="432a9-118">**LPropCompareProp** returns one of the following values for most property types:</span></span> 
  
- <span data-ttu-id="432a9-119">Меньше нуля, если значение параметра _lpSPropValueA_ меньше значения, заданного параметром _lpSPropValueB._</span><span class="sxs-lookup"><span data-stu-id="432a9-119">Less than zero if the value indicated by the  _lpSPropValueA_ parameter is less than that indicated by the  _lpSPropValueB_ parameter.</span></span> 
    
- <span data-ttu-id="432a9-120">Больше нуля, если значение _lpSPropValueA_ больше, чем указано _в lpSPropValueB._</span><span class="sxs-lookup"><span data-stu-id="432a9-120">Greater than zero if the value indicated by  _lpSPropValueA_ is greater than that indicated by  _lpSPropValueB_.</span></span>
    
- <span data-ttu-id="432a9-121">Ноль, если значение _lpSPropValueA_ равно значению, задаваемом _lpSPropValueB._</span><span class="sxs-lookup"><span data-stu-id="432a9-121">Zero if the value indicated by  _lpSPropValueA_ equals the value indicated by  _lpSPropValueB_.</span></span> 
    
<span data-ttu-id="432a9-122">Для типов свойств, которые не имеют внутренней упорядочения, например типа Boolean или ошибок, функция **LPropCompareProp** возвращает неопределенные значения, если значения двух свойств не равны.</span><span class="sxs-lookup"><span data-stu-id="432a9-122">For property types that have no intrinsic ordering, such as Boolean or error types, the **LPropCompareProp** function returns an undefined value if the two property values are not equal.</span></span> <span data-ttu-id="432a9-123">Это неопределяемая величина не является zero и согласована во всех вызовах.</span><span class="sxs-lookup"><span data-stu-id="432a9-123">This undefined value is nonzero and consistent across calls.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="432a9-124">Примечания</span><span class="sxs-lookup"><span data-stu-id="432a9-124">Remarks</span></span>

<span data-ttu-id="432a9-125">Используйте **функцию LPropCompareProp** только в том случае, если типы двух свойств, которые необходимо сравнить, одинаковы.</span><span class="sxs-lookup"><span data-stu-id="432a9-125">Use the **LPropCompareProp** function only if the types of the two properties to be compared are the same.</span></span> 
  
<span data-ttu-id="432a9-126">Перед вызовом **LPropCompareProp** клиентские приложения или поставщик службы должны сначала получить свойства для сравнения с вызовом метода [IMAPIProp::GetProps.](imapiprop-getprops.md)</span><span class="sxs-lookup"><span data-stu-id="432a9-126">Before calling **LPropCompareProp**, a client application or service provider must first retrieve the properties for comparison with a call to the [IMAPIProp::GetProps](imapiprop-getprops.md) method.</span></span> <span data-ttu-id="432a9-127">Когда клиент или поставщик вызывает **LPropCompareProp,** функция сначала проверяет теги свойств, чтобы убедиться, что сравнение значений свойств допустимо.</span><span class="sxs-lookup"><span data-stu-id="432a9-127">When a client or provider calls **LPropCompareProp**, the function first examines the property tags to make sure that the comparison of property values is valid.</span></span> <span data-ttu-id="432a9-128">Затем функция сравнивает значения свойств, возвращая соответствующее значение.</span><span class="sxs-lookup"><span data-stu-id="432a9-128">The function then compares the property values, returning an appropriate value.</span></span> 
  
<span data-ttu-id="432a9-129">Если значения свойств являются несовершенными, **LPropCompareProp** определяет, какая из них больше.</span><span class="sxs-lookup"><span data-stu-id="432a9-129">If the property values are unequal, **LPropCompareProp** determines which one is the greater.</span></span> <span data-ttu-id="432a9-130">Свойства, **сравниваемые с LPropCompareProp,** не должны принадлежать одному объекту.</span><span class="sxs-lookup"><span data-stu-id="432a9-130">The properties that **LPropCompareProp** compares do not have to belong to the same object.</span></span> 
  

