---
title: DisplayMode Cell (Action Tags Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm60039
localization_priority: Normal
ms.assetid: 0dfad40b-f97e-0c4a-2102-7344d1317b82
description: Определяет, отображается ли тег действия, когда пользователь нанося указатель на тег, когда фигура выбрана, или все время.
ms.openlocfilehash: 0254ad361c63dfdeddaf8a1c2173e99aa1c05398
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33415819"
---
# <a name="displaymode-cell-action-tags-section"></a><span data-ttu-id="3bd82-103">DisplayMode Cell (Action Tags Section)</span><span class="sxs-lookup"><span data-stu-id="3bd82-103">DisplayMode Cell (Action Tags Section)</span></span>

<span data-ttu-id="3bd82-104">Определяет, отображается ли тег действия, когда пользователь нанося указатель на тег, когда фигура выбрана, или все время.</span><span class="sxs-lookup"><span data-stu-id="3bd82-104">Determines whether the action tag appears when the user moves the pointer over the tag, when the shape is selected, or all the time.</span></span>
  
> [!NOTE]
> <span data-ttu-id="3bd82-105">В предыдущих версиях Microsoft Visio теги действий назывались смарт-тегами.</span><span class="sxs-lookup"><span data-stu-id="3bd82-105">In previous versions of Microsoft Visio, action tags are called smart tags.</span></span> 
  
|<span data-ttu-id="3bd82-106">**Значение**</span><span class="sxs-lookup"><span data-stu-id="3bd82-106">**Value**</span></span>|<span data-ttu-id="3bd82-107">**Режим отображения**</span><span class="sxs-lookup"><span data-stu-id="3bd82-107">**Display Mode**</span></span>|<span data-ttu-id="3bd82-108">**Константа автоматизации**</span><span class="sxs-lookup"><span data-stu-id="3bd82-108">**Automation constant**</span></span>|
|:-----|:-----|:-----|
| <span data-ttu-id="3bd82-109">0</span><span class="sxs-lookup"><span data-stu-id="3bd82-109">0</span></span>  <br/> | <span data-ttu-id="3bd82-110">Отображается, когда мышь приостанавливована на теге (по умолчанию).</span><span class="sxs-lookup"><span data-stu-id="3bd82-110">Appears when the mouse is paused over the tag (the default).</span></span>  <br/> |<span data-ttu-id="3bd82-111">**visSmartTagDispModeMouseOver**</span><span class="sxs-lookup"><span data-stu-id="3bd82-111">**visSmartTagDispModeMouseOver**</span></span> <br/> |
| <span data-ttu-id="3bd82-112">1 </span><span class="sxs-lookup"><span data-stu-id="3bd82-112">1</span></span>  <br/> | <span data-ttu-id="3bd82-113">Отображается при выборе фигуры.</span><span class="sxs-lookup"><span data-stu-id="3bd82-113">Appears while the shape is selected.</span></span>  <br/> |<span data-ttu-id="3bd82-114">**visSmartTagDispModeShapeSelected**</span><span class="sxs-lookup"><span data-stu-id="3bd82-114">**visSmartTagDispModeShapeSelected**</span></span> <br/> |
| <span data-ttu-id="3bd82-115">2 </span><span class="sxs-lookup"><span data-stu-id="3bd82-115">2</span></span>  <br/> | <span data-ttu-id="3bd82-116">Отображается постоянно.</span><span class="sxs-lookup"><span data-stu-id="3bd82-116">Appears all the time.</span></span>  <br/> |<span data-ttu-id="3bd82-117">**visSmartTagDispModeAlways**</span><span class="sxs-lookup"><span data-stu-id="3bd82-117">**visSmartTagDispModeAlways**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="3bd82-118">Примечания</span><span class="sxs-lookup"><span data-stu-id="3bd82-118">Remarks</span></span>

<span data-ttu-id="3bd82-119">Теги действий не отображаются в печатных и опубликованных выходных данных.</span><span class="sxs-lookup"><span data-stu-id="3bd82-119">Action tags do not appear on printed or published output.</span></span> 
  
<span data-ttu-id="3bd82-120">Если тег действия определен для страницы и эта ячейка содержит значение 1, тег никогда не отображается, так как страницу невозможно выбрать.</span><span class="sxs-lookup"><span data-stu-id="3bd82-120">If an action tag is defined for a page, and this cell contains a value of 1, the tag never appears because a page cannot be selected.</span></span> 
  
<span data-ttu-id="3bd82-121">Чтобы получить ссылку на ячейку DisplayMode по имени из другой формулы или из программы с помощью свойства **CellsU,** используйте:</span><span class="sxs-lookup"><span data-stu-id="3bd82-121">To get a reference to the DisplayMode cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="3bd82-122">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="3bd82-122">Cell name:</span></span>  <br/> | <span data-ttu-id="3bd82-123">SmartTags.</span><span class="sxs-lookup"><span data-stu-id="3bd82-123">SmartTags.</span></span>  <span data-ttu-id="3bd82-124">*name*  . DisplayMode, где SmartTags.</span><span class="sxs-lookup"><span data-stu-id="3bd82-124">*name*  .DisplayMode           where SmartTags.</span></span> <span data-ttu-id="3bd82-125">*имя* — название строки тегов действий.</span><span class="sxs-lookup"><span data-stu-id="3bd82-125">*name*  is the name of the action tag row</span></span>  <br/> |
   
<span data-ttu-id="3bd82-126">Чтобы получить ссылку на ячейку DisplayMode по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="3bd82-126">To get a reference to the DisplayMode cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="3bd82-127">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="3bd82-127">Section index:</span></span>  <br/> |<span data-ttu-id="3bd82-128">**visSectionSmartTag**</span><span class="sxs-lookup"><span data-stu-id="3bd82-128">**visSectionSmartTag**</span></span> <br/> |
| <span data-ttu-id="3bd82-129">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="3bd82-129">Row index:</span></span>  <br/> |<span data-ttu-id="3bd82-130">**visRowSmartTag** +  *i*, где *i* = 0, 1, 2…</span><span class="sxs-lookup"><span data-stu-id="3bd82-130">**visRowSmartTag** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="3bd82-131">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="3bd82-131">Cell index:</span></span>  <br/> |<span data-ttu-id="3bd82-132">**visSmartTagDisplayMode**</span><span class="sxs-lookup"><span data-stu-id="3bd82-132">**visSmartTagDisplayMode**</span></span> <br/> |
   

