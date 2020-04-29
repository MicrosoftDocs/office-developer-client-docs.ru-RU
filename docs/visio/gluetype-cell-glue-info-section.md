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
description: Определяет, использует ли Одномерная фигура статическую ("точка-точка") или динамическую (фигурную фигуру) приклеить к другой фигуре.
ms.openlocfilehash: ae4eddf17c6e7b5e56cb3397f03d0721d965c9b7
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33410674"
---
# <a name="gluetype-cell-glue-info-section"></a><span data-ttu-id="97e57-103">GlueType Cell (Glue Info Section)</span><span class="sxs-lookup"><span data-stu-id="97e57-103">GlueType Cell (Glue Info Section)</span></span>

<span data-ttu-id="97e57-104">Определяет, использует ли Одномерная фигура статическую ("точка-точка") или динамическую (фигурную фигуру) приклеить к другой фигуре.</span><span class="sxs-lookup"><span data-stu-id="97e57-104">Determines whether a 1-D shape uses static (point-to-point) or dynamic (shape-to-shape) glue when it is glued to another shape.</span></span>
  
|<span data-ttu-id="97e57-105">**Значение**</span><span class="sxs-lookup"><span data-stu-id="97e57-105">**Value**</span></span>|<span data-ttu-id="97e57-106">**Описание**</span><span class="sxs-lookup"><span data-stu-id="97e57-106">**Description**</span></span>|<span data-ttu-id="97e57-107">**Константа автоматизации**</span><span class="sxs-lookup"><span data-stu-id="97e57-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
| <span data-ttu-id="97e57-108">&amp;H0</span><span class="sxs-lookup"><span data-stu-id="97e57-108">&amp;H0</span></span>  <br/> | <span data-ttu-id="97e57-109">Значение, используемое по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="97e57-109">Default.</span></span> <span data-ttu-id="97e57-110">Разрешить динамическое приклеивание только для динамического соединителя; в противном случае используйте статическую привязывание.</span><span class="sxs-lookup"><span data-stu-id="97e57-110">Allow dynamic glue for the dynamic connector only; otherwise, use static glue.</span></span>  <br/> |<span data-ttu-id="97e57-111">**висглуетипедефаулт**</span><span class="sxs-lookup"><span data-stu-id="97e57-111">**visGlueTypeDefault**</span></span> <br/> |
| <span data-ttu-id="97e57-112">&amp;H1</span><span class="sxs-lookup"><span data-stu-id="97e57-112">&amp;H1</span></span>  <br/> | <span data-ttu-id="97e57-113">Разрешить динамическое привязывание.</span><span class="sxs-lookup"><span data-stu-id="97e57-113">Allow dynamic glue.</span></span>  <br/> | <span data-ttu-id="97e57-114">Устаревшие в Visio 2002</span><span class="sxs-lookup"><span data-stu-id="97e57-114">Obsolete in Visio 2002</span></span>  <br/> |
| <span data-ttu-id="97e57-115">&amp;H2</span><span class="sxs-lookup"><span data-stu-id="97e57-115">&amp;H2</span></span>  <br/> | <span data-ttu-id="97e57-116">Разрешить динамическое привязывание.</span><span class="sxs-lookup"><span data-stu-id="97e57-116">Allow dynamic glue.</span></span>  <br/> |<span data-ttu-id="97e57-117">**висглуетипевалкинг**</span><span class="sxs-lookup"><span data-stu-id="97e57-117">**visGlueTypeWalking**</span></span> <br/> |
| <span data-ttu-id="97e57-118">&amp;H4</span><span class="sxs-lookup"><span data-stu-id="97e57-118">&amp;H4</span></span>  <br/> | <span data-ttu-id="97e57-119">Не разрешать динамическое приклеивание.</span><span class="sxs-lookup"><span data-stu-id="97e57-119">Do not allow dynamic glue.</span></span>  <br/> |<span data-ttu-id="97e57-120">**висглуетипеновалкинг**</span><span class="sxs-lookup"><span data-stu-id="97e57-120">**visGlueTypeNoWalking**</span></span> <br/> |
| <span data-ttu-id="97e57-121">&amp;H8</span><span class="sxs-lookup"><span data-stu-id="97e57-121">&amp;H8</span></span>  <br/> | <span data-ttu-id="97e57-122">Не разрешать подключаться к этой двумерной фигуре с динамической привязкой.</span><span class="sxs-lookup"><span data-stu-id="97e57-122">Do not allow this 2-D shape to be connected to with dynamic glue.</span></span>  <br/> |<span data-ttu-id="97e57-123">**висглуетипеновалкингто**</span><span class="sxs-lookup"><span data-stu-id="97e57-123">**visGlueTypeNoWalkingTo**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="97e57-124">Примечания</span><span class="sxs-lookup"><span data-stu-id="97e57-124">Remarks</span></span>

