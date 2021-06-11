---
title: RelCubBezTo Row (Geometry Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 77777dd4-5a2c-4048-9ea4-9bd876862963
description: Содержит x и y-координаты конечной точки кривой кубического Bézier относительно ширины и высоты фигуры, x - и y -координаты точки управления в начале ширины и высоты кривой относительной формы, а также x - и y-координаты точки управления окончанием ширины и высоты кривой относительной формы.
ms.openlocfilehash: cb886706c4c5cbb3488a95b57dcc84e0e45ee326
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33430331"
---
# <a name="relcubbezto-row-geometry-section"></a><span data-ttu-id="14b02-103">RelCubBezTo Row (Geometry Section)</span><span class="sxs-lookup"><span data-stu-id="14b02-103">RelCubBezTo Row (Geometry Section)</span></span>

<span data-ttu-id="14b02-104">Содержит  *x*  и  *y-координаты*  конечной точки кривой кубического Bézier относительно ширины и высоты фигуры, x  *-*  и  *y*  -координаты точки управления в начале ширины и высоты кривой относительной формы, а также  *x*  - и  *y-координаты*  точки управления окончанием ширины и высоты кривой относительной формы.</span><span class="sxs-lookup"><span data-stu-id="14b02-104">Contains the  *x*  - and  *y*  -coordinates of the endpoint of a cubic Bézier curve relative to the shape's width and height, the  *x*  - and  *y*  -coordinates of the control point of the beginning of the curve relative shape's width and height, and the  *x*  - and  *y*  -coordinates of the control point of the ending of the curve relative shape's width and height.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="14b02-105">Строка **RelCubBezTo** может сохраняться только в форматах файлов .vsdx, .vsdm, .vstx, .vstm, .vssx и .vssm file.</span><span class="sxs-lookup"><span data-stu-id="14b02-105">A **RelCubBezTo** row can only be persisted in the .vsdx, .vsdm, .vstx, .vstm, .vssx, and .vssm file formats.</span></span> <span data-ttu-id="14b02-106">Если файл сохранен в форматах 2003-2010 Visio, строка **RelCubBezTo** преобразуется в строку [NURBSTo.](nurbsto-row-geometry-section.md)</span><span class="sxs-lookup"><span data-stu-id="14b02-106">When a file is saved to the Visio 2003-2010 formats, the **RelCubBezTo** row is converted to a [NURBSTo](nurbsto-row-geometry-section.md) row.</span></span> 
  
<span data-ttu-id="14b02-107">Строка **RelCubBezTo** содержит следующие ячейки.</span><span class="sxs-lookup"><span data-stu-id="14b02-107">A **RelCubBezTo** row contains the following cells.</span></span> 
  
|<span data-ttu-id="14b02-108">**Cell**</span><span class="sxs-lookup"><span data-stu-id="14b02-108">**Cell**</span></span>|<span data-ttu-id="14b02-109">**Описание**</span><span class="sxs-lookup"><span data-stu-id="14b02-109">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="14b02-110">X</span><span class="sxs-lookup"><span data-stu-id="14b02-110">X</span></span>](x-cell-geometry-section.md) <br/> |<span data-ttu-id="14b02-111">X-координата конечной вершины кривой кубического Bézier относительно ширины фигуры. </span><span class="sxs-lookup"><span data-stu-id="14b02-111">The  *x*  -coordinate of the ending vertex of a cubic Bézier curve relative to the width of the shape.</span></span>  <br/> |
|[<span data-ttu-id="14b02-112">Да</span><span class="sxs-lookup"><span data-stu-id="14b02-112">Y</span></span>](y-cell-geometry-section.md) <br/> |<span data-ttu-id="14b02-113">y-координата конечной вершины кривой кубического Bézier относительно высоты фигуры. </span><span class="sxs-lookup"><span data-stu-id="14b02-113">The  *y*  -coordinate of the ending vertex of a cubic Bézier curve relative to the height of the shape.</span></span>  <br/> |
|[<span data-ttu-id="14b02-114">A</span><span class="sxs-lookup"><span data-stu-id="14b02-114">A</span></span>](a-cell-geometry-section.md) <br/> |<span data-ttu-id="14b02-115">X-координата точки начала управления кривой относительно ширины фигуры;  точка на дуге. Точка управления лучше всего расположена между началом и окончанием вершин дуги.</span><span class="sxs-lookup"><span data-stu-id="14b02-115">The  *x*  -coordinate of the curve's beginning control point relative to the shape's width; a point on the arc. The control point is best located between the beginning and ending vertices of the arc.</span></span>  <br/> |
|[<span data-ttu-id="14b02-116">B</span><span class="sxs-lookup"><span data-stu-id="14b02-116">B</span></span>](b-cell-geometry-section.md) <br/> |<span data-ttu-id="14b02-117">Y-координата точки начала управления кривой относительно высоты фигуры. </span><span class="sxs-lookup"><span data-stu-id="14b02-117">The  *y*  -coordinate of a curve's beginning control point relative to the shape's height.</span></span>  <br/> |
|[<span data-ttu-id="14b02-118">C</span><span class="sxs-lookup"><span data-stu-id="14b02-118">C</span></span>](c-cell-geometry-section.md) <br/> |<span data-ttu-id="14b02-119">X-координата конечной точки управления кривой относительно ширины фигуры;  точка на дуге. Точка управления лучше всего расположена между точкой начала управления и конечной вершиной дуги.</span><span class="sxs-lookup"><span data-stu-id="14b02-119">The  *x*  -coordinate of the curve's ending control point relative to the shape's width; a point on the arc. The control point is best located between the beginning control point and ending vertices of the arc.</span></span>  <br/> |
|[<span data-ttu-id="14b02-120">D</span><span class="sxs-lookup"><span data-stu-id="14b02-120">D</span></span>](d-cell-geometry-section.md) <br/> |<span data-ttu-id="14b02-121">Y-координата конечной точки управления кривой относительно высоты фигуры. </span><span class="sxs-lookup"><span data-stu-id="14b02-121">The  *y*  -coordinate of a curve's ending control point relative to the shape's height.</span></span>  <br/> |
   

