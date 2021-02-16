---
title: Geometry Section
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm2055
localization_priority: Normal
ms.assetid: 75601a1e-6b1a-27ee-a2bd-69e569315982
description: Содержит строки, которые перечисляют координаты вершин для линий и дуг, которые составляют фигуру.
ms.openlocfilehash: d45f960ecc697dc6f0f5a0efa18e6cbbc6e4fff0
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/29/2019
ms.locfileid: "34542284"
---
# <a name="geometry-section"></a><span data-ttu-id="fa81e-103">Geometry Section</span><span class="sxs-lookup"><span data-stu-id="fa81e-103">Geometry Section</span></span>

<span data-ttu-id="fa81e-104">Содержит строки, которые перечисляют координаты вершин для линий и дуг, которые составляют фигуру.</span><span class="sxs-lookup"><span data-stu-id="fa81e-104">Contains rows that list the coordinates of the vertices for the lines and arcs that make up the shape.</span></span> 
  
<span data-ttu-id="fa81e-105">Геометрия фигуры может быть выражена в нескольких **разделах геометрии.**</span><span class="sxs-lookup"><span data-stu-id="fa81e-105">The geometry of a shape can be expressed in multiple **Geometry** sections.</span></span> <span data-ttu-id="fa81e-106">Несколько путей могут быть полезны, если у нескольких путей [](clippingpath-cell-foreign-image-info-section.md) разные свойства (например, пути обрезки изображений).</span><span class="sxs-lookup"><span data-stu-id="fa81e-106">Multiple paths can be useful when multiple paths have different properties (e.g. [image clipping](clippingpath-cell-foreign-image-info-section.md) paths).</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="fa81e-107">Примечания</span><span class="sxs-lookup"><span data-stu-id="fa81e-107">Remarks</span></span>

<span data-ttu-id="fa81e-108">Раздел **"Геометрия"** содержит следующие типы строк.</span><span class="sxs-lookup"><span data-stu-id="fa81e-108">The **Geometry** section contains the following row types.</span></span> <span data-ttu-id="fa81e-109">Подробные сведения см. в темах по строкам.</span><span class="sxs-lookup"><span data-stu-id="fa81e-109">For details, see the row topics.</span></span> 
  
