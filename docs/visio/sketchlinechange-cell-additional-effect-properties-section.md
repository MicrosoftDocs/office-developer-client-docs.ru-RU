---
title: SketchLineChange Cell (Additional Effect Properties Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 39192535-b55b-4c49-b63f-edb542c7a2e5
description: Определяет объем случайного выбора линии фигуры из геометрии фигуры при использовании эффекта наброска в процентах от длины раздела. Если значение ячейки SketchLineChange — 0%, геометрия линии фигуры соответствует геометрии фигуры. Если значение составляет 100 %, геометрия линии фигуры не следует за геометрией фигуры.
ms.openlocfilehash: ba57a4d2e43a91475f4c3ab4862f723eb2653a89
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33419508"
---
# <a name="sketchlinechange-cell-additional-effect-properties-section"></a><span data-ttu-id="ccfb5-105">SketchLineChange Cell (Additional Effect Properties Section)</span><span class="sxs-lookup"><span data-stu-id="ccfb5-105">SketchLineChange Cell (Additional Effect Properties Section)</span></span>

<span data-ttu-id="ccfb5-106">Определяет объем случайного выбора линии фигуры из геометрии фигуры при использовании эффекта наброска в процентах от длины раздела.</span><span class="sxs-lookup"><span data-stu-id="ccfb5-106">Determines the amount of randomization of the shape's line from the shape's geometry when using a sketch effect, as a percentage of the length of a section.</span></span> <span data-ttu-id="ccfb5-107">Если значение ячейки **SketchLineChange** — 0%, геометрия линии фигуры соответствует геометрии фигуры.</span><span class="sxs-lookup"><span data-stu-id="ccfb5-107">If the value of the **SketchLineChange** cell is set to 0%, the geometry of the shape's line matches the shape's geometry.</span></span> <span data-ttu-id="ccfb5-108">Если значение составляет 100 %, геометрия линии фигуры не следует за геометрией фигуры.</span><span class="sxs-lookup"><span data-stu-id="ccfb5-108">If the value is 100%, the geometry of the shape's line does not follow the geometry of the shape.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="ccfb5-109">Примечания</span><span class="sxs-lookup"><span data-stu-id="ccfb5-109">Remarks</span></span>

<span data-ttu-id="ccfb5-110">Для наилучших результатов идеальный диапазон значений для ячейки **SketchLineChange** находится в диапазоне от 15% до 50%.</span><span class="sxs-lookup"><span data-stu-id="ccfb5-110">For best results, the ideal range of values for the **SketchLineChange** cell is between 15% and 50%.</span></span> <span data-ttu-id="ccfb5-111">Значение ниже 15 % почти не заметно; Значение больше 50 % может привести к слишком большому случайному выбору строки.</span><span class="sxs-lookup"><span data-stu-id="ccfb5-111">A value below 15% is barely noticeable; a value greater than 50% could randomize the line too much.</span></span> 
  
<span data-ttu-id="ccfb5-112">Чтобы получить ссылку на ячейку **SketchLineChange** по имени из другой формулы, по значению атрибута **N** элемента **Cell** или из программы, использующей свойство **CellsU,** используйте:</span><span class="sxs-lookup"><span data-stu-id="ccfb5-112">To get a reference to the **SketchLineChange** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="ccfb5-113">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="ccfb5-113">Cell name:</span></span>  <br/> | <span data-ttu-id="ccfb5-114">SketchLineChange</span><span class="sxs-lookup"><span data-stu-id="ccfb5-114">SketchLineChange</span></span>  <br/> |
   
<span data-ttu-id="ccfb5-115">Чтобы получить ссылку на ячейку **SketchLineChange** по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="ccfb5-115">To get a reference to the **SketchLineChange** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="ccfb5-116">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="ccfb5-116">Section index:</span></span>  <br/> |<span data-ttu-id="ccfb5-117">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="ccfb5-117">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="ccfb5-118">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="ccfb5-118">Row index:</span></span>  <br/> |<span data-ttu-id="ccfb5-119">**visRowOtherEffectProperties**</span><span class="sxs-lookup"><span data-stu-id="ccfb5-119">**visRowOtherEffectProperties**</span></span> <br/> |
| <span data-ttu-id="ccfb5-120">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="ccfb5-120">Cell index:</span></span>  <br/> |<span data-ttu-id="ccfb5-121">**visSketchLineChange**</span><span class="sxs-lookup"><span data-stu-id="ccfb5-121">**visSketchLineChange**</span></span> <br/> |
   

