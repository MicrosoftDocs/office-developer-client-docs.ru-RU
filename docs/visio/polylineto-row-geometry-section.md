---
title: Строка PolylineTo (раздел геометрии)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251757
localization_priority: Normal
ms.assetid: b78a993f-4165-438d-39cf-9461b2877f17
description: Содержит x - и y-координаты последнего точки ломаной и ломаной формулы.
ms.openlocfilehash: 56cecb2eeaa1702461b1096fe468974f2f0b1f52
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19814388"
---
# <a name="polylineto-row-geometry-section"></a><span data-ttu-id="063f5-103">Строка PolylineTo (раздел геометрии)</span><span class="sxs-lookup"><span data-stu-id="063f5-103">PolylineTo Row (Geometry Section)</span></span>

<span data-ttu-id="063f5-104">Содержит *x* - и *y* -координаты последнего точки ломаной и ломаной формулы.</span><span class="sxs-lookup"><span data-stu-id="063f5-104">Contains  *x*  - and  *y*  -coordinates of the last point of a polyline and a polyline formula.</span></span> 
  
<span data-ttu-id="063f5-105">Строка PolylineTo содержит следующие ячейки.</span><span class="sxs-lookup"><span data-stu-id="063f5-105">A PolylineTo row contains the following cells.</span></span>
  
|<span data-ttu-id="063f5-106">**Cell**</span><span class="sxs-lookup"><span data-stu-id="063f5-106">**Cell**</span></span>|<span data-ttu-id="063f5-107">**Описание**</span><span class="sxs-lookup"><span data-stu-id="063f5-107">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="063f5-108">X</span><span class="sxs-lookup"><span data-stu-id="063f5-108">X</span></span>](x-cell-geometry-section.md) <br/> |<span data-ttu-id="063f5-109">*X* -координаты окончания вершины ломаной.</span><span class="sxs-lookup"><span data-stu-id="063f5-109">The  *x*  -coordinate of the ending vertex of a polyline.</span></span>  <br/> |
|[<span data-ttu-id="063f5-110">Y</span><span class="sxs-lookup"><span data-stu-id="063f5-110">Y</span></span>](y-cell-geometry-section.md) <br/> |<span data-ttu-id="063f5-111">*Y* -координат окончания вершины ломаной.</span><span class="sxs-lookup"><span data-stu-id="063f5-111">The  *y*  -coordinate of the ending vertex of a polyline.</span></span>  <br/> |
|[<span data-ttu-id="063f5-112">A</span><span class="sxs-lookup"><span data-stu-id="063f5-112">A</span></span>](a-cell-geometry-section.md) <br/> |<span data-ttu-id="063f5-113">Формула ломаной.</span><span class="sxs-lookup"><span data-stu-id="063f5-113">The polyline formula.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="063f5-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="063f5-114">Remarks</span></span>

<span data-ttu-id="063f5-115">Строки, представленные в виде строки ломаной эквивалентны на линии, представленные в виде последовательности строк LineTo, но ломаной строке эффективнее.</span><span class="sxs-lookup"><span data-stu-id="063f5-115">Lines represented as a Polyline row are equivalent to lines represented as a sequence of LineTo rows, but a Polyline row is more efficient.</span></span> <span data-ttu-id="063f5-116">Можно переместить строку PolylineTo LineTo строки, можно легко посмотреть Геометрия фигуры.</span><span class="sxs-lookup"><span data-stu-id="063f5-116">You can change a PolylineTo row to a LineTo row so you can easily see the shape geometry.</span></span> <span data-ttu-id="063f5-117">Для этого щелкните правой кнопкой мыши строку PolylineTo и нажмите кнопку **Развернуть строку** в контекстном меню.</span><span class="sxs-lookup"><span data-stu-id="063f5-117">To do this, right-click the PolylineTo row, and then click **Expand Row** on the shortcut menu.</span></span> 
  
<span data-ttu-id="063f5-118">Чтобы изменить тип строки на PolylineTo строку, щелкните правой кнопкой мыши строку и нажмите кнопку **Изменить тип строки** в контекстном меню.</span><span class="sxs-lookup"><span data-stu-id="063f5-118">To change a row type to a PolylineTo row, right-click the row, and then click **Change Row Type** on the shortcut menu.</span></span> 
  

