---
title: Ячейка GlueType (раздел "Сведения о приклеивании")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm420
localization_priority: Normal
ms.assetid: fffbefd6-8b0b-0023-6b03-026d1c6e885e
description: Определяет, используется ли одномерной фигуры static (точка-точка) или динамической связывающих (фигура к фигуре), когда он связан с другой фигурой.
ms.openlocfilehash: 162827521cda6fe4a37d17a8f7d36d7a36718519
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19813858"
---
# <a name="gluetype-cell-glue-info-section"></a><span data-ttu-id="3b7d8-103">Ячейка GlueType (раздел "Сведения о приклеивании")</span><span class="sxs-lookup"><span data-stu-id="3b7d8-103">GlueType Cell (Glue Info Section)</span></span>

<span data-ttu-id="3b7d8-104">Определяет, используется ли одномерной фигуры static (точка-точка) или динамической связывающих (фигура к фигуре), когда он связан с другой фигурой.</span><span class="sxs-lookup"><span data-stu-id="3b7d8-104">Determines whether a 1-D shape uses static (point-to-point) or dynamic (shape-to-shape) glue when it is glued to another shape.</span></span>
  
|<span data-ttu-id="3b7d8-105">**Значение**</span><span class="sxs-lookup"><span data-stu-id="3b7d8-105">**Value**</span></span>|<span data-ttu-id="3b7d8-106">**Описание**</span><span class="sxs-lookup"><span data-stu-id="3b7d8-106">**Description**</span></span>|<span data-ttu-id="3b7d8-107">**Константа автоматизации**</span><span class="sxs-lookup"><span data-stu-id="3b7d8-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
| <span data-ttu-id="3b7d8-108">&amp;H0</span><span class="sxs-lookup"><span data-stu-id="3b7d8-108">&amp;H0</span></span>  <br/> | <span data-ttu-id="3b7d8-109">Значение, используемое по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="3b7d8-109">Default.</span></span> <span data-ttu-id="3b7d8-110">Разрешить динамические связывающих для динамического соединителя. в противном случае используйте статические связывающих.</span><span class="sxs-lookup"><span data-stu-id="3b7d8-110">Allow dynamic glue for the dynamic connector only; otherwise, use static glue.</span></span>  <br/> |<span data-ttu-id="3b7d8-111">**visGlueTypeDefault**</span><span class="sxs-lookup"><span data-stu-id="3b7d8-111">**visGlueTypeDefault**</span></span> <br/> |
| <span data-ttu-id="3b7d8-112">&amp;H1</span><span class="sxs-lookup"><span data-stu-id="3b7d8-112">&amp;H1</span></span>  <br/> | <span data-ttu-id="3b7d8-113">Разрешить динамические связывающих.</span><span class="sxs-lookup"><span data-stu-id="3b7d8-113">Allow dynamic glue.</span></span>  <br/> | <span data-ttu-id="3b7d8-114">Устаревший атрибут в Visio 2002</span><span class="sxs-lookup"><span data-stu-id="3b7d8-114">Obsolete in Visio 2002</span></span>  <br/> |
| <span data-ttu-id="3b7d8-115">&amp;H2</span><span class="sxs-lookup"><span data-stu-id="3b7d8-115">&amp;H2</span></span>  <br/> | <span data-ttu-id="3b7d8-116">Разрешить динамические связывающих.</span><span class="sxs-lookup"><span data-stu-id="3b7d8-116">Allow dynamic glue.</span></span>  <br/> |<span data-ttu-id="3b7d8-117">**visGlueTypeWalking**</span><span class="sxs-lookup"><span data-stu-id="3b7d8-117">**visGlueTypeWalking**</span></span> <br/> |
| <span data-ttu-id="3b7d8-118">&amp;H4</span><span class="sxs-lookup"><span data-stu-id="3b7d8-118">&amp;H4</span></span>  <br/> | <span data-ttu-id="3b7d8-119">Не разрешать динамического связывающих.</span><span class="sxs-lookup"><span data-stu-id="3b7d8-119">Do not allow dynamic glue.</span></span>  <br/> |<span data-ttu-id="3b7d8-120">**visGlueTypeNoWalking**</span><span class="sxs-lookup"><span data-stu-id="3b7d8-120">**visGlueTypeNoWalking**</span></span> <br/> |
| <span data-ttu-id="3b7d8-121">&amp;H8</span><span class="sxs-lookup"><span data-stu-id="3b7d8-121">&amp;H8</span></span>  <br/> | <span data-ttu-id="3b7d8-122">Не разрешать в этом плоских фигур связаны с динамических связывающих.</span><span class="sxs-lookup"><span data-stu-id="3b7d8-122">Do not allow this 2-D shape to be connected to with dynamic glue.</span></span>  <br/> |<span data-ttu-id="3b7d8-123">**visGlueTypeNoWalkingTo**</span><span class="sxs-lookup"><span data-stu-id="3b7d8-123">**visGlueTypeNoWalkingTo**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="3b7d8-124">Замечания</span><span class="sxs-lookup"><span data-stu-id="3b7d8-124">Remarks</span></span>

