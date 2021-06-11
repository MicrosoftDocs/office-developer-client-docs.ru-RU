---
title: SplineKnot Row (Geometry Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm3050
localization_priority: Normal
ms.assetid: 9fbae27d-4f1b-c5f7-aacb-16f359331e83
description: Содержит x и y-координаты для точки управления spline и узла spline.
ms.openlocfilehash: 432b714772d96e0ab0861bbfb62075258404e607
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407419"
---
# <a name="splineknot-row-geometry-section"></a><span data-ttu-id="a880c-103">SplineKnot Row (Geometry Section)</span><span class="sxs-lookup"><span data-stu-id="a880c-103">SplineKnot Row (Geometry Section)</span></span>

<span data-ttu-id="a880c-104">Содержит  *x*  и  *y-координаты*  для точки управления spline и узла spline.</span><span class="sxs-lookup"><span data-stu-id="a880c-104">Contains  *x*  - and  *y*  -coordinates for a spline's control point and a spline's knot.</span></span> 
  
<span data-ttu-id="a880c-105">Строка SplineKnot содержит следующие ячейки.</span><span class="sxs-lookup"><span data-stu-id="a880c-105">A SplineKnot row contains the following cells.</span></span>
  
|<span data-ttu-id="a880c-106">**Cell**</span><span class="sxs-lookup"><span data-stu-id="a880c-106">**Cell**</span></span>|<span data-ttu-id="a880c-107">**Описание**</span><span class="sxs-lookup"><span data-stu-id="a880c-107">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="a880c-108">X</span><span class="sxs-lookup"><span data-stu-id="a880c-108">X</span></span>](x-cell-geometry-section.md) <br/> |<span data-ttu-id="a880c-109">Координата *X* контрольной точки.</span><span class="sxs-lookup"><span data-stu-id="a880c-109">The  *x*  -coordinate of a control point.</span></span>  <br/> |
|[<span data-ttu-id="a880c-110">Да</span><span class="sxs-lookup"><span data-stu-id="a880c-110">Y</span></span>](y-cell-geometry-section.md) <br/> |<span data-ttu-id="a880c-111">Координата *Y* контрольной точки.</span><span class="sxs-lookup"><span data-stu-id="a880c-111">The  *y*  -coordinate of a control point.</span></span>  <br/> |
|[<span data-ttu-id="a880c-112">A</span><span class="sxs-lookup"><span data-stu-id="a880c-112">A</span></span>](a-cell-geometry-section.md) <br/> |<span data-ttu-id="a880c-113">Один из узлов spline (кроме последнего или первых двух).</span><span class="sxs-lookup"><span data-stu-id="a880c-113">One of the spline's knots (other than the last one or the first two).</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a880c-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="a880c-114">Remarks</span></span>

<span data-ttu-id="a880c-115">Visio отображает определение spline в разделе Геометрия, содержаще строку SplineStart, а затем одну или несколько строк SplineKnot.</span><span class="sxs-lookup"><span data-stu-id="a880c-115">Visio displays the definition of a spline in a Geometry section that contains a SplineStart row followed by one or more SplineKnot rows.</span></span> <span data-ttu-id="a880c-116">Строке SplineStart должен предшествовать другой вид строки, например строка MoveTo, чтобы указать первую точку управления spline.</span><span class="sxs-lookup"><span data-stu-id="a880c-116">The SplineStart row must be preceded by another kind of row, such as a MoveTo row, to indicate the first control point of the spline.</span></span> <span data-ttu-id="a880c-117">В предыдущей строке может быть строка LineTo, ArcTo, NURBSTo, PolylineTo или EllipticalArcTo, если spline следует сегменту этого типа.</span><span class="sxs-lookup"><span data-stu-id="a880c-117">The preceding row can be a LineTo, ArcTo, NURBSTo, PolylineTo, or EllipticalArcTo row if the spline follows a segment of that type.</span></span>
  

