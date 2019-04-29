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
# <a name="quickstylefillcolor-cell-quick-style-section"></a><span data-ttu-id="314ac-103">QuickStyleFillColor Cell (Quick Style Section)</span><span class="sxs-lookup"><span data-stu-id="314ac-103">QuickStyleFillColor Cell (Quick Style Section)</span></span>

<span data-ttu-id="314ac-104">Определяет, какой цвет темы использует Заливка фигуры, в виде целого числа от 0 до 7.</span><span class="sxs-lookup"><span data-stu-id="314ac-104">Determines which theme color that a shape's fill uses, as an integer from 0 to 7</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="314ac-105">Значение</span><span class="sxs-lookup"><span data-stu-id="314ac-105">Value</span></span>  <br/> |<span data-ttu-id="314ac-106">Описание</span><span class="sxs-lookup"><span data-stu-id="314ac-106">Description</span></span>  <br/> |
|<span data-ttu-id="314ac-107">нуль</span><span class="sxs-lookup"><span data-stu-id="314ac-107">0</span></span>  <br/> |<span data-ttu-id="314ac-108">Цвет заливки фигур наследуется от цвета темной темы.</span><span class="sxs-lookup"><span data-stu-id="314ac-108">The shape fill color inherits from the Dark theme color.</span></span>  <br/> |
|<span data-ttu-id="314ac-109">1,1</span><span class="sxs-lookup"><span data-stu-id="314ac-109">1</span></span>  <br/> |<span data-ttu-id="314ac-110">Цвет заливки фигур наследуется от цвета светлой темы.</span><span class="sxs-lookup"><span data-stu-id="314ac-110">The shape fill color inherits from the Light theme color.</span></span>  <br/> |
|<span data-ttu-id="314ac-111">2</span><span class="sxs-lookup"><span data-stu-id="314ac-111">2</span></span>  <br/> |<span data-ttu-id="314ac-112">Цвет заливки фигуры наследуется от цвета темы "акцент 1"</span><span class="sxs-lookup"><span data-stu-id="314ac-112">The shape fill color inherits from the Accent 1 theme color</span></span>  <br/> |
|<span data-ttu-id="314ac-113">4</span><span class="sxs-lookup"><span data-stu-id="314ac-113">3</span></span>  <br/> |<span data-ttu-id="314ac-114">Цвет заливки фигуры наследуется от цвета темы "акцент 2"</span><span class="sxs-lookup"><span data-stu-id="314ac-114">The shape fill color inherits from the Accent 2 theme color</span></span>  <br/> |
|<span data-ttu-id="314ac-115">SP4</span><span class="sxs-lookup"><span data-stu-id="314ac-115">4</span></span>  <br/> |<span data-ttu-id="314ac-116">Цвет заливки фигуры наследуется от цвета темы "акцент 3"</span><span class="sxs-lookup"><span data-stu-id="314ac-116">The shape fill color inherits from the Accent 3 theme color</span></span>  <br/> |
|<span data-ttu-id="314ac-117">17:00</span><span class="sxs-lookup"><span data-stu-id="314ac-117">5</span></span>  <br/> |<span data-ttu-id="314ac-118">Цвет заливки фигуры наследуется от цвета темы "акцент 4"</span><span class="sxs-lookup"><span data-stu-id="314ac-118">The shape fill color inherits from the Accent 4 theme color</span></span>  <br/> |
|<span data-ttu-id="314ac-119">ICMPv6</span><span class="sxs-lookup"><span data-stu-id="314ac-119">6</span></span>  <br/> |<span data-ttu-id="314ac-120">Цвет заливки фигуры наследуется от цвета темы "акцент 5"</span><span class="sxs-lookup"><span data-stu-id="314ac-120">The shape fill color inherits from the Accent 5 theme color</span></span>  <br/> |
|<span data-ttu-id="314ac-121">см</span><span class="sxs-lookup"><span data-stu-id="314ac-121">7</span></span>  <br/> |<span data-ttu-id="314ac-122">Цвет заливки фигуры наследуется от цвета темы "акцент 6"</span><span class="sxs-lookup"><span data-stu-id="314ac-122">The shape fill color inherits from the Accent 6 theme color</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="314ac-123">Примечания</span><span class="sxs-lookup"><span data-stu-id="314ac-123">Remarks</span></span>

<span data-ttu-id="314ac-124">Чтобы получить ссылку на ячейку **QuickStyleFillColor** по имени из другой формулы, по значению атрибута **N** элемента **ячейки** или из программы с помощью свойства **CellsU** , используйте:</span><span class="sxs-lookup"><span data-stu-id="314ac-124">To get a reference to the **QuickStyleFillColor** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="314ac-125">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="314ac-125">Cell name:</span></span>  <br/> | <span data-ttu-id="314ac-126">QuickStyleFillColor</span><span class="sxs-lookup"><span data-stu-id="314ac-126">QuickStyleFillColor</span></span>  <br/> |
   
<span data-ttu-id="314ac-127">Чтобы получить ссылку на ячейку **QuickStyleFillColor** по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="314ac-127">To get a reference to the **QuickStyleFillColor** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="314ac-128">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="314ac-128">Section index:</span></span>  <br/> |<span data-ttu-id="314ac-129">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="314ac-129">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="314ac-130">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="314ac-130">Row index:</span></span>  <br/> |<span data-ttu-id="314ac-131">**Висровкуиккстилепропертиес**</span><span class="sxs-lookup"><span data-stu-id="314ac-131">**visRowQuickStyleProperties**</span></span> <br/> |
| <span data-ttu-id="314ac-132">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="314ac-132">Cell index:</span></span>  <br/> |<span data-ttu-id="314ac-133">**Вискуиккстилефиллколор**</span><span class="sxs-lookup"><span data-stu-id="314ac-133">**visQuickStyleFillColor**</span></span> <br/> |
   

