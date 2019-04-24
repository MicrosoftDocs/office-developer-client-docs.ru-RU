---
title: ObjType Cell (Miscellaneous Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm745
localization_priority: Normal
ms.assetid: 3afee07b-e91a-a91c-fba2-0e3251dd6385
description: Определяет, являются ли объекты размещаемыми или маршрутизируемыйи в схемах при использовании диалогового окна Настройка макета для размещения фигур.
ms.openlocfilehash: 7a607fdb53ad569e84976b6f9911fbd89f7f2628
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32361014"
---
# <a name="objtype-cell-miscellaneous-section"></a><span data-ttu-id="66da7-103">ObjType Cell (Miscellaneous Section)</span><span class="sxs-lookup"><span data-stu-id="66da7-103">ObjType Cell (Miscellaneous Section)</span></span>

<span data-ttu-id="66da7-104">Определяет, являются ли объекты размещаемыми или маршрутизируемыйи в схемах при использовании диалогового окна **Настройка макета** для размещения фигур.</span><span class="sxs-lookup"><span data-stu-id="66da7-104">Determines whether objects are placeable or routable in diagrams when you use the **Configure Layout** dialog box to lay out shapes.</span></span> 
  
|<span data-ttu-id="66da7-105">**Value**</span><span class="sxs-lookup"><span data-stu-id="66da7-105">**Value**</span></span>|<span data-ttu-id="66da7-106">**Описание**</span><span class="sxs-lookup"><span data-stu-id="66da7-106">**Description**</span></span>|<span data-ttu-id="66da7-107">**Константа автоматизации**</span><span class="sxs-lookup"><span data-stu-id="66da7-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="66da7-108">&amp;H0</span><span class="sxs-lookup"><span data-stu-id="66da7-108">&amp;H0</span></span>  <br/> |<span data-ttu-id="66da7-109">Значение, используемое по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="66da7-109">Default.</span></span> <span data-ttu-id="66da7-110">Приложение принимает решение в зависимости от контекста рисования.</span><span class="sxs-lookup"><span data-stu-id="66da7-110">The application decides based on the drawing context.</span></span>  <br/> |<span data-ttu-id="66da7-111">**ВислофлагсвисдеЦидес**</span><span class="sxs-lookup"><span data-stu-id="66da7-111">**visLOFlagsVisDecides**</span></span> <br/> |
|<span data-ttu-id="66da7-112">&amp;H1</span><span class="sxs-lookup"><span data-stu-id="66da7-112">&amp;H1</span></span>  <br/> |<span data-ttu-id="66da7-113">Размещена фигура.</span><span class="sxs-lookup"><span data-stu-id="66da7-113">Shape is placeable.</span></span>  <br/> |<span data-ttu-id="66da7-114">**Вислофлагсплакабле**</span><span class="sxs-lookup"><span data-stu-id="66da7-114">**visLOFlagsPlacable**</span></span> <br/> |
|<span data-ttu-id="66da7-115">&amp;H2</span><span class="sxs-lookup"><span data-stu-id="66da7-115">&amp;H2</span></span>  <br/> |<span data-ttu-id="66da7-116">Фигура поддерживает маршрутизацию.</span><span class="sxs-lookup"><span data-stu-id="66da7-116">Shape is routable.</span></span> <span data-ttu-id="66da7-117">Должен быть одномерным (1-D) фигурой.</span><span class="sxs-lookup"><span data-stu-id="66da7-117">Must be a one-dimensional (1-D) shape.</span></span>  <br/> |<span data-ttu-id="66da7-118">**Вислофлагсраутабле**</span><span class="sxs-lookup"><span data-stu-id="66da7-118">**visLOFlagsRoutable**</span></span> <br/> |
|<span data-ttu-id="66da7-119">&amp;H4</span><span class="sxs-lookup"><span data-stu-id="66da7-119">&amp;H4</span></span>  <br/> |<span data-ttu-id="66da7-120">Фигура не размещена, но не поддерживает маршрутизацию.</span><span class="sxs-lookup"><span data-stu-id="66da7-120">Shape is not placeable, not routable.</span></span>  <br/> |<span data-ttu-id="66da7-121">**Вислофлагсдонт**</span><span class="sxs-lookup"><span data-stu-id="66da7-121">**visLOFlagsDont**</span></span> <br/> |
|<span data-ttu-id="66da7-122">&amp;H8</span><span class="sxs-lookup"><span data-stu-id="66da7-122">&amp;H8</span></span>  <br/> |<span data-ttu-id="66da7-123">Группа содержит фигуры для размещения и маршрутизации.</span><span class="sxs-lookup"><span data-stu-id="66da7-123">Group contains placeable/routable shapes.</span></span>  <br/> |<span data-ttu-id="66da7-124">**Вислофлагспнрграуп**</span><span class="sxs-lookup"><span data-stu-id="66da7-124">**visLOFlagsPNRGroup**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="66da7-125">Примечания</span><span class="sxs-lookup"><span data-stu-id="66da7-125">Remarks</span></span>

<span data-ttu-id="66da7-126">По умолчанию ячейка ObjType имеет значение No формула для фигуры, которое оценивается как 0, что означает, что приложение определяет, может ли фигура быть размещена в зависимости от контекста.</span><span class="sxs-lookup"><span data-stu-id="66da7-126">By default, the ObjType cell is set to No Formula for a shape, which evaluates to 0, meaning that the application determines whether the shape can be placeable depending on its context.</span></span> <span data-ttu-id="66da7-127">Например, если вы рисуете простой прямоугольник, значение его ячейки ObjType будет равно 0.</span><span class="sxs-lookup"><span data-stu-id="66da7-127">For example, if you draw a simple rectangle, the value of its ObjType cell is 0.</span></span> <span data-ttu-id="66da7-128">Если затем использовать инструмент **Connector** для подключения прямоугольника к другой фигуре, Visio сбрасывает значение ячейки ObjType прямоугольника в 1 (размещаемое).</span><span class="sxs-lookup"><span data-stu-id="66da7-128">If you then use the **Connector** tool to connect the rectangle to another shape, Visio resets the value of the rectangle's ObjType cell to 1 (placeable).</span></span> 
  
<span data-ttu-id="66da7-129">Значение ячейки ObjType может быть сочетанием значений.</span><span class="sxs-lookup"><span data-stu-id="66da7-129">The value of the ObjType cell can be a combination of values.</span></span> <span data-ttu-id="66da7-130">Однако если задается неразмещаемый бит (&amp;H4), то он имеет приоритет над другими значениями, кроме значения группы (&amp;H8).</span><span class="sxs-lookup"><span data-stu-id="66da7-130">If the non-placeable bit is set (&amp;H4), however, it takes precedence over other values except the group value (&amp;H8).</span></span>
  
<span data-ttu-id="66da7-131">Чтобы получить ссылку на ячейку ObjType по имени из другой формулы или из программы с помощью свойства **CellsU** , используйте следующее:</span><span class="sxs-lookup"><span data-stu-id="66da7-131">To get a reference to the ObjType cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="66da7-132">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="66da7-132">Cell name:</span></span>  <br/> |<span data-ttu-id="66da7-133">ObjType</span><span class="sxs-lookup"><span data-stu-id="66da7-133">ObjType</span></span>  <br/> |
   
<span data-ttu-id="66da7-134">Чтобы получить ссылку на ячейку ObjType по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="66da7-134">To get a reference to the ObjType cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="66da7-135">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="66da7-135">Section index:</span></span>  <br/> |<span data-ttu-id="66da7-136">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="66da7-136">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="66da7-137">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="66da7-137">Row index:</span></span>  <br/> |<span data-ttu-id="66da7-138">**Висровмиск**</span><span class="sxs-lookup"><span data-stu-id="66da7-138">**visRowMisc**</span></span> <br/> |
|<span data-ttu-id="66da7-139">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="66da7-139">Cell index:</span></span>  <br/> |<span data-ttu-id="66da7-140">**Вислофлагс**</span><span class="sxs-lookup"><span data-stu-id="66da7-140">**visLOFlags**</span></span> <br/> |
   

