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
description: Содержит x и y-координаты, положение второго до последнего узла, положение последнего веса, положение первого узла, положение первого веса и формулу для неинформированной рациональной B-spline (NURBS).
ms.openlocfilehash: a5fc83f9581277580d076c2a850bfe937602aef0
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33404717"
---
# <a name="nurbsto-row-geometry-section"></a><span data-ttu-id="db625-103">NURBSTo Row (Geometry Section)</span><span class="sxs-lookup"><span data-stu-id="db625-103">NURBSTo Row (Geometry Section)</span></span>

<span data-ttu-id="db625-104">Содержит  *x*  и  *y-координаты,*  положение второго до последнего узла, положение последнего веса, положение первого узла, положение первого веса и формулу для неинформированной рациональной B-spline (NURBS).</span><span class="sxs-lookup"><span data-stu-id="db625-104">Contains the  *x*  - and  *y*  -coordinates, position of the second to last knot, position of the last weight, position of the first knot, position of the first weight, and the formula for a nonuniform rational B-spline (NURBS).</span></span> 
  
<span data-ttu-id="db625-105">Строка NURBSTo содержит следующие ячейки.</span><span class="sxs-lookup"><span data-stu-id="db625-105">A NURBSTo row contains the following cells.</span></span>
  
|<span data-ttu-id="db625-106">**Cell**</span><span class="sxs-lookup"><span data-stu-id="db625-106">**Cell**</span></span>|<span data-ttu-id="db625-107">**Описание**</span><span class="sxs-lookup"><span data-stu-id="db625-107">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="db625-108">X</span><span class="sxs-lookup"><span data-stu-id="db625-108">X</span></span>](x-cell-geometry-section.md) <br/> |<span data-ttu-id="db625-109">X-координата последней точки управления NURBS. </span><span class="sxs-lookup"><span data-stu-id="db625-109">The  *x*  -coordinate of the last control point of a NURBS.</span></span>  <br/> |
|[<span data-ttu-id="db625-110">Да</span><span class="sxs-lookup"><span data-stu-id="db625-110">Y</span></span>](y-cell-geometry-section.md) <br/> |<span data-ttu-id="db625-111">Y-координата последней точки управления NURBS. </span><span class="sxs-lookup"><span data-stu-id="db625-111">The  *y*  -coordinate of the last control point of a NURBS.</span></span>  <br/> |
|[<span data-ttu-id="db625-112">A</span><span class="sxs-lookup"><span data-stu-id="db625-112">A</span></span>](a-cell-geometry-section.md) <br/> |<span data-ttu-id="db625-113">Второй до последнего узла NURBS.</span><span class="sxs-lookup"><span data-stu-id="db625-113">The second to the last knot of the NURBS.</span></span>  <br/> |
|[<span data-ttu-id="db625-114">B</span><span class="sxs-lookup"><span data-stu-id="db625-114">B</span></span>](b-cell-geometry-section.md) <br/> |<span data-ttu-id="db625-115">Последний вес NURBS.</span><span class="sxs-lookup"><span data-stu-id="db625-115">The last weight of the NURBS.</span></span>  <br/> |
|[<span data-ttu-id="db625-116">C</span><span class="sxs-lookup"><span data-stu-id="db625-116">C</span></span>](c-cell-geometry-section.md) <br/> |<span data-ttu-id="db625-117">Первый узел NURBS.</span><span class="sxs-lookup"><span data-stu-id="db625-117">The first knot of the NURBS.</span></span>  <br/> |
|[<span data-ttu-id="db625-118">D</span><span class="sxs-lookup"><span data-stu-id="db625-118">D</span></span>](d-cell-geometry-section.md) <br/> |<span data-ttu-id="db625-119">Первый вес NURBS.</span><span class="sxs-lookup"><span data-stu-id="db625-119">The first weight of the NURBS.</span></span>  <br/> |
|[<span data-ttu-id="db625-120">E</span><span class="sxs-lookup"><span data-stu-id="db625-120">E</span></span>](e-cell-geometry-section.md) <br/> |<span data-ttu-id="db625-121">Формула NURBS.</span><span class="sxs-lookup"><span data-stu-id="db625-121">A NURBS formula.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="db625-122">Примечания</span><span class="sxs-lookup"><span data-stu-id="db625-122">Remarks</span></span>

<span data-ttu-id="db625-123">NURBS — это распространенный способ математического представления кривой.</span><span class="sxs-lookup"><span data-stu-id="db625-123">NURBS is a common way to represent a curve mathematically.</span></span> <span data-ttu-id="db625-124">Можно создать NURBS с помощью средства **Freeform.**</span><span class="sxs-lookup"><span data-stu-id="db625-124">You can create a NURBS with the **Freeform** tool.</span></span> 
  

