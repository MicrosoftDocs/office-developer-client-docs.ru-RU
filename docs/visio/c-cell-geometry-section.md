---
title: C Cell (Geometry Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm140
localization_priority: Normal
ms.assetid: d51a1dd8-678a-a34d-658d-bd7a027dd379
description: Представляет различные сведения в разных строках. В этой таблице описывается ячейка C на основе строки, в которой она расположена.
ms.openlocfilehash: 0284fea02c7eb890b56b6c865a69eb36662d8ae6
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/29/2019
ms.locfileid: "34541892"
---
# <a name="c-cell-geometry-section"></a><span data-ttu-id="59fbb-104">C Cell (Geometry Section)</span><span class="sxs-lookup"><span data-stu-id="59fbb-104">C Cell (Geometry Section)</span></span>

<span data-ttu-id="59fbb-105">Представляет различные сведения в разных строках.</span><span class="sxs-lookup"><span data-stu-id="59fbb-105">Represents different information in different rows.</span></span> <span data-ttu-id="59fbb-106">В этой таблице описывается ячейка C на основе строки, в которой она расположена.</span><span class="sxs-lookup"><span data-stu-id="59fbb-106">This table describes the C cell based on the row in which it's located.</span></span>
  
|<span data-ttu-id="59fbb-107">Строка</span><span class="sxs-lookup"><span data-stu-id="59fbb-107">Row</span></span>|<span data-ttu-id="59fbb-108">Описание</span><span class="sxs-lookup"><span data-stu-id="59fbb-108">Description</span></span>|
|:-----|:-----|
|[<span data-ttu-id="59fbb-109">EllipticalArcTo</span><span class="sxs-lookup"><span data-stu-id="59fbb-109">EllipticalArcTo</span></span>](ellipticalarcto-row-geometry-section.md) <br/> | <span data-ttu-id="59fbb-110">Угол основной оси дуги относительно оси *x* его родительского элемента.</span><span class="sxs-lookup"><span data-stu-id="59fbb-110">The angle of an arc's major axis relative to the  *x*  -axis of its parent.</span></span>  <br/> |
|[<span data-ttu-id="59fbb-111">NURBSTo</span><span class="sxs-lookup"><span data-stu-id="59fbb-111">NURBSTo</span></span>](nurbsto-row-geometry-section.md) <br/> | <span data-ttu-id="59fbb-112">Первый кнот в неоднородного рациональном-сплайне (NURBS).</span><span class="sxs-lookup"><span data-stu-id="59fbb-112">The first knot of the nonuniform rational B-spline (NURBS).</span></span>  <br/> |
|[<span data-ttu-id="59fbb-113">SplineStart</span><span class="sxs-lookup"><span data-stu-id="59fbb-113">SplineStart</span></span>](splinestart-row-geometry-section.md) <br/> | <span data-ttu-id="59fbb-114">Последний кнот сплайна.</span><span class="sxs-lookup"><span data-stu-id="59fbb-114">The last knot of a spline.</span></span>  <br/> |
|[<span data-ttu-id="59fbb-115">Ellipse</span><span class="sxs-lookup"><span data-stu-id="59fbb-115">Ellipse</span></span>](ellipse-row-geometry-section.md) <br/> | <span data-ttu-id="59fbb-116">Координата *x* точки эллипса; связать с координатой *y* , представленной ячейкой [D](d-cell-geometry-section.md) .</span><span class="sxs-lookup"><span data-stu-id="59fbb-116">An  *x*  -coordinate of a point on an ellipse; paired with the  *y*  -coordinate represented by the [D](d-cell-geometry-section.md) cell.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="59fbb-117">Примечания</span><span class="sxs-lookup"><span data-stu-id="59fbb-117">Remarks</span></span>

<span data-ttu-id="59fbb-118">Чтобы получить ссылку на ячейку C по имени из другой формулы или из программы с помощью свойства **CellsU** , используйте:</span><span class="sxs-lookup"><span data-stu-id="59fbb-118">To get a reference to the C cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="59fbb-119">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="59fbb-119">Cell name:</span></span>  <br/> | <span data-ttu-id="59fbb-120">Геометрия *i* . C *j* , где *i* и *j* = <1>, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="59fbb-120">Geometry  *i*  .C  *j*            where  *i*  and  *j*  = <1>, 2, 3...</span></span>  <br/> |
|| <span data-ttu-id="59fbb-121">Геометрия *i* . C1 (строка "эллипс")</span><span class="sxs-lookup"><span data-stu-id="59fbb-121">Geometry  *i*  .C1 (Ellipse row)</span></span>  <br/> |
   
<span data-ttu-id="59fbb-122">Чтобы получить ссылку на ячейку C по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="59fbb-122">To get a reference to the C cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="59fbb-123">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="59fbb-123">Section index:</span></span>  <br/> |<span data-ttu-id="59fbb-124">**visSectionFirstComponent** +  *i*, где *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="59fbb-124">**visSectionFirstComponent** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="59fbb-125">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="59fbb-125">Row index:</span></span>  <br/> |<span data-ttu-id="59fbb-126">**visRowVertex** +  *j*, где *j* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="59fbb-126">**visRowVertex** +  *j*            where  *j*  = 0, 1, 2...</span></span>  <br/> |
||<span data-ttu-id="59fbb-127">**висроввертекс** (Строка "эллипс")</span><span class="sxs-lookup"><span data-stu-id="59fbb-127">**visRowVertex** (Ellipse row)</span></span>  <br/> |
| <span data-ttu-id="59fbb-128">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="59fbb-128">Cell index:</span></span>  <br/> |<span data-ttu-id="59fbb-129">**висекцентриЦитянгле** (Строка строка ellipticalarcto)</span><span class="sxs-lookup"><span data-stu-id="59fbb-129">**visEccentricityAngle** (EllipticalArcTo row)</span></span>  <br/> |
||<span data-ttu-id="59fbb-130">**виснурбскнотпрев** (Строка NURBSTo)</span><span class="sxs-lookup"><span data-stu-id="59fbb-130">**visNURBSKnotPrev** (NURBSTo row)</span></span>  <br/> |
||<span data-ttu-id="59fbb-131">**visSplineKnot3** (Строка строка splinestart)</span><span class="sxs-lookup"><span data-stu-id="59fbb-131">**visSplineKnot3** (SplineStart row)</span></span>  <br/> |
||<span data-ttu-id="59fbb-132">**виселлипсеминоркс** (Строка "эллипс")</span><span class="sxs-lookup"><span data-stu-id="59fbb-132">**visEllipseMinorX** (Ellipse row)</span></span>  <br/> |
   

