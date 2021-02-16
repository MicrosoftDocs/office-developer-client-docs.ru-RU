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
description: Представляет различные сведения в разных строках. В этой таблице описывается ячейка A на основе строки, в которой она расположена.
ms.openlocfilehash: 7009658c7a6844a5c6071f502c05114a4accd7b7
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/29/2019
ms.locfileid: "34541304"
---
# <a name="a-cell-geometry-section"></a><span data-ttu-id="4708f-104">A Cell (Geometry Section)</span><span class="sxs-lookup"><span data-stu-id="4708f-104">A Cell (Geometry Section)</span></span>

<span data-ttu-id="4708f-105">Представляет различные сведения в разных строках.</span><span class="sxs-lookup"><span data-stu-id="4708f-105">Represents different information in different rows.</span></span> <span data-ttu-id="4708f-106">В этой таблице описывается ячейка A на основе строки, в которой она расположена.</span><span class="sxs-lookup"><span data-stu-id="4708f-106">This table describes the A cell based on the row in which it's located.</span></span>
  
|<span data-ttu-id="4708f-107">Строка</span><span class="sxs-lookup"><span data-stu-id="4708f-107">Row</span></span>|<span data-ttu-id="4708f-108">Описание</span><span class="sxs-lookup"><span data-stu-id="4708f-108">Description</span></span>|
|:-----|:-----|
|[<span data-ttu-id="4708f-109">ArcTo</span><span class="sxs-lookup"><span data-stu-id="4708f-109">ArcTo</span></span>](arcto-row-geometry-section.md) <br/> | <span data-ttu-id="4708f-110">Расстояние от средней точки дуги до средней точки ее разоряемой.</span><span class="sxs-lookup"><span data-stu-id="4708f-110">The distance from the arc's midpoint to the midpoint of its chord.</span></span>  <br/> |
|[<span data-ttu-id="4708f-111">EllipticalArcTo</span><span class="sxs-lookup"><span data-stu-id="4708f-111">EllipticalArcTo</span></span>](ellipticalarcto-row-geometry-section.md) <br/> | <span data-ttu-id="4708f-112">X-координата контрольной точки дуги, точки на дуге.  Контрольная точка лучше всего расположена примерно на середине между началом и конечной вершиной дуги. В противном случае дуга может увеличиваться до крайнего размера, чтобы пройти через контрольную точку с непредсказуемыми результатами.</span><span class="sxs-lookup"><span data-stu-id="4708f-112">The  *x*  -coordinate of the arc's control point, a point on the arc. The control point is best located about halfway between the beginning and ending vertices of the arc. Otherwise, the arc may grow to an extreme size in order to pass through the control point, with unpredictable results.</span></span>  <br/> |
|[<span data-ttu-id="4708f-113">PolylineTo</span><span class="sxs-lookup"><span data-stu-id="4708f-113">PolylineTo</span></span>](polylineto-row-geometry-section.md) <br/> | <span data-ttu-id="4708f-114">Многолинейная формула.</span><span class="sxs-lookup"><span data-stu-id="4708f-114">The polyline formula.</span></span>  <br/> |
|[<span data-ttu-id="4708f-115">NURBSTo</span><span class="sxs-lookup"><span data-stu-id="4708f-115">NURBSTo</span></span>](nurbsto-row-geometry-section.md) <br/> | <span data-ttu-id="4708f-116">От второго до последнего вехи неуникционного рационального B-spline (NURBS).</span><span class="sxs-lookup"><span data-stu-id="4708f-116">The second to the last knot of the nonuniform rational B-spline (NURBS).</span></span>  <br/> |
|[<span data-ttu-id="4708f-117">SplineStart</span><span class="sxs-lookup"><span data-stu-id="4708f-117">SplineStart</span></span>](splinestart-row-geometry-section.md) <br/> | <span data-ttu-id="4708f-118">Вторая часть сплайна.</span><span class="sxs-lookup"><span data-stu-id="4708f-118">The second knot of the spline.</span></span>  <br/> |
|[<span data-ttu-id="4708f-119">SplineKnot</span><span class="sxs-lookup"><span data-stu-id="4708f-119">SplineKnot</span></span>](splineknot-row-geometry-section.md) <br/> | <span data-ttu-id="4708f-120">Одна из подмайок сплайна (кроме последней или первой).</span><span class="sxs-lookup"><span data-stu-id="4708f-120">One of the spline's knots (other than the last one or the first two).</span></span>  <br/> |
|[<span data-ttu-id="4708f-121">InfiniteLine</span><span class="sxs-lookup"><span data-stu-id="4708f-121">InfiniteLine</span></span>](infiniteline-row-geometry-section.md) <br/> | <span data-ttu-id="4708f-122">X-координата точки на бесконечной линии;  сопряжено с *координатой Y,* представленной ячейкой [B.](b-cell-geometry-section.md)</span><span class="sxs-lookup"><span data-stu-id="4708f-122">An  *x*  -coordinate of a point on the infinite line; paired with  *y*  -coordinate represented by the [B](b-cell-geometry-section.md) cell.</span></span>  <br/> |
|[<span data-ttu-id="4708f-123">Ellipse</span><span class="sxs-lookup"><span data-stu-id="4708f-123">Ellipse</span></span>](ellipse-row-geometry-section.md) <br/> | <span data-ttu-id="4708f-124">X-координата точки на эллипсе;  сопряжено с *координатой Y,* представленной ячейкой [B.](b-cell-geometry-section.md)</span><span class="sxs-lookup"><span data-stu-id="4708f-124">An  *x*  -coordinate of a point on the ellipse; paired with  *y*  -coordinate represented by the [B](b-cell-geometry-section.md) cell.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="4708f-125">Примечания</span><span class="sxs-lookup"><span data-stu-id="4708f-125">Remarks</span></span>

