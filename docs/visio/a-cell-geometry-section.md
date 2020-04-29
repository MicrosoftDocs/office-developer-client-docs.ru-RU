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
description: Представляет различные сведения в разных строках. В этой таблице описывается ячейка, основанная на строке, в которой она расположена.
ms.openlocfilehash: 7009658c7a6844a5c6071f502c05114a4accd7b7
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/29/2019
ms.locfileid: "34541304"
---
# <a name="a-cell-geometry-section"></a>A Cell (Geometry Section)

Представляет различные сведения в разных строках. В этой таблице описывается ячейка, основанная на строке, в которой она расположена.
  
|Строка|Описание|
|:-----|:-----|
|[ArcTo](arcto-row-geometry-section.md) <br/> | Расстояние от средней дуги до средней точки аккорда.  <br/> |
|[EllipticalArcTo](ellipticalarcto-row-geometry-section.md) <br/> | Координата *x* контрольной точки дуги, точка на дуги. Контрольная точка лучше всего расположена около посередине между начальным и конечным вершинами дуги. В противном случае дуга может увеличиться до экстремального размера для прохождения через контрольную точку с непредсказуемыми результатами.  <br/> |
|[PolylineTo](polylineto-row-geometry-section.md) <br/> | Формула ломаной линии.  <br/> |
|[NURBSTo](nurbsto-row-geometry-section.md) <br/> | Вторая — последняя кнот неоднородного рационального сплайна B-сплайна (NURBS).  <br/> |
|[SplineStart](splinestart-row-geometry-section.md) <br/> | Второй кнот сплайна.  <br/> |
|[SplineKnot](splineknot-row-geometry-section.md) <br/> | Один из Кнотс сплайна (отличный от последнего или первых двух).  <br/> |
|[InfiniteLine](infiniteline-row-geometry-section.md) <br/> | Координата *x* точки на бесконечной линии; Связывание с координатой *y* , представленной в ячейке [B](b-cell-geometry-section.md) .  <br/> |
|[Ellipse](ellipse-row-geometry-section.md) <br/> | Координата *x* точки эллипса; Связывание с координатой *y* , представленной в ячейке [B](b-cell-geometry-section.md) .  <br/> |
   
## <a name="remarks"></a>Примечания

Чтобы получить ссылку на ячейку по имени из другой формулы или из программы с помощью свойства **CellsU** , используйте следующее: 
  
|||
|:-----|:-----|
| Имя ячейки:  <br/> | Геометрия *i* . A *j* , где *i* и *j* = <1>, 2, 3...  <br/> |
|| Геометрия *i* . A1 (строка infiniteline и эллиптические строки), где *i* = <1>, 2, 3...  <br/> |
   
Чтобы получить ссылку на ячейку по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами: 
  
|||
|:-----|:-----|
| Индекс раздела:  <br/> |**visSectionFirstComponent** +  *i*, где *i* = 0, 1, 2...  <br/> |
| Индекс строки:  <br/> |**visRowVertex** +  *j*, где *j* = 0, 1, 2...  <br/> |
||**visRowVertex** (строки InfiniteLine и Ellipse)  <br/> |
| Индекс ячейки:  <br/> |**висбов** (строка строка ArcTo)  <br/> |
||**висконтролкс** (строка строка ellipticalarcto)  <br/> |
||**висконтроли** (строка строка ellipticalarcto)  <br/> |
||**висполилинедата** (строка ломаной линии)  <br/> |
||**виснурбскнот** (строка NURBSTo)  <br/> |
||**виссплинекнот** (строки строка splinestart и строка splineknot)  <br/> |
||**visInfiniteLineX2** (строка строка infiniteline)  <br/> |
||**виселлипсемажоркс** (строка "эллипс")  <br/> |
   

