---
title: Строка RelLineTo (раздел "Геометрия")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: a900e174-d26a-4314-ae4f-d89e186350ce
description: Содержит x - и y-координаты окончания вершины отрезка прямой линии относительно ширины и высоты фигуры.
ms.openlocfilehash: 26cb63ac6cc0708be4e5668174022af63391c129
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19814564"
---
# <a name="rellineto-row-geometry-section"></a><span data-ttu-id="a42f5-103">Строка RelLineTo (раздел "Геометрия")</span><span class="sxs-lookup"><span data-stu-id="a42f5-103">RelLineTo Row (Geometry Section)</span></span>

<span data-ttu-id="a42f5-104">Содержит *x* - и *y* -координаты окончания вершины отрезка прямой линии относительно ширины и высоты фигуры.</span><span class="sxs-lookup"><span data-stu-id="a42f5-104">Contains  *x*  -and  *y*  -coordinates of the ending vertex of a straight line segment relative to a shape's width and height.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="a42f5-105">Строка **RelLineTo** только могут быть сохранены в форматы файлов vsdx (en), .vsdm, .vstx, .vstm, .vssx и .vssm.</span><span class="sxs-lookup"><span data-stu-id="a42f5-105">A **RelLineTo** row can only be persisted in the .vsdx, .vsdm, .vstx, .vstm, .vssx, and .vssm file formats.</span></span> <span data-ttu-id="a42f5-106">При сохранении файла в Visio 2003-2010 форматы строки **RelLineTo** преобразуется в строку [LineTo](lineto-row-geometry-section.md) .</span><span class="sxs-lookup"><span data-stu-id="a42f5-106">When a file is saved to the Visio 2003-2010 formats, the **RelLineTo** row is converted to a [LineTo](lineto-row-geometry-section.md) row.</span></span> 
  
<span data-ttu-id="a42f5-107">Строка **RelLineTo** содержит следующие ячейки.</span><span class="sxs-lookup"><span data-stu-id="a42f5-107">A **RelLineTo** row contains the following cells.</span></span> 
  
|<span data-ttu-id="a42f5-108">**Cell**</span><span class="sxs-lookup"><span data-stu-id="a42f5-108">**Cell**</span></span>|<span data-ttu-id="a42f5-109">**Описание**</span><span class="sxs-lookup"><span data-stu-id="a42f5-109">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="a42f5-110">X</span><span class="sxs-lookup"><span data-stu-id="a42f5-110">X</span></span>](x-cell-geometry-section.md) <br/> |<span data-ttu-id="a42f5-111">*X* -координаты окончания вершины сегмента прямой ширине фигуры.</span><span class="sxs-lookup"><span data-stu-id="a42f5-111">The  *x*  -coordinate of the ending vertex of a straight line segment relative to the shape's width.</span></span>  <br/> |
|[<span data-ttu-id="a42f5-112">Да</span><span class="sxs-lookup"><span data-stu-id="a42f5-112">Y</span></span>](y-cell-geometry-section.md) <br/> |<span data-ttu-id="a42f5-113">*Y* -координат окончания вершины сегмента прямой высоте фигуры.</span><span class="sxs-lookup"><span data-stu-id="a42f5-113">The  *y*  -coordinate of the ending vertex of a straight line segment relative to the shape's height.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a42f5-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="a42f5-114">Remarks</span></span>

<span data-ttu-id="a42f5-115">Значения в строке **RelLineTo** эквивалентны значения в строку [LineTo](lineto-row-geometry-section.md) , умноженное ширину и высоту фигуры.</span><span class="sxs-lookup"><span data-stu-id="a42f5-115">Values in the **RelLineTo** row are equivalent to values in a [LineTo](lineto-row-geometry-section.md) row that are multiplied by the width and height of the shape.</span></span> <span data-ttu-id="a42f5-116">Например: **RelLineTo** строку, где значение ячейки **X** — «0» и «0,5» имеет значение ячейки **Y** можно заменить **LineTo** строку, где значение ячейки **X** — это формула «ширина*0" и ячейки **Y** — это Формула «Высота*0,5.»</span><span class="sxs-lookup"><span data-stu-id="a42f5-116">For example: a **RelLineTo** row where the value of the **X** cell is "0" and the value of the **Y** cell is "0.5" can be replaced with **LineTo** row where the value of the **X** cell is the formula "Width*0" and the **Y** cell is the formula "Height*0.5."</span></span> 
  

