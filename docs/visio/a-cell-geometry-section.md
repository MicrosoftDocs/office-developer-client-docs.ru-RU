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
ms.openlocfilehash: 7009658c7a6844a5c6071f502c05114a4accd7b7
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/29/2019
ms.locfileid: "34541304"
---
# <a name="a-cell-geometry-section"></a><span data-ttu-id="dd678-104">A Cell (Geometry Section)</span><span class="sxs-lookup"><span data-stu-id="dd678-104">A Cell (Geometry Section)</span></span>

<span data-ttu-id="dd678-105">Представляет различные сведения в разных строках.</span><span class="sxs-lookup"><span data-stu-id="dd678-105">Represents different information in different rows.</span></span> <span data-ttu-id="dd678-106">В этой таблице описывается ячейка, основанная на строке, в которой она расположена.</span><span class="sxs-lookup"><span data-stu-id="dd678-106">This table describes the A cell based on the row in which it's located.</span></span>
  
|<span data-ttu-id="dd678-107">Строка</span><span class="sxs-lookup"><span data-stu-id="dd678-107">Row</span></span>|<span data-ttu-id="dd678-108">Описание</span><span class="sxs-lookup"><span data-stu-id="dd678-108">Description</span></span>|
|:-----|:-----|
|[<span data-ttu-id="dd678-109">ArcTo</span><span class="sxs-lookup"><span data-stu-id="dd678-109">ArcTo</span></span>](arcto-row-geometry-section.md) <br/> | <span data-ttu-id="dd678-110">Расстояние от средней дуги до средней точки аккорда.</span><span class="sxs-lookup"><span data-stu-id="dd678-110">The distance from the arc's midpoint to the midpoint of its chord.</span></span>  <br/> |
|[<span data-ttu-id="dd678-111">EllipticalArcTo</span><span class="sxs-lookup"><span data-stu-id="dd678-111">EllipticalArcTo</span></span>](ellipticalarcto-row-geometry-section.md) <br/> | <span data-ttu-id="dd678-112">Координата *x* контрольной точки дуги, точка на дуги. Контрольная точка лучше всего расположена около посередине между начальным и конечным вершинами дуги. В противном случае дуга может увеличиться до экстремального размера для прохождения через контрольную точку с непредсказуемыми результатами.</span><span class="sxs-lookup"><span data-stu-id="dd678-112">The  *x*  -coordinate of the arc's control point, a point on the arc. The control point is best located about halfway between the beginning and ending vertices of the arc. Otherwise, the arc may grow to an extreme size in order to pass through the control point, with unpredictable results.</span></span>  <br/> |
|[<span data-ttu-id="dd678-113">PolylineTo</span><span class="sxs-lookup"><span data-stu-id="dd678-113">PolylineTo</span></span>](polylineto-row-geometry-section.md) <br/> | <span data-ttu-id="dd678-114">Формула ломаной линии.</span><span class="sxs-lookup"><span data-stu-id="dd678-114">The polyline formula.</span></span>  <br/> |
|[<span data-ttu-id="dd678-115">NURBSTo</span><span class="sxs-lookup"><span data-stu-id="dd678-115">NURBSTo</span></span>](nurbsto-row-geometry-section.md) <br/> | <span data-ttu-id="dd678-116">Вторая — последняя кнот неоднородного рационального сплайна B-сплайна (NURBS).</span><span class="sxs-lookup"><span data-stu-id="dd678-116">The second to the last knot of the nonuniform rational B-spline (NURBS).</span></span>  <br/> |
|[<span data-ttu-id="dd678-117">SplineStart</span><span class="sxs-lookup"><span data-stu-id="dd678-117">SplineStart</span></span>](splinestart-row-geometry-section.md) <br/> | <span data-ttu-id="dd678-118">Второй кнот сплайна.</span><span class="sxs-lookup"><span data-stu-id="dd678-118">The second knot of the spline.</span></span>  <br/> |
|[<span data-ttu-id="dd678-119">SplineKnot</span><span class="sxs-lookup"><span data-stu-id="dd678-119">SplineKnot</span></span>](splineknot-row-geometry-section.md) <br/> | <span data-ttu-id="dd678-120">Один из Кнотс сплайна (отличный от последнего или первых двух).</span><span class="sxs-lookup"><span data-stu-id="dd678-120">One of the spline's knots (other than the last one or the first two).</span></span>  <br/> |
|[<span data-ttu-id="dd678-121">InfiniteLine</span><span class="sxs-lookup"><span data-stu-id="dd678-121">InfiniteLine</span></span>](infiniteline-row-geometry-section.md) <br/> | <span data-ttu-id="dd678-122">Координата *x* точки на бесконечной линии; Связывание с координатой *y* , представленной в ячейке [B](b-cell-geometry-section.md) .</span><span class="sxs-lookup"><span data-stu-id="dd678-122">An  *x*  -coordinate of a point on the infinite line; paired with  *y*  -coordinate represented by the [B](b-cell-geometry-section.md) cell.</span></span>  <br/> |
|[<span data-ttu-id="dd678-123">Ellipse</span><span class="sxs-lookup"><span data-stu-id="dd678-123">Ellipse</span></span>](ellipse-row-geometry-section.md) <br/> | <span data-ttu-id="dd678-124">Координата *x* точки эллипса; Связывание с координатой *y* , представленной в ячейке [B](b-cell-geometry-section.md) .</span><span class="sxs-lookup"><span data-stu-id="dd678-124">An  *x*  -coordinate of a point on the ellipse; paired with  *y*  -coordinate represented by the [B](b-cell-geometry-section.md) cell.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="dd678-125">Примечания</span><span class="sxs-lookup"><span data-stu-id="dd678-125">Remarks</span></span>

