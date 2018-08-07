---
title: Ячейка QuickStyleVariation (раздел "Экспресс-стиль")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: e3b58a19-9f1a-4f2b-9fe2-45cbb7ec6898
description: Определяет, следует ли переопределить формулы и значения текста, строки и заливки цвет (или комбинацию этих свойств) с помощью цвета, контрастность с фон диаграммы. Значение — побитовое или 0, 1, 2, 4 и 8.
ms.openlocfilehash: fe6462798b61a0713f98196974876144cf4606e7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19814517"
---
# <a name="quickstylevariation-cell-quick-style-section"></a><span data-ttu-id="02aa8-104">Ячейка QuickStyleVariation (раздел "Экспресс-стиль")</span><span class="sxs-lookup"><span data-stu-id="02aa8-104">QuickStyleVariation Cell (Quick Style Section)</span></span>

<span data-ttu-id="02aa8-105">Определяет, следует ли переопределить формулы и значения текста, строки и заливки цвет (или комбинацию этих свойств) с помощью цвета, контрастность с фон диаграммы.</span><span class="sxs-lookup"><span data-stu-id="02aa8-105">Determines whether to override the formulas and values of text, line, and fill color (or a combination of those properties) by using colors that contrast with the diagram background.</span></span> <span data-ttu-id="02aa8-106">Значение — побитовое или 0, 1, 2, 4 и 8.</span><span class="sxs-lookup"><span data-stu-id="02aa8-106">Value is a bitwise OR of 0, 1, 2, 4, and 8.</span></span>
  
|<span data-ttu-id="02aa8-107">**Значение**</span><span class="sxs-lookup"><span data-stu-id="02aa8-107">**Value**</span></span>|<span data-ttu-id="02aa8-108">**Описание**</span><span class="sxs-lookup"><span data-stu-id="02aa8-108">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="02aa8-109">0</span><span class="sxs-lookup"><span data-stu-id="02aa8-109">0</span></span>  <br/> |<span data-ttu-id="02aa8-110">Не изменяйте текстом фигуры, строки, или заливки цвет (или любое сочетание этих свойств) видимыми от цвета заданного фона темы.</span><span class="sxs-lookup"><span data-stu-id="02aa8-110">Do not alter a shape's text, line, or fill color (or any combination of those properties) to remain visible against a theme's given background color.</span></span>  <br/> |
|<span data-ttu-id="02aa8-111">1</span><span class="sxs-lookup"><span data-stu-id="02aa8-111">1</span></span>  <br/> |<span data-ttu-id="02aa8-112">Не изменяйте текстом фигуры, строки, или заливки цвет (или любое сочетание этих свойств) видимыми от цвета заданного фона темы.</span><span class="sxs-lookup"><span data-stu-id="02aa8-112">Do not alter a shape's text, line, or fill color (or any combination of those properties) to remain visible against a theme's given background color.</span></span>  <br/> |
|<span data-ttu-id="02aa8-113">2</span><span class="sxs-lookup"><span data-stu-id="02aa8-113">2</span></span>  <br/> |<span data-ttu-id="02aa8-114">Измените цвет текста фигуры, при необходимости видимыми от темы присваивает цвет фона.</span><span class="sxs-lookup"><span data-stu-id="02aa8-114">Alter a shape's text color, if necessary, to remain visible against a theme's given background color.</span></span>  <br/> |
|<span data-ttu-id="02aa8-115">4</span><span class="sxs-lookup"><span data-stu-id="02aa8-115">4</span></span>  <br/> |<span data-ttu-id="02aa8-116">Измените цвет линии фигуры, при необходимости видимыми от темы присваивает цвет фона.</span><span class="sxs-lookup"><span data-stu-id="02aa8-116">Alter a shape's line color, if necessary, to remain visible against a theme's given background color.</span></span>  <br/> |
|<span data-ttu-id="02aa8-117">8</span><span class="sxs-lookup"><span data-stu-id="02aa8-117">8</span></span>  <br/> |<span data-ttu-id="02aa8-118">Изменение цвета заливки фигуры, при необходимости видимыми от темы присваивает цвет фона.</span><span class="sxs-lookup"><span data-stu-id="02aa8-118">Alter a shape's fill color, if necessary, to remain visible against a theme's given background color.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="02aa8-119">Замечания</span><span class="sxs-lookup"><span data-stu-id="02aa8-119">Remarks</span></span>

