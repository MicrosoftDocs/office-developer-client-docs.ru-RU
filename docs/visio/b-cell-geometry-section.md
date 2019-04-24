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
ms.openlocfilehash: ff032b5af2918ec9865360ede5c3d76e8e872e9a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32346244"
---
# <a name="b-cell-geometry-section"></a>B Cell (Geometry Section)

Представляет различные сведения в разных строках. В этой таблице описывается ячейка B на основе строки, в которой она расположена.
  
|**Строка**|**Описание**|
|:-----|:-----|
|[EllipticalArcTo](ellipticalarcto-row-geometry-section.md) <br/> | Координата *y* контрольной точки дуги.  <br/> |
|[NURBSTo](nurbsto-row-geometry-section.md) <br/> | Последний вес неоднородного рационального B-сплайна (NURBS).  <br/> |
|[SplineStart](splinestart-row-geometry-section.md) <br/> | Первый кнот сплайна.  <br/> |
|[InfiniteLine](infiniteline-row-geometry-section.md) <br/> | Координата *y* точки на бесконечной линии; Связывание с координатой *x* , представленной [](a-cell-geometry-section.md) ячейкой.  <br/> |
|[Ellipse](ellipse-row-geometry-section.md) <br/> | Координата *y* точки эллипса; Связывание с координатой *x* , представленной [](a-cell-geometry-section.md) ячейкой.  <br/> |
   
## <a name="remarks"></a>Комментарии

Чтобы получить ссылку на ячейку B по имени из другой формулы или из программы с помощью свойства **CellsU** , используйте: 
  
|||
|:-----|:-----|
| Имя ячейки:  <br/> | Геометрия *i* . B *j* , где *i* и *j* = <1>, 2, 3...  <br/> |
|| Геометрия *i* . Строки B1 (строка infiniteline и Ellipse)  <br/> |
   
Чтобы получить ссылку на ячейку B по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами: 
  
|||
|:-----|:-----|
| Индекс раздела:  <br/> |**visSectionFirstComponent** +  *i*, где *i* = 0, 1, 2...  <br/> |
| Индекс строки:  <br/> |**visRowVertex** +  *j*, где *j* = 0, 1, 2...  <br/> |
||**visRowVertex** (строки InfiniteLine и Ellipse)  <br/> |
| Индекс ячейки:  <br/> |**висконтролкс** (Строка строка ellipticalarcto)  <br/> |
||**висконтроли** (Строка строка ellipticalarcto)  <br/> |
||**виснурбсвеигхт** (Строка NURBSTo)  <br/> |
||**visSplineKnot2** (Строка строка splinestart)  <br/> |
||**visInfiniteLineY2** (Строка строка infiniteline)  <br/> |
||**виселлипсемажори** (Строка "эллипс")  <br/> |
   

