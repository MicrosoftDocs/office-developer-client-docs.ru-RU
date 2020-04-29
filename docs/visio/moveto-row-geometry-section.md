---
title: MoveTo Row (Geometry Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm3030
localization_priority: Normal
ms.assetid: c5b20257-676c-279d-f730-1b6fbbe98305
description: Содержит координаты x и y первой вершины фигуры или представляет координаты x и y первой вершины после разрыва в контуре.
ms.openlocfilehash: fc414093348b8da04fa3503053584395976982dd
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33429700"
---
# <a name="moveto-row-geometry-section"></a><span data-ttu-id="9a718-103">MoveTo Row (Geometry Section)</span><span class="sxs-lookup"><span data-stu-id="9a718-103">MoveTo Row (Geometry Section)</span></span>

<span data-ttu-id="9a718-104">Содержит координаты *x* и *y* первой вершины фигуры или представляет координаты *x* и *y* первой вершины после разрыва в контуре.</span><span class="sxs-lookup"><span data-stu-id="9a718-104">Contains the  *x*  - and  *y*  -coordinates of the first vertex of a shape, or represents the  *x*  - and  *y*  -coordinates of the first vertex after a break in a path.</span></span> 
  
<span data-ttu-id="9a718-105">Строка **MoveTo** содержит следующие ячейки.</span><span class="sxs-lookup"><span data-stu-id="9a718-105">A **MoveTo** row contains the following cells.</span></span> 
  
|<span data-ttu-id="9a718-106">**Cell**</span><span class="sxs-lookup"><span data-stu-id="9a718-106">**Cell**</span></span>|<span data-ttu-id="9a718-107">**Описание**</span><span class="sxs-lookup"><span data-stu-id="9a718-107">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="9a718-108">X</span><span class="sxs-lookup"><span data-stu-id="9a718-108">X</span></span>](x-cell-geometry-section.md) <br/> |<span data-ttu-id="9a718-109">Если строка **MoveTo** находится в первой строке раздела, то ячейка x представляет координату *x* первой вершины фигуры.</span><span class="sxs-lookup"><span data-stu-id="9a718-109">If the **MoveTo** row is the first row in the section, the X cell represents the  *x*  -coordinate of the first vertex of a shape.</span></span> <span data-ttu-id="9a718-110">Если строка **MoveTo** находится между двумя строками, ячейка x представляет координату *x* первой вершины после разрыва в пути.</span><span class="sxs-lookup"><span data-stu-id="9a718-110">If the **MoveTo** row appears between two rows, the X cell represents the  *x*  -coordinate of the first vertex after the break in the path.</span></span>  <br/> |
|[<span data-ttu-id="9a718-111">Y (да)</span><span class="sxs-lookup"><span data-stu-id="9a718-111">Y</span></span>](y-cell-geometry-section.md) <br/> |<span data-ttu-id="9a718-112">Если строка **MoveTo** находится в первой строке раздела, то ячейка y представляет координату *y* первой вершины фигуры.</span><span class="sxs-lookup"><span data-stu-id="9a718-112">If the **MoveTo** row is the first row in the section, the Y cell represents the  *y*  -coordinate of the first vertex of a shape.</span></span> <span data-ttu-id="9a718-113">Если строка **MoveTo** находится между двумя строками, ячейка y представляет координату *y* первой вершины после разрыва в пути.</span><span class="sxs-lookup"><span data-stu-id="9a718-113">If the **MoveTo** row appears between two rows, the Y cell represents the  *y*  -coordinate of the first vertex after the break in the path.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="9a718-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="9a718-114">Remarks</span></span>

<span data-ttu-id="9a718-115">Строка **MoveTo** содержит координаты *x* и *y* первой вершины для фигуры, если строка **MoveTo** является первой строкой в разделе.</span><span class="sxs-lookup"><span data-stu-id="9a718-115">The **MoveTo** row contains the  *x*  - and  *y*  -coordinates of the first vertex for the shape if the **MoveTo** row is the first row in the section.</span></span> <span data-ttu-id="9a718-116">Обычно это первая вершина, размещаемая при рисовании фигуры, и она не обязательно соответствует начальной точке фигуры 1-D.</span><span class="sxs-lookup"><span data-stu-id="9a718-116">Usually this is the first vertex placed when the shape was drawn, and it does not necessarily correspond to the begin point of a 1-D shape.</span></span> 
  
<span data-ttu-id="9a718-117">Раздел геометрии должен начинаться с строки **строка relmoveto** или **MoveTo** , но вы также можете использовать строки **MoveTo** и **строка relmoveto** , чтобы представить зазор в обводки контура фигуры.</span><span class="sxs-lookup"><span data-stu-id="9a718-117">A geometry section must begin with either a **RelMoveTo** or a **MoveTo** row, but you can also use the **MoveTo** and **RelMoveTo** rows to represent a gap in the stroking of a shape's path.</span></span> <span data-ttu-id="9a718-118">Однако если путь используется для определения границы области заливки, этот зазор интерпретируется как отрезок прямой линии.</span><span class="sxs-lookup"><span data-stu-id="9a718-118">However, when the path is used to define the boundary of a filled region, this gap is interpreted as a straight line segment.</span></span> <span data-ttu-id="9a718-119">Чтобы вставить такой зазор, вставьте строку между двумя строками и измените тип строки на **MoveTo**.</span><span class="sxs-lookup"><span data-stu-id="9a718-119">To insert such a gap, insert a row between two rows and change the row type to **MoveTo**.</span></span> <span data-ttu-id="9a718-120">Если строка **MoveTo** находится между двумя строками, она содержит координаты *x* и *y* первой вершины строки после разрыва в пути фигуры.</span><span class="sxs-lookup"><span data-stu-id="9a718-120">If the **MoveTo** row is between two rows, it contains the  *x*  - and  *y*  -coordinates of the first vertex of the line after the break in the shape's path.</span></span> 
  

