---
title: C Cell (Geometry Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm140
localization_priority: Normal
ms.assetid: d51a1dd8-678a-a34d-658d-bd7a027dd379
description: Представляет различные сведения в разных строках. В этой таблице описывается ячейка C на основе строки, в которой она расположена.
ms.openlocfilehash: 0284fea02c7eb890b56b6c865a69eb36662d8ae6
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/29/2019
ms.locfileid: "34541892"
---
# <a name="c-cell-geometry-section"></a>C Cell (Geometry Section)

Представляет различные сведения в разных строках. В этой таблице описывается ячейка C на основе строки, в которой она расположена.
  
|Строка|Описание|
|:-----|:-----|
|[EllipticalArcTo](ellipticalarcto-row-geometry-section.md) <br/> | Угол основной оси дуги относительно  *оси x-axis*  родительской.  <br/> |
|[NURBSTo](nurbsto-row-geometry-section.md) <br/> | Первый узел неинформированной рациональной B-spline (NURBS).  <br/> |
|[SplineStart](splinestart-row-geometry-section.md) <br/> | Последний узел spline.  <br/> |
|[Ellipse](ellipse-row-geometry-section.md) <br/> | *X-координата* точки на эллипсе; в паре с *y-координатой,* представленной ячейкой [D.](d-cell-geometry-section.md)  <br/> |
   
## <a name="remarks"></a>Примечания

Чтобы получить ссылку на ячейку C по имени из другой формулы или из программы с помощью свойства **CellsU,** используйте: 
  
|||
|:-----|:-----|
| Имя ячейки:  <br/> | Геометрия  *i*  . C  *j,*            *где i*  и  *j*  = <1>, 2, 3...  <br/> |
|| Геометрия  *i*  . C1 (строка Ellipse)  <br/> |
   
Чтобы получить ссылку на ячейку C по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами: 
  
|||
|:-----|:-----|
| Индекс раздела:  <br/> |**visSectionFirstComponent** +  *i*, где *i* = 0, 1, 2...  <br/> |
| Индекс строки:  <br/> |**visRowVertex** +  *j*, где *j* = 0, 1, 2...  <br/> |
||**visRowVertex** (строка Ellipse)  <br/> |
| Индекс ячейки:  <br/> |**visEccentricityAngle** (ряд EllipticalArcTo)  <br/> |
||**visNURBSKnotPrev** (ряд NURBSTo)  <br/> |
||**visSplineKnot3** (строка SplineStart)  <br/> |
||**visEllipseMinorX** (строка Ellipse)  <br/> |
   

