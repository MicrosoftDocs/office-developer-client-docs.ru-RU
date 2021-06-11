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
# <a name="geometry-section"></a><span data-ttu-id="3d1ad-103">Geometry Section</span><span class="sxs-lookup"><span data-stu-id="3d1ad-103">Geometry Section</span></span>

<span data-ttu-id="3d1ad-104">Содержит строки, которые перечисляют координаты вершин для линий и дуг, которые составляют фигуру.</span><span class="sxs-lookup"><span data-stu-id="3d1ad-104">Contains rows that list the coordinates of the vertices for the lines and arcs that make up the shape.</span></span> 
  
<span data-ttu-id="3d1ad-105">Геометрия фигуры может быть выражена в нескольких **разделах Геометрия.**</span><span class="sxs-lookup"><span data-stu-id="3d1ad-105">The geometry of a shape can be expressed in multiple **Geometry** sections.</span></span> <span data-ttu-id="3d1ad-106">Несколько путей могут быть полезны, если несколько путей имеют различные свойства (например, пути [вырезки изображений).](clippingpath-cell-foreign-image-info-section.md)</span><span class="sxs-lookup"><span data-stu-id="3d1ad-106">Multiple paths can be useful when multiple paths have different properties (e.g. [image clipping](clippingpath-cell-foreign-image-info-section.md) paths).</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="3d1ad-107">Примечания</span><span class="sxs-lookup"><span data-stu-id="3d1ad-107">Remarks</span></span>

<span data-ttu-id="3d1ad-108">Раздел **Geometry** содержит следующие типы строк.</span><span class="sxs-lookup"><span data-stu-id="3d1ad-108">The **Geometry** section contains the following row types.</span></span> <span data-ttu-id="3d1ad-109">Подробные сведения см. в разделе строки.</span><span class="sxs-lookup"><span data-stu-id="3d1ad-109">For details, see the row topics.</span></span> 
  
