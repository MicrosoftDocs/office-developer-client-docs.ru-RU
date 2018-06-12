---
title: Строка SplineKnot (раздел геометрии)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm3050
localization_priority: Normal
ms.assetid: 9fbae27d-4f1b-c5f7-aacb-16f359331e83
description: Содержит x - и y-координаты точки управления сплайн и число узлов сплайна.
ms.openlocfilehash: 297889208e064870dd37ed45a17fef7cb4b333b7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19814934"
---
# <a name="splineknot-row-geometry-section"></a><span data-ttu-id="9893d-103">Строка SplineKnot (раздел геометрии)</span><span class="sxs-lookup"><span data-stu-id="9893d-103">SplineKnot Row (Geometry Section)</span></span>

<span data-ttu-id="9893d-104">Содержит *x* - и *y* -координаты точки управления сплайн и число узлов сплайна.</span><span class="sxs-lookup"><span data-stu-id="9893d-104">Contains  *x*  - and  *y*  -coordinates for a spline's control point and a spline's knot.</span></span> 
  
<span data-ttu-id="9893d-105">Строка SplineKnot содержит следующие ячейки.</span><span class="sxs-lookup"><span data-stu-id="9893d-105">A SplineKnot row contains the following cells.</span></span>
  
|<span data-ttu-id="9893d-106">**Cell**</span><span class="sxs-lookup"><span data-stu-id="9893d-106">**Cell**</span></span>|<span data-ttu-id="9893d-107">**Описание**</span><span class="sxs-lookup"><span data-stu-id="9893d-107">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="9893d-108">X</span><span class="sxs-lookup"><span data-stu-id="9893d-108">X</span></span>](x-cell-geometry-section.md) <br/> |<span data-ttu-id="9893d-109">*X* -координата точки управления.</span><span class="sxs-lookup"><span data-stu-id="9893d-109">The  *x*  -coordinate of a control point.</span></span>  <br/> |
|[<span data-ttu-id="9893d-110">Y</span><span class="sxs-lookup"><span data-stu-id="9893d-110">Y</span></span>](y-cell-geometry-section.md) <br/> |<span data-ttu-id="9893d-111">*Y* -координата точки управления.</span><span class="sxs-lookup"><span data-stu-id="9893d-111">The  *y*  -coordinate of a control point.</span></span>  <br/> |
|[<span data-ttu-id="9893d-112">A</span><span class="sxs-lookup"><span data-stu-id="9893d-112">A</span></span>](a-cell-geometry-section.md) <br/> |<span data-ttu-id="9893d-113">Один из узлов сплайна (кроме последней или первых двух).</span><span class="sxs-lookup"><span data-stu-id="9893d-113">One of the spline's knots (other than the last one or the first two).</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="9893d-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="9893d-114">Remarks</span></span>

<span data-ttu-id="9893d-115">Visio отображается определение сплайна в раздел геометрии, в котором содержится строка SplineStart, а затем одна или несколько строк SplineKnot.</span><span class="sxs-lookup"><span data-stu-id="9893d-115">Visio displays the definition of a spline in a Geometry section that contains a SplineStart row followed by one or more SplineKnot rows.</span></span> <span data-ttu-id="9893d-116">Строка SplineStart должен предшествовать строки, например MoveTo строку, чтобы указать, первый элемент управления точкой для другого типа.</span><span class="sxs-lookup"><span data-stu-id="9893d-116">The SplineStart row must be preceded by another kind of row, such as a MoveTo row, to indicate the first control point of the spline.</span></span> <span data-ttu-id="9893d-117">Предыдущей строке может быть строкой LineTo, ArcTo, NURBSTo, PolylineTo или EllipticalArcTo сплайн за сегмент этого типа.</span><span class="sxs-lookup"><span data-stu-id="9893d-117">The preceding row can be a LineTo, ArcTo, NURBSTo, PolylineTo, or EllipticalArcTo row if the spline follows a segment of that type.</span></span>
  

