---
title: SketchLineWeight Cell (Additional Effect Properties Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6cb838be-1d6d-48e1-8e9e-bd126f0c2385
description: Определяет дополнительную толщину, добавленную к весу строки в результате эффекта эскиза, в точках от 0 до 50. Толщина линии фигуры увеличивается по мере увеличения значения ячейки SketchLineWeight.
ms.openlocfilehash: 0ee71bbaec59f5c79b72314b08478f8028b4e0ba
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33404514"
---
# <a name="sketchlineweight-cell-additional-effect-properties-section"></a><span data-ttu-id="735b8-104">SketchLineWeight Cell (Additional Effect Properties Section)</span><span class="sxs-lookup"><span data-stu-id="735b8-104">SketchLineWeight Cell (Additional Effect Properties Section)</span></span>

<span data-ttu-id="735b8-105">Определяет дополнительную толщину, добавленную к весу строки в результате эффекта эскиза, в точках от 0 до 50.</span><span class="sxs-lookup"><span data-stu-id="735b8-105">Determines the additional thickness added to line weight as the result of a sketch effect, in points from 0 to 50.</span></span> <span data-ttu-id="735b8-106">Толщина линии фигуры увеличивается по мере увеличения значения ячейки **SketchLineWeight.**</span><span class="sxs-lookup"><span data-stu-id="735b8-106">The thickness of a shape's line increases as the value of the **SketchLineWeight** cell increases.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="735b8-107">Примечания</span><span class="sxs-lookup"><span data-stu-id="735b8-107">Remarks</span></span>

<span data-ttu-id="735b8-108">Чтобы получить ссылку на ячейку **SketchLineWeight** по имени из другой формулы, по значению атрибута **N** элемента **Cell** или из программы, использующей свойство **CellsU,** используйте:</span><span class="sxs-lookup"><span data-stu-id="735b8-108">To get a reference to the **SketchLineWeight** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="735b8-109">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="735b8-109">Cell name:</span></span>  <br/> | <span data-ttu-id="735b8-110">SketchLineWeight</span><span class="sxs-lookup"><span data-stu-id="735b8-110">SketchLineWeight</span></span>  <br/> |
   
<span data-ttu-id="735b8-111">Чтобы получить ссылку на **ячейку SketchLineWeight** по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="735b8-111">To get a reference to the **SketchLineWeight** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="735b8-112">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="735b8-112">Section index:</span></span>  <br/> |<span data-ttu-id="735b8-113">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="735b8-113">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="735b8-114">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="735b8-114">Row index:</span></span>  <br/> |<span data-ttu-id="735b8-115">**visRowOtherEffectProperties**</span><span class="sxs-lookup"><span data-stu-id="735b8-115">**visRowOtherEffectProperties**</span></span> <br/> |
| <span data-ttu-id="735b8-116">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="735b8-116">Cell index:</span></span>  <br/> |<span data-ttu-id="735b8-117">**visSketchLineWeight**</span><span class="sxs-lookup"><span data-stu-id="735b8-117">**visSketchLineWeight**</span></span> <br/> |
   

