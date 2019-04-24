---
title: PolylineTo Row (Geometry Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251757
localization_priority: Normal
ms.assetid: b78a993f-4165-438d-39cf-9461b2877f17
description: Содержит координаты x и y последней точки ломаной линии и формулы ломаной линии.
ms.openlocfilehash: 13e5bd7138103094f0f00ad0512e33e9e6ad5e7f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359831"
---
# <a name="polylineto-row-geometry-section"></a><span data-ttu-id="5db0d-103">PolylineTo Row (Geometry Section)</span><span class="sxs-lookup"><span data-stu-id="5db0d-103">PolylineTo Row (Geometry Section)</span></span>

<span data-ttu-id="5db0d-104">Содержит координаты *x* и *y* последней точки ломаной линии и формулы ломаной линии.</span><span class="sxs-lookup"><span data-stu-id="5db0d-104">Contains  *x*  - and  *y*  -coordinates of the last point of a polyline and a polyline formula.</span></span> 
  
<span data-ttu-id="5db0d-105">Строка С преЗначением В виде lineTo содержит следующие ячейки.</span><span class="sxs-lookup"><span data-stu-id="5db0d-105">A PolylineTo row contains the following cells.</span></span>
  
|<span data-ttu-id="5db0d-106">**Cell**</span><span class="sxs-lookup"><span data-stu-id="5db0d-106">**Cell**</span></span>|<span data-ttu-id="5db0d-107">**Описание**</span><span class="sxs-lookup"><span data-stu-id="5db0d-107">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="5db0d-108">X</span><span class="sxs-lookup"><span data-stu-id="5db0d-108">X</span></span>](x-cell-geometry-section.md) <br/> |<span data-ttu-id="5db0d-109">Координата *X* последней вершины ломаной линии.</span><span class="sxs-lookup"><span data-stu-id="5db0d-109">The  *x*  -coordinate of the ending vertex of a polyline.</span></span>  <br/> |
|[<span data-ttu-id="5db0d-110">Y (да)</span><span class="sxs-lookup"><span data-stu-id="5db0d-110">Y</span></span>](y-cell-geometry-section.md) <br/> |<span data-ttu-id="5db0d-111">Координата *Y* последней вершины ломаной линии.</span><span class="sxs-lookup"><span data-stu-id="5db0d-111">The  *y*  -coordinate of the ending vertex of a polyline.</span></span>  <br/> |
|[<span data-ttu-id="5db0d-112">А</span><span class="sxs-lookup"><span data-stu-id="5db0d-112">A</span></span>](a-cell-geometry-section.md) <br/> |<span data-ttu-id="5db0d-113">Формула ломаной линии.</span><span class="sxs-lookup"><span data-stu-id="5db0d-113">The polyline formula.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="5db0d-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="5db0d-114">Remarks</span></span>

<span data-ttu-id="5db0d-115">Линии, представленные в виде строки ломаной линии, эквивалентны строкам, представленным как последовательность строк LineTo, но строка ломаной линии более эффективна.</span><span class="sxs-lookup"><span data-stu-id="5db0d-115">Lines represented as a Polyline row are equivalent to lines represented as a sequence of LineTo rows, but a Polyline row is more efficient.</span></span> <span data-ttu-id="5db0d-116">Вы можете изменить строку lineTo на строку LineTo, чтобы можно было легко увидеть геометрию фигуры.</span><span class="sxs-lookup"><span data-stu-id="5db0d-116">You can change a PolylineTo row to a LineTo row so you can easily see the shape geometry.</span></span> <span data-ttu-id="5db0d-117">Для этого щелкните правой кнопкой мыши строку, а затем выберите **развернуть строку** в контекстном меню.</span><span class="sxs-lookup"><span data-stu-id="5db0d-117">To do this, right-click the PolylineTo row, and then click **Expand Row** on the shortcut menu.</span></span> 
  
<span data-ttu-id="5db0d-118">Чтобы изменить тип строки на строку, щелкните строку правой кнопкой мыши и выберите в контекстном меню команду **изменить тип строки** .</span><span class="sxs-lookup"><span data-stu-id="5db0d-118">To change a row type to a PolylineTo row, right-click the row, and then click **Change Row Type** on the shortcut menu.</span></span> 
  

