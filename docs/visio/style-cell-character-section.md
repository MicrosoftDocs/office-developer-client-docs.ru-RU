---
title: Ячейка Style (раздел "Символ")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251249
localization_priority: Normal
ms.assetid: 4372f1e1-f0a9-2f63-ff79-58f2afdceed5
description: Отображает формат символов, применяемый к диапазону текста в блоке текста фигуры.
ms.openlocfilehash: 48bda5eb798f439e2616b2b910d7ec5ac719d060
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19814946"
---
# <a name="style-cell-character-section"></a><span data-ttu-id="4913c-103">Ячейка Style (раздел "Символ")</span><span class="sxs-lookup"><span data-stu-id="4913c-103">Style Cell (Character Section)</span></span>

<span data-ttu-id="4913c-104">Отображает формат символов, применяемый к диапазону текста в блоке текста фигуры.</span><span class="sxs-lookup"><span data-stu-id="4913c-104">Shows the character formatting applied to a range of text in the shape's text block.</span></span>
  
|<span data-ttu-id="4913c-105">**Стиль**</span><span class="sxs-lookup"><span data-stu-id="4913c-105">**Style**</span></span>|<span data-ttu-id="4913c-106">**Значение**</span><span class="sxs-lookup"><span data-stu-id="4913c-106">**Value**</span></span>|<span data-ttu-id="4913c-107">**Константа автоматизации**</span><span class="sxs-lookup"><span data-stu-id="4913c-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
| <span data-ttu-id="4913c-108">Полужирный</span><span class="sxs-lookup"><span data-stu-id="4913c-108">Bold</span></span>  <br/> | <span data-ttu-id="4913c-109">&amp;H1</span><span class="sxs-lookup"><span data-stu-id="4913c-109">&amp;H1</span></span>  <br/> |<span data-ttu-id="4913c-110">**visBold**</span><span class="sxs-lookup"><span data-stu-id="4913c-110">**visBold**</span></span> <br/> |
| <span data-ttu-id="4913c-111">Курсив</span><span class="sxs-lookup"><span data-stu-id="4913c-111">Italic</span></span>  <br/> | <span data-ttu-id="4913c-112">&amp;H2</span><span class="sxs-lookup"><span data-stu-id="4913c-112">&amp;H2</span></span>  <br/> |<span data-ttu-id="4913c-113">**visItalic**</span><span class="sxs-lookup"><span data-stu-id="4913c-113">**visItalic**</span></span> <br/> |
| <span data-ttu-id="4913c-114">Подчеркивание</span><span class="sxs-lookup"><span data-stu-id="4913c-114">Underline</span></span>  <br/> | <span data-ttu-id="4913c-115">&amp;H4</span><span class="sxs-lookup"><span data-stu-id="4913c-115">&amp;H4</span></span>  <br/> |<span data-ttu-id="4913c-116">**visUnderLine**</span><span class="sxs-lookup"><span data-stu-id="4913c-116">**visUnderLine**</span></span> <br/> |
| <span data-ttu-id="4913c-117">Малые прописные</span><span class="sxs-lookup"><span data-stu-id="4913c-117">Small caps</span></span>  <br/> | <span data-ttu-id="4913c-118">&amp;H8</span><span class="sxs-lookup"><span data-stu-id="4913c-118">&amp;H8</span></span>  <br/> |<span data-ttu-id="4913c-119">**visSmallCaps**</span><span class="sxs-lookup"><span data-stu-id="4913c-119">**visSmallCaps**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="4913c-120">Замечания</span><span class="sxs-lookup"><span data-stu-id="4913c-120">Remarks</span></span>

<span data-ttu-id="4913c-121">Стиль ячейки содержит сведения о форматировании применяется поддиапазона текстом фигуры в том случае, если в разделе символов содержит несколько строк.</span><span class="sxs-lookup"><span data-stu-id="4913c-121">The Style cell contains formatting information applied to a sub-range of a shape's text if the Characters section contains multiple rows.</span></span> <span data-ttu-id="4913c-122">В противном случае содержит сведения о форматировании для всех текста фигуры.</span><span class="sxs-lookup"><span data-stu-id="4913c-122">Otherwise, it contains formatting information for all of the shape's text.</span></span>
  
