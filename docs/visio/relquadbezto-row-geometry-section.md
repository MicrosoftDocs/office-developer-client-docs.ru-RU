---
title: RelQuadBezTo Row (Geometry Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 5ae57707-5a50-43f0-8c78-516790b5034e
description: Содержит x - и y-координаты конечной точки квадратной кривой Bézier относительно ширины и высоты фигуры, а также x - и y-координаты точки управления ширины и высоты кривой относительной формы.
ms.openlocfilehash: f517fa006c6630a26e9162adfbb1be2139487e63
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33423358"
---
# <a name="relquadbezto-row-geometry-section"></a><span data-ttu-id="405e3-103">RelQuadBezTo Row (Geometry Section)</span><span class="sxs-lookup"><span data-stu-id="405e3-103">RelQuadBezTo Row (Geometry Section)</span></span>

<span data-ttu-id="405e3-104">Содержит *x* - и y-координаты конечной точки квадратной кривой Bézier относительно ширины и высоты фигуры, а также x *-* и *y-координаты* точки управления ширины и высоты кривой относительной формы. </span><span class="sxs-lookup"><span data-stu-id="405e3-104">Contains the  *x*  - and  *y*  -coordinates of the endpoint of a quadratic Bézier curve relative to the shape's width and height and the  *x*  - and  *y*  -coordinates of the control point of the curve relative shape's width and height.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="405e3-105">Строка **RelQuadBezTo** может сохраняться только в форматах файлов .vsdx, .vsdm, .vstx, .vstm, .vssx и .vssm.</span><span class="sxs-lookup"><span data-stu-id="405e3-105">A **RelQuadBezTo** row can only be persisted in the .vsdx, .vsdm, .vstx, .vstm, .vssx, and .vssm file formats.</span></span> <span data-ttu-id="405e3-106">Если файл сохранен в форматах 2003-2010 Visio, строка **RelQuadBezTo** преобразуется в строку [NURBSTo.](nurbsto-row-geometry-section.md)</span><span class="sxs-lookup"><span data-stu-id="405e3-106">When a file is saved to the Visio 2003-2010 formats, the **RelQuadBezTo** row is converted to a [NURBSTo](nurbsto-row-geometry-section.md) row.</span></span> 
  
<span data-ttu-id="405e3-107">Строка **RelQuadBezTo** содержит следующие ячейки.</span><span class="sxs-lookup"><span data-stu-id="405e3-107">A **RelQuadBezTo** row contains the following cells.</span></span> 
  
|<span data-ttu-id="405e3-108">**Cell**</span><span class="sxs-lookup"><span data-stu-id="405e3-108">**Cell**</span></span>|<span data-ttu-id="405e3-109">**Описание**</span><span class="sxs-lookup"><span data-stu-id="405e3-109">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="405e3-110">X</span><span class="sxs-lookup"><span data-stu-id="405e3-110">X</span></span>](x-cell-geometry-section.md) <br/> |<span data-ttu-id="405e3-111">X-координата конечной вершины квадратной кривой Bézier относительно ширины фигуры. </span><span class="sxs-lookup"><span data-stu-id="405e3-111">The  *x*  -coordinate of the ending vertex of a quadratic Bézier curve relative to the width of the shape.</span></span>  <br/> |
|[<span data-ttu-id="405e3-112">Да</span><span class="sxs-lookup"><span data-stu-id="405e3-112">Y</span></span>](y-cell-geometry-section.md) <br/> |<span data-ttu-id="405e3-113">y-координата конечной вершины квадратной кривой Bézier относительно высоты фигуры. </span><span class="sxs-lookup"><span data-stu-id="405e3-113">The  *y*  -coordinate of the ending vertex of a quadratic Bézier curve relative to the height of the shape.</span></span>  <br/> |
|[<span data-ttu-id="405e3-114">A</span><span class="sxs-lookup"><span data-stu-id="405e3-114">A</span></span>](a-cell-geometry-section.md) <br/> |<span data-ttu-id="405e3-115">X-координата точки управления кривой относительно ширины фигуры;  точка на дуге. Точка управления расположена на полпути между началом и окончанием вершин дуги.</span><span class="sxs-lookup"><span data-stu-id="405e3-115">The  *x*  -coordinate of the curve's control point relative to the shape's width; a point on the arc. The control point is best located about halfway between the beginning and ending vertices of the arc.</span></span>  <br/> |
|[<span data-ttu-id="405e3-116">B</span><span class="sxs-lookup"><span data-stu-id="405e3-116">B</span></span>](b-cell-geometry-section.md) <br/> |<span data-ttu-id="405e3-117">Y-координата точки управления кривой относительно высоты фигуры. </span><span class="sxs-lookup"><span data-stu-id="405e3-117">The  *y*  -coordinate of a curve's control point relative to the shape's height.</span></span>  <br/> |
   

