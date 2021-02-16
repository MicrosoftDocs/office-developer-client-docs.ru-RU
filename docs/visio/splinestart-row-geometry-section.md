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
description: Содержит координаты x и y для второй контрольной точки сплайна, его второй замещести, первой степени, последней затеи и степени сплайна.
ms.openlocfilehash: 2ec06619770af4e5dbcc1a763595b6e01a39052b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33417478"
---
# <a name="splinestart-row-geometry-section"></a>SplineStart Row (Geometry Section)

Содержит  *координаты x*  и  *y*  для второй контрольной точки сплайна, его второй замещести, первой степени, последней затеи и степени сплайна. 
  
Строка SplineStart содержит следующие ячейки.
  
|**Cell**|**Описание**|
|:-----|:-----|
|[X](x-cell-geometry-section.md) <br/> |Координата *X* второй контрольной точки сплайна.  <br/> |
|[Y](y-cell-geometry-section.md) <br/> |Координата *Y* второй контрольной точки сплайна.  <br/> |
|[A](a-cell-geometry-section.md) <br/> |Вторая часть сплайна.  <br/> |
|[B](b-cell-geometry-section.md) <br/> |Первая ветвь сплайна.  <br/> |
|[C](c-cell-geometry-section.md) <br/> |Последняя часть сплайна.  <br/> |
|[D](d-cell-geometry-section.md) <br/> |Степень сплайна (от 1 до 25).  <br/> |
   
## <a name="remarks"></a>Примечания

Visio отображает определение сплайна в разделе "Геометрия", который содержит строку SplineStart, за которой следует одна или несколько строк SplineKnot. Перед строкой SplineStart должен быть другой вид строки, например строка MoveTo, чтобы указать первую контрольную точку сплайна. Предыдущей строкой может быть строка LineTo, ArcTo, NURBSTo, PolylineTo или EllipticalArcTo, если spline следует за сегментом этого типа.
  

