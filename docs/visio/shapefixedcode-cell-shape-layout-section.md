---
title: ShapeFixedCode Cell (Shape Layout Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm880
localization_priority: Normal
ms.assetid: a1736a5c-421c-2bdb-b164-76a8cd06cc3d
description: Указывает поведение размещения для размещения фигуры.
ms.openlocfilehash: eae44a0579129fbe8da1c0cc8c37318beb024563
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33431745"
---
# <a name="shapefixedcode-cell-shape-layout-section"></a><span data-ttu-id="72f09-103">ShapeFixedCode Cell (Shape Layout Section)</span><span class="sxs-lookup"><span data-stu-id="72f09-103">ShapeFixedCode Cell (Shape Layout Section)</span></span>

<span data-ttu-id="72f09-104">Указывает поведение размещения для размещения фигуры.</span><span class="sxs-lookup"><span data-stu-id="72f09-104">Specifies placement behavior for a placeable shape.</span></span>
  
|<span data-ttu-id="72f09-105">**Значение**</span><span class="sxs-lookup"><span data-stu-id="72f09-105">**Value**</span></span>|<span data-ttu-id="72f09-106">**Режим выбора**</span><span class="sxs-lookup"><span data-stu-id="72f09-106">**Selection mode**</span></span>|<span data-ttu-id="72f09-107">**Константа автоматизации**</span><span class="sxs-lookup"><span data-stu-id="72f09-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="72f09-108">&amp;H1</span><span class="sxs-lookup"><span data-stu-id="72f09-108">&amp;H1</span></span>  <br/> |<span data-ttu-id="72f09-109">Не перемещайте эту фигуру, когда фигуры выложены с помощью диалогового окна **Configure Layout.**</span><span class="sxs-lookup"><span data-stu-id="72f09-109">Don't move this shape when shapes are laid out by using the **Configure Layout** dialog box.</span></span>  <br/> |<span data-ttu-id="72f09-110">**visSLOFixedPlacement**</span><span class="sxs-lookup"><span data-stu-id="72f09-110">**visSLOFixedPlacement**</span></span> <br/> |
|<span data-ttu-id="72f09-111">&amp;H2</span><span class="sxs-lookup"><span data-stu-id="72f09-111">&amp;H2</span></span>  <br/> |<span data-ttu-id="72f09-112">Не двигайте эту фигуру и не позволяйте фигурам, которые вспахить, помещать поверх нее.</span><span class="sxs-lookup"><span data-stu-id="72f09-112">Don't move this shape and do not allow shapes that plow to be placed on top of it.</span></span>  <br/> |<span data-ttu-id="72f09-113">**visSLOFixedPlow**</span><span class="sxs-lookup"><span data-stu-id="72f09-113">**visSLOFixedPlow**</span></span> <br/> |
|<span data-ttu-id="72f09-114">&amp;H4</span><span class="sxs-lookup"><span data-stu-id="72f09-114">&amp;H4</span></span>  <br/> |<span data-ttu-id="72f09-115">Не перемещайте эту фигуру и не позволяйте фигурам, которые вспахить, помещать поверх нее.</span><span class="sxs-lookup"><span data-stu-id="72f09-115">Don't move this shape and allow shapes that plow to be placed on top of it.</span></span>  <br/> |<span data-ttu-id="72f09-116">**visSLOFixedPermeablePlow**</span><span class="sxs-lookup"><span data-stu-id="72f09-116">**visSLOFixedPermeablePlow**</span></span> <br/> |
|<span data-ttu-id="72f09-117">&amp;H20 (32)</span><span class="sxs-lookup"><span data-stu-id="72f09-117">&amp;H20 (32)</span></span>  <br/> |<span data-ttu-id="72f09-118">Игнорируйте расположения точек подключения при маршруте.</span><span class="sxs-lookup"><span data-stu-id="72f09-118">Ignore connection point locations when being routed to.</span></span>  <br/> |<span data-ttu-id="72f09-119">**visSLOFixedConnPtsIgnore**</span><span class="sxs-lookup"><span data-stu-id="72f09-119">**visSLOFixedConnPtsIgnore**</span></span> <br/> |
|<span data-ttu-id="72f09-120">&amp;H40 (64)</span><span class="sxs-lookup"><span data-stu-id="72f09-120">&amp;H40 (64)</span></span>  <br/> |<span data-ttu-id="72f09-121">Только разрешить маршрутику в стороны с точками подключения.</span><span class="sxs-lookup"><span data-stu-id="72f09-121">Only allow routing to sides with connection points.</span></span>  <br/> |<span data-ttu-id="72f09-122">**visSLOFixedConnPtsOnly**</span><span class="sxs-lookup"><span data-stu-id="72f09-122">**visSLOFixedConnPtsOnly**</span></span> <br/> |
|<span data-ttu-id="72f09-123">&amp;H80 (128)</span><span class="sxs-lookup"><span data-stu-id="72f09-123">&amp;H80 (128)</span></span>  <br/> |<span data-ttu-id="72f09-124">Не приклеить к периметру этой фигуры.</span><span class="sxs-lookup"><span data-stu-id="72f09-124">Don't glue to the perimeter of this shape.</span></span> <span data-ttu-id="72f09-125">Вместо этого приклейте к окне выравнивания фигуры.</span><span class="sxs-lookup"><span data-stu-id="72f09-125">Glue to the shape's alignment box instead.</span></span>  <br/> |<span data-ttu-id="72f09-126">**visSLOFixedNoFoldToShape**</span><span class="sxs-lookup"><span data-stu-id="72f09-126">**visSLOFixedNoFoldToShape**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="72f09-127">Примечания</span><span class="sxs-lookup"><span data-stu-id="72f09-127">Remarks</span></span>

<span data-ttu-id="72f09-128">Вы также можете установить значение этой  ячейки  на вкладке Размещение в диалоговом [](run-in-developer-mode-display-the-developer-tab.md) окне Поведение (с выбранной фигурой на вкладке Разработчик, в группе **Shape Design** нажмите кнопку **Поведение,** а затем щелкните вкладку **Размещение).**</span><span class="sxs-lookup"><span data-stu-id="72f09-128">You can also set the value of this cell on the **Placement** tab in the **Behavior** dialog box (with a shape selected, on the [Developer](run-in-developer-mode-display-the-developer-tab.md) tab, in the **Shape Design** group, click **Behavior**, and then click the **Placement** tab).</span></span> 
  
<span data-ttu-id="72f09-129">Вы можете установить любое сочетание этих значений для этой ячейки.</span><span class="sxs-lookup"><span data-stu-id="72f09-129">You can set any combination of these values for this cell.</span></span> <span data-ttu-id="72f09-130">Например, можно ввести значение 3 (H3), которое исключает движение при выкладке фигур с помощью диалогового окна Configure Layout (на вкладке Design, в группе Макет, щелкните страницу повторной макета, а затем нажмите кнопку Дополнительные параметры макета) и при размещении других фигур на или вблизи &amp; фигуры.     </span><span class="sxs-lookup"><span data-stu-id="72f09-130">For example, you can enter the value 3 (&amp;H3), which eliminates movement when you lay out shapes by using the **Configure Layout** dialog box (on the **Design** tab, in the **Layout** group, click **Re-Layout Page**, and then click **More Layout Options** ) and when other placeable shapes are placed on or near the shape.</span></span> 
  
<span data-ttu-id="72f09-131">В версиях до Visio 2000 года такое поведение устанавливается с помощью ячейки ObjInteract в разделе Разное.</span><span class="sxs-lookup"><span data-stu-id="72f09-131">In versions earlier than Visio 2000, you set this behavior using the ObjInteract cell in the Miscellaneous section.</span></span> 
  
<span data-ttu-id="72f09-132">Чтобы получить ссылку на ячейку ShapeFixedCode по имени из другой формулы или из программы с помощью свойства **CellsU,** используйте:</span><span class="sxs-lookup"><span data-stu-id="72f09-132">To get a reference to the ShapeFixedCode cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="72f09-133">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="72f09-133">Cell name:</span></span>  <br/> |<span data-ttu-id="72f09-134">ShapeFixedCode</span><span class="sxs-lookup"><span data-stu-id="72f09-134">ShapeFixedCode</span></span>  <br/> |
   
<span data-ttu-id="72f09-135">Чтобы получить ссылку на ячейку ShapeFixedCode по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="72f09-135">To get a reference to the ShapeFixedCode cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="72f09-136">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="72f09-136">Section index:</span></span>  <br/> |<span data-ttu-id="72f09-137">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="72f09-137">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="72f09-138">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="72f09-138">Row index:</span></span>  <br/> |<span data-ttu-id="72f09-139">**visRowShapeLayout**</span><span class="sxs-lookup"><span data-stu-id="72f09-139">**visRowShapeLayout**</span></span> <br/> |
|<span data-ttu-id="72f09-140">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="72f09-140">Cell index:</span></span>  <br/> |<span data-ttu-id="72f09-141">**visSLOFixedCode**</span><span class="sxs-lookup"><span data-stu-id="72f09-141">**visSLOFixedCode**</span></span> <br/> |
   

