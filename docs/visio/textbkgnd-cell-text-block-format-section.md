---
title: Ячейка TextBkgnd (раздел формат блока текст)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251267
localization_priority: Normal
ms.assetid: a238bf1c-1acd-eacd-22f3-a48acaaa4549
description: Определяет цвет фона текста для фигуры.
ms.openlocfilehash: 2256a4c89812924af820c020c225f4b82b1d4856
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19815018"
---
# <a name="textbkgnd-cell-text-block-format-section"></a><span data-ttu-id="40923-103">Ячейка TextBkgnd (раздел формат блока текст)</span><span class="sxs-lookup"><span data-stu-id="40923-103">TextBkgnd Cell (Text Block Format Section)</span></span>

<span data-ttu-id="40923-104">Определяет цвет фона текста для фигуры.</span><span class="sxs-lookup"><span data-stu-id="40923-104">Determines the text background color for a shape.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="40923-105">Замечания</span><span class="sxs-lookup"><span data-stu-id="40923-105">Remarks</span></span>

<span data-ttu-id="40923-106">Ячейка TextBkgnd может иметь любое значение от 0 до 24 или 255.</span><span class="sxs-lookup"><span data-stu-id="40923-106">The TextBkgnd cell can have any value from 0 through 24, or 255.</span></span> <span data-ttu-id="40923-107">0 до 255 ( *visTxtBlklOpaque*), то это означает фон прозрачным текста.</span><span class="sxs-lookup"><span data-stu-id="40923-107">The values 0 and 255 ( *visTxtBlklOpaque*) both indicate a transparent text background.</span></span> 
  
<span data-ttu-id="40923-108">Чтобы ввести другой цвет, используйте функции RGB или HSL, а также один — например, RGB (255,127,255) + 1.</span><span class="sxs-lookup"><span data-stu-id="40923-108">To enter a custom color, use the RGB or HSL function plus one—for example, RGB(255,127,255)+1.</span></span> <span data-ttu-id="40923-109">Настраиваемые цвета значение цвета RGB, а RGB ( *r, g, b*) + 1, а не числа, будут отображаться в окне таблицы свойств фигуры.</span><span class="sxs-lookup"><span data-stu-id="40923-109">The value of a custom color is its RGB color, and RGB( *r, g, b*)+1, rather than a number, will be shown in the ShapeSheet window.</span></span> <span data-ttu-id="40923-110">При использовании в операции, настраиваемые цвета имеют значения 25 и выше.</span><span class="sxs-lookup"><span data-stu-id="40923-110">When used in numeric operations, custom colors have values of 25 and above.</span></span> 
  
<span data-ttu-id="40923-111">Можно задать прозрачность цвет фона текст в ячейке TextBkgndTrans.</span><span class="sxs-lookup"><span data-stu-id="40923-111">You can set the transparency of the text background color in the TextBkgndTrans cell.</span></span>
  
<span data-ttu-id="40923-112">Чтобы получить ссылку на ячейку TextBkgnd по имени из другой формулы или из файла с помощью свойства **CellsU** , используйте:</span><span class="sxs-lookup"><span data-stu-id="40923-112">To get a reference to the TextBkgnd cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="40923-113">Имя ячейки.</span><span class="sxs-lookup"><span data-stu-id="40923-113">Cell name:</span></span>  <br/> |<span data-ttu-id="40923-114">TextBkgnd</span><span class="sxs-lookup"><span data-stu-id="40923-114">TextBkgnd</span></span>  <br/> |
   
<span data-ttu-id="40923-115">Для получения ссылки на ячейки TextBkgnd по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы:</span><span class="sxs-lookup"><span data-stu-id="40923-115">To get a reference to the TextBkgnd cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="40923-116">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="40923-116">Section index:</span></span>  <br/> |<span data-ttu-id="40923-117">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="40923-117">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="40923-118">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="40923-118">Row index:</span></span>  <br/> |<span data-ttu-id="40923-119">**visRowText**</span><span class="sxs-lookup"><span data-stu-id="40923-119">**visRowText**</span></span> <br/> |
|<span data-ttu-id="40923-120">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="40923-120">Cell index:</span></span>  <br/> |<span data-ttu-id="40923-121">**visTxtBlkBkgnd**</span><span class="sxs-lookup"><span data-stu-id="40923-121">**visTxtBlkBkgnd**</span></span> <br/> |
   

