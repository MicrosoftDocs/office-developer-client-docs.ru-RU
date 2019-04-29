---
title: Ячейка Y (раздел "Геометрия")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251750
localization_priority: Normal
ms.assetid: a53b5787-f419-7a36-3c04-c63b3c173ac7
description: Представляет положение фигуры по оси Y в локальной системе координат. В этой таблице описывается ячейка Y с учетом столбца, в котором она расположена.
ms.openlocfilehash: 9e823b8d21682b419a70ce498016abf575f36f6b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33420943"
---
# <a name="y-cell-geometry-section"></a><span data-ttu-id="bedfb-104">Ячейка Y (раздел "Геометрия")</span><span class="sxs-lookup"><span data-stu-id="bedfb-104">Y Cell (Geometry Section)</span></span>

<span data-ttu-id="bedfb-105">Представляет положение фигуры по оси *Y* в локальной системе координат.</span><span class="sxs-lookup"><span data-stu-id="bedfb-105">Represents a  *y*  -coordinate on a shape in local coordinates.</span></span> <span data-ttu-id="bedfb-106">В этой таблице описывается ячейка Y с учетом столбца, в котором она расположена.</span><span class="sxs-lookup"><span data-stu-id="bedfb-106">This table describes the Y cell based on the row in which it's located.</span></span> 
  
|<span data-ttu-id="bedfb-107">**Строка**</span><span class="sxs-lookup"><span data-stu-id="bedfb-107">**Row**</span></span>|<span data-ttu-id="bedfb-108">**Описание**</span><span class="sxs-lookup"><span data-stu-id="bedfb-108">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="bedfb-109">NURBSTo</span><span class="sxs-lookup"><span data-stu-id="bedfb-109">NURBSTo</span></span>](nurbsto-row-geometry-section.md) <br/> | <span data-ttu-id="bedfb-110">Если строка MoveTo находится в первой строке раздела, то ячейка Y представляет координату *Y* первой вершины пути.</span><span class="sxs-lookup"><span data-stu-id="bedfb-110">If the MoveTo row is the first row in the section, the Y cell represents the  *y*  -coordinate of the first vertex of a path.</span></span> <span data-ttu-id="bedfb-111">Если строка MoveTo находится между двух строк, то ячейка Y представляет координату *Y* первой вершины после прерывания пути.</span><span class="sxs-lookup"><span data-stu-id="bedfb-111">If the MoveTo row appears between two rows, the Y cell represents the  *y*  -coordinate of the first vertex after the break in the path.</span></span>  <br/> |
|[<span data-ttu-id="bedfb-112">LineTo</span><span class="sxs-lookup"><span data-stu-id="bedfb-112">LineTo</span></span>](lineto-row-geometry-section.md) <br/> | <span data-ttu-id="bedfb-113">Координата *Y* последней вершины сегмента прямой линии.</span><span class="sxs-lookup"><span data-stu-id="bedfb-113">The  *y*  -coordinate of the ending vertex of a straight line segment.</span></span>  <br/> |
|[<span data-ttu-id="bedfb-114">ArcTo</span><span class="sxs-lookup"><span data-stu-id="bedfb-114">ArcTo</span></span>](arcto-row-geometry-section.md) <br/> | <span data-ttu-id="bedfb-115">Координата *Y* последней вершины дуги.</span><span class="sxs-lookup"><span data-stu-id="bedfb-115">The  *y*  -coordinate of the ending vertex of an arc.</span></span>  <br/> |
|[<span data-ttu-id="bedfb-116">EllipticalArcTo</span><span class="sxs-lookup"><span data-stu-id="bedfb-116">EllipticalArcTo</span></span>](ellipticalarcto-row-geometry-section.md) <br/> | <span data-ttu-id="bedfb-117">Координата *Y* последней вершины дуги эллипса.</span><span class="sxs-lookup"><span data-stu-id="bedfb-117">The  *y*  -coordinate of the ending vertex of an elliptical arc.</span></span>  <br/> |
|[<span data-ttu-id="bedfb-118">PolylineTo</span><span class="sxs-lookup"><span data-stu-id="bedfb-118">PolylineTo</span></span>](polylineto-row-geometry-section.md) <br/> | <span data-ttu-id="bedfb-119">Координата *Y* последней вершины ломаной линии.</span><span class="sxs-lookup"><span data-stu-id="bedfb-119">The  *y*  -coordinate of the ending vertex of a polyline.</span></span>  <br/> |
|[<span data-ttu-id="bedfb-120">NURBSTo</span><span class="sxs-lookup"><span data-stu-id="bedfb-120">NURBSTo</span></span>](nurbsto-row-geometry-section.md) <br/> | <span data-ttu-id="bedfb-121">Координата *Y* последней контрольной точки неоднородного рационального B-сплайна (NURBS).</span><span class="sxs-lookup"><span data-stu-id="bedfb-121">The  *y*  -coordinate of the last control point of a nonuniform rational B-spline (NURBS).</span></span>  <br/> |
|[<span data-ttu-id="bedfb-122">SplineStart</span><span class="sxs-lookup"><span data-stu-id="bedfb-122">SplineStart</span></span>](splinestart-row-geometry-section.md) <br/> | <span data-ttu-id="bedfb-123">Координата *Y* второй контрольной точки сплайна.</span><span class="sxs-lookup"><span data-stu-id="bedfb-123">The  *y*  -coordinate of a spline's second control point.</span></span>  <br/> |
|[<span data-ttu-id="bedfb-124">SplineKnot</span><span class="sxs-lookup"><span data-stu-id="bedfb-124">SplineKnot</span></span>](splineknot-row-geometry-section.md) <br/> | <span data-ttu-id="bedfb-125">Координата *Y* контрольной точки.</span><span class="sxs-lookup"><span data-stu-id="bedfb-125">The  *y*  -coordinate of a control point.</span></span>  <br/> |
|[<span data-ttu-id="bedfb-126">InfiniteLine</span><span class="sxs-lookup"><span data-stu-id="bedfb-126">InfiniteLine</span></span>](infiniteline-row-geometry-section.md) <br/> | <span data-ttu-id="bedfb-127">Координата *Y* точки на бесконечной прямой.</span><span class="sxs-lookup"><span data-stu-id="bedfb-127">A  *y-*  coordinate of a point on the infinite line.</span></span>  <br/> |
|[<span data-ttu-id="bedfb-128">Ellipse</span><span class="sxs-lookup"><span data-stu-id="bedfb-128">Ellipse</span></span>](ellipse-row-geometry-section.md) <br/> | <span data-ttu-id="bedfb-129">Координата *Y* в центре эллипса.</span><span class="sxs-lookup"><span data-stu-id="bedfb-129">The  *y*  -coordinate of the center of the ellipse.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="bedfb-130">Замечания</span><span class="sxs-lookup"><span data-stu-id="bedfb-130">Remarks</span></span>

