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
# <a name="ellipse-row-geometry-section"></a><span data-ttu-id="bdbb5-103">Ellipse Row (Geometry Section)</span><span class="sxs-lookup"><span data-stu-id="bdbb5-103">Ellipse Row (Geometry Section)</span></span>

<span data-ttu-id="bdbb5-104">Содержит координаты *x* и *y* центральной точки эллипса и две точки эллипса.</span><span class="sxs-lookup"><span data-stu-id="bdbb5-104">Contains the  *x*  - and  *y*  -coordinates of the ellipse's center point and two points on the ellipse.</span></span> 
  
<span data-ttu-id="bdbb5-105">Строка эллипса содержит следующие ячейки.</span><span class="sxs-lookup"><span data-stu-id="bdbb5-105">An Ellipse row contains the following cells.</span></span>
  
|<span data-ttu-id="bdbb5-106">**Cell**</span><span class="sxs-lookup"><span data-stu-id="bdbb5-106">**Cell**</span></span>|<span data-ttu-id="bdbb5-107">**Описание**</span><span class="sxs-lookup"><span data-stu-id="bdbb5-107">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="bdbb5-108">X</span><span class="sxs-lookup"><span data-stu-id="bdbb5-108">X</span></span>](x-cell-geometry-section.md) <br/> |<span data-ttu-id="bdbb5-109">Координата *x* центральной точки.</span><span class="sxs-lookup"><span data-stu-id="bdbb5-109">The  *x*  -coordinate of the center point.</span></span>  <br/> |
|[<span data-ttu-id="bdbb5-110">Y (да)</span><span class="sxs-lookup"><span data-stu-id="bdbb5-110">Y</span></span>](y-cell-geometry-section.md) <br/> |<span data-ttu-id="bdbb5-111">Координата *y* центральной точки.</span><span class="sxs-lookup"><span data-stu-id="bdbb5-111">The  *y*  -coordinate of the center point.</span></span>  <br/> |
|[<span data-ttu-id="bdbb5-112">A</span><span class="sxs-lookup"><span data-stu-id="bdbb5-112">A</span></span>](a-cell-geometry-section.md) <br/> |<span data-ttu-id="bdbb5-113">Координата x одной точки эллипса; Связывание с координатой *y* , представленной в ячейке B.</span><span class="sxs-lookup"><span data-stu-id="bdbb5-113">The x-coordinate of one point on the ellipse; paired with  *y*  -coordinate represented by the B cell.</span></span>  <br/> |
|[<span data-ttu-id="bdbb5-114">З</span><span class="sxs-lookup"><span data-stu-id="bdbb5-114">B</span></span>](b-cell-geometry-section.md) <br/> |<span data-ttu-id="bdbb5-115">Координата *y* одной точки эллипса; Связывание с координатой x, представленной ячейкой.</span><span class="sxs-lookup"><span data-stu-id="bdbb5-115">The  *y*  -coordinate of one point on the ellipse; paired with x-coordinate represented by the A cell.</span></span>  <br/> |
|[<span data-ttu-id="bdbb5-116">C</span><span class="sxs-lookup"><span data-stu-id="bdbb5-116">C</span></span>](c-cell-geometry-section.md) <br/> |<span data-ttu-id="bdbb5-117">Координата *x* другой точки эллипса; Связывание с координатой *y* , представленной ячейкой D.</span><span class="sxs-lookup"><span data-stu-id="bdbb5-117">The  *x*  -coordinate of another point on the ellipse; paired with  *y*  -coordinate represented by the D cell.</span></span>  <br/> |
|[<span data-ttu-id="bdbb5-118">D</span><span class="sxs-lookup"><span data-stu-id="bdbb5-118">D</span></span>](d-cell-geometry-section.md) <br/> |<span data-ttu-id="bdbb5-119">Координата *y* другой точки эллипса; Связывание с координатой *y* , представленной в ячейке C.</span><span class="sxs-lookup"><span data-stu-id="bdbb5-119">The  *y*  -coordinate of another point on the ellipse; paired with  *y*  -coordinate represented by the C cell.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="bdbb5-120">Примечания</span><span class="sxs-lookup"><span data-stu-id="bdbb5-120">Remarks</span></span>

<span data-ttu-id="bdbb5-121">Раздел геометрии, содержащий эллипс или строку строка infiniteline, не должен содержать других строк.</span><span class="sxs-lookup"><span data-stu-id="bdbb5-121">A geometry section that contains an Ellipse or an InfiniteLine row should not contain any other rows.</span></span>
  

