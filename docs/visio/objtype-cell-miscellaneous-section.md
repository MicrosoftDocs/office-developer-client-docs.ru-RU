---
title: Ячейка ObjType (раздел "Прочее")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm745
localization_priority: Normal
ms.assetid: 3afee07b-e91a-a91c-fba2-0e3251dd6385
description: Определяет, являются ли объекты размещаемыми или маршрутизируемый в схемах, при использовании диалогового окна "Настройка макета" для размещения форм.
ms.openlocfilehash: 23887e1d265e9e5ac1dfa9750bab65e8428b1c76
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19814326"
---
# <a name="objtype-cell-miscellaneous-section"></a><span data-ttu-id="c44b2-103">Ячейка ObjType (раздел "Прочее")</span><span class="sxs-lookup"><span data-stu-id="c44b2-103">ObjType Cell (Miscellaneous Section)</span></span>

<span data-ttu-id="c44b2-104">Определяет, являются ли объекты размещаемыми или маршрутизируемый в схемах, при использовании диалогового окна " **Настройка макета** " для размещения форм.</span><span class="sxs-lookup"><span data-stu-id="c44b2-104">Determines whether objects are placeable or routable in diagrams when you use the **Configure Layout** dialog box to lay out shapes.</span></span> 
  
|<span data-ttu-id="c44b2-105">**Значение**</span><span class="sxs-lookup"><span data-stu-id="c44b2-105">**Value**</span></span>|<span data-ttu-id="c44b2-106">**Описание**</span><span class="sxs-lookup"><span data-stu-id="c44b2-106">**Description**</span></span>|<span data-ttu-id="c44b2-107">**Константа автоматизации**</span><span class="sxs-lookup"><span data-stu-id="c44b2-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="c44b2-108">&amp;H0</span><span class="sxs-lookup"><span data-stu-id="c44b2-108">&amp;H0</span></span>  <br/> |<span data-ttu-id="c44b2-109">Значение, используемое по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="c44b2-109">Default.</span></span> <span data-ttu-id="c44b2-110">Приложение решает зависимости в контекст рисования.</span><span class="sxs-lookup"><span data-stu-id="c44b2-110">The application decides based on the drawing context.</span></span>  <br/> |<span data-ttu-id="c44b2-111">**visLOFlagsVisDecides**</span><span class="sxs-lookup"><span data-stu-id="c44b2-111">**visLOFlagsVisDecides**</span></span> <br/> |
|<span data-ttu-id="c44b2-112">&amp;H1</span><span class="sxs-lookup"><span data-stu-id="c44b2-112">&amp;H1</span></span>  <br/> |<span data-ttu-id="c44b2-113">Размещаемые фигуры.</span><span class="sxs-lookup"><span data-stu-id="c44b2-113">Shape is placeable.</span></span>  <br/> |<span data-ttu-id="c44b2-114">**visLOFlagsPlacable**</span><span class="sxs-lookup"><span data-stu-id="c44b2-114">**visLOFlagsPlacable**</span></span> <br/> |
|<span data-ttu-id="c44b2-115">&amp;H2</span><span class="sxs-lookup"><span data-stu-id="c44b2-115">&amp;H2</span></span>  <br/> |<span data-ttu-id="c44b2-116">Фигура поддержки маршрутизации.</span><span class="sxs-lookup"><span data-stu-id="c44b2-116">Shape is routable.</span></span> <span data-ttu-id="c44b2-117">Должен быть одномерный фигуры (1 D).</span><span class="sxs-lookup"><span data-stu-id="c44b2-117">Must be a one-dimensional (1-D) shape.</span></span>  <br/> |<span data-ttu-id="c44b2-118">**visLOFlagsRoutable**</span><span class="sxs-lookup"><span data-stu-id="c44b2-118">**visLOFlagsRoutable**</span></span> <br/> |
|<span data-ttu-id="c44b2-119">&amp;H4</span><span class="sxs-lookup"><span data-stu-id="c44b2-119">&amp;H4</span></span>  <br/> |<span data-ttu-id="c44b2-120">Фигура не является размещаемого, не поддержки маршрутизации.</span><span class="sxs-lookup"><span data-stu-id="c44b2-120">Shape is not placeable, not routable.</span></span>  <br/> |<span data-ttu-id="c44b2-121">**visLOFlagsDont**</span><span class="sxs-lookup"><span data-stu-id="c44b2-121">**visLOFlagsDont**</span></span> <br/> |
|<span data-ttu-id="c44b2-122">&amp;H8</span><span class="sxs-lookup"><span data-stu-id="c44b2-122">&amp;H8</span></span>  <br/> |<span data-ttu-id="c44b2-123">Группа содержит размещаемого/маршрутизируемые фигур.</span><span class="sxs-lookup"><span data-stu-id="c44b2-123">Group contains placeable/routable shapes.</span></span>  <br/> |<span data-ttu-id="c44b2-124">**visLOFlagsPNRGroup**</span><span class="sxs-lookup"><span data-stu-id="c44b2-124">**visLOFlagsPNRGroup**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c44b2-125">Замечания</span><span class="sxs-lookup"><span data-stu-id="c44b2-125">Remarks</span></span>

