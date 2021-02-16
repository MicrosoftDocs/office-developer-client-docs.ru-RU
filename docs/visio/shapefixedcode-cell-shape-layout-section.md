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
description: Определяет поведение размещения для размещения фигуры.
ms.openlocfilehash: eae44a0579129fbe8da1c0cc8c37318beb024563
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33431745"
---
# <a name="shapefixedcode-cell-shape-layout-section"></a><span data-ttu-id="3c8e4-103">ShapeFixedCode Cell (Shape Layout Section)</span><span class="sxs-lookup"><span data-stu-id="3c8e4-103">ShapeFixedCode Cell (Shape Layout Section)</span></span>

<span data-ttu-id="3c8e4-104">Определяет поведение размещения для размещения фигуры.</span><span class="sxs-lookup"><span data-stu-id="3c8e4-104">Specifies placement behavior for a placeable shape.</span></span>
  
|<span data-ttu-id="3c8e4-105">**Значение**</span><span class="sxs-lookup"><span data-stu-id="3c8e4-105">**Value**</span></span>|<span data-ttu-id="3c8e4-106">**Режим выделения**</span><span class="sxs-lookup"><span data-stu-id="3c8e4-106">**Selection mode**</span></span>|<span data-ttu-id="3c8e4-107">**Константа автоматизации**</span><span class="sxs-lookup"><span data-stu-id="3c8e4-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="3c8e4-108">&amp;H1</span><span class="sxs-lookup"><span data-stu-id="3c8e4-108">&amp;H1</span></span>  <br/> |<span data-ttu-id="3c8e4-109">Не перемещайте эту фигуру, если фигуры выложены с помощью диалоговых окна "Настройка  макета".</span><span class="sxs-lookup"><span data-stu-id="3c8e4-109">Don't move this shape when shapes are laid out by using the **Configure Layout** dialog box.</span></span>  <br/> |<span data-ttu-id="3c8e4-110">**visSLOFixedPlacement**</span><span class="sxs-lookup"><span data-stu-id="3c8e4-110">**visSLOFixedPlacement**</span></span> <br/> |
|<span data-ttu-id="3c8e4-111">&amp;H2</span><span class="sxs-lookup"><span data-stu-id="3c8e4-111">&amp;H2</span></span>  <br/> |<span data-ttu-id="3c8e4-112">Не перемещайте эту фигуру и не разрешать размещать на ней фигуры, которые помещаются поверх него.</span><span class="sxs-lookup"><span data-stu-id="3c8e4-112">Don't move this shape and do not allow shapes that plow to be placed on top of it.</span></span>  <br/> |<span data-ttu-id="3c8e4-113">**visSLOFixedPlow**</span><span class="sxs-lookup"><span data-stu-id="3c8e4-113">**visSLOFixedPlow**</span></span> <br/> |
|<span data-ttu-id="3c8e4-114">&amp;H4</span><span class="sxs-lookup"><span data-stu-id="3c8e4-114">&amp;H4</span></span>  <br/> |<span data-ttu-id="3c8e4-115">Не перемещайте эту фигуру и не разрешать помещать поверх нее фигуры, которые помещаются на plow.</span><span class="sxs-lookup"><span data-stu-id="3c8e4-115">Don't move this shape and allow shapes that plow to be placed on top of it.</span></span>  <br/> |<span data-ttu-id="3c8e4-116">**visSLOFixedPermeablePlow**</span><span class="sxs-lookup"><span data-stu-id="3c8e4-116">**visSLOFixedPermeablePlow**</span></span> <br/> |
|<span data-ttu-id="3c8e4-117">&amp;H20 (32)</span><span class="sxs-lookup"><span data-stu-id="3c8e4-117">&amp;H20 (32)</span></span>  <br/> |<span data-ttu-id="3c8e4-118">Игнорировать расположения точек подключения при маршруте.</span><span class="sxs-lookup"><span data-stu-id="3c8e4-118">Ignore connection point locations when being routed to.</span></span>  <br/> |<span data-ttu-id="3c8e4-119">**visSLOFixedConnPtsIgnore**</span><span class="sxs-lookup"><span data-stu-id="3c8e4-119">**visSLOFixedConnPtsIgnore**</span></span> <br/> |
|<span data-ttu-id="3c8e4-120">&amp;H40 (64)</span><span class="sxs-lookup"><span data-stu-id="3c8e4-120">&amp;H40 (64)</span></span>  <br/> |<span data-ttu-id="3c8e4-121">Разрешить только маршрутику на стороны с точками подключения.</span><span class="sxs-lookup"><span data-stu-id="3c8e4-121">Only allow routing to sides with connection points.</span></span>  <br/> |<span data-ttu-id="3c8e4-122">**visSLOFixedConnPtsOnly**</span><span class="sxs-lookup"><span data-stu-id="3c8e4-122">**visSLOFixedConnPtsOnly**</span></span> <br/> |
|<span data-ttu-id="3c8e4-123">&amp;H80 (128)</span><span class="sxs-lookup"><span data-stu-id="3c8e4-123">&amp;H80 (128)</span></span>  <br/> |<span data-ttu-id="3c8e4-124">Не привяжйтесь к периметру этой фигуры.</span><span class="sxs-lookup"><span data-stu-id="3c8e4-124">Don't glue to the perimeter of this shape.</span></span> <span data-ttu-id="3c8e4-125">Вместо этого привяжйте к поле выравнивания фигуры.</span><span class="sxs-lookup"><span data-stu-id="3c8e4-125">Glue to the shape's alignment box instead.</span></span>  <br/> |<span data-ttu-id="3c8e4-126">**visSLOFixedNoFoldToShape**</span><span class="sxs-lookup"><span data-stu-id="3c8e4-126">**visSLOFixedNoFoldToShape**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="3c8e4-127">Примечания</span><span class="sxs-lookup"><span data-stu-id="3c8e4-127">Remarks</span></span>

