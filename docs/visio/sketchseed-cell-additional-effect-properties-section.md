---
title: Ячейка SketchSeed (раздел "Дополнительные свойства эффекта")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6f62650d-36f8-4c6e-b79f-c9c397a5954d
description: Представляет значение случайный выбор используется для определения геометрии эффекта эскиза как положительное целое число. Значение ячейки SketchSeed создается случайным образом при применении эффекта эскиза фигуры.
ms.openlocfilehash: 7c9d23e19da1a94bb37f1fc916e2f08095976d09
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19814885"
---
# <a name="sketchseed-cell-additional-effect-properties-section"></a><span data-ttu-id="89c84-104">Ячейка SketchSeed (раздел "Дополнительные свойства эффекта")</span><span class="sxs-lookup"><span data-stu-id="89c84-104">SketchSeed Cell (Additional Effect Properties Section)</span></span>

<span data-ttu-id="89c84-105">Представляет значение случайный выбор используется для определения геометрии эффекта эскиза как положительное целое число.</span><span class="sxs-lookup"><span data-stu-id="89c84-105">Represents a randomization value used to determine the geometry of a sketch effect, as a positive integer.</span></span> <span data-ttu-id="89c84-106">Значение ячейки **SketchSeed** создается случайным образом при применении эффекта эскиза фигуры.</span><span class="sxs-lookup"><span data-stu-id="89c84-106">The value of the **SketchSeed** cell is randomly created when a sketch effect is applied to the shape.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="89c84-107">Замечания</span><span class="sxs-lookup"><span data-stu-id="89c84-107">Remarks</span></span>

<span data-ttu-id="89c84-108">Для получения ссылки на ячейки **SketchSeed** по имени из другой формулы, по значению атрибута **N** элемент **ячейки** и программы, с помощью свойства **CellsU** , используйте:</span><span class="sxs-lookup"><span data-stu-id="89c84-108">To get a reference to the **SketchSeed** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="89c84-109">Имя ячейки.</span><span class="sxs-lookup"><span data-stu-id="89c84-109">Cell name:</span></span>  <br/> | <span data-ttu-id="89c84-110">SketchSeed</span><span class="sxs-lookup"><span data-stu-id="89c84-110">SketchSeed</span></span>  <br/> |
   
<span data-ttu-id="89c84-111">Для получения ссылки на ячейки **SketchSeed** по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы:</span><span class="sxs-lookup"><span data-stu-id="89c84-111">To get a reference to the **SketchSeed** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="89c84-112">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="89c84-112">Section index:</span></span>  <br/> |<span data-ttu-id="89c84-113">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="89c84-113">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="89c84-114">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="89c84-114">Row index:</span></span>  <br/> |<span data-ttu-id="89c84-115">**visRowOtherEffectProperties**</span><span class="sxs-lookup"><span data-stu-id="89c84-115">**visRowOtherEffectProperties**</span></span> <br/> |
| <span data-ttu-id="89c84-116">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="89c84-116">Cell index:</span></span>  <br/> |<span data-ttu-id="89c84-117">**visSketchSeed**</span><span class="sxs-lookup"><span data-stu-id="89c84-117">**visSketchSeed**</span></span> <br/> |
   