<span data-ttu-id="dd678-126">Чтобы получить ссылку на ячейку по имени из другой формулы или из программы с помощью свойства **CellsU** , используйте следующее:</span><span class="sxs-lookup"><span data-stu-id="dd678-126">To get a reference to the A cell by name from another formula, or from a program, using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="dd678-127">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="dd678-127">Cell name:</span></span>  <br/> | <span data-ttu-id="dd678-128">Геометрия *i* . A *j* , где *i* и *j* = <1>, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="dd678-128">Geometry  *i*  .A  *j*            where  *i*  and  *j*  = <1>, 2, 3...</span></span>  <br/> |
|| <span data-ttu-id="dd678-129">Геометрия *i* . A1 (строка infiniteline и эллиптические строки), где *i* = <1>, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="dd678-129">Geometry  *i*  .A1 (InfiniteLine and Ellipse rows)            where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="dd678-130">Чтобы получить ссылку на ячейку по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="dd678-130">To get a reference to the A cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="dd678-131">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="dd678-131">Section index:</span></span>  <br/> |<span data-ttu-id="dd678-132">**visSectionFirstComponent** +  *i*, где *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="dd678-132">**visSectionFirstComponent** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="dd678-133">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="dd678-133">Row index:</span></span>  <br/> |<span data-ttu-id="dd678-134">**visRowVertex** +  *j*, где *j* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="dd678-134">**visRowVertex** +  *j*            where  *j*  = 0, 1, 2...</span></span>  <br/> |
||<span data-ttu-id="dd678-135">**visRowVertex** (строки InfiniteLine и Ellipse)</span><span class="sxs-lookup"><span data-stu-id="dd678-135">**visRowVertex** (InfiniteLine and Ellipse rows)</span></span>  <br/> |
| <span data-ttu-id="dd678-136">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="dd678-136">Cell index:</span></span>  <br/> |<span data-ttu-id="dd678-137">**висбов** (строка строка ArcTo)</span><span class="sxs-lookup"><span data-stu-id="dd678-137">**visBow** (ArcTo row)</span></span>  <br/> |
||<span data-ttu-id="dd678-138">**висконтролкс** (строка строка ellipticalarcto)</span><span class="sxs-lookup"><span data-stu-id="dd678-138">**visControlX** (EllipticalArcTo row)</span></span>  <br/> |
||<span data-ttu-id="dd678-139">**висконтроли** (строка строка ellipticalarcto)</span><span class="sxs-lookup"><span data-stu-id="dd678-139">**visControlY** (EllipticalArcTo row)</span></span>  <br/> |
||<span data-ttu-id="dd678-140">**висполилинедата** (строка ломаной линии)</span><span class="sxs-lookup"><span data-stu-id="dd678-140">**visPolylineData** (Polyline row)</span></span>  <br/> |
||<span data-ttu-id="dd678-141">**виснурбскнот** (строка NURBSTo)</span><span class="sxs-lookup"><span data-stu-id="dd678-141">**visNURBSKnot** (NURBSTo row)</span></span>  <br/> |
||<span data-ttu-id="dd678-142">**виссплинекнот** (строки строка splinestart и строка splineknot)</span><span class="sxs-lookup"><span data-stu-id="dd678-142">**visSplineKnot** (SplineStart and SplineKnot rows)</span></span>  <br/> |
||<span data-ttu-id="dd678-143">**visInfiniteLineX2** (строка строка infiniteline)</span><span class="sxs-lookup"><span data-stu-id="dd678-143">**visInfiniteLineX2** (InfiniteLine row)</span></span>  <br/> |
||<span data-ttu-id="dd678-144">**виселлипсемажоркс** (строка "эллипс")</span><span class="sxs-lookup"><span data-stu-id="dd678-144">**visEllipseMajorX** (Ellipse row)</span></span>  <br/> |
   

