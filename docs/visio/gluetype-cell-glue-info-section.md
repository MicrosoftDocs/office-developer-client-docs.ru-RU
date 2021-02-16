---
title: GlueType Cell (Glue Info Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm420
localization_priority: Normal
ms.assetid: fffbefd6-8b0b-0023-6b03-026d1c6e885e
description: Определяет, использует ли однообразная фигура статический (точка-точка) или динамический (от фигуры к фигуре) при наклеии к другой фигуре.
ms.openlocfilehash: ae4eddf17c6e7b5e56cb3397f03d0721d965c9b7
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33410674"
---
# <a name="gluetype-cell-glue-info-section"></a><span data-ttu-id="a2b39-103">GlueType Cell (Glue Info Section)</span><span class="sxs-lookup"><span data-stu-id="a2b39-103">GlueType Cell (Glue Info Section)</span></span>

<span data-ttu-id="a2b39-104">Определяет, использует ли однообразная фигура статический (точка-точка) или динамический (от фигуры к фигуре) при наклеии к другой фигуре.</span><span class="sxs-lookup"><span data-stu-id="a2b39-104">Determines whether a 1-D shape uses static (point-to-point) or dynamic (shape-to-shape) glue when it is glued to another shape.</span></span>
  
|<span data-ttu-id="a2b39-105">**Значение**</span><span class="sxs-lookup"><span data-stu-id="a2b39-105">**Value**</span></span>|<span data-ttu-id="a2b39-106">**Описание**</span><span class="sxs-lookup"><span data-stu-id="a2b39-106">**Description**</span></span>|<span data-ttu-id="a2b39-107">**Константа автоматизации**</span><span class="sxs-lookup"><span data-stu-id="a2b39-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
| <span data-ttu-id="a2b39-108">&amp;H0</span><span class="sxs-lookup"><span data-stu-id="a2b39-108">&amp;H0</span></span>  <br/> | <span data-ttu-id="a2b39-109">Значение, используемое по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="a2b39-109">Default.</span></span> <span data-ttu-id="a2b39-110">Разрешить динамическое приклеить только для динамического соединитела; в противном случае используйте статический приклейки.</span><span class="sxs-lookup"><span data-stu-id="a2b39-110">Allow dynamic glue for the dynamic connector only; otherwise, use static glue.</span></span>  <br/> |<span data-ttu-id="a2b39-111">**visGlueTypeDefault**</span><span class="sxs-lookup"><span data-stu-id="a2b39-111">**visGlueTypeDefault**</span></span> <br/> |
| <span data-ttu-id="a2b39-112">&amp;H1</span><span class="sxs-lookup"><span data-stu-id="a2b39-112">&amp;H1</span></span>  <br/> | <span data-ttu-id="a2b39-113">Разрешить динамическое приклеить.</span><span class="sxs-lookup"><span data-stu-id="a2b39-113">Allow dynamic glue.</span></span>  <br/> | <span data-ttu-id="a2b39-114">Устаревшее в Visio 2002</span><span class="sxs-lookup"><span data-stu-id="a2b39-114">Obsolete in Visio 2002</span></span>  <br/> |
| <span data-ttu-id="a2b39-115">&amp;H2</span><span class="sxs-lookup"><span data-stu-id="a2b39-115">&amp;H2</span></span>  <br/> | <span data-ttu-id="a2b39-116">Разрешить динамическое приклеить.</span><span class="sxs-lookup"><span data-stu-id="a2b39-116">Allow dynamic glue.</span></span>  <br/> |<span data-ttu-id="a2b39-117">**visGlueTypeType**</span><span class="sxs-lookup"><span data-stu-id="a2b39-117">**visGlueTypeWalking**</span></span> <br/> |
| <span data-ttu-id="a2b39-118">&amp;H4</span><span class="sxs-lookup"><span data-stu-id="a2b39-118">&amp;H4</span></span>  <br/> | <span data-ttu-id="a2b39-119">Не разрешайте динамическое приклеить.</span><span class="sxs-lookup"><span data-stu-id="a2b39-119">Do not allow dynamic glue.</span></span>  <br/> |<span data-ttu-id="a2b39-120">**visGlueTypeNo Дейсинг**</span><span class="sxs-lookup"><span data-stu-id="a2b39-120">**visGlueTypeNoWalking**</span></span> <br/> |
| <span data-ttu-id="a2b39-121">&amp;H8</span><span class="sxs-lookup"><span data-stu-id="a2b39-121">&amp;H8</span></span>  <br/> | <span data-ttu-id="a2b39-122">Не разрешайте связывать эту двух d-фигуру с помощью динамического приклейки.</span><span class="sxs-lookup"><span data-stu-id="a2b39-122">Do not allow this 2-D shape to be connected to with dynamic glue.</span></span>  <br/> |<span data-ttu-id="a2b39-123">**visGlueTypeNoTypeNoTypeingTo**</span><span class="sxs-lookup"><span data-stu-id="a2b39-123">**visGlueTypeNoWalkingTo**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a2b39-124">Примечания</span><span class="sxs-lookup"><span data-stu-id="a2b39-124">Remarks</span></span>

<span data-ttu-id="a2b39-125">Если эта ячейка содержит значение 1, 2 или 3, динамический приклей будет установлен при любом из следующих значений:</span><span class="sxs-lookup"><span data-stu-id="a2b39-125">If this cell contains a value of 1, 2 or 3, dynamic glue will be established when either of the following occurs:</span></span>
  
- <span data-ttu-id="a2b39-126">Фигуры динамически привяются в пользовательском интерфейсе.</span><span class="sxs-lookup"><span data-stu-id="a2b39-126">Shapes are dynamically glued in the user interface.</span></span>
    
- <span data-ttu-id="a2b39-127">Фигуры прикрепиваются к ячейке PinX или PinY другой фигуры из программы.</span><span class="sxs-lookup"><span data-stu-id="a2b39-127">Shapes are glued to the PinX or PinY cell of another shape from a program.</span></span>
    
<span data-ttu-id="a2b39-128">Если фигуры прикрепиваются к ячейкам фигур, кроме PinX или PinY из программы, используется статический приклейки.</span><span class="sxs-lookup"><span data-stu-id="a2b39-128">If shapes are glued to shape cells other than PinX or PinY from a program, then static glue is used.</span></span>
  
<span data-ttu-id="a2b39-129">Если изменить это значение, не разрешив динамическое приклеить, существующий динамический приклей не изменится.</span><span class="sxs-lookup"><span data-stu-id="a2b39-129">Changing this value from allowing to not allowing dynamic glue does not sever or change existing dynamic glue.</span></span> <span data-ttu-id="a2b39-130">Программы могут устанавливать динамический приклейки, даже если динамический приклейки отключен в ячейке GlueType.</span><span class="sxs-lookup"><span data-stu-id="a2b39-130">Programs can establish dynamic glue even if dynamic glue is disabled in the GlueType cell.</span></span>
  
<span data-ttu-id="a2b39-131">Чтобы получить ссылку на ячейку GlueType по имени из другой формулы или из программы с помощью свойства **CellsU,** используйте:</span><span class="sxs-lookup"><span data-stu-id="a2b39-131">To get a reference to the GlueType cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="a2b39-132">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="a2b39-132">Cell name:</span></span>  <br/> | <span data-ttu-id="a2b39-133">GlueType</span><span class="sxs-lookup"><span data-stu-id="a2b39-133">GlueType</span></span>  <br/> |
   
<span data-ttu-id="a2b39-134">Чтобы получить ссылку на ячейку GlueType по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="a2b39-134">To get a reference to the GlueType cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="a2b39-135">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="a2b39-135">Section index:</span></span>  <br/> |<span data-ttu-id="a2b39-136">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="a2b39-136">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="a2b39-137">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="a2b39-137">Row index:</span></span>  <br/> |<span data-ttu-id="a2b39-138">**visRowMisc**</span><span class="sxs-lookup"><span data-stu-id="a2b39-138">**visRowMisc**</span></span> <br/> |
| <span data-ttu-id="a2b39-139">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="a2b39-139">Cell index:</span></span>  <br/> |<span data-ttu-id="a2b39-140">**visGlueType**</span><span class="sxs-lookup"><span data-stu-id="a2b39-140">**visGlueType**</span></span> <br/> |
   

