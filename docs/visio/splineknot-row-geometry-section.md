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
description: Содержит координаты x и y для контрольной точки сплайна и кнотного сплайна.
ms.openlocfilehash: 432b714772d96e0ab0861bbfb62075258404e607
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328128"
---
# <a name="splineknot-row-geometry-section"></a><span data-ttu-id="d4536-103">SplineKnot Row (Geometry Section)</span><span class="sxs-lookup"><span data-stu-id="d4536-103">SplineKnot Row (Geometry Section)</span></span>

<span data-ttu-id="d4536-104">Содержит координаты *x* и *y* для контрольной точки сплайна и кнотного сплайна.</span><span class="sxs-lookup"><span data-stu-id="d4536-104">Contains  *x*  - and  *y*  -coordinates for a spline's control point and a spline's knot.</span></span> 
  
<span data-ttu-id="d4536-105">Строка строка splineknot содержит следующие ячейки.</span><span class="sxs-lookup"><span data-stu-id="d4536-105">A SplineKnot row contains the following cells.</span></span>
  
|<span data-ttu-id="d4536-106">**Cell**</span><span class="sxs-lookup"><span data-stu-id="d4536-106">**Cell**</span></span>|<span data-ttu-id="d4536-107">**Описание**</span><span class="sxs-lookup"><span data-stu-id="d4536-107">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="d4536-108">X</span><span class="sxs-lookup"><span data-stu-id="d4536-108">X</span></span>](x-cell-geometry-section.md) <br/> |<span data-ttu-id="d4536-109">Координата *X* контрольной точки.</span><span class="sxs-lookup"><span data-stu-id="d4536-109">The  *x*  -coordinate of a control point.</span></span>  <br/> |
|[<span data-ttu-id="d4536-110">Y (да)</span><span class="sxs-lookup"><span data-stu-id="d4536-110">Y</span></span>](y-cell-geometry-section.md) <br/> |<span data-ttu-id="d4536-111">Координата *Y* контрольной точки.</span><span class="sxs-lookup"><span data-stu-id="d4536-111">The  *y*  -coordinate of a control point.</span></span>  <br/> |
|[<span data-ttu-id="d4536-112">Определенно</span><span class="sxs-lookup"><span data-stu-id="d4536-112">A</span></span>](a-cell-geometry-section.md) <br/> |<span data-ttu-id="d4536-113">Один из Кнотс сплайна (отличный от последнего или первых двух).</span><span class="sxs-lookup"><span data-stu-id="d4536-113">One of the spline's knots (other than the last one or the first two).</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d4536-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="d4536-114">Remarks</span></span>

<span data-ttu-id="d4536-115">Visio отображает определение сплайна в геометрическом разделе, содержащем строку строка splinestart, за которой следует одна или несколько строк строка splineknot.</span><span class="sxs-lookup"><span data-stu-id="d4536-115">Visio displays the definition of a spline in a Geometry section that contains a SplineStart row followed by one or more SplineKnot rows.</span></span> <span data-ttu-id="d4536-116">Строке строка splinestart должен предшествовать другой тип строки, например строка MoveTo, чтобы показать первую контрольную точку сплайна.</span><span class="sxs-lookup"><span data-stu-id="d4536-116">The SplineStart row must be preceded by another kind of row, such as a MoveTo row, to indicate the first control point of the spline.</span></span> <span data-ttu-id="d4536-117">Предыдущая строка может быть строкой LineTo, строка ArcTo, NURBSTo, полисплайна или строка ellipticalarcto, если сплайн соответствует сегменту этого типа.</span><span class="sxs-lookup"><span data-stu-id="d4536-117">The preceding row can be a LineTo, ArcTo, NURBSTo, PolylineTo, or EllipticalArcTo row if the spline follows a segment of that type.</span></span>
  

