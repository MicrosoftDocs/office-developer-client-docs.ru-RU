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
description: Содержит строки, в которых перечислены координаты вершин для линий и дуг, составляющих фигуру.
ms.openlocfilehash: d45f960ecc697dc6f0f5a0efa18e6cbbc6e4fff0
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/29/2019
ms.locfileid: "34542284"
---
# <a name="geometry-section"></a><span data-ttu-id="4f65e-103">Geometry Section</span><span class="sxs-lookup"><span data-stu-id="4f65e-103">Geometry Section</span></span>

<span data-ttu-id="4f65e-104">Содержит строки, в которых перечислены координаты вершин для линий и дуг, составляющих фигуру.</span><span class="sxs-lookup"><span data-stu-id="4f65e-104">Contains rows that list the coordinates of the vertices for the lines and arcs that make up the shape.</span></span> 
  
<span data-ttu-id="4f65e-105">Геометрия фигуры может быть выражена в нескольких разделах **геометрии** .</span><span class="sxs-lookup"><span data-stu-id="4f65e-105">The geometry of a shape can be expressed in multiple **Geometry** sections.</span></span> <span data-ttu-id="4f65e-106">Несколько путей удобно использовать, если несколько путей имеют различные свойства (например, [обтравочные](clippingpath-cell-foreign-image-info-section.md) контуры изображений).</span><span class="sxs-lookup"><span data-stu-id="4f65e-106">Multiple paths can be useful when multiple paths have different properties (e.g. [image clipping](clippingpath-cell-foreign-image-info-section.md) paths).</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="4f65e-107">Примечания</span><span class="sxs-lookup"><span data-stu-id="4f65e-107">Remarks</span></span>

<span data-ttu-id="4f65e-108">Раздел " **геометрия** " содержит следующие типы строк.</span><span class="sxs-lookup"><span data-stu-id="4f65e-108">The **Geometry** section contains the following row types.</span></span> <span data-ttu-id="4f65e-109">Дополнительные сведения см.</span><span class="sxs-lookup"><span data-stu-id="4f65e-109">For details, see the row topics.</span></span> 
  