<span data-ttu-id="3b7d8-125">Если эта ячейка содержит значение 1, 2 или 3, динамический связывающих будет установлено когда происходит одно из следующих:</span><span class="sxs-lookup"><span data-stu-id="3b7d8-125">If this cell contains a value of 1, 2 or 3, dynamic glue will be established when either of the following occurs:</span></span>
  
- <span data-ttu-id="3b7d8-126">Фигур динамически связан в пользовательском интерфейсе.</span><span class="sxs-lookup"><span data-stu-id="3b7d8-126">Shapes are dynamically glued in the user interface.</span></span>
    
- <span data-ttu-id="3b7d8-127">Фигуры являются привязку PinX или PinY ячейки другую фигуру из программы.</span><span class="sxs-lookup"><span data-stu-id="3b7d8-127">Shapes are glued to the PinX or PinY cell of another shape from a program.</span></span>
    
<span data-ttu-id="3b7d8-128">Если фигуры являются привязку ячейки фигуры, отличный от PinX или PinY из программы, статические связывающих используется.</span><span class="sxs-lookup"><span data-stu-id="3b7d8-128">If shapes are glued to shape cells other than PinX or PinY from a program, then static glue is used.</span></span>
  
<span data-ttu-id="3b7d8-129">При изменении данного значения из разрешение не позволяет динамической связывающих не сервера или изменение существующей динамической связывающих.</span><span class="sxs-lookup"><span data-stu-id="3b7d8-129">Changing this value from allowing to not allowing dynamic glue does not sever or change existing dynamic glue.</span></span> <span data-ttu-id="3b7d8-130">Программы можно установить динамических связывающих, даже если динамических связывающих отключена в ячейке приклеивания.</span><span class="sxs-lookup"><span data-stu-id="3b7d8-130">Programs can establish dynamic glue even if dynamic glue is disabled in the GlueType cell.</span></span>
  
<span data-ttu-id="3b7d8-131">Для получения ссылки на ячейки приклеивания по имени, из другой формулы, и программы, с помощью свойства **CellsU** , используйте следующую команду:</span><span class="sxs-lookup"><span data-stu-id="3b7d8-131">To get a reference to the GlueType cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="3b7d8-132">Имя ячейки.</span><span class="sxs-lookup"><span data-stu-id="3b7d8-132">Cell name:</span></span>  <br/> | <span data-ttu-id="3b7d8-133">Приклеивания</span><span class="sxs-lookup"><span data-stu-id="3b7d8-133">GlueType</span></span>  <br/> |
   
<span data-ttu-id="3b7d8-134">Для получения ссылки на ячейки приклеивания по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы:</span><span class="sxs-lookup"><span data-stu-id="3b7d8-134">To get a reference to the GlueType cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="3b7d8-135">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="3b7d8-135">Section index:</span></span>  <br/> |<span data-ttu-id="3b7d8-136">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="3b7d8-136">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="3b7d8-137">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="3b7d8-137">Row index:</span></span>  <br/> |<span data-ttu-id="3b7d8-138">**visRowMisc**</span><span class="sxs-lookup"><span data-stu-id="3b7d8-138">**visRowMisc**</span></span> <br/> |
| <span data-ttu-id="3b7d8-139">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="3b7d8-139">Cell index:</span></span>  <br/> |<span data-ttu-id="3b7d8-140">**visGlueType**</span><span class="sxs-lookup"><span data-stu-id="3b7d8-140">**visGlueType**</span></span> <br/> |
   