<span data-ttu-id="bedfb-131">Чтобы получить ссылку на ячейку Y по имени из другой формулы или из программы с помощью свойства **CellsU**, укажите следующее:</span><span class="sxs-lookup"><span data-stu-id="bedfb-131">To get a reference to the Y cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="bedfb-132">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="bedfb-132">Cell name:</span></span>  <br/> | <span data-ttu-id="bedfb-133">Геометрия *i* .Y *j*, где *i* и *j* = <1>, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="bedfb-133">Geometry  *i*  .Y  *j*            where  *i*  and  *j*  = <1>, 2, 3...</span></span>  <br/> |
|| <span data-ttu-id="bedfb-134">Геометрия *i* .Y1 (строки InfiniteLine и Ellipse), где *i* = <1>, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="bedfb-134">Geometry  *i*  .Y1 (InfiniteLine and Ellipse rows)            where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="bedfb-135">Чтобы получить ссылку на ячейку Y по индексу из программы, укажите свойство **CellsSRC** с такими аргументами:</span><span class="sxs-lookup"><span data-stu-id="bedfb-135">To get a reference to the Y cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="bedfb-136">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="bedfb-136">Section index:</span></span>  <br/> |<span data-ttu-id="bedfb-137">**visSectionFirstComponent** +  *i*, где *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="bedfb-137">**visSectionFirstComponent** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="bedfb-138">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="bedfb-138">Row index:</span></span>  <br/> |<span data-ttu-id="bedfb-139">**visRowVertex** +  *j*, где *j* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="bedfb-139">**visRowVertex** +  *j*            where  *j*  = 0, 1, 2...</span></span>  <br/> |
||<span data-ttu-id="bedfb-140">**visRowVertex** (строки InfiniteLine и Ellipse)</span><span class="sxs-lookup"><span data-stu-id="bedfb-140">**visRowVertex** (InfiniteLine and Ellipse rows)</span></span>  <br/> |
| <span data-ttu-id="bedfb-141">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="bedfb-141">Cell index:</span></span>  <br/> |<span data-ttu-id="bedfb-142">**visY** (строки MoveTo, LineTo, ArcTo, EllipticalArcTo, NURBSTo, Polyline, SplineStart и SplineKnot)</span><span class="sxs-lookup"><span data-stu-id="bedfb-142">**visY** (MoveTo, LineTo, ArcTo, EllipticalArcTo, NURBSTo, Polyline, SplineStart, and SplineKnot rows)</span></span>  <br/> |
||<span data-ttu-id="bedfb-143">**visInfiniteLineY1** (строка InfiniteLine)</span><span class="sxs-lookup"><span data-stu-id="bedfb-143">**visInfiniteLineY1** (InfiniteLine row)</span></span>  <br/> |
||<span data-ttu-id="bedfb-144">**visEllipseCenterY** (строка Ellipse)</span><span class="sxs-lookup"><span data-stu-id="bedfb-144">**visEllipseCenterY** (Ellipse row)</span></span>  <br/> |
   

