---
title: A Cell (Geometry Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm51215
localization_priority: Normal
ms.assetid: 6853df0f-d22e-89ca-7d34-342b9c0bea23
description: Представляет различные сведения в разных строках. В этой таблице описывается ячейка, основанная на строке, в которой она расположена.
ms.openlocfilehash: 42f346b06cad827cfe56fc113a8387d1a31a6867
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33432921"
---
# <a name="a-cell-geometry-section"></a><span data-ttu-id="13694-104">A Cell (Geometry Section)</span><span class="sxs-lookup"><span data-stu-id="13694-104">A Cell (Geometry Section)</span></span>

<span data-ttu-id="13694-105">Представляет различные сведения в разных строках.</span><span class="sxs-lookup"><span data-stu-id="13694-105">Represents different information in different rows.</span></span> <span data-ttu-id="13694-106">В этой таблице описывается ячейка, основанная на строке, в которой она расположена.</span><span class="sxs-lookup"><span data-stu-id="13694-106">This table describes the A cell based on the row in which it's located.</span></span>
  
|<span data-ttu-id="13694-107">**Строка**</span><span class="sxs-lookup"><span data-stu-id="13694-107">**Row**</span></span>|<span data-ttu-id="13694-108">**Описание**</span><span class="sxs-lookup"><span data-stu-id="13694-108">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="13694-109">ArcTo</span><span class="sxs-lookup"><span data-stu-id="13694-109">ArcTo</span></span>](arcto-row-geometry-section.md) <br/> | <span data-ttu-id="13694-110">Расстояние от средней дуги до средней точки аккорда.</span><span class="sxs-lookup"><span data-stu-id="13694-110">The distance from the arc's midpoint to the midpoint of its chord.</span></span>  <br/> |
|[<span data-ttu-id="13694-111">EllipticalArcTo</span><span class="sxs-lookup"><span data-stu-id="13694-111">EllipticalArcTo</span></span>](ellipticalarcto-row-geometry-section.md) <br/> | <span data-ttu-id="13694-112">Координата *x* контрольной точки дуги, точка на дуги. Контрольная точка лучше всего расположена около посередине между начальным и конечным вершинами дуги. В противном случае дуга может увеличиться до экстремального размера для прохождения через контрольную точку с непредсказуемыми результатами.</span><span class="sxs-lookup"><span data-stu-id="13694-112">The  *x*  -coordinate of the arc's control point, a point on the arc. The control point is best located about halfway between the beginning and ending vertices of the arc. Otherwise, the arc may grow to an extreme size in order to pass through the control point, with unpredictable results.</span></span>  <br/> |
|[<span data-ttu-id="13694-113">PolylineTo</span><span class="sxs-lookup"><span data-stu-id="13694-113">PolylineTo</span></span>](polylineto-row-geometry-section.md) <br/> | <span data-ttu-id="13694-114">Формула ломаной линии.</span><span class="sxs-lookup"><span data-stu-id="13694-114">The polyline formula.</span></span>  <br/> |
|[<span data-ttu-id="13694-115">NURBSTo</span><span class="sxs-lookup"><span data-stu-id="13694-115">NURBSTo</span></span>](nurbsto-row-geometry-section.md) <br/> | <span data-ttu-id="13694-116">Вторая — последняя кнот неоднородного рационального сплайна B-сплайна (NURBS).</span><span class="sxs-lookup"><span data-stu-id="13694-116">The second to the last knot of the nonuniform rational B-spline (NURBS).</span></span>  <br/> |
|[<span data-ttu-id="13694-117">SplineStart</span><span class="sxs-lookup"><span data-stu-id="13694-117">SplineStart</span></span>](splinestart-row-geometry-section.md) <br/> | <span data-ttu-id="13694-118">Второй кнот сплайна.</span><span class="sxs-lookup"><span data-stu-id="13694-118">The second knot of the spline.</span></span>  <br/> |
|[<span data-ttu-id="13694-119">SplineKnot</span><span class="sxs-lookup"><span data-stu-id="13694-119">SplineKnot</span></span>](splineknot-row-geometry-section.md) <br/> | <span data-ttu-id="13694-120">Один из Кнотс сплайна (отличный от последнего или первых двух).</span><span class="sxs-lookup"><span data-stu-id="13694-120">One of the spline's knots (other than the last one or the first two).</span></span>  <br/> |
|[<span data-ttu-id="13694-121">InfiniteLine</span><span class="sxs-lookup"><span data-stu-id="13694-121">InfiniteLine</span></span>](infiniteline-row-geometry-section.md) <br/> | <span data-ttu-id="13694-122">Координата *x* точки на бесконечной линии; Связывание с координатой *y* , представленной в ячейке [B](b-cell-geometry-section.md) .</span><span class="sxs-lookup"><span data-stu-id="13694-122">An  *x*  -coordinate of a point on the infinite line; paired with  *y*  -coordinate represented by the [B](b-cell-geometry-section.md) cell.</span></span>  <br/> |
|[<span data-ttu-id="13694-123">Ellipse</span><span class="sxs-lookup"><span data-stu-id="13694-123">Ellipse</span></span>](ellipse-row-geometry-section.md) <br/> | <span data-ttu-id="13694-124">Координата *x* точки эллипса; Связывание с координатой *y* , представленной в ячейке [B](b-cell-geometry-section.md) .</span><span class="sxs-lookup"><span data-stu-id="13694-124">An  *x*  -coordinate of a point on the ellipse; paired with  *y*  -coordinate represented by the [B](b-cell-geometry-section.md) cell.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="13694-125">Примечания</span><span class="sxs-lookup"><span data-stu-id="13694-125">Remarks</span></span>

