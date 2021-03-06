---
title: RelEllipticalArcTo Row (Geometry Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 9b7da082-5e55-411d-b109-7fb6fa8f6e8e
description: Содержит x и y-координаты конечной точки эллиптической дуги относительно ширины и высоты фигуры, x - и y-координаты точек управления на дуге относительно ширины и высоты фигуры, угол от оси x-axis до основной оси эллипса и соотношение между основными и небольшими осями эллипса.
ms.openlocfilehash: e38f5f2baf6bb9ade31c2778799a3ece968147f4
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409099"
---
# <a name="relellipticalarcto-row-geometry-section"></a>RelEllipticalArcTo Row (Geometry Section)

Содержит *x* и y-координаты конечной точки эллиптической дуги относительно ширины и высоты фигуры, *x* - и *y-координаты* точек управления на дуге относительно ширины и высоты фигуры, угол от оси *x-axis* до основной оси эллипса и соотношение между основными и небольшими осями эллипса.  
  
> [!NOTE]
> Строка **RelEllipticalArcTo** может сохраняться только в форматах файлов .vsdx, .vsdm, .vstx, .vstm, .vssx и .vssm. Когда файл сохранен в форматах 2003-2010 Visio, строка **RelEllipticalArcTo** преобразуется в строку [EllipticalArcTo.](ellipticalarcto-row-geometry-section.md) 
  
Строка **RelEllipticalArcTo** содержит следующие ячейки. 
  
|**Cell**|**Описание**|
|:-----|:-----|
|[X](x-cell-geometry-section.md) <br/> |X-координата конечной вершины на дуге относительно ширины фигуры.   <br/> |
|[Да](y-cell-geometry-section.md) <br/> |Y-координата конечной вершины на дуге относительно высоты фигуры.   <br/> |
|[A](a-cell-geometry-section.md) <br/> |X-координата точки управления дуги относительно ширины фигуры;  точка на дуге. Точка управления расположена на полпути между началом и окончанием вершин дуги. В противном случае дуга может вырасти до крайнего размера, чтобы пройти через точку управления с непредсказуемыми результатами.  <br/> |
|[B](b-cell-geometry-section.md) <br/> |Y-координата точки управления дуги относительно ширины фигуры.   <br/> |
|[C](c-cell-geometry-section.md) <br/> |Угол основной оси дуги относительно  *оси x-axis*  родительской.  <br/> |
|[D](d-cell-geometry-section.md) <br/> |Отношение основной оси дуги к ее малой оси. Несмотря на обычное значение этих слов, "основная" ось не должна быть больше оси "minor", поэтому это соотношение не должно быть больше 1. Установка этой ячейки на значение меньше 0 или более 1000 может привести к непредсказуемым результатам.  <br/> |
   
## <a name="remarks"></a>Примечания

Значения в строке **RelEllipticalArcTo** эквивалентны значениям в строке [EllipticalArcTo,](ellipticalarcto-row-geometry-section.md) умноженной на ширину и высоту фигуры. Например, строка **RelEllipticalArcTo,** в которой ячейки **X**, **Y,** **A,** **B,** **C** и **D** имеют значения 1, 1, 1.5, 0.5, 15 дег и 1.5 (соответственно) на строку **EllipticalArcTo** с формулами ячейки  `Width*1` , , , , , ,  `Height*1'`  `Width*1.5`  `Height*0.5` 15 deg и 1.5 (соответственно).
  

