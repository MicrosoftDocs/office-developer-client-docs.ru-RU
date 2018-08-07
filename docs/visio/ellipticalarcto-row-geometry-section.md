---
title: Строка EllipticalArcTo (раздел "Геометрия")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm3015
localization_priority: Normal
ms.assetid: 7ceb30a8-1d05-feff-35d8-08a198784a27
description: Содержит x - и y-координаты руководство пользователя конечной точки, x - и y-координаты контрольные точки на дуги, угол из x-ось главных осей эллипса и отношение между эллипса основной и дополнительной осей.
ms.openlocfilehash: 9a356429f14a20b72a8bd55689855e2954d4a807
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19813679"
---
# <a name="ellipticalarcto-row-geometry-section"></a><span data-ttu-id="089d5-103">Строка EllipticalArcTo (раздел "Геометрия")</span><span class="sxs-lookup"><span data-stu-id="089d5-103">EllipticalArcTo Row (Geometry Section)</span></span>

<span data-ttu-id="089d5-104">Содержит *x* - и *y* - координаты руководство конечную точку, *x* - и *y* -координаты контрольные точки на дуги, угол из *x* -ось главных осей эллипса и отношение между эллипса основную и промежуточные r осей.</span><span class="sxs-lookup"><span data-stu-id="089d5-104">Contains  *x*  - and  *y*  -coordinates of an elliptical arc's endpoint,  *x*  - and  *y*  -coordinates of the control points on the arc, angle from the  *x*  -axis to the ellipse's major axis, and ratio between the ellipse's major and minor axes.</span></span> 
  
<span data-ttu-id="089d5-105">Строка EllipticalArcTo содержит следующие ячеек.</span><span class="sxs-lookup"><span data-stu-id="089d5-105">An EllipticalArcTo row contains the following cells.</span></span>
  
|<span data-ttu-id="089d5-106">**Cell**</span><span class="sxs-lookup"><span data-stu-id="089d5-106">**Cell**</span></span>|<span data-ttu-id="089d5-107">**Описание**</span><span class="sxs-lookup"><span data-stu-id="089d5-107">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="089d5-108">X</span><span class="sxs-lookup"><span data-stu-id="089d5-108">X</span></span>](x-cell-geometry-section.md) <br/> |<span data-ttu-id="089d5-109">*X* -координаты окончания вершины на дугу.</span><span class="sxs-lookup"><span data-stu-id="089d5-109">The  *x*  -coordinate of the ending vertex on an arc.</span></span>  <br/> |
|[<span data-ttu-id="089d5-110">Да</span><span class="sxs-lookup"><span data-stu-id="089d5-110">Y</span></span>](y-cell-geometry-section.md) <br/> |<span data-ttu-id="089d5-111">*Y* -координат окончания вершины на дугу.</span><span class="sxs-lookup"><span data-stu-id="089d5-111">The  *y*  -coordinate of the ending vertex on an arc.</span></span>  <br/> |
|[<span data-ttu-id="089d5-112">A</span><span class="sxs-lookup"><span data-stu-id="089d5-112">A</span></span>](a-cell-geometry-section.md) <br/> |<span data-ttu-id="089d5-113">*X* -координата точки управления дуги; точка дуги. Контрольная точка расположена лучше всего о пользователю между начала и окончания грани дуги. В противном случае дуги может расти в размерах чрезмерную размера для передачи через точку управления с непредсказуемым последствиям.</span><span class="sxs-lookup"><span data-stu-id="089d5-113">The  *x*  -coordinate of the arc's control point; a point on the arc. The control point is best located about halfway between the beginning and ending vertices of the arc. Otherwise, the arc may grow to an extreme size in order to pass through the control point, with unpredictable results.</span></span>  <br/> |
|[<span data-ttu-id="089d5-114">B</span><span class="sxs-lookup"><span data-stu-id="089d5-114">B</span></span>](b-cell-geometry-section.md) <br/> |<span data-ttu-id="089d5-115">*Y* -координата точки управления arc.</span><span class="sxs-lookup"><span data-stu-id="089d5-115">The  *y*  -coordinate of an arc's control point.</span></span>  <br/> |
|[<span data-ttu-id="089d5-116">C</span><span class="sxs-lookup"><span data-stu-id="089d5-116">C</span></span>](c-cell-geometry-section.md) <br/> |<span data-ttu-id="089d5-117">Угол дуги главных осей относительно *x* -ось родительского элемента.</span><span class="sxs-lookup"><span data-stu-id="089d5-117">The angle of an arc's major axis relative to the  *x*  -axis of its parent.</span></span>  <br/> |
|[<span data-ttu-id="089d5-118">D</span><span class="sxs-lookup"><span data-stu-id="089d5-118">D</span></span>](d-cell-geometry-section.md) <br/> |<span data-ttu-id="089d5-119">Отношение arc главных осей его вспомогательные оси.</span><span class="sxs-lookup"><span data-stu-id="089d5-119">The ratio of an arc's major axis to its minor axis.</span></span> <span data-ttu-id="089d5-120">Несмотря на обычных значение из этих слов, должно быть больше оси «дополнительный номер», поэтому этот коэффициент не должен быть больше 1 имеет оси «основные».</span><span class="sxs-lookup"><span data-stu-id="089d5-120">Despite the usual meaning of these words, the "major" axis does not have to be greater than the "minor" axis, so this ratio does not have to be greater than 1.</span></span> <span data-ttu-id="089d5-121">Установка для этой ячейки значение меньше или равно 0 или выше, чем 1000 может привести к непредсказуемым последствиям.</span><span class="sxs-lookup"><span data-stu-id="089d5-121">Setting this cell to a value less than or equal to 0 or greater than 1000 can lead to unpredictable results.</span></span>  <br/> |
   

