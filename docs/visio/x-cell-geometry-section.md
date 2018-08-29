---
title: Ячейка X (раздел "Геометрия")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1135
localization_priority: Normal
ms.assetid: 2416b323-e084-18e1-c9be-a797078dfab9
description: Представляет положение фигуры по оси X в локальной системе координат. В этой таблице описывается ячейка X с учетом столбца, в котором она расположена.
ms.openlocfilehash: e5bc99d4f73d49741c4378009dfc2a883bb655ed
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19815183"
---
# <a name="x-cell-geometry-section"></a><span data-ttu-id="c0105-104">Ячейка X (раздел "Геометрия")</span><span class="sxs-lookup"><span data-stu-id="c0105-104">X Cell (Geometry Section)</span></span>

<span data-ttu-id="c0105-105">Представляет положение фигуры по оси *X* в локальной системе координат.</span><span class="sxs-lookup"><span data-stu-id="c0105-105">Represents an  *x*  -coordinate on a shape in local coordinates.</span></span> <span data-ttu-id="c0105-106">В этой таблице описывается ячейка X с учетом столбца, в котором она расположена.</span><span class="sxs-lookup"><span data-stu-id="c0105-106">This table describes the X cell based on the row in which it's located.</span></span> 
  
|<span data-ttu-id="c0105-107">**Строка**</span><span class="sxs-lookup"><span data-stu-id="c0105-107">**Row**</span></span>|<span data-ttu-id="c0105-108">**Описание**</span><span class="sxs-lookup"><span data-stu-id="c0105-108">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="c0105-109">MoveTo</span><span class="sxs-lookup"><span data-stu-id="c0105-109">MoveTo Method</span></span>](moveto-row-geometry-section.md) <br/> | <span data-ttu-id="c0105-110">Если строка MoveTo находится в первой строке раздела, то ячейка X представляет координату *X* первой вершины пути.</span><span class="sxs-lookup"><span data-stu-id="c0105-110">If the MoveTo row is the first row in the section, the X cell represents the  *x*  -coordinate of the first vertex of a path.</span></span> <span data-ttu-id="c0105-111">Если строка MoveTo находится между двух строк, то ячейка X представляет координату *X* первой вершины после прерывания пути.</span><span class="sxs-lookup"><span data-stu-id="c0105-111">If the MoveTo row appears between two rows, the X cell represents the  *x*  -coordinate of the first vertex after the break in the path.</span></span>  <br/> |
|[<span data-ttu-id="c0105-112">LineTo</span><span class="sxs-lookup"><span data-stu-id="c0105-112">LineTo</span></span>](lineto-row-geometry-section.md) <br/> | <span data-ttu-id="c0105-113">Координата *X* последней вершины сегмента прямой линии.</span><span class="sxs-lookup"><span data-stu-id="c0105-113">The  *x*  -coordinate of the ending vertex of a straight line segment.</span></span>  <br/> |
|[<span data-ttu-id="c0105-114">ArcTo</span><span class="sxs-lookup"><span data-stu-id="c0105-114">ArcTo</span></span>](arcto-row-geometry-section.md) <br/> | <span data-ttu-id="c0105-115">Координата *X* последней вершины дуги.</span><span class="sxs-lookup"><span data-stu-id="c0105-115">The  *x*  -coordinate of the ending vertex of an arc.</span></span>  <br/> |
|[<span data-ttu-id="c0105-116">EllipticalArcTo</span><span class="sxs-lookup"><span data-stu-id="c0105-116">EllipticalArcTo</span></span>](ellipticalarcto-row-geometry-section.md) <br/> | <span data-ttu-id="c0105-117">Координата *X* последней вершины дуги эллипса.</span><span class="sxs-lookup"><span data-stu-id="c0105-117">The  *x*  -coordinate of the ending vertex of an elliptical arc.</span></span>  <br/> |
|[<span data-ttu-id="c0105-118">PolylineTo</span><span class="sxs-lookup"><span data-stu-id="c0105-118">PolylineTo</span></span>](polylineto-row-geometry-section.md) <br/> | <span data-ttu-id="c0105-119">Координата *X* последней вершины ломаной линии.</span><span class="sxs-lookup"><span data-stu-id="c0105-119">The  *x*  -coordinate of the ending vertex of a polyline.</span></span>  <br/> |
|[<span data-ttu-id="c0105-120">NURBSTo</span><span class="sxs-lookup"><span data-stu-id="c0105-120">NURBSTo</span></span>](nurbsto-row-geometry-section.md) <br/> | <span data-ttu-id="c0105-121">Координата *X* последней контрольной точки неоднородного рационального B-сплайна (NURBS).</span><span class="sxs-lookup"><span data-stu-id="c0105-121">The  *x*  -coordinate of the last control point of a nonuniform rational B-spline (NURBS).</span></span>  <br/> |
|[<span data-ttu-id="c0105-122">SplineStart</span><span class="sxs-lookup"><span data-stu-id="c0105-122">SplineStart</span></span>](splinestart-row-geometry-section.md) <br/> | <span data-ttu-id="c0105-123">Координата *X* второй контрольной точки сплайна.</span><span class="sxs-lookup"><span data-stu-id="c0105-123">The  *x*  -coordinate of a spline's second control point.</span></span>  <br/> |
|[<span data-ttu-id="c0105-124">SplineKnot</span><span class="sxs-lookup"><span data-stu-id="c0105-124">SplineKnot</span></span>](splineknot-row-geometry-section.md) <br/> | <span data-ttu-id="c0105-125">Координата *X* контрольной точки.</span><span class="sxs-lookup"><span data-stu-id="c0105-125">The  *x*  -coordinate of a control point.</span></span>  <br/> |
|[<span data-ttu-id="c0105-126">InfiniteLine</span><span class="sxs-lookup"><span data-stu-id="c0105-126">InfiniteLine</span></span>](infiniteline-row-geometry-section.md) <br/> | <span data-ttu-id="c0105-127">Координата *X* точки на бесконечной прямой.</span><span class="sxs-lookup"><span data-stu-id="c0105-127">An  *x*  -coordinate of a point on the infinite line.</span></span>  <br/> |
|[<span data-ttu-id="c0105-128">Ellipse</span><span class="sxs-lookup"><span data-stu-id="c0105-128">Ellipse</span></span>](ellipse-row-geometry-section.md) <br/> | <span data-ttu-id="c0105-129">Координата *X* в центре эллипса.</span><span class="sxs-lookup"><span data-stu-id="c0105-129">The  *x*  -coordinate of the center of the ellipse.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c0105-130">Замечания</span><span class="sxs-lookup"><span data-stu-id="c0105-130">Remarks</span></span>

