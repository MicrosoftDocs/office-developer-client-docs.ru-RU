---
title: NURBSTo Row (Geometry Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251758
localization_priority: Normal
ms.assetid: 7e47acfe-5ec0-3689-eb89-0168f596a739
description: Содержит координаты x и y, положение секунды с последним весом, положение последнего веса, положение первого веса, положение первого Кнот, положение первого веса и формула для неоднородного рационального B-сплайна (NURBS).
ms.openlocfilehash: a5fc83f9581277580d076c2a850bfe937602aef0
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33404717"
---
# <a name="nurbsto-row-geometry-section"></a><span data-ttu-id="ab6af-103">NURBSTo Row (Geometry Section)</span><span class="sxs-lookup"><span data-stu-id="ab6af-103">NURBSTo Row (Geometry Section)</span></span>

<span data-ttu-id="ab6af-104">Содержит координаты *x* и *y* , положение секунды с последним весом, положение последнего веса, положение первого веса, положение первого Кнот, положение первого веса и формула для неоднородного рационального B-сплайна (NURBS).</span><span class="sxs-lookup"><span data-stu-id="ab6af-104">Contains the  *x*  - and  *y*  -coordinates, position of the second to last knot, position of the last weight, position of the first knot, position of the first weight, and the formula for a nonuniform rational B-spline (NURBS).</span></span> 
  
<span data-ttu-id="ab6af-105">Строка NURBSTo содержит следующие ячейки.</span><span class="sxs-lookup"><span data-stu-id="ab6af-105">A NURBSTo row contains the following cells.</span></span>
  
|<span data-ttu-id="ab6af-106">**Cell**</span><span class="sxs-lookup"><span data-stu-id="ab6af-106">**Cell**</span></span>|<span data-ttu-id="ab6af-107">**Описание**</span><span class="sxs-lookup"><span data-stu-id="ab6af-107">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="ab6af-108">X</span><span class="sxs-lookup"><span data-stu-id="ab6af-108">X</span></span>](x-cell-geometry-section.md) <br/> |<span data-ttu-id="ab6af-109">Координата *x* последней контрольной точки объекта NURBS.</span><span class="sxs-lookup"><span data-stu-id="ab6af-109">The  *x*  -coordinate of the last control point of a NURBS.</span></span>  <br/> |
|[<span data-ttu-id="ab6af-110">Y (да)</span><span class="sxs-lookup"><span data-stu-id="ab6af-110">Y</span></span>](y-cell-geometry-section.md) <br/> |<span data-ttu-id="ab6af-111">Координата *y* последней контрольной точки объекта NURBS.</span><span class="sxs-lookup"><span data-stu-id="ab6af-111">The  *y*  -coordinate of the last control point of a NURBS.</span></span>  <br/> |
|[<span data-ttu-id="ab6af-112">Определенно</span><span class="sxs-lookup"><span data-stu-id="ab6af-112">A</span></span>](a-cell-geometry-section.md) <br/> |<span data-ttu-id="ab6af-113">Второе значение к последнему кноту NURBS.</span><span class="sxs-lookup"><span data-stu-id="ab6af-113">The second to the last knot of the NURBS.</span></span>  <br/> |
|[<span data-ttu-id="ab6af-114">З</span><span class="sxs-lookup"><span data-stu-id="ab6af-114">B</span></span>](b-cell-geometry-section.md) <br/> |<span data-ttu-id="ab6af-115">Последний вес NURBS.</span><span class="sxs-lookup"><span data-stu-id="ab6af-115">The last weight of the NURBS.</span></span>  <br/> |
|[<span data-ttu-id="ab6af-116">C</span><span class="sxs-lookup"><span data-stu-id="ab6af-116">C</span></span>](c-cell-geometry-section.md) <br/> |<span data-ttu-id="ab6af-117">Первый кнот NURBS.</span><span class="sxs-lookup"><span data-stu-id="ab6af-117">The first knot of the NURBS.</span></span>  <br/> |
|[<span data-ttu-id="ab6af-118">D</span><span class="sxs-lookup"><span data-stu-id="ab6af-118">D</span></span>](d-cell-geometry-section.md) <br/> |<span data-ttu-id="ab6af-119">Первый вес объекта NURBS.</span><span class="sxs-lookup"><span data-stu-id="ab6af-119">The first weight of the NURBS.</span></span>  <br/> |
|[<span data-ttu-id="ab6af-120">E</span><span class="sxs-lookup"><span data-stu-id="ab6af-120">E</span></span>](e-cell-geometry-section.md) <br/> |<span data-ttu-id="ab6af-121">Формула NURBS.</span><span class="sxs-lookup"><span data-stu-id="ab6af-121">A NURBS formula.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ab6af-122">Примечания</span><span class="sxs-lookup"><span data-stu-id="ab6af-122">Remarks</span></span>

<span data-ttu-id="ab6af-123">NURBS — это распространенный способ математического представления кривой.</span><span class="sxs-lookup"><span data-stu-id="ab6af-123">NURBS is a common way to represent a curve mathematically.</span></span> <span data-ttu-id="ab6af-124">Вы можете создать NURBS с помощью инструмента " **Полилиния** ".</span><span class="sxs-lookup"><span data-stu-id="ab6af-124">You can create a NURBS with the **Freeform** tool.</span></span> 
  

