---
title: Строка SplineKnot (раздел "Геометрия")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm3050
localization_priority: Normal
ms.assetid: 9fbae27d-4f1b-c5f7-aacb-16f359331e83
description: Содержит x - и y-координаты точки управления сплайн и число узлов сплайна.
ms.openlocfilehash: 297889208e064870dd37ed45a17fef7cb4b333b7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19814934"
---
# <a name="splineknot-row-geometry-section"></a>Строка SplineKnot (раздел "Геометрия")

Содержит *x* - и *y* -координаты точки управления сплайн и число узлов сплайна. 
  
Строка SplineKnot содержит следующие ячейки.
  
|**Cell**|**Описание**|
|:-----|:-----|
|[X](x-cell-geometry-section.md) <br/> |*X* -координата точки управления.  <br/> |
|[Да](y-cell-geometry-section.md) <br/> |*Y* -координата точки управления.  <br/> |
|[A](a-cell-geometry-section.md) <br/> |Один из узлов сплайна (кроме последней или первых двух).  <br/> |
   
## <a name="remarks"></a>Замечания

Visio отображается определение сплайна в раздел геометрии, в котором содержится строка SplineStart, а затем одна или несколько строк SplineKnot. Строка SplineStart должен предшествовать строки, например MoveTo строку, чтобы указать, первый элемент управления точкой для другого типа. Предыдущей строке может быть строкой LineTo, ArcTo, NURBSTo, PolylineTo или EllipticalArcTo сплайн за сегмент этого типа.
  

