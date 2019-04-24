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
description: Показывает форматирование символов, применяемое к диапазону текста в блоке текста фигуры.
ms.openlocfilehash: 349bdc42485aa511011aeb85a43f1ab3e4ea853d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32329813"
---
# <a name="style-cell-character-section"></a><span data-ttu-id="b882c-103">Style Cell (Character Section)</span><span class="sxs-lookup"><span data-stu-id="b882c-103">Style Cell (Character Section)</span></span>

<span data-ttu-id="b882c-104">Показывает форматирование символов, применяемое к диапазону текста в блоке текста фигуры.</span><span class="sxs-lookup"><span data-stu-id="b882c-104">Shows the character formatting applied to a range of text in the shape's text block.</span></span>
  
|<span data-ttu-id="b882c-105">**Style**</span><span class="sxs-lookup"><span data-stu-id="b882c-105">**Style**</span></span>|<span data-ttu-id="b882c-106">**Значение**</span><span class="sxs-lookup"><span data-stu-id="b882c-106">**Value**</span></span>|<span data-ttu-id="b882c-107">**Константа автоматизации**</span><span class="sxs-lookup"><span data-stu-id="b882c-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
| <span data-ttu-id="b882c-108">Полужирный</span><span class="sxs-lookup"><span data-stu-id="b882c-108">Bold</span></span>  <br/> | <span data-ttu-id="b882c-109">&amp;H1</span><span class="sxs-lookup"><span data-stu-id="b882c-109">&amp;H1</span></span>  <br/> |<span data-ttu-id="b882c-110">**Висболд**</span><span class="sxs-lookup"><span data-stu-id="b882c-110">**visBold**</span></span> <br/> |
| <span data-ttu-id="b882c-111">Курсив</span><span class="sxs-lookup"><span data-stu-id="b882c-111">Italic</span></span>  <br/> | <span data-ttu-id="b882c-112">&amp;H2</span><span class="sxs-lookup"><span data-stu-id="b882c-112">&amp;H2</span></span>  <br/> |<span data-ttu-id="b882c-113">**Виситалик**</span><span class="sxs-lookup"><span data-stu-id="b882c-113">**visItalic**</span></span> <br/> |
| <span data-ttu-id="b882c-114">Подчеркнутый</span><span class="sxs-lookup"><span data-stu-id="b882c-114">Underline</span></span>  <br/> | <span data-ttu-id="b882c-115">&amp;H4</span><span class="sxs-lookup"><span data-stu-id="b882c-115">&amp;H4</span></span>  <br/> |<span data-ttu-id="b882c-116">**Висундерлине**</span><span class="sxs-lookup"><span data-stu-id="b882c-116">**visUnderLine**</span></span> <br/> |
| <span data-ttu-id="b882c-117">Малые прописные</span><span class="sxs-lookup"><span data-stu-id="b882c-117">Small caps</span></span>  <br/> | <span data-ttu-id="b882c-118">&amp;H8</span><span class="sxs-lookup"><span data-stu-id="b882c-118">&amp;H8</span></span>  <br/> |<span data-ttu-id="b882c-119">**Виссмаллкапс**</span><span class="sxs-lookup"><span data-stu-id="b882c-119">**visSmallCaps**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b882c-120">Комментарии</span><span class="sxs-lookup"><span data-stu-id="b882c-120">Remarks</span></span>

<span data-ttu-id="b882c-121">Ячейка style содержит сведения о форматировании, примененные к поддиапазону текста фигуры, если раздел символы содержит несколько строк.</span><span class="sxs-lookup"><span data-stu-id="b882c-121">The Style cell contains formatting information applied to a sub-range of a shape's text if the Characters section contains multiple rows.</span></span> <span data-ttu-id="b882c-122">В противном случае он содержит сведения о форматировании для всего текста фигуры.</span><span class="sxs-lookup"><span data-stu-id="b882c-122">Otherwise, it contains formatting information for all of the shape's text.</span></span>
  
