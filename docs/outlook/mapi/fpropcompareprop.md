---
title: FPropCompareProp
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.FPropCompareProp
api_type:
- COM
ms.assetid: 17cb53c4-7154-4a4e-b4ec-de720fa055cb
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 7726811467324242037ec11a69ae0b1b123d7f21
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33427159"
---
# <a name="fpropcompareprop"></a><span data-ttu-id="8dd9c-103">FPropCompareProp</span><span class="sxs-lookup"><span data-stu-id="8dd9c-103">FPropCompareProp</span></span>

<span data-ttu-id="8dd9c-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8dd9c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8dd9c-105">Сравнивает два значения свойств с помощью указанного реляционного оператора.</span><span class="sxs-lookup"><span data-stu-id="8dd9c-105">Compares two property values using a specified relational operator.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="8dd9c-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="8dd9c-106">Header file:</span></span>  <br/> |<span data-ttu-id="8dd9c-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="8dd9c-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="8dd9c-108">Реализовано в:</span><span class="sxs-lookup"><span data-stu-id="8dd9c-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="8dd9c-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="8dd9c-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="8dd9c-110">Вызывающая сторона:</span><span class="sxs-lookup"><span data-stu-id="8dd9c-110">Called by:</span></span>  <br/> |<span data-ttu-id="8dd9c-111">Клиентские приложения и поставщики услуг</span><span class="sxs-lookup"><span data-stu-id="8dd9c-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
BOOL FPropCompareProp(
  LPSPropValue lpSPropValue1,
  ULONG ulRelOp,
  LPSPropValue lpSPropValue2
);
```

## <a name="parameters"></a><span data-ttu-id="8dd9c-112">Parameters</span><span class="sxs-lookup"><span data-stu-id="8dd9c-112">Parameters</span></span>

<span data-ttu-id="8dd9c-113">_lpSPropValue1_</span><span class="sxs-lookup"><span data-stu-id="8dd9c-113">_lpSPropValue1_</span></span>
  
> <span data-ttu-id="8dd9c-114">[in] Указатель на [структуру SPropValue,](spropvalue.md) определяющей первое значение свойства для сравнения.</span><span class="sxs-lookup"><span data-stu-id="8dd9c-114">[in] Pointer to an [SPropValue](spropvalue.md) structure defining the first property value for comparison.</span></span> 
    
<span data-ttu-id="8dd9c-115">_ulRelOp_</span><span class="sxs-lookup"><span data-stu-id="8dd9c-115">_ulRelOp_</span></span>
  
> <span data-ttu-id="8dd9c-116">[in] Реляционный оператор для сравнения.</span><span class="sxs-lookup"><span data-stu-id="8dd9c-116">[in] The relational operator to use in the comparison.</span></span> <span data-ttu-id="8dd9c-117">Допустимые значения см. в структуре [SComparePropsRestriction.](scomparepropsrestriction.md)</span><span class="sxs-lookup"><span data-stu-id="8dd9c-117">For allowable values, see the [SComparePropsRestriction](scomparepropsrestriction.md) structure.</span></span> 
    
<span data-ttu-id="8dd9c-118">_lpSPropValue2_</span><span class="sxs-lookup"><span data-stu-id="8dd9c-118">_lpSPropValue2_</span></span>
  
> <span data-ttu-id="8dd9c-119">[in] Указатель на **структуру SPropValue,** определяющей второе значение свойства для сравнения.</span><span class="sxs-lookup"><span data-stu-id="8dd9c-119">[in] Pointer to an **SPropValue** structure defining the second property value for comparison.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="8dd9c-120">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="8dd9c-120">Return value</span></span>

<span data-ttu-id="8dd9c-121">TRUE</span><span class="sxs-lookup"><span data-stu-id="8dd9c-121">TRUE</span></span> 
  
> <span data-ttu-id="8dd9c-122">Значения свойств удовлетворяют указанному отношению.</span><span class="sxs-lookup"><span data-stu-id="8dd9c-122">The property values satisfy the specified relation.</span></span> 
    
<span data-ttu-id="8dd9c-123">FALSE</span><span class="sxs-lookup"><span data-stu-id="8dd9c-123">FALSE</span></span> 
  
> <span data-ttu-id="8dd9c-124">Значения свойств не удовлетворяют указанному отношению.</span><span class="sxs-lookup"><span data-stu-id="8dd9c-124">The property values do not satisfy the specified relation.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="8dd9c-125">Примечания</span><span class="sxs-lookup"><span data-stu-id="8dd9c-125">Remarks</span></span>

<span data-ttu-id="8dd9c-126">Метод сравнения зависит от типов свойств, указанных в [определениях свойств SPropValue.](spropvalue.md)</span><span class="sxs-lookup"><span data-stu-id="8dd9c-126">The comparison method depends on the property types specified in the [SPropValue](spropvalue.md) property definitions.</span></span> <span data-ttu-id="8dd9c-127">Функции **FPropCompareProp** и [FPropContainsProp](fpropcontainsprop.md) можно использовать для подготовки ограничений для создания таблицы.</span><span class="sxs-lookup"><span data-stu-id="8dd9c-127">The **FPropCompareProp** and [FPropContainsProp](fpropcontainsprop.md) functions can be used to prepare restrictions for generating a table.</span></span> 
  
<span data-ttu-id="8dd9c-128">Порядок сравнения  _lpSPropValue1_, _ ulRelOp _, _ lpSPropValue2 _.</span><span class="sxs-lookup"><span data-stu-id="8dd9c-128">The order of comparison is  _lpSPropValue1_, _ ulRelOp _, _ lpSPropValue2 _.</span></span> <span data-ttu-id="8dd9c-129">Если сравниваемые типы свойств не совпадают, функция **FPropCompareProp** возвращает FALSE.</span><span class="sxs-lookup"><span data-stu-id="8dd9c-129">If the property types of the property values to be compared do not match, the **FPropCompareProp** function returns FALSE.</span></span> 
  

