---
title: SketchLineChange Cell (Additional Effect Properties Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 39192535-b55b-4c49-b63f-edb542c7a2e5
description: Определяет количество рандомизации линии фигуры из геометрии фигуры при использовании эффекта эскиза в процентах от длины раздела. Если значение ячейки SketchLineChange установлено до 0%, геометрия линии фигуры соответствует геометрии фигуры. Если значение 100%, геометрия линии фигуры не следует геометрии фигуры.
ms.openlocfilehash: ba57a4d2e43a91475f4c3ab4862f723eb2653a89
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33419508"
---
# <a name="sketchlinechange-cell-additional-effect-properties-section"></a><span data-ttu-id="4cfe6-105">SketchLineChange Cell (Additional Effect Properties Section)</span><span class="sxs-lookup"><span data-stu-id="4cfe6-105">SketchLineChange Cell (Additional Effect Properties Section)</span></span>

<span data-ttu-id="4cfe6-106">Определяет количество рандомизации линии фигуры из геометрии фигуры при использовании эффекта эскиза в процентах от длины раздела.</span><span class="sxs-lookup"><span data-stu-id="4cfe6-106">Determines the amount of randomization of the shape's line from the shape's geometry when using a sketch effect, as a percentage of the length of a section.</span></span> <span data-ttu-id="4cfe6-107">Если значение ячейки **SketchLineChange** установлено до 0%, геометрия линии фигуры соответствует геометрии фигуры.</span><span class="sxs-lookup"><span data-stu-id="4cfe6-107">If the value of the **SketchLineChange** cell is set to 0%, the geometry of the shape's line matches the shape's geometry.</span></span> <span data-ttu-id="4cfe6-108">Если значение 100%, геометрия линии фигуры не следует геометрии фигуры.</span><span class="sxs-lookup"><span data-stu-id="4cfe6-108">If the value is 100%, the geometry of the shape's line does not follow the geometry of the shape.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="4cfe6-109">Примечания</span><span class="sxs-lookup"><span data-stu-id="4cfe6-109">Remarks</span></span>

<span data-ttu-id="4cfe6-110">Для наилучших результатов идеальный диапазон значений для ячейки **SketchLineChange** составляет от 15% до 50%.</span><span class="sxs-lookup"><span data-stu-id="4cfe6-110">For best results, the ideal range of values for the **SketchLineChange** cell is between 15% and 50%.</span></span> <span data-ttu-id="4cfe6-111">Значение ниже 15% едва заметно; значение, большее 50%, может слишком рандомизировать строку.</span><span class="sxs-lookup"><span data-stu-id="4cfe6-111">A value below 15% is barely noticeable; a value greater than 50% could randomize the line too much.</span></span> 
  
<span data-ttu-id="4cfe6-112">Чтобы получить ссылку на ячейку **SketchLineChange** по имени из другой формулы, по значению атрибута **N** элемента **Cell** или из программы с использованием свойства **CellsU,** используйте:</span><span class="sxs-lookup"><span data-stu-id="4cfe6-112">To get a reference to the **SketchLineChange** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="4cfe6-113">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="4cfe6-113">Cell name:</span></span>  <br/> | <span data-ttu-id="4cfe6-114">SketchLineChange</span><span class="sxs-lookup"><span data-stu-id="4cfe6-114">SketchLineChange</span></span>  <br/> |
   
<span data-ttu-id="4cfe6-115">Чтобы получить ссылку на **ячейку SketchLineChange** по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="4cfe6-115">To get a reference to the **SketchLineChange** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="4cfe6-116">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="4cfe6-116">Section index:</span></span>  <br/> |<span data-ttu-id="4cfe6-117">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="4cfe6-117">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="4cfe6-118">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="4cfe6-118">Row index:</span></span>  <br/> |<span data-ttu-id="4cfe6-119">**visRowOtherEffectProperties**</span><span class="sxs-lookup"><span data-stu-id="4cfe6-119">**visRowOtherEffectProperties**</span></span> <br/> |
| <span data-ttu-id="4cfe6-120">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="4cfe6-120">Cell index:</span></span>  <br/> |<span data-ttu-id="4cfe6-121">**visSketchLineChange**</span><span class="sxs-lookup"><span data-stu-id="4cfe6-121">**visSketchLineChange**</span></span> <br/> |
   

