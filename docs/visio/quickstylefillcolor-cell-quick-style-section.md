---
title: QuickStyleFillColor Cell (Quick Style Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 41250e47-404c-40e7-99be-9bb8c1ed5ba2
description: Определяет, какой цвет темы использует Заливка фигуры, в виде целого числа от 0 до 7.
ms.openlocfilehash: 3ace0de7e3bfc878a2101eaca3847ef079b8f919
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407965"
---
# <a name="quickstylefillcolor-cell-quick-style-section"></a><span data-ttu-id="cc965-103">QuickStyleFillColor Cell (Quick Style Section)</span><span class="sxs-lookup"><span data-stu-id="cc965-103">QuickStyleFillColor Cell (Quick Style Section)</span></span>

<span data-ttu-id="cc965-104">Определяет, какой цвет темы использует Заливка фигуры, в виде целого числа от 0 до 7.</span><span class="sxs-lookup"><span data-stu-id="cc965-104">Determines which theme color that a shape's fill uses, as an integer from 0 to 7</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="cc965-105">Значение</span><span class="sxs-lookup"><span data-stu-id="cc965-105">Value</span></span>  <br/> |<span data-ttu-id="cc965-106">Описание</span><span class="sxs-lookup"><span data-stu-id="cc965-106">Description</span></span>  <br/> |
|<span data-ttu-id="cc965-107">нуль</span><span class="sxs-lookup"><span data-stu-id="cc965-107">0</span></span>  <br/> |<span data-ttu-id="cc965-108">Цвет заливки фигур наследуется от цвета темной темы.</span><span class="sxs-lookup"><span data-stu-id="cc965-108">The shape fill color inherits from the Dark theme color.</span></span>  <br/> |
|<span data-ttu-id="cc965-109">1,1</span><span class="sxs-lookup"><span data-stu-id="cc965-109">1</span></span>  <br/> |<span data-ttu-id="cc965-110">Цвет заливки фигур наследуется от цвета светлой темы.</span><span class="sxs-lookup"><span data-stu-id="cc965-110">The shape fill color inherits from the Light theme color.</span></span>  <br/> |
|<span data-ttu-id="cc965-111">2</span><span class="sxs-lookup"><span data-stu-id="cc965-111">2</span></span>  <br/> |<span data-ttu-id="cc965-112">Цвет заливки фигуры наследуется от цвета темы "акцент 1"</span><span class="sxs-lookup"><span data-stu-id="cc965-112">The shape fill color inherits from the Accent 1 theme color</span></span>  <br/> |
|<span data-ttu-id="cc965-113">4</span><span class="sxs-lookup"><span data-stu-id="cc965-113">3</span></span>  <br/> |<span data-ttu-id="cc965-114">Цвет заливки фигуры наследуется от цвета темы "акцент 2"</span><span class="sxs-lookup"><span data-stu-id="cc965-114">The shape fill color inherits from the Accent 2 theme color</span></span>  <br/> |
|<span data-ttu-id="cc965-115">4 </span><span class="sxs-lookup"><span data-stu-id="cc965-115">4</span></span>  <br/> |<span data-ttu-id="cc965-116">Цвет заливки фигуры наследуется от цвета темы "акцент 3"</span><span class="sxs-lookup"><span data-stu-id="cc965-116">The shape fill color inherits from the Accent 3 theme color</span></span>  <br/> |
|<span data-ttu-id="cc965-117">5 </span><span class="sxs-lookup"><span data-stu-id="cc965-117">5</span></span>  <br/> |<span data-ttu-id="cc965-118">Цвет заливки фигуры наследуется от цвета темы "акцент 4"</span><span class="sxs-lookup"><span data-stu-id="cc965-118">The shape fill color inherits from the Accent 4 theme color</span></span>  <br/> |
|<span data-ttu-id="cc965-119">6 </span><span class="sxs-lookup"><span data-stu-id="cc965-119">6</span></span>  <br/> |<span data-ttu-id="cc965-120">Цвет заливки фигуры наследуется от цвета темы "акцент 5"</span><span class="sxs-lookup"><span data-stu-id="cc965-120">The shape fill color inherits from the Accent 5 theme color</span></span>  <br/> |
|<span data-ttu-id="cc965-121">7 </span><span class="sxs-lookup"><span data-stu-id="cc965-121">7</span></span>  <br/> |<span data-ttu-id="cc965-122">Цвет заливки фигуры наследуется от цвета темы "акцент 6"</span><span class="sxs-lookup"><span data-stu-id="cc965-122">The shape fill color inherits from the Accent 6 theme color</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="cc965-123">Примечания</span><span class="sxs-lookup"><span data-stu-id="cc965-123">Remarks</span></span>

<span data-ttu-id="cc965-124">Чтобы получить ссылку на ячейку **QuickStyleFillColor** по имени из другой формулы, по значению атрибута **N** элемента **ячейки** или из программы с помощью свойства **CellsU** , используйте:</span><span class="sxs-lookup"><span data-stu-id="cc965-124">To get a reference to the **QuickStyleFillColor** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="cc965-125">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="cc965-125">Cell name:</span></span>  <br/> | <span data-ttu-id="cc965-126">QuickStyleFillColor</span><span class="sxs-lookup"><span data-stu-id="cc965-126">QuickStyleFillColor</span></span>  <br/> |
   
<span data-ttu-id="cc965-127">Чтобы получить ссылку на ячейку **QuickStyleFillColor** по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="cc965-127">To get a reference to the **QuickStyleFillColor** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="cc965-128">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="cc965-128">Section index:</span></span>  <br/> |<span data-ttu-id="cc965-129">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="cc965-129">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="cc965-130">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="cc965-130">Row index:</span></span>  <br/> |<span data-ttu-id="cc965-131">**висровкуиккстилепропертиес**</span><span class="sxs-lookup"><span data-stu-id="cc965-131">**visRowQuickStyleProperties**</span></span> <br/> |
| <span data-ttu-id="cc965-132">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="cc965-132">Cell index:</span></span>  <br/> |<span data-ttu-id="cc965-133">**вискуиккстилефиллколор**</span><span class="sxs-lookup"><span data-stu-id="cc965-133">**visQuickStyleFillColor**</span></span> <br/> |
   

