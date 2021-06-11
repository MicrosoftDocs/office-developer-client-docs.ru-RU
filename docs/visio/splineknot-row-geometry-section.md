---
title: SplineKnot Row (Geometry Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm3050
localization_priority: Normal
ms.assetid: 9fbae27d-4f1b-c5f7-aacb-16f359331e83
description: Содержит x и y-координаты для точки управления spline и узла spline.
ms.openlocfilehash: 432b714772d96e0ab0861bbfb62075258404e607
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407419"
---
# <a name="splineknot-row-geometry-section"></a>SplineKnot Row (Geometry Section)

Содержит  *x*  и  *y-координаты*  для точки управления spline и узла spline. 
  
Строка SplineKnot содержит следующие ячейки.
  
|**Cell**|**Описание**|
|:-----|:-----|
|[X](x-cell-geometry-section.md) <br/> |Координата *X* контрольной точки.  <br/> |
|[Да](y-cell-geometry-section.md) <br/> |Координата *Y* контрольной точки.  <br/> |
|[A](a-cell-geometry-section.md) <br/> |Один из узлов spline (кроме последнего или первых двух).  <br/> |
   
## <a name="remarks"></a>Примечания

Visio отображает определение spline в разделе Геометрия, содержаще строку SplineStart, а затем одну или несколько строк SplineKnot. Строке SplineStart должен предшествовать другой вид строки, например строка MoveTo, чтобы указать первую точку управления spline. В предыдущей строке может быть строка LineTo, ArcTo, NURBSTo, PolylineTo или EllipticalArcTo, если spline следует сегменту этого типа.
  

