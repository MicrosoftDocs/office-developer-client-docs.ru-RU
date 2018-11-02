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
ms.openlocfilehash: 0985ed0c5d4482bb22f46bdc9198afc343c61e5f
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22565538"
---
# <a name="lpropcompareprop"></a><span data-ttu-id="ff98c-103">LPropCompareProp</span><span class="sxs-lookup"><span data-stu-id="ff98c-103">LPropCompareProp</span></span>

  
  
<span data-ttu-id="ff98c-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ff98c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ff98c-105">Сравнивает два значения свойств, чтобы определить, является ли они равны.</span><span class="sxs-lookup"><span data-stu-id="ff98c-105">Compares two property values to determine whether they are equal.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="ff98c-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="ff98c-106">Header file:</span></span>  <br/> |<span data-ttu-id="ff98c-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="ff98c-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="ff98c-108">Реализовано в:</span><span class="sxs-lookup"><span data-stu-id="ff98c-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="ff98c-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="ff98c-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="ff98c-110">Вызывающая сторона:</span><span class="sxs-lookup"><span data-stu-id="ff98c-110">Called by:</span></span>  <br/> |<span data-ttu-id="ff98c-111">Клиентские приложения и поставщиков услуг</span><span class="sxs-lookup"><span data-stu-id="ff98c-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
LONG LPropCompareProp(
  LPSPropValue lpSPropValueA,
  LPSPropValue lpSPropValueB
);
```

## <a name="parameters"></a><span data-ttu-id="ff98c-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="ff98c-112">Parameters</span></span>

 <span data-ttu-id="ff98c-113">_lpSPropValueA_</span><span class="sxs-lookup"><span data-stu-id="ff98c-113">_lpSPropValueA_</span></span>
  
> <span data-ttu-id="ff98c-114">[in] Указатель на структуру [SPropValue](spropvalue.md) определение первое значение свойства для сравнения.</span><span class="sxs-lookup"><span data-stu-id="ff98c-114">[in] Pointer to an [SPropValue](spropvalue.md) structure defining the first property value to be compared.</span></span> 
    
 <span data-ttu-id="ff98c-115">_lpSPropValueB_</span><span class="sxs-lookup"><span data-stu-id="ff98c-115">_lpSPropValueB_</span></span>
  
> <span data-ttu-id="ff98c-116">[in] Указатель на структуру **SPropValue** определение второе значение свойства для сравнения.</span><span class="sxs-lookup"><span data-stu-id="ff98c-116">[in] Pointer to an **SPropValue** structure defining the second property value to be compared.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="ff98c-117">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="ff98c-117">Return value</span></span>

 <span data-ttu-id="ff98c-118">**LPropCompareProp** возвращает одно из следующих значений для большинства типов свойств:</span><span class="sxs-lookup"><span data-stu-id="ff98c-118">**LPropCompareProp** returns one of the following values for most property types:</span></span> 
  
- <span data-ttu-id="ff98c-119">Меньше нуля Если значение указанный в параметре параметр _lpSPropValueA_ меньше значения, указанного параметром _lpSPropValueB_ .</span><span class="sxs-lookup"><span data-stu-id="ff98c-119">Less than zero if the value indicated by the  _lpSPropValueA_ parameter is less than that indicated by the  _lpSPropValueB_ parameter.</span></span> 
    
- <span data-ttu-id="ff98c-120">Больше нуля, если значение указанный в параметре _lpSPropValueA_ больше, чем, указанный в параметре _lpSPropValueB_.</span><span class="sxs-lookup"><span data-stu-id="ff98c-120">Greater than zero if the value indicated by  _lpSPropValueA_ is greater than that indicated by  _lpSPropValueB_.</span></span>
    
- <span data-ttu-id="ff98c-121">Ноль, если значение указанный в параметре _lpSPropValueA_ равно значению, указанный в параметре _lpSPropValueB_.</span><span class="sxs-lookup"><span data-stu-id="ff98c-121">Zero if the value indicated by  _lpSPropValueA_ equals the value indicated by  _lpSPropValueB_.</span></span> 
    
<span data-ttu-id="ff98c-122">Для типы свойств, которые имеют встроенные порядок не, такие как логическое значение или типы ошибок функция **LPropCompareProp** возвращает значение undefined, если два значения не равны.</span><span class="sxs-lookup"><span data-stu-id="ff98c-122">For property types that have no intrinsic ordering, such as Boolean or error types, the **LPropCompareProp** function returns an undefined value if the two property values are not equal.</span></span> <span data-ttu-id="ff98c-123">Это значение undefined значение отличное от нуля и согласованные вызовах.</span><span class="sxs-lookup"><span data-stu-id="ff98c-123">This undefined value is nonzero and consistent across calls.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="ff98c-124">Примечания</span><span class="sxs-lookup"><span data-stu-id="ff98c-124">Remarks</span></span>

<span data-ttu-id="ff98c-125">Используйте функцию **LPropCompareProp** только в том случае, если типы два свойства, которые нужно сравнить, совпадают.</span><span class="sxs-lookup"><span data-stu-id="ff98c-125">Use the **LPropCompareProp** function only if the types of the two properties to be compared are the same.</span></span> 
  
<span data-ttu-id="ff98c-126">До вызова метода **LPropCompareProp**, клиентское приложение или поставщик услуг необходимо сначала получить свойства для сравнения с помощью вызова метода [IMAPIProp::GetProps](imapiprop-getprops.md) .</span><span class="sxs-lookup"><span data-stu-id="ff98c-126">Before calling **LPropCompareProp**, a client application or service provider must first retrieve the properties for comparison with a call to the [IMAPIProp::GetProps](imapiprop-getprops.md) method.</span></span> <span data-ttu-id="ff98c-127">Когда вызовы клиента или поставщика **LPropCompareProp**, функция сначала проверяет тегов свойств, чтобы убедиться в том, сравнение значений свойств является допустимым.</span><span class="sxs-lookup"><span data-stu-id="ff98c-127">When a client or provider calls **LPropCompareProp**, the function first examines the property tags to make sure that the comparison of property values is valid.</span></span> <span data-ttu-id="ff98c-128">Функция затем сравнивает значения свойств, соответствующие значения.</span><span class="sxs-lookup"><span data-stu-id="ff98c-128">The function then compares the property values, returning an appropriate value.</span></span> 
  
<span data-ttu-id="ff98c-129">Если значения свойств не равны, **LPropCompareProp** определяет, какой из них более высокой версии.</span><span class="sxs-lookup"><span data-stu-id="ff98c-129">If the property values are unequal, **LPropCompareProp** determines which one is the greater.</span></span> <span data-ttu-id="ff98c-130">Свойства, которые сопоставлены **LPropCompareProp** нет необходимости принадлежащих на тот же объект.</span><span class="sxs-lookup"><span data-stu-id="ff98c-130">The properties that **LPropCompareProp** compares do not have to belong to the same object.</span></span> 
  

