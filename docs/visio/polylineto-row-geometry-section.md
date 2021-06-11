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
description: Содержит x и y-координаты последней точки полилиновой и полилиновой формулы.
ms.openlocfilehash: 13e5bd7138103094f0f00ad0512e33e9e6ad5e7f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439466"
---
# <a name="polylineto-row-geometry-section"></a><span data-ttu-id="73b3f-103">PolylineTo Row (Geometry Section)</span><span class="sxs-lookup"><span data-stu-id="73b3f-103">PolylineTo Row (Geometry Section)</span></span>

<span data-ttu-id="73b3f-104">Содержит  *x*  и  *y-координаты*  последней точки полилиновой и полилиновой формулы.</span><span class="sxs-lookup"><span data-stu-id="73b3f-104">Contains  *x*  - and  *y*  -coordinates of the last point of a polyline and a polyline formula.</span></span> 
  
<span data-ttu-id="73b3f-105">Строка PolylineTo содержит следующие ячейки.</span><span class="sxs-lookup"><span data-stu-id="73b3f-105">A PolylineTo row contains the following cells.</span></span>
  
|<span data-ttu-id="73b3f-106">**Cell**</span><span class="sxs-lookup"><span data-stu-id="73b3f-106">**Cell**</span></span>|<span data-ttu-id="73b3f-107">**Описание**</span><span class="sxs-lookup"><span data-stu-id="73b3f-107">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="73b3f-108">X</span><span class="sxs-lookup"><span data-stu-id="73b3f-108">X</span></span>](x-cell-geometry-section.md) <br/> |<span data-ttu-id="73b3f-109">Координата *X* последней вершины ломаной линии.</span><span class="sxs-lookup"><span data-stu-id="73b3f-109">The  *x*  -coordinate of the ending vertex of a polyline.</span></span>  <br/> |
|[<span data-ttu-id="73b3f-110">Да</span><span class="sxs-lookup"><span data-stu-id="73b3f-110">Y</span></span>](y-cell-geometry-section.md) <br/> |<span data-ttu-id="73b3f-111">Координата *Y* последней вершины ломаной линии.</span><span class="sxs-lookup"><span data-stu-id="73b3f-111">The  *y*  -coordinate of the ending vertex of a polyline.</span></span>  <br/> |
|[<span data-ttu-id="73b3f-112">A</span><span class="sxs-lookup"><span data-stu-id="73b3f-112">A</span></span>](a-cell-geometry-section.md) <br/> |<span data-ttu-id="73b3f-113">Формула полилинов.</span><span class="sxs-lookup"><span data-stu-id="73b3f-113">The polyline formula.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="73b3f-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="73b3f-114">Remarks</span></span>

<span data-ttu-id="73b3f-115">Строки, представленные в качестве строки Polyline, эквивалентны строкам, представленным в качестве последовательности строк LineTo, но строка Polyline эффективнее.</span><span class="sxs-lookup"><span data-stu-id="73b3f-115">Lines represented as a Polyline row are equivalent to lines represented as a sequence of LineTo rows, but a Polyline row is more efficient.</span></span> <span data-ttu-id="73b3f-116">Вы можете изменить строку PolylineTo на строку LineTo, чтобы можно было легко увидеть геометрию фигуры.</span><span class="sxs-lookup"><span data-stu-id="73b3f-116">You can change a PolylineTo row to a LineTo row so you can easily see the shape geometry.</span></span> <span data-ttu-id="73b3f-117">Чтобы сделать это, щелкните правой кнопкой мыши строку PolylineTo, а затем щелкните **Расширение строки** в меню ярлыка.</span><span class="sxs-lookup"><span data-stu-id="73b3f-117">To do this, right-click the PolylineTo row, and then click **Expand Row** on the shortcut menu.</span></span> 
  
<span data-ttu-id="73b3f-118">Чтобы изменить тип строки на строку PolylineTo, щелкните правой кнопкой мыши строку и нажмите кнопку **Изменить** тип строки в меню ярлыка.</span><span class="sxs-lookup"><span data-stu-id="73b3f-118">To change a row type to a PolylineTo row, right-click the row, and then click **Change Row Type** on the shortcut menu.</span></span> 
  

