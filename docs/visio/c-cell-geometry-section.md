---
title: Ячейка C (раздел "Геометрия")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm140
localization_priority: Normal
ms.assetid: d51a1dd8-678a-a34d-658d-bd7a027dd379
description: Представляет различные сведения в различных строк. В следующей таблице описаны C ячейки, основанную на строке, в котором он находится.
ms.openlocfilehash: 1b9a813be825f2deeb5c90d596ffd9f3705bcef6
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19813323"
---
# <a name="c-cell-geometry-section"></a><span data-ttu-id="32af2-104">Ячейка C (раздел "Геометрия")</span><span class="sxs-lookup"><span data-stu-id="32af2-104">C Cell (Geometry Section)</span></span>

<span data-ttu-id="32af2-105">Представляет различные сведения в различных строк.</span><span class="sxs-lookup"><span data-stu-id="32af2-105">Represents different information in different rows.</span></span> <span data-ttu-id="32af2-106">В следующей таблице описаны C ячейки, основанную на строке, в котором он находится.</span><span class="sxs-lookup"><span data-stu-id="32af2-106">This table describes the C cell based on the row in which it's located.</span></span>
  
|<span data-ttu-id="32af2-107">**Row**</span><span class="sxs-lookup"><span data-stu-id="32af2-107">**Row**</span></span>|<span data-ttu-id="32af2-108">**Описание**</span><span class="sxs-lookup"><span data-stu-id="32af2-108">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="32af2-109">EllipticalArcTo</span><span class="sxs-lookup"><span data-stu-id="32af2-109">EllipticalArcTo</span></span>](ellipticalarcto-row-geometry-section.md) <br/> | <span data-ttu-id="32af2-110">Угол дуги главных осей относительно *x* -ось родительского элемента.</span><span class="sxs-lookup"><span data-stu-id="32af2-110">The angle of an arc's major axis relative to the  *x*  -axis of its parent.</span></span>  <br/> |
|[<span data-ttu-id="32af2-111">NURBSTo</span><span class="sxs-lookup"><span data-stu-id="32af2-111">NURBSTo</span></span>](nurbsto-row-geometry-section.md) <br/> | <span data-ttu-id="32af2-112">Первый узел неоднородной rational-сплайн (NURBS).</span><span class="sxs-lookup"><span data-stu-id="32af2-112">The first knot of the nonuniform rational B-spline (NURBS).</span></span>  <br/> |
|[<span data-ttu-id="32af2-113">SplineStart</span><span class="sxs-lookup"><span data-stu-id="32af2-113">SplineStart</span></span>](splinestart-row-geometry-section.md) <br/> | <span data-ttu-id="32af2-114">Последний число узлов сплайна.</span><span class="sxs-lookup"><span data-stu-id="32af2-114">The last knot of a spline.</span></span>  <br/> |
|[<span data-ttu-id="32af2-115">Эллипс</span><span class="sxs-lookup"><span data-stu-id="32af2-115">Ellipse</span></span>](ellipse-row-geometry-section.md) <br/> | <span data-ttu-id="32af2-116">*X* -координаты точки на эллипсы; в сочетании с *y* -координата, представленного в ячейке [D](d-cell-geometry-section.md) .</span><span class="sxs-lookup"><span data-stu-id="32af2-116">An  *x*  -coordinate of a point on an ellipse; paired with the  *y*  -coordinate represented by the [D](d-cell-geometry-section.md) cell.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="32af2-117">Замечания</span><span class="sxs-lookup"><span data-stu-id="32af2-117">Remarks</span></span>

<span data-ttu-id="32af2-118">Чтобы получить ссылку на ячейку C по имени из другой формулы, и программы, с помощью свойства **CellsU** , используйте следующую команду:</span><span class="sxs-lookup"><span data-stu-id="32af2-118">To get a reference to the C cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="32af2-119">Имя ячейки.</span><span class="sxs-lookup"><span data-stu-id="32af2-119">Cell name:</span></span>  <br/> | <span data-ttu-id="32af2-120">Геометрия *i* . C *j* где *i* и *j* = < 1 > 2, 3...</span><span class="sxs-lookup"><span data-stu-id="32af2-120">Geometry  *i*  .C  *j*            where  *i*  and  *j*  = <1>, 2, 3...</span></span>  <br/> |
|| <span data-ttu-id="32af2-121">Геометрия *i* . C1 (эллипс строка)</span><span class="sxs-lookup"><span data-stu-id="32af2-121">Geometry  *i*  .C1 (Ellipse row)</span></span>  <br/> |
   
<span data-ttu-id="32af2-122">Для получения ссылки на ячейки C по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы:</span><span class="sxs-lookup"><span data-stu-id="32af2-122">To get a reference to the C cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="32af2-123">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="32af2-123">Section index:</span></span>  <br/> |<span data-ttu-id="32af2-124">**visSectionFirstComponent** +  *i* где *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="32af2-124">**visSectionFirstComponent** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="32af2-125">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="32af2-125">Row index:</span></span>  <br/> |<span data-ttu-id="32af2-126">**visRowVertex** +  *j* где *j* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="32af2-126">**visRowVertex** +  *j*            where  *j*  = 0, 1, 2...</span></span>  <br/> |
||<span data-ttu-id="32af2-127">**visRowVertex** (Эллипс строка)</span><span class="sxs-lookup"><span data-stu-id="32af2-127">**visRowVertex** (Ellipse row)</span></span>  <br/> |
| <span data-ttu-id="32af2-128">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="32af2-128">Cell index:</span></span>  <br/> |<span data-ttu-id="32af2-129">**visEccentricityAngle** (Строка EllipticalArcTo)</span><span class="sxs-lookup"><span data-stu-id="32af2-129">**visEccentricityAngle** (EllipticalArcTo row)</span></span>  <br/> |
||<span data-ttu-id="32af2-130">**visNURBSKnotPrev** (Строка NURBSTo)</span><span class="sxs-lookup"><span data-stu-id="32af2-130">**visNURBSKnotPrev** (NURBSTo row)</span></span>  <br/> |
||<span data-ttu-id="32af2-131">**visSplineKnot3** (Строка SplineStart)</span><span class="sxs-lookup"><span data-stu-id="32af2-131">**visSplineKnot3** (SplineStart row)</span></span>  <br/> |
||<span data-ttu-id="32af2-132">**visEllipseMinorX** (Эллипс строка)</span><span class="sxs-lookup"><span data-stu-id="32af2-132">**visEllipseMinorX** (Ellipse row)</span></span>  <br/> |
   

