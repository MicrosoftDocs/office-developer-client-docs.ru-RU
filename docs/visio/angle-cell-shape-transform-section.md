---
title: Angle Cell (Shape Transform Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251196
localization_priority: Normal
ms.assetid: d05a001c-9001-90d9-5028-f38b90acc53e
description: 'Представляет текущий угол вращения фигуры относительно родительского элемента. По умолчанию для определения угла вращения одномерной фигуры используется формула: = ATAN2 (Енди-Begin-EndX-BeginX).'
ms.openlocfilehash: 85f64c6111b492940d278a5558508a2dea6b1e1a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341470"
---
# <a name="angle-cell-shape-transform-section"></a><span data-ttu-id="6457e-104">Angle Cell (Shape Transform Section)</span><span class="sxs-lookup"><span data-stu-id="6457e-104">Angle Cell (Shape Transform Section)</span></span>

<span data-ttu-id="6457e-105">Представляет текущий угол вращения фигуры относительно родительского элемента.</span><span class="sxs-lookup"><span data-stu-id="6457e-105">Represents the shape's current angle of rotation in relation to its parent.</span></span> <span data-ttu-id="6457e-106">По умолчанию для определения угла вращения одномерной фигуры используется формула: = ATAN2 (Енди-Begin-EndX-BeginX).</span><span class="sxs-lookup"><span data-stu-id="6457e-106">The default formula for determining the rotation angle of a 1-D shape is: =ATAN2(EndY-BeginY,EndX-BeginX).</span></span>
  
## <a name="remarks"></a><span data-ttu-id="6457e-107">Комментарии</span><span class="sxs-lookup"><span data-stu-id="6457e-107">Remarks</span></span>

<span data-ttu-id="6457e-108">Чтобы получить ссылку на ячейку угла по имени из другой формулы или из программы с помощью свойства **CellsU** , используйте следующее:</span><span class="sxs-lookup"><span data-stu-id="6457e-108">To get a reference to the Angle cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="6457e-109">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="6457e-109">Cell name:</span></span>  <br/> | <span data-ttu-id="6457e-110">Угловая</span><span class="sxs-lookup"><span data-stu-id="6457e-110">Angle</span></span>  <br/> |
   
<span data-ttu-id="6457e-111">Чтобы получить ссылку на ячейку Angle по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="6457e-111">To get a reference to the Angle cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="6457e-112">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="6457e-112">Section index:</span></span>  <br/> |<span data-ttu-id="6457e-113">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="6457e-113">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="6457e-114">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="6457e-114">Row index:</span></span>  <br/> |<span data-ttu-id="6457e-115">**Висровксформаут**</span><span class="sxs-lookup"><span data-stu-id="6457e-115">**visRowXFormOut**</span></span> <br/> |
| <span data-ttu-id="6457e-116">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="6457e-116">Cell index:</span></span>  <br/> |<span data-ttu-id="6457e-117">**Висксформангле**</span><span class="sxs-lookup"><span data-stu-id="6457e-117">**visXFormAngle**</span></span> <br/> |
   

