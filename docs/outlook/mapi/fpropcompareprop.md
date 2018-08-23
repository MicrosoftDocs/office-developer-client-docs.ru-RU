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
ms.openlocfilehash: adccbaf65adec2c517c4890f722198e8262092cb
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22564607"
---
# <a name="fpropcompareprop"></a><span data-ttu-id="b52e4-103">FPropCompareProp</span><span class="sxs-lookup"><span data-stu-id="b52e4-103">FPropCompareProp</span></span>

<span data-ttu-id="b52e4-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b52e4-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b52e4-105">Сравнение двух значений свойств с помощью указанного оператор сравнения.</span><span class="sxs-lookup"><span data-stu-id="b52e4-105">Compares two property values using a specified relational operator.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="b52e4-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="b52e4-106">Header file:</span></span>  <br/> |<span data-ttu-id="b52e4-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="b52e4-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="b52e4-108">Реализованный:</span><span class="sxs-lookup"><span data-stu-id="b52e4-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="b52e4-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="b52e4-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="b52e4-110">Вызывается:</span><span class="sxs-lookup"><span data-stu-id="b52e4-110">Called by:</span></span>  <br/> |<span data-ttu-id="b52e4-111">Клиентские приложения и поставщиков услуг</span><span class="sxs-lookup"><span data-stu-id="b52e4-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
BOOL FPropCompareProp(
  LPSPropValue lpSPropValue1,
  ULONG ulRelOp,
  LPSPropValue lpSPropValue2
);
```

## <a name="parameters"></a><span data-ttu-id="b52e4-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="b52e4-112">Parameters</span></span>

<span data-ttu-id="b52e4-113">_lpSPropValue1_</span><span class="sxs-lookup"><span data-stu-id="b52e4-113">_lpSPropValue1_</span></span>
  
> <span data-ttu-id="b52e4-114">[in] Указатель на структуру [SPropValue](spropvalue.md) определение первое значение свойства для сравнения.</span><span class="sxs-lookup"><span data-stu-id="b52e4-114">[in] Pointer to an [SPropValue](spropvalue.md) structure defining the first property value for comparison.</span></span> 
    
<span data-ttu-id="b52e4-115">_ulRelOp_</span><span class="sxs-lookup"><span data-stu-id="b52e4-115">_ulRelOp_</span></span>
  
> <span data-ttu-id="b52e4-116">[in] Оператор сравнения для использования в сравнении.</span><span class="sxs-lookup"><span data-stu-id="b52e4-116">[in] The relational operator to use in the comparison.</span></span> <span data-ttu-id="b52e4-117">Допустимые значения структуры [SComparePropsRestriction](scomparepropsrestriction.md) см.</span><span class="sxs-lookup"><span data-stu-id="b52e4-117">For allowable values, see the [SComparePropsRestriction](scomparepropsrestriction.md) structure.</span></span> 
    
<span data-ttu-id="b52e4-118">_lpSPropValue2_</span><span class="sxs-lookup"><span data-stu-id="b52e4-118">_lpSPropValue2_</span></span>
  
> <span data-ttu-id="b52e4-119">[in] Указатель на структуру **SPropValue** определение второе значение свойства для сравнения.</span><span class="sxs-lookup"><span data-stu-id="b52e4-119">[in] Pointer to an **SPropValue** structure defining the second property value for comparison.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="b52e4-120">������������ ��������</span><span class="sxs-lookup"><span data-stu-id="b52e4-120">Return value</span></span>

<span data-ttu-id="b52e4-121">TRUE</span><span class="sxs-lookup"><span data-stu-id="b52e4-121">TRUE</span></span> 
  
> <span data-ttu-id="b52e4-122">Значения свойств удовлетворяет указанным отношением.</span><span class="sxs-lookup"><span data-stu-id="b52e4-122">The property values satisfy the specified relation.</span></span> 
    
<span data-ttu-id="b52e4-123">FALSE</span><span class="sxs-lookup"><span data-stu-id="b52e4-123">FALSE</span></span> 
  
> <span data-ttu-id="b52e4-124">Значения свойств не удовлетворяет указанным отношением.</span><span class="sxs-lookup"><span data-stu-id="b52e4-124">The property values do not satisfy the specified relation.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="b52e4-125">Замечания</span><span class="sxs-lookup"><span data-stu-id="b52e4-125">Remarks</span></span>

<span data-ttu-id="b52e4-126">Метод сравнения зависит от типы свойств, указанных в определениях свойство [SPropValue](spropvalue.md) .</span><span class="sxs-lookup"><span data-stu-id="b52e4-126">The comparison method depends on the property types specified in the [SPropValue](spropvalue.md) property definitions.</span></span> <span data-ttu-id="b52e4-127">Функции **FPropCompareProp** и [FPropContainsProp](fpropcontainsprop.md) можно использовать для подготовки ограничения для создания таблицы.</span><span class="sxs-lookup"><span data-stu-id="b52e4-127">The **FPropCompareProp** and [FPropContainsProp](fpropcontainsprop.md) functions can be used to prepare restrictions for generating a table.</span></span> 
  
<span data-ttu-id="b52e4-128">Порядок сравнения — _lpSPropValue1_, _ ulRelOp _, _ lpSPropValue2 _.</span><span class="sxs-lookup"><span data-stu-id="b52e4-128">The order of comparison is  _lpSPropValue1_, _ ulRelOp _, _ lpSPropValue2 _.</span></span> <span data-ttu-id="b52e4-129">Если типы свойств значений свойств, которые будут сравниваться не совпадают, функция **FPropCompareProp** возвращает значение FALSE.</span><span class="sxs-lookup"><span data-stu-id="b52e4-129">If the property types of the property values to be compared do not match, the **FPropCompareProp** function returns FALSE.</span></span> 
  

