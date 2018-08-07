---
title: Ячейка D (раздел "Геометрия")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251753
localization_priority: Normal
ms.assetid: 5f1fdf59-db58-561c-e187-1af72a8b87f2
description: Представляет различные сведения в различных строк. В следующей таблице описаны ячейке D, основанную на строке, в котором он находится.
ms.openlocfilehash: ed67197e46ee159ba2175b0e86623fe1704992d2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19813517"
---
# <a name="d-cell-geometry-section"></a>Ячейка D (раздел "Геометрия")

Представляет различные сведения в различных строк. В следующей таблице описаны ячейке D, основанную на строке, в котором он находится.
  
|**Row**|**Описание**|
|:-----|:-----|
|[EllipticalArcTo](ellipticalarcto-row-geometry-section.md) <br/> | Отношение arc главных осей его вспомогательные оси. Несмотря на обычных значение из этих слов, должно быть больше оси «дополнительный номер», поэтому этот коэффициент не должен быть больше 1 имеет оси «основные». Установка для этой ячейки значение меньше или равно 0 или выше, чем 1000 может привести к непредсказуемым последствиям.  <br/> |
|[NURBSTo](nurbsto-row-geometry-section.md) <br/> | Первый вес неоднородной rational-сплайн (NURBS).  <br/> |
|[SplineStart](splinestart-row-geometry-section.md) <br/> | Степень сплайна (целое число от 1 до 25).  <br/> |
|[Эллипс](ellipse-row-geometry-section.md) <br/> | *Y* -координаты точки на эллипсы; в сочетании с *x* -координата, представленный в ячейку [C](c-cell-geometry-section.md) .  <br/> |
   
## <a name="remarks"></a>Замечания

Чтобы получить ссылку на ячейке D по имени из другой формулы, и программы, с помощью свойства **CellsU** , используйте: 
  
|||
|:-----|:-----|
| Имя ячейки.  <br/> | Геометрия *i* . D *j* где *i* и *j* = < 1 > 2, 3...  <br/> |
|| Геометрия *i* . D1 (строка эллипс) где *i* = < 1 > 2, 3...  <br/> |
   
Для получения ссылки на ячейки D по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы: 
  
|||
|:-----|:-----|
| Индекс раздела:  <br/> |**visSectionFirstComponent** +  *i* где *i* = 0, 1, 2...  <br/> |
| Индекс строки:  <br/> |**visRowVertex** +  *j* где *j* = 0, 1, 2...  <br/> |
||**visRowVertex** (Эллипс строка)  <br/> |
| Индекс ячейки  <br/> |**visAspectRatio** (Строка EllipticalArcTo)  <br/> |
||**visNURBSWeightPrev** (Строка NURBSTo)  <br/> |
||**visSplineDegree** (Строка SplineStart)  <br/> |
||**visEllipseMinorY** (Эллипс строка)  <br/> |
   