|<span data-ttu-id="4f65e-110">Строка</span><span class="sxs-lookup"><span data-stu-id="4f65e-110">Row</span></span>|<span data-ttu-id="4f65e-111">Описание</span><span class="sxs-lookup"><span data-stu-id="4f65e-111">Description</span></span>|
|:-----|:-----|
|[<span data-ttu-id="4f65e-112">MoveTo</span><span class="sxs-lookup"><span data-stu-id="4f65e-112">MoveTo</span></span>](moveto-row-geometry-section.md) <br/> |<span data-ttu-id="4f65e-113">Перейти к координате.</span><span class="sxs-lookup"><span data-stu-id="4f65e-113">Move to a coordinate.</span></span>  <br/> |
|[<span data-ttu-id="4f65e-114">LineTo</span><span class="sxs-lookup"><span data-stu-id="4f65e-114">LineTo</span></span>](lineto-row-geometry-section.md) <br/> |<span data-ttu-id="4f65e-115">Нарисуйте линию по координатам.</span><span class="sxs-lookup"><span data-stu-id="4f65e-115">Draw a line to a coordinate.</span></span>  <br/> |
|[<span data-ttu-id="4f65e-116">ArcTo</span><span class="sxs-lookup"><span data-stu-id="4f65e-116">ArcTo</span></span>](arcto-row-geometry-section.md) <br/> |<span data-ttu-id="4f65e-117">Рисование круговой дуги в координатах.</span><span class="sxs-lookup"><span data-stu-id="4f65e-117">Draw a circular arc to a coordinate.</span></span>  <br/> |
|[<span data-ttu-id="4f65e-118">EllipticalArcTo</span><span class="sxs-lookup"><span data-stu-id="4f65e-118">EllipticalArcTo</span></span>](ellipticalarcto-row-geometry-section.md) <br/> |<span data-ttu-id="4f65e-119">Нарисуйте эллиптическую дугу по координатам.</span><span class="sxs-lookup"><span data-stu-id="4f65e-119">Draw an elliptical arc to a coordinate.</span></span>  <br/> |
|[<span data-ttu-id="4f65e-120">PolylineTo</span><span class="sxs-lookup"><span data-stu-id="4f65e-120">PolylineTo</span></span>](polylineto-row-geometry-section.md) <br/> |<span data-ttu-id="4f65e-121">Рисование ломаной линии или последовательных линий в координатах.</span><span class="sxs-lookup"><span data-stu-id="4f65e-121">Draw a polyline, or consecutive lines, to a coordinate.</span></span>  <br/> |
|[<span data-ttu-id="4f65e-122">NURBSTo</span><span class="sxs-lookup"><span data-stu-id="4f65e-122">NURBSTo</span></span>](nurbsto-row-geometry-section.md) <br/> |<span data-ttu-id="4f65e-123">Рисование неоднородного рационального B-сплайна (NURBS) в координатах.</span><span class="sxs-lookup"><span data-stu-id="4f65e-123">Draw a non-uniform rational B-spline (NURBS) to a coordinate.</span></span>  <br/> |
|[<span data-ttu-id="4f65e-124">SplineStart</span><span class="sxs-lookup"><span data-stu-id="4f65e-124">SplineStart</span></span>](splinestart-row-geometry-section.md) <br/> |<span data-ttu-id="4f65e-125">Начало сплайна.</span><span class="sxs-lookup"><span data-stu-id="4f65e-125">Start a spline.</span></span>  <br/> |
|[<span data-ttu-id="4f65e-126">SplineKnot</span><span class="sxs-lookup"><span data-stu-id="4f65e-126">SplineKnot</span></span>](splineknot-row-geometry-section.md) <br/> |<span data-ttu-id="4f65e-127">Нарисуйте сегмент сплайна в координату кнот.</span><span class="sxs-lookup"><span data-stu-id="4f65e-127">Draw a spline segment to a knot coordinate.</span></span>  <br/> |
|[<span data-ttu-id="4f65e-128">InfiniteLine</span><span class="sxs-lookup"><span data-stu-id="4f65e-128">InfiniteLine</span></span>](infiniteline-row-geometry-section.md) <br/> |<span data-ttu-id="4f65e-129">Нарисуйте бесконечную линию от одной координаты к другой.</span><span class="sxs-lookup"><span data-stu-id="4f65e-129">Draw an infinite line from one coordinate to another.</span></span>  <br/> |
|[<span data-ttu-id="4f65e-130">Ellipse</span><span class="sxs-lookup"><span data-stu-id="4f65e-130">Ellipse</span></span>](ellipse-row-geometry-section.md) <br/> |<span data-ttu-id="4f65e-131">Рисование эллипса по Центральной координате и основной или дополнительной оси.</span><span class="sxs-lookup"><span data-stu-id="4f65e-131">Draw an ellipse from a center coordinate and a major/minor axis.</span></span>  <br/> |
|[<span data-ttu-id="4f65e-132">RelCubBezTo</span><span class="sxs-lookup"><span data-stu-id="4f65e-132">RelCubBezTo</span></span>](relcubbezto-row-geometry-section.md) <br/> |<span data-ttu-id="4f65e-133">Рисование кривой Безье третьего порядка относительно ширины и высоты фигуры.</span><span class="sxs-lookup"><span data-stu-id="4f65e-133">Draw a cubic Bezier curve relative to the width and height of the shape.</span></span>  <br/> |
|[<span data-ttu-id="4f65e-134">RelEllipticalArcTo</span><span class="sxs-lookup"><span data-stu-id="4f65e-134">RelEllipticalArcTo</span></span>](relellipticalarcto-row-geometry-section.md) <br/> |<span data-ttu-id="4f65e-135">Нарисуйте эллиптическую дугу по координатам относительно высоты и ширины фигуры.</span><span class="sxs-lookup"><span data-stu-id="4f65e-135">Draw an elliptical arc to a coordinate relative to the height and width of the shape.</span></span>  <br/> |
|[<span data-ttu-id="4f65e-136">RelLineTo</span><span class="sxs-lookup"><span data-stu-id="4f65e-136">RelLineTo</span></span>](rellineto-row-geometry-section.md) <br/> |<span data-ttu-id="4f65e-137">Рисование линии по координатам относительно высоты и ширины фигуры.</span><span class="sxs-lookup"><span data-stu-id="4f65e-137">Draw a line to a coordinate relative the height and width of a shape.</span></span>  <br/> |
|[<span data-ttu-id="4f65e-138">RelMoveTo</span><span class="sxs-lookup"><span data-stu-id="4f65e-138">RelMoveTo</span></span>](relmoveto-row-geometry-section.md) <br/> |<span data-ttu-id="4f65e-139">Переход на координату, связанную с шириной и высотой фигуры.</span><span class="sxs-lookup"><span data-stu-id="4f65e-139">Move to a coordinate relative to the width and height of the shape.</span></span>  <br/> |
|[<span data-ttu-id="4f65e-140">RelQuadBezTo</span><span class="sxs-lookup"><span data-stu-id="4f65e-140">RelQuadBezTo</span></span>](relquadbezto-row-geometry-section.md) <br/> |<span data-ttu-id="4f65e-141">Рисует кривую Безье второго размера относительно ширины и высоты фигуры.</span><span class="sxs-lookup"><span data-stu-id="4f65e-141">Draws a quadratic Bezier curve relative to the width and height of the shape.</span></span>  <br/> |
   
<span data-ttu-id="4f65e-142">Чтобы изменить тип строки в этом разделе, щелкните строку правой кнопкой мыши и выберите в контекстном меню команду **изменить тип строки** .</span><span class="sxs-lookup"><span data-stu-id="4f65e-142">To change a row type in this section, right-click the row, and then click **Change Row Type** on the shortcut menu.</span></span> 
  

