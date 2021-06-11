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
description: Содержит x и y-координаты первой вершины фигуры или представляет x - и y-координаты первой вершины после перерыва в пути.
ms.openlocfilehash: fc414093348b8da04fa3503053584395976982dd
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33429700"
---
# <a name="moveto-row-geometry-section"></a><span data-ttu-id="296ee-103">MoveTo Row (Geometry Section)</span><span class="sxs-lookup"><span data-stu-id="296ee-103">MoveTo Row (Geometry Section)</span></span>

<span data-ttu-id="296ee-104">Содержит  *x*  и  *y-координаты*  первой вершины фигуры или представляет x  *-*  и  *y-координаты*  первой вершины после перерыва в пути.</span><span class="sxs-lookup"><span data-stu-id="296ee-104">Contains the  *x*  - and  *y*  -coordinates of the first vertex of a shape, or represents the  *x*  - and  *y*  -coordinates of the first vertex after a break in a path.</span></span> 
  
<span data-ttu-id="296ee-105">Строка **MoveTo** содержит следующие ячейки.</span><span class="sxs-lookup"><span data-stu-id="296ee-105">A **MoveTo** row contains the following cells.</span></span> 
  
|<span data-ttu-id="296ee-106">**Cell**</span><span class="sxs-lookup"><span data-stu-id="296ee-106">**Cell**</span></span>|<span data-ttu-id="296ee-107">**Описание**</span><span class="sxs-lookup"><span data-stu-id="296ee-107">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="296ee-108">X</span><span class="sxs-lookup"><span data-stu-id="296ee-108">X</span></span>](x-cell-geometry-section.md) <br/> |<span data-ttu-id="296ee-109">Если **строка MoveTo** — это первая строка в разделе, X-ячейка представляет  *x-координату*  первого вершины фигуры.</span><span class="sxs-lookup"><span data-stu-id="296ee-109">If the **MoveTo** row is the first row in the section, the X cell represents the  *x*  -coordinate of the first vertex of a shape.</span></span> <span data-ttu-id="296ee-110">Если **строка MoveTo** отображается между двумя строками, X-ячейка представляет  *x-координату*  первой вершины после перерыва в пути.</span><span class="sxs-lookup"><span data-stu-id="296ee-110">If the **MoveTo** row appears between two rows, the X cell represents the  *x*  -coordinate of the first vertex after the break in the path.</span></span>  <br/> |
|[<span data-ttu-id="296ee-111">Да</span><span class="sxs-lookup"><span data-stu-id="296ee-111">Y</span></span>](y-cell-geometry-section.md) <br/> |<span data-ttu-id="296ee-112">Если **строка MoveTo** — это первая строка в разделе, ячейка Y представляет  *y-координату*  первого вершины фигуры.</span><span class="sxs-lookup"><span data-stu-id="296ee-112">If the **MoveTo** row is the first row in the section, the Y cell represents the  *y*  -coordinate of the first vertex of a shape.</span></span> <span data-ttu-id="296ee-113">Если **строка MoveTo** отображается между двумя строками, ячейка Y представляет  *y-координату*  первой вершины после перерыва в пути.</span><span class="sxs-lookup"><span data-stu-id="296ee-113">If the **MoveTo** row appears between two rows, the Y cell represents the  *y*  -coordinate of the first vertex after the break in the path.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="296ee-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="296ee-114">Remarks</span></span>

<span data-ttu-id="296ee-115">Строка **MoveTo** содержит  *x*  и  *y-координаты*  первой вершины фигуры, если строка **MoveTo** является первой строкой в разделе.</span><span class="sxs-lookup"><span data-stu-id="296ee-115">The **MoveTo** row contains the  *x*  - and  *y*  -coordinates of the first vertex for the shape if the **MoveTo** row is the first row in the section.</span></span> <span data-ttu-id="296ee-116">Обычно это первый вершина, помещаемая при нарисовании фигуры, и она не обязательно соответствует точке начала формы 1-D.</span><span class="sxs-lookup"><span data-stu-id="296ee-116">Usually this is the first vertex placed when the shape was drawn, and it does not necessarily correspond to the begin point of a 1-D shape.</span></span> 
  
<span data-ttu-id="296ee-117">Раздел геометрии должен начинаться с **строки RelMoveTo** или **MoveTo,** но вы также можете использовать **строки MoveTo** и **RelMoveTo** для представления пробела в поглаживание пути фигуры.</span><span class="sxs-lookup"><span data-stu-id="296ee-117">A geometry section must begin with either a **RelMoveTo** or a **MoveTo** row, but you can also use the **MoveTo** and **RelMoveTo** rows to represent a gap in the stroking of a shape's path.</span></span> <span data-ttu-id="296ee-118">Однако, когда путь используется для определения границы заполненного региона, этот разрыв интерпретируется как сегмент прямой линии.</span><span class="sxs-lookup"><span data-stu-id="296ee-118">However, when the path is used to define the boundary of a filled region, this gap is interpreted as a straight line segment.</span></span> <span data-ttu-id="296ee-119">Чтобы вставить такой пробел, вставьте строку между двумя строками и измените тип строки на **MoveTo.**</span><span class="sxs-lookup"><span data-stu-id="296ee-119">To insert such a gap, insert a row between two rows and change the row type to **MoveTo**.</span></span> <span data-ttu-id="296ee-120">Если **строка MoveTo** находится между двумя строками, она содержит x  *и*  *y-координаты*  первого вершины линии после перерыва в пути фигуры.</span><span class="sxs-lookup"><span data-stu-id="296ee-120">If the **MoveTo** row is between two rows, it contains the  *x*  - and  *y*  -coordinates of the first vertex of the line after the break in the shape's path.</span></span> 
  

