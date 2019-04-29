---
title: Ячейка X (раздел "Геометрия")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1135
localization_priority: Normal
ms.assetid: 2416b323-e084-18e1-c9be-a797078dfab9
description: Представляет положение фигуры по оси X в локальной системе координат. В этой таблице описывается ячейка X с учетом столбца, в котором она расположена.
ms.openlocfilehash: 6554000a86a6bf27d343a5647161bbe416725e64
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33423946"
---
# <a name="x-cell-geometry-section"></a>Ячейка X (раздел "Геометрия")

Представляет положение фигуры по оси *X* в локальной системе координат. В этой таблице описывается ячейка X с учетом столбца, в котором она расположена. 
  
|**Строка**|**Описание**|
|:-----|:-----|
|[MoveTo](moveto-row-geometry-section.md) <br/> | Если строка MoveTo находится в первой строке раздела, то ячейка X представляет координату *X* первой вершины пути. Если строка MoveTo находится между двух строк, то ячейка X представляет координату *X* первой вершины после прерывания пути.  <br/> |
|[LineTo](lineto-row-geometry-section.md) <br/> | Координата *X* последней вершины сегмента прямой линии.  <br/> |
|[ArcTo](arcto-row-geometry-section.md) <br/> | Координата *X* последней вершины дуги.  <br/> |
|[EllipticalArcTo](ellipticalarcto-row-geometry-section.md) <br/> | Координата *X* последней вершины дуги эллипса.  <br/> |
|[PolylineTo](polylineto-row-geometry-section.md) <br/> | Координата *X* последней вершины ломаной линии.  <br/> |
|[NURBSTo](nurbsto-row-geometry-section.md) <br/> | Координата *X* последней контрольной точки неоднородного рационального B-сплайна (NURBS).  <br/> |
|[SplineStart](splinestart-row-geometry-section.md) <br/> | Координата *X* второй контрольной точки сплайна.  <br/> |
|[SplineKnot](splineknot-row-geometry-section.md) <br/> | Координата *X* контрольной точки.  <br/> |
|[InfiniteLine](infiniteline-row-geometry-section.md) <br/> | Координата *X* точки на бесконечной прямой.  <br/> |
|[Ellipse](ellipse-row-geometry-section.md) <br/> | Координата *X* в центре эллипса.  <br/> |
   
## <a name="remarks"></a>Замечания

Чтобы получить ссылку на ячейку X по имени из другой формулы или из программы с помощью свойства **CellsU**, укажите следующее: 
  
|||
|:-----|:-----|
| Имя ячейки:  <br/> | Геометрия *i* .X *j*, где *i* и *j* = <1>, 2, 3...  <br/> |
|| Геометрия *i* .X1 (строки InfiniteLine и Ellipse), где *i* = <1>, 2, 3...  <br/> |
   
Чтобы получить ссылку на ячейку X по индексу из программы, укажите свойство **CellsSRC** с такими аргументами: 
  
|||
|:-----|:-----|
| Индекс раздела:  <br/> |**visSectionFirstComponent** +  *i*, где *i* = 0, 1, 2...  <br/> |
| Индекс строки:  <br/> |**visRowVertex** +  *j*, где *j* = 0, 1, 2...  <br/> |
||**visRowVertex** (строки InfiniteLine и Ellipse)  <br/> |
| Индекс ячейки:  <br/> |**visX** (строки MoveTo, LineTo, ArcTo, EllipticalArcTo, NURBSTo, Polyline, SplineStart и SplineKnot)  <br/> |
||**visInfiniteLineX1** (строка InfiniteLine)  <br/> |
||**visEllipseCenterX** (строка Ellipse)  <br/> |
   

