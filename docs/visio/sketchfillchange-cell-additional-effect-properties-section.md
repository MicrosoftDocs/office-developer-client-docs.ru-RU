---
title: SketchFillChange Cell (Additional Effect Properties Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 939f8f90-dee5-4175-b32a-e2964eb40681
description: Определяет степень случайности заливки фигуры на основе геометрии фигуры при использовании эффекты эскиза в процентном соотношении от длины раздела. Если для ячейки SketchFillChange задано значение 0%, связанная геометрия заливки фигуры соответствует геометрии фигуры. Если значение равно 100%, ограничительная геометрия заливки фигуры не будет соответствовать геометрии фигуры.
ms.openlocfilehash: 8726e9dd6ca6257fb8dbbbef3dce1d4ec344e28b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32339816"
---
# <a name="sketchfillchange-cell-additional-effect-properties-section"></a><span data-ttu-id="16193-105">SketchFillChange Cell (Additional Effect Properties Section)</span><span class="sxs-lookup"><span data-stu-id="16193-105">SketchFillChange Cell (Additional Effect Properties Section)</span></span>

<span data-ttu-id="16193-106">Определяет степень случайности заливки фигуры на основе геометрии фигуры при использовании эффекты эскиза в процентном соотношении от длины раздела.</span><span class="sxs-lookup"><span data-stu-id="16193-106">Determines the amount of randomization of the shape's fill from the shape's geometry when using a sketch effect, as a percentage of the length of a section.</span></span> <span data-ttu-id="16193-107">Если для ячейки **SketchFillChange** задано значение 0%, связанная геометрия заливки фигуры соответствует геометрии фигуры.</span><span class="sxs-lookup"><span data-stu-id="16193-107">If the value of the **SketchFillChange** cell is set to 0%, the bounding geometry of a shape's fill matches the shape's geometry.</span></span> <span data-ttu-id="16193-108">Если значение равно 100%, ограничительная геометрия заливки фигуры не будет соответствовать геометрии фигуры.</span><span class="sxs-lookup"><span data-stu-id="16193-108">If the value is 100%, the bounding geometry of the shape's fill does not follow the geometry of the shape.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="16193-109">Комментарии</span><span class="sxs-lookup"><span data-stu-id="16193-109">Remarks</span></span>

<span data-ttu-id="16193-110">Для достижения лучших результатов идеальный диапазон значений для ячейки **SketchFillChange** составляет от 15 до 50%.</span><span class="sxs-lookup"><span data-stu-id="16193-110">For best results, the ideal range of values for the **SketchFillChange** cell is between 15% and 50%.</span></span> <span data-ttu-id="16193-111">Значение, меньшее 15%, практически заметно; значение, превышающее 50%, становится более случайным.</span><span class="sxs-lookup"><span data-stu-id="16193-111">A value below 15% is barely noticeable; a value greater than 50% is increasingly more randomized.</span></span> 
  
<span data-ttu-id="16193-112">Чтобы получить ссылку на ячейку **SketchFillChange** по имени из другой формулы, по значению атрибута **N** элемента **ячейки** или из программы с помощью свойства **CellsU** , используйте:</span><span class="sxs-lookup"><span data-stu-id="16193-112">To get a reference to the **SketchFillChange** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="16193-113">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="16193-113">Cell name:</span></span>  <br/> | <span data-ttu-id="16193-114">SketchFillChange</span><span class="sxs-lookup"><span data-stu-id="16193-114">SketchFillChange</span></span>  <br/> |
   
<span data-ttu-id="16193-115">Чтобы получить ссылку на ячейку **SketchFillChange** по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="16193-115">To get a reference to the **SketchFillChange** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="16193-116">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="16193-116">Section index:</span></span>  <br/> |<span data-ttu-id="16193-117">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="16193-117">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="16193-118">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="16193-118">Row index:</span></span>  <br/> |<span data-ttu-id="16193-119">**Висровосереффектпропертиес**</span><span class="sxs-lookup"><span data-stu-id="16193-119">**visRowOtherEffectProperties**</span></span> <br/> |
| <span data-ttu-id="16193-120">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="16193-120">Cell index:</span></span>  <br/> |<span data-ttu-id="16193-121">**Висскетчфиллчанже**</span><span class="sxs-lookup"><span data-stu-id="16193-121">**visSketchFillChange**</span></span> <br/> |
   