<span data-ttu-id="3c8e4-128">Вы также можете установить значение этой  ячейки  на вкладке "Размещение" в диалоговом окне  "Поведение" (с выбранной фигурой, на вкладке "Разработчик", в группе "Проектирование фигуры" щелкните "Поведение" и выберите вкладку **"Размещение").** [](run-in-developer-mode-display-the-developer-tab.md)</span><span class="sxs-lookup"><span data-stu-id="3c8e4-128">You can also set the value of this cell on the **Placement** tab in the **Behavior** dialog box (with a shape selected, on the [Developer](run-in-developer-mode-display-the-developer-tab.md) tab, in the **Shape Design** group, click **Behavior**, and then click the **Placement** tab).</span></span> 
  
<span data-ttu-id="3c8e4-129">Для этой ячейки можно настроить любое сочетание этих значений.</span><span class="sxs-lookup"><span data-stu-id="3c8e4-129">You can set any combination of these values for this cell.</span></span> <span data-ttu-id="3c8e4-130">Например, можно ввести значение 3 ( H3), которое исключает перемещение при размещении фигур с помощью диалоговых окна "Настройка макета" (на вкладке "Конструктор" в группе "Макет" щелкните "Страница повторного макета" и нажмите кнопку "Дополнительные параметры макета"), а также когда другие помещаемые фигуры размещаются на фигуре или рядом с &amp; фигурой.     </span><span class="sxs-lookup"><span data-stu-id="3c8e4-130">For example, you can enter the value 3 (&amp;H3), which eliminates movement when you lay out shapes by using the **Configure Layout** dialog box (on the **Design** tab, in the **Layout** group, click **Re-Layout Page**, and then click **More Layout Options** ) and when other placeable shapes are placed on or near the shape.</span></span> 
  
<span data-ttu-id="3c8e4-131">В версиях, более ранних, чем Visio 2000, такое поведение задано с помощью ячейки ObjInteract в разделе "Прочие".</span><span class="sxs-lookup"><span data-stu-id="3c8e4-131">In versions earlier than Visio 2000, you set this behavior using the ObjInteract cell in the Miscellaneous section.</span></span> 
  
<span data-ttu-id="3c8e4-132">Чтобы получить ссылку на ячейку ShapeFixedCode по имени из другой формулы или из программы с помощью свойства **CellsU,** используйте:</span><span class="sxs-lookup"><span data-stu-id="3c8e4-132">To get a reference to the ShapeFixedCode cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="3c8e4-133">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="3c8e4-133">Cell name:</span></span>  <br/> |<span data-ttu-id="3c8e4-134">ShapeFixedCode</span><span class="sxs-lookup"><span data-stu-id="3c8e4-134">ShapeFixedCode</span></span>  <br/> |
   
<span data-ttu-id="3c8e4-135">Чтобы получить ссылку на ячейку ShapeFixedCode по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="3c8e4-135">To get a reference to the ShapeFixedCode cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="3c8e4-136">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="3c8e4-136">Section index:</span></span>  <br/> |<span data-ttu-id="3c8e4-137">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="3c8e4-137">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="3c8e4-138">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="3c8e4-138">Row index:</span></span>  <br/> |<span data-ttu-id="3c8e4-139">**visRowShapeLayout**</span><span class="sxs-lookup"><span data-stu-id="3c8e4-139">**visRowShapeLayout**</span></span> <br/> |
|<span data-ttu-id="3c8e4-140">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="3c8e4-140">Cell index:</span></span>  <br/> |<span data-ttu-id="3c8e4-141">**visSLOFixedCode**</span><span class="sxs-lookup"><span data-stu-id="3c8e4-141">**visSLOFixedCode**</span></span> <br/> |
   

