---
title: Ячейка ShapeFixedCode (раздел "Макет фигуры")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm880
localization_priority: Normal
ms.assetid: a1736a5c-421c-2bdb-b164-76a8cd06cc3d
description: Указывает поведение размещаемой фигуры.
ms.openlocfilehash: 6ae83fa70cc545c88080ce27046bd8c226c060e3
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19814763"
---
# <a name="shapefixedcode-cell-shape-layout-section"></a><span data-ttu-id="05fee-103">Ячейка ShapeFixedCode (раздел "Макет фигуры")</span><span class="sxs-lookup"><span data-stu-id="05fee-103">ShapeFixedCode Cell (Shape Layout Section)</span></span>

<span data-ttu-id="05fee-104">Указывает поведение размещаемой фигуры.</span><span class="sxs-lookup"><span data-stu-id="05fee-104">Specifies placement behavior for a placeable shape.</span></span>
  
|<span data-ttu-id="05fee-105">**Значение**</span><span class="sxs-lookup"><span data-stu-id="05fee-105">**Value**</span></span>|<span data-ttu-id="05fee-106">**Выбор режима**</span><span class="sxs-lookup"><span data-stu-id="05fee-106">**Selection mode**</span></span>|<span data-ttu-id="05fee-107">**Константа автоматизации**</span><span class="sxs-lookup"><span data-stu-id="05fee-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="05fee-108">&amp;H1</span><span class="sxs-lookup"><span data-stu-id="05fee-108">&amp;H1</span></span>  <br/> |<span data-ttu-id="05fee-109">Не перемещать этой фигуры, когда расположения фигур с помощью диалогового окна " **Настройка макета** ".</span><span class="sxs-lookup"><span data-stu-id="05fee-109">Don't move this shape when shapes are laid out by using the **Configure Layout** dialog box.</span></span>  <br/> |<span data-ttu-id="05fee-110">**visSLOFixedPlacement**</span><span class="sxs-lookup"><span data-stu-id="05fee-110">**visSLOFixedPlacement**</span></span> <br/> |
|<span data-ttu-id="05fee-111">&amp;H2</span><span class="sxs-lookup"><span data-stu-id="05fee-111">&amp;H2</span></span>  <br/> |<span data-ttu-id="05fee-112">Не перемещать этой фигуры и не разрешать фигуры, которые сдвигать должна размещаться на его основе.</span><span class="sxs-lookup"><span data-stu-id="05fee-112">Don't move this shape and do not allow shapes that plow to be placed on top of it.</span></span>  <br/> |<span data-ttu-id="05fee-113">**visSLOFixedPlow**</span><span class="sxs-lookup"><span data-stu-id="05fee-113">**visSLOFixedPlow**</span></span> <br/> |
|<span data-ttu-id="05fee-114">&amp;H4</span><span class="sxs-lookup"><span data-stu-id="05fee-114">&amp;H4</span></span>  <br/> |<span data-ttu-id="05fee-115">Не переместить фигуру и разрешить фигуры, которые сдвигать должна размещаться на его основе.</span><span class="sxs-lookup"><span data-stu-id="05fee-115">Don't move this shape and allow shapes that plow to be placed on top of it.</span></span>  <br/> |<span data-ttu-id="05fee-116">**visSLOFixedPermeablePlow**</span><span class="sxs-lookup"><span data-stu-id="05fee-116">**visSLOFixedPermeablePlow**</span></span> <br/> |
|<span data-ttu-id="05fee-117">&amp;H20 (32)</span><span class="sxs-lookup"><span data-stu-id="05fee-117">&amp;H20 (32)</span></span>  <br/> |<span data-ttu-id="05fee-118">Когда поступает в игнорировать местоположения точек подключения.</span><span class="sxs-lookup"><span data-stu-id="05fee-118">Ignore connection point locations when being routed to.</span></span>  <br/> |<span data-ttu-id="05fee-119">**visSLOFixedConnPtsIgnore**</span><span class="sxs-lookup"><span data-stu-id="05fee-119">**visSLOFixedConnPtsIgnore**</span></span> <br/> |
|<span data-ttu-id="05fee-120">&amp;H40 (64)</span><span class="sxs-lookup"><span data-stu-id="05fee-120">&amp;H40 (64)</span></span>  <br/> |<span data-ttu-id="05fee-121">Разрешать только маршрутизации и точек подключения.</span><span class="sxs-lookup"><span data-stu-id="05fee-121">Only allow routing to sides with connection points.</span></span>  <br/> |<span data-ttu-id="05fee-122">**visSLOFixedConnPtsOnly**</span><span class="sxs-lookup"><span data-stu-id="05fee-122">**visSLOFixedConnPtsOnly**</span></span> <br/> |
|<span data-ttu-id="05fee-123">&amp;H80 (128)</span><span class="sxs-lookup"><span data-stu-id="05fee-123">&amp;H80 (128)</span></span>  <br/> |<span data-ttu-id="05fee-124">Не связывания для периметра этой фигуры.</span><span class="sxs-lookup"><span data-stu-id="05fee-124">Don't glue to the perimeter of this shape.</span></span> <span data-ttu-id="05fee-125">Вместо этого связывания фигуры выравнивание.</span><span class="sxs-lookup"><span data-stu-id="05fee-125">Glue to the shape's alignment box instead.</span></span>  <br/> |<span data-ttu-id="05fee-126">**visSLOFixedNoFoldToShape**</span><span class="sxs-lookup"><span data-stu-id="05fee-126">**visSLOFixedNoFoldToShape**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="05fee-127">Замечания</span><span class="sxs-lookup"><span data-stu-id="05fee-127">Remarks</span></span>

