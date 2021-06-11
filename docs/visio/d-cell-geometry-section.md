---
title: D Cell (Geometry Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251753
localization_priority: Normal
ms.assetid: 5f1fdf59-db58-561c-e187-1af72a8b87f2
description: Представляет различные сведения в разных строках. В этой таблице описывается ячейка D на основе строки, в которой она расположена.
ms.openlocfilehash: a76093f028986907b58175bc6b8c81a7056cfe07
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/29/2019
ms.locfileid: "34542501"
---
# <a name="d-cell-geometry-section"></a>D Cell (Geometry Section)

Представляет различные сведения в разных строках. В этой таблице описывается ячейка D на основе строки, в которой она расположена.
  
|Строка|Описание|
|:-----|:-----|
|[EllipticalArcTo](ellipticalarcto-row-geometry-section.md) <br/> | Отношение основной оси дуги к ее малой оси. Несмотря на обычное значение этих слов, "основная" ось не должна быть больше оси "minor", поэтому это соотношение не должно быть больше 1. Установка этой ячейки на значение меньше 0 или более 1000 может привести к непредсказуемым результатам.  <br/> |
|[NURBSTo](nurbsto-row-geometry-section.md) <br/> | Первый вес несвязаного рационального B-spline (NURBS).  <br/> |
|[SplineStart](splinestart-row-geometry-section.md) <br/> | Степень spline (integer от 1 до 25).  <br/> |
|[Ellipse](ellipse-row-geometry-section.md) <br/> | y-координата точки на эллипсе;  в паре  с x-координатами, представленными [ячейкой C.](c-cell-geometry-section.md)  <br/> |
   
## <a name="remarks"></a>Примечания

Чтобы получить ссылку на ячейку D по имени из другой формулы или из программы с помощью свойства **CellsU,** используйте: 
  
|||
|:-----|:-----|
| Имя ячейки:  <br/> | Геометрия  *i*  . D  *j,*            *где i*  и  *j*  = <1>, 2, 3 ...  <br/> |
|| Геометрия  *i*  . D1 (строка Ellipse), где  *i*  = <1>, 2, 3...  <br/> |
   
Чтобы получить ссылку на ячейку D по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами: 
  
|||
|:-----|:-----|
| Индекс раздела:  <br/> |**visSectionFirstComponent** +  *i*, где *i* = 0, 1, 2...  <br/> |
| Индекс строки:  <br/> |**visRowVertex** +  *j*, где *j* = 0, 1, 2...  <br/> |
||**visRowVertex** (строка Ellipse)  <br/> |
| Индекс ячейки  <br/> |**visAspectRatio** (ряд EllipticalArcTo)  <br/> |
||**visNURBSWeightPrev** (ряд NURBSTo)  <br/> |
||**visSplineDegree** (строка SplineStart)  <br/> |
||**visEllipseMinorY** (строка Ellipse)  <br/> |
   

