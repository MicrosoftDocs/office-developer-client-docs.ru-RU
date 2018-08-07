---
title: Ячейка B (раздел "Геометрия")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251751
localization_priority: Normal
ms.assetid: b0fb6a47-47d8-ab9c-854d-0b0bbfdfcc27
description: Представляет различные сведения в различных строк. В следующей таблице описаны ячейки B, основанную на строке, в котором он находится.
ms.openlocfilehash: 7d6f51d037be4852c6a101ad6e576a3a13488cb7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19813175"
---
# <a name="b-cell-geometry-section"></a><span data-ttu-id="56e8f-104">Ячейка B (раздел "Геометрия")</span><span class="sxs-lookup"><span data-stu-id="56e8f-104">B Cell (Geometry Section)</span></span>

<span data-ttu-id="56e8f-105">Представляет различные сведения в различных строк.</span><span class="sxs-lookup"><span data-stu-id="56e8f-105">Represents different information in different rows.</span></span> <span data-ttu-id="56e8f-106">В следующей таблице описаны ячейки B, основанную на строке, в котором он находится.</span><span class="sxs-lookup"><span data-stu-id="56e8f-106">This table describes the B cell based on the row in which it's located.</span></span>
  
|<span data-ttu-id="56e8f-107">**Row**</span><span class="sxs-lookup"><span data-stu-id="56e8f-107">**Row**</span></span>|<span data-ttu-id="56e8f-108">**Описание**</span><span class="sxs-lookup"><span data-stu-id="56e8f-108">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="56e8f-109">EllipticalArcTo</span><span class="sxs-lookup"><span data-stu-id="56e8f-109">EllipticalArcTo</span></span>](ellipticalarcto-row-geometry-section.md) <br/> | <span data-ttu-id="56e8f-110">*Y* -координата точки управления arc.</span><span class="sxs-lookup"><span data-stu-id="56e8f-110">The  *y*  -coordinate of an arc's control point.</span></span>  <br/> |
|[<span data-ttu-id="56e8f-111">NURBSTo</span><span class="sxs-lookup"><span data-stu-id="56e8f-111">NURBSTo</span></span>](nurbsto-row-geometry-section.md) <br/> | <span data-ttu-id="56e8f-112">Последний вес неоднородной rational-сплайн (NURBS).</span><span class="sxs-lookup"><span data-stu-id="56e8f-112">The last weight of the nonuniform rational B-spline (NURBS).</span></span>  <br/> |
|[<span data-ttu-id="56e8f-113">SplineStart</span><span class="sxs-lookup"><span data-stu-id="56e8f-113">SplineStart</span></span>](splinestart-row-geometry-section.md) <br/> | <span data-ttu-id="56e8f-114">Первый узел сплайна.</span><span class="sxs-lookup"><span data-stu-id="56e8f-114">The first knot of a spline.</span></span>  <br/> |
|[<span data-ttu-id="56e8f-115">InfiniteLine</span><span class="sxs-lookup"><span data-stu-id="56e8f-115">InfiniteLine</span></span>](infiniteline-row-geometry-section.md) <br/> | <span data-ttu-id="56e8f-116">*Y* -координаты точки на неограниченное строке. в сочетании с *x* -координата, представленное [ячейке](a-cell-geometry-section.md) .</span><span class="sxs-lookup"><span data-stu-id="56e8f-116">A  *y*  -coordinate of a point on an infinite line; paired with  *x*  -coordinate represented by the [A](a-cell-geometry-section.md) cell.</span></span>  <br/> |
|[<span data-ttu-id="56e8f-117">Эллипс</span><span class="sxs-lookup"><span data-stu-id="56e8f-117">Ellipse</span></span>](ellipse-row-geometry-section.md) <br/> | <span data-ttu-id="56e8f-118">*Y* -координаты точки на эллипсы; в сочетании с *x* -координата, представленное [ячейке](a-cell-geometry-section.md) .</span><span class="sxs-lookup"><span data-stu-id="56e8f-118">A  *y*  -coordinate of a point on an ellipse; paired with  *x*  -coordinate represented by the [A](a-cell-geometry-section.md) cell.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="56e8f-119">Замечания</span><span class="sxs-lookup"><span data-stu-id="56e8f-119">Remarks</span></span>

