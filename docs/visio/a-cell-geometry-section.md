---
title: Ячейка A (раздел "Геометрия")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm51215
localization_priority: Normal
ms.assetid: 6853df0f-d22e-89ca-7d34-342b9c0bea23
description: Представляет различные сведения в различных строк. В следующей таблице описаны ячейки A, основанную на строке, в котором он находится.
ms.openlocfilehash: b907552c2346292a6b14baf16481b6b40cc80fc4
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19813117"
---
# <a name="a-cell-geometry-section"></a><span data-ttu-id="e3691-104">Ячейка A (раздел "Геометрия")</span><span class="sxs-lookup"><span data-stu-id="e3691-104">A Cell (Geometry Section)</span></span>

<span data-ttu-id="e3691-105">Представляет различные сведения в различных строк.</span><span class="sxs-lookup"><span data-stu-id="e3691-105">Represents different information in different rows.</span></span> <span data-ttu-id="e3691-106">В следующей таблице описаны ячейки A, основанную на строке, в котором он находится.</span><span class="sxs-lookup"><span data-stu-id="e3691-106">This table describes the A cell based on the row in which it's located.</span></span>
  
|<span data-ttu-id="e3691-107">**Row**</span><span class="sxs-lookup"><span data-stu-id="e3691-107">**Row**</span></span>|<span data-ttu-id="e3691-108">**Описание**</span><span class="sxs-lookup"><span data-stu-id="e3691-108">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="e3691-109">ArcTo</span><span class="sxs-lookup"><span data-stu-id="e3691-109">ArcTo</span></span>](arcto-row-geometry-section.md) <br/> | <span data-ttu-id="e3691-110">Расстояние от среднего дуги по центру его кабеля.</span><span class="sxs-lookup"><span data-stu-id="e3691-110">The distance from the arc's midpoint to the midpoint of its chord.</span></span>  <br/> |
|[<span data-ttu-id="e3691-111">EllipticalArcTo</span><span class="sxs-lookup"><span data-stu-id="e3691-111">EllipticalArcTo</span></span>](ellipticalarcto-row-geometry-section.md) <br/> | <span data-ttu-id="e3691-112">*X* -координата точки управления дуги, точку на дуги. Контрольная точка расположена лучше всего о пользователю между начала и окончания грани дуги. В противном случае дуги может расти в размерах чрезмерную размера для передачи через точку управления с непредсказуемым последствиям.</span><span class="sxs-lookup"><span data-stu-id="e3691-112">The  *x*  -coordinate of the arc's control point, a point on the arc. The control point is best located about halfway between the beginning and ending vertices of the arc. Otherwise, the arc may grow to an extreme size in order to pass through the control point, with unpredictable results.</span></span>  <br/> |
|[<span data-ttu-id="e3691-113">PolylineTo</span><span class="sxs-lookup"><span data-stu-id="e3691-113">PolylineTo</span></span>](polylineto-row-geometry-section.md) <br/> | <span data-ttu-id="e3691-114">Формула ломаной.</span><span class="sxs-lookup"><span data-stu-id="e3691-114">The polyline formula.</span></span>  <br/> |
|[<span data-ttu-id="e3691-115">NURBSTo</span><span class="sxs-lookup"><span data-stu-id="e3691-115">NURBSTo</span></span>](nurbsto-row-geometry-section.md) <br/> | <span data-ttu-id="e3691-116">Второй — к последней узлов неоднородной rational-сплайн (NURBS).</span><span class="sxs-lookup"><span data-stu-id="e3691-116">The second to the last knot of the nonuniform rational B-spline (NURBS).</span></span>  <br/> |
|[<span data-ttu-id="e3691-117">SplineStart</span><span class="sxs-lookup"><span data-stu-id="e3691-117">SplineStart</span></span>](splinestart-row-geometry-section.md) <br/> | <span data-ttu-id="e3691-118">Второй узел сплайн.</span><span class="sxs-lookup"><span data-stu-id="e3691-118">The second knot of the spline.</span></span>  <br/> |
|[<span data-ttu-id="e3691-119">SplineKnot</span><span class="sxs-lookup"><span data-stu-id="e3691-119">SplineKnot</span></span>](splineknot-row-geometry-section.md) <br/> | <span data-ttu-id="e3691-120">Один из узлов сплайна (кроме последней или первых двух).</span><span class="sxs-lookup"><span data-stu-id="e3691-120">One of the spline's knots (other than the last one or the first two).</span></span>  <br/> |
|[<span data-ttu-id="e3691-121">InfiniteLine</span><span class="sxs-lookup"><span data-stu-id="e3691-121">InfiniteLine</span></span>](infiniteline-row-geometry-section.md) <br/> | <span data-ttu-id="e3691-122">*X* -координаты точки на строке не ограничен. в сочетании с *y* -координата, представленное [B](b-cell-geometry-section.md) ячейки.</span><span class="sxs-lookup"><span data-stu-id="e3691-122">An  *x*  -coordinate of a point on the infinite line; paired with  *y*  -coordinate represented by the [B](b-cell-geometry-section.md) cell.</span></span>  <br/> |
|[<span data-ttu-id="e3691-123">Эллипс</span><span class="sxs-lookup"><span data-stu-id="e3691-123">Ellipse</span></span>](ellipse-row-geometry-section.md) <br/> | <span data-ttu-id="e3691-124">*X* -координаты точки на эллипс; в сочетании с *y* -координата, представленное [B](b-cell-geometry-section.md) ячейки.</span><span class="sxs-lookup"><span data-stu-id="e3691-124">An  *x*  -coordinate of a point on the ellipse; paired with  *y*  -coordinate represented by the [B](b-cell-geometry-section.md) cell.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e3691-125">Замечания</span><span class="sxs-lookup"><span data-stu-id="e3691-125">Remarks</span></span>