|<span data-ttu-id="3d1ad-110">Строка</span><span class="sxs-lookup"><span data-stu-id="3d1ad-110">Row</span></span>|<span data-ttu-id="3d1ad-111">Описание</span><span class="sxs-lookup"><span data-stu-id="3d1ad-111">Description</span></span>|
|:-----|:-----|
|[<span data-ttu-id="3d1ad-112">MoveTo</span><span class="sxs-lookup"><span data-stu-id="3d1ad-112">MoveTo</span></span>](moveto-row-geometry-section.md) <br/> |<span data-ttu-id="3d1ad-113">Перемещение в координаты.</span><span class="sxs-lookup"><span data-stu-id="3d1ad-113">Move to a coordinate.</span></span>  <br/> |
|[<span data-ttu-id="3d1ad-114">LineTo</span><span class="sxs-lookup"><span data-stu-id="3d1ad-114">LineTo</span></span>](lineto-row-geometry-section.md) <br/> |<span data-ttu-id="3d1ad-115">Нарисуйте строку в координату.</span><span class="sxs-lookup"><span data-stu-id="3d1ad-115">Draw a line to a coordinate.</span></span>  <br/> |
|[<span data-ttu-id="3d1ad-116">ArcTo</span><span class="sxs-lookup"><span data-stu-id="3d1ad-116">ArcTo</span></span>](arcto-row-geometry-section.md) <br/> |<span data-ttu-id="3d1ad-117">Нарисуйте круговую дугу в координаты.</span><span class="sxs-lookup"><span data-stu-id="3d1ad-117">Draw a circular arc to a coordinate.</span></span>  <br/> |
|[<span data-ttu-id="3d1ad-118">EllipticalArcTo</span><span class="sxs-lookup"><span data-stu-id="3d1ad-118">EllipticalArcTo</span></span>](ellipticalarcto-row-geometry-section.md) <br/> |<span data-ttu-id="3d1ad-119">Нарисуйте эллиптическую дугу в координаты.</span><span class="sxs-lookup"><span data-stu-id="3d1ad-119">Draw an elliptical arc to a coordinate.</span></span>  <br/> |
|[<span data-ttu-id="3d1ad-120">PolylineTo</span><span class="sxs-lookup"><span data-stu-id="3d1ad-120">PolylineTo</span></span>](polylineto-row-geometry-section.md) <br/> |<span data-ttu-id="3d1ad-121">Нарисуйте в координате полилин или последовательные строки.</span><span class="sxs-lookup"><span data-stu-id="3d1ad-121">Draw a polyline, or consecutive lines, to a coordinate.</span></span>  <br/> |
|[<span data-ttu-id="3d1ad-122">NURBSTo</span><span class="sxs-lookup"><span data-stu-id="3d1ad-122">NURBSTo</span></span>](nurbsto-row-geometry-section.md) <br/> |<span data-ttu-id="3d1ad-123">Нарисуйте не однородный рациональный B-spline (NURBS) в координату.</span><span class="sxs-lookup"><span data-stu-id="3d1ad-123">Draw a non-uniform rational B-spline (NURBS) to a coordinate.</span></span>  <br/> |
|[<span data-ttu-id="3d1ad-124">SplineStart</span><span class="sxs-lookup"><span data-stu-id="3d1ad-124">SplineStart</span></span>](splinestart-row-geometry-section.md) <br/> |<span data-ttu-id="3d1ad-125">Запустите spline.</span><span class="sxs-lookup"><span data-stu-id="3d1ad-125">Start a spline.</span></span>  <br/> |
|[<span data-ttu-id="3d1ad-126">SplineKnot</span><span class="sxs-lookup"><span data-stu-id="3d1ad-126">SplineKnot</span></span>](splineknot-row-geometry-section.md) <br/> |<span data-ttu-id="3d1ad-127">Нарисуйте сегмент spline в координату узла.</span><span class="sxs-lookup"><span data-stu-id="3d1ad-127">Draw a spline segment to a knot coordinate.</span></span>  <br/> |
|[<span data-ttu-id="3d1ad-128">InfiniteLine</span><span class="sxs-lookup"><span data-stu-id="3d1ad-128">InfiniteLine</span></span>](infiniteline-row-geometry-section.md) <br/> |<span data-ttu-id="3d1ad-129">Нарисуйте бесконечную линию из одной координаты в другую.</span><span class="sxs-lookup"><span data-stu-id="3d1ad-129">Draw an infinite line from one coordinate to another.</span></span>  <br/> |
|[<span data-ttu-id="3d1ad-130">Ellipse</span><span class="sxs-lookup"><span data-stu-id="3d1ad-130">Ellipse</span></span>](ellipse-row-geometry-section.md) <br/> |<span data-ttu-id="3d1ad-131">Нарисуйте эллипс из центральной координаты и оси мажор/минор.</span><span class="sxs-lookup"><span data-stu-id="3d1ad-131">Draw an ellipse from a center coordinate and a major/minor axis.</span></span>  <br/> |
|[<span data-ttu-id="3d1ad-132">RelCubBezTo</span><span class="sxs-lookup"><span data-stu-id="3d1ad-132">RelCubBezTo</span></span>](relcubbezto-row-geometry-section.md) <br/> |<span data-ttu-id="3d1ad-133">Нарисуйте кубический кривой Безье относительно ширины и высоты фигуры.</span><span class="sxs-lookup"><span data-stu-id="3d1ad-133">Draw a cubic Bezier curve relative to the width and height of the shape.</span></span>  <br/> |
|[<span data-ttu-id="3d1ad-134">RelEllipticalArcTo</span><span class="sxs-lookup"><span data-stu-id="3d1ad-134">RelEllipticalArcTo</span></span>](relellipticalarcto-row-geometry-section.md) <br/> |<span data-ttu-id="3d1ad-135">Нарисуйте эллиптическую дугу в координату относительно высоты и ширины фигуры.</span><span class="sxs-lookup"><span data-stu-id="3d1ad-135">Draw an elliptical arc to a coordinate relative to the height and width of the shape.</span></span>  <br/> |
|[<span data-ttu-id="3d1ad-136">RelLineTo</span><span class="sxs-lookup"><span data-stu-id="3d1ad-136">RelLineTo</span></span>](rellineto-row-geometry-section.md) <br/> |<span data-ttu-id="3d1ad-137">Нарисуйте строку в координате относительно высоты и ширины фигуры.</span><span class="sxs-lookup"><span data-stu-id="3d1ad-137">Draw a line to a coordinate relative the height and width of a shape.</span></span>  <br/> |
|[<span data-ttu-id="3d1ad-138">RelMoveTo</span><span class="sxs-lookup"><span data-stu-id="3d1ad-138">RelMoveTo</span></span>](relmoveto-row-geometry-section.md) <br/> |<span data-ttu-id="3d1ad-139">Перемещение в координаты относительно ширины и высоты фигуры.</span><span class="sxs-lookup"><span data-stu-id="3d1ad-139">Move to a coordinate relative to the width and height of the shape.</span></span>  <br/> |
|[<span data-ttu-id="3d1ad-140">RelQuadBezTo</span><span class="sxs-lookup"><span data-stu-id="3d1ad-140">RelQuadBezTo</span></span>](relquadbezto-row-geometry-section.md) <br/> |<span data-ttu-id="3d1ad-141">Рисует квадратную кривую Безье относительно ширины и высоты фигуры.</span><span class="sxs-lookup"><span data-stu-id="3d1ad-141">Draws a quadratic Bezier curve relative to the width and height of the shape.</span></span>  <br/> |
   
<span data-ttu-id="3d1ad-142">Чтобы изменить тип строки в этом разделе, щелкните правой кнопкой мыши строку и нажмите **кнопку Изменить** строку в меню ярлыка.</span><span class="sxs-lookup"><span data-stu-id="3d1ad-142">To change a row type in this section, right-click the row, and then click **Change Row Type** on the shortcut menu.</span></span> 
  

