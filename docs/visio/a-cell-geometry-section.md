---
title: A Cell (Geometry Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm51215
localization_priority: Normal
ms.assetid: 6853df0f-d22e-89ca-7d34-342b9c0bea23
description: Представляет различные сведения в разных строках. В этой таблице описывается ячейка A на основе строки, в которой она расположена.
ms.openlocfilehash: 7009658c7a6844a5c6071f502c05114a4accd7b7
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/29/2019
ms.locfileid: "34541304"
---
# <a name="a-cell-geometry-section"></a>A Cell (Geometry Section)

Представляет различные сведения в разных строках. В этой таблице описывается ячейка A на основе строки, в которой она расположена.
  
|Строка|Описание|
|:-----|:-----|
|[ArcTo](arcto-row-geometry-section.md) <br/> | Расстояние от средней точки дуги до средней точки ее разоряемой.  <br/> |
|[EllipticalArcTo](ellipticalarcto-row-geometry-section.md) <br/> | X-координата контрольной точки дуги, точки на дуге.  Контрольная точка лучше всего расположена примерно на середине между началом и конечной вершиной дуги. В противном случае дуга может увеличиваться до крайнего размера, чтобы пройти через контрольную точку с непредсказуемыми результатами.  <br/> |
|[PolylineTo](polylineto-row-geometry-section.md) <br/> | Многолинейная формула.  <br/> |
|[NURBSTo](nurbsto-row-geometry-section.md) <br/> | От второго до последнего вехи неуникционного рационального B-spline (NURBS).  <br/> |
|[SplineStart](splinestart-row-geometry-section.md) <br/> | Вторая часть сплайна.  <br/> |
|[SplineKnot](splineknot-row-geometry-section.md) <br/> | Одна из подмайок сплайна (кроме последней или первой).  <br/> |
|[InfiniteLine](infiniteline-row-geometry-section.md) <br/> | X-координата точки на бесконечной линии;  сопряжено с *координатой Y,* представленной ячейкой [B.](b-cell-geometry-section.md)  <br/> |
|[Ellipse](ellipse-row-geometry-section.md) <br/> | X-координата точки на эллипсе;  сопряжено с *координатой Y,* представленной ячейкой [B.](b-cell-geometry-section.md)  <br/> |
   
## <a name="remarks"></a>Примечания

Чтобы получить ссылку на ячейку A по имени из другой формулы или из программы, используя свойство **CellsU,** используйте: 
  
|||
|:-----|:-----|
| Имя ячейки:  <br/> | Геометрия  *i*  .  *J,*            *где i*  и  *j*  = <1>, 2, 3...  <br/> |
|| Геометрия  *i*  . A1 (строки InfiniteLine и Ellipse),  *где i*  = <1>, 2, 3...  <br/> |
   
Чтобы получить ссылку на ячейку A по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами: 
  
|||
|:-----|:-----|
| Индекс раздела:  <br/> |**visSectionFirstComponent** +  *i*, где *i* = 0, 1, 2...  <br/> |
| Индекс строки:  <br/> |**visRowVertex** +  *j*, где *j* = 0, 1, 2...  <br/> |
||**visRowVertex** (строки InfiniteLine и Ellipse)  <br/> |
| Индекс ячейки:  <br/> |**visBow** (строка ArcTo)  <br/> |
||**visControlX** (строка EllipticalArcTo)  <br/> |
||**visControlY** (строка EllipticalArcTo)  <br/> |
||**visPolylineData** (строка Polyline)  <br/> |
||**visNURBSKnot** (строка NURBSTo)  <br/> |
||**visSplineKnot** (строки SplineStart и SplineKnot)  <br/> |
||**visInfiniteLineX2** (строка InfiniteLine)  <br/> |
||**visEllipseMajorX** (строка Ellipse)  <br/> |
   

