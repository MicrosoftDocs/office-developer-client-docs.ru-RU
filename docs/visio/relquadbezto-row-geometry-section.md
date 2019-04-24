---
title: RelQuadBezTo Row (Geometry Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 5ae57707-5a50-43f0-8c78-516790b5034e
description: Содержит координаты x и y конечной точки квадратичной кривой Безье относительно ширины и высоты фигуры, а также координат x и y контрольной точки кривой относительно ширины и высоты фигуры.
ms.openlocfilehash: f517fa006c6630a26e9162adfbb1be2139487e63
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32319931"
---
# <a name="relquadbezto-row-geometry-section"></a><span data-ttu-id="108b1-103">RelQuadBezTo Row (Geometry Section)</span><span class="sxs-lookup"><span data-stu-id="108b1-103">RelQuadBezTo Row (Geometry Section)</span></span>

<span data-ttu-id="108b1-104">Содержит координаты *x* и *y* конечной точки квадратичной кривой Безье относительно ширины и высоты фигуры, а также координат *x* и *y* контрольной точки кривой относительно ширины и высоты фигуры.</span><span class="sxs-lookup"><span data-stu-id="108b1-104">Contains the  *x*  - and  *y*  -coordinates of the endpoint of a quadratic Bézier curve relative to the shape's width and height and the  *x*  - and  *y*  -coordinates of the control point of the curve relative shape's width and height.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="108b1-105">Строку **строка relquadbezto** можно хранить только в форматах vsdx, vsdm, vstx, vstm, vssx и vssm.</span><span class="sxs-lookup"><span data-stu-id="108b1-105">A **RelQuadBezTo** row can only be persisted in the .vsdx, .vsdm, .vstx, .vstm, .vssx, and .vssm file formats.</span></span> <span data-ttu-id="108b1-106">При сохранении файла в форматах Visio 2003-2010 строка **строка relquadbezto** преобразуется в строку [NURBSTo](nurbsto-row-geometry-section.md) .</span><span class="sxs-lookup"><span data-stu-id="108b1-106">When a file is saved to the Visio 2003-2010 formats, the **RelQuadBezTo** row is converted to a [NURBSTo](nurbsto-row-geometry-section.md) row.</span></span> 
  
<span data-ttu-id="108b1-107">Строка **строка relquadbezto** содержит следующие ячейки.</span><span class="sxs-lookup"><span data-stu-id="108b1-107">A **RelQuadBezTo** row contains the following cells.</span></span> 
  
|<span data-ttu-id="108b1-108">**Cell**</span><span class="sxs-lookup"><span data-stu-id="108b1-108">**Cell**</span></span>|<span data-ttu-id="108b1-109">**Описание**</span><span class="sxs-lookup"><span data-stu-id="108b1-109">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="108b1-110">X</span><span class="sxs-lookup"><span data-stu-id="108b1-110">X</span></span>](x-cell-geometry-section.md) <br/> |<span data-ttu-id="108b1-111">Координата *x* конечной вершины кривой Безье второго уровня относительно ширины фигуры.</span><span class="sxs-lookup"><span data-stu-id="108b1-111">The  *x*  -coordinate of the ending vertex of a quadratic Bézier curve relative to the width of the shape.</span></span>  <br/> |
|[<span data-ttu-id="108b1-112">Y (да)</span><span class="sxs-lookup"><span data-stu-id="108b1-112">Y</span></span>](y-cell-geometry-section.md) <br/> |<span data-ttu-id="108b1-113">Координата *y* конечной вершины кривой Безье второго уровня относительно высоты фигуры.</span><span class="sxs-lookup"><span data-stu-id="108b1-113">The  *y*  -coordinate of the ending vertex of a quadratic Bézier curve relative to the height of the shape.</span></span>  <br/> |
|[<span data-ttu-id="108b1-114">Определенно</span><span class="sxs-lookup"><span data-stu-id="108b1-114">A</span></span>](a-cell-geometry-section.md) <br/> |<span data-ttu-id="108b1-115">Координата *x* контрольной точки кривой относительно ширины фигуры; точка на дуги. Контрольная точка лучше всего расположена около посередине между начальным и конечным вершинами дуги.</span><span class="sxs-lookup"><span data-stu-id="108b1-115">The  *x*  -coordinate of the curve's control point relative to the shape's width; a point on the arc. The control point is best located about halfway between the beginning and ending vertices of the arc.</span></span>  <br/> |
|[<span data-ttu-id="108b1-116">З</span><span class="sxs-lookup"><span data-stu-id="108b1-116">B</span></span>](b-cell-geometry-section.md) <br/> |<span data-ttu-id="108b1-117">Координата *y* контрольной точки кривой относительно высоты фигуры.</span><span class="sxs-lookup"><span data-stu-id="108b1-117">The  *y*  -coordinate of a curve's control point relative to the shape's height.</span></span>  <br/> |
   

