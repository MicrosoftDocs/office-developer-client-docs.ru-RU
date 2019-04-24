---
title: ShdwForegnd Cell (Fill Format Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251244
localization_priority: Normal
ms.assetid: ea153390-631d-79fd-c1ba-4c281239a24e
description: Определяет цвет, используемый для переднего плана (штриха) узора заливки тени фигуры.
ms.openlocfilehash: 602df83dcb88d4137b0609f9a8b1084a40148a10
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32349107"
---
# <a name="shdwforegnd-cell-fill-format-section"></a><span data-ttu-id="2e319-103">ShdwForegnd Cell (Fill Format Section)</span><span class="sxs-lookup"><span data-stu-id="2e319-103">ShdwForegnd Cell (Fill Format Section)</span></span>

<span data-ttu-id="2e319-104">Определяет цвет, используемый для переднего плана (штриха) узора заливки тени фигуры.</span><span class="sxs-lookup"><span data-stu-id="2e319-104">Determines the color used for the foreground (stroke) of the shape's drop shadow fill pattern.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="2e319-105">Примечания</span><span class="sxs-lookup"><span data-stu-id="2e319-105">Remarks</span></span>

<span data-ttu-id="2e319-106">Чтобы задать цвет, введите число в диапазоне от 0 до 23, которое представляет собой индекс в наборе цветов.</span><span class="sxs-lookup"><span data-stu-id="2e319-106">To set the color, enter a number from 0 to 23, which is an index into a collection of colors.</span></span>
  
<span data-ttu-id="2e319-107">Чтобы ввести настраиваемый цвет, используйте функцию RGB или HSL.</span><span class="sxs-lookup"><span data-stu-id="2e319-107">To enter a custom color, use the RGB or HSL function.</span></span> <span data-ttu-id="2e319-108">Значение настраиваемого цвета — это цвет RGB, а RGB ( *r, g, b*), а не число, будут отображаться в окне таблицы свойств фигуры.</span><span class="sxs-lookup"><span data-stu-id="2e319-108">The value of a custom color is its RGB color, and RGB( *r, g, b*), rather than a number, will be shown in the ShapeSheet window.</span></span> <span data-ttu-id="2e319-109">При использовании в числовых операциях дополнительные цвета имеют значения 24 и выше.</span><span class="sxs-lookup"><span data-stu-id="2e319-109">When used in numeric operations, custom colors have values of 24 and above.</span></span> 
  
<span data-ttu-id="2e319-110">Вы можете задать прозрачность цвета переднего плана для узорной заливки тени фигуры в ячейке ShdwForegndTrans.</span><span class="sxs-lookup"><span data-stu-id="2e319-110">You can set the transparency of the foreground color of the shape's drop shadow fill pattern in the ShdwForegndTrans cell.</span></span>
  
<span data-ttu-id="2e319-111">Чтобы получить ссылку на ячейку ShdwForegnd по имени из другой формулы или из программы с помощью свойства **CellsU** , используйте следующее:</span><span class="sxs-lookup"><span data-stu-id="2e319-111">To get a reference to the ShdwForegnd cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="2e319-112">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="2e319-112">Cell name:</span></span>  <br/> | <span data-ttu-id="2e319-113">ShdwForegnd</span><span class="sxs-lookup"><span data-stu-id="2e319-113">ShdwForegnd</span></span>  <br/> |
   
<span data-ttu-id="2e319-114">Чтобы получить ссылку на ячейку ShdwForegnd по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="2e319-114">To get a reference to the ShdwForegnd cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="2e319-115">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="2e319-115">Section index:</span></span>  <br/> |<span data-ttu-id="2e319-116">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="2e319-116">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="2e319-117">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="2e319-117">Row index:</span></span>  <br/> |<span data-ttu-id="2e319-118">**Висровфилл**</span><span class="sxs-lookup"><span data-stu-id="2e319-118">**visRowFill**</span></span> <br/> |
| <span data-ttu-id="2e319-119">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="2e319-119">Cell index:</span></span>  <br/> |<span data-ttu-id="2e319-120">**Висфиллшдвфорегнд**</span><span class="sxs-lookup"><span data-stu-id="2e319-120">**visFillShdwForegnd**</span></span> <br/> |
   