<span data-ttu-id="4913c-123">Значение представляет двоичное число, в котором каждый бит указывает стиль знака.</span><span class="sxs-lookup"><span data-stu-id="4913c-123">The value represents a binary number in which each bit indicates a character style.</span></span> <span data-ttu-id="4913c-124">Например значение 3 представляет текст, отформатированный в курсивом и полужирным шрифтом.</span><span class="sxs-lookup"><span data-stu-id="4913c-124">For example, a value of 3 represents text formatted in both italic and bold.</span></span> <span data-ttu-id="4913c-125">Если значение стиля равно 0, текст обычная или неформатированный.</span><span class="sxs-lookup"><span data-stu-id="4913c-125">If the value of Style is 0, the text is plain, or unformatted.</span></span> <span data-ttu-id="4913c-126">Вы можете проверить для определенного формата, с помощью типа Boolean бит\* функции.</span><span class="sxs-lookup"><span data-stu-id="4913c-126">You can test for a particular format using Boolean BIT\* functions.</span></span> <span data-ttu-id="4913c-127">Обратитесь к документации программирования для получения дополнительных сведений об этих функций.</span><span class="sxs-lookup"><span data-stu-id="4913c-127">See your programming documentation for details about these functions.</span></span>
  
<span data-ttu-id="4913c-128">Чтобы получить ссылку на стиль ячейки по имени из другой формулы, и программы, с помощью свойства **CellsU** , используйте следующую команду:</span><span class="sxs-lookup"><span data-stu-id="4913c-128">To get a reference to the Style cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="4913c-129">Имя ячейки.</span><span class="sxs-lookup"><span data-stu-id="4913c-129">Cell name:</span></span>  <br/> | <span data-ttu-id="4913c-130">Char.Style [ *i* ] где *i* = < 1 > 2, 3...</span><span class="sxs-lookup"><span data-stu-id="4913c-130">Char.Style[  *i*  ]            where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="4913c-131">Для получения ссылки на ячейки стиль по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы:</span><span class="sxs-lookup"><span data-stu-id="4913c-131">To get a reference to the Style cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="4913c-132">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="4913c-132">Section index:</span></span>  <br/> |<span data-ttu-id="4913c-133">**visSectionCharacter**</span><span class="sxs-lookup"><span data-stu-id="4913c-133">**visSectionCharacter**</span></span> <br/> |
| <span data-ttu-id="4913c-134">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="4913c-134">Row index:</span></span>  <br/> |<span data-ttu-id="4913c-135">**visRowCharacter** +  *i* где *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="4913c-135">**visRowCharacter** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="4913c-136">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="4913c-136">Cell index:</span></span>  <br/> |<span data-ttu-id="4913c-137">**visCharacterStyle**</span><span class="sxs-lookup"><span data-stu-id="4913c-137">**visCharacterStyle**</span></span> <br/> |
   
 <span data-ttu-id="4913c-138">*Пример*</span><span class="sxs-lookup"><span data-stu-id="4913c-138">*Example*</span></span> 
  
<span data-ttu-id="4913c-139">Предположим, что цвета ячеек в первой строке раздел знаков фигуры задано значение эту формулу:</span><span class="sxs-lookup"><span data-stu-id="4913c-139">Suppose the Color cell in the first row of a shape's Character section is set to this formula:</span></span>
  
<span data-ttu-id="4913c-140">= IF(BITAND(Char.Style,1)=1,4,3)</span><span class="sxs-lookup"><span data-stu-id="4913c-140">= IF(BITAND(Char.Style,1)=1,4,3)</span></span>
  
<span data-ttu-id="4913c-141">Если заглавной фигуры текст полужирным шрифтом, текст, к которому применяется первой строки свойства символ будет синий (4); в противном случае будет отображаться зеленым цветом (3).</span><span class="sxs-lookup"><span data-stu-id="4913c-141">Then if the first character of the shape's text is bold, the text covered by the first Character properties row will be blue (4); otherwise it will be green (3).</span></span> <span data-ttu-id="4913c-142">В этом примере предполагается, что цвета по умолчанию вступают в силу.</span><span class="sxs-lookup"><span data-stu-id="4913c-142">This example assumes default colors are in effect.</span></span>
  
<span data-ttu-id="4913c-143">Ниже приведен пример настройки стилей ячеек в программу.</span><span class="sxs-lookup"><span data-stu-id="4913c-143">The following is an example of setting the Style cell in a program.</span></span> <span data-ttu-id="4913c-144">Первый оператор ссылается на ячейку стиль по имени, а вторая инструкция ссылается на ячейку стиль по индексу.</span><span class="sxs-lookup"><span data-stu-id="4913c-144">The first statement references the Style cell by name, and the second statement references the Style cell by index.</span></span> <span data-ttu-id="4913c-145">Оба italic особенности текст, к которому применяется второй строке раздел знаков фигуры.</span><span class="sxs-lookup"><span data-stu-id="4913c-145">Both statements apply italic to the text covered by the second row of a shape's Character section.</span></span>
  

