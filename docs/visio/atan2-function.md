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
description: Возвращает угол между вектор, представленное x, y и направление x-оси. Результатом является число в текущей единицы измерения углов.
ms.openlocfilehash: dfd62ce628a3a46ff14b3ffc3f07074a39c66e14
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19813149"
---
# <a name="atan2-function"></a><span data-ttu-id="17683-104">Функция ATAN2</span><span class="sxs-lookup"><span data-stu-id="17683-104">ATAN2 Function</span></span>

<span data-ttu-id="17683-105">Возвращает угол между вектор, представленное *x, y* и направления *x* -оси.</span><span class="sxs-lookup"><span data-stu-id="17683-105">Returns the angle between the vector represented by  *x,y*  and the direction of the  *x*  -axis.</span></span> <span data-ttu-id="17683-106">Результатом является число в текущей единицы измерения углов.</span><span class="sxs-lookup"><span data-stu-id="17683-106">The result is a number in the current unit of measure for angles.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="17683-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="17683-107">Syntax</span></span>

<span data-ttu-id="17683-108">То функция ATAN2 (** *y* **, ** *x* **)</span><span class="sxs-lookup"><span data-stu-id="17683-108">ATAN2(** *y* **, ** *x* ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="17683-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="17683-109">Parameters</span></span>

|<span data-ttu-id="17683-110">**Имя**</span><span class="sxs-lookup"><span data-stu-id="17683-110">**Name**</span></span>|<span data-ttu-id="17683-111">**Обязательный или необязательный**</span><span class="sxs-lookup"><span data-stu-id="17683-111">**Required/Optional**</span></span>|<span data-ttu-id="17683-112">**Тип данных**</span><span class="sxs-lookup"><span data-stu-id="17683-112">**Data Type**</span></span>|<span data-ttu-id="17683-113">**Описание**</span><span class="sxs-lookup"><span data-stu-id="17683-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="17683-114">_y_</span><span class="sxs-lookup"><span data-stu-id="17683-114">_y_</span></span> <br/> |<span data-ttu-id="17683-115">Обязательный</span><span class="sxs-lookup"><span data-stu-id="17683-115">Required</span></span>  <br/> |<span data-ttu-id="17683-116">**Числовой**</span><span class="sxs-lookup"><span data-stu-id="17683-116">**Numeric**</span></span> <br/> |<span data-ttu-id="17683-117">_Y_— значение точки.</span><span class="sxs-lookup"><span data-stu-id="17683-117">The  _y_-value of the point.</span></span>  <br/> |
| <span data-ttu-id="17683-118">_x_</span><span class="sxs-lookup"><span data-stu-id="17683-118">_x_</span></span> <br/> |<span data-ttu-id="17683-119">Обязательный</span><span class="sxs-lookup"><span data-stu-id="17683-119">Required</span></span>  <br/> |<span data-ttu-id="17683-120">**Числовой**</span><span class="sxs-lookup"><span data-stu-id="17683-120">**Numeric**</span></span> <br/> |<span data-ttu-id="17683-121">_X_— значение точки.</span><span class="sxs-lookup"><span data-stu-id="17683-121">The  _x_-value of the point.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="17683-122">Замечания</span><span class="sxs-lookup"><span data-stu-id="17683-122">Remarks</span></span>

<span data-ttu-id="17683-123">Арктангенс — это угол отсчитывается против часовой стрелки от срабатывание *x* -ось в строке, которая с ним координат (0, 0) и точки, представленной *x* и *y* .</span><span class="sxs-lookup"><span data-stu-id="17683-123">The arctangent is the angle measured counterclockwise from the positive  *x*  -axis to a line that intersects the origin (0,0) and the point represented by  *x*  and  *y*  .</span></span> <span data-ttu-id="17683-124">В Microsoft Visio ATAN2(0,0) возвращает значение 0.</span><span class="sxs-lookup"><span data-stu-id="17683-124">In Microsoft Visio, ATAN2(0,0) returns 0.</span></span> <span data-ttu-id="17683-125">Для принудительной результатов то функция ATAN2 в разных угловые измерения, используйте Градусов или RAD функции.</span><span class="sxs-lookup"><span data-stu-id="17683-125">To force the result of ATAN2 into a different angular measurement, use the DEG or RAD function.</span></span> 
  
<span data-ttu-id="17683-126">Функция то функция ATAN2 является antifunction функция TAN.</span><span class="sxs-lookup"><span data-stu-id="17683-126">The ATAN2 function is the antifunction of the TAN function.</span></span> <span data-ttu-id="17683-127">Функция то функция ATAN2 возвращает угол, чьи угол равно *y* , разделенные на *x* .</span><span class="sxs-lookup"><span data-stu-id="17683-127">The ATAN2 function returns the angle whose angle is equal to  *y*  divided by  *x*  .</span></span> <span data-ttu-id="17683-128">Если то функция ATAN2 (*y, x*), представляющее угол в правом треугольник, *y* — это «положительно стороне» и *x* является «рядом с стороне», поэтому функции может быть записано в формате ATAN2(opposite,adjacent).</span><span class="sxs-lookup"><span data-stu-id="17683-128">If ATAN2(*y,x*) represents an angle in a right triangle,  *y*  is the "opposite side" and  *x*  is the "adjacent side," so the function could be written as ATAN2(opposite,adjacent).</span></span> 
  
## <a name="example-1"></a><span data-ttu-id="17683-129">Пример 1</span><span class="sxs-lookup"><span data-stu-id="17683-129">Example 1</span></span>

<span data-ttu-id="17683-130">ATAN2(1.25,2.25)</span><span class="sxs-lookup"><span data-stu-id="17683-130">ATAN2(1.25,2.25)</span></span>
  
<span data-ttu-id="17683-131">Возвращает 29.0456 градусов</span><span class="sxs-lookup"><span data-stu-id="17683-131">Returns 29.0456 deg</span></span>
  
## <a name="example-2"></a><span data-ttu-id="17683-132">Пример 2</span><span class="sxs-lookup"><span data-stu-id="17683-132">Example 2</span></span>

<span data-ttu-id="17683-133">ATAN2(1,SQRT(3))</span><span class="sxs-lookup"><span data-stu-id="17683-133">ATAN2(1,SQRT(3))</span></span>
  
<span data-ttu-id="17683-134">Возвращает 30 градусов</span><span class="sxs-lookup"><span data-stu-id="17683-134">Returns 30 deg</span></span>
  
## <a name="example-3"></a><span data-ttu-id="17683-135">Пример 3</span><span class="sxs-lookup"><span data-stu-id="17683-135">Example 3</span></span>

<span data-ttu-id="17683-136">ATAN2(1,1)</span><span class="sxs-lookup"><span data-stu-id="17683-136">ATAN2(1,1)</span></span>
  
<span data-ttu-id="17683-137">Возвращает 45 градусов</span><span class="sxs-lookup"><span data-stu-id="17683-137">Returns 45 deg</span></span>
  

