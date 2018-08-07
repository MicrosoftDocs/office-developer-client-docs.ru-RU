---
title: Ячейка C (раздел "Геометрия")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm140
localization_priority: Normal
ms.assetid: d51a1dd8-678a-a34d-658d-bd7a027dd379
description: Представляет различные сведения в различных строк. В следующей таблице описаны C ячейки, основанную на строке, в котором он находится.
ms.openlocfilehash: 1b9a813be825f2deeb5c90d596ffd9f3705bcef6
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19813323"
---
# <a name="c-cell-geometry-section"></a>Ячейка C (раздел "Геометрия")

Представляет различные сведения в различных строк. В следующей таблице описаны C ячейки, основанную на строке, в котором он находится.
  
|**Row**|**Описание**|
|:-----|:-----|
|[EllipticalArcTo](ellipticalarcto-row-geometry-section.md) <br/> | Угол дуги главных осей относительно *x* -ось родительского элемента.  <br/> |
|[NURBSTo](nurbsto-row-geometry-section.md) <br/> | Первый узел неоднородной rational-сплайн (NURBS).  <br/> |
|[SplineStart](splinestart-row-geometry-section.md) <br/> | Последний число узлов сплайна.  <br/> |
|[Эллипс](ellipse-row-geometry-section.md) <br/> | *X* -координаты точки на эллипсы; в сочетании с *y* -координата, представленного в ячейке [D](d-cell-geometry-section.md) .  <br/> |
   
## <a name="remarks"></a>Замечания

Чтобы получить ссылку на ячейку C по имени из другой формулы, и программы, с помощью свойства **CellsU** , используйте следующую команду: 
  
|||
|:-----|:-----|
| Имя ячейки.  <br/> | Геометрия *i* . C *j* где *i* и *j* = < 1 > 2, 3...  <br/> |
|| Геометрия *i* . C1 (эллипс строка)  <br/> |
   
Для получения ссылки на ячейки C по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы: 
  
|||
|:-----|:-----|
| Индекс раздела:  <br/> |**visSectionFirstComponent** +  *i* где *i* = 0, 1, 2...  <br/> |
| Индекс строки:  <br/> |**visRowVertex** +  *j* где *j* = 0, 1, 2...  <br/> |
||**visRowVertex** (Эллипс строка)  <br/> |
| Индекс ячейки:  <br/> |**visEccentricityAngle** (Строка EllipticalArcTo)  <br/> |
||**visNURBSKnotPrev** (Строка NURBSTo)  <br/> |
||**visSplineKnot3** (Строка SplineStart)  <br/> |
||**visEllipseMinorX** (Эллипс строка)  <br/> |
   

