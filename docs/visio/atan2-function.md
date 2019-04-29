---
title: Функция ATAN2
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251397
localization_priority: Normal
ms.assetid: 524278fb-196e-9cf9-e27b-d03642beeee4
description: Возвращает угол между вектором, представленным x, y и направлением оси x. Результатом является число в текущей единице измерения для углов.
ms.openlocfilehash: 906c024f2a78d6e11c1bbf770c14d04299cadca8
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436484"
---
# <a name="atan2-function"></a><span data-ttu-id="a52fe-104">Функция ATAN2</span><span class="sxs-lookup"><span data-stu-id="a52fe-104">ATAN2 Function</span></span>

<span data-ttu-id="a52fe-105">Возвращает угол между вектором, представленным *x, y* и направлением оси *x* .</span><span class="sxs-lookup"><span data-stu-id="a52fe-105">Returns the angle between the vector represented by  *x,y*  and the direction of the  *x*  -axis.</span></span> <span data-ttu-id="a52fe-106">Результатом является число в текущей единице измерения для углов.</span><span class="sxs-lookup"><span data-stu-id="a52fe-106">The result is a number in the current unit of measure for angles.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="a52fe-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a52fe-107">Syntax</span></span>

<span data-ttu-id="a52fe-108">ATAN2 (\* \* *y* \* \*, \* \* *x* \* \*)</span><span class="sxs-lookup"><span data-stu-id="a52fe-108">ATAN2(\*\* *y* \*\*, \*\* *x* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="a52fe-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="a52fe-109">Parameters</span></span>

|<span data-ttu-id="a52fe-110">**Имя**</span><span class="sxs-lookup"><span data-stu-id="a52fe-110">**Name**</span></span>|<span data-ttu-id="a52fe-111">**Необходимость**</span><span class="sxs-lookup"><span data-stu-id="a52fe-111">**Required/Optional**</span></span>|<span data-ttu-id="a52fe-112">**Тип данных**</span><span class="sxs-lookup"><span data-stu-id="a52fe-112">**Data Type**</span></span>|<span data-ttu-id="a52fe-113">**Описание**</span><span class="sxs-lookup"><span data-stu-id="a52fe-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="a52fe-114">_y_</span><span class="sxs-lookup"><span data-stu-id="a52fe-114">_y_</span></span> <br/> |<span data-ttu-id="a52fe-115">Обязательный</span><span class="sxs-lookup"><span data-stu-id="a52fe-115">Required</span></span>  <br/> |<span data-ttu-id="a52fe-116">**Числовой**</span><span class="sxs-lookup"><span data-stu-id="a52fe-116">**Numeric**</span></span> <br/> |<span data-ttu-id="a52fe-117">Значение _y_точки.</span><span class="sxs-lookup"><span data-stu-id="a52fe-117">The  _y_-value of the point.</span></span>  <br/> |
| <span data-ttu-id="a52fe-118">_x_</span><span class="sxs-lookup"><span data-stu-id="a52fe-118">_x_</span></span> <br/> |<span data-ttu-id="a52fe-119">Обязательный</span><span class="sxs-lookup"><span data-stu-id="a52fe-119">Required</span></span>  <br/> |<span data-ttu-id="a52fe-120">**Числовой**</span><span class="sxs-lookup"><span data-stu-id="a52fe-120">**Numeric**</span></span> <br/> |<span data-ttu-id="a52fe-121">Значение _x_точки.</span><span class="sxs-lookup"><span data-stu-id="a52fe-121">The  _x_-value of the point.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a52fe-122">Примечания</span><span class="sxs-lookup"><span data-stu-id="a52fe-122">Remarks</span></span>

<span data-ttu-id="a52fe-123">Арктангенс — это угол, который измеряется против положительной оси *x* в строку, пересекающую начало координат (0, 0), и точку, представленную *x* и *y* .</span><span class="sxs-lookup"><span data-stu-id="a52fe-123">The arctangent is the angle measured counterclockwise from the positive  *x*  -axis to a line that intersects the origin (0,0) and the point represented by  *x*  and  *y*  .</span></span> <span data-ttu-id="a52fe-124">В Microsoft Visio ATAN2 (0, 0) возвращает значение 0.</span><span class="sxs-lookup"><span data-stu-id="a52fe-124">In Microsoft Visio, ATAN2(0,0) returns 0.</span></span> <span data-ttu-id="a52fe-125">Чтобы принудительно применить результат ATAN2 к другому измерению в угловом измерении, используйте функцию град или RAD.</span><span class="sxs-lookup"><span data-stu-id="a52fe-125">To force the result of ATAN2 into a different angular measurement, use the DEG or RAD function.</span></span> 
  
<span data-ttu-id="a52fe-126">Функция ATAN2 является функцией функции TAN.</span><span class="sxs-lookup"><span data-stu-id="a52fe-126">The ATAN2 function is the antifunction of the TAN function.</span></span> <span data-ttu-id="a52fe-127">Функция ATAN2 Возвращает угол, угол которого равен *y* . \*\*</span><span class="sxs-lookup"><span data-stu-id="a52fe-127">The ATAN2 function returns the angle whose angle is equal to  *y*  divided by  *x*  .</span></span> <span data-ttu-id="a52fe-128">Если ATAN2 (*y, x*) представляет угол в прямоугольном треугольнике, *y* — "противоположная сторона", а *x* — "смежная сторона", поэтому функцию можно записать как atan2 (противоположную, смежную).</span><span class="sxs-lookup"><span data-stu-id="a52fe-128">If ATAN2(*y,x*) represents an angle in a right triangle,  *y*  is the "opposite side" and  *x*  is the "adjacent side," so the function could be written as ATAN2(opposite,adjacent).</span></span> 
  
## <a name="example-1"></a><span data-ttu-id="a52fe-129">Пример 1</span><span class="sxs-lookup"><span data-stu-id="a52fe-129">Example 1</span></span>

<span data-ttu-id="a52fe-130">ATAN2 (1,25, 2,25)</span><span class="sxs-lookup"><span data-stu-id="a52fe-130">ATAN2(1.25,2.25)</span></span>
  
<span data-ttu-id="a52fe-131">Возвращает 29,0456 град</span><span class="sxs-lookup"><span data-stu-id="a52fe-131">Returns 29.0456 deg</span></span>
  
## <a name="example-2"></a><span data-ttu-id="a52fe-132">Пример 2</span><span class="sxs-lookup"><span data-stu-id="a52fe-132">Example 2</span></span>

<span data-ttu-id="a52fe-133">ATAN2 (1, SQRT (3))</span><span class="sxs-lookup"><span data-stu-id="a52fe-133">ATAN2(1,SQRT(3))</span></span>
  
<span data-ttu-id="a52fe-134">Возвращает 30 градусов</span><span class="sxs-lookup"><span data-stu-id="a52fe-134">Returns 30 deg</span></span>
  
## <a name="example-3"></a><span data-ttu-id="a52fe-135">Пример 3</span><span class="sxs-lookup"><span data-stu-id="a52fe-135">Example 3</span></span>

<span data-ttu-id="a52fe-136">ATAN2 (1, 1)</span><span class="sxs-lookup"><span data-stu-id="a52fe-136">ATAN2(1,1)</span></span>
  
<span data-ttu-id="a52fe-137">Возвращает 45 град</span><span class="sxs-lookup"><span data-stu-id="a52fe-137">Returns 45 deg</span></span>
  

