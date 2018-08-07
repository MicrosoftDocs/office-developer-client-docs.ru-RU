---
title: Ячейка A (раздел "Геометрия")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm51215
localization_priority: Normal
ms.assetid: 6853df0f-d22e-89ca-7d34-342b9c0bea23
description: Представляет различные сведения в различных строк. В следующей таблице описаны ячейки A, основанную на строке, в котором он находится.
ms.openlocfilehash: b907552c2346292a6b14baf16481b6b40cc80fc4
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19813117"
---
# <a name="a-cell-geometry-section"></a>Ячейка A (раздел "Геометрия")

Представляет различные сведения в различных строк. В следующей таблице описаны ячейки A, основанную на строке, в котором он находится.
  
|**Row**|**Описание**|
|:-----|:-----|
|[ArcTo](arcto-row-geometry-section.md) <br/> | Расстояние от среднего дуги по центру его кабеля.  <br/> |
|[EllipticalArcTo](ellipticalarcto-row-geometry-section.md) <br/> | *X* -координата точки управления дуги, точку на дуги. Контрольная точка расположена лучше всего о пользователю между начала и окончания грани дуги. В противном случае дуги может расти в размерах чрезмерную размера для передачи через точку управления с непредсказуемым последствиям.  <br/> |
|[PolylineTo](polylineto-row-geometry-section.md) <br/> | Формула ломаной.  <br/> |
|[NURBSTo](nurbsto-row-geometry-section.md) <br/> | Второй — к последней узлов неоднородной rational-сплайн (NURBS).  <br/> |
|[SplineStart](splinestart-row-geometry-section.md) <br/> | Второй узел сплайн.  <br/> |
|[SplineKnot](splineknot-row-geometry-section.md) <br/> | Один из узлов сплайна (кроме последней или первых двух).  <br/> |
|[InfiniteLine](infiniteline-row-geometry-section.md) <br/> | *X* -координаты точки на строке не ограничен. в сочетании с *y* -координата, представленное [B](b-cell-geometry-section.md) ячейки.  <br/> |
|[Эллипс](ellipse-row-geometry-section.md) <br/> | *X* -координаты точки на эллипс; в сочетании с *y* -координата, представленное [B](b-cell-geometry-section.md) ячейки.  <br/> |
   
## <a name="remarks"></a>Замечания

Для получения ссылки на ячейки A по имени, из другой формулы или из программы, с помощью свойства **CellsU** , используйте следующую команду: 
  
|||
|:-----|:-----|
| Имя ячейки.  <br/> | Геометрия *i* . *J* где *i* и *j* = < 1 > 2, 3...  <br/> |
|| Геометрия *i* . A1 (InfiniteLine и эллипс строк) где *i* = < 1 > 2, 3...  <br/> |
   
Для получения ссылки на ячейки A по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы: 
  
|||
|:-----|:-----|
| Индекс раздела:  <br/> |**visSectionFirstComponent** +  *i* где *i* = 0, 1, 2...  <br/> |
| Индекс строки:  <br/> |**visRowVertex** +  *j* где *j* = 0, 1, 2...  <br/> |
||**visRowVertex** (InfiniteLine и эллипс строк)  <br/> |
| Индекс ячейки:  <br/> |**visBow** (Строка ArcTo)  <br/> |
||**visControlX** (Строка EllipticalArcTo)  <br/> |
||**visControlY** (Строка EllipticalArcTo)  <br/> |
||**visPolylineData** (Ломаной строка)  <br/> |
||**visNURBSKnot** (Строка NURBSTo)  <br/> |
||**visSplineKnot** (SplineStart и SplineKnot строк)  <br/> |
||**visInfiniteLineX2** (Строка InfiniteLine)  <br/> |
||**visEllipseMajorX** (Эллипс строка)  <br/> |
   

