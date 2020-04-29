---
title: QuickStyleLineColor Cell (Quick Style Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: dcfb792f-e02a-4059-acec-a178d221097c
description: Определяет цвет темы, используемый в линии фигуры, в виде целого числа от 0 до 7.
ms.openlocfilehash: 010b943f2266b1e0ee192e5f1341d73851d176fd
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33437045"
---
# <a name="quickstylelinecolor-cell-quick-style-section"></a><span data-ttu-id="695c2-103">QuickStyleLineColor Cell (Quick Style Section)</span><span class="sxs-lookup"><span data-stu-id="695c2-103">QuickStyleLineColor Cell (Quick Style Section)</span></span>

<span data-ttu-id="695c2-104">Определяет цвет темы, используемый в линии фигуры, в виде целого числа от 0 до 7.</span><span class="sxs-lookup"><span data-stu-id="695c2-104">Determines which theme color that a shape's line uses, as an integer from 0 to 7.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="695c2-105">Значение</span><span class="sxs-lookup"><span data-stu-id="695c2-105">Value</span></span>  <br/> |<span data-ttu-id="695c2-106">Описание</span><span class="sxs-lookup"><span data-stu-id="695c2-106">Description</span></span>  <br/> |
|<span data-ttu-id="695c2-107">нуль</span><span class="sxs-lookup"><span data-stu-id="695c2-107">0</span></span>  <br/> |<span data-ttu-id="695c2-108">Цвет линии фигуры наследуется от темного цвета темы.</span><span class="sxs-lookup"><span data-stu-id="695c2-108">The shape line color inherits from the Dark theme color.</span></span>  <br/> |
|<span data-ttu-id="695c2-109">1,1</span><span class="sxs-lookup"><span data-stu-id="695c2-109">1</span></span>  <br/> |<span data-ttu-id="695c2-110">Цвет линии фигуры наследуется от цвета светлой темы.</span><span class="sxs-lookup"><span data-stu-id="695c2-110">The shape line color inherits from the Light theme color.</span></span>  <br/> |
|<span data-ttu-id="695c2-111">2</span><span class="sxs-lookup"><span data-stu-id="695c2-111">2</span></span>  <br/> |<span data-ttu-id="695c2-112">Цвет линии фигуры наследуется от цвета темы "акцент 1"</span><span class="sxs-lookup"><span data-stu-id="695c2-112">The shape line color inherits from the Accent 1 theme color</span></span>  <br/> |
|<span data-ttu-id="695c2-113">4</span><span class="sxs-lookup"><span data-stu-id="695c2-113">3</span></span>  <br/> |<span data-ttu-id="695c2-114">Цвет линии фигуры наследуется от цвета темы "акцент 2"</span><span class="sxs-lookup"><span data-stu-id="695c2-114">The shape line color inherits from the Accent 2 theme color</span></span>  <br/> |
|<span data-ttu-id="695c2-115">4 </span><span class="sxs-lookup"><span data-stu-id="695c2-115">4</span></span>  <br/> |<span data-ttu-id="695c2-116">Цвет линии фигуры наследуется от цвета темы "акцент 3"</span><span class="sxs-lookup"><span data-stu-id="695c2-116">The shape line color inherits from the Accent 3 theme color</span></span>  <br/> |
|<span data-ttu-id="695c2-117">5 </span><span class="sxs-lookup"><span data-stu-id="695c2-117">5</span></span>  <br/> |<span data-ttu-id="695c2-118">Цвет линии фигуры наследуется от цвета темы "акцент 4"</span><span class="sxs-lookup"><span data-stu-id="695c2-118">The shape line color inherits from the Accent 4 theme color</span></span>  <br/> |
|<span data-ttu-id="695c2-119">6 </span><span class="sxs-lookup"><span data-stu-id="695c2-119">6</span></span>  <br/> |<span data-ttu-id="695c2-120">Цвет линии фигуры наследуется от цвета темы "акцент 5"</span><span class="sxs-lookup"><span data-stu-id="695c2-120">The shape line color inherits from the Accent 5 theme color</span></span>  <br/> |
|<span data-ttu-id="695c2-121">7 </span><span class="sxs-lookup"><span data-stu-id="695c2-121">7</span></span>  <br/> |<span data-ttu-id="695c2-122">Цвет линии фигуры наследуется от цвета темы "акцент 6"</span><span class="sxs-lookup"><span data-stu-id="695c2-122">The shape line color inherits from the Accent 6 theme color</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="695c2-123">Примечания</span><span class="sxs-lookup"><span data-stu-id="695c2-123">Remarks</span></span>

<span data-ttu-id="695c2-124">Чтобы получить ссылку на ячейку **QuickStyleLineColor** по имени из другой формулы, по значению атрибута **N** элемента **ячейки** или из программы с помощью свойства **CellsU** , используйте:</span><span class="sxs-lookup"><span data-stu-id="695c2-124">To get a reference to the **QuickStyleLineColor** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="695c2-125">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="695c2-125">Cell name:</span></span>  <br/> | <span data-ttu-id="695c2-126">QuickStyleLineColor</span><span class="sxs-lookup"><span data-stu-id="695c2-126">QuickStyleLineColor</span></span>  <br/> |
   
<span data-ttu-id="695c2-127">Чтобы получить ссылку на ячейку **QuickStyleLineColor** по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="695c2-127">To get a reference to the **QuickStyleLineColor** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="695c2-128">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="695c2-128">Section index:</span></span>  <br/> |<span data-ttu-id="695c2-129">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="695c2-129">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="695c2-130">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="695c2-130">Row index:</span></span>  <br/> |<span data-ttu-id="695c2-131">**висровкуиккстилепропертиес**</span><span class="sxs-lookup"><span data-stu-id="695c2-131">**visRowQuickStyleProperties**</span></span> <br/> |
| <span data-ttu-id="695c2-132">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="695c2-132">Cell index:</span></span>  <br/> |<span data-ttu-id="695c2-133">**вискуиккстилелинеколор**</span><span class="sxs-lookup"><span data-stu-id="695c2-133">**visQuickStyleLineColor**</span></span> <br/> |
   

