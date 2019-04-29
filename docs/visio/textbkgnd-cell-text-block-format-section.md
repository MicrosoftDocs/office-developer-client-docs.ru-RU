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
# <a name="textbkgnd-cell-text-block-format-section"></a><span data-ttu-id="d38cc-103">TextBkgnd Cell (Text Block Format Section)</span><span class="sxs-lookup"><span data-stu-id="d38cc-103">TextBkgnd Cell (Text Block Format Section)</span></span>

<span data-ttu-id="d38cc-104">Определяет цвет фона текста для фигуры.</span><span class="sxs-lookup"><span data-stu-id="d38cc-104">Determines the text background color for a shape.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="d38cc-105">Примечания</span><span class="sxs-lookup"><span data-stu-id="d38cc-105">Remarks</span></span>

<span data-ttu-id="d38cc-106">Ячейка TextBkgnd может иметь любое значение в диапазоне от 0 до 24 или 255.</span><span class="sxs-lookup"><span data-stu-id="d38cc-106">The TextBkgnd cell can have any value from 0 through 24, or 255.</span></span> <span data-ttu-id="d38cc-107">Значения 0 и 255 ( *висткстблклопакуе*) указывают на прозрачный фон текста.</span><span class="sxs-lookup"><span data-stu-id="d38cc-107">The values 0 and 255 ( *visTxtBlklOpaque*) both indicate a transparent text background.</span></span> 
  
<span data-ttu-id="d38cc-108">Чтобы ввести настраиваемый цвет, используйте функцию RGB или HSL, а другую — например, RGB (255127255) + 1.</span><span class="sxs-lookup"><span data-stu-id="d38cc-108">To enter a custom color, use the RGB or HSL function plus one—for example, RGB(255,127,255)+1.</span></span> <span data-ttu-id="d38cc-109">Значением настраиваемого цвета является цвет RGB, а RGB ( *r, g, b*) + 1, а не число, будет отображаться в окне таблицы свойств фигуры.</span><span class="sxs-lookup"><span data-stu-id="d38cc-109">The value of a custom color is its RGB color, and RGB( *r, g, b*)+1, rather than a number, will be shown in the ShapeSheet window.</span></span> <span data-ttu-id="d38cc-110">При использовании в числовых операциях дополнительные цвета имеют значения 25 и выше.</span><span class="sxs-lookup"><span data-stu-id="d38cc-110">When used in numeric operations, custom colors have values of 25 and above.</span></span> 
  
<span data-ttu-id="d38cc-111">Вы можете задать прозрачность цвета фона текста в ячейке TextBkgndTrans.</span><span class="sxs-lookup"><span data-stu-id="d38cc-111">You can set the transparency of the text background color in the TextBkgndTrans cell.</span></span>
  
<span data-ttu-id="d38cc-112">Чтобы получить ссылку на ячейку TextBkgnd по имени из другой формулы или из программы с помощью свойства **CellsU** , используйте следующее:</span><span class="sxs-lookup"><span data-stu-id="d38cc-112">To get a reference to the TextBkgnd cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="d38cc-113">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="d38cc-113">Cell name:</span></span>  <br/> |<span data-ttu-id="d38cc-114">TextBkgnd</span><span class="sxs-lookup"><span data-stu-id="d38cc-114">TextBkgnd</span></span>  <br/> |
   
<span data-ttu-id="d38cc-115">Чтобы получить ссылку на ячейку TextBkgnd по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="d38cc-115">To get a reference to the TextBkgnd cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="d38cc-116">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="d38cc-116">Section index:</span></span>  <br/> |<span data-ttu-id="d38cc-117">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="d38cc-117">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="d38cc-118">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="d38cc-118">Row index:</span></span>  <br/> |<span data-ttu-id="d38cc-119">**Висровтекст**</span><span class="sxs-lookup"><span data-stu-id="d38cc-119">**visRowText**</span></span> <br/> |
|<span data-ttu-id="d38cc-120">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="d38cc-120">Cell index:</span></span>  <br/> |<span data-ttu-id="d38cc-121">**Висткстблкбкгнд**</span><span class="sxs-lookup"><span data-stu-id="d38cc-121">**visTxtBlkBkgnd**</span></span> <br/> |
   

