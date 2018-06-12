---
title: Раздел геометрии
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm2055
localization_priority: Normal
ms.assetid: 75601a1e-6b1a-27ee-a2bd-69e569315982
description: Содержит строки, в которых перечислены координаты грани для линий и дуг, образующих фигуру.
ms.openlocfilehash: 59f85c512b7038f6cfddcb657435730a2e724bd6
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19813839"
---
# <a name="geometry-section"></a><span data-ttu-id="7f615-103">Раздел геометрии</span><span class="sxs-lookup"><span data-stu-id="7f615-103">Geometry Section</span></span>

<span data-ttu-id="7f615-104">Содержит строки, в которых перечислены координаты грани для линий и дуг, образующих фигуру.</span><span class="sxs-lookup"><span data-stu-id="7f615-104">Contains rows that list the coordinates of the vertices for the lines and arcs that make up the shape.</span></span> 
  
<span data-ttu-id="7f615-105">Геометрия фигуры может быть выражено в нескольких разделах **геометрии** .</span><span class="sxs-lookup"><span data-stu-id="7f615-105">The geometry of a shape can be expressed in multiple **Geometry** sections.</span></span> <span data-ttu-id="7f615-106">Несколько путей можно использовать при нескольких путей иметь различные свойства (например, пути [кадрирование изображений](clippingpath-cell-foreign-image-info-section.md) ).</span><span class="sxs-lookup"><span data-stu-id="7f615-106">Multiple paths can be useful when multiple paths have different properties (e.g. [image clipping](clippingpath-cell-foreign-image-info-section.md) paths).</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="7f615-107">Замечания</span><span class="sxs-lookup"><span data-stu-id="7f615-107">Remarks</span></span>

<span data-ttu-id="7f615-108">Раздел **геометрии** содержит следующие типы строки.</span><span class="sxs-lookup"><span data-stu-id="7f615-108">The **Geometry** section contains the following row types.</span></span> <span data-ttu-id="7f615-109">Дополнительные сведения см в разделах строки.</span><span class="sxs-lookup"><span data-stu-id="7f615-109">For details, see the row topics.</span></span> 
  