<span data-ttu-id="c0105-131">Чтобы получить ссылку на ячейку X по имени из другой формулы или из программы с помощью свойства **CellsU**, укажите следующее:</span><span class="sxs-lookup"><span data-stu-id="c0105-131">To get a reference to the X cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="c0105-132">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="c0105-132">Cell name:</span></span>  <br/> | <span data-ttu-id="c0105-133">Геометрия *i* .X *j*, где *i* и *j* = <1>, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="c0105-133">Geometry  *i*  .X  *j*            where  *i*  and  *j*  = <1>, 2, 3...</span></span>  <br/> |
|| <span data-ttu-id="c0105-134">Геометрия *i* .X1 (строки InfiniteLine и Ellipse), где *i* = <1>, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="c0105-134">Geometry  *i*  .X1 (InfiniteLine and Ellipse rows)            where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="c0105-135">Чтобы получить ссылку на ячейку X по индексу из программы, укажите свойство **CellsSRC** с такими аргументами:</span><span class="sxs-lookup"><span data-stu-id="c0105-135">To get a reference to the X cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="c0105-136">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="c0105-136">Section index:</span></span>  <br/> |<span data-ttu-id="c0105-137">**visSectionFirstComponent** +  *i*, где *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="c0105-137">**visSectionFirstComponent** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="c0105-138">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="c0105-138">Row index:</span></span>  <br/> |<span data-ttu-id="c0105-139">**visRowVertex** +  *j*, где *j* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="c0105-139">**visRowVertex** +  *j*            where  *j*  = 0, 1, 2...</span></span>  <br/> |
||<span data-ttu-id="c0105-140">**visRowVertex** (строки InfiniteLine и Ellipse)</span><span class="sxs-lookup"><span data-stu-id="c0105-140">**visRowVertex** (InfiniteLine and Ellipse rows)</span></span>  <br/> |
| <span data-ttu-id="c0105-141">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="c0105-141">Cell index:</span></span>  <br/> |<span data-ttu-id="c0105-142">**visX** (строки MoveTo, LineTo, ArcTo, EllipticalArcTo, NURBSTo, Polyline, SplineStart и SplineKnot)</span><span class="sxs-lookup"><span data-stu-id="c0105-142">**visX** (MoveTo, LineTo, ArcTo, EllipticalArcTo, NURBSTo, Polyline, SplineStart, and SplineKnot rows)</span></span>  <br/> |
||<span data-ttu-id="c0105-143">**visInfiniteLineX1** (строка InfiniteLine)</span><span class="sxs-lookup"><span data-stu-id="c0105-143">**visInfiniteLineX1** (InfiniteLine row)</span></span>  <br/> |
||<span data-ttu-id="c0105-144">**visEllipseCenterX** (строка Ellipse)</span><span class="sxs-lookup"><span data-stu-id="c0105-144">**visEllipseCenterX** (Ellipse row)</span></span>  <br/> |
   

