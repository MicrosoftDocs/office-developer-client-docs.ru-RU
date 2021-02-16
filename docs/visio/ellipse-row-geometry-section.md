---
title: Ellipse Row (Geometry Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm3010
localization_priority: Normal
ms.assetid: 183fb303-4acb-a486-7b97-f11f7ae3978f
description: Содержит координаты x и y центральной точки эллипса и две точки эллипса.
ms.openlocfilehash: 5121ba0c7bf97eaeaaf8a438dd40eccddada4362
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33421832"
---
# <a name="ellipse-row-geometry-section"></a><span data-ttu-id="d9cdb-103">Ellipse Row (Geometry Section)</span><span class="sxs-lookup"><span data-stu-id="d9cdb-103">Ellipse Row (Geometry Section)</span></span>

<span data-ttu-id="d9cdb-104">Содержит  *координаты x*  и  *y*  центральной точки эллипса и две точки эллипса.</span><span class="sxs-lookup"><span data-stu-id="d9cdb-104">Contains the  *x*  - and  *y*  -coordinates of the ellipse's center point and two points on the ellipse.</span></span> 
  
<span data-ttu-id="d9cdb-105">Строка Ellipse содержит следующие ячейки.</span><span class="sxs-lookup"><span data-stu-id="d9cdb-105">An Ellipse row contains the following cells.</span></span>
  
|<span data-ttu-id="d9cdb-106">**Cell**</span><span class="sxs-lookup"><span data-stu-id="d9cdb-106">**Cell**</span></span>|<span data-ttu-id="d9cdb-107">**Описание**</span><span class="sxs-lookup"><span data-stu-id="d9cdb-107">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="d9cdb-108">X</span><span class="sxs-lookup"><span data-stu-id="d9cdb-108">X</span></span>](x-cell-geometry-section.md) <br/> |<span data-ttu-id="d9cdb-109">X-координата центральной точки. </span><span class="sxs-lookup"><span data-stu-id="d9cdb-109">The  *x*  -coordinate of the center point.</span></span>  <br/> |
|[<span data-ttu-id="d9cdb-110">Y</span><span class="sxs-lookup"><span data-stu-id="d9cdb-110">Y</span></span>](y-cell-geometry-section.md) <br/> |<span data-ttu-id="d9cdb-111">Координата  *Y*  центральной точки.</span><span class="sxs-lookup"><span data-stu-id="d9cdb-111">The  *y*  -coordinate of the center point.</span></span>  <br/> |
|[<span data-ttu-id="d9cdb-112">A</span><span class="sxs-lookup"><span data-stu-id="d9cdb-112">A</span></span>](a-cell-geometry-section.md) <br/> |<span data-ttu-id="d9cdb-113">X-координата одной точки на эллипсе; в паре  *с координатой y,*  представленной ячейкой B.</span><span class="sxs-lookup"><span data-stu-id="d9cdb-113">The x-coordinate of one point on the ellipse; paired with  *y*  -coordinate represented by the B cell.</span></span>  <br/> |
|[<span data-ttu-id="d9cdb-114">B</span><span class="sxs-lookup"><span data-stu-id="d9cdb-114">B</span></span>](b-cell-geometry-section.md) <br/> |<span data-ttu-id="d9cdb-115">Y-координата одной точки на эллипсе;  в паре с X-координатой, представленной ячейкой A.</span><span class="sxs-lookup"><span data-stu-id="d9cdb-115">The  *y*  -coordinate of one point on the ellipse; paired with x-coordinate represented by the A cell.</span></span>  <br/> |
|[<span data-ttu-id="d9cdb-116">C</span><span class="sxs-lookup"><span data-stu-id="d9cdb-116">C</span></span>](c-cell-geometry-section.md) <br/> |<span data-ttu-id="d9cdb-117">X-координата другой точки на эллипсе;  сопряжено с *координатой y,* представленной ячейкой D.</span><span class="sxs-lookup"><span data-stu-id="d9cdb-117">The  *x*  -coordinate of another point on the ellipse; paired with  *y*  -coordinate represented by the D cell.</span></span>  <br/> |
|[<span data-ttu-id="d9cdb-118">D</span><span class="sxs-lookup"><span data-stu-id="d9cdb-118">D</span></span>](d-cell-geometry-section.md) <br/> |<span data-ttu-id="d9cdb-119">Y-координата другой точки на эллипсе;  сопряжено с *координатой y,* представленной ячейкой C.</span><span class="sxs-lookup"><span data-stu-id="d9cdb-119">The  *y*  -coordinate of another point on the ellipse; paired with  *y*  -coordinate represented by the C cell.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d9cdb-120">Примечания</span><span class="sxs-lookup"><span data-stu-id="d9cdb-120">Remarks</span></span>

<span data-ttu-id="d9cdb-121">Раздел геометрии, содержащий строку Ellipse или InfiniteLine, не должен содержать другие строки.</span><span class="sxs-lookup"><span data-stu-id="d9cdb-121">A geometry section that contains an Ellipse or an InfiniteLine row should not contain any other rows.</span></span>
  

