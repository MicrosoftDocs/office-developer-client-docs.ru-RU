---
title: ReplaceCopyCells Cell (Change Shape Behavior Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 2f36aefd-da49-47ea-9b90-2fa1a2298849
description: Указывает список ячеек таблицы свойств фигуры, которые копируются из старой фигуры в фигуру замены во время операции замены фигуры.
ms.openlocfilehash: f2a7908a623c861d0284821b2d8ae5fc71690685
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409344"
---
# <a name="replacecopycells-cell-change-shape-behavior-section"></a><span data-ttu-id="b3c39-103">ReplaceCopyCells Cell (Change Shape Behavior Section)</span><span class="sxs-lookup"><span data-stu-id="b3c39-103">ReplaceCopyCells Cell (Change Shape Behavior Section)</span></span>

<span data-ttu-id="b3c39-104">Указывает список ячеек таблицы свойств фигуры, которые копируются из старой фигуры в фигуру замены во время операции замены фигуры.</span><span class="sxs-lookup"><span data-stu-id="b3c39-104">Indicates a list of cells in the ShapeSheet that are copied from an old shape to the replacement shape during a shape replacement operation.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="b3c39-105">Примечания</span><span class="sxs-lookup"><span data-stu-id="b3c39-105">Remarks</span></span>

<span data-ttu-id="b3c39-106">Образец фигуры замены должен содержать вызов функции **DEPENDSON** в ячейке **ReplaceCopyCells** , где каждый аргумент функции является ссылкой на ячейку.</span><span class="sxs-lookup"><span data-stu-id="b3c39-106">The master shape of the replacement must contain a **DEPENDSON** function call in the **ReplaceCopyCells** cell, where each argument in the function is a reference to a cell.</span></span> <span data-ttu-id="b3c39-107">Эти ячейки копируются из старой фигуры в фигуру, которая является результатом операции замены фигур, независимо от того, где они находятся в таблице свойств фигуры.</span><span class="sxs-lookup"><span data-stu-id="b3c39-107">Those cells are copied from the old shape to the shape that results from a shape replacement operation, regardless of where they are in the ShapeSheet.</span></span> 
  
<span data-ttu-id="b3c39-108">Значения и/или формулы, ссылающиеся на другие ячейки, копируются в полученную фигуру.</span><span class="sxs-lookup"><span data-stu-id="b3c39-108">Values and/or formulas that reference other cells are copied to the resulting shape.</span></span> <span data-ttu-id="b3c39-109">Если в полученной фигуре нет указанной ячейки, то скопированная ячейка содержит только значение.</span><span class="sxs-lookup"><span data-stu-id="b3c39-109">If the resulting shape does not have the referenced cell, the copied cell contains the value only.</span></span> 
  
<span data-ttu-id="b3c39-110">Ссылки в ячейке **ReplaceCopyCells** переопределяют защиту для ячеек, как определено в разделе **Защита** , и в ячейках **ReplaceLockFormat**, **ReplaceLockShapeData**и **ReplaceLockText** .</span><span class="sxs-lookup"><span data-stu-id="b3c39-110">References in the **ReplaceCopyCells** cell override protection set on cells as defined in the **Protection** section and the **ReplaceLockFormat**, **ReplaceLockShapeData**, and **ReplaceLockText** cells.</span></span> 
  
<span data-ttu-id="b3c39-111">Чтобы получить ссылку на ячейку **ReplaceCopyCells** по имени из другой формулы, по значению атрибута **N** элемента **ячейки** или из программы с помощью свойства **CellsU** , используйте:</span><span class="sxs-lookup"><span data-stu-id="b3c39-111">To get a reference to the **ReplaceCopyCells** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="b3c39-112">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="b3c39-112">Cell name:</span></span>  <br/> | <span data-ttu-id="b3c39-113">ReplaceCopyCells</span><span class="sxs-lookup"><span data-stu-id="b3c39-113">ReplaceCopyCells</span></span>  <br/> |
   
<span data-ttu-id="b3c39-114">Чтобы получить ссылку на ячейку **ReplaceCopyCells** по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="b3c39-114">To get a reference to the **ReplaceCopyCells** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="b3c39-115">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="b3c39-115">Section index:</span></span>  <br/> |<span data-ttu-id="b3c39-116">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="b3c39-116">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="b3c39-117">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="b3c39-117">Row index:</span></span>  <br/> |<span data-ttu-id="b3c39-118">**Висровреплацебехавиорс**</span><span class="sxs-lookup"><span data-stu-id="b3c39-118">**visRowReplaceBehaviors**</span></span> <br/> |
| <span data-ttu-id="b3c39-119">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="b3c39-119">Cell index:</span></span>  <br/> |<span data-ttu-id="b3c39-120">**Висреплацекопицеллс**</span><span class="sxs-lookup"><span data-stu-id="b3c39-120">**visReplaceCopyCells**</span></span> <br/> |
   

