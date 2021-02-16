---
title: ShdwType Cell (Page Properties Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm60084
localization_priority: Normal
ms.assetid: 551166d0-3aaa-0fd7-e742-cf3450ba90ed
description: Указывает тип теней по умолчанию для страницы.
ms.openlocfilehash: f1fc72484d94788ca2798760ca935c89c3e841ad
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33424100"
---
# <a name="shdwtype-cell-page-properties-section"></a><span data-ttu-id="ee52b-103">ShdwType Cell (Page Properties Section)</span><span class="sxs-lookup"><span data-stu-id="ee52b-103">ShdwType Cell (Page Properties Section)</span></span>

<span data-ttu-id="ee52b-104">Указывает тип теней по умолчанию для страницы.</span><span class="sxs-lookup"><span data-stu-id="ee52b-104">Indicates the default shadow type for a page.</span></span>
  
|<span data-ttu-id="ee52b-105">**Значение**</span><span class="sxs-lookup"><span data-stu-id="ee52b-105">**Value**</span></span>|<span data-ttu-id="ee52b-106">**Описание**</span><span class="sxs-lookup"><span data-stu-id="ee52b-106">**Description**</span></span>|<span data-ttu-id="ee52b-107">**Константа автоматизации**</span><span class="sxs-lookup"><span data-stu-id="ee52b-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
| <span data-ttu-id="ee52b-108">1 </span><span class="sxs-lookup"><span data-stu-id="ee52b-108">1</span></span>  <br/> | <span data-ttu-id="ee52b-109">Простой</span><span class="sxs-lookup"><span data-stu-id="ee52b-109">Simple</span></span>  <br/> |<span data-ttu-id="ee52b-110">**visFSTSimple**</span><span class="sxs-lookup"><span data-stu-id="ee52b-110">**visFSTSimple**</span></span> <br/> |
| <span data-ttu-id="ee52b-111">2 </span><span class="sxs-lookup"><span data-stu-id="ee52b-111">2</span></span>  <br/> | <span data-ttu-id="ee52b-112">Oblique</span><span class="sxs-lookup"><span data-stu-id="ee52b-112">Oblique</span></span>  <br/> |<span data-ttu-id="ee52b-113">**visFSTOblique**</span><span class="sxs-lookup"><span data-stu-id="ee52b-113">**visFSTOblique**</span></span> <br/> |
|<span data-ttu-id="ee52b-114">3 </span><span class="sxs-lookup"><span data-stu-id="ee52b-114">3</span></span>  <br/> |<span data-ttu-id="ee52b-115">Внутренний</span><span class="sxs-lookup"><span data-stu-id="ee52b-115">Inner</span></span>  <br/> |<span data-ttu-id="ee52b-116">**visFSTInner**</span><span class="sxs-lookup"><span data-stu-id="ee52b-116">**visFSTInner**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ee52b-117">Примечания</span><span class="sxs-lookup"><span data-stu-id="ee52b-117">Remarks</span></span>

 <span data-ttu-id="ee52b-118">Тип теней, описанный в этой ячейке, используется, когда для ячейки ShapeShdwType (тип теней для отдельной фигуры на странице) установлено значение Page Default (**visFSTPageDefault).**</span><span class="sxs-lookup"><span data-stu-id="ee52b-118">The shadow type described in this cell is used whenever the ShapeShdwType Cell (the shadow type for an individual shape on the page) is set to Page Default (**visFSTPageDefault** ).</span></span> 
  
<span data-ttu-id="ee52b-119">Простые типы теней описываются как тени смещения в пользовательском интерфейсе.</span><span class="sxs-lookup"><span data-stu-id="ee52b-119">Simple shadow types are described as offset shadows in the user interface (UI).</span></span> <span data-ttu-id="ee52b-120">Простая тень дает эффект тени фигуры на параллельную плоскость, расположенную на некотором расстоянии от нее.</span><span class="sxs-lookup"><span data-stu-id="ee52b-120">A simple shadow gives the effect of the shape being shadowed onto a parallel plane located some distance behind it.</span></span> <span data-ttu-id="ee52b-121">Косые тени описываются как косые тени в пользовательском интерфейсе и дают эффект отвершения тени на плоскость, перпендикулярную фигуре.</span><span class="sxs-lookup"><span data-stu-id="ee52b-121">Oblique shadows are described as oblique shadows in the UI and give the effect of a shadow being cast onto a plane perpendicular to the shape.</span></span> 
  
<span data-ttu-id="ee52b-122">Список предопределяемых простых и нестрогих  типов теней  см. в  списке стилей на  вкладке "Тени" диалоговых окна "Настройка страницы" (на вкладке "Конструктор" щелкните стрелку "Настройка страницы"). </span><span class="sxs-lookup"><span data-stu-id="ee52b-122">For a list of predefined simple and oblique shadow types, see the **Style** list on the **Shadows** tab of the **Page Setup** dialog box (on the **Design** tab, click the **Page Setup** arrow).</span></span> 
  
<span data-ttu-id="ee52b-123">Чтобы получить ссылку на ячейку ShdwType по имени из другой формулы или из программы с помощью свойства **CellsU,** используйте:</span><span class="sxs-lookup"><span data-stu-id="ee52b-123">To get a reference to the ShdwType cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="ee52b-124">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="ee52b-124">Cell name:</span></span>  <br/> | <span data-ttu-id="ee52b-125">ShdwType</span><span class="sxs-lookup"><span data-stu-id="ee52b-125">ShdwType</span></span>  <br/> |
   
<span data-ttu-id="ee52b-126">Чтобы получить ссылку на ячейку ShapeShdwOffsetX по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="ee52b-126">To get a reference to the ShapeShdwOffsetX cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="ee52b-127">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="ee52b-127">Section index:</span></span>  <br/> |<span data-ttu-id="ee52b-128">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="ee52b-128">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="ee52b-129">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="ee52b-129">Row index:</span></span>  <br/> |<span data-ttu-id="ee52b-130">**visRowPage**</span><span class="sxs-lookup"><span data-stu-id="ee52b-130">**visRowPage**</span></span> <br/> |
| <span data-ttu-id="ee52b-131">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="ee52b-131">Cell index:</span></span>  <br/> |<span data-ttu-id="ee52b-132">**visPageShdwType**</span><span class="sxs-lookup"><span data-stu-id="ee52b-132">**visPageShdwType**</span></span> <br/> |
   

