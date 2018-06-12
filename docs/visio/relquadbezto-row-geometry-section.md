---
title: Строка RelQuadBezTo (раздел геометрии)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 5ae57707-5a50-43f0-8c78-516790b5034e
description: Содержит x - и y - координаты конечной точки кривая Безье относительно фигуры ширину и высоту и x - и y-координаты точки управления фигуры график относительно ширины и высоты.
ms.openlocfilehash: 99796e85a857fd320598cb48993fc29bdfa4964d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19814608"
---
# <a name="relquadbezto-row-geometry-section"></a><span data-ttu-id="3b631-103">Строка RelQuadBezTo (раздел геометрии)</span><span class="sxs-lookup"><span data-stu-id="3b631-103">RelQuadBezTo Row (Geometry Section)</span></span>

<span data-ttu-id="3b631-104">Содержит *x* - и *y* - координаты конечной точки кривая Безье относительно фигуры ширину и высоту и *x* - и *y* -координаты точки управления фигуры график относительно ширины и высоты.</span><span class="sxs-lookup"><span data-stu-id="3b631-104">Contains the  *x*  - and  *y*  -coordinates of the endpoint of a quadratic Bézier curve relative to the shape's width and height and the  *x*  - and  *y*  -coordinates of the control point of the curve relative shape's width and height.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="3b631-105">Строка **RelQuadBezTo** только могут быть сохранены в форматы файлов vsdx (en), .vsdm, .vstx, .vstm, .vssx и .vssm.</span><span class="sxs-lookup"><span data-stu-id="3b631-105">A **RelQuadBezTo** row can only be persisted in the .vsdx, .vsdm, .vstx, .vstm, .vssx, and .vssm file formats.</span></span> <span data-ttu-id="3b631-106">При сохранении файла в Visio 2003-2010 форматы строки **RelQuadBezTo** преобразуется в строку [NURBSTo](nurbsto-row-geometry-section.md) .</span><span class="sxs-lookup"><span data-stu-id="3b631-106">When a file is saved to the Visio 2003-2010 formats, the **RelQuadBezTo** row is converted to a [NURBSTo](nurbsto-row-geometry-section.md) row.</span></span> 
  
<span data-ttu-id="3b631-107">Строка **RelQuadBezTo** содержит следующие ячейки.</span><span class="sxs-lookup"><span data-stu-id="3b631-107">A **RelQuadBezTo** row contains the following cells.</span></span> 
  
|<span data-ttu-id="3b631-108">**Cell**</span><span class="sxs-lookup"><span data-stu-id="3b631-108">**Cell**</span></span>|<span data-ttu-id="3b631-109">**Описание**</span><span class="sxs-lookup"><span data-stu-id="3b631-109">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="3b631-110">X</span><span class="sxs-lookup"><span data-stu-id="3b631-110">X</span></span>](x-cell-geometry-section.md) <br/> |<span data-ttu-id="3b631-111">*X* -координаты окончания вершины кривая Безье ширине фигуры.</span><span class="sxs-lookup"><span data-stu-id="3b631-111">The  *x*  -coordinate of the ending vertex of a quadratic Bézier curve relative to the width of the shape.</span></span>  <br/> |
|[<span data-ttu-id="3b631-112">Y</span><span class="sxs-lookup"><span data-stu-id="3b631-112">Y</span></span>](y-cell-geometry-section.md) <br/> |<span data-ttu-id="3b631-113">*Y* -координат окончания вершины кривая Безье высоте фигуры.</span><span class="sxs-lookup"><span data-stu-id="3b631-113">The  *y*  -coordinate of the ending vertex of a quadratic Bézier curve relative to the height of the shape.</span></span>  <br/> |
|[<span data-ttu-id="3b631-114">A</span><span class="sxs-lookup"><span data-stu-id="3b631-114">A</span></span>](a-cell-geometry-section.md) <br/> |<span data-ttu-id="3b631-115">*X* -координата точки управления график ширине фигуры; точка дуги. Контрольная точка расположена лучше всего о пользователю между начала и окончания грани дуги.</span><span class="sxs-lookup"><span data-stu-id="3b631-115">The  *x*  -coordinate of the curve's control point relative to the shape's width; a point on the arc. The control point is best located about halfway between the beginning and ending vertices of the arc.</span></span>  <br/> |
|[<span data-ttu-id="3b631-116">B</span><span class="sxs-lookup"><span data-stu-id="3b631-116">B</span></span>](b-cell-geometry-section.md) <br/> |<span data-ttu-id="3b631-117">*Y* -координата точки управления график высоте фигуры.</span><span class="sxs-lookup"><span data-stu-id="3b631-117">The  *y*  -coordinate of a curve's control point relative to the shape's height.</span></span>  <br/> |
   

