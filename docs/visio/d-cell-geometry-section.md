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
description: Представляет различные сведения в разных строках. В этой таблице описывается ячейка D, основанная на строке, в которой она расположена.
ms.openlocfilehash: 1da6ac19e6a50ea87f07bf3e3c9f96378b512ba8
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33424380"
---
# <a name="d-cell-geometry-section"></a>D Cell (Geometry Section)

Представляет различные сведения в разных строках. В этой таблице описывается ячейка D, основанная на строке, в которой она расположена.
  
|**Строка**|**Описание**|
|:-----|:-----|
|[EllipticalArcTo](ellipticalarcto-row-geometry-section.md) <br/> | Отношение основной оси дуги к ее вспомогательной оси. Несмотря на обычное значение этих слов, ось "Major" не должна превышать "младшую" ось, поэтому значение этого коэффициента не должно превышать 1. Присвоение этой ячейке значения меньше или равно 0 или больше 1000 может привести к непредсказуемым результатам.  <br/> |
|[NURBSTo](nurbsto-row-geometry-section.md) <br/> | Первый вес рационального понеоднородногоного B-сплайна (NURBS).  <br/> |
|[SplineStart](splinestart-row-geometry-section.md) <br/> | Степень сплайна (целое число от 1 до 25).  <br/> |
|[Ellipse](ellipse-row-geometry-section.md) <br/> | Координата *y* точки эллипса; Связывание с координатой *x* , представленной в ячейке [C](c-cell-geometry-section.md) .  <br/> |
   
## <a name="remarks"></a>Примечания

Чтобы получить ссылку на ячейку D по имени из другой формулы или из программы с помощью свойства **CellsU** , используйте: 
  
|||
|:-----|:-----|
| Имя ячейки:  <br/> | Геометрия *i* . D *j* , где *i* и *j* = <1>, 2, 3...  <br/> |
|| Геометрия *i* . D1 (строка эллипса), где *i* = <1>, 2, 3...  <br/> |
   
Чтобы получить ссылку на ячейку D по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами: 
  
|||
|:-----|:-----|
| Индекс раздела:  <br/> |**visSectionFirstComponent** +  *i*, где *i* = 0, 1, 2...  <br/> |
| Индекс строки:  <br/> |**visRowVertex** +  *j*, где *j* = 0, 1, 2...  <br/> |
||**висроввертекс** (Строка "эллипс")  <br/> |
| Индекс ячейки  <br/> |**висаспектратио** (Строка строка ellipticalarcto)  <br/> |
||**виснурбсвеигхтпрев** (Строка NURBSTo)  <br/> |
||**виссплинедегри** (Строка строка splinestart)  <br/> |
||**виселлипсеминори** (Строка "эллипс")  <br/> |
   