<span data-ttu-id="4708f-126">Чтобы получить ссылку на ячейку A по имени из другой формулы или из программы, используя свойство **CellsU,** используйте:</span><span class="sxs-lookup"><span data-stu-id="4708f-126">To get a reference to the A cell by name from another formula, or from a program, using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="4708f-127">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="4708f-127">Cell name:</span></span>  <br/> | <span data-ttu-id="4708f-128">Геометрия  *i*  .  *J,*            *где i*  и  *j*  = <1>, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="4708f-128">Geometry  *i*  .A  *j*            where  *i*  and  *j*  = <1>, 2, 3...</span></span>  <br/> |
|| <span data-ttu-id="4708f-129">Геометрия  *i*  . A1 (строки InfiniteLine и Ellipse),  *где i*  = <1>, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="4708f-129">Geometry  *i*  .A1 (InfiniteLine and Ellipse rows)            where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="4708f-130">Чтобы получить ссылку на ячейку A по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="4708f-130">To get a reference to the A cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="4708f-131">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="4708f-131">Section index:</span></span>  <br/> |<span data-ttu-id="4708f-132">**visSectionFirstComponent** +  *i*, где *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="4708f-132">**visSectionFirstComponent** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="4708f-133">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="4708f-133">Row index:</span></span>  <br/> |<span data-ttu-id="4708f-134">**visRowVertex** +  *j*, где *j* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="4708f-134">**visRowVertex** +  *j*            where  *j*  = 0, 1, 2...</span></span>  <br/> |
||<span data-ttu-id="4708f-135">**visRowVertex** (строки InfiniteLine и Ellipse)</span><span class="sxs-lookup"><span data-stu-id="4708f-135">**visRowVertex** (InfiniteLine and Ellipse rows)</span></span>  <br/> |
| <span data-ttu-id="4708f-136">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="4708f-136">Cell index:</span></span>  <br/> |<span data-ttu-id="4708f-137">**visBow** (строка ArcTo)</span><span class="sxs-lookup"><span data-stu-id="4708f-137">**visBow** (ArcTo row)</span></span>  <br/> |
||<span data-ttu-id="4708f-138">**visControlX** (строка EllipticalArcTo)</span><span class="sxs-lookup"><span data-stu-id="4708f-138">**visControlX** (EllipticalArcTo row)</span></span>  <br/> |
||<span data-ttu-id="4708f-139">**visControlY** (строка EllipticalArcTo)</span><span class="sxs-lookup"><span data-stu-id="4708f-139">**visControlY** (EllipticalArcTo row)</span></span>  <br/> |
||<span data-ttu-id="4708f-140">**visPolylineData** (строка Polyline)</span><span class="sxs-lookup"><span data-stu-id="4708f-140">**visPolylineData** (Polyline row)</span></span>  <br/> |
||<span data-ttu-id="4708f-141">**visNURBSKnot** (строка NURBSTo)</span><span class="sxs-lookup"><span data-stu-id="4708f-141">**visNURBSKnot** (NURBSTo row)</span></span>  <br/> |
||<span data-ttu-id="4708f-142">**visSplineKnot** (строки SplineStart и SplineKnot)</span><span class="sxs-lookup"><span data-stu-id="4708f-142">**visSplineKnot** (SplineStart and SplineKnot rows)</span></span>  <br/> |
||<span data-ttu-id="4708f-143">**visInfiniteLineX2** (строка InfiniteLine)</span><span class="sxs-lookup"><span data-stu-id="4708f-143">**visInfiniteLineX2** (InfiniteLine row)</span></span>  <br/> |
||<span data-ttu-id="4708f-144">**visEllipseMajorX** (строка Ellipse)</span><span class="sxs-lookup"><span data-stu-id="4708f-144">**visEllipseMajorX** (Ellipse row)</span></span>  <br/> |
   

