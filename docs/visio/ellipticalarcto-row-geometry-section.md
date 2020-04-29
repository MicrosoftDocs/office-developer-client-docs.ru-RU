---
title: EllipticalArcTo Row (Geometry Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm3015
localization_priority: Normal
ms.assetid: 7ceb30a8-1d05-feff-35d8-08a198784a27
description: Содержит координаты x и y конечной точки эллиптической дуги, координаты x и y элемента управления, указывающие на дугу, угол от оси x до основной оси эллипса и соотношение между основными и дополнительными осями эллипса.
ms.openlocfilehash: c6db7560a05652ca3bfcadb2fd4857ac39370562
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33421405"
---
# <a name="ellipticalarcto-row-geometry-section"></a><span data-ttu-id="1fb48-103">EllipticalArcTo Row (Geometry Section)</span><span class="sxs-lookup"><span data-stu-id="1fb48-103">EllipticalArcTo Row (Geometry Section)</span></span>

<span data-ttu-id="1fb48-104">Содержит координаты *x* и *y* конечной точки эллиптической дуги, координаты *x* и *y* элемента управления, указывающие на дугу, угол от оси *x* до основной оси эллипса и соотношение между основными и дополнительными осями эллипса.</span><span class="sxs-lookup"><span data-stu-id="1fb48-104">Contains  *x*  - and  *y*  -coordinates of an elliptical arc's endpoint,  *x*  - and  *y*  -coordinates of the control points on the arc, angle from the  *x*  -axis to the ellipse's major axis, and ratio between the ellipse's major and minor axes.</span></span> 
  
<span data-ttu-id="1fb48-105">Строка строка ellipticalarcto содержит следующие ячейки.</span><span class="sxs-lookup"><span data-stu-id="1fb48-105">An EllipticalArcTo row contains the following cells.</span></span>
  
|<span data-ttu-id="1fb48-106">**Cell**</span><span class="sxs-lookup"><span data-stu-id="1fb48-106">**Cell**</span></span>|<span data-ttu-id="1fb48-107">**Описание**</span><span class="sxs-lookup"><span data-stu-id="1fb48-107">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="1fb48-108">X</span><span class="sxs-lookup"><span data-stu-id="1fb48-108">X</span></span>](x-cell-geometry-section.md) <br/> |<span data-ttu-id="1fb48-109">Координата *x* конечной вершины дуги.</span><span class="sxs-lookup"><span data-stu-id="1fb48-109">The  *x*  -coordinate of the ending vertex on an arc.</span></span>  <br/> |
|[<span data-ttu-id="1fb48-110">Y (да)</span><span class="sxs-lookup"><span data-stu-id="1fb48-110">Y</span></span>](y-cell-geometry-section.md) <br/> |<span data-ttu-id="1fb48-111">Координата *y* конечной вершины дуги.</span><span class="sxs-lookup"><span data-stu-id="1fb48-111">The  *y*  -coordinate of the ending vertex on an arc.</span></span>  <br/> |
|[<span data-ttu-id="1fb48-112">Определенно</span><span class="sxs-lookup"><span data-stu-id="1fb48-112">A</span></span>](a-cell-geometry-section.md) <br/> |<span data-ttu-id="1fb48-113">Координата *x* контрольной точки дуги; точка на дуги. Контрольная точка лучше всего расположена около посередине между начальным и конечным вершинами дуги. В противном случае дуга может увеличиться до экстремального размера для прохождения через контрольную точку с непредсказуемыми результатами.</span><span class="sxs-lookup"><span data-stu-id="1fb48-113">The  *x*  -coordinate of the arc's control point; a point on the arc. The control point is best located about halfway between the beginning and ending vertices of the arc. Otherwise, the arc may grow to an extreme size in order to pass through the control point, with unpredictable results.</span></span>  <br/> |
|[<span data-ttu-id="1fb48-114">З</span><span class="sxs-lookup"><span data-stu-id="1fb48-114">B</span></span>](b-cell-geometry-section.md) <br/> |<span data-ttu-id="1fb48-115">Координата *y* контрольной точки дуги.</span><span class="sxs-lookup"><span data-stu-id="1fb48-115">The  *y*  -coordinate of an arc's control point.</span></span>  <br/> |
|[<span data-ttu-id="1fb48-116">C</span><span class="sxs-lookup"><span data-stu-id="1fb48-116">C</span></span>](c-cell-geometry-section.md) <br/> |<span data-ttu-id="1fb48-117">Угол основной оси дуги относительно оси *x* его родительского элемента.</span><span class="sxs-lookup"><span data-stu-id="1fb48-117">The angle of an arc's major axis relative to the  *x*  -axis of its parent.</span></span>  <br/> |
|[<span data-ttu-id="1fb48-118">D</span><span class="sxs-lookup"><span data-stu-id="1fb48-118">D</span></span>](d-cell-geometry-section.md) <br/> |<span data-ttu-id="1fb48-119">Отношение основной оси дуги к ее вспомогательной оси.</span><span class="sxs-lookup"><span data-stu-id="1fb48-119">The ratio of an arc's major axis to its minor axis.</span></span> <span data-ttu-id="1fb48-120">Несмотря на обычное значение этих слов, ось "Major" не должна превышать "младшую" ось, поэтому значение этого коэффициента не должно превышать 1.</span><span class="sxs-lookup"><span data-stu-id="1fb48-120">Despite the usual meaning of these words, the "major" axis does not have to be greater than the "minor" axis, so this ratio does not have to be greater than 1.</span></span> <span data-ttu-id="1fb48-121">Присвоение этой ячейке значения меньше или равно 0 или больше 1000 может привести к непредсказуемым результатам.</span><span class="sxs-lookup"><span data-stu-id="1fb48-121">Setting this cell to a value less than or equal to 0 or greater than 1000 can lead to unpredictable results.</span></span>  <br/> |
   

