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
description: Представляет различные сведения в разных строках. В этой таблице описывается ячейка на основе строки, в которой она расположена.
ms.openlocfilehash: 7009658c7a6844a5c6071f502c05114a4accd7b7
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/29/2019
ms.locfileid: "34541304"
---
# <a name="a-cell-geometry-section"></a><span data-ttu-id="fd040-104">A Cell (Geometry Section)</span><span class="sxs-lookup"><span data-stu-id="fd040-104">A Cell (Geometry Section)</span></span>

<span data-ttu-id="fd040-105">Представляет различные сведения в разных строках.</span><span class="sxs-lookup"><span data-stu-id="fd040-105">Represents different information in different rows.</span></span> <span data-ttu-id="fd040-106">В этой таблице описывается ячейка на основе строки, в которой она расположена.</span><span class="sxs-lookup"><span data-stu-id="fd040-106">This table describes the A cell based on the row in which it's located.</span></span>
  
|<span data-ttu-id="fd040-107">Строка</span><span class="sxs-lookup"><span data-stu-id="fd040-107">Row</span></span>|<span data-ttu-id="fd040-108">Описание</span><span class="sxs-lookup"><span data-stu-id="fd040-108">Description</span></span>|
|:-----|:-----|
|[<span data-ttu-id="fd040-109">ArcTo</span><span class="sxs-lookup"><span data-stu-id="fd040-109">ArcTo</span></span>](arcto-row-geometry-section.md) <br/> | <span data-ttu-id="fd040-110">Расстояние от середины дуги до середины аккорда.</span><span class="sxs-lookup"><span data-stu-id="fd040-110">The distance from the arc's midpoint to the midpoint of its chord.</span></span>  <br/> |
|[<span data-ttu-id="fd040-111">EllipticalArcTo</span><span class="sxs-lookup"><span data-stu-id="fd040-111">EllipticalArcTo</span></span>](ellipticalarcto-row-geometry-section.md) <br/> | <span data-ttu-id="fd040-112">X-координата точки управления дуги, точки на дуге.  Точка управления расположена на полпути между началом и окончанием вершин дуги. В противном случае дуга может вырасти до крайнего размера, чтобы пройти через точку управления с непредсказуемыми результатами.</span><span class="sxs-lookup"><span data-stu-id="fd040-112">The  *x*  -coordinate of the arc's control point, a point on the arc. The control point is best located about halfway between the beginning and ending vertices of the arc. Otherwise, the arc may grow to an extreme size in order to pass through the control point, with unpredictable results.</span></span>  <br/> |
|[<span data-ttu-id="fd040-113">PolylineTo</span><span class="sxs-lookup"><span data-stu-id="fd040-113">PolylineTo</span></span>](polylineto-row-geometry-section.md) <br/> | <span data-ttu-id="fd040-114">Формула полилинов.</span><span class="sxs-lookup"><span data-stu-id="fd040-114">The polyline formula.</span></span>  <br/> |
|[<span data-ttu-id="fd040-115">NURBSTo</span><span class="sxs-lookup"><span data-stu-id="fd040-115">NURBSTo</span></span>](nurbsto-row-geometry-section.md) <br/> | <span data-ttu-id="fd040-116">Второй до последнего узла неинформированной рациональной B-spline (NURBS).</span><span class="sxs-lookup"><span data-stu-id="fd040-116">The second to the last knot of the nonuniform rational B-spline (NURBS).</span></span>  <br/> |
|[<span data-ttu-id="fd040-117">SplineStart</span><span class="sxs-lookup"><span data-stu-id="fd040-117">SplineStart</span></span>](splinestart-row-geometry-section.md) <br/> | <span data-ttu-id="fd040-118">Второй узел spline.</span><span class="sxs-lookup"><span data-stu-id="fd040-118">The second knot of the spline.</span></span>  <br/> |
|[<span data-ttu-id="fd040-119">SplineKnot</span><span class="sxs-lookup"><span data-stu-id="fd040-119">SplineKnot</span></span>](splineknot-row-geometry-section.md) <br/> | <span data-ttu-id="fd040-120">Один из узлов spline (кроме последнего или первых двух).</span><span class="sxs-lookup"><span data-stu-id="fd040-120">One of the spline's knots (other than the last one or the first two).</span></span>  <br/> |
|[<span data-ttu-id="fd040-121">InfiniteLine</span><span class="sxs-lookup"><span data-stu-id="fd040-121">InfiniteLine</span></span>](infiniteline-row-geometry-section.md) <br/> | <span data-ttu-id="fd040-122">*X-координата* точки на бесконечной строке; в паре *с y-coordinate,* представленным ячейкой [B.](b-cell-geometry-section.md)</span><span class="sxs-lookup"><span data-stu-id="fd040-122">An  *x*  -coordinate of a point on the infinite line; paired with  *y*  -coordinate represented by the [B](b-cell-geometry-section.md) cell.</span></span>  <br/> |
|[<span data-ttu-id="fd040-123">Ellipse</span><span class="sxs-lookup"><span data-stu-id="fd040-123">Ellipse</span></span>](ellipse-row-geometry-section.md) <br/> | <span data-ttu-id="fd040-124">*X-координата* точки на эллипсе; в паре *с y-coordinate,* представленным ячейкой [B.](b-cell-geometry-section.md)</span><span class="sxs-lookup"><span data-stu-id="fd040-124">An  *x*  -coordinate of a point on the ellipse; paired with  *y*  -coordinate represented by the [B](b-cell-geometry-section.md) cell.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="fd040-125">Примечания</span><span class="sxs-lookup"><span data-stu-id="fd040-125">Remarks</span></span>

