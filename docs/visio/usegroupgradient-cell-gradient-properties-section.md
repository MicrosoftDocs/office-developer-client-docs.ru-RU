---
title: UseGroupGradient Cell (Gradient Properties Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: f1dcf0ec-8b4a-4ee1-9208-b1c84e30d37b
description: Определяет, принимает ли фигура градиент, если фигура сгруппирована вместе с другими фигурами в качестве boolean. Значение ячейки UseGroupGradient влияет только на заливку фигуры.
ms.openlocfilehash: a69b48095aec93705c686a5401051f1d1e368d18
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33411367"
---
# <a name="usegroupgradient-cell-gradient-properties-section"></a><span data-ttu-id="88797-104">UseGroupGradient Cell (Gradient Properties Section)</span><span class="sxs-lookup"><span data-stu-id="88797-104">UseGroupGradient Cell (Gradient Properties Section)</span></span>

<span data-ttu-id="88797-105">Определяет, принимает ли фигура градиент, если фигура сгруппирована вместе с другими фигурами в качестве boolean.</span><span class="sxs-lookup"><span data-stu-id="88797-105">Determines whether the shape takes on a gradient when the shape is grouped together with other shapes, as a Boolean.</span></span> <span data-ttu-id="88797-106">Значение ячейки **UseGroupGradient** влияет только на заливку фигуры.</span><span class="sxs-lookup"><span data-stu-id="88797-106">The value of **UseGroupGradient** cell affects the shape fill only.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="88797-107">Примечания</span><span class="sxs-lookup"><span data-stu-id="88797-107">Remarks</span></span>

<span data-ttu-id="88797-108">Чтобы получить ссылку на ячейку **UseGroupGradient** по имени из другой формулы, по значению атрибута **N** элемента **Cell** или из программы, использующей свойство **CellsU,** используйте:</span><span class="sxs-lookup"><span data-stu-id="88797-108">To get a reference to the **UseGroupGradient** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="88797-109">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="88797-109">Cell name:</span></span>  <br/> | <span data-ttu-id="88797-110">UseGroupGradient</span><span class="sxs-lookup"><span data-stu-id="88797-110">UseGroupGradient</span></span>  <br/> |
   
<span data-ttu-id="88797-111">Чтобы получить ссылку на ячейку **UseGroupGradient** по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="88797-111">To get a reference to the **UseGroupGradient** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="88797-112">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="88797-112">Section index:</span></span>  <br/> |<span data-ttu-id="88797-113">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="88797-113">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="88797-114">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="88797-114">Row index:</span></span>  <br/> |<span data-ttu-id="88797-115">**visRowGradientProperties**</span><span class="sxs-lookup"><span data-stu-id="88797-115">**visRowGradientProperties**</span></span> <br/> |
| <span data-ttu-id="88797-116">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="88797-116">Cell index:</span></span>  <br/> |<span data-ttu-id="88797-117">\*\*visUseGroupGradient \*\*</span><span class="sxs-lookup"><span data-stu-id="88797-117">\*\*visUseGroupGradient \*\*</span></span> <br/> |
   

