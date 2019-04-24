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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357437"
---
# <a name="lpropcompareprop"></a><span data-ttu-id="6ff72-103">LPropCompareProp</span><span class="sxs-lookup"><span data-stu-id="6ff72-103">LPropCompareProp</span></span>

  
  
<span data-ttu-id="6ff72-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6ff72-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6ff72-105">Сравнивает два значения свойства, чтобы определить, равны ли они.</span><span class="sxs-lookup"><span data-stu-id="6ff72-105">Compares two property values to determine whether they are equal.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="6ff72-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="6ff72-106">Header file:</span></span>  <br/> |<span data-ttu-id="6ff72-107">Мапиутил. h</span><span class="sxs-lookup"><span data-stu-id="6ff72-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="6ff72-108">Реализовано в:</span><span class="sxs-lookup"><span data-stu-id="6ff72-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="6ff72-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="6ff72-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="6ff72-110">Вызывающая сторона:</span><span class="sxs-lookup"><span data-stu-id="6ff72-110">Called by:</span></span>  <br/> |<span data-ttu-id="6ff72-111">Клиентские приложения и поставщики услуг</span><span class="sxs-lookup"><span data-stu-id="6ff72-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
LONG LPropCompareProp(
  LPSPropValue lpSPropValueA,
  LPSPropValue lpSPropValueB
);
```

## <a name="parameters"></a><span data-ttu-id="6ff72-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="6ff72-112">Parameters</span></span>

 <span data-ttu-id="6ff72-113">_Лпспропвалуеа_</span><span class="sxs-lookup"><span data-stu-id="6ff72-113">_lpSPropValueA_</span></span>
  
> <span data-ttu-id="6ff72-114">возврата Указатель на структуру [спропвалуе](spropvalue.md) , определяющую значение первого свойства, которое требуется сравнить.</span><span class="sxs-lookup"><span data-stu-id="6ff72-114">[in] Pointer to an [SPropValue](spropvalue.md) structure defining the first property value to be compared.</span></span> 
    
 <span data-ttu-id="6ff72-115">_Лпспропвалуеб_</span><span class="sxs-lookup"><span data-stu-id="6ff72-115">_lpSPropValueB_</span></span>
  
> <span data-ttu-id="6ff72-116">возврата Указатель на структуру **спропвалуе** , определяющую второе значение свойства, которое требуется сравнить.</span><span class="sxs-lookup"><span data-stu-id="6ff72-116">[in] Pointer to an **SPropValue** structure defining the second property value to be compared.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="6ff72-117">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="6ff72-117">Return value</span></span>

 <span data-ttu-id="6ff72-118">**Лпропкомпарепроп** возвращает одно из следующих значений для большинства типов свойств:</span><span class="sxs-lookup"><span data-stu-id="6ff72-118">**LPropCompareProp** returns one of the following values for most property types:</span></span> 
  
- <span data-ttu-id="6ff72-119">Меньше нуля, если значение, указанное параметром _лпспропвалуеа_ , меньше, чем указано в параметре _лпспропвалуеб_ .</span><span class="sxs-lookup"><span data-stu-id="6ff72-119">Less than zero if the value indicated by the  _lpSPropValueA_ parameter is less than that indicated by the  _lpSPropValueB_ parameter.</span></span> 
    
- <span data-ttu-id="6ff72-120">Больше нуля, если значение, указанное в _лпспропвалуеа_ , больше, чем указано в _лпспропвалуеб_.</span><span class="sxs-lookup"><span data-stu-id="6ff72-120">Greater than zero if the value indicated by  _lpSPropValueA_ is greater than that indicated by  _lpSPropValueB_.</span></span>
    
- <span data-ttu-id="6ff72-121">Ноль, если значение, заданное параметром _лпспропвалуеа_ , равно значению, указанному в параметре _лпспропвалуеб_.</span><span class="sxs-lookup"><span data-stu-id="6ff72-121">Zero if the value indicated by  _lpSPropValueA_ equals the value indicated by  _lpSPropValueB_.</span></span> 
    
<span data-ttu-id="6ff72-122">Для типов свойств, не имеющих внутреннего упорядочения, таких как логические типы или типы ошибок, функция **лпропкомпарепроп** возвращает неопределенное значение, если два значения свойства не равны.</span><span class="sxs-lookup"><span data-stu-id="6ff72-122">For property types that have no intrinsic ordering, such as Boolean or error types, the **LPropCompareProp** function returns an undefined value if the two property values are not equal.</span></span> <span data-ttu-id="6ff72-123">Это неопределенное значение ненулевое и согласованное в вызовах.</span><span class="sxs-lookup"><span data-stu-id="6ff72-123">This undefined value is nonzero and consistent across calls.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="6ff72-124">Примечания</span><span class="sxs-lookup"><span data-stu-id="6ff72-124">Remarks</span></span>

<span data-ttu-id="6ff72-125">Используйте функцию **лпропкомпарепроп** только в том случае, если типы двух сравниваемых свойств совпадают.</span><span class="sxs-lookup"><span data-stu-id="6ff72-125">Use the **LPropCompareProp** function only if the types of the two properties to be compared are the same.</span></span> 
  
<span data-ttu-id="6ff72-126">Перед вызовом **лпропкомпарепроп**клиентское приложение или поставщик услуг сначала должны получить свойства для сравнения с вызовом метода [IMAPIProp::](imapiprop-getprops.md) .</span><span class="sxs-lookup"><span data-stu-id="6ff72-126">Before calling **LPropCompareProp**, a client application or service provider must first retrieve the properties for comparison with a call to the [IMAPIProp::GetProps](imapiprop-getprops.md) method.</span></span> <span data-ttu-id="6ff72-127">Когда клиент или поставщик вызывает **лпропкомпарепроп**, функция сначала проверяет теги свойств, чтобы убедиться, что сравнение значений свойств является допустимым.</span><span class="sxs-lookup"><span data-stu-id="6ff72-127">When a client or provider calls **LPropCompareProp**, the function first examines the property tags to make sure that the comparison of property values is valid.</span></span> <span data-ttu-id="6ff72-128">Затем функция сравнивает значения свойств, возвращая соответствующее значение.</span><span class="sxs-lookup"><span data-stu-id="6ff72-128">The function then compares the property values, returning an appropriate value.</span></span> 
  
<span data-ttu-id="6ff72-129">Если значения свойств не совпадают, **лпропкомпарепроп** определяет, какой из них больше.</span><span class="sxs-lookup"><span data-stu-id="6ff72-129">If the property values are unequal, **LPropCompareProp** determines which one is the greater.</span></span> <span data-ttu-id="6ff72-130">Свойства, сравниваемые **лпропкомпарепроп** , не обязательно должны принадлежать одному и тому же объекту.</span><span class="sxs-lookup"><span data-stu-id="6ff72-130">The properties that **LPropCompareProp** compares do not have to belong to the same object.</span></span> 
  

