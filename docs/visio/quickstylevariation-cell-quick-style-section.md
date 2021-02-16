---
title: QuickStyleVariation Cell (Quick Style Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: e3b58a19-9f1a-4f2b-9fe2-45cbb7ec6898
description: Определяет, следует ли переопределять формулы и значения текста, строки и цвета заливки (или сочетание этих свойств) с помощью цветов, контрастных с фоном схемы. Значение — битовая или 0, 1, 2, 4 и 8.
ms.openlocfilehash: 736e2287c00c24774ef8b677613235d642697f4b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33433796"
---
# <a name="quickstylevariation-cell-quick-style-section"></a><span data-ttu-id="55ec4-104">QuickStyleVariation Cell (Quick Style Section)</span><span class="sxs-lookup"><span data-stu-id="55ec4-104">QuickStyleVariation Cell (Quick Style Section)</span></span>

<span data-ttu-id="55ec4-105">Определяет, следует ли переопределять формулы и значения текста, строки и цвета заливки (или сочетание этих свойств) с помощью цветов, контрастных с фоном схемы.</span><span class="sxs-lookup"><span data-stu-id="55ec4-105">Determines whether to override the formulas and values of text, line, and fill color (or a combination of those properties) by using colors that contrast with the diagram background.</span></span> <span data-ttu-id="55ec4-106">Значение — битовая или 0, 1, 2, 4 и 8.</span><span class="sxs-lookup"><span data-stu-id="55ec4-106">Value is a bitwise OR of 0, 1, 2, 4, and 8.</span></span>
  
|<span data-ttu-id="55ec4-107">**Значение**</span><span class="sxs-lookup"><span data-stu-id="55ec4-107">**Value**</span></span>|<span data-ttu-id="55ec4-108">**Описание**</span><span class="sxs-lookup"><span data-stu-id="55ec4-108">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="55ec4-109">0</span><span class="sxs-lookup"><span data-stu-id="55ec4-109">0</span></span>  <br/> |<span data-ttu-id="55ec4-110">Не изменяя текст, строку или цвет заливки фигуры (или любое сочетание этих свойств), чтобы они оставались видимыми для заданного цвета фона темы.</span><span class="sxs-lookup"><span data-stu-id="55ec4-110">Do not alter a shape's text, line, or fill color (or any combination of those properties) to remain visible against a theme's given background color.</span></span>  <br/> |
|<span data-ttu-id="55ec4-111">1 </span><span class="sxs-lookup"><span data-stu-id="55ec4-111">1</span></span>  <br/> |<span data-ttu-id="55ec4-112">Не изменяя текст, строку или цвет заливки фигуры (или любое сочетание этих свойств), чтобы они оставались видимыми для заданного цвета фона темы.</span><span class="sxs-lookup"><span data-stu-id="55ec4-112">Do not alter a shape's text, line, or fill color (or any combination of those properties) to remain visible against a theme's given background color.</span></span>  <br/> |
|<span data-ttu-id="55ec4-113">2 </span><span class="sxs-lookup"><span data-stu-id="55ec4-113">2</span></span>  <br/> |<span data-ttu-id="55ec4-114">При необходимости измените цвет текста фигуры, чтобы он был виден для заданного цвета фона темы.</span><span class="sxs-lookup"><span data-stu-id="55ec4-114">Alter a shape's text color, if necessary, to remain visible against a theme's given background color.</span></span>  <br/> |
|<span data-ttu-id="55ec4-115">4 </span><span class="sxs-lookup"><span data-stu-id="55ec4-115">4</span></span>  <br/> |<span data-ttu-id="55ec4-116">При необходимости измените цвет линии фигуры, чтобы она оставалась видимой для заданного цвета фона темы.</span><span class="sxs-lookup"><span data-stu-id="55ec4-116">Alter a shape's line color, if necessary, to remain visible against a theme's given background color.</span></span>  <br/> |
|<span data-ttu-id="55ec4-117">8 </span><span class="sxs-lookup"><span data-stu-id="55ec4-117">8</span></span>  <br/> |<span data-ttu-id="55ec4-118">При необходимости измените цвет заливки фигуры, чтобы она оставалась видимой для заданного цвета фона темы.</span><span class="sxs-lookup"><span data-stu-id="55ec4-118">Alter a shape's fill color, if necessary, to remain visible against a theme's given background color.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="55ec4-119">Примечания</span><span class="sxs-lookup"><span data-stu-id="55ec4-119">Remarks</span></span>

<span data-ttu-id="55ec4-120">Используйте ячейку QuickStyleVariation, чтобы гарантировать видимость текста или строк, когда они находятся за пределами видимой геометрии фигуры (например, в фигуре, текстовая рамка которой находится ниже нижней части фигуры, например в сетевых диаграммах).</span><span class="sxs-lookup"><span data-stu-id="55ec4-120">Use the QuickStyleVariation cell to guarantee visibility in either text or lines when they are outside any visible shape geometry (for example, in a shape whose textbox is below the bottom of the shape, such as those in Network Diagrams).</span></span> <span data-ttu-id="55ec4-121">Значение ячейки по умолчанию — 0, что означает, что ее поведение неактивно.</span><span class="sxs-lookup"><span data-stu-id="55ec4-121">The cell's default value is 0, which means that its behavior is inactive.</span></span> <span data-ttu-id="55ec4-122">Любое другое значение активирует поведение ячейки.</span><span class="sxs-lookup"><span data-stu-id="55ec4-122">Any other value triggers the cell's behavior.</span></span>
  
<span data-ttu-id="55ec4-123">Значение QuickStyleVariation переопределяет значение, произведенное функцией THEMEVAL, когда оно находится в ячейках Color (Character Section), FillForegnd или LineColor (или выдаваемых прямыми ссылками на эти три свойства с помощью THEMEVAL("CharacterColor"), THEMEVAL("FillColor"), и THEMEVAL("LineColor")).</span><span class="sxs-lookup"><span data-stu-id="55ec4-123">The QuickStyleVariation value overrides the value produced by the THEMEVAL function when it resides in the Color (Character Section), FillForegnd, or LineColor cells (or produced by direct references to these three properties by means of THEMEVAL("CharacterColor"), THEMEVAL("FillColor"), and THEMEVAL("LineColor")).</span></span>
  
<span data-ttu-id="55ec4-124">Чтобы получить ссылку на ячейку **QuickStyleVariation** по имени из другой формулы, получив значение атрибута **N** элемента **Cell** или из программы с помощью свойства **CellsU,** используйте:</span><span class="sxs-lookup"><span data-stu-id="55ec4-124">To get a reference to the **QuickStyleVariation** cell by name from another formula, by getting the value of the **N** attribute of a **Cell** element, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="55ec4-125">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="55ec4-125">Cell name:</span></span>  <br/> |<span data-ttu-id="55ec4-126">QuickStyleVariation</span><span class="sxs-lookup"><span data-stu-id="55ec4-126">QuickStyleVariation</span></span>  <br/> |
   
<span data-ttu-id="55ec4-127">Чтобы получить ссылку на ячейку **QuickStyleVariation** по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="55ec4-127">To get a reference to the **QuickStyleVariation** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="55ec4-128">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="55ec4-128">Section index:</span></span>  <br/> |<span data-ttu-id="55ec4-129">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="55ec4-129">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="55ec4-130">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="55ec4-130">Row index:</span></span>  <br/> |<span data-ttu-id="55ec4-131">**visRowQuickStyleProperties**</span><span class="sxs-lookup"><span data-stu-id="55ec4-131">**visRowQuickStyleProperties**</span></span> <br/> |
|<span data-ttu-id="55ec4-132">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="55ec4-132">Cell index:</span></span>  <br/> |<span data-ttu-id="55ec4-133">**visQuickStyleVariation**</span><span class="sxs-lookup"><span data-stu-id="55ec4-133">**visQuickStyleVariation**</span></span> <br/> |
   

