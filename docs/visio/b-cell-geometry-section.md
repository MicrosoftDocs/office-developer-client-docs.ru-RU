---
title: B Cell (Geometry Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251751
localization_priority: Normal
ms.assetid: b0fb6a47-47d8-ab9c-854d-0b0bbfdfcc27
description: Представляет различные сведения в разных строках. В этой таблице описывается ячейка B на основе строки, в которой она расположена.
ms.openlocfilehash: 46c8aa418f495905630fed2833d84afc93945346
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/29/2019
ms.locfileid: "34537796"
---
# <a name="b-cell-geometry-section"></a>B Cell (Geometry Section)

Представляет различные сведения в разных строках. В этой таблице описывается ячейка B на основе строки, в которой она расположена.
  
|Строка|Описание|
|:-----|:-----|
|[EllipticalArcTo](ellipticalarcto-row-geometry-section.md) <br/> | Y-координата контрольной точки дуги.   <br/> |
|[NURBSTo](nurbsto-row-geometry-section.md) <br/> | Последний вес несвязаного рационального B-spline (NURBS).  <br/> |
|[SplineStart](splinestart-row-geometry-section.md) <br/> | Первая ветвь сплайна.  <br/> |
|[InfiniteLine](infiniteline-row-geometry-section.md) <br/> | Y-координата точки на бесконечной линии;  сопряжено  с x-координатой, представленной ячейкой [A.](a-cell-geometry-section.md)  <br/> |
|[Ellipse](ellipse-row-geometry-section.md) <br/> | Y-координата точки на эллипсе;  сопряжено  с x-координатой, представленной ячейкой [A.](a-cell-geometry-section.md)  <br/> |
   
## <a name="remarks"></a>Примечания

Чтобы получить ссылку на ячейку B по имени из другой формулы или из программы, используя свойство **CellsU,** используйте: 
  
|||
|:-----|:-----|
| Имя ячейки:  <br/> | Геометрия  *i*  . B  *j,*            *где i*  и  *j*  = <1>, 2, 3...  <br/> |
|| Геометрия  *i*  . B1 (строки InfiniteLine и Ellipse)  <br/> |
   
Чтобы получить ссылку на ячейку B по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами: 
  
|||
|:-----|:-----|
| Индекс раздела:  <br/> |**visSectionFirstComponent** +  *i*, где *i* = 0, 1, 2...  <br/> |
| Индекс строки:  <br/> |**visRowVertex** +  *j*, где *j* = 0, 1, 2...  <br/> |
||**visRowVertex** (строки InfiniteLine и Ellipse)  <br/> |
| Индекс ячейки:  <br/> |**visControlX** (строка EllipticalArcTo)  <br/> |
||**visControlY** (строка EllipticalArcTo)  <br/> |
||**visNURBSWeight** (строка NURBSTo)  <br/> |
||**visSplineKnot2** (строка SplineStart)  <br/> |
||**visInfiniteLineY2** (строка InfiniteLine)  <br/> |
||**visEllipseMajorY** (строка Ellipse)  <br/> |
   

