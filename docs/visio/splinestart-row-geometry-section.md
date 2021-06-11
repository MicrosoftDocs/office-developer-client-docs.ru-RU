---
title: SplineStart Row (Geometry Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm3055
localization_priority: Normal
ms.assetid: 8e327e00-0844-efa4-900b-6954d3b009bb
description: Содержит x и y-координаты для второй точки управления spline, ее второго узла, первого узла, последнего узла и степени spline.
ms.openlocfilehash: 2ec06619770af4e5dbcc1a763595b6e01a39052b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33417478"
---
# <a name="splinestart-row-geometry-section"></a>SplineStart Row (Geometry Section)

Содержит  *x*  и  *y-координаты*  для второй точки управления spline, ее второго узла, первого узла, последнего узла и степени spline. 
  
Строка SplineStart содержит следующие ячейки.
  
|**Cell**|**Описание**|
|:-----|:-----|
|[X](x-cell-geometry-section.md) <br/> |Координата *X* второй контрольной точки сплайна.  <br/> |
|[Да](y-cell-geometry-section.md) <br/> |Координата *Y* второй контрольной точки сплайна.  <br/> |
|[A](a-cell-geometry-section.md) <br/> |Второй узел spline.  <br/> |
|[B](b-cell-geometry-section.md) <br/> |Первый узел spline.  <br/> |
|[C](c-cell-geometry-section.md) <br/> |Последний узел spline.  <br/> |
|[D](d-cell-geometry-section.md) <br/> |Степень spline (integer от 1 до 25).  <br/> |
   
## <a name="remarks"></a>Примечания

Visio отображает определение spline в разделе Геометрия, содержаще строку SplineStart, а затем одну или несколько строк SplineKnot. Строке SplineStart должен предшествовать другой вид строки, например строка MoveTo, чтобы указать первую точку управления spline. В предыдущей строке может быть строка LineTo, ArcTo, NURBSTo, PolylineTo или EllipticalArcTo, если spline следует сегменту этого типа.
  

