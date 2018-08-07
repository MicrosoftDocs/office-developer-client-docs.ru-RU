---
title: Ячейка D (раздел "Геометрия")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251753
localization_priority: Normal
ms.assetid: 5f1fdf59-db58-561c-e187-1af72a8b87f2
description: Представляет различные сведения в различных строк. В следующей таблице описаны ячейке D, основанную на строке, в котором он находится.
ms.openlocfilehash: ed67197e46ee159ba2175b0e86623fe1704992d2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19813517"
---
# <a name="d-cell-geometry-section"></a><span data-ttu-id="fe350-104">Ячейка D (раздел "Геометрия")</span><span class="sxs-lookup"><span data-stu-id="fe350-104">D Cell (Geometry Section)</span></span>

<span data-ttu-id="fe350-105">Представляет различные сведения в различных строк.</span><span class="sxs-lookup"><span data-stu-id="fe350-105">Represents different information in different rows.</span></span> <span data-ttu-id="fe350-106">В следующей таблице описаны ячейке D, основанную на строке, в котором он находится.</span><span class="sxs-lookup"><span data-stu-id="fe350-106">This table describes the D cell based on the row in which it's located.</span></span>
  
|<span data-ttu-id="fe350-107">**Row**</span><span class="sxs-lookup"><span data-stu-id="fe350-107">**Row**</span></span>|<span data-ttu-id="fe350-108">**Описание**</span><span class="sxs-lookup"><span data-stu-id="fe350-108">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="fe350-109">EllipticalArcTo</span><span class="sxs-lookup"><span data-stu-id="fe350-109">EllipticalArcTo</span></span>](ellipticalarcto-row-geometry-section.md) <br/> | <span data-ttu-id="fe350-110">Отношение arc главных осей его вспомогательные оси.</span><span class="sxs-lookup"><span data-stu-id="fe350-110">The ratio of an arc's major axis to its minor axis.</span></span> <span data-ttu-id="fe350-111">Несмотря на обычных значение из этих слов, должно быть больше оси «дополнительный номер», поэтому этот коэффициент не должен быть больше 1 имеет оси «основные».</span><span class="sxs-lookup"><span data-stu-id="fe350-111">Despite the usual meaning of these words, the "major" axis does not have to be greater than the "minor" axis, so this ratio does not have to be greater than 1.</span></span> <span data-ttu-id="fe350-112">Установка для этой ячейки значение меньше или равно 0 или выше, чем 1000 может привести к непредсказуемым последствиям.</span><span class="sxs-lookup"><span data-stu-id="fe350-112">Setting this cell to a value less than or equal to 0 or greater than 1000 can lead to unpredictable results.</span></span>  <br/> |
|[<span data-ttu-id="fe350-113">NURBSTo</span><span class="sxs-lookup"><span data-stu-id="fe350-113">NURBSTo</span></span>](nurbsto-row-geometry-section.md) <br/> | <span data-ttu-id="fe350-114">Первый вес неоднородной rational-сплайн (NURBS).</span><span class="sxs-lookup"><span data-stu-id="fe350-114">The first weight of the nonuniform rational B-spline (NURBS).</span></span>  <br/> |
|[<span data-ttu-id="fe350-115">SplineStart</span><span class="sxs-lookup"><span data-stu-id="fe350-115">SplineStart</span></span>](splinestart-row-geometry-section.md) <br/> | <span data-ttu-id="fe350-116">Степень сплайна (целое число от 1 до 25).</span><span class="sxs-lookup"><span data-stu-id="fe350-116">The degree of a spline (an integer from 1 to 25).</span></span>  <br/> |
|[<span data-ttu-id="fe350-117">Эллипс</span><span class="sxs-lookup"><span data-stu-id="fe350-117">Ellipse</span></span>](ellipse-row-geometry-section.md) <br/> | <span data-ttu-id="fe350-118">*Y* -координаты точки на эллипсы; в сочетании с *x* -координата, представленный в ячейку [C](c-cell-geometry-section.md) .</span><span class="sxs-lookup"><span data-stu-id="fe350-118">A  *y*  -coordinate of a point on an ellipse; paired with the  *x*  -coordinate represented by the [C](c-cell-geometry-section.md) cell.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="fe350-119">Замечания</span><span class="sxs-lookup"><span data-stu-id="fe350-119">Remarks</span></span>

<span data-ttu-id="fe350-120">Чтобы получить ссылку на ячейке D по имени из другой формулы, и программы, с помощью свойства **CellsU** , используйте:</span><span class="sxs-lookup"><span data-stu-id="fe350-120">To get a reference to the D cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="fe350-121">Имя ячейки.</span><span class="sxs-lookup"><span data-stu-id="fe350-121">Cell name:</span></span>  <br/> | <span data-ttu-id="fe350-122">Геометрия *i* . D *j* где *i* и *j* = < 1 > 2, 3...</span><span class="sxs-lookup"><span data-stu-id="fe350-122">Geometry  *i*  .D  *j*            where  *i*  and  *j*  = <1>, 2, 3...</span></span>  <br/> |
|| <span data-ttu-id="fe350-123">Геометрия *i* . D1 (строка эллипс) где *i* = < 1 > 2, 3...</span><span class="sxs-lookup"><span data-stu-id="fe350-123">Geometry  *i*  .D1 (Ellipse row)            where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="fe350-124">Для получения ссылки на ячейки D по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы:</span><span class="sxs-lookup"><span data-stu-id="fe350-124">To get a reference to the D cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="fe350-125">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="fe350-125">Section index:</span></span>  <br/> |<span data-ttu-id="fe350-126">**visSectionFirstComponent** +  *i* где *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="fe350-126">**visSectionFirstComponent** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="fe350-127">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="fe350-127">Row index:</span></span>  <br/> |<span data-ttu-id="fe350-128">**visRowVertex** +  *j* где *j* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="fe350-128">**visRowVertex** +  *j*            where  *j*  = 0, 1, 2...</span></span>  <br/> |
||<span data-ttu-id="fe350-129">**visRowVertex** (Эллипс строка)</span><span class="sxs-lookup"><span data-stu-id="fe350-129">**visRowVertex** (Ellipse row)</span></span>  <br/> |
| <span data-ttu-id="fe350-130">Индекс ячейки</span><span class="sxs-lookup"><span data-stu-id="fe350-130">Cell index</span></span>  <br/> |<span data-ttu-id="fe350-131">**visAspectRatio** (Строка EllipticalArcTo)</span><span class="sxs-lookup"><span data-stu-id="fe350-131">**visAspectRatio** (EllipticalArcTo row)</span></span>  <br/> |
||<span data-ttu-id="fe350-132">**visNURBSWeightPrev** (Строка NURBSTo)</span><span class="sxs-lookup"><span data-stu-id="fe350-132">**visNURBSWeightPrev** (NURBSTo row)</span></span>  <br/> |
||<span data-ttu-id="fe350-133">**visSplineDegree** (Строка SplineStart)</span><span class="sxs-lookup"><span data-stu-id="fe350-133">**visSplineDegree** (SplineStart row)</span></span>  <br/> |
||<span data-ttu-id="fe350-134">**visEllipseMinorY** (Эллипс строка)</span><span class="sxs-lookup"><span data-stu-id="fe350-134">**visEllipseMinorY** (Ellipse row)</span></span>  <br/> |
   