<span data-ttu-id="56e8f-120">Для получения ссылки на ячейки B по имени, из другой формулы или из программы, с помощью свойства **CellsU** , используйте следующую команду:</span><span class="sxs-lookup"><span data-stu-id="56e8f-120">To get a reference to the B cell by name from another formula, or from a program, using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="56e8f-121">Имя ячейки.</span><span class="sxs-lookup"><span data-stu-id="56e8f-121">Cell name:</span></span>  <br/> | <span data-ttu-id="56e8f-122">Геометрия *i* . B *j* где *i* и *j* = < 1 > 2, 3...</span><span class="sxs-lookup"><span data-stu-id="56e8f-122">Geometry  *i*  .B  *j*            where  *i*  and  *j*  = <1>, 2, 3...</span></span>  <br/> |
|| <span data-ttu-id="56e8f-123">Геометрия *i* . B1 (InfiniteLine и эллипс строк)</span><span class="sxs-lookup"><span data-stu-id="56e8f-123">Geometry  *i*  .B1 (InfiniteLine and Ellipse rows)</span></span>  <br/> |
   
<span data-ttu-id="56e8f-124">Для получения ссылки на ячейки B по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы:</span><span class="sxs-lookup"><span data-stu-id="56e8f-124">To get a reference to the B cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="56e8f-125">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="56e8f-125">Section index:</span></span>  <br/> |<span data-ttu-id="56e8f-126">**visSectionFirstComponent** +  *i* где *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="56e8f-126">**visSectionFirstComponent** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="56e8f-127">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="56e8f-127">Row index:</span></span>  <br/> |<span data-ttu-id="56e8f-128">**visRowVertex** +  *j* где *j* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="56e8f-128">**visRowVertex** +  *j*            where  *j*  = 0, 1, 2...</span></span>  <br/> |
||<span data-ttu-id="56e8f-129">**visRowVertex** (InfiniteLine и эллипс строк)</span><span class="sxs-lookup"><span data-stu-id="56e8f-129">**visRowVertex** (InfiniteLine and Ellipse rows)</span></span>  <br/> |
| <span data-ttu-id="56e8f-130">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="56e8f-130">Cell index:</span></span>  <br/> |<span data-ttu-id="56e8f-131">**visControlX** (Строка EllipticalArcTo)</span><span class="sxs-lookup"><span data-stu-id="56e8f-131">**visControlX** (EllipticalArcTo row)</span></span>  <br/> |
||<span data-ttu-id="56e8f-132">**visControlY** (Строка EllipticalArcTo)</span><span class="sxs-lookup"><span data-stu-id="56e8f-132">**visControlY** (EllipticalArcTo row)</span></span>  <br/> |
||<span data-ttu-id="56e8f-133">**visNURBSWeight** (Строка NURBSTo)</span><span class="sxs-lookup"><span data-stu-id="56e8f-133">**visNURBSWeight** (NURBSTo row)</span></span>  <br/> |
||<span data-ttu-id="56e8f-134">**visSplineKnot2** (Строка SplineStart)</span><span class="sxs-lookup"><span data-stu-id="56e8f-134">**visSplineKnot2** (SplineStart row)</span></span>  <br/> |
||<span data-ttu-id="56e8f-135">**visInfiniteLineY2** (Строка InfiniteLine)</span><span class="sxs-lookup"><span data-stu-id="56e8f-135">**visInfiniteLineY2** (InfiniteLine row)</span></span>  <br/> |
||<span data-ttu-id="56e8f-136">**visEllipseMajorY** (Эллипс строка)</span><span class="sxs-lookup"><span data-stu-id="56e8f-136">**visEllipseMajorY** (Ellipse row)</span></span>  <br/> |
   

