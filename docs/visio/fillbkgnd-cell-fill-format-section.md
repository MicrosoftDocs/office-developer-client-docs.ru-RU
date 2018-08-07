---
title: Ячейка FillBkgnd (раздел "Формат заливки")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm365
localization_priority: Normal
ms.assetid: 603d698f-a025-538c-8767-18e7716a9a5f
description: Определяет цвет, используемый в качестве фона (заливки) узора заливки фигуры.
ms.openlocfilehash: d1222026887313d7737a3a0ded9e798e9bf5ea30
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19813748"
---
# <a name="fillbkgnd-cell-fill-format-section"></a><span data-ttu-id="e0fdf-103">Ячейка FillBkgnd (раздел "Формат заливки")</span><span class="sxs-lookup"><span data-stu-id="e0fdf-103">FillBkgnd Cell (Fill Format Section)</span></span>

<span data-ttu-id="e0fdf-104">Определяет цвет, используемый в качестве фона (заливки) узора заливки фигуры.</span><span class="sxs-lookup"><span data-stu-id="e0fdf-104">Determines the color used for the background (fill) of the shape's fill pattern.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="e0fdf-105">Замечания</span><span class="sxs-lookup"><span data-stu-id="e0fdf-105">Remarks</span></span>

<span data-ttu-id="e0fdf-106">Чтобы задать цвет, введите число от 0 до 23.</span><span class="sxs-lookup"><span data-stu-id="e0fdf-106">To set the color, enter a number from 0 to 23.</span></span>
  
<span data-ttu-id="e0fdf-107">Чтобы ввести другой цвет, используйте функцию RGB или HSL.</span><span class="sxs-lookup"><span data-stu-id="e0fdf-107">To enter a custom color, use the RGB or HSL function.</span></span> <span data-ttu-id="e0fdf-108">Настраиваемые цвета значение цвета RGB, а RGB (*r, g, b*), а не числа, будут отображаться в окне таблицы свойств фигуры.</span><span class="sxs-lookup"><span data-stu-id="e0fdf-108">The value of a custom color is its RGB color, and RGB(*r, g, b*), rather than a number, will be shown in the ShapeSheet window.</span></span> <span data-ttu-id="e0fdf-109">При использовании в операции, настраиваемые цвета имеют значения из 24 и выше.</span><span class="sxs-lookup"><span data-stu-id="e0fdf-109">When used in numeric operations, custom colors have values of 24 and above.</span></span> 
  
<span data-ttu-id="e0fdf-110">Можно задать Прозрачность заливки фона в ячейке FillBkgndTrans.</span><span class="sxs-lookup"><span data-stu-id="e0fdf-110">You can set the transparency of the background fill in the FillBkgndTrans cell.</span></span> 
  
<span data-ttu-id="e0fdf-111">Чтобы получить ссылку на ячейку FillBkgnd по имени из другой формулы, и программы, с помощью свойства **CellsU** , используйте следующую команду:</span><span class="sxs-lookup"><span data-stu-id="e0fdf-111">To get a reference to the FillBkgnd cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="e0fdf-112">Имя ячейки.</span><span class="sxs-lookup"><span data-stu-id="e0fdf-112">Cell name:</span></span>  <br/> | <span data-ttu-id="e0fdf-113">FillBkgnd</span><span class="sxs-lookup"><span data-stu-id="e0fdf-113">FillBkgnd</span></span>  <br/> |
   
<span data-ttu-id="e0fdf-114">Для получения ссылки на ячейки FillBkgnd по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы:</span><span class="sxs-lookup"><span data-stu-id="e0fdf-114">To get a reference to the FillBkgnd cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="e0fdf-115">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="e0fdf-115">Section index:</span></span>  <br/> |<span data-ttu-id="e0fdf-116">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="e0fdf-116">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="e0fdf-117">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="e0fdf-117">Row index:</span></span>  <br/> |<span data-ttu-id="e0fdf-118">**visRowFill**</span><span class="sxs-lookup"><span data-stu-id="e0fdf-118">**visRowFill**</span></span> <br/> |
| <span data-ttu-id="e0fdf-119">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="e0fdf-119">Cell index:</span></span>  <br/> |<span data-ttu-id="e0fdf-120">**visFillBkgnd**</span><span class="sxs-lookup"><span data-stu-id="e0fdf-120">**visFillBkgnd**</span></span> <br/> |
   