<span data-ttu-id="05fee-128">Значение ячейки также можно настроить на вкладке **Размещение** в диалоговом окне **поведение** (с фигуры, выбранные на вкладке [Разработчик](run-in-developer-mode-display-the-developer-tab.md) в группе **Создать фигуру** нажмите кнопку **поведение**и затем перейдите на вкладку **Размещение** ).</span><span class="sxs-lookup"><span data-stu-id="05fee-128">You can also set the value of this cell on the **Placement** tab in the **Behavior** dialog box (with a shape selected, on the [Developer](run-in-developer-mode-display-the-developer-tab.md) tab, in the **Shape Design** group, click **Behavior**, and then click the **Placement** tab).</span></span> 
  
<span data-ttu-id="05fee-129">Можно задать любое сочетание следующих значений для этой ячейки.</span><span class="sxs-lookup"><span data-stu-id="05fee-129">You can set any combination of these values for this cell.</span></span> <span data-ttu-id="05fee-130">Например, можно ввести значение 3 (&amp;H3), которая позволяет устранить перемещения при расположении фигур с помощью диалогового окна " **Настройка макета** " (на вкладке **Конструктор** в группе **Макет** выберите пункт **Изменить расположение**и нажмите кнопку ** Дополнительные параметры макета** ) и помещения других размещаемые фигуры на или близок к фигуре.</span><span class="sxs-lookup"><span data-stu-id="05fee-130">For example, you can enter the value 3 (&amp;H3), which eliminates movement when you lay out shapes by using the **Configure Layout** dialog box (on the **Design** tab, in the **Layout** group, click **Re-Layout Page**, and then click **More Layout Options** ) and when other placeable shapes are placed on or near the shape.</span></span> 
  
<span data-ttu-id="05fee-131">Более ранних чем Visio 2000 в версиях задайте это поведение, с помощью ObjInteract ячеек в разделе Разное.</span><span class="sxs-lookup"><span data-stu-id="05fee-131">In versions earlier than Visio 2000, you set this behavior using the ObjInteract cell in the Miscellaneous section.</span></span> 
  
<span data-ttu-id="05fee-132">Чтобы получить ссылку на ячейку ShapeFixedCode по имени из другой формулы или из файла с помощью свойства **CellsU** , используйте:</span><span class="sxs-lookup"><span data-stu-id="05fee-132">To get a reference to the ShapeFixedCode cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="05fee-133">Имя ячейки.</span><span class="sxs-lookup"><span data-stu-id="05fee-133">Cell name:</span></span>  <br/> |<span data-ttu-id="05fee-134">ShapeFixedCode</span><span class="sxs-lookup"><span data-stu-id="05fee-134">ShapeFixedCode</span></span>  <br/> |
   
<span data-ttu-id="05fee-135">Для получения ссылки на ячейки ShapeFixedCode по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы:</span><span class="sxs-lookup"><span data-stu-id="05fee-135">To get a reference to the ShapeFixedCode cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="05fee-136">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="05fee-136">Section index:</span></span>  <br/> |<span data-ttu-id="05fee-137">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="05fee-137">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="05fee-138">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="05fee-138">Row index:</span></span>  <br/> |<span data-ttu-id="05fee-139">**visRowShapeLayout**</span><span class="sxs-lookup"><span data-stu-id="05fee-139">**visRowShapeLayout**</span></span> <br/> |
|<span data-ttu-id="05fee-140">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="05fee-140">Cell index:</span></span>  <br/> |<span data-ttu-id="05fee-141">**visSLOFixedCode**</span><span class="sxs-lookup"><span data-stu-id="05fee-141">**visSLOFixedCode**</span></span> <br/> |
   

