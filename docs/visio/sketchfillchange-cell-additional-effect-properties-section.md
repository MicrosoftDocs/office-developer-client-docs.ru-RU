---
title: SketchFillChange Cell (Additional Effect Properties Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 939f8f90-dee5-4175-b32a-e2964eb40681
description: Определяет объем случайного выбора заливки фигуры из геометрии фигуры при использовании эффекта наброска в процентах от длины раздела. Если значение ячейки SketchFillChange составляет 0 %, вязая геометрия заливки фигуры соответствует геометрии фигуры. Если значение составляет 100 %, ограниченная геометрия заливки фигуры не следует за геометрией фигуры.
ms.openlocfilehash: 8726e9dd6ca6257fb8dbbbef3dce1d4ec344e28b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408077"
---
# <a name="sketchfillchange-cell-additional-effect-properties-section"></a><span data-ttu-id="0501d-105">SketchFillChange Cell (Additional Effect Properties Section)</span><span class="sxs-lookup"><span data-stu-id="0501d-105">SketchFillChange Cell (Additional Effect Properties Section)</span></span>

<span data-ttu-id="0501d-106">Определяет объем случайного выбора заливки фигуры из геометрии фигуры при использовании эффекта наброска в процентах от длины раздела.</span><span class="sxs-lookup"><span data-stu-id="0501d-106">Determines the amount of randomization of the shape's fill from the shape's geometry when using a sketch effect, as a percentage of the length of a section.</span></span> <span data-ttu-id="0501d-107">Если значение ячейки **SketchFillChange** — 0 %, то ограниченная геометрия заливки фигуры соответствует геометрии фигуры.</span><span class="sxs-lookup"><span data-stu-id="0501d-107">If the value of the **SketchFillChange** cell is set to 0%, the bounding geometry of a shape's fill matches the shape's geometry.</span></span> <span data-ttu-id="0501d-108">Если значение составляет 100 %, ограниченная геометрия заливки фигуры не следует за геометрией фигуры.</span><span class="sxs-lookup"><span data-stu-id="0501d-108">If the value is 100%, the bounding geometry of the shape's fill does not follow the geometry of the shape.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="0501d-109">Примечания</span><span class="sxs-lookup"><span data-stu-id="0501d-109">Remarks</span></span>

<span data-ttu-id="0501d-110">Для наилучших результатов идеальный диапазон значений для ячейки **SketchFillChange** находится в диапазоне от 15% до 50%.</span><span class="sxs-lookup"><span data-stu-id="0501d-110">For best results, the ideal range of values for the **SketchFillChange** cell is between 15% and 50%.</span></span> <span data-ttu-id="0501d-111">Значение ниже 15 % почти не заметно; Значение больше 50% все чаще случайным образом.</span><span class="sxs-lookup"><span data-stu-id="0501d-111">A value below 15% is barely noticeable; a value greater than 50% is increasingly more randomized.</span></span> 
  
<span data-ttu-id="0501d-112">Чтобы получить ссылку на ячейку **SketchFillChange** по имени из другой формулы, по значению атрибута **N** элемента **Cell** или из программы, использующей свойство **CellsU,** используйте:</span><span class="sxs-lookup"><span data-stu-id="0501d-112">To get a reference to the **SketchFillChange** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="0501d-113">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="0501d-113">Cell name:</span></span>  <br/> | <span data-ttu-id="0501d-114">SketchFillChange</span><span class="sxs-lookup"><span data-stu-id="0501d-114">SketchFillChange</span></span>  <br/> |
   
<span data-ttu-id="0501d-115">Чтобы получить ссылку на ячейку **SketchFillChange** по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="0501d-115">To get a reference to the **SketchFillChange** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="0501d-116">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="0501d-116">Section index:</span></span>  <br/> |<span data-ttu-id="0501d-117">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="0501d-117">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="0501d-118">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="0501d-118">Row index:</span></span>  <br/> |<span data-ttu-id="0501d-119">**visRowOtherEffectProperties**</span><span class="sxs-lookup"><span data-stu-id="0501d-119">**visRowOtherEffectProperties**</span></span> <br/> |
| <span data-ttu-id="0501d-120">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="0501d-120">Cell index:</span></span>  <br/> |<span data-ttu-id="0501d-121">**visSketchFillChange**</span><span class="sxs-lookup"><span data-stu-id="0501d-121">**visSketchFillChange**</span></span> <br/> |
   

