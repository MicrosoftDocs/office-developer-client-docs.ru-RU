---
title: Ячейка SketchFillChange (раздел "Дополнительные свойства эффекта")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 939f8f90-dee5-4175-b32a-e2964eb40681
description: Определяет объем случайный выбор заливки фигуры с геометрией фигуры при использовании эффекта эскиза в процентном соотношении от Длина раздела. Если ячейка SketchFillChange имеет значение 0%, ограничивающий геометрии заливки фигуры сопоставляет Геометрия фигуры. Если значение равно 100%, ограничивающий геометрии заливки фигуры не соответствует Геометрия фигуры.
ms.openlocfilehash: 8dda34e03188909e167a4abda6f62da3d43c4dd7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19814887"
---
# <a name="sketchfillchange-cell-additional-effect-properties-section"></a><span data-ttu-id="18528-105">Ячейка SketchFillChange (раздел "Дополнительные свойства эффекта")</span><span class="sxs-lookup"><span data-stu-id="18528-105">SketchFillChange Cell (Additional Effect Properties Section)</span></span>

<span data-ttu-id="18528-106">Определяет объем случайный выбор заливки фигуры с геометрией фигуры при использовании эффекта эскиза в процентном соотношении от Длина раздела.</span><span class="sxs-lookup"><span data-stu-id="18528-106">Determines the amount of randomization of the shape's fill from the shape's geometry when using a sketch effect, as a percentage of the length of a section.</span></span> <span data-ttu-id="18528-107">Если ячейка **SketchFillChange** имеет значение 0%, ограничивающий геометрии заливки фигуры сопоставляет Геометрия фигуры.</span><span class="sxs-lookup"><span data-stu-id="18528-107">If the value of the **SketchFillChange** cell is set to 0%, the bounding geometry of a shape's fill matches the shape's geometry.</span></span> <span data-ttu-id="18528-108">Если значение равно 100%, ограничивающий геометрии заливки фигуры не соответствует Геометрия фигуры.</span><span class="sxs-lookup"><span data-stu-id="18528-108">If the value is 100%, the bounding geometry of the shape's fill does not follow the geometry of the shape.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="18528-109">Замечания</span><span class="sxs-lookup"><span data-stu-id="18528-109">Remarks</span></span>

<span data-ttu-id="18528-110">Для достижения наилучших результатов идеальный диапазон значений для ячейки **SketchFillChange** находится в пределах 15% и 50%.</span><span class="sxs-lookup"><span data-stu-id="18528-110">For best results, the ideal range of values for the **SketchFillChange** cell is between 15% and 50%.</span></span> <span data-ttu-id="18528-111">Значение меньше 15% трудно заметить; значение больше, чем 50% по мере возрастания более произвольное.</span><span class="sxs-lookup"><span data-stu-id="18528-111">A value below 15% is barely noticeable; a value greater than 50% is increasingly more randomized.</span></span> 
  
<span data-ttu-id="18528-112">Для получения ссылки на ячейки **SketchFillChange** по имени из другой формулы, по значению атрибута **N** элемент **ячейки** и программы, с помощью свойства **CellsU** , используйте:</span><span class="sxs-lookup"><span data-stu-id="18528-112">To get a reference to the **SketchFillChange** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="18528-113">Имя ячейки.</span><span class="sxs-lookup"><span data-stu-id="18528-113">Cell name:</span></span>  <br/> | <span data-ttu-id="18528-114">SketchFillChange</span><span class="sxs-lookup"><span data-stu-id="18528-114">SketchFillChange</span></span>  <br/> |
   
<span data-ttu-id="18528-115">Для получения ссылки на ячейки **SketchFillChange** по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы:</span><span class="sxs-lookup"><span data-stu-id="18528-115">To get a reference to the **SketchFillChange** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="18528-116">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="18528-116">Section index:</span></span>  <br/> |<span data-ttu-id="18528-117">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="18528-117">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="18528-118">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="18528-118">Row index:</span></span>  <br/> |<span data-ttu-id="18528-119">**visRowOtherEffectProperties**</span><span class="sxs-lookup"><span data-stu-id="18528-119">**visRowOtherEffectProperties**</span></span> <br/> |
| <span data-ttu-id="18528-120">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="18528-120">Cell index:</span></span>  <br/> |<span data-ttu-id="18528-121">**visSketchFillChange**</span><span class="sxs-lookup"><span data-stu-id="18528-121">**visSketchFillChange**</span></span> <br/> |
   

