---
title: FillBkgnd Cell (Fill Format Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm365
localization_priority: Normal
ms.assetid: 603d698f-a025-538c-8767-18e7716a9a5f
description: Определяет цвет, используемый для фона (заливки) узора заливки фигуры.
ms.openlocfilehash: f4df5d2b44a50380c996b9b2e0f7cda7d212093b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436645"
---
# <a name="fillbkgnd-cell-fill-format-section"></a><span data-ttu-id="a6128-103">FillBkgnd Cell (Fill Format Section)</span><span class="sxs-lookup"><span data-stu-id="a6128-103">FillBkgnd Cell (Fill Format Section)</span></span>

<span data-ttu-id="a6128-104">Определяет цвет, используемый для фона (заливки) узора заливки фигуры.</span><span class="sxs-lookup"><span data-stu-id="a6128-104">Determines the color used for the background (fill) of the shape's fill pattern.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="a6128-105">Примечания</span><span class="sxs-lookup"><span data-stu-id="a6128-105">Remarks</span></span>

<span data-ttu-id="a6128-106">Чтобы задать цвет, введите число от 0 до 23.</span><span class="sxs-lookup"><span data-stu-id="a6128-106">To set the color, enter a number from 0 to 23.</span></span>
  
<span data-ttu-id="a6128-107">Чтобы ввести настраиваемый цвет, используйте функцию RGB или HSL.</span><span class="sxs-lookup"><span data-stu-id="a6128-107">To enter a custom color, use the RGB or HSL function.</span></span> <span data-ttu-id="a6128-108">Значение настраиваемого цвета — это цвет RGB, а RGB (*r, g, b*), а не число, будут отображаться в окне таблицы свойств фигуры.</span><span class="sxs-lookup"><span data-stu-id="a6128-108">The value of a custom color is its RGB color, and RGB(*r, g, b*), rather than a number, will be shown in the ShapeSheet window.</span></span> <span data-ttu-id="a6128-109">При использовании в числовых операциях дополнительные цвета имеют значения 24 и выше.</span><span class="sxs-lookup"><span data-stu-id="a6128-109">When used in numeric operations, custom colors have values of 24 and above.</span></span> 
  
<span data-ttu-id="a6128-110">Вы можете задать прозрачность фоновой заливки в ячейке FillBkgndTrans.</span><span class="sxs-lookup"><span data-stu-id="a6128-110">You can set the transparency of the background fill in the FillBkgndTrans cell.</span></span> 
  
<span data-ttu-id="a6128-111">Чтобы получить ссылку на ячейку FillBkgnd по имени из другой формулы или из программы с помощью свойства **CellsU** , используйте следующее:</span><span class="sxs-lookup"><span data-stu-id="a6128-111">To get a reference to the FillBkgnd cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="a6128-112">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="a6128-112">Cell name:</span></span>  <br/> | <span data-ttu-id="a6128-113">FillBkgnd</span><span class="sxs-lookup"><span data-stu-id="a6128-113">FillBkgnd</span></span>  <br/> |
   
<span data-ttu-id="a6128-114">Чтобы получить ссылку на ячейку FillBkgnd по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="a6128-114">To get a reference to the FillBkgnd cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="a6128-115">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="a6128-115">Section index:</span></span>  <br/> |<span data-ttu-id="a6128-116">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="a6128-116">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="a6128-117">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="a6128-117">Row index:</span></span>  <br/> |<span data-ttu-id="a6128-118">**Висровфилл**</span><span class="sxs-lookup"><span data-stu-id="a6128-118">**visRowFill**</span></span> <br/> |
| <span data-ttu-id="a6128-119">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="a6128-119">Cell index:</span></span>  <br/> |<span data-ttu-id="a6128-120">**Висфиллбкгнд**</span><span class="sxs-lookup"><span data-stu-id="a6128-120">**visFillBkgnd**</span></span> <br/> |
   

