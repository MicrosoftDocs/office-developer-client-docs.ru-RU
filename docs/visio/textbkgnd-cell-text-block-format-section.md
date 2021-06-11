---
title: TextBkgnd Cell (Text Block Format Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251267
localization_priority: Normal
ms.assetid: a238bf1c-1acd-eacd-22f3-a48acaaa4549
description: Определяет цвет фона текста для фигуры.
ms.openlocfilehash: 2450bf0cb0e013c0f9310eacfca0f5a20e7e6063
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33406544"
---
# <a name="textbkgnd-cell-text-block-format-section"></a><span data-ttu-id="4a272-103">TextBkgnd Cell (Text Block Format Section)</span><span class="sxs-lookup"><span data-stu-id="4a272-103">TextBkgnd Cell (Text Block Format Section)</span></span>

<span data-ttu-id="4a272-104">Определяет цвет фона текста для фигуры.</span><span class="sxs-lookup"><span data-stu-id="4a272-104">Determines the text background color for a shape.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="4a272-105">Примечания</span><span class="sxs-lookup"><span data-stu-id="4a272-105">Remarks</span></span>

<span data-ttu-id="4a272-106">Ячейка TextBkgnd может иметь любое значение от 0 до 24 или 255.</span><span class="sxs-lookup"><span data-stu-id="4a272-106">The TextBkgnd cell can have any value from 0 through 24, or 255.</span></span> <span data-ttu-id="4a272-107">Значения 0 и 255 *(visTxtBlklOpaque)* указывают на прозрачный текстовый фон.</span><span class="sxs-lookup"><span data-stu-id="4a272-107">The values 0 and 255 ( *visTxtBlklOpaque*) both indicate a transparent text background.</span></span> 
  
<span data-ttu-id="4a272-108">Чтобы ввести настраиваемый цвет, используйте функцию RGB или HSL плюс одну, например RGB (255 127 255)+1.</span><span class="sxs-lookup"><span data-stu-id="4a272-108">To enter a custom color, use the RGB or HSL function plus one—for example, RGB(255,127,255)+1.</span></span> <span data-ttu-id="4a272-109">Значение настраиваемого цвета — это цвет RGB, и RGB *(r, g, b*)+1, а не номер будут показаны в окне ShapeSheet.</span><span class="sxs-lookup"><span data-stu-id="4a272-109">The value of a custom color is its RGB color, and RGB( *r, g, b*)+1, rather than a number, will be shown in the ShapeSheet window.</span></span> <span data-ttu-id="4a272-110">Пользовательские цвета, используемые в числовом режиме, имеют значения 25 и выше.</span><span class="sxs-lookup"><span data-stu-id="4a272-110">When used in numeric operations, custom colors have values of 25 and above.</span></span> 
  
<span data-ttu-id="4a272-111">Можно установить прозрачность цвета фона текста в ячейке TextBkgndTrans.</span><span class="sxs-lookup"><span data-stu-id="4a272-111">You can set the transparency of the text background color in the TextBkgndTrans cell.</span></span>
  
<span data-ttu-id="4a272-112">Чтобы получить ссылку на ячейку TextBkgnd по имени из другой формулы или из программы с помощью свойства **CellsU,** используйте:</span><span class="sxs-lookup"><span data-stu-id="4a272-112">To get a reference to the TextBkgnd cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="4a272-113">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="4a272-113">Cell name:</span></span>  <br/> |<span data-ttu-id="4a272-114">TextBkgnd</span><span class="sxs-lookup"><span data-stu-id="4a272-114">TextBkgnd</span></span>  <br/> |
   
<span data-ttu-id="4a272-115">Чтобы получить ссылку на ячейку TextBkgnd по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="4a272-115">To get a reference to the TextBkgnd cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="4a272-116">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="4a272-116">Section index:</span></span>  <br/> |<span data-ttu-id="4a272-117">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="4a272-117">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="4a272-118">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="4a272-118">Row index:</span></span>  <br/> |<span data-ttu-id="4a272-119">**visRowText**</span><span class="sxs-lookup"><span data-stu-id="4a272-119">**visRowText**</span></span> <br/> |
|<span data-ttu-id="4a272-120">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="4a272-120">Cell index:</span></span>  <br/> |<span data-ttu-id="4a272-121">**visTxtBlkBkgnd**</span><span class="sxs-lookup"><span data-stu-id="4a272-121">**visTxtBlkBkgnd**</span></span> <br/> |
   

