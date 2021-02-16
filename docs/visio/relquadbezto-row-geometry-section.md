---
title: RelQuadBezTo Row (Geometry Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 5ae57707-5a50-43f0-8c78-516790b5034e
description: Содержит координаты x и y конечной точки кривой Безье первого кадра относительно ширины и высоты фигуры, а также координат x и y контрольной точки относительной ширины и высоты кривой.
ms.openlocfilehash: f517fa006c6630a26e9162adfbb1be2139487e63
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33423358"
---
# <a name="relquadbezto-row-geometry-section"></a><span data-ttu-id="820ae-103">RelQuadBezTo Row (Geometry Section)</span><span class="sxs-lookup"><span data-stu-id="820ae-103">RelQuadBezTo Row (Geometry Section)</span></span>

<span data-ttu-id="820ae-104">Содержит координаты  *x*  и  *y*  конечной точки кривой Безье первого кадра относительно ширины и высоты фигуры, а также координат  *x*  и  *y*  контрольной точки относительной ширины и высоты кривой.</span><span class="sxs-lookup"><span data-stu-id="820ae-104">Contains the  *x*  - and  *y*  -coordinates of the endpoint of a quadratic Bézier curve relative to the shape's width and height and the  *x*  - and  *y*  -coordinates of the control point of the curve relative shape's width and height.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="820ae-105">Строка **RelQuadBezTo** может сохраняться только в форматах VSDX, VSDM, VSTX, VSTM, VSSX и VSSM.</span><span class="sxs-lookup"><span data-stu-id="820ae-105">A **RelQuadBezTo** row can only be persisted in the .vsdx, .vsdm, .vstx, .vstm, .vssx, and .vssm file formats.</span></span> <span data-ttu-id="820ae-106">При сохранении файла в форматах Visio 2003-2010 строка **RelQuadBezTo** преобразуется в строку [NURBSTo.](nurbsto-row-geometry-section.md)</span><span class="sxs-lookup"><span data-stu-id="820ae-106">When a file is saved to the Visio 2003-2010 formats, the **RelQuadBezTo** row is converted to a [NURBSTo](nurbsto-row-geometry-section.md) row.</span></span> 
  
<span data-ttu-id="820ae-107">Строка **RelQuadBezTo** содержит следующие ячейки.</span><span class="sxs-lookup"><span data-stu-id="820ae-107">A **RelQuadBezTo** row contains the following cells.</span></span> 
  
|<span data-ttu-id="820ae-108">**Cell**</span><span class="sxs-lookup"><span data-stu-id="820ae-108">**Cell**</span></span>|<span data-ttu-id="820ae-109">**Описание**</span><span class="sxs-lookup"><span data-stu-id="820ae-109">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="820ae-110">X</span><span class="sxs-lookup"><span data-stu-id="820ae-110">X</span></span>](x-cell-geometry-section.md) <br/> |<span data-ttu-id="820ae-111">X-координата конечной вершины кривой Безье х относительно ширины фигуры. </span><span class="sxs-lookup"><span data-stu-id="820ae-111">The  *x*  -coordinate of the ending vertex of a quadratic Bézier curve relative to the width of the shape.</span></span>  <br/> |
|[<span data-ttu-id="820ae-112">Y</span><span class="sxs-lookup"><span data-stu-id="820ae-112">Y</span></span>](y-cell-geometry-section.md) <br/> |<span data-ttu-id="820ae-113">Y-координата конечной вершины кривой Безье Y относительно высоты фигуры. </span><span class="sxs-lookup"><span data-stu-id="820ae-113">The  *y*  -coordinate of the ending vertex of a quadratic Bézier curve relative to the height of the shape.</span></span>  <br/> |
|[<span data-ttu-id="820ae-114">A</span><span class="sxs-lookup"><span data-stu-id="820ae-114">A</span></span>](a-cell-geometry-section.md) <br/> |<span data-ttu-id="820ae-115">X-координата контрольной точки кривой относительно ширины фигуры;  точка на дуге. Контрольная точка лучше всего расположена примерно на середине между началом и конечной вершиной дуги.</span><span class="sxs-lookup"><span data-stu-id="820ae-115">The  *x*  -coordinate of the curve's control point relative to the shape's width; a point on the arc. The control point is best located about halfway between the beginning and ending vertices of the arc.</span></span>  <br/> |
|[<span data-ttu-id="820ae-116">B</span><span class="sxs-lookup"><span data-stu-id="820ae-116">B</span></span>](b-cell-geometry-section.md) <br/> |<span data-ttu-id="820ae-117">Координата  *Y*  контрольной точки кривой относительно высоты фигуры.</span><span class="sxs-lookup"><span data-stu-id="820ae-117">The  *y*  -coordinate of a curve's control point relative to the shape's height.</span></span>  <br/> |
   

