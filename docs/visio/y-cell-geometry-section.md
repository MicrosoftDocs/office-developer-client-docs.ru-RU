---
title: Ячейка Y (раздел "Геометрия")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251750
localization_priority: Normal
ms.assetid: a53b5787-f419-7a36-3c04-c63b3c173ac7
description: Представляет положение фигуры по оси Y в локальной системе координат. В этой таблице описывается ячейка Y с учетом столбца, в котором она расположена.
ms.openlocfilehash: 9e823b8d21682b419a70ce498016abf575f36f6b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32342814"
---
# <a name="y-cell-geometry-section"></a>Ячейка Y (раздел "Геометрия")

Представляет положение фигуры по оси *Y* в локальной системе координат. В этой таблице описывается ячейка Y с учетом столбца, в котором она расположена. 
  
|**Строка**|**Описание**|
|:-----|:-----|
|[NURBSTo](nurbsto-row-geometry-section.md) <br/> | Если строка MoveTo находится в первой строке раздела, то ячейка Y представляет координату *Y* первой вершины пути. Если строка MoveTo находится между двух строк, то ячейка Y представляет координату *Y* первой вершины после прерывания пути.  <br/> |
|[LineTo](lineto-row-geometry-section.md) <br/> | Координата *Y* последней вершины сегмента прямой линии.  <br/> |
|[ArcTo](arcto-row-geometry-section.md) <br/> | Координата *Y* последней вершины дуги.  <br/> |
|[EllipticalArcTo](ellipticalarcto-row-geometry-section.md) <br/> | Координата *Y* последней вершины дуги эллипса.  <br/> |
|[PolylineTo](polylineto-row-geometry-section.md) <br/> | Координата *Y* последней вершины ломаной линии.  <br/> |
|[NURBSTo](nurbsto-row-geometry-section.md) <br/> | Координата *Y* последней контрольной точки неоднородного рационального B-сплайна (NURBS).  <br/> |
|[SplineStart](splinestart-row-geometry-section.md) <br/> | Координата *Y* второй контрольной точки сплайна.  <br/> |
|[SplineKnot](splineknot-row-geometry-section.md) <br/> | Координата *Y* контрольной точки.  <br/> |
|[InfiniteLine](infiniteline-row-geometry-section.md) <br/> | Координата *Y* точки на бесконечной прямой.  <br/> |
|[Ellipse](ellipse-row-geometry-section.md) <br/> | Координата *Y* в центре эллипса.  <br/> |
   
## <a name="remarks"></a>Замечания

Чтобы получить ссылку на ячейку Y по имени из другой формулы или из программы с помощью свойства **CellsU**, укажите следующее: 
  
|||
|:-----|:-----|
| Имя ячейки:  <br/> | Геометрия *i* .Y *j*, где *i* и *j* = <1>, 2, 3...  <br/> |
|| Геометрия *i* .Y1 (строки InfiniteLine и Ellipse), где *i* = <1>, 2, 3...  <br/> |
   
Чтобы получить ссылку на ячейку Y по индексу из программы, укажите свойство **CellsSRC** с такими аргументами: 
  
|||
|:-----|:-----|
| Индекс раздела:  <br/> |**visSectionFirstComponent** +  *i*, где *i* = 0, 1, 2...  <br/> |
| Индекс строки:  <br/> |**visRowVertex** +  *j*, где *j* = 0, 1, 2...  <br/> |
||**visRowVertex** (строки InfiniteLine и Ellipse)  <br/> |
| Индекс ячейки:  <br/> |**visY** (строки MoveTo, LineTo, ArcTo, EllipticalArcTo, NURBSTo, Polyline, SplineStart и SplineKnot)  <br/> |
||**visInfiniteLineY1** (строка InfiniteLine)  <br/> |
||**visEllipseCenterY** (строка Ellipse)  <br/> |
   

