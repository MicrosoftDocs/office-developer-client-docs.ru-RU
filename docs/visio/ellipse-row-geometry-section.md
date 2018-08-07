---
title: Строка Ellipse (раздел "Геометрия")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm3010
localization_priority: Normal
ms.assetid: 183fb303-4acb-a486-7b97-f11f7ae3978f
description: Содержит x - и y-координаты центра эллипса и двумя точками на эллипс.
ms.openlocfilehash: 0a2acb0efa20f67d04581f827edbfc4fb4a2d6b0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19813677"
---
# <a name="ellipse-row-geometry-section"></a><span data-ttu-id="a5615-103">Строка Ellipse (раздел "Геометрия")</span><span class="sxs-lookup"><span data-stu-id="a5615-103">Ellipse Row (Geometry Section)</span></span>

<span data-ttu-id="a5615-104">Содержит *x* - и *y* -координаты центра эллипса и двумя точками на эллипс.</span><span class="sxs-lookup"><span data-stu-id="a5615-104">Contains the  *x*  - and  *y*  -coordinates of the ellipse's center point and two points on the ellipse.</span></span> 
  
<span data-ttu-id="a5615-105">Строка эллипс содержит следующие ячеек.</span><span class="sxs-lookup"><span data-stu-id="a5615-105">An Ellipse row contains the following cells.</span></span>
  
|<span data-ttu-id="a5615-106">**Cell**</span><span class="sxs-lookup"><span data-stu-id="a5615-106">**Cell**</span></span>|<span data-ttu-id="a5615-107">**Описание**</span><span class="sxs-lookup"><span data-stu-id="a5615-107">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="a5615-108">X</span><span class="sxs-lookup"><span data-stu-id="a5615-108">X</span></span>](x-cell-geometry-section.md) <br/> |<span data-ttu-id="a5615-109">*X* -координаты центральной точки.</span><span class="sxs-lookup"><span data-stu-id="a5615-109">The  *x*  -coordinate of the center point.</span></span>  <br/> |
|[<span data-ttu-id="a5615-110">Да</span><span class="sxs-lookup"><span data-stu-id="a5615-110">Y</span></span>](y-cell-geometry-section.md) <br/> |<span data-ttu-id="a5615-111">*Y* -координат центральной точки.</span><span class="sxs-lookup"><span data-stu-id="a5615-111">The  *y*  -coordinate of the center point.</span></span>  <br/> |
|[<span data-ttu-id="a5615-112">A</span><span class="sxs-lookup"><span data-stu-id="a5615-112">A</span></span>](a-cell-geometry-section.md) <br/> |<span data-ttu-id="a5615-113">X координата одной точки на эллипс; в сочетании с *y* -координата, представленное B ячейки.</span><span class="sxs-lookup"><span data-stu-id="a5615-113">The x-coordinate of one point on the ellipse; paired with  *y*  -coordinate represented by the B cell.</span></span>  <br/> |
|[<span data-ttu-id="a5615-114">B</span><span class="sxs-lookup"><span data-stu-id="a5615-114">B</span></span>](b-cell-geometry-section.md) <br/> |<span data-ttu-id="a5615-115">*Y* -координата одной точки на эллипс; в сочетании с представленной ячейке по оси x.</span><span class="sxs-lookup"><span data-stu-id="a5615-115">The  *y*  -coordinate of one point on the ellipse; paired with x-coordinate represented by the A cell.</span></span>  <br/> |
|[<span data-ttu-id="a5615-116">C</span><span class="sxs-lookup"><span data-stu-id="a5615-116">C</span></span>](c-cell-geometry-section.md) <br/> |<span data-ttu-id="a5615-117">*X* -координаты другой точки на эллипс; в сочетании с *y* -координата, представленного в ячейке D.</span><span class="sxs-lookup"><span data-stu-id="a5615-117">The  *x*  -coordinate of another point on the ellipse; paired with  *y*  -coordinate represented by the D cell.</span></span>  <br/> |
|[<span data-ttu-id="a5615-118">D</span><span class="sxs-lookup"><span data-stu-id="a5615-118">D</span></span>](d-cell-geometry-section.md) <br/> |<span data-ttu-id="a5615-119">*Y* -координат другой точки на эллипс; в сочетании с *y* -координата, представленный в ячейку C.</span><span class="sxs-lookup"><span data-stu-id="a5615-119">The  *y*  -coordinate of another point on the ellipse; paired with  *y*  -coordinate represented by the C cell.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a5615-120">Замечания</span><span class="sxs-lookup"><span data-stu-id="a5615-120">Remarks</span></span>

<span data-ttu-id="a5615-121">Раздел геометрии содержит эллипсы или строке InfiniteLine не должен содержать других строк.</span><span class="sxs-lookup"><span data-stu-id="a5615-121">A geometry section that contains an Ellipse or an InfiniteLine row should not contain any other rows.</span></span>
  

