---
title: B Cell (Geometry Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251751
localization_priority: Normal
ms.assetid: b0fb6a47-47d8-ab9c-854d-0b0bbfdfcc27
description: Представляет различные сведения в разных строках. В этой таблице описывается ячейка B на основе строки, в которой она расположена.
ms.openlocfilehash: 46c8aa418f495905630fed2833d84afc93945346
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/29/2019
ms.locfileid: "34537796"
---
# <a name="b-cell-geometry-section"></a><span data-ttu-id="259da-104">B Cell (Geometry Section)</span><span class="sxs-lookup"><span data-stu-id="259da-104">B Cell (Geometry Section)</span></span>

<span data-ttu-id="259da-105">Представляет различные сведения в разных строках.</span><span class="sxs-lookup"><span data-stu-id="259da-105">Represents different information in different rows.</span></span> <span data-ttu-id="259da-106">В этой таблице описывается ячейка B на основе строки, в которой она расположена.</span><span class="sxs-lookup"><span data-stu-id="259da-106">This table describes the B cell based on the row in which it's located.</span></span>
  
|<span data-ttu-id="259da-107">Строка</span><span class="sxs-lookup"><span data-stu-id="259da-107">Row</span></span>|<span data-ttu-id="259da-108">Описание</span><span class="sxs-lookup"><span data-stu-id="259da-108">Description</span></span>|
|:-----|:-----|
|[<span data-ttu-id="259da-109">EllipticalArcTo</span><span class="sxs-lookup"><span data-stu-id="259da-109">EllipticalArcTo</span></span>](ellipticalarcto-row-geometry-section.md) <br/> | <span data-ttu-id="259da-110">Координата *y* контрольной точки дуги.</span><span class="sxs-lookup"><span data-stu-id="259da-110">The  *y*  -coordinate of an arc's control point.</span></span>  <br/> |
|[<span data-ttu-id="259da-111">NURBSTo</span><span class="sxs-lookup"><span data-stu-id="259da-111">NURBSTo</span></span>](nurbsto-row-geometry-section.md) <br/> | <span data-ttu-id="259da-112">Последний вес неоднородного рационального B-сплайна (NURBS).</span><span class="sxs-lookup"><span data-stu-id="259da-112">The last weight of the nonuniform rational B-spline (NURBS).</span></span>  <br/> |
|[<span data-ttu-id="259da-113">SplineStart</span><span class="sxs-lookup"><span data-stu-id="259da-113">SplineStart</span></span>](splinestart-row-geometry-section.md) <br/> | <span data-ttu-id="259da-114">Первый кнот сплайна.</span><span class="sxs-lookup"><span data-stu-id="259da-114">The first knot of a spline.</span></span>  <br/> |
|[<span data-ttu-id="259da-115">InfiniteLine</span><span class="sxs-lookup"><span data-stu-id="259da-115">InfiniteLine</span></span>](infiniteline-row-geometry-section.md) <br/> | <span data-ttu-id="259da-116">Координата *y* точки на бесконечной линии; Связывание с координатой *x* [, представленной ячейкой](a-cell-geometry-section.md) .</span><span class="sxs-lookup"><span data-stu-id="259da-116">A  *y*  -coordinate of a point on an infinite line; paired with  *x*  -coordinate represented by the [A](a-cell-geometry-section.md) cell.</span></span>  <br/> |
|[<span data-ttu-id="259da-117">Ellipse</span><span class="sxs-lookup"><span data-stu-id="259da-117">Ellipse</span></span>](ellipse-row-geometry-section.md) <br/> | <span data-ttu-id="259da-118">Координата *y* точки эллипса; Связывание с координатой *x* [, представленной ячейкой](a-cell-geometry-section.md) .</span><span class="sxs-lookup"><span data-stu-id="259da-118">A  *y*  -coordinate of a point on an ellipse; paired with  *x*  -coordinate represented by the [A](a-cell-geometry-section.md) cell.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="259da-119">Примечания</span><span class="sxs-lookup"><span data-stu-id="259da-119">Remarks</span></span>

<span data-ttu-id="259da-120">Чтобы получить ссылку на ячейку B по имени из другой формулы или из программы с помощью свойства **CellsU** , используйте:</span><span class="sxs-lookup"><span data-stu-id="259da-120">To get a reference to the B cell by name from another formula, or from a program, using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="259da-121">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="259da-121">Cell name:</span></span>  <br/> | <span data-ttu-id="259da-122">Геометрия *i* . B *j* , где *i* и *j* = <1>, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="259da-122">Geometry  *i*  .B  *j*            where  *i*  and  *j*  = <1>, 2, 3...</span></span>  <br/> |
|| <span data-ttu-id="259da-123">Геометрия *i* . Строки B1 (строка infiniteline и Ellipse)</span><span class="sxs-lookup"><span data-stu-id="259da-123">Geometry  *i*  .B1 (InfiniteLine and Ellipse rows)</span></span>  <br/> |
   
<span data-ttu-id="259da-124">Чтобы получить ссылку на ячейку B по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="259da-124">To get a reference to the B cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="259da-125">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="259da-125">Section index:</span></span>  <br/> |<span data-ttu-id="259da-126">**visSectionFirstComponent** +  *i*, где *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="259da-126">**visSectionFirstComponent** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="259da-127">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="259da-127">Row index:</span></span>  <br/> |<span data-ttu-id="259da-128">**visRowVertex** +  *j*, где *j* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="259da-128">**visRowVertex** +  *j*            where  *j*  = 0, 1, 2...</span></span>  <br/> |
||<span data-ttu-id="259da-129">**visRowVertex** (строки InfiniteLine и Ellipse)</span><span class="sxs-lookup"><span data-stu-id="259da-129">**visRowVertex** (InfiniteLine and Ellipse rows)</span></span>  <br/> |
| <span data-ttu-id="259da-130">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="259da-130">Cell index:</span></span>  <br/> |<span data-ttu-id="259da-131">**висконтролкс** (строка строка ellipticalarcto)</span><span class="sxs-lookup"><span data-stu-id="259da-131">**visControlX** (EllipticalArcTo row)</span></span>  <br/> |
||<span data-ttu-id="259da-132">**висконтроли** (строка строка ellipticalarcto)</span><span class="sxs-lookup"><span data-stu-id="259da-132">**visControlY** (EllipticalArcTo row)</span></span>  <br/> |
||<span data-ttu-id="259da-133">**виснурбсвеигхт** (строка NURBSTo)</span><span class="sxs-lookup"><span data-stu-id="259da-133">**visNURBSWeight** (NURBSTo row)</span></span>  <br/> |
||<span data-ttu-id="259da-134">**visSplineKnot2** (строка строка splinestart)</span><span class="sxs-lookup"><span data-stu-id="259da-134">**visSplineKnot2** (SplineStart row)</span></span>  <br/> |
||<span data-ttu-id="259da-135">**visInfiniteLineY2** (строка строка infiniteline)</span><span class="sxs-lookup"><span data-stu-id="259da-135">**visInfiniteLineY2** (InfiniteLine row)</span></span>  <br/> |
||<span data-ttu-id="259da-136">**виселлипсемажори** (строка "эллипс")</span><span class="sxs-lookup"><span data-stu-id="259da-136">**visEllipseMajorY** (Ellipse row)</span></span>  <br/> |
   

