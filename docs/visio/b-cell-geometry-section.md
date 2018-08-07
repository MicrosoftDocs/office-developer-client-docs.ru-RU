---
title: Ячейка B (раздел "Геометрия")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251751
localization_priority: Normal
ms.assetid: b0fb6a47-47d8-ab9c-854d-0b0bbfdfcc27
description: Представляет различные сведения в различных строк. В следующей таблице описаны ячейки B, основанную на строке, в котором он находится.
ms.openlocfilehash: 7d6f51d037be4852c6a101ad6e576a3a13488cb7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19813175"
---
# <a name="b-cell-geometry-section"></a>Ячейка B (раздел "Геометрия")

Представляет различные сведения в различных строк. В следующей таблице описаны ячейки B, основанную на строке, в котором он находится.
  
|**Row**|**Описание**|
|:-----|:-----|
|[EllipticalArcTo](ellipticalarcto-row-geometry-section.md) <br/> | *Y* -координата точки управления arc.  <br/> |
|[NURBSTo](nurbsto-row-geometry-section.md) <br/> | Последний вес неоднородной rational-сплайн (NURBS).  <br/> |
|[SplineStart](splinestart-row-geometry-section.md) <br/> | Первый узел сплайна.  <br/> |
|[InfiniteLine](infiniteline-row-geometry-section.md) <br/> | *Y* -координаты точки на неограниченное строке. в сочетании с *x* -координата, представленное [ячейке](a-cell-geometry-section.md) .  <br/> |
|[Эллипс](ellipse-row-geometry-section.md) <br/> | *Y* -координаты точки на эллипсы; в сочетании с *x* -координата, представленное [ячейке](a-cell-geometry-section.md) .  <br/> |
   
## <a name="remarks"></a>Замечания

Для получения ссылки на ячейки B по имени, из другой формулы или из программы, с помощью свойства **CellsU** , используйте следующую команду: 
  
|||
|:-----|:-----|
| Имя ячейки.  <br/> | Геометрия *i* . B *j* где *i* и *j* = < 1 > 2, 3...  <br/> |
|| Геометрия *i* . B1 (InfiniteLine и эллипс строк)  <br/> |
   
Для получения ссылки на ячейки B по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы: 
  
|||
|:-----|:-----|
| Индекс раздела:  <br/> |**visSectionFirstComponent** +  *i* где *i* = 0, 1, 2...  <br/> |
| Индекс строки:  <br/> |**visRowVertex** +  *j* где *j* = 0, 1, 2...  <br/> |
||**visRowVertex** (InfiniteLine и эллипс строк)  <br/> |
| Индекс ячейки:  <br/> |**visControlX** (Строка EllipticalArcTo)  <br/> |
||**visControlY** (Строка EllipticalArcTo)  <br/> |
||**visNURBSWeight** (Строка NURBSTo)  <br/> |
||**visSplineKnot2** (Строка SplineStart)  <br/> |
||**visInfiniteLineY2** (Строка InfiniteLine)  <br/> |
||**visEllipseMajorY** (Эллипс строка)  <br/> |
   

