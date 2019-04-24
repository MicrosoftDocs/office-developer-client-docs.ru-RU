---
title: Функция CEILING
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251405
localization_priority: Normal
ms.assetid: 1a8d6d48-7ae3-5483-28d2-5b1706088a53
description: Округляет число от 0 (нуля) до следующего экземпляра множителя. Если не указано значение Multiple, число округляется от 0 до следующего целого числа.
ms.openlocfilehash: 449f17d1b68c116cccb2635723a3f6277d0ac2a9
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32337228"
---
# <a name="ceiling-function"></a><span data-ttu-id="7afbf-104">Функция CEILING</span><span class="sxs-lookup"><span data-stu-id="7afbf-104">CEILING Function</span></span>

<span data-ttu-id="7afbf-105">Округляет число от 0 (нуля) до следующего экземпляра множителя. __</span><span class="sxs-lookup"><span data-stu-id="7afbf-105">Rounds a number away from 0 (zero) to the next instance of  _multiple_.</span></span> <span data-ttu-id="7afbf-106">Если не указано значение _Multiple_ , число округляется от 0 до следующего целого числа.</span><span class="sxs-lookup"><span data-stu-id="7afbf-106">If  _multiple_ is not specified, the number rounds away from 0 to the next integer.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="7afbf-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="7afbf-107">Syntax</span></span>

<span data-ttu-id="7afbf-108">CEILING (\* \* *число* \* \* \* \* \* *несколько* \* \*)</span><span class="sxs-lookup"><span data-stu-id="7afbf-108">CEILING(\*\* *number* \*\*, \*\* *multiple* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="7afbf-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="7afbf-109">Parameters</span></span>

|<span data-ttu-id="7afbf-110">**Имя**</span><span class="sxs-lookup"><span data-stu-id="7afbf-110">**Name**</span></span>|<span data-ttu-id="7afbf-111">**Необходимость**</span><span class="sxs-lookup"><span data-stu-id="7afbf-111">**Required/Optional**</span></span>|<span data-ttu-id="7afbf-112">**Тип данных**</span><span class="sxs-lookup"><span data-stu-id="7afbf-112">**Data Type**</span></span>|<span data-ttu-id="7afbf-113">**Описание**</span><span class="sxs-lookup"><span data-stu-id="7afbf-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="7afbf-114">_число_</span><span class="sxs-lookup"><span data-stu-id="7afbf-114">_number_</span></span> <br/> |<span data-ttu-id="7afbf-115">Обязательный</span><span class="sxs-lookup"><span data-stu-id="7afbf-115">Required</span></span>  <br/> |<span data-ttu-id="7afbf-116">**Number**</span><span class="sxs-lookup"><span data-stu-id="7afbf-116">**Number**</span></span> <br/> |<span data-ttu-id="7afbf-117">Округляемое число.</span><span class="sxs-lookup"><span data-stu-id="7afbf-117">The number to round.</span></span>  <br/> |
| <span data-ttu-id="7afbf-118">_сразу_</span><span class="sxs-lookup"><span data-stu-id="7afbf-118">_multiple_</span></span> <br/> |<span data-ttu-id="7afbf-119">Обязательный</span><span class="sxs-lookup"><span data-stu-id="7afbf-119">Required</span></span>  <br/> |<span data-ttu-id="7afbf-120">**Number**</span><span class="sxs-lookup"><span data-stu-id="7afbf-120">**Number**</span></span> <br/> |<span data-ttu-id="7afbf-121">Точность до.</span><span class="sxs-lookup"><span data-stu-id="7afbf-121">The multiple to round to.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="7afbf-122">Комментарии</span><span class="sxs-lookup"><span data-stu-id="7afbf-122">Remarks</span></span>

 <span data-ttu-id="7afbf-123">_Число_ и _множество_ должны иметь одинаковые знаки или #NUM!</span><span class="sxs-lookup"><span data-stu-id="7afbf-123">_Number_ and  _multiple_ must have the same signs, or a #NUM!</span></span> <span data-ttu-id="7afbf-124">возвращается ошибка.</span><span class="sxs-lookup"><span data-stu-id="7afbf-124">error is returned.</span></span> <span data-ttu-id="7afbf-125">Если один или _несколько_ _чисел_ не могут быть преобразованы в значение, то #VALUE!</span><span class="sxs-lookup"><span data-stu-id="7afbf-125">If either  _number_ or  _multiple_ cannot be converted to a value, a #VALUE!</span></span> <span data-ttu-id="7afbf-126">возвращается ошибка.</span><span class="sxs-lookup"><span data-stu-id="7afbf-126">error is returned.</span></span> <span data-ttu-id="7afbf-127">Если один или _несколько_ _чисел_ имеют значение 0, результат равен 0.</span><span class="sxs-lookup"><span data-stu-id="7afbf-127">If either  _number_ or  _multiple_ is 0, the result is 0.</span></span> 
  
## <a name="example-1"></a><span data-ttu-id="7afbf-128">Пример 1</span><span class="sxs-lookup"><span data-stu-id="7afbf-128">Example 1</span></span>

<span data-ttu-id="7afbf-129">CEILING (3.7)</span><span class="sxs-lookup"><span data-stu-id="7afbf-129">CEILING(3.7)</span></span>
  
<span data-ttu-id="7afbf-130">Возвращает 4</span><span class="sxs-lookup"><span data-stu-id="7afbf-130">Returns 4</span></span>
  
## <a name="example-2"></a><span data-ttu-id="7afbf-131">Пример 2</span><span class="sxs-lookup"><span data-stu-id="7afbf-131">Example 2</span></span>

<span data-ttu-id="7afbf-132">CEILING (-3,7)</span><span class="sxs-lookup"><span data-stu-id="7afbf-132">CEILING(-3.7)</span></span>
  
<span data-ttu-id="7afbf-133">Возвращает значение — 4</span><span class="sxs-lookup"><span data-stu-id="7afbf-133">Returns -4</span></span>
  
## <a name="example-3"></a><span data-ttu-id="7afbf-134">Пример 3</span><span class="sxs-lookup"><span data-stu-id="7afbf-134">Example 3</span></span>

<span data-ttu-id="7afbf-135">CEILING (3.7, 0,25)</span><span class="sxs-lookup"><span data-stu-id="7afbf-135">CEILING(3.7, 0.25)</span></span>
  
<span data-ttu-id="7afbf-136">Возвращает 3,75</span><span class="sxs-lookup"><span data-stu-id="7afbf-136">Returns 3.75</span></span>
  