|<span data-ttu-id="fa81e-110">Строка</span><span class="sxs-lookup"><span data-stu-id="fa81e-110">Row</span></span>|<span data-ttu-id="fa81e-111">Описание</span><span class="sxs-lookup"><span data-stu-id="fa81e-111">Description</span></span>|
|:-----|:-----|
|[<span data-ttu-id="fa81e-112">MoveTo</span><span class="sxs-lookup"><span data-stu-id="fa81e-112">MoveTo</span></span>](moveto-row-geometry-section.md) <br/> |<span data-ttu-id="fa81e-113">Перейти к координате.</span><span class="sxs-lookup"><span data-stu-id="fa81e-113">Move to a coordinate.</span></span>  <br/> |
|[<span data-ttu-id="fa81e-114">LineTo</span><span class="sxs-lookup"><span data-stu-id="fa81e-114">LineTo</span></span>](lineto-row-geometry-section.md) <br/> |<span data-ttu-id="fa81e-115">Нарисуйте линию в координату.</span><span class="sxs-lookup"><span data-stu-id="fa81e-115">Draw a line to a coordinate.</span></span>  <br/> |
|[<span data-ttu-id="fa81e-116">ArcTo</span><span class="sxs-lookup"><span data-stu-id="fa81e-116">ArcTo</span></span>](arcto-row-geometry-section.md) <br/> |<span data-ttu-id="fa81e-117">Нарисуйте циклическая дуга к координате.</span><span class="sxs-lookup"><span data-stu-id="fa81e-117">Draw a circular arc to a coordinate.</span></span>  <br/> |
|[<span data-ttu-id="fa81e-118">EllipticalArcTo</span><span class="sxs-lookup"><span data-stu-id="fa81e-118">EllipticalArcTo</span></span>](ellipticalarcto-row-geometry-section.md) <br/> |<span data-ttu-id="fa81e-119">Нарисуйте эллиптическую дугу в координате.</span><span class="sxs-lookup"><span data-stu-id="fa81e-119">Draw an elliptical arc to a coordinate.</span></span>  <br/> |
|[<span data-ttu-id="fa81e-120">PolylineTo</span><span class="sxs-lookup"><span data-stu-id="fa81e-120">PolylineTo</span></span>](polylineto-row-geometry-section.md) <br/> |<span data-ttu-id="fa81e-121">Нарисуйте многолинейную или последовательные линии в координате.</span><span class="sxs-lookup"><span data-stu-id="fa81e-121">Draw a polyline, or consecutive lines, to a coordinate.</span></span>  <br/> |
|[<span data-ttu-id="fa81e-122">NURBSTo</span><span class="sxs-lookup"><span data-stu-id="fa81e-122">NURBSTo</span></span>](nurbsto-row-geometry-section.md) <br/> |<span data-ttu-id="fa81e-123">Нарисуйте не однородный логический B-spline (NURBS) в координате.</span><span class="sxs-lookup"><span data-stu-id="fa81e-123">Draw a non-uniform rational B-spline (NURBS) to a coordinate.</span></span>  <br/> |
|[<span data-ttu-id="fa81e-124">SplineStart</span><span class="sxs-lookup"><span data-stu-id="fa81e-124">SplineStart</span></span>](splinestart-row-geometry-section.md) <br/> |<span data-ttu-id="fa81e-125">Запустите spline.</span><span class="sxs-lookup"><span data-stu-id="fa81e-125">Start a spline.</span></span>  <br/> |
|[<span data-ttu-id="fa81e-126">SplineKnot</span><span class="sxs-lookup"><span data-stu-id="fa81e-126">SplineKnot</span></span>](splineknot-row-geometry-section.md) <br/> |<span data-ttu-id="fa81e-127">Отрисовка сегмента сплайна в координате координаты координаты.</span><span class="sxs-lookup"><span data-stu-id="fa81e-127">Draw a spline segment to a knot coordinate.</span></span>  <br/> |
|[<span data-ttu-id="fa81e-128">InfiniteLine</span><span class="sxs-lookup"><span data-stu-id="fa81e-128">InfiniteLine</span></span>](infiniteline-row-geometry-section.md) <br/> |<span data-ttu-id="fa81e-129">Нарисуйте бесконечное число строк из одной координаты в другую.</span><span class="sxs-lookup"><span data-stu-id="fa81e-129">Draw an infinite line from one coordinate to another.</span></span>  <br/> |
|[<span data-ttu-id="fa81e-130">Ellipse</span><span class="sxs-lookup"><span data-stu-id="fa81e-130">Ellipse</span></span>](ellipse-row-geometry-section.md) <br/> |<span data-ttu-id="fa81e-131">Нарисуйте эллипс из центральной координаты и основной или второстепенной оси.</span><span class="sxs-lookup"><span data-stu-id="fa81e-131">Draw an ellipse from a center coordinate and a major/minor axis.</span></span>  <br/> |
|[<span data-ttu-id="fa81e-132">RelCubBezTo</span><span class="sxs-lookup"><span data-stu-id="fa81e-132">RelCubBezTo</span></span>](relcubbezto-row-geometry-section.md) <br/> |<span data-ttu-id="fa81e-133">Нарисуйте кривая Безье по ширине и высоте фигуры.</span><span class="sxs-lookup"><span data-stu-id="fa81e-133">Draw a cubic Bezier curve relative to the width and height of the shape.</span></span>  <br/> |
|[<span data-ttu-id="fa81e-134">RelEllipticalArcTo</span><span class="sxs-lookup"><span data-stu-id="fa81e-134">RelEllipticalArcTo</span></span>](relellipticalarcto-row-geometry-section.md) <br/> |<span data-ttu-id="fa81e-135">Нарисуйте эллиптическую дугу к координате относительно высоты и ширины фигуры.</span><span class="sxs-lookup"><span data-stu-id="fa81e-135">Draw an elliptical arc to a coordinate relative to the height and width of the shape.</span></span>  <br/> |
|[<span data-ttu-id="fa81e-136">RelLineTo</span><span class="sxs-lookup"><span data-stu-id="fa81e-136">RelLineTo</span></span>](rellineto-row-geometry-section.md) <br/> |<span data-ttu-id="fa81e-137">Нарисуйте линию к координате относительно высоты и ширины фигуры.</span><span class="sxs-lookup"><span data-stu-id="fa81e-137">Draw a line to a coordinate relative the height and width of a shape.</span></span>  <br/> |
|[<span data-ttu-id="fa81e-138">RelMoveTo</span><span class="sxs-lookup"><span data-stu-id="fa81e-138">RelMoveTo</span></span>](relmoveto-row-geometry-section.md) <br/> |<span data-ttu-id="fa81e-139">Перемещение к координате относительно ширины и высоты фигуры.</span><span class="sxs-lookup"><span data-stu-id="fa81e-139">Move to a coordinate relative to the width and height of the shape.</span></span>  <br/> |
|[<span data-ttu-id="fa81e-140">RelQuadBezTo</span><span class="sxs-lookup"><span data-stu-id="fa81e-140">RelQuadBezTo</span></span>](relquadbezto-row-geometry-section.md) <br/> |<span data-ttu-id="fa81e-141">Рисует кривую Безье четверного безье относительно ширины и высоты фигуры.</span><span class="sxs-lookup"><span data-stu-id="fa81e-141">Draws a quadratic Bezier curve relative to the width and height of the shape.</span></span>  <br/> |
   
<span data-ttu-id="fa81e-142">Чтобы изменить тип строки в этом разделе, щелкните  ее правой кнопкой мыши и выберите пункт "Изменить тип строки" в ярлыковом меню.</span><span class="sxs-lookup"><span data-stu-id="fa81e-142">To change a row type in this section, right-click the row, and then click **Change Row Type** on the shortcut menu.</span></span> 
  

