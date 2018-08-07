---
title: Ячейка ReplaceCopyCells (раздел "Изменение поведения фигуры")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 2f36aefd-da49-47ea-9b90-2fa1a2298849
description: Указывает список ячеек в таблице свойств фигуры, которые копируются из старой фигуры фигуры замещения во время операции замены фигуры.
ms.openlocfilehash: 1e3b5e4dbc29372f75b7a7ed8013a7dd82d94e1d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19814566"
---
# <a name="replacecopycells-cell-change-shape-behavior-section"></a><span data-ttu-id="9bce2-103">Ячейка ReplaceCopyCells (раздел "Изменение поведения фигуры")</span><span class="sxs-lookup"><span data-stu-id="9bce2-103">ReplaceCopyCells Cell (Change Shape Behavior Section)</span></span>

<span data-ttu-id="9bce2-104">Указывает список ячеек в таблице свойств фигуры, которые копируются из старой фигуры фигуры замещения во время операции замены фигуры.</span><span class="sxs-lookup"><span data-stu-id="9bce2-104">Indicates a list of cells in the ShapeSheet that are copied from an old shape to the replacement shape during a shape replacement operation.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="9bce2-105">Замечания</span><span class="sxs-lookup"><span data-stu-id="9bce2-105">Remarks</span></span>

<span data-ttu-id="9bce2-106">Основной фигуры замены должно содержать вызов функции **DEPENDSON** в ячейке **ReplaceCopyCells** , где каждый аргумент в функцию — это ссылка на ячейку.</span><span class="sxs-lookup"><span data-stu-id="9bce2-106">The master shape of the replacement must contain a **DEPENDSON** function call in the **ReplaceCopyCells** cell, where each argument in the function is a reference to a cell.</span></span> <span data-ttu-id="9bce2-107">Эти ячейки копируются из старой фигуры в фигуру, результатом операции замены фигуры, независимо от того, где они находятся в таблице свойств фигуры.</span><span class="sxs-lookup"><span data-stu-id="9bce2-107">Those cells are copied from the old shape to the shape that results from a shape replacement operation, regardless of where they are in the ShapeSheet.</span></span> 
  
<span data-ttu-id="9bce2-108">Результирующая фигура копируются значения и/или формулы, ссылающиеся на другие ячейки.</span><span class="sxs-lookup"><span data-stu-id="9bce2-108">Values and/or formulas that reference other cells are copied to the resulting shape.</span></span> <span data-ttu-id="9bce2-109">Если результирующая фигура не имеет связанной ячейки, скопированные ячейки содержит только значение.</span><span class="sxs-lookup"><span data-stu-id="9bce2-109">If the resulting shape does not have the referenced cell, the copied cell contains the value only.</span></span> 
  
<span data-ttu-id="9bce2-110">Ссылки в ячейке **ReplaceCopyCells** переопределить set защиты для ячеек, определенных в разделе **Защита** и **ReplaceLockFormat**, **ReplaceLockShapeData**и **ReplaceLockText** ячеек.</span><span class="sxs-lookup"><span data-stu-id="9bce2-110">References in the **ReplaceCopyCells** cell override protection set on cells as defined in the **Protection** section and the **ReplaceLockFormat**, **ReplaceLockShapeData**, and **ReplaceLockText** cells.</span></span> 
  
<span data-ttu-id="9bce2-111">Для получения ссылки на ячейки **ReplaceCopyCells** по имени из другой формулы, по значению атрибута **N** элемент **ячейки** и программы, с помощью свойства **CellsU** , используйте:</span><span class="sxs-lookup"><span data-stu-id="9bce2-111">To get a reference to the **ReplaceCopyCells** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="9bce2-112">Имя ячейки.</span><span class="sxs-lookup"><span data-stu-id="9bce2-112">Cell name:</span></span>  <br/> | <span data-ttu-id="9bce2-113">ReplaceCopyCells</span><span class="sxs-lookup"><span data-stu-id="9bce2-113">ReplaceCopyCells</span></span>  <br/> |
   
<span data-ttu-id="9bce2-114">Для получения ссылки на ячейки **ReplaceCopyCells** по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы:</span><span class="sxs-lookup"><span data-stu-id="9bce2-114">To get a reference to the **ReplaceCopyCells** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="9bce2-115">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="9bce2-115">Section index:</span></span>  <br/> |<span data-ttu-id="9bce2-116">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="9bce2-116">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="9bce2-117">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="9bce2-117">Row index:</span></span>  <br/> |<span data-ttu-id="9bce2-118">**visRowReplaceBehaviors**</span><span class="sxs-lookup"><span data-stu-id="9bce2-118">**visRowReplaceBehaviors**</span></span> <br/> |
| <span data-ttu-id="9bce2-119">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="9bce2-119">Cell index:</span></span>  <br/> |<span data-ttu-id="9bce2-120">**visReplaceCopyCells**</span><span class="sxs-lookup"><span data-stu-id="9bce2-120">**visReplaceCopyCells**</span></span> <br/> |
   

