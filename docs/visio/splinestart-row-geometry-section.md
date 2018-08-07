---
title: Строка SplineStart (раздел "Геометрия")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm3055
localization_priority: Normal
ms.assetid: 8e327e00-0844-efa4-900b-6954d3b009bb
description: Содержит x - и y-координаты сплайн второй контрольной точки, его второй число узлов, его первого число узлов, последний число узлов и степень сплайн.
ms.openlocfilehash: 0944da12e6090fde41dc5927b5705e103d29f76d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19814936"
---
# <a name="splinestart-row-geometry-section"></a>Строка SplineStart (раздел "Геометрия")

Содержит *x* - и *y* -координаты сплайн второй контрольной точки, его второй число узлов, его первого число узлов, последний число узлов и степень сплайн. 
  
Строка SplineStart содержит следующие ячейки.
  
|**Cell**|**Описание**|
|:-----|:-----|
|[X](x-cell-geometry-section.md) <br/> |*X* -Координата второй контрольной точки сплайна.  <br/> |
|[Да](y-cell-geometry-section.md) <br/> |*Y* -Координата второй контрольной точки сплайна.  <br/> |
|[A](a-cell-geometry-section.md) <br/> |Второй узел сплайн.  <br/> |
|[B](b-cell-geometry-section.md) <br/> |Первый узел сплайна.  <br/> |
|[C](c-cell-geometry-section.md) <br/> |Последний число узлов сплайна.  <br/> |
|[D](d-cell-geometry-section.md) <br/> |Степень сплайна (целое число от 1 до 25).  <br/> |
   
## <a name="remarks"></a>Замечания

Visio отображается определение сплайна в раздел геометрии, в котором содержится строка SplineStart, а затем одна или несколько строк SplineKnot. Строка SplineStart должен предшествовать строки, например MoveTo строку, чтобы указать, первый элемент управления точкой для другого типа. Предыдущей строке может быть строкой LineTo, ArcTo, NURBSTo, PolylineTo или EllipticalArcTo сплайн за сегмент этого типа.
  

