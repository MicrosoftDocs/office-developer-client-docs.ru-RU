---
title: Style Cell (Character Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251249
localization_priority: Normal
ms.assetid: 4372f1e1-f0a9-2f63-ff79-58f2afdceed5
description: Показывает форматирование символов, применяемого к диапазону текста в текстовом блоке фигуры.
ms.openlocfilehash: 349bdc42485aa511011aeb85a43f1ab3e4ea853d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33411430"
---
# <a name="style-cell-character-section"></a><span data-ttu-id="2f130-103">Style Cell (Character Section)</span><span class="sxs-lookup"><span data-stu-id="2f130-103">Style Cell (Character Section)</span></span>

<span data-ttu-id="2f130-104">Показывает форматирование символов, применяемого к диапазону текста в текстовом блоке фигуры.</span><span class="sxs-lookup"><span data-stu-id="2f130-104">Shows the character formatting applied to a range of text in the shape's text block.</span></span>
  
|<span data-ttu-id="2f130-105">**Style**</span><span class="sxs-lookup"><span data-stu-id="2f130-105">**Style**</span></span>|<span data-ttu-id="2f130-106">**Значение**</span><span class="sxs-lookup"><span data-stu-id="2f130-106">**Value**</span></span>|<span data-ttu-id="2f130-107">**Константа автоматизации**</span><span class="sxs-lookup"><span data-stu-id="2f130-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
| <span data-ttu-id="2f130-108">Полужирный</span><span class="sxs-lookup"><span data-stu-id="2f130-108">Bold</span></span>  <br/> | <span data-ttu-id="2f130-109">&amp;H1</span><span class="sxs-lookup"><span data-stu-id="2f130-109">&amp;H1</span></span>  <br/> |<span data-ttu-id="2f130-110">**visBold**</span><span class="sxs-lookup"><span data-stu-id="2f130-110">**visBold**</span></span> <br/> |
| <span data-ttu-id="2f130-111">Курсив</span><span class="sxs-lookup"><span data-stu-id="2f130-111">Italic</span></span>  <br/> | <span data-ttu-id="2f130-112">&amp;H2</span><span class="sxs-lookup"><span data-stu-id="2f130-112">&amp;H2</span></span>  <br/> |<span data-ttu-id="2f130-113">**visItalic**</span><span class="sxs-lookup"><span data-stu-id="2f130-113">**visItalic**</span></span> <br/> |
| <span data-ttu-id="2f130-114">Подчеркнутый</span><span class="sxs-lookup"><span data-stu-id="2f130-114">Underline</span></span>  <br/> | <span data-ttu-id="2f130-115">&amp;H4</span><span class="sxs-lookup"><span data-stu-id="2f130-115">&amp;H4</span></span>  <br/> |<span data-ttu-id="2f130-116">**visUnderLine**</span><span class="sxs-lookup"><span data-stu-id="2f130-116">**visUnderLine**</span></span> <br/> |
| <span data-ttu-id="2f130-117">Маленькие шапки</span><span class="sxs-lookup"><span data-stu-id="2f130-117">Small caps</span></span>  <br/> | <span data-ttu-id="2f130-118">&amp;H8</span><span class="sxs-lookup"><span data-stu-id="2f130-118">&amp;H8</span></span>  <br/> |<span data-ttu-id="2f130-119">**visSmallCaps**</span><span class="sxs-lookup"><span data-stu-id="2f130-119">**visSmallCaps**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="2f130-120">Примечания</span><span class="sxs-lookup"><span data-stu-id="2f130-120">Remarks</span></span>

<span data-ttu-id="2f130-121">Ячейка Style содержит сведения форматирования, применяемые к подстанце текста фигуры, если раздел Символы содержит несколько строк.</span><span class="sxs-lookup"><span data-stu-id="2f130-121">The Style cell contains formatting information applied to a sub-range of a shape's text if the Characters section contains multiple rows.</span></span> <span data-ttu-id="2f130-122">В противном случае он содержит сведения о формате для всего текста фигуры.</span><span class="sxs-lookup"><span data-stu-id="2f130-122">Otherwise, it contains formatting information for all of the shape's text.</span></span>
  
<span data-ttu-id="2f130-123">Это значение представляет двоичный номер, в котором каждый бит указывает стиль символов.</span><span class="sxs-lookup"><span data-stu-id="2f130-123">The value represents a binary number in which each bit indicates a character style.</span></span> <span data-ttu-id="2f130-124">Например, значение 3 представляет текст, отформатированный как в виде италика, так и жирного.</span><span class="sxs-lookup"><span data-stu-id="2f130-124">For example, a value of 3 represents text formatted in both italic and bold.</span></span> <span data-ttu-id="2f130-125">Если значение Style — 0, текст является простым или неформатным.</span><span class="sxs-lookup"><span data-stu-id="2f130-125">If the value of Style is 0, the text is plain, or unformatted.</span></span> <span data-ttu-id="2f130-126">Вы можете протестировать для определенного формата с помощью функций БИТ \* Boolean.</span><span class="sxs-lookup"><span data-stu-id="2f130-126">You can test for a particular format using Boolean BIT\* functions.</span></span> <span data-ttu-id="2f130-127">Сведения об этих функциях см. в документации по программированию.</span><span class="sxs-lookup"><span data-stu-id="2f130-127">See your programming documentation for details about these functions.</span></span>
  
<span data-ttu-id="2f130-128">Чтобы получить ссылку на ячейку Style по имени из другой формулы или из программы с помощью свойства **CellsU,** используйте:</span><span class="sxs-lookup"><span data-stu-id="2f130-128">To get a reference to the Style cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="2f130-129">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="2f130-129">Cell name:</span></span>  <br/> | <span data-ttu-id="2f130-130">Char.Style[  *i*  ] где  *i*  = <1>, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="2f130-130">Char.Style[  *i*  ]            where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="2f130-131">Чтобы получить ссылку на ячейку Style по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="2f130-131">To get a reference to the Style cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="2f130-132">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="2f130-132">Section index:</span></span>  <br/> |<span data-ttu-id="2f130-133">**visSectionCharacter**</span><span class="sxs-lookup"><span data-stu-id="2f130-133">**visSectionCharacter**</span></span> <br/> |
| <span data-ttu-id="2f130-134">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="2f130-134">Row index:</span></span>  <br/> |<span data-ttu-id="2f130-135">**visRowCharacter**  +   *i,* *где i* = 0, 1, 2 ...</span><span class="sxs-lookup"><span data-stu-id="2f130-135">**visRowCharacter** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="2f130-136">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="2f130-136">Cell index:</span></span>  <br/> |<span data-ttu-id="2f130-137">**visCharacterStyle**</span><span class="sxs-lookup"><span data-stu-id="2f130-137">**visCharacterStyle**</span></span> <br/> |
   
 <span data-ttu-id="2f130-138">*Пример*</span><span class="sxs-lookup"><span data-stu-id="2f130-138">*Example*</span></span> 
  
<span data-ttu-id="2f130-139">Предположим, что ячейка Color в первом ряду раздела Символ фигуры заданной для этой формулы:</span><span class="sxs-lookup"><span data-stu-id="2f130-139">Suppose the Color cell in the first row of a shape's Character section is set to this formula:</span></span>
  
<span data-ttu-id="2f130-140">= IF(BITAND(Char.Style,1)=1,4,3)</span><span class="sxs-lookup"><span data-stu-id="2f130-140">= IF(BITAND(Char.Style,1)=1,4,3)</span></span>
  
<span data-ttu-id="2f130-141">Затем, если первый символ текста фигуры имеет полужирный характер, текст, охватываемый первой строкой свойств символов, будет синим (4); в противном случае он будет зеленым (3).</span><span class="sxs-lookup"><span data-stu-id="2f130-141">Then if the first character of the shape's text is bold, the text covered by the first Character properties row will be blue (4); otherwise it will be green (3).</span></span> <span data-ttu-id="2f130-142">В этом примере предполагается, что по умолчанию имеются цвета.</span><span class="sxs-lookup"><span data-stu-id="2f130-142">This example assumes default colors are in effect.</span></span>
  
<span data-ttu-id="2f130-143">Ниже приводится пример настройки ячейки Style в программе.</span><span class="sxs-lookup"><span data-stu-id="2f130-143">The following is an example of setting the Style cell in a program.</span></span> <span data-ttu-id="2f130-144">В первом заявлении ссылается ячейка Style по имени, а во втором - ячейка Style по индексу.</span><span class="sxs-lookup"><span data-stu-id="2f130-144">The first statement references the Style cell by name, and the second statement references the Style cell by index.</span></span> <span data-ttu-id="2f130-145">Оба утверждения применяются в тексте, накрытом второй строкой раздела Символ фигуры.</span><span class="sxs-lookup"><span data-stu-id="2f130-145">Both statements apply italic to the text covered by the second row of a shape's Character section.</span></span>
  