<span data-ttu-id="02aa8-120">Используйте ячейку QuickStyleVariation, чтобы гарантировать видимости в текст или строки, когда они находятся вне любого геометрии видимым фигуры (например, в фигуру, чьи textbox является ниже в нижней части фигуры, некоторые из которых схем сети).</span><span class="sxs-lookup"><span data-stu-id="02aa8-120">Use the QuickStyleVariation cell to guarantee visibility in either text or lines when they are outside any visible shape geometry (for example, in a shape whose textbox is below the bottom of the shape, such as those in Network Diagrams).</span></span> <span data-ttu-id="02aa8-121">Значение ячейки по умолчанию — 0, что означает, что его поведение неактивна.</span><span class="sxs-lookup"><span data-stu-id="02aa8-121">The cell's default value is 0, which means that its behavior is inactive.</span></span> <span data-ttu-id="02aa8-122">Любое другое значение запускает поведение ячейки.</span><span class="sxs-lookup"><span data-stu-id="02aa8-122">Any other value triggers the cell's behavior.</span></span>
  
<span data-ttu-id="02aa8-123">Значение QuickStyleVariation переопределяет значение, созданное функцию THEMEVAL, когда он располагается в цвет (раздел символ), FillForegnd или цвет линии ячеек (или созданные средством прямые ссылки на эти три свойства с помощью THEMEVAL (» [[[CharacterColor»), THEMEVAL("FillColor") и THEMEVAL("LineColor")).</span><span class="sxs-lookup"><span data-stu-id="02aa8-123">The QuickStyleVariation value overrides the value produced by the THEMEVAL function when it resides in the Color (Character Section), FillForegnd, or LineColor cells (or produced by direct references to these three properties by means of THEMEVAL("CharacterColor"), THEMEVAL("FillColor"), and THEMEVAL("LineColor")).</span></span>
  
<span data-ttu-id="02aa8-124">Для получения ссылки на ячейки **QuickStyleVariation** по имени из другой формулы, получив значение атрибута **N** элемента **ячейки** или из файла с помощью свойства **CellsU** , используйте:</span><span class="sxs-lookup"><span data-stu-id="02aa8-124">To get a reference to the **QuickStyleVariation** cell by name from another formula, by getting the value of the **N** attribute of a **Cell** element, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="02aa8-125">Имя ячейки.</span><span class="sxs-lookup"><span data-stu-id="02aa8-125">Cell name:</span></span>  <br/> |<span data-ttu-id="02aa8-126">QuickStyleVariation</span><span class="sxs-lookup"><span data-stu-id="02aa8-126">QuickStyleVariation</span></span>  <br/> |
   
<span data-ttu-id="02aa8-127">Для получения ссылки на ячейки **QuickStyleVariation** по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы:</span><span class="sxs-lookup"><span data-stu-id="02aa8-127">To get a reference to the **QuickStyleVariation** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="02aa8-128">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="02aa8-128">Section index:</span></span>  <br/> |<span data-ttu-id="02aa8-129">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="02aa8-129">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="02aa8-130">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="02aa8-130">Row index:</span></span>  <br/> |<span data-ttu-id="02aa8-131">**visRowQuickStyleProperties**</span><span class="sxs-lookup"><span data-stu-id="02aa8-131">**visRowQuickStyleProperties**</span></span> <br/> |
|<span data-ttu-id="02aa8-132">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="02aa8-132">Cell index:</span></span>  <br/> |<span data-ttu-id="02aa8-133">**visQuickStyleVariation**</span><span class="sxs-lookup"><span data-stu-id="02aa8-133">**visQuickStyleVariation**</span></span> <br/> |
   