<span data-ttu-id="97e57-125">Если эта ячейка содержит значение 1, 2 или 3, динамическое приклеивание будет установлено в следующих случаях:</span><span class="sxs-lookup"><span data-stu-id="97e57-125">If this cell contains a value of 1, 2 or 3, dynamic glue will be established when either of the following occurs:</span></span>
  
- <span data-ttu-id="97e57-126">Фигуры динамически связаны в пользовательском интерфейсе.</span><span class="sxs-lookup"><span data-stu-id="97e57-126">Shapes are dynamically glued in the user interface.</span></span>
    
- <span data-ttu-id="97e57-127">Фигуры привязываются к ячейке PinX или PinY другой фигуры из программы.</span><span class="sxs-lookup"><span data-stu-id="97e57-127">Shapes are glued to the PinX or PinY cell of another shape from a program.</span></span>
    
<span data-ttu-id="97e57-128">Если фигуры привязываются к ячейкам фигур, отличным от PinX или PinY, в программе, то используется статическая приклеивание.</span><span class="sxs-lookup"><span data-stu-id="97e57-128">If shapes are glued to shape cells other than PinX or PinY from a program, then static glue is used.</span></span>
  
<span data-ttu-id="97e57-129">Изменение этого значения с "разрешить" без разрешения динамической приклеивание не является критичным или изменяет существующее динамическое привязывание.</span><span class="sxs-lookup"><span data-stu-id="97e57-129">Changing this value from allowing to not allowing dynamic glue does not sever or change existing dynamic glue.</span></span> <span data-ttu-id="97e57-130">Программы могут устанавливать динамическую привязывание, даже если динамическое приклеивание отключено в ячейке GlueType.</span><span class="sxs-lookup"><span data-stu-id="97e57-130">Programs can establish dynamic glue even if dynamic glue is disabled in the GlueType cell.</span></span>
  
<span data-ttu-id="97e57-131">Чтобы получить ссылку на ячейку GlueType по имени из другой формулы или из программы с помощью свойства **CellsU** , используйте следующее:</span><span class="sxs-lookup"><span data-stu-id="97e57-131">To get a reference to the GlueType cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="97e57-132">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="97e57-132">Cell name:</span></span>  <br/> | <span data-ttu-id="97e57-133">GlueType</span><span class="sxs-lookup"><span data-stu-id="97e57-133">GlueType</span></span>  <br/> |
   
<span data-ttu-id="97e57-134">Чтобы получить ссылку на ячейку GlueType по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="97e57-134">To get a reference to the GlueType cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="97e57-135">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="97e57-135">Section index:</span></span>  <br/> |<span data-ttu-id="97e57-136">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="97e57-136">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="97e57-137">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="97e57-137">Row index:</span></span>  <br/> |<span data-ttu-id="97e57-138">**висровмиск**</span><span class="sxs-lookup"><span data-stu-id="97e57-138">**visRowMisc**</span></span> <br/> |
| <span data-ttu-id="97e57-139">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="97e57-139">Cell index:</span></span>  <br/> |<span data-ttu-id="97e57-140">**висглуетипе**</span><span class="sxs-lookup"><span data-stu-id="97e57-140">**visGlueType**</span></span> <br/> |
   

