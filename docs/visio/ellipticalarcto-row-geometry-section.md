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
description: Содержит координаты x и y конечной точки эллиптической дуги, x - и y -координат контрольных точек на дуге, угол от оси X до основной оси эллипса и соотношение между основной и второстепенной осями эллипса.
ms.openlocfilehash: c6db7560a05652ca3bfcadb2fd4857ac39370562
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33421405"
---
# <a name="ellipticalarcto-row-geometry-section"></a><span data-ttu-id="63b95-103">EllipticalArcTo Row (Geometry Section)</span><span class="sxs-lookup"><span data-stu-id="63b95-103">EllipticalArcTo Row (Geometry Section)</span></span>

<span data-ttu-id="63b95-104">Содержит  *координаты x*  и  *y*  конечной точки эллиптической дуги,  *x*  -  *и y*  -координат контрольных точек на дуге, угол от  *оси X*  до основной оси эллипса и соотношение между основной и второстепенной осями эллипса.</span><span class="sxs-lookup"><span data-stu-id="63b95-104">Contains  *x*  - and  *y*  -coordinates of an elliptical arc's endpoint,  *x*  - and  *y*  -coordinates of the control points on the arc, angle from the  *x*  -axis to the ellipse's major axis, and ratio between the ellipse's major and minor axes.</span></span> 
  
<span data-ttu-id="63b95-105">Строка EllipticalArcTo содержит следующие ячейки.</span><span class="sxs-lookup"><span data-stu-id="63b95-105">An EllipticalArcTo row contains the following cells.</span></span>
  
|<span data-ttu-id="63b95-106">**Cell**</span><span class="sxs-lookup"><span data-stu-id="63b95-106">**Cell**</span></span>|<span data-ttu-id="63b95-107">**Описание**</span><span class="sxs-lookup"><span data-stu-id="63b95-107">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="63b95-108">X</span><span class="sxs-lookup"><span data-stu-id="63b95-108">X</span></span>](x-cell-geometry-section.md) <br/> |<span data-ttu-id="63b95-109">X-координата конечной вершины на дуге. </span><span class="sxs-lookup"><span data-stu-id="63b95-109">The  *x*  -coordinate of the ending vertex on an arc.</span></span>  <br/> |
|[<span data-ttu-id="63b95-110">Y</span><span class="sxs-lookup"><span data-stu-id="63b95-110">Y</span></span>](y-cell-geometry-section.md) <br/> |<span data-ttu-id="63b95-111">Координата  *Y*  конечной вершины на дуге.</span><span class="sxs-lookup"><span data-stu-id="63b95-111">The  *y*  -coordinate of the ending vertex on an arc.</span></span>  <br/> |
|[<span data-ttu-id="63b95-112">A</span><span class="sxs-lookup"><span data-stu-id="63b95-112">A</span></span>](a-cell-geometry-section.md) <br/> |<span data-ttu-id="63b95-113">X-координата контрольной точки дуги;  точка на дуге. Контрольная точка лучше всего расположена примерно на середине между началом и конечной вершиной дуги. В противном случае дуга может увеличиваться до крайнего размера, чтобы пройти через контрольную точку с непредсказуемыми результатами.</span><span class="sxs-lookup"><span data-stu-id="63b95-113">The  *x*  -coordinate of the arc's control point; a point on the arc. The control point is best located about halfway between the beginning and ending vertices of the arc. Otherwise, the arc may grow to an extreme size in order to pass through the control point, with unpredictable results.</span></span>  <br/> |
|[<span data-ttu-id="63b95-114">B</span><span class="sxs-lookup"><span data-stu-id="63b95-114">B</span></span>](b-cell-geometry-section.md) <br/> |<span data-ttu-id="63b95-115">Y-координата контрольной точки дуги. </span><span class="sxs-lookup"><span data-stu-id="63b95-115">The  *y*  -coordinate of an arc's control point.</span></span>  <br/> |
|[<span data-ttu-id="63b95-116">C</span><span class="sxs-lookup"><span data-stu-id="63b95-116">C</span></span>](c-cell-geometry-section.md) <br/> |<span data-ttu-id="63b95-117">Угол основной оси дуги относительно  *оси x*  родительской оси.</span><span class="sxs-lookup"><span data-stu-id="63b95-117">The angle of an arc's major axis relative to the  *x*  -axis of its parent.</span></span>  <br/> |
|[<span data-ttu-id="63b95-118">D</span><span class="sxs-lookup"><span data-stu-id="63b95-118">D</span></span>](d-cell-geometry-section.md) <br/> |<span data-ttu-id="63b95-119">Отношение основной оси дуги к ее второстепенной оси.</span><span class="sxs-lookup"><span data-stu-id="63b95-119">The ratio of an arc's major axis to its minor axis.</span></span> <span data-ttu-id="63b95-120">Несмотря на обычное значение этих слов, "основная" ось не должна быть больше оси "minor", поэтому это соотношение не должно быть больше 1.</span><span class="sxs-lookup"><span data-stu-id="63b95-120">Despite the usual meaning of these words, the "major" axis does not have to be greater than the "minor" axis, so this ratio does not have to be greater than 1.</span></span> <span data-ttu-id="63b95-121">Установка для этой ячейки значения, меньшего или равного 0 или больше 1000, может привести к непредсказуемым результатам.</span><span class="sxs-lookup"><span data-stu-id="63b95-121">Setting this cell to a value less than or equal to 0 or greater than 1000 can lead to unpredictable results.</span></span>  <br/> |
   

