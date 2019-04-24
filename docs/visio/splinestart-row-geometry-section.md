---
title: SplineStart Row (Geometry Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm3055
localization_priority: Normal
ms.assetid: 8e327e00-0844-efa4-900b-6954d3b009bb
description: Содержит координаты x и y для второй контрольной точки сплайна, второй Кнот, ее первый Кнот, последний кнот и степень сплайна.
ms.openlocfilehash: 2ec06619770af4e5dbcc1a763595b6e01a39052b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32358795"
---
# <a name="splinestart-row-geometry-section"></a><span data-ttu-id="4ad8c-103">SplineStart Row (Geometry Section)</span><span class="sxs-lookup"><span data-stu-id="4ad8c-103">SplineStart Row (Geometry Section)</span></span>

<span data-ttu-id="4ad8c-104">Содержит координаты *x* и *y* для второй контрольной точки сплайна, второй Кнот, ее первый Кнот, последний кнот и степень сплайна.</span><span class="sxs-lookup"><span data-stu-id="4ad8c-104">Contains  *x*  - and  *y*  -coordinates for a spline's second control point, its second knot, its first knot, the last knot, and the degree of the spline.</span></span> 
  
<span data-ttu-id="4ad8c-105">Строка строка splinestart содержит следующие ячейки.</span><span class="sxs-lookup"><span data-stu-id="4ad8c-105">A SplineStart row contains the following cells.</span></span>
  
|<span data-ttu-id="4ad8c-106">**Cell**</span><span class="sxs-lookup"><span data-stu-id="4ad8c-106">**Cell**</span></span>|<span data-ttu-id="4ad8c-107">**Описание**</span><span class="sxs-lookup"><span data-stu-id="4ad8c-107">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="4ad8c-108">X</span><span class="sxs-lookup"><span data-stu-id="4ad8c-108">X</span></span>](x-cell-geometry-section.md) <br/> |<span data-ttu-id="4ad8c-109">Координата *X* второй контрольной точки сплайна.</span><span class="sxs-lookup"><span data-stu-id="4ad8c-109">The  *x*  -coordinate of a spline's second control point.</span></span>  <br/> |
|[<span data-ttu-id="4ad8c-110">Y (да)</span><span class="sxs-lookup"><span data-stu-id="4ad8c-110">Y</span></span>](y-cell-geometry-section.md) <br/> |<span data-ttu-id="4ad8c-111">Координата *Y* второй контрольной точки сплайна.</span><span class="sxs-lookup"><span data-stu-id="4ad8c-111">The  *y*  -coordinate of a spline's second control point.</span></span>  <br/> |
|[<span data-ttu-id="4ad8c-112">А</span><span class="sxs-lookup"><span data-stu-id="4ad8c-112">A</span></span>](a-cell-geometry-section.md) <br/> |<span data-ttu-id="4ad8c-113">Второй кнот сплайна.</span><span class="sxs-lookup"><span data-stu-id="4ad8c-113">The second knot of the spline.</span></span>  <br/> |
|[<span data-ttu-id="4ad8c-114">З</span><span class="sxs-lookup"><span data-stu-id="4ad8c-114">B</span></span>](b-cell-geometry-section.md) <br/> |<span data-ttu-id="4ad8c-115">Первый кнот сплайна.</span><span class="sxs-lookup"><span data-stu-id="4ad8c-115">The first knot of a spline.</span></span>  <br/> |
|[<span data-ttu-id="4ad8c-116">C</span><span class="sxs-lookup"><span data-stu-id="4ad8c-116">C</span></span>](c-cell-geometry-section.md) <br/> |<span data-ttu-id="4ad8c-117">Последний кнот сплайна.</span><span class="sxs-lookup"><span data-stu-id="4ad8c-117">The last knot of a spline.</span></span>  <br/> |
|[<span data-ttu-id="4ad8c-118">D</span><span class="sxs-lookup"><span data-stu-id="4ad8c-118">D</span></span>](d-cell-geometry-section.md) <br/> |<span data-ttu-id="4ad8c-119">Степень сплайна (целое число от 1 до 25).</span><span class="sxs-lookup"><span data-stu-id="4ad8c-119">The degree of a spline (an integer from 1 to 25).</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="4ad8c-120">Примечания</span><span class="sxs-lookup"><span data-stu-id="4ad8c-120">Remarks</span></span>

<span data-ttu-id="4ad8c-121">Visio отображает определение сплайна в геометрическом разделе, содержащем строку строка splinestart, за которой следует одна или несколько строк строка splineknot.</span><span class="sxs-lookup"><span data-stu-id="4ad8c-121">Visio displays the definition of a spline in a Geometry section that contains a SplineStart row followed by one or more SplineKnot rows.</span></span> <span data-ttu-id="4ad8c-122">Строке строка splinestart должен предшествовать другой тип строки, например строка MoveTo, чтобы показать первую контрольную точку сплайна.</span><span class="sxs-lookup"><span data-stu-id="4ad8c-122">The SplineStart row must be preceded by another kind of row, such as a MoveTo row, to indicate the first control point of the spline.</span></span> <span data-ttu-id="4ad8c-123">Предыдущая строка может быть строкой LineTo, строка ArcTo, NURBSTo, полисплайна или строка ellipticalarcto, если сплайн соответствует сегменту этого типа.</span><span class="sxs-lookup"><span data-stu-id="4ad8c-123">The preceding row can be a LineTo, ArcTo, NURBSTo, PolylineTo, or EllipticalArcTo row if the spline follows a segment of that type.</span></span>
  

