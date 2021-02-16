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
description: Содержит координаты x и y для второй контрольной точки сплайна, его второй замещести, первой степени, последней затеи и степени сплайна.
ms.openlocfilehash: 2ec06619770af4e5dbcc1a763595b6e01a39052b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33417478"
---
# <a name="splinestart-row-geometry-section"></a><span data-ttu-id="d7402-103">SplineStart Row (Geometry Section)</span><span class="sxs-lookup"><span data-stu-id="d7402-103">SplineStart Row (Geometry Section)</span></span>

<span data-ttu-id="d7402-104">Содержит  *координаты x*  и  *y*  для второй контрольной точки сплайна, его второй замещести, первой степени, последней затеи и степени сплайна.</span><span class="sxs-lookup"><span data-stu-id="d7402-104">Contains  *x*  - and  *y*  -coordinates for a spline's second control point, its second knot, its first knot, the last knot, and the degree of the spline.</span></span> 
  
<span data-ttu-id="d7402-105">Строка SplineStart содержит следующие ячейки.</span><span class="sxs-lookup"><span data-stu-id="d7402-105">A SplineStart row contains the following cells.</span></span>
  
|<span data-ttu-id="d7402-106">**Cell**</span><span class="sxs-lookup"><span data-stu-id="d7402-106">**Cell**</span></span>|<span data-ttu-id="d7402-107">**Описание**</span><span class="sxs-lookup"><span data-stu-id="d7402-107">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="d7402-108">X</span><span class="sxs-lookup"><span data-stu-id="d7402-108">X</span></span>](x-cell-geometry-section.md) <br/> |<span data-ttu-id="d7402-109">Координата *X* второй контрольной точки сплайна.</span><span class="sxs-lookup"><span data-stu-id="d7402-109">The  *x*  -coordinate of a spline's second control point.</span></span>  <br/> |
|[<span data-ttu-id="d7402-110">Y</span><span class="sxs-lookup"><span data-stu-id="d7402-110">Y</span></span>](y-cell-geometry-section.md) <br/> |<span data-ttu-id="d7402-111">Координата *Y* второй контрольной точки сплайна.</span><span class="sxs-lookup"><span data-stu-id="d7402-111">The  *y*  -coordinate of a spline's second control point.</span></span>  <br/> |
|[<span data-ttu-id="d7402-112">A</span><span class="sxs-lookup"><span data-stu-id="d7402-112">A</span></span>](a-cell-geometry-section.md) <br/> |<span data-ttu-id="d7402-113">Вторая часть сплайна.</span><span class="sxs-lookup"><span data-stu-id="d7402-113">The second knot of the spline.</span></span>  <br/> |
|[<span data-ttu-id="d7402-114">B</span><span class="sxs-lookup"><span data-stu-id="d7402-114">B</span></span>](b-cell-geometry-section.md) <br/> |<span data-ttu-id="d7402-115">Первая ветвь сплайна.</span><span class="sxs-lookup"><span data-stu-id="d7402-115">The first knot of a spline.</span></span>  <br/> |
|[<span data-ttu-id="d7402-116">C</span><span class="sxs-lookup"><span data-stu-id="d7402-116">C</span></span>](c-cell-geometry-section.md) <br/> |<span data-ttu-id="d7402-117">Последняя часть сплайна.</span><span class="sxs-lookup"><span data-stu-id="d7402-117">The last knot of a spline.</span></span>  <br/> |
|[<span data-ttu-id="d7402-118">D</span><span class="sxs-lookup"><span data-stu-id="d7402-118">D</span></span>](d-cell-geometry-section.md) <br/> |<span data-ttu-id="d7402-119">Степень сплайна (от 1 до 25).</span><span class="sxs-lookup"><span data-stu-id="d7402-119">The degree of a spline (an integer from 1 to 25).</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d7402-120">Примечания</span><span class="sxs-lookup"><span data-stu-id="d7402-120">Remarks</span></span>

<span data-ttu-id="d7402-121">Visio отображает определение сплайна в разделе "Геометрия", который содержит строку SplineStart, за которой следует одна или несколько строк SplineKnot.</span><span class="sxs-lookup"><span data-stu-id="d7402-121">Visio displays the definition of a spline in a Geometry section that contains a SplineStart row followed by one or more SplineKnot rows.</span></span> <span data-ttu-id="d7402-122">Перед строкой SplineStart должен быть другой вид строки, например строка MoveTo, чтобы указать первую контрольную точку сплайна.</span><span class="sxs-lookup"><span data-stu-id="d7402-122">The SplineStart row must be preceded by another kind of row, such as a MoveTo row, to indicate the first control point of the spline.</span></span> <span data-ttu-id="d7402-123">Предыдущей строкой может быть строка LineTo, ArcTo, NURBSTo, PolylineTo или EllipticalArcTo, если spline следует за сегментом этого типа.</span><span class="sxs-lookup"><span data-stu-id="d7402-123">The preceding row can be a LineTo, ArcTo, NURBSTo, PolylineTo, or EllipticalArcTo row if the spline follows a segment of that type.</span></span>
  

