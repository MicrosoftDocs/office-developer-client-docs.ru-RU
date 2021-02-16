---
title: SketchSeed Cell (Additional Effect Properties Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6f62650d-36f8-4c6e-b79f-c9c397a5954d
description: Представляет значение случайности, используемого для определения геометрии эффекта наброска, в качестве положительного значения. Значение ячейки SketchSeed создается случайным образом, когда к фигуре применяется эффект наброска.
ms.openlocfilehash: 3ec58fbfa183d1a6d7bb6960672658f9a6cca073
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33434398"
---
# <a name="sketchseed-cell-additional-effect-properties-section"></a><span data-ttu-id="81faf-104">SketchSeed Cell (Additional Effect Properties Section)</span><span class="sxs-lookup"><span data-stu-id="81faf-104">SketchSeed Cell (Additional Effect Properties Section)</span></span>

<span data-ttu-id="81faf-105">Представляет значение случайности, используемого для определения геометрии эффекта наброска, в качестве положительного значения.</span><span class="sxs-lookup"><span data-stu-id="81faf-105">Represents a randomization value used to determine the geometry of a sketch effect, as a positive integer.</span></span> <span data-ttu-id="81faf-106">Значение ячейки **SketchSeed** создается случайным образом, когда к фигуре применяется эффект наброска.</span><span class="sxs-lookup"><span data-stu-id="81faf-106">The value of the **SketchSeed** cell is randomly created when a sketch effect is applied to the shape.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="81faf-107">Примечания</span><span class="sxs-lookup"><span data-stu-id="81faf-107">Remarks</span></span>

<span data-ttu-id="81faf-108">Чтобы получить ссылку на ячейку **SketchSeed** по имени из другой формулы, по значению атрибута **N** элемента **Cell** или из программы, использующей свойство **CellsU,** используйте:</span><span class="sxs-lookup"><span data-stu-id="81faf-108">To get a reference to the **SketchSeed** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="81faf-109">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="81faf-109">Cell name:</span></span>  <br/> | <span data-ttu-id="81faf-110">SketchSeed</span><span class="sxs-lookup"><span data-stu-id="81faf-110">SketchSeed</span></span>  <br/> |
   
<span data-ttu-id="81faf-111">Чтобы получить ссылку на ячейку **SketchSeed** по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="81faf-111">To get a reference to the **SketchSeed** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="81faf-112">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="81faf-112">Section index:</span></span>  <br/> |<span data-ttu-id="81faf-113">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="81faf-113">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="81faf-114">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="81faf-114">Row index:</span></span>  <br/> |<span data-ttu-id="81faf-115">**visRowOtherEffectProperties**</span><span class="sxs-lookup"><span data-stu-id="81faf-115">**visRowOtherEffectProperties**</span></span> <br/> |
| <span data-ttu-id="81faf-116">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="81faf-116">Cell index:</span></span>  <br/> |<span data-ttu-id="81faf-117">**visSketchSeed**</span><span class="sxs-lookup"><span data-stu-id="81faf-117">**visSketchSeed**</span></span> <br/> |
   