<span data-ttu-id="13694-126">Чтобы получить ссылку на ячейку по имени из другой формулы или из программы с помощью свойства **CellsU** , используйте следующее:</span><span class="sxs-lookup"><span data-stu-id="13694-126">To get a reference to the A cell by name from another formula, or from a program, using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="13694-127">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="13694-127">Cell name:</span></span>  <br/> | <span data-ttu-id="13694-128">Геометрия *i* . A *j* , где *i* и *j* = <1>, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="13694-128">Geometry  *i*  .A  *j*            where  *i*  and  *j*  = <1>, 2, 3...</span></span>  <br/> |
|| <span data-ttu-id="13694-129">Геометрия *i* . A1 (строка infiniteline и эллиптические строки), где *i* = <1>, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="13694-129">Geometry  *i*  .A1 (InfiniteLine and Ellipse rows)            where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="13694-130">Чтобы получить ссылку на ячейку по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="13694-130">To get a reference to the A cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="13694-131">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="13694-131">Section index:</span></span>  <br/> |<span data-ttu-id="13694-132">**visSectionFirstComponent** +  *i*, где *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="13694-132">**visSectionFirstComponent** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="13694-133">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="13694-133">Row index:</span></span>  <br/> |<span data-ttu-id="13694-134">**visRowVertex** +  *j*, где *j* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="13694-134">**visRowVertex** +  *j*            where  *j*  = 0, 1, 2...</span></span>  <br/> |
||<span data-ttu-id="13694-135">**visRowVertex** (строки InfiniteLine и Ellipse)</span><span class="sxs-lookup"><span data-stu-id="13694-135">**visRowVertex** (InfiniteLine and Ellipse rows)</span></span>  <br/> |
| <span data-ttu-id="13694-136">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="13694-136">Cell index:</span></span>  <br/> |<span data-ttu-id="13694-137">**висбов** (Строка строка ArcTo)</span><span class="sxs-lookup"><span data-stu-id="13694-137">**visBow** (ArcTo row)</span></span>  <br/> |
||<span data-ttu-id="13694-138">**висконтролкс** (Строка строка ellipticalarcto)</span><span class="sxs-lookup"><span data-stu-id="13694-138">**visControlX** (EllipticalArcTo row)</span></span>  <br/> |
||<span data-ttu-id="13694-139">**висконтроли** (Строка строка ellipticalarcto)</span><span class="sxs-lookup"><span data-stu-id="13694-139">**visControlY** (EllipticalArcTo row)</span></span>  <br/> |
||<span data-ttu-id="13694-140">**висполилинедата** (Строка ломаной линии)</span><span class="sxs-lookup"><span data-stu-id="13694-140">**visPolylineData** (Polyline row)</span></span>  <br/> |
||<span data-ttu-id="13694-141">**виснурбскнот** (Строка NURBSTo)</span><span class="sxs-lookup"><span data-stu-id="13694-141">**visNURBSKnot** (NURBSTo row)</span></span>  <br/> |
||<span data-ttu-id="13694-142">**виссплинекнот** (Строки строка splinestart и строка splineknot)</span><span class="sxs-lookup"><span data-stu-id="13694-142">**visSplineKnot** (SplineStart and SplineKnot rows)</span></span>  <br/> |
||<span data-ttu-id="13694-143">**visInfiniteLineX2** (Строка строка infiniteline)</span><span class="sxs-lookup"><span data-stu-id="13694-143">**visInfiniteLineX2** (InfiniteLine row)</span></span>  <br/> |
||<span data-ttu-id="13694-144">**виселлипсемажоркс** (Строка "эллипс")</span><span class="sxs-lookup"><span data-stu-id="13694-144">**visEllipseMajorX** (Ellipse row)</span></span>  <br/> |
   