<span data-ttu-id="b882c-123">Значение представляет двоичное число, в котором каждый бит указывает на стиль символа.</span><span class="sxs-lookup"><span data-stu-id="b882c-123">The value represents a binary number in which each bit indicates a character style.</span></span> <span data-ttu-id="b882c-124">Например, значение 3 представляет текст, отформатированный курсивом и полужирным шрифтом.</span><span class="sxs-lookup"><span data-stu-id="b882c-124">For example, a value of 3 represents text formatted in both italic and bold.</span></span> <span data-ttu-id="b882c-125">Если значение style равно 0, текст является простым или неформатированным.</span><span class="sxs-lookup"><span data-stu-id="b882c-125">If the value of Style is 0, the text is plain, or unformatted.</span></span> <span data-ttu-id="b882c-126">Вы можете проверить определенный формат, используя логические\* функции.</span><span class="sxs-lookup"><span data-stu-id="b882c-126">You can test for a particular format using Boolean BIT\* functions.</span></span> <span data-ttu-id="b882c-127">Сведения об этих функциях можно найти в документации по программированию.</span><span class="sxs-lookup"><span data-stu-id="b882c-127">See your programming documentation for details about these functions.</span></span>
  
<span data-ttu-id="b882c-128">Чтобы получить ссылку на ячейку Style по имени из другой формулы или из программы с помощью свойства **CellsU** , используйте:</span><span class="sxs-lookup"><span data-stu-id="b882c-128">To get a reference to the Style cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="b882c-129">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="b882c-129">Cell name:</span></span>  <br/> | <span data-ttu-id="b882c-130">Char. Style [ *i* ], где *i* = <1>, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="b882c-130">Char.Style[  *i*  ]            where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="b882c-131">Чтобы получить ссылку на ячейку Style по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="b882c-131">To get a reference to the Style cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="b882c-132">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="b882c-132">Section index:</span></span>  <br/> |<span data-ttu-id="b882c-133">**Виссектиончарактер**</span><span class="sxs-lookup"><span data-stu-id="b882c-133">**visSectionCharacter**</span></span> <br/> |
| <span data-ttu-id="b882c-134">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="b882c-134">Row index:</span></span>  <br/> |<span data-ttu-id="b882c-135">**висровчарактер** +  *i* , где *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="b882c-135">**visRowCharacter** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="b882c-136">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="b882c-136">Cell index:</span></span>  <br/> |<span data-ttu-id="b882c-137">**Висчарактерстиле**</span><span class="sxs-lookup"><span data-stu-id="b882c-137">**visCharacterStyle**</span></span> <br/> |
   
 <span data-ttu-id="b882c-138">*Пример*</span><span class="sxs-lookup"><span data-stu-id="b882c-138">*Example*</span></span> 
  
<span data-ttu-id="b882c-139">Предположим, что ячейка Color в первой строке раздела символов фигуры имеет значение, равное следующей формуле:</span><span class="sxs-lookup"><span data-stu-id="b882c-139">Suppose the Color cell in the first row of a shape's Character section is set to this formula:</span></span>
  
<span data-ttu-id="b882c-140">= IF (бит. И (char. Style, 1) = 1, 4, 3)</span><span class="sxs-lookup"><span data-stu-id="b882c-140">= IF(BITAND(Char.Style,1)=1,4,3)</span></span>
  
<span data-ttu-id="b882c-141">Затем, если первый символ текста фигуры выделен полужирным шрифтом, текст, покрываемый первой строкой свойств символов, будет синим (4). в противном случае он будет зеленым (3).</span><span class="sxs-lookup"><span data-stu-id="b882c-141">Then if the first character of the shape's text is bold, the text covered by the first Character properties row will be blue (4); otherwise it will be green (3).</span></span> <span data-ttu-id="b882c-142">В этом примере предполагается, что действуют цвета, используемые по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="b882c-142">This example assumes default colors are in effect.</span></span>
  
<span data-ttu-id="b882c-143">Ниже приведен пример установки ячейки Style в программе.</span><span class="sxs-lookup"><span data-stu-id="b882c-143">The following is an example of setting the Style cell in a program.</span></span> <span data-ttu-id="b882c-144">Первый оператор ссылается на ячейку Style по имени, а второй оператор ссылается на ячейку Style по индексу.</span><span class="sxs-lookup"><span data-stu-id="b882c-144">The first statement references the Style cell by name, and the second statement references the Style cell by index.</span></span> <span data-ttu-id="b882c-145">Оба оператора Применяют курсив к тексту, который охватывает вторая строка раздела символов фигуры.</span><span class="sxs-lookup"><span data-stu-id="b882c-145">Both statements apply italic to the text covered by the second row of a shape's Character section.</span></span>
  