<span data-ttu-id="c44b2-126">По умолчанию ячейки объектного значение No формулу для фигуры, который имеет значение 0, что означает, что приложение определяет, является ли фигура может быть размещаемого в зависимости от его контекста.</span><span class="sxs-lookup"><span data-stu-id="c44b2-126">By default, the ObjType cell is set to No Formula for a shape, which evaluates to 0, meaning that the application determines whether the shape can be placeable depending on its context.</span></span> <span data-ttu-id="c44b2-127">Например если простой прямоугольник значения ячейки его объектного равно 0.</span><span class="sxs-lookup"><span data-stu-id="c44b2-127">For example, if you draw a simple rectangle, the value of its ObjType cell is 0.</span></span> <span data-ttu-id="c44b2-128">При использовании средства **соединитель** для подключения прямоугольника другую фигуру Visio сбрасывает значение ячейки объектного прямоугольника 1 (размещаемого).</span><span class="sxs-lookup"><span data-stu-id="c44b2-128">If you then use the **Connector** tool to connect the rectangle to another shape, Visio resets the value of the rectangle's ObjType cell to 1 (placeable).</span></span> 
  
<span data-ttu-id="c44b2-129">Значение ячейки объектного может быть комбинацию значений.</span><span class="sxs-lookup"><span data-stu-id="c44b2-129">The value of the ObjType cell can be a combination of values.</span></span> <span data-ttu-id="c44b2-130">Если не размещаемой бита (&amp;H4), однако преимущество перед других значений, кроме значение группы (&amp;H8).</span><span class="sxs-lookup"><span data-stu-id="c44b2-130">If the non-placeable bit is set (&amp;H4), however, it takes precedence over other values except the group value (&amp;H8).</span></span>
  
<span data-ttu-id="c44b2-131">Чтобы получить ссылку на ячейку объектного по имени из другой формулы, и программы, с помощью свойства **CellsU** , используйте следующую команду:</span><span class="sxs-lookup"><span data-stu-id="c44b2-131">To get a reference to the ObjType cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="c44b2-132">Имя ячейки.</span><span class="sxs-lookup"><span data-stu-id="c44b2-132">Cell name:</span></span>  <br/> |<span data-ttu-id="c44b2-133">Объектного</span><span class="sxs-lookup"><span data-stu-id="c44b2-133">ObjType</span></span>  <br/> |
   
<span data-ttu-id="c44b2-134">Для получения ссылки на ячейки объектного по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы:</span><span class="sxs-lookup"><span data-stu-id="c44b2-134">To get a reference to the ObjType cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="c44b2-135">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="c44b2-135">Section index:</span></span>  <br/> |<span data-ttu-id="c44b2-136">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="c44b2-136">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="c44b2-137">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="c44b2-137">Row index:</span></span>  <br/> |<span data-ttu-id="c44b2-138">**visRowMisc**</span><span class="sxs-lookup"><span data-stu-id="c44b2-138">**visRowMisc**</span></span> <br/> |
|<span data-ttu-id="c44b2-139">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="c44b2-139">Cell index:</span></span>  <br/> |<span data-ttu-id="c44b2-140">**visLOFlags**</span><span class="sxs-lookup"><span data-stu-id="c44b2-140">**visLOFlags**</span></span> <br/> |
   