|<span data-ttu-id="7f615-110">**Row**</span><span class="sxs-lookup"><span data-stu-id="7f615-110">**Row**</span></span>|<span data-ttu-id="7f615-111">**Описание**</span><span class="sxs-lookup"><span data-stu-id="7f615-111">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="7f615-112">MoveTo</span><span class="sxs-lookup"><span data-stu-id="7f615-112">MoveTo</span></span>](moveto-row-geometry-section.md) <br/> |<span data-ttu-id="7f615-113">Перемещение координаты.</span><span class="sxs-lookup"><span data-stu-id="7f615-113">Move to a coordinate.</span></span>  <br/> |
|[<span data-ttu-id="7f615-114">LineTo</span><span class="sxs-lookup"><span data-stu-id="7f615-114">LineTo</span></span>](lineto-row-geometry-section.md) <br/> |<span data-ttu-id="7f615-115">Линии координаты.</span><span class="sxs-lookup"><span data-stu-id="7f615-115">Draw a line to a coordinate.</span></span>  <br/> |
|[<span data-ttu-id="7f615-116">ArcTo</span><span class="sxs-lookup"><span data-stu-id="7f615-116">ArcTo</span></span>](arcto-row-geometry-section.md) <br/> |<span data-ttu-id="7f615-117">Нарисуйте дугу координаты.</span><span class="sxs-lookup"><span data-stu-id="7f615-117">Draw a circular arc to a coordinate.</span></span>  <br/> |
|[<span data-ttu-id="7f615-118">EllipticalArcTo</span><span class="sxs-lookup"><span data-stu-id="7f615-118">EllipticalArcTo</span></span>](ellipticalarcto-row-geometry-section.md) <br/> |<span data-ttu-id="7f615-119">Создайте руководство, чтобы координаты.</span><span class="sxs-lookup"><span data-stu-id="7f615-119">Draw an elliptical arc to a coordinate.</span></span>  <br/> |
|[<span data-ttu-id="7f615-120">PolylineTo</span><span class="sxs-lookup"><span data-stu-id="7f615-120">PolylineTo</span></span>](polylineto-row-geometry-section.md) <br/> |<span data-ttu-id="7f615-121">Рисование ломаной или последовательных строк для координаты.</span><span class="sxs-lookup"><span data-stu-id="7f615-121">Draw a polyline, or consecutive lines, to a coordinate.</span></span>  <br/> |
|[<span data-ttu-id="7f615-122">NURBSTo</span><span class="sxs-lookup"><span data-stu-id="7f615-122">NURBSTo</span></span>](nurbsto-row-geometry-section.md) <br/> |<span data-ttu-id="7f615-123">Создавать неоднородной rational-сплайн (NURBS), чтобы координаты.</span><span class="sxs-lookup"><span data-stu-id="7f615-123">Draw a non-uniform rational B-spline (NURBS) to a coordinate.</span></span>  <br/> |
|[<span data-ttu-id="7f615-124">SplineStart</span><span class="sxs-lookup"><span data-stu-id="7f615-124">SplineStart</span></span>](splinestart-row-geometry-section.md) <br/> |<span data-ttu-id="7f615-125">Запустите сплайна.</span><span class="sxs-lookup"><span data-stu-id="7f615-125">Start a spline.</span></span>  <br/> |
|[<span data-ttu-id="7f615-126">SplineKnot</span><span class="sxs-lookup"><span data-stu-id="7f615-126">SplineKnot</span></span>](splineknot-row-geometry-section.md) <br/> |<span data-ttu-id="7f615-127">Нарисуйте сегмента сплайна координата число узлов.</span><span class="sxs-lookup"><span data-stu-id="7f615-127">Draw a spline segment to a knot coordinate.</span></span>  <br/> |
|[<span data-ttu-id="7f615-128">InfiniteLine</span><span class="sxs-lookup"><span data-stu-id="7f615-128">InfiniteLine</span></span>](infiniteline-row-geometry-section.md) <br/> |<span data-ttu-id="7f615-129">Рисование бесконечное строки из одного координат в другую.</span><span class="sxs-lookup"><span data-stu-id="7f615-129">Draw an infinite line from one coordinate to another.</span></span>  <br/> |
|[<span data-ttu-id="7f615-130">Эллипс</span><span class="sxs-lookup"><span data-stu-id="7f615-130">Ellipse</span></span>](ellipse-row-geometry-section.md) <br/> |<span data-ttu-id="7f615-131">Рисование эллипсы из центра координат и основные и вспомогательные оси.</span><span class="sxs-lookup"><span data-stu-id="7f615-131">Draw an ellipse from a center coordinate and a major/minor axis.</span></span>  <br/> |
|[<span data-ttu-id="7f615-132">RelCubBezTo</span><span class="sxs-lookup"><span data-stu-id="7f615-132">RelCubBezTo</span></span>](relcubbezto-row-geometry-section.md) <br/> |<span data-ttu-id="7f615-133">Рисование кубические Безье график относительно ширину и высоту фигуры.</span><span class="sxs-lookup"><span data-stu-id="7f615-133">Draw a cubic Bezier curve relative to the width and height of the shape.</span></span>  <br/> |
|[<span data-ttu-id="7f615-134">RelEllipticalArcTo</span><span class="sxs-lookup"><span data-stu-id="7f615-134">RelEllipticalArcTo</span></span>](relellipticalarcto-row-geometry-section.md) <br/> |<span data-ttu-id="7f615-135">Рисование руководство для координат относительно высоту и ширину фигуры.</span><span class="sxs-lookup"><span data-stu-id="7f615-135">Draw an elliptical arc to a coordinate relative to the height and width of the shape.</span></span>  <br/> |
|[<span data-ttu-id="7f615-136">RelLineTo</span><span class="sxs-lookup"><span data-stu-id="7f615-136">RelLineTo</span></span>](rellineto-row-geometry-section.md) <br/> |<span data-ttu-id="7f615-137">Линии координат относительно высоту и ширину фигуры.</span><span class="sxs-lookup"><span data-stu-id="7f615-137">Draw a line to a coordinate relative the height and width of a shape.</span></span>  <br/> |
|[<span data-ttu-id="7f615-138">RelMoveTo</span><span class="sxs-lookup"><span data-stu-id="7f615-138">RelMoveTo</span></span>](relmoveto-row-geometry-section.md) <br/> |<span data-ttu-id="7f615-139">Перемещение координат относительно ширину и высоту фигуры.</span><span class="sxs-lookup"><span data-stu-id="7f615-139">Move to a coordinate relative to the width and height of the shape.</span></span>  <br/> |
|[<span data-ttu-id="7f615-140">RelQuadBezTo</span><span class="sxs-lookup"><span data-stu-id="7f615-140">RelQuadBezTo</span></span>](relquadbezto-row-geometry-section.md) <br/> |<span data-ttu-id="7f615-141">Рисование кривой Безье второго относительно ширину и высоту фигуры.</span><span class="sxs-lookup"><span data-stu-id="7f615-141">Draws a quadratic Bezier curve relative to the width and height of the shape.</span></span>  <br/> |
   
<span data-ttu-id="7f615-142">Чтобы изменить тип строки в этом разделе, щелкните правой кнопкой мыши строку и нажмите кнопку **Изменить тип строки** в контекстном меню.</span><span class="sxs-lookup"><span data-stu-id="7f615-142">To change a row type in this section, right-click the row, and then click **Change Row Type** on the shortcut menu.</span></span> 
  

