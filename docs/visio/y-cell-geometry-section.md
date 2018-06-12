---
title: Ячейка Y (раздел геометрии)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251750
localization_priority: Normal
ms.assetid: a53b5787-f419-7a36-3c04-c63b3c173ac7
description: Представляет y-координат на фигуры в локальной системе координат. В следующей таблице описаны ячейки Y, основанную на строке, в котором он находится.
ms.openlocfilehash: 461fd0ec41d34132f469c811292550d2f7e094f0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19815218"
---
# <a name="y-cell-geometry-section"></a>Ячейка Y (раздел геометрии)

Представляет *y* -координат на фигуры в локальной системе координат. В следующей таблице описаны ячейки Y, основанную на строке, в котором он находится. 
  
|**Row**|**Описание**|
|:-----|:-----|
|[NURBSTo](nurbsto-row-geometry-section.md) <br/> | Если строка MoveTo является первой строки в разделе, ячейки Y представляет *y* -координата первой вершины пути. Если отображается строка MoveTo между двумя строками, ячейки Y представляет *y* -координата первой вершины после приостановки выполнения в поле путь.  <br/> |
|[LineTo](lineto-row-geometry-section.md) <br/> | *Y* -координат окончания вершины прямой сегмент.  <br/> |
|[ArcTo](arcto-row-geometry-section.md) <br/> | *Y* -координат окончания вершины дугу.  <br/> |
|[EllipticalArcTo](ellipticalarcto-row-geometry-section.md) <br/> | *Y* -координат окончания вершины руководство.  <br/> |
|[PolylineTo](polylineto-row-geometry-section.md) <br/> | *Y* -координат окончания вершины ломаной.  <br/> |
|[NURBSTo](nurbsto-row-geometry-section.md) <br/> | *Y* -координата последний элемент управления точкой неоднородной rational B — (NURBS).  <br/> |
|[SplineStart](splinestart-row-geometry-section.md) <br/> | *Y* -Координата второй контрольной точки сплайна.  <br/> |
|[SplineKnot](splineknot-row-geometry-section.md) <br/> | *Y* -координата точки управления.  <br/> |
|[InfiniteLine](infiniteline-row-geometry-section.md) <br/> | *Y -* координата точки в строке не ограничен.  <br/> |
|[Эллипс](ellipse-row-geometry-section.md) <br/> | *Y* -координаты центра эллипса.  <br/> |
   
## <a name="remarks"></a>Замечания

Чтобы получить ссылку на ячейку Y по имени из другой формулы, и программы, с помощью свойства **CellsU** , используйте следующую команду: 
  
|||
|:-----|:-----|
| Имя ячейки.  <br/> | Геометрия *i* . Y *j* где *i* и *j* = < 1 > 2, 3...  <br/> |
|| Геометрия *i* . Y1 (InfiniteLine и эллипс строк) где *i* = < 1 > 2, 3...  <br/> |
   
Для получения ссылки на ячейки Y по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы: 
  
|||
|:-----|:-----|
| Индекс раздела:  <br/> |**visSectionFirstComponent** +  *i* где *i* = 0, 1, 2...  <br/> |
| Индекс строки:  <br/> |**visRowVertex** +  *j* где *j* = 0, 1, 2...  <br/> |
||**visRowVertex** (InfiniteLine и эллипс строк)  <br/> |
| Индекс ячейки:  <br/> |**visY** (MoveTo, LineTo, ArcTo, EllipticalArcTo, NURBSTo, Polyline, SplineStart и SplineKnot строк)  <br/> |
||**visInfiniteLineY1** (Строка InfiniteLine)  <br/> |
||**visEllipseCenterY** (Эллипс строка)  <br/> |
   

