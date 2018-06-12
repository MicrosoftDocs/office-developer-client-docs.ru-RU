---
title: Строка RelCubBezTo (раздел геометрии)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 77777dd4-5a2c-4048-9ea4-9bd876862963
description: Содержит x - и y - координаты конечной точки кубические Безье график относительно фигуры ширину и высоту, x - и y - координат контрольной точки в начало фигуры график относительно ширины и высоты и x - и y-координаты элемент управления l точка конца фигуры график относительно ширины и высоты.
ms.openlocfilehash: 918701c19e36753dcbf1a210dda2234d1e540d6d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19814560"
---
# <a name="relcubbezto-row-geometry-section"></a><span data-ttu-id="24181-103">Строка RelCubBezTo (раздел геометрии)</span><span class="sxs-lookup"><span data-stu-id="24181-103">RelCubBezTo Row (Geometry Section)</span></span>

<span data-ttu-id="24181-104">Содержит *x* - и *y* - координаты конечной точки кубические Безье график относительно фигуры ширину и высоту, *x* - и *y* -координат контрольной точки в начало ширину и высоту фигуры относительно график и *x* - и *y* -координаты точки управления завершения фигуры график относительно ширины и высоты.</span><span class="sxs-lookup"><span data-stu-id="24181-104">Contains the  *x*  - and  *y*  -coordinates of the endpoint of a cubic Bézier curve relative to the shape's width and height, the  *x*  - and  *y*  -coordinates of the control point of the beginning of the curve relative shape's width and height, and the  *x*  - and  *y*  -coordinates of the control point of the ending of the curve relative shape's width and height.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="24181-105">Строка **RelCubBezTo** только могут быть сохранены в форматы файлов vsdx (en), .vsdm, .vstx, .vstm, .vssx и .vssm.</span><span class="sxs-lookup"><span data-stu-id="24181-105">A **RelCubBezTo** row can only be persisted in the .vsdx, .vsdm, .vstx, .vstm, .vssx, and .vssm file formats.</span></span> <span data-ttu-id="24181-106">При сохранении файла в Visio 2003-2010 форматы строки **RelCubBezTo** преобразуется в строку [NURBSTo](nurbsto-row-geometry-section.md) .</span><span class="sxs-lookup"><span data-stu-id="24181-106">When a file is saved to the Visio 2003-2010 formats, the **RelCubBezTo** row is converted to a [NURBSTo](nurbsto-row-geometry-section.md) row.</span></span> 
  
<span data-ttu-id="24181-107">Строка **RelCubBezTo** содержит следующие ячейки.</span><span class="sxs-lookup"><span data-stu-id="24181-107">A **RelCubBezTo** row contains the following cells.</span></span> 
  
|<span data-ttu-id="24181-108">**Cell**</span><span class="sxs-lookup"><span data-stu-id="24181-108">**Cell**</span></span>|<span data-ttu-id="24181-109">**Описание**</span><span class="sxs-lookup"><span data-stu-id="24181-109">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="24181-110">X</span><span class="sxs-lookup"><span data-stu-id="24181-110">X</span></span>](x-cell-geometry-section.md) <br/> |<span data-ttu-id="24181-111">*X* -координаты окончания вершины кубические Безье график ширине фигуры.</span><span class="sxs-lookup"><span data-stu-id="24181-111">The  *x*  -coordinate of the ending vertex of a cubic Bézier curve relative to the width of the shape.</span></span>  <br/> |
|[<span data-ttu-id="24181-112">Y</span><span class="sxs-lookup"><span data-stu-id="24181-112">Y</span></span>](y-cell-geometry-section.md) <br/> |<span data-ttu-id="24181-113">*Y* -координат окончания вершины кубические Безье график высоте фигуры.</span><span class="sxs-lookup"><span data-stu-id="24181-113">The  *y*  -coordinate of the ending vertex of a cubic Bézier curve relative to the height of the shape.</span></span>  <br/> |
|[<span data-ttu-id="24181-114">A</span><span class="sxs-lookup"><span data-stu-id="24181-114">A</span></span>](a-cell-geometry-section.md) <br/> |<span data-ttu-id="24181-115">*X* -координата график абонента Приступая к работе с контрольной точки относительно ширины фигуры; точка дуги. Контрольная точка лучше всего находится между начала и окончания грани дуги.</span><span class="sxs-lookup"><span data-stu-id="24181-115">The  *x*  -coordinate of the curve's beginning control point relative to the shape's width; a point on the arc. The control point is best located between the beginning and ending vertices of the arc.</span></span>  <br/> |
|[<span data-ttu-id="24181-116">B</span><span class="sxs-lookup"><span data-stu-id="24181-116">B</span></span>](b-cell-geometry-section.md) <br/> |<span data-ttu-id="24181-117">*Y* -координата график абонента Приступая к работе с контрольной точки высоте фигуры.</span><span class="sxs-lookup"><span data-stu-id="24181-117">The  *y*  -coordinate of a curve's beginning control point relative to the shape's height.</span></span>  <br/> |
|[<span data-ttu-id="24181-118">C</span><span class="sxs-lookup"><span data-stu-id="24181-118">C</span></span>](c-cell-geometry-section.md) <br/> |<span data-ttu-id="24181-119">*X* -координата график окончания точки управления ширине фигуры; точка дуги. Контрольная точка лучше всего находится между первый элемент управления точка и заканчивая грани дуги.</span><span class="sxs-lookup"><span data-stu-id="24181-119">The  *x*  -coordinate of the curve's ending control point relative to the shape's width; a point on the arc. The control point is best located between the beginning control point and ending vertices of the arc.</span></span>  <br/> |
|[<span data-ttu-id="24181-120">D</span><span class="sxs-lookup"><span data-stu-id="24181-120">D</span></span>](d-cell-geometry-section.md) <br/> |<span data-ttu-id="24181-121">*Y* -координата график окончания точки управления высоте фигуры.</span><span class="sxs-lookup"><span data-stu-id="24181-121">The  *y*  -coordinate of a curve's ending control point relative to the shape's height.</span></span>  <br/> |
   

