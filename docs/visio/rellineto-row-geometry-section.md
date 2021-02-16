---
title: RelLineTo Row (Geometry Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: a900e174-d26a-4314-ae4f-d89e186350ce
description: Содержит координаты x и y конечной вершины сегмента прямой линии относительно ширины и высоты фигуры.
ms.openlocfilehash: 2e85033b4a2e16c2df09b1a09655fcd4b97dd03d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33437163"
---
# <a name="rellineto-row-geometry-section"></a><span data-ttu-id="e871c-103">RelLineTo Row (Geometry Section)</span><span class="sxs-lookup"><span data-stu-id="e871c-103">RelLineTo Row (Geometry Section)</span></span>

<span data-ttu-id="e871c-104">Содержит  *координаты*  x и  *y*  конечной вершины сегмента прямой линии относительно ширины и высоты фигуры.</span><span class="sxs-lookup"><span data-stu-id="e871c-104">Contains  *x*  -and  *y*  -coordinates of the ending vertex of a straight line segment relative to a shape's width and height.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="e871c-105">Строка **RelLineTo** может сохраняться только в форматах VSDX, VSDM, VSTX, VSTM, VSSX и VSSM.</span><span class="sxs-lookup"><span data-stu-id="e871c-105">A **RelLineTo** row can only be persisted in the .vsdx, .vsdm, .vstx, .vstm, .vssx, and .vssm file formats.</span></span> <span data-ttu-id="e871c-106">При сохранении файла в форматах Visio 2003-2010 строка **RelLineTo** преобразуется в [строку LineTo.](lineto-row-geometry-section.md)</span><span class="sxs-lookup"><span data-stu-id="e871c-106">When a file is saved to the Visio 2003-2010 formats, the **RelLineTo** row is converted to a [LineTo](lineto-row-geometry-section.md) row.</span></span> 
  
<span data-ttu-id="e871c-107">Строка **RelLineTo** содержит следующие ячейки.</span><span class="sxs-lookup"><span data-stu-id="e871c-107">A **RelLineTo** row contains the following cells.</span></span> 
  
|<span data-ttu-id="e871c-108">**Cell**</span><span class="sxs-lookup"><span data-stu-id="e871c-108">**Cell**</span></span>|<span data-ttu-id="e871c-109">**Описание**</span><span class="sxs-lookup"><span data-stu-id="e871c-109">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="e871c-110">X</span><span class="sxs-lookup"><span data-stu-id="e871c-110">X</span></span>](x-cell-geometry-section.md) <br/> |<span data-ttu-id="e871c-111">X-координата конечной вершины прямого сегмента относительно ширины фигуры. </span><span class="sxs-lookup"><span data-stu-id="e871c-111">The  *x*  -coordinate of the ending vertex of a straight line segment relative to the shape's width.</span></span>  <br/> |
|[<span data-ttu-id="e871c-112">Y</span><span class="sxs-lookup"><span data-stu-id="e871c-112">Y</span></span>](y-cell-geometry-section.md) <br/> |<span data-ttu-id="e871c-113">Координата  *Y*  конечной вершины сегмента прямой линии относительно высоты фигуры.</span><span class="sxs-lookup"><span data-stu-id="e871c-113">The  *y*  -coordinate of the ending vertex of a straight line segment relative to the shape's height.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e871c-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="e871c-114">Remarks</span></span>

<span data-ttu-id="e871c-115">Значения в строке **RelLineTo** эквивалентны значениям в строке [LineTo,](lineto-row-geometry-section.md) умноженным на ширину и высоту фигуры.</span><span class="sxs-lookup"><span data-stu-id="e871c-115">Values in the **RelLineTo** row are equivalent to values in a [LineTo](lineto-row-geometry-section.md) row that are multiplied by the width and height of the shape.</span></span> <span data-ttu-id="e871c-116">Например, строку **RelLineTo,** где значение ячейки **X** — "0", а значение ячейки **Y** — "0,5", можно заменить строкой **LineTo,** где значение ячейки **X** — это формула "Width 0", а ячейка ***Y***— формула "Height 0.5".</span><span class="sxs-lookup"><span data-stu-id="e871c-116">For example: a **RelLineTo** row where the value of the **X** cell is "0" and the value of the **Y** cell is "0.5" can be replaced with **LineTo** row where the value of the **X** cell is the formula "Width *0" and the **Y** cell is the formula "Height* 0.5."</span></span> 
  

