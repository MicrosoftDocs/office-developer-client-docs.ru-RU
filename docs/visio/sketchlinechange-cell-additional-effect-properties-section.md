---
title: Ячейка SketchLineChange (раздел "Дополнительные свойства эффекта")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 39192535-b55b-4c49-b63f-edb542c7a2e5
description: Определяет объем случайный выбор строки фигуры с геометрией фигуры при использовании эффекта эскиза в процентном соотношении от Длина раздела. Если ячейка SketchLineChange имеет значение 0%, Геометрия фигуры строки соответствует Геометрия фигуры. Если значение равно 100%, Геометрия фигуры строки не соответствует Геометрия фигуры.
ms.openlocfilehash: 57d2af1a914710d7e5a58686b577014ceb7af424
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19814882"
---
# <a name="sketchlinechange-cell-additional-effect-properties-section"></a><span data-ttu-id="b0c26-105">Ячейка SketchLineChange (раздел "Дополнительные свойства эффекта")</span><span class="sxs-lookup"><span data-stu-id="b0c26-105">SketchLineChange Cell (Additional Effect Properties Section)</span></span>

<span data-ttu-id="b0c26-106">Определяет объем случайный выбор строки фигуры с геометрией фигуры при использовании эффекта эскиза в процентном соотношении от Длина раздела.</span><span class="sxs-lookup"><span data-stu-id="b0c26-106">Determines the amount of randomization of the shape's line from the shape's geometry when using a sketch effect, as a percentage of the length of a section.</span></span> <span data-ttu-id="b0c26-107">Если ячейка **SketchLineChange** имеет значение 0%, Геометрия фигуры строки соответствует Геометрия фигуры.</span><span class="sxs-lookup"><span data-stu-id="b0c26-107">If the value of the **SketchLineChange** cell is set to 0%, the geometry of the shape's line matches the shape's geometry.</span></span> <span data-ttu-id="b0c26-108">Если значение равно 100%, Геометрия фигуры строки не соответствует Геометрия фигуры.</span><span class="sxs-lookup"><span data-stu-id="b0c26-108">If the value is 100%, the geometry of the shape's line does not follow the geometry of the shape.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="b0c26-109">Замечания</span><span class="sxs-lookup"><span data-stu-id="b0c26-109">Remarks</span></span>

<span data-ttu-id="b0c26-110">Для достижения наилучших результатов идеальный диапазон значений для ячейки **SketchLineChange** находится в пределах 15% и 50%.</span><span class="sxs-lookup"><span data-stu-id="b0c26-110">For best results, the ideal range of values for the **SketchLineChange** cell is between 15% and 50%.</span></span> <span data-ttu-id="b0c26-111">Значение меньше 15% трудно заметить; значение больше, чем 50% может слишком много randomize строки.</span><span class="sxs-lookup"><span data-stu-id="b0c26-111">A value below 15% is barely noticeable; a value greater than 50% could randomize the line too much.</span></span> 
  
<span data-ttu-id="b0c26-112">Для получения ссылки на ячейки **SketchLineChange** по имени из другой формулы, по значению атрибута **N** элемент **ячейки** и программы, с помощью свойства **CellsU** , используйте:</span><span class="sxs-lookup"><span data-stu-id="b0c26-112">To get a reference to the **SketchLineChange** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="b0c26-113">Имя ячейки.</span><span class="sxs-lookup"><span data-stu-id="b0c26-113">Cell name:</span></span>  <br/> | <span data-ttu-id="b0c26-114">SketchLineChange</span><span class="sxs-lookup"><span data-stu-id="b0c26-114">SketchLineChange</span></span>  <br/> |
   
<span data-ttu-id="b0c26-115">Для получения ссылки на ячейки **SketchLineChange** по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы:</span><span class="sxs-lookup"><span data-stu-id="b0c26-115">To get a reference to the **SketchLineChange** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="b0c26-116">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="b0c26-116">Section index:</span></span>  <br/> |<span data-ttu-id="b0c26-117">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="b0c26-117">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="b0c26-118">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="b0c26-118">Row index:</span></span>  <br/> |<span data-ttu-id="b0c26-119">**visRowOtherEffectProperties**</span><span class="sxs-lookup"><span data-stu-id="b0c26-119">**visRowOtherEffectProperties**</span></span> <br/> |
| <span data-ttu-id="b0c26-120">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="b0c26-120">Cell index:</span></span>  <br/> |<span data-ttu-id="b0c26-121">**visSketchLineChange**</span><span class="sxs-lookup"><span data-stu-id="b0c26-121">**visSketchLineChange**</span></span> <br/> |
   

