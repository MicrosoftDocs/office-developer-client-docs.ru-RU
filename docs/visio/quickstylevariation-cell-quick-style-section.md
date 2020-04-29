---
title: QuickStyleVariation Cell (Quick Style Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: e3b58a19-9f1a-4f2b-9fe2-45cbb7ec6898
description: Определяет, переопределяются ли формулы и значения цвета текста, линий и заливки (или их комбинации) с помощью цветов, которые отличаются фоном схемы. Значение — это побитовое значение, равное 0, 1, 2, 4 и 8.
ms.openlocfilehash: 736e2287c00c24774ef8b677613235d642697f4b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33433796"
---
# <a name="quickstylevariation-cell-quick-style-section"></a><span data-ttu-id="5c294-104">QuickStyleVariation Cell (Quick Style Section)</span><span class="sxs-lookup"><span data-stu-id="5c294-104">QuickStyleVariation Cell (Quick Style Section)</span></span>

<span data-ttu-id="5c294-105">Определяет, переопределяются ли формулы и значения цвета текста, линий и заливки (или их комбинации) с помощью цветов, которые отличаются фоном схемы.</span><span class="sxs-lookup"><span data-stu-id="5c294-105">Determines whether to override the formulas and values of text, line, and fill color (or a combination of those properties) by using colors that contrast with the diagram background.</span></span> <span data-ttu-id="5c294-106">Значение — это побитовое значение, равное 0, 1, 2, 4 и 8.</span><span class="sxs-lookup"><span data-stu-id="5c294-106">Value is a bitwise OR of 0, 1, 2, 4, and 8.</span></span>
  
|<span data-ttu-id="5c294-107">**Значение**</span><span class="sxs-lookup"><span data-stu-id="5c294-107">**Value**</span></span>|<span data-ttu-id="5c294-108">**Описание**</span><span class="sxs-lookup"><span data-stu-id="5c294-108">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="5c294-109">нуль</span><span class="sxs-lookup"><span data-stu-id="5c294-109">0</span></span>  <br/> |<span data-ttu-id="5c294-110">Не изменяйте цвет текста, линии или заливки фигуры (или любое сочетание этих свойств), чтобы они оставались видимыми для данного цвета фона темы.</span><span class="sxs-lookup"><span data-stu-id="5c294-110">Do not alter a shape's text, line, or fill color (or any combination of those properties) to remain visible against a theme's given background color.</span></span>  <br/> |
|<span data-ttu-id="5c294-111">1,1</span><span class="sxs-lookup"><span data-stu-id="5c294-111">1</span></span>  <br/> |<span data-ttu-id="5c294-112">Не изменяйте цвет текста, линии или заливки фигуры (или любое сочетание этих свойств), чтобы они оставались видимыми для данного цвета фона темы.</span><span class="sxs-lookup"><span data-stu-id="5c294-112">Do not alter a shape's text, line, or fill color (or any combination of those properties) to remain visible against a theme's given background color.</span></span>  <br/> |
|<span data-ttu-id="5c294-113">2</span><span class="sxs-lookup"><span data-stu-id="5c294-113">2</span></span>  <br/> |<span data-ttu-id="5c294-114">При необходимости измените цвет текста фигуры, чтобы он оставался видимым для данного цвета фона темы.</span><span class="sxs-lookup"><span data-stu-id="5c294-114">Alter a shape's text color, if necessary, to remain visible against a theme's given background color.</span></span>  <br/> |
|<span data-ttu-id="5c294-115">4 </span><span class="sxs-lookup"><span data-stu-id="5c294-115">4</span></span>  <br/> |<span data-ttu-id="5c294-116">При необходимости измените цвет линии фигуры, чтобы она оставалась видимой по отношению к цвету фона, заданному темой.</span><span class="sxs-lookup"><span data-stu-id="5c294-116">Alter a shape's line color, if necessary, to remain visible against a theme's given background color.</span></span>  <br/> |
|<span data-ttu-id="5c294-117">8 </span><span class="sxs-lookup"><span data-stu-id="5c294-117">8</span></span>  <br/> |<span data-ttu-id="5c294-118">При необходимости измените цвет заливки фигуры, чтобы она оставалась видимой по отношению к цвету фона, заданному темой.</span><span class="sxs-lookup"><span data-stu-id="5c294-118">Alter a shape's fill color, if necessary, to remain visible against a theme's given background color.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="5c294-119">Примечания</span><span class="sxs-lookup"><span data-stu-id="5c294-119">Remarks</span></span>

<span data-ttu-id="5c294-120">Используйте ячейку QuickStyleVariation, чтобы гарантировать видимость текста или линий, когда они выходят за границы любой видимой геометрии фигуры (например, в фигуре, текстовое поле которого находится ниже нижней границы фигуры, например, на схеме сети).</span><span class="sxs-lookup"><span data-stu-id="5c294-120">Use the QuickStyleVariation cell to guarantee visibility in either text or lines when they are outside any visible shape geometry (for example, in a shape whose textbox is below the bottom of the shape, such as those in Network Diagrams).</span></span> <span data-ttu-id="5c294-121">Значение по умолчанию для ячейки равно 0, что означает, что ее поведение неактивна.</span><span class="sxs-lookup"><span data-stu-id="5c294-121">The cell's default value is 0, which means that its behavior is inactive.</span></span> <span data-ttu-id="5c294-122">Любое другое значение инициирует поведение ячейки.</span><span class="sxs-lookup"><span data-stu-id="5c294-122">Any other value triggers the cell's behavior.</span></span>
  
<span data-ttu-id="5c294-123">Значение QuickStyleVariation переопределяет значение, созданное функцией THEMEVAL, когда оно находится в ячейках Color (символ), FillForegnd или LineColor (или вызывается прямыми ссылками на эти три свойства с помощью THEMEVAL ("Чарактерколор"), THEMEVAL ("") и THEMEVAL ("LineColor")).</span><span class="sxs-lookup"><span data-stu-id="5c294-123">The QuickStyleVariation value overrides the value produced by the THEMEVAL function when it resides in the Color (Character Section), FillForegnd, or LineColor cells (or produced by direct references to these three properties by means of THEMEVAL("CharacterColor"), THEMEVAL("FillColor"), and THEMEVAL("LineColor")).</span></span>
  
<span data-ttu-id="5c294-124">Чтобы получить ссылку на ячейку **QuickStyleVariation** по имени из другой формулы, путем получения значения атрибута **N** элемента **Cell** или из программы с помощью свойства **CellsU** , используйте следующее:</span><span class="sxs-lookup"><span data-stu-id="5c294-124">To get a reference to the **QuickStyleVariation** cell by name from another formula, by getting the value of the **N** attribute of a **Cell** element, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="5c294-125">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="5c294-125">Cell name:</span></span>  <br/> |<span data-ttu-id="5c294-126">QuickStyleVariation</span><span class="sxs-lookup"><span data-stu-id="5c294-126">QuickStyleVariation</span></span>  <br/> |
   
<span data-ttu-id="5c294-127">Чтобы получить ссылку на ячейку **QuickStyleVariation** по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="5c294-127">To get a reference to the **QuickStyleVariation** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="5c294-128">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="5c294-128">Section index:</span></span>  <br/> |<span data-ttu-id="5c294-129">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="5c294-129">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="5c294-130">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="5c294-130">Row index:</span></span>  <br/> |<span data-ttu-id="5c294-131">**висровкуиккстилепропертиес**</span><span class="sxs-lookup"><span data-stu-id="5c294-131">**visRowQuickStyleProperties**</span></span> <br/> |
|<span data-ttu-id="5c294-132">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="5c294-132">Cell index:</span></span>  <br/> |<span data-ttu-id="5c294-133">**вискуиккстилевариатион**</span><span class="sxs-lookup"><span data-stu-id="5c294-133">**visQuickStyleVariation**</span></span> <br/> |
   

