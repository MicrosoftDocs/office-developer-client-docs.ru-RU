---
title: Строка MoveTo (раздел "Геометрия")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm3030
localization_priority: Normal
ms.assetid: c5b20257-676c-279d-f730-1b6fbbe98305
description: Содержит x - и y - координаты первой вершины фигуры или представляет x - и y-координат первой вершины после приостановки пути.
ms.openlocfilehash: cee62701074269350ae52c6fa7f7aee5cb612f49
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19814286"
---
# <a name="moveto-row-geometry-section"></a><span data-ttu-id="81f40-103">Строка MoveTo (раздел "Геометрия")</span><span class="sxs-lookup"><span data-stu-id="81f40-103">MoveTo Row (Geometry Section)</span></span>

<span data-ttu-id="81f40-104">Содержит *x* - и *y* - координаты первой вершины фигуры или представляет *x* - и *y* -координат первой вершины после приостановки пути.</span><span class="sxs-lookup"><span data-stu-id="81f40-104">Contains the  *x*  - and  *y*  -coordinates of the first vertex of a shape, or represents the  *x*  - and  *y*  -coordinates of the first vertex after a break in a path.</span></span> 
  
<span data-ttu-id="81f40-105">Строка **MoveTo** содержит следующие ячейки.</span><span class="sxs-lookup"><span data-stu-id="81f40-105">A **MoveTo** row contains the following cells.</span></span> 
  
|<span data-ttu-id="81f40-106">**Cell**</span><span class="sxs-lookup"><span data-stu-id="81f40-106">**Cell**</span></span>|<span data-ttu-id="81f40-107">**Описание**</span><span class="sxs-lookup"><span data-stu-id="81f40-107">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="81f40-108">X</span><span class="sxs-lookup"><span data-stu-id="81f40-108">X</span></span>](x-cell-geometry-section.md) <br/> |<span data-ttu-id="81f40-109">Если строка **MoveTo** является первой строки в разделе, ячейки X представляет *x* -координата первой вершины фигуры.</span><span class="sxs-lookup"><span data-stu-id="81f40-109">If the **MoveTo** row is the first row in the section, the X cell represents the  *x*  -coordinate of the first vertex of a shape.</span></span> <span data-ttu-id="81f40-110">Если отображается строка **MoveTo** между двумя строками, ячейки X представляет *x* -координата первой вершины после приостановки выполнения в поле путь.</span><span class="sxs-lookup"><span data-stu-id="81f40-110">If the **MoveTo** row appears between two rows, the X cell represents the  *x*  -coordinate of the first vertex after the break in the path.</span></span>  <br/> |
|[<span data-ttu-id="81f40-111">Да</span><span class="sxs-lookup"><span data-stu-id="81f40-111">Y</span></span>](y-cell-geometry-section.md) <br/> |<span data-ttu-id="81f40-112">Если строка **MoveTo** является первой строки в разделе, ячейки Y представляет *y* -координата первой вершины фигуры.</span><span class="sxs-lookup"><span data-stu-id="81f40-112">If the **MoveTo** row is the first row in the section, the Y cell represents the  *y*  -coordinate of the first vertex of a shape.</span></span> <span data-ttu-id="81f40-113">Если отображается строка **MoveTo** между двумя строками, ячейки Y представляет *y* -координата первой вершины после приостановки выполнения в поле путь.</span><span class="sxs-lookup"><span data-stu-id="81f40-113">If the **MoveTo** row appears between two rows, the Y cell represents the  *y*  -coordinate of the first vertex after the break in the path.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="81f40-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="81f40-114">Remarks</span></span>

<span data-ttu-id="81f40-115">Строка **MoveTo** содержит *x* - и *y* -координат первой вершины фигуры, если строка **MoveTo** является первой строки в разделе.</span><span class="sxs-lookup"><span data-stu-id="81f40-115">The **MoveTo** row contains the  *x*  - and  *y*  -coordinates of the first vertex for the shape if the **MoveTo** row is the first row in the section.</span></span> <span data-ttu-id="81f40-116">Обычно это первой вершины, когда был представляют собой фигуры, и его необязательно соответствует начальной точки одномерной фигуры.</span><span class="sxs-lookup"><span data-stu-id="81f40-116">Usually this is the first vertex placed when the shape was drawn, and it does not necessarily correspond to the begin point of a 1-D shape.</span></span> 
  
<span data-ttu-id="81f40-117">Раздел геометрии должен начинаться с **RelMoveTo** или **MoveTo** строки, но можно также использовать **MoveTo** и **RelMoveTo** строк для представления разрывов в обводка фигуры путь.</span><span class="sxs-lookup"><span data-stu-id="81f40-117">A geometry section must begin with either a **RelMoveTo** or a **MoveTo** row, but you can also use the **MoveTo** and **RelMoveTo** rows to represent a gap in the stroking of a shape's path.</span></span> <span data-ttu-id="81f40-118">Тем не менее если путь используется для определения границ заполненной области, пропуска считается прямой сегмент.</span><span class="sxs-lookup"><span data-stu-id="81f40-118">However, when the path is used to define the boundary of a filled region, this gap is interpreted as a straight line segment.</span></span> <span data-ttu-id="81f40-119">Чтобы вставить таких разрывов, вставить строку между двумя строками и измените тип строки на **MoveTo**.</span><span class="sxs-lookup"><span data-stu-id="81f40-119">To insert such a gap, insert a row between two rows and change the row type to **MoveTo**.</span></span> <span data-ttu-id="81f40-120">Если строка **MoveTo** между двух строк, он содержит *x* - и *y* -координаты первой вершины в строке после приостановки выполнения в путь фигуры.</span><span class="sxs-lookup"><span data-stu-id="81f40-120">If the **MoveTo** row is between two rows, it contains the  *x*  - and  *y*  -coordinates of the first vertex of the line after the break in the shape's path.</span></span> 
  

