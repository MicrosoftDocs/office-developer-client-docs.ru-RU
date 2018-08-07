---
title: Строка SplineStart (раздел "Геометрия")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm3055
localization_priority: Normal
ms.assetid: 8e327e00-0844-efa4-900b-6954d3b009bb
description: Содержит x - и y-координаты сплайн второй контрольной точки, его второй число узлов, его первого число узлов, последний число узлов и степень сплайн.
ms.openlocfilehash: 0944da12e6090fde41dc5927b5705e103d29f76d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19814936"
---
# <a name="splinestart-row-geometry-section"></a><span data-ttu-id="f4a3a-103">Строка SplineStart (раздел "Геометрия")</span><span class="sxs-lookup"><span data-stu-id="f4a3a-103">SplineStart Row (Geometry Section)</span></span>

<span data-ttu-id="f4a3a-104">Содержит *x* - и *y* -координаты сплайн второй контрольной точки, его второй число узлов, его первого число узлов, последний число узлов и степень сплайн.</span><span class="sxs-lookup"><span data-stu-id="f4a3a-104">Contains  *x*  - and  *y*  -coordinates for a spline's second control point, its second knot, its first knot, the last knot, and the degree of the spline.</span></span> 
  
<span data-ttu-id="f4a3a-105">Строка SplineStart содержит следующие ячейки.</span><span class="sxs-lookup"><span data-stu-id="f4a3a-105">A SplineStart row contains the following cells.</span></span>
  
|<span data-ttu-id="f4a3a-106">**Cell**</span><span class="sxs-lookup"><span data-stu-id="f4a3a-106">**Cell**</span></span>|<span data-ttu-id="f4a3a-107">**Описание**</span><span class="sxs-lookup"><span data-stu-id="f4a3a-107">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="f4a3a-108">X</span><span class="sxs-lookup"><span data-stu-id="f4a3a-108">X</span></span>](x-cell-geometry-section.md) <br/> |<span data-ttu-id="f4a3a-109">*X* -Координата второй контрольной точки сплайна.</span><span class="sxs-lookup"><span data-stu-id="f4a3a-109">The  *x*  -coordinate of a spline's second control point.</span></span>  <br/> |
|[<span data-ttu-id="f4a3a-110">Да</span><span class="sxs-lookup"><span data-stu-id="f4a3a-110">Y</span></span>](y-cell-geometry-section.md) <br/> |<span data-ttu-id="f4a3a-111">*Y* -Координата второй контрольной точки сплайна.</span><span class="sxs-lookup"><span data-stu-id="f4a3a-111">The  *y*  -coordinate of a spline's second control point.</span></span>  <br/> |
|[<span data-ttu-id="f4a3a-112">A</span><span class="sxs-lookup"><span data-stu-id="f4a3a-112">A</span></span>](a-cell-geometry-section.md) <br/> |<span data-ttu-id="f4a3a-113">Второй узел сплайн.</span><span class="sxs-lookup"><span data-stu-id="f4a3a-113">The second knot of the spline.</span></span>  <br/> |
|[<span data-ttu-id="f4a3a-114">B</span><span class="sxs-lookup"><span data-stu-id="f4a3a-114">B</span></span>](b-cell-geometry-section.md) <br/> |<span data-ttu-id="f4a3a-115">Первый узел сплайна.</span><span class="sxs-lookup"><span data-stu-id="f4a3a-115">The first knot of a spline.</span></span>  <br/> |
|[<span data-ttu-id="f4a3a-116">C</span><span class="sxs-lookup"><span data-stu-id="f4a3a-116">C</span></span>](c-cell-geometry-section.md) <br/> |<span data-ttu-id="f4a3a-117">Последний число узлов сплайна.</span><span class="sxs-lookup"><span data-stu-id="f4a3a-117">The last knot of a spline.</span></span>  <br/> |
|[<span data-ttu-id="f4a3a-118">D</span><span class="sxs-lookup"><span data-stu-id="f4a3a-118">D</span></span>](d-cell-geometry-section.md) <br/> |<span data-ttu-id="f4a3a-119">Степень сплайна (целое число от 1 до 25).</span><span class="sxs-lookup"><span data-stu-id="f4a3a-119">The degree of a spline (an integer from 1 to 25).</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f4a3a-120">Замечания</span><span class="sxs-lookup"><span data-stu-id="f4a3a-120">Remarks</span></span>

<span data-ttu-id="f4a3a-121">Visio отображается определение сплайна в раздел геометрии, в котором содержится строка SplineStart, а затем одна или несколько строк SplineKnot.</span><span class="sxs-lookup"><span data-stu-id="f4a3a-121">Visio displays the definition of a spline in a Geometry section that contains a SplineStart row followed by one or more SplineKnot rows.</span></span> <span data-ttu-id="f4a3a-122">Строка SplineStart должен предшествовать строки, например MoveTo строку, чтобы указать, первый элемент управления точкой для другого типа.</span><span class="sxs-lookup"><span data-stu-id="f4a3a-122">The SplineStart row must be preceded by another kind of row, such as a MoveTo row, to indicate the first control point of the spline.</span></span> <span data-ttu-id="f4a3a-123">Предыдущей строке может быть строкой LineTo, ArcTo, NURBSTo, PolylineTo или EllipticalArcTo сплайн за сегмент этого типа.</span><span class="sxs-lookup"><span data-stu-id="f4a3a-123">The preceding row can be a LineTo, ArcTo, NURBSTo, PolylineTo, or EllipticalArcTo row if the spline follows a segment of that type.</span></span>
  

