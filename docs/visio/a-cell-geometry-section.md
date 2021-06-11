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
description: Представляет различные сведения в разных строках. В этой таблице описывается ячейка на основе строки, в которой она расположена.
ms.openlocfilehash: 7009658c7a6844a5c6071f502c05114a4accd7b7
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/29/2019
ms.locfileid: "34541304"
---
# <a name="a-cell-geometry-section"></a>A Cell (Geometry Section)

Представляет различные сведения в разных строках. В этой таблице описывается ячейка на основе строки, в которой она расположена.
  
|Строка|Описание|
|:-----|:-----|
|[ArcTo](arcto-row-geometry-section.md) <br/> | Расстояние от середины дуги до середины аккорда.  <br/> |
|[EllipticalArcTo](ellipticalarcto-row-geometry-section.md) <br/> | X-координата точки управления дуги, точки на дуге.  Точка управления расположена на полпути между началом и окончанием вершин дуги. В противном случае дуга может вырасти до крайнего размера, чтобы пройти через точку управления с непредсказуемыми результатами.  <br/> |
|[PolylineTo](polylineto-row-geometry-section.md) <br/> | Формула полилинов.  <br/> |
|[NURBSTo](nurbsto-row-geometry-section.md) <br/> | Второй до последнего узла неинформированной рациональной B-spline (NURBS).  <br/> |
|[SplineStart](splinestart-row-geometry-section.md) <br/> | Второй узел spline.  <br/> |
|[SplineKnot](splineknot-row-geometry-section.md) <br/> | Один из узлов spline (кроме последнего или первых двух).  <br/> |
|[InfiniteLine](infiniteline-row-geometry-section.md) <br/> | *X-координата* точки на бесконечной строке; в паре *с y-coordinate,* представленным ячейкой [B.](b-cell-geometry-section.md)  <br/> |
|[Ellipse](ellipse-row-geometry-section.md) <br/> | *X-координата* точки на эллипсе; в паре *с y-coordinate,* представленным ячейкой [B.](b-cell-geometry-section.md)  <br/> |
   
## <a name="remarks"></a>Примечания

Чтобы получить ссылку на ячейку по имени из другой формулы или из программы, используя свойство **CellsU,** используйте: 
  
|||
|:-----|:-----|
| Имя ячейки:  <br/> | Геометрия  *i*  .  *J,*            *где i*  и  *j*  = <1>, 2, 3...  <br/> |
|| Геометрия  *i*  . A1 (строки InfiniteLine и Ellipse), где  *i*  = <1>, 2, 3...  <br/> |
   
Чтобы получить ссылку на ячейку по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами: 
  
|||
|:-----|:-----|
| Индекс раздела:  <br/> |**visSectionFirstComponent** +  *i*, где *i* = 0, 1, 2...  <br/> |
| Индекс строки:  <br/> |**visRowVertex** +  *j*, где *j* = 0, 1, 2...  <br/> |
||**visRowVertex** (строки InfiniteLine и Ellipse)  <br/> |
| Индекс ячейки:  <br/> |**visBow** (строка ArcTo)  <br/> |
||**visControlX** (ряд EllipticalArcTo)  <br/> |
||**visControlY** (ряд EllipticalArcTo)  <br/> |
||**visPolylineData** (строка Polyline)  <br/> |
||**visNURBSKnot** (ряд NURBSTo)  <br/> |
||**visSplineKnot** (строки SplineStart и SplineKnot)  <br/> |
||**visInfiniteLineX2** (строка InfiniteLine)  <br/> |
||**visEllipseMajorX** (строка Ellipse)  <br/> |
   

