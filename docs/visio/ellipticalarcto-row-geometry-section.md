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
description: Содержит x и y-координаты конечной точки эллиптической дуги, x и y-координаты точек управления на дуге, угол от оси x до основной оси эллипса и соотношение между основными и небольшими осями эллипса.
ms.openlocfilehash: c6db7560a05652ca3bfcadb2fd4857ac39370562
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33421405"
---
# <a name="ellipticalarcto-row-geometry-section"></a><span data-ttu-id="50584-103">EllipticalArcTo Row (Geometry Section)</span><span class="sxs-lookup"><span data-stu-id="50584-103">EllipticalArcTo Row (Geometry Section)</span></span>

<span data-ttu-id="50584-104">Содержит  *x*  и  *y-координаты*  конечной точки эллиптической дуги,  *x*  и  *y-координаты*  точек управления на дуге, угол от оси  *x*  до основной оси эллипса и соотношение между основными и небольшими осями эллипса.</span><span class="sxs-lookup"><span data-stu-id="50584-104">Contains  *x*  - and  *y*  -coordinates of an elliptical arc's endpoint,  *x*  - and  *y*  -coordinates of the control points on the arc, angle from the  *x*  -axis to the ellipse's major axis, and ratio between the ellipse's major and minor axes.</span></span> 
  
<span data-ttu-id="50584-105">Строка EllipticalArcTo содержит следующие ячейки.</span><span class="sxs-lookup"><span data-stu-id="50584-105">An EllipticalArcTo row contains the following cells.</span></span>
  
|<span data-ttu-id="50584-106">**Cell**</span><span class="sxs-lookup"><span data-stu-id="50584-106">**Cell**</span></span>|<span data-ttu-id="50584-107">**Описание**</span><span class="sxs-lookup"><span data-stu-id="50584-107">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="50584-108">X</span><span class="sxs-lookup"><span data-stu-id="50584-108">X</span></span>](x-cell-geometry-section.md) <br/> |<span data-ttu-id="50584-109">X-координата конечной вершины на дуге. </span><span class="sxs-lookup"><span data-stu-id="50584-109">The  *x*  -coordinate of the ending vertex on an arc.</span></span>  <br/> |
|[<span data-ttu-id="50584-110">Да</span><span class="sxs-lookup"><span data-stu-id="50584-110">Y</span></span>](y-cell-geometry-section.md) <br/> |<span data-ttu-id="50584-111">Y-координата конечной вершины на дуге. </span><span class="sxs-lookup"><span data-stu-id="50584-111">The  *y*  -coordinate of the ending vertex on an arc.</span></span>  <br/> |
|[<span data-ttu-id="50584-112">A</span><span class="sxs-lookup"><span data-stu-id="50584-112">A</span></span>](a-cell-geometry-section.md) <br/> |<span data-ttu-id="50584-113">*X-координата* точки управления дуги; точка на дуге. Точка управления расположена на полпути между началом и окончанием вершин дуги. В противном случае дуга может вырасти до крайнего размера, чтобы пройти через точку управления с непредсказуемыми результатами.</span><span class="sxs-lookup"><span data-stu-id="50584-113">The  *x*  -coordinate of the arc's control point; a point on the arc. The control point is best located about halfway between the beginning and ending vertices of the arc. Otherwise, the arc may grow to an extreme size in order to pass through the control point, with unpredictable results.</span></span>  <br/> |
|[<span data-ttu-id="50584-114">B</span><span class="sxs-lookup"><span data-stu-id="50584-114">B</span></span>](b-cell-geometry-section.md) <br/> |<span data-ttu-id="50584-115">Y-координата точки управления дуги. </span><span class="sxs-lookup"><span data-stu-id="50584-115">The  *y*  -coordinate of an arc's control point.</span></span>  <br/> |
|[<span data-ttu-id="50584-116">C</span><span class="sxs-lookup"><span data-stu-id="50584-116">C</span></span>](c-cell-geometry-section.md) <br/> |<span data-ttu-id="50584-117">Угол основной оси дуги относительно  *оси x-axis*  родительской.</span><span class="sxs-lookup"><span data-stu-id="50584-117">The angle of an arc's major axis relative to the  *x*  -axis of its parent.</span></span>  <br/> |
|[<span data-ttu-id="50584-118">D</span><span class="sxs-lookup"><span data-stu-id="50584-118">D</span></span>](d-cell-geometry-section.md) <br/> |<span data-ttu-id="50584-119">Отношение основной оси дуги к ее малой оси.</span><span class="sxs-lookup"><span data-stu-id="50584-119">The ratio of an arc's major axis to its minor axis.</span></span> <span data-ttu-id="50584-120">Несмотря на обычное значение этих слов, "основная" ось не должна быть больше оси "minor", поэтому это соотношение не должно быть больше 1.</span><span class="sxs-lookup"><span data-stu-id="50584-120">Despite the usual meaning of these words, the "major" axis does not have to be greater than the "minor" axis, so this ratio does not have to be greater than 1.</span></span> <span data-ttu-id="50584-121">Установка этой ячейки на значение меньше 0 или более 1000 может привести к непредсказуемым результатам.</span><span class="sxs-lookup"><span data-stu-id="50584-121">Setting this cell to a value less than or equal to 0 or greater than 1000 can lead to unpredictable results.</span></span>  <br/> |
   

