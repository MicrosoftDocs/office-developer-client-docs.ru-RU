---
title: RelCubBezTo Row (Geometry Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 77777dd4-5a2c-4048-9ea4-9bd876862963
description: Содержит координаты x и y конечной точки кривой Безье второго канала относительно ширины и высоты фигуры, координаты x и y контрольной точки начала относительной ширины и высоты кривой, а также координаты X и Y контрольной точки относительно ширины и высоты кривой.
ms.openlocfilehash: cb886706c4c5cbb3488a95b57dcc84e0e45ee326
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33430331"
---
# <a name="relcubbezto-row-geometry-section"></a><span data-ttu-id="89067-103">RelCubBezTo Row (Geometry Section)</span><span class="sxs-lookup"><span data-stu-id="89067-103">RelCubBezTo Row (Geometry Section)</span></span>

<span data-ttu-id="89067-104">Содержит координаты  *x*  и  *y*  конечной точки кривой Безье второго канала относительно ширины и высоты фигуры, координаты  *x*  и  *y*  контрольной точки начала относительной ширины и высоты кривой, а также координаты  *X*  и  *Y*  контрольной точки относительно ширины и высоты кривой.</span><span class="sxs-lookup"><span data-stu-id="89067-104">Contains the  *x*  - and  *y*  -coordinates of the endpoint of a cubic Bézier curve relative to the shape's width and height, the  *x*  - and  *y*  -coordinates of the control point of the beginning of the curve relative shape's width and height, and the  *x*  - and  *y*  -coordinates of the control point of the ending of the curve relative shape's width and height.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="89067-105">Строка **RelCubBezTo** может сохраняться только в форматах VSDX, VSDM, VSTX, VSTM, VSSX и VSSM.</span><span class="sxs-lookup"><span data-stu-id="89067-105">A **RelCubBezTo** row can only be persisted in the .vsdx, .vsdm, .vstx, .vstm, .vssx, and .vssm file formats.</span></span> <span data-ttu-id="89067-106">При сохранении файла в форматах Visio 2003-2010 строка **RelCubBezTo** преобразуется в строку [NURBSTo.](nurbsto-row-geometry-section.md)</span><span class="sxs-lookup"><span data-stu-id="89067-106">When a file is saved to the Visio 2003-2010 formats, the **RelCubBezTo** row is converted to a [NURBSTo](nurbsto-row-geometry-section.md) row.</span></span> 
  
<span data-ttu-id="89067-107">Строка **RelCubBezTo** содержит следующие ячейки.</span><span class="sxs-lookup"><span data-stu-id="89067-107">A **RelCubBezTo** row contains the following cells.</span></span> 
  
|<span data-ttu-id="89067-108">**Cell**</span><span class="sxs-lookup"><span data-stu-id="89067-108">**Cell**</span></span>|<span data-ttu-id="89067-109">**Описание**</span><span class="sxs-lookup"><span data-stu-id="89067-109">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="89067-110">X</span><span class="sxs-lookup"><span data-stu-id="89067-110">X</span></span>](x-cell-geometry-section.md) <br/> |<span data-ttu-id="89067-111">X-координата конечной вершины кривой Безье- безье кубического канала относительно ширины фигуры. </span><span class="sxs-lookup"><span data-stu-id="89067-111">The  *x*  -coordinate of the ending vertex of a cubic Bézier curve relative to the width of the shape.</span></span>  <br/> |
|[<span data-ttu-id="89067-112">Y</span><span class="sxs-lookup"><span data-stu-id="89067-112">Y</span></span>](y-cell-geometry-section.md) <br/> |<span data-ttu-id="89067-113">Y-координата конечной вершины кривой Безье Y относительно высоты фигуры. </span><span class="sxs-lookup"><span data-stu-id="89067-113">The  *y*  -coordinate of the ending vertex of a cubic Bézier curve relative to the height of the shape.</span></span>  <br/> |
|[<span data-ttu-id="89067-114">A</span><span class="sxs-lookup"><span data-stu-id="89067-114">A</span></span>](a-cell-geometry-section.md) <br/> |<span data-ttu-id="89067-115">X-координата точки управления начала кривой относительно ширины фигуры;  точка на дуге. Контрольная точка лучше всего расположена между началом и конечной вершиной дуги.</span><span class="sxs-lookup"><span data-stu-id="89067-115">The  *x*  -coordinate of the curve's beginning control point relative to the shape's width; a point on the arc. The control point is best located between the beginning and ending vertices of the arc.</span></span>  <br/> |
|[<span data-ttu-id="89067-116">B</span><span class="sxs-lookup"><span data-stu-id="89067-116">B</span></span>](b-cell-geometry-section.md) <br/> |<span data-ttu-id="89067-117">Координата  *Y*  точки начала контрольной точки кривой относительно высоты фигуры.</span><span class="sxs-lookup"><span data-stu-id="89067-117">The  *y*  -coordinate of a curve's beginning control point relative to the shape's height.</span></span>  <br/> |
|[<span data-ttu-id="89067-118">C</span><span class="sxs-lookup"><span data-stu-id="89067-118">C</span></span>](c-cell-geometry-section.md) <br/> |<span data-ttu-id="89067-119">X-координата конечной контрольной точки кривой относительно ширины фигуры;  точка на дуге. Контрольная точка лучше всего расположена между точки управления и конечной вершиной дуги.</span><span class="sxs-lookup"><span data-stu-id="89067-119">The  *x*  -coordinate of the curve's ending control point relative to the shape's width; a point on the arc. The control point is best located between the beginning control point and ending vertices of the arc.</span></span>  <br/> |
|[<span data-ttu-id="89067-120">D</span><span class="sxs-lookup"><span data-stu-id="89067-120">D</span></span>](d-cell-geometry-section.md) <br/> |<span data-ttu-id="89067-121">Координата  *Y*  конечной контрольной точки кривой относительно высоты фигуры.</span><span class="sxs-lookup"><span data-stu-id="89067-121">The  *y*  -coordinate of a curve's ending control point relative to the shape's height.</span></span>  <br/> |
   

