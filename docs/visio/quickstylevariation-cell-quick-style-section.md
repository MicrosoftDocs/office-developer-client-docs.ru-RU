---
title: QuickStyleVariation Cell (Quick Style Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: e3b58a19-9f1a-4f2b-9fe2-45cbb7ec6898
description: Определяет, переопределять ли формулы и значения текста, строки и заполнять цвет (или сочетание этих свойств) с помощью цветов, контрастных с фоном схемы. Значение немного или 0, 1, 2, 4 и 8.
ms.openlocfilehash: 736e2287c00c24774ef8b677613235d642697f4b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33433796"
---
# <a name="quickstylevariation-cell-quick-style-section"></a><span data-ttu-id="c2055-104">QuickStyleVariation Cell (Quick Style Section)</span><span class="sxs-lookup"><span data-stu-id="c2055-104">QuickStyleVariation Cell (Quick Style Section)</span></span>

<span data-ttu-id="c2055-105">Определяет, переопределять ли формулы и значения текста, строки и заполнять цвет (или сочетание этих свойств) с помощью цветов, контрастных с фоном схемы.</span><span class="sxs-lookup"><span data-stu-id="c2055-105">Determines whether to override the formulas and values of text, line, and fill color (or a combination of those properties) by using colors that contrast with the diagram background.</span></span> <span data-ttu-id="c2055-106">Значение немного или 0, 1, 2, 4 и 8.</span><span class="sxs-lookup"><span data-stu-id="c2055-106">Value is a bitwise OR of 0, 1, 2, 4, and 8.</span></span>
  
|<span data-ttu-id="c2055-107">**Значение**</span><span class="sxs-lookup"><span data-stu-id="c2055-107">**Value**</span></span>|<span data-ttu-id="c2055-108">**Описание**</span><span class="sxs-lookup"><span data-stu-id="c2055-108">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="c2055-109">0</span><span class="sxs-lookup"><span data-stu-id="c2055-109">0</span></span>  <br/> |<span data-ttu-id="c2055-110">Не измените текст фигуры, строку или цвет заливки (или любое сочетание этих свойств), чтобы оставаться видимым в фоновом цвете темы.</span><span class="sxs-lookup"><span data-stu-id="c2055-110">Do not alter a shape's text, line, or fill color (or any combination of those properties) to remain visible against a theme's given background color.</span></span>  <br/> |
|<span data-ttu-id="c2055-111">1</span><span class="sxs-lookup"><span data-stu-id="c2055-111">1</span></span>  <br/> |<span data-ttu-id="c2055-112">Не измените текст фигуры, строку или цвет заливки (или любое сочетание этих свойств), чтобы оставаться видимым в фоновом цвете темы.</span><span class="sxs-lookup"><span data-stu-id="c2055-112">Do not alter a shape's text, line, or fill color (or any combination of those properties) to remain visible against a theme's given background color.</span></span>  <br/> |
|<span data-ttu-id="c2055-113">2</span><span class="sxs-lookup"><span data-stu-id="c2055-113">2</span></span>  <br/> |<span data-ttu-id="c2055-114">Измените текстовый цвет фигуры, если это необходимо, чтобы оставаться видимым в фоновом цвете темы.</span><span class="sxs-lookup"><span data-stu-id="c2055-114">Alter a shape's text color, if necessary, to remain visible against a theme's given background color.</span></span>  <br/> |
|<span data-ttu-id="c2055-115">4 </span><span class="sxs-lookup"><span data-stu-id="c2055-115">4</span></span>  <br/> |<span data-ttu-id="c2055-116">При необходимости измените цвет строки фигуры, чтобы она оставалась видимой в фоновом цвете темы.</span><span class="sxs-lookup"><span data-stu-id="c2055-116">Alter a shape's line color, if necessary, to remain visible against a theme's given background color.</span></span>  <br/> |
|<span data-ttu-id="c2055-117">8 </span><span class="sxs-lookup"><span data-stu-id="c2055-117">8</span></span>  <br/> |<span data-ttu-id="c2055-118">При необходимости измените цвет заполнения фигуры, чтобы оставаться видимым в фоновом цвете темы.</span><span class="sxs-lookup"><span data-stu-id="c2055-118">Alter a shape's fill color, if necessary, to remain visible against a theme's given background color.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c2055-119">Примечания</span><span class="sxs-lookup"><span data-stu-id="c2055-119">Remarks</span></span>

<span data-ttu-id="c2055-120">Используйте ячейку QuickStyleVariation, чтобы гарантировать видимость в тексте или строках, когда они находятся вне любой видимой геометрии фигуры (например, в форме, текстовая коробка которой находится ниже нижней части фигуры, например в сетевых схемах).</span><span class="sxs-lookup"><span data-stu-id="c2055-120">Use the QuickStyleVariation cell to guarantee visibility in either text or lines when they are outside any visible shape geometry (for example, in a shape whose textbox is below the bottom of the shape, such as those in Network Diagrams).</span></span> <span data-ttu-id="c2055-121">Значение ячейки по умолчанию — 0, что означает, что ее поведение неактивно.</span><span class="sxs-lookup"><span data-stu-id="c2055-121">The cell's default value is 0, which means that its behavior is inactive.</span></span> <span data-ttu-id="c2055-122">Любое другое значение вызывает поведение ячейки.</span><span class="sxs-lookup"><span data-stu-id="c2055-122">Any other value triggers the cell's behavior.</span></span>
  
<span data-ttu-id="c2055-123">Значение QuickStyleVariation переопределяет значение, произведенное функцией THEMEVAL, когда оно находится в ячейках Color (Character Section), FillForegnd или LineColor (или производимых прямыми ссылками на эти три свойства с помощью THEMEVAL ("CharacterColor"), THEMEVAL ("FillColor" и THEMEVAL ("LineColor")).</span><span class="sxs-lookup"><span data-stu-id="c2055-123">The QuickStyleVariation value overrides the value produced by the THEMEVAL function when it resides in the Color (Character Section), FillForegnd, or LineColor cells (or produced by direct references to these three properties by means of THEMEVAL("CharacterColor"), THEMEVAL("FillColor"), and THEMEVAL("LineColor")).</span></span>
  
<span data-ttu-id="c2055-124">Чтобы получить ссылку на **ячейку QuickStyleVariation** по имени из другой формулы, получив значение **атрибута N** элемента **Cell** или из программы с помощью свойства **CellsU,** используйте:</span><span class="sxs-lookup"><span data-stu-id="c2055-124">To get a reference to the **QuickStyleVariation** cell by name from another formula, by getting the value of the **N** attribute of a **Cell** element, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="c2055-125">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="c2055-125">Cell name:</span></span>  <br/> |<span data-ttu-id="c2055-126">QuickStyleVariation</span><span class="sxs-lookup"><span data-stu-id="c2055-126">QuickStyleVariation</span></span>  <br/> |
   
<span data-ttu-id="c2055-127">Чтобы получить ссылку на **ячейку QuickStyleVariation** по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="c2055-127">To get a reference to the **QuickStyleVariation** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="c2055-128">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="c2055-128">Section index:</span></span>  <br/> |<span data-ttu-id="c2055-129">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="c2055-129">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="c2055-130">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="c2055-130">Row index:</span></span>  <br/> |<span data-ttu-id="c2055-131">**visRowQuickStyleProperties**</span><span class="sxs-lookup"><span data-stu-id="c2055-131">**visRowQuickStyleProperties**</span></span> <br/> |
|<span data-ttu-id="c2055-132">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="c2055-132">Cell index:</span></span>  <br/> |<span data-ttu-id="c2055-133">**visQuickStyleVariation**</span><span class="sxs-lookup"><span data-stu-id="c2055-133">**visQuickStyleVariation**</span></span> <br/> |
   