<span data-ttu-id="e3691-126">Для получения ссылки на ячейки A по имени, из другой формулы или из программы, с помощью свойства **CellsU** , используйте следующую команду:</span><span class="sxs-lookup"><span data-stu-id="e3691-126">To get a reference to the A cell by name from another formula, or from a program, using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="e3691-127">Имя ячейки.</span><span class="sxs-lookup"><span data-stu-id="e3691-127">Cell name:</span></span>  <br/> | <span data-ttu-id="e3691-128">Геометрия *i* . *J* где *i* и *j* = < 1 > 2, 3...</span><span class="sxs-lookup"><span data-stu-id="e3691-128">Geometry  *i*  .A  *j*            where  *i*  and  *j*  = <1>, 2, 3...</span></span>  <br/> |
|| <span data-ttu-id="e3691-129">Геометрия *i* . A1 (InfiniteLine и эллипс строк) где *i* = < 1 > 2, 3...</span><span class="sxs-lookup"><span data-stu-id="e3691-129">Geometry  *i*  .A1 (InfiniteLine and Ellipse rows)            where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="e3691-130">Для получения ссылки на ячейки A по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы:</span><span class="sxs-lookup"><span data-stu-id="e3691-130">To get a reference to the A cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="e3691-131">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="e3691-131">Section index:</span></span>  <br/> |<span data-ttu-id="e3691-132">**visSectionFirstComponent** +  *i* где *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="e3691-132">**visSectionFirstComponent** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="e3691-133">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="e3691-133">Row index:</span></span>  <br/> |<span data-ttu-id="e3691-134">**visRowVertex** +  *j* где *j* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="e3691-134">**visRowVertex** +  *j*            where  *j*  = 0, 1, 2...</span></span>  <br/> |
||<span data-ttu-id="e3691-135">**visRowVertex** (InfiniteLine и эллипс строк)</span><span class="sxs-lookup"><span data-stu-id="e3691-135">**visRowVertex** (InfiniteLine and Ellipse rows)</span></span>  <br/> |
| <span data-ttu-id="e3691-136">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="e3691-136">Cell index:</span></span>  <br/> |<span data-ttu-id="e3691-137">**visBow** (Строка ArcTo)</span><span class="sxs-lookup"><span data-stu-id="e3691-137">**visBow** (ArcTo row)</span></span>  <br/> |
||<span data-ttu-id="e3691-138">**visControlX** (Строка EllipticalArcTo)</span><span class="sxs-lookup"><span data-stu-id="e3691-138">**visControlX** (EllipticalArcTo row)</span></span>  <br/> |
||<span data-ttu-id="e3691-139">**visControlY** (Строка EllipticalArcTo)</span><span class="sxs-lookup"><span data-stu-id="e3691-139">**visControlY** (EllipticalArcTo row)</span></span>  <br/> |
||<span data-ttu-id="e3691-140">**visPolylineData** (Ломаной строка)</span><span class="sxs-lookup"><span data-stu-id="e3691-140">**visPolylineData** (Polyline row)</span></span>  <br/> |
||<span data-ttu-id="e3691-141">**visNURBSKnot** (Строка NURBSTo)</span><span class="sxs-lookup"><span data-stu-id="e3691-141">**visNURBSKnot** (NURBSTo row)</span></span>  <br/> |
||<span data-ttu-id="e3691-142">**visSplineKnot** (SplineStart и SplineKnot строк)</span><span class="sxs-lookup"><span data-stu-id="e3691-142">**visSplineKnot** (SplineStart and SplineKnot rows)</span></span>  <br/> |
||<span data-ttu-id="e3691-143">**visInfiniteLineX2** (Строка InfiniteLine)</span><span class="sxs-lookup"><span data-stu-id="e3691-143">**visInfiniteLineX2** (InfiniteLine row)</span></span>  <br/> |
||<span data-ttu-id="e3691-144">**visEllipseMajorX** (Эллипс строка)</span><span class="sxs-lookup"><span data-stu-id="e3691-144">**visEllipseMajorX** (Ellipse row)</span></span>  <br/> |
   