<span data-ttu-id="fd040-126">Чтобы получить ссылку на ячейку по имени из другой формулы или из программы, используя свойство **CellsU,** используйте:</span><span class="sxs-lookup"><span data-stu-id="fd040-126">To get a reference to the A cell by name from another formula, or from a program, using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="fd040-127">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="fd040-127">Cell name:</span></span>  <br/> | <span data-ttu-id="fd040-128">Геометрия  *i*  .  *J,*            *где i*  и  *j*  = <1>, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="fd040-128">Geometry  *i*  .A  *j*            where  *i*  and  *j*  = <1>, 2, 3...</span></span>  <br/> |
|| <span data-ttu-id="fd040-129">Геометрия  *i*  . A1 (строки InfiniteLine и Ellipse), где  *i*  = <1>, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="fd040-129">Geometry  *i*  .A1 (InfiniteLine and Ellipse rows)            where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="fd040-130">Чтобы получить ссылку на ячейку по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="fd040-130">To get a reference to the A cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="fd040-131">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="fd040-131">Section index:</span></span>  <br/> |<span data-ttu-id="fd040-132">**visSectionFirstComponent** +  *i*, где *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="fd040-132">**visSectionFirstComponent** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="fd040-133">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="fd040-133">Row index:</span></span>  <br/> |<span data-ttu-id="fd040-134">**visRowVertex** +  *j*, где *j* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="fd040-134">**visRowVertex** +  *j*            where  *j*  = 0, 1, 2...</span></span>  <br/> |
||<span data-ttu-id="fd040-135">**visRowVertex** (строки InfiniteLine и Ellipse)</span><span class="sxs-lookup"><span data-stu-id="fd040-135">**visRowVertex** (InfiniteLine and Ellipse rows)</span></span>  <br/> |
| <span data-ttu-id="fd040-136">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="fd040-136">Cell index:</span></span>  <br/> |<span data-ttu-id="fd040-137">**visBow** (строка ArcTo)</span><span class="sxs-lookup"><span data-stu-id="fd040-137">**visBow** (ArcTo row)</span></span>  <br/> |
||<span data-ttu-id="fd040-138">**visControlX** (ряд EllipticalArcTo)</span><span class="sxs-lookup"><span data-stu-id="fd040-138">**visControlX** (EllipticalArcTo row)</span></span>  <br/> |
||<span data-ttu-id="fd040-139">**visControlY** (ряд EllipticalArcTo)</span><span class="sxs-lookup"><span data-stu-id="fd040-139">**visControlY** (EllipticalArcTo row)</span></span>  <br/> |
||<span data-ttu-id="fd040-140">**visPolylineData** (строка Polyline)</span><span class="sxs-lookup"><span data-stu-id="fd040-140">**visPolylineData** (Polyline row)</span></span>  <br/> |
||<span data-ttu-id="fd040-141">**visNURBSKnot** (ряд NURBSTo)</span><span class="sxs-lookup"><span data-stu-id="fd040-141">**visNURBSKnot** (NURBSTo row)</span></span>  <br/> |
||<span data-ttu-id="fd040-142">**visSplineKnot** (строки SplineStart и SplineKnot)</span><span class="sxs-lookup"><span data-stu-id="fd040-142">**visSplineKnot** (SplineStart and SplineKnot rows)</span></span>  <br/> |
||<span data-ttu-id="fd040-143">**visInfiniteLineX2** (строка InfiniteLine)</span><span class="sxs-lookup"><span data-stu-id="fd040-143">**visInfiniteLineX2** (InfiniteLine row)</span></span>  <br/> |
||<span data-ttu-id="fd040-144">**visEllipseMajorX** (строка Ellipse)</span><span class="sxs-lookup"><span data-stu-id="fd040-144">**visEllipseMajorX** (Ellipse row)</span></span>  <br/> |
   

