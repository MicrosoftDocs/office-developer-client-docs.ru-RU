---
title: D Cell (Geometry Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251753
localization_priority: Normal
ms.assetid: 5f1fdf59-db58-561c-e187-1af72a8b87f2
description: Представляет различные сведения в разных строках. В этой таблице описывается ячейка D, основанная на строке, в которой она расположена.
ms.openlocfilehash: a76093f028986907b58175bc6b8c81a7056cfe07
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/29/2019
ms.locfileid: "34542501"
---
# <a name="d-cell-geometry-section"></a><span data-ttu-id="aedba-104">D Cell (Geometry Section)</span><span class="sxs-lookup"><span data-stu-id="aedba-104">D Cell (Geometry Section)</span></span>

<span data-ttu-id="aedba-105">Представляет различные сведения в разных строках.</span><span class="sxs-lookup"><span data-stu-id="aedba-105">Represents different information in different rows.</span></span> <span data-ttu-id="aedba-106">В этой таблице описывается ячейка D, основанная на строке, в которой она расположена.</span><span class="sxs-lookup"><span data-stu-id="aedba-106">This table describes the D cell based on the row in which it's located.</span></span>
  
|<span data-ttu-id="aedba-107">Строка</span><span class="sxs-lookup"><span data-stu-id="aedba-107">Row</span></span>|<span data-ttu-id="aedba-108">Описание</span><span class="sxs-lookup"><span data-stu-id="aedba-108">Description</span></span>|
|:-----|:-----|
|[<span data-ttu-id="aedba-109">EllipticalArcTo</span><span class="sxs-lookup"><span data-stu-id="aedba-109">EllipticalArcTo</span></span>](ellipticalarcto-row-geometry-section.md) <br/> | <span data-ttu-id="aedba-110">Отношение основной оси дуги к ее вспомогательной оси.</span><span class="sxs-lookup"><span data-stu-id="aedba-110">The ratio of an arc's major axis to its minor axis.</span></span> <span data-ttu-id="aedba-111">Несмотря на обычное значение этих слов, ось "Major" не должна превышать "младшую" ось, поэтому значение этого коэффициента не должно превышать 1.</span><span class="sxs-lookup"><span data-stu-id="aedba-111">Despite the usual meaning of these words, the "major" axis does not have to be greater than the "minor" axis, so this ratio does not have to be greater than 1.</span></span> <span data-ttu-id="aedba-112">Присвоение этой ячейке значения меньше или равно 0 или больше 1000 может привести к непредсказуемым результатам.</span><span class="sxs-lookup"><span data-stu-id="aedba-112">Setting this cell to a value less than or equal to 0 or greater than 1000 can lead to unpredictable results.</span></span>  <br/> |
|[<span data-ttu-id="aedba-113">NURBSTo</span><span class="sxs-lookup"><span data-stu-id="aedba-113">NURBSTo</span></span>](nurbsto-row-geometry-section.md) <br/> | <span data-ttu-id="aedba-114">Первый вес рационального понеоднородногоного B-сплайна (NURBS).</span><span class="sxs-lookup"><span data-stu-id="aedba-114">The first weight of the nonuniform rational B-spline (NURBS).</span></span>  <br/> |
|[<span data-ttu-id="aedba-115">SplineStart</span><span class="sxs-lookup"><span data-stu-id="aedba-115">SplineStart</span></span>](splinestart-row-geometry-section.md) <br/> | <span data-ttu-id="aedba-116">Степень сплайна (целое число от 1 до 25).</span><span class="sxs-lookup"><span data-stu-id="aedba-116">The degree of a spline (an integer from 1 to 25).</span></span>  <br/> |
|[<span data-ttu-id="aedba-117">Ellipse</span><span class="sxs-lookup"><span data-stu-id="aedba-117">Ellipse</span></span>](ellipse-row-geometry-section.md) <br/> | <span data-ttu-id="aedba-118">Координата *y* точки эллипса; Связывание с координатой *x* , представленной в ячейке [C](c-cell-geometry-section.md) .</span><span class="sxs-lookup"><span data-stu-id="aedba-118">A  *y*  -coordinate of a point on an ellipse; paired with the  *x*  -coordinate represented by the [C](c-cell-geometry-section.md) cell.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="aedba-119">Примечания</span><span class="sxs-lookup"><span data-stu-id="aedba-119">Remarks</span></span>

<span data-ttu-id="aedba-120">Чтобы получить ссылку на ячейку D по имени из другой формулы или из программы с помощью свойства **CellsU** , используйте:</span><span class="sxs-lookup"><span data-stu-id="aedba-120">To get a reference to the D cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="aedba-121">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="aedba-121">Cell name:</span></span>  <br/> | <span data-ttu-id="aedba-122">Геометрия *i* . D *j* , где *i* и *j* = <1>, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="aedba-122">Geometry  *i*  .D  *j*            where  *i*  and  *j*  = <1>, 2, 3...</span></span>  <br/> |
|| <span data-ttu-id="aedba-123">Геометрия *i* . D1 (строка эллипса), где *i* = <1>, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="aedba-123">Geometry  *i*  .D1 (Ellipse row)            where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="aedba-124">Чтобы получить ссылку на ячейку D по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="aedba-124">To get a reference to the D cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="aedba-125">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="aedba-125">Section index:</span></span>  <br/> |<span data-ttu-id="aedba-126">**visSectionFirstComponent** +  *i*, где *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="aedba-126">**visSectionFirstComponent** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="aedba-127">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="aedba-127">Row index:</span></span>  <br/> |<span data-ttu-id="aedba-128">**visRowVertex** +  *j*, где *j* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="aedba-128">**visRowVertex** +  *j*            where  *j*  = 0, 1, 2...</span></span>  <br/> |
||<span data-ttu-id="aedba-129">**висроввертекс** (Строка "эллипс")</span><span class="sxs-lookup"><span data-stu-id="aedba-129">**visRowVertex** (Ellipse row)</span></span>  <br/> |
| <span data-ttu-id="aedba-130">Индекс ячейки</span><span class="sxs-lookup"><span data-stu-id="aedba-130">Cell index</span></span>  <br/> |<span data-ttu-id="aedba-131">**висаспектратио** (Строка строка ellipticalarcto)</span><span class="sxs-lookup"><span data-stu-id="aedba-131">**visAspectRatio** (EllipticalArcTo row)</span></span>  <br/> |
||<span data-ttu-id="aedba-132">**виснурбсвеигхтпрев** (Строка NURBSTo)</span><span class="sxs-lookup"><span data-stu-id="aedba-132">**visNURBSWeightPrev** (NURBSTo row)</span></span>  <br/> |
||<span data-ttu-id="aedba-133">**виссплинедегри** (Строка строка splinestart)</span><span class="sxs-lookup"><span data-stu-id="aedba-133">**visSplineDegree** (SplineStart row)</span></span>  <br/> |
||<span data-ttu-id="aedba-134">**виселлипсеминори** (Строка "эллипс")</span><span class="sxs-lookup"><span data-stu-id="aedba-134">**visEllipseMinorY** (Ellipse row)</span></span>  <br/> |
   

