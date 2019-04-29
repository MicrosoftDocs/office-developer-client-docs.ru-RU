---
title: RelCubBezTo Row (Geometry Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 77777dd4-5a2c-4048-9ea4-9bd876862963
description: Содержит координаты x и y конечной точки кривой Безье третьего порядка относительно ширины и высоты фигуры, а также координат x и y контрольной точки начала относительной ширины и высоты фигуры, а также координаты x и y для объекта контро. точка l окончания ширины и высоты фигуры относительной кривой.
ms.openlocfilehash: cb886706c4c5cbb3488a95b57dcc84e0e45ee326
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33430331"
---
# <a name="relcubbezto-row-geometry-section"></a><span data-ttu-id="b4b96-103">RelCubBezTo Row (Geometry Section)</span><span class="sxs-lookup"><span data-stu-id="b4b96-103">RelCubBezTo Row (Geometry Section)</span></span>

<span data-ttu-id="b4b96-104">Содержит координаты *x* и *y* конечной точки кривой Безье третьего порядка относительно ширины и высоты фигуры, а также координаты *x* и *y* точки управления начала относительной ширины и высоты фигуры. Координаты *x* и *y* контрольной точки окончания для ширины и высоты фигуры относительной кривой.</span><span class="sxs-lookup"><span data-stu-id="b4b96-104">Contains the  *x*  - and  *y*  -coordinates of the endpoint of a cubic Bézier curve relative to the shape's width and height, the  *x*  - and  *y*  -coordinates of the control point of the beginning of the curve relative shape's width and height, and the  *x*  - and  *y*  -coordinates of the control point of the ending of the curve relative shape's width and height.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="b4b96-105">Строку **строка relcubbezto** можно хранить только в форматах vsdx, vsdm, vstx, vstm, vssx и vssm.</span><span class="sxs-lookup"><span data-stu-id="b4b96-105">A **RelCubBezTo** row can only be persisted in the .vsdx, .vsdm, .vstx, .vstm, .vssx, and .vssm file formats.</span></span> <span data-ttu-id="b4b96-106">При сохранении файла в форматах Visio 2003-2010 строка **строка relcubbezto** преобразуется в строку [NURBSTo](nurbsto-row-geometry-section.md) .</span><span class="sxs-lookup"><span data-stu-id="b4b96-106">When a file is saved to the Visio 2003-2010 formats, the **RelCubBezTo** row is converted to a [NURBSTo](nurbsto-row-geometry-section.md) row.</span></span> 
  
<span data-ttu-id="b4b96-107">Строка **строка relcubbezto** содержит следующие ячейки.</span><span class="sxs-lookup"><span data-stu-id="b4b96-107">A **RelCubBezTo** row contains the following cells.</span></span> 
  
|<span data-ttu-id="b4b96-108">**Cell**</span><span class="sxs-lookup"><span data-stu-id="b4b96-108">**Cell**</span></span>|<span data-ttu-id="b4b96-109">**Описание**</span><span class="sxs-lookup"><span data-stu-id="b4b96-109">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="b4b96-110">X</span><span class="sxs-lookup"><span data-stu-id="b4b96-110">X</span></span>](x-cell-geometry-section.md) <br/> |<span data-ttu-id="b4b96-111">Координата *x* конечной вершины кривой Безье третьего порядка относительно ширины фигуры.</span><span class="sxs-lookup"><span data-stu-id="b4b96-111">The  *x*  -coordinate of the ending vertex of a cubic Bézier curve relative to the width of the shape.</span></span>  <br/> |
|[<span data-ttu-id="b4b96-112">Y (да)</span><span class="sxs-lookup"><span data-stu-id="b4b96-112">Y</span></span>](y-cell-geometry-section.md) <br/> |<span data-ttu-id="b4b96-113">Координата *y* конечной вершины кривой Безье третьего порядка относительно высоты фигуры.</span><span class="sxs-lookup"><span data-stu-id="b4b96-113">The  *y*  -coordinate of the ending vertex of a cubic Bézier curve relative to the height of the shape.</span></span>  <br/> |
|[<span data-ttu-id="b4b96-114">A</span><span class="sxs-lookup"><span data-stu-id="b4b96-114">A</span></span>](a-cell-geometry-section.md) <br/> |<span data-ttu-id="b4b96-115">Координата *x* начальной контрольной точки кривой относительно ширины фигуры; точка на дуги. Контрольная точка лучше всего расположена между начальным и конечным вершинами дуги.</span><span class="sxs-lookup"><span data-stu-id="b4b96-115">The  *x*  -coordinate of the curve's beginning control point relative to the shape's width; a point on the arc. The control point is best located between the beginning and ending vertices of the arc.</span></span>  <br/> |
|[<span data-ttu-id="b4b96-116">З</span><span class="sxs-lookup"><span data-stu-id="b4b96-116">B</span></span>](b-cell-geometry-section.md) <br/> |<span data-ttu-id="b4b96-117">Координата *y* начальной контрольной точки кривой относительно высоты фигуры.</span><span class="sxs-lookup"><span data-stu-id="b4b96-117">The  *y*  -coordinate of a curve's beginning control point relative to the shape's height.</span></span>  <br/> |
|[<span data-ttu-id="b4b96-118">C</span><span class="sxs-lookup"><span data-stu-id="b4b96-118">C</span></span>](c-cell-geometry-section.md) <br/> |<span data-ttu-id="b4b96-119">Координата x конечной точки кривой по *оси x* относительно ширины фигуры; точка на дуги. Контрольная точка лучше всего расположена между начальной контрольной точкой дуги и конечными вершинами дуги.</span><span class="sxs-lookup"><span data-stu-id="b4b96-119">The  *x*  -coordinate of the curve's ending control point relative to the shape's width; a point on the arc. The control point is best located between the beginning control point and ending vertices of the arc.</span></span>  <br/> |
|[<span data-ttu-id="b4b96-120">D</span><span class="sxs-lookup"><span data-stu-id="b4b96-120">D</span></span>](d-cell-geometry-section.md) <br/> |<span data-ttu-id="b4b96-121">Координата *y* конечной точки кривой относительно высоты фигуры.</span><span class="sxs-lookup"><span data-stu-id="b4b96-121">The  *y*  -coordinate of a curve's ending control point relative to the shape's height.</span></span>  <br/> |
   

