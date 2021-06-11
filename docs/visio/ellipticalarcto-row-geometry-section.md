---
title: EllipticalArcTo Row (Geometry Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm3015
localization_priority: Normal
ms.assetid: 7ceb30a8-1d05-feff-35d8-08a198784a27
description: Содержит x и y-координаты конечной точки эллиптической дуги, x и y-координаты точек управления на дуге, угол от оси x до основной оси эллипса и соотношение между основными и небольшими осями эллипса.
ms.openlocfilehash: c6db7560a05652ca3bfcadb2fd4857ac39370562
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33421405"
---
# <a name="ellipticalarcto-row-geometry-section"></a>EllipticalArcTo Row (Geometry Section)

Содержит  *x*  и  *y-координаты*  конечной точки эллиптической дуги,  *x*  и  *y-координаты*  точек управления на дуге, угол от оси  *x*  до основной оси эллипса и соотношение между основными и небольшими осями эллипса. 
  
Строка EllipticalArcTo содержит следующие ячейки.
  
|**Cell**|**Описание**|
|:-----|:-----|
|[X](x-cell-geometry-section.md) <br/> |X-координата конечной вершины на дуге.   <br/> |
|[Да](y-cell-geometry-section.md) <br/> |Y-координата конечной вершины на дуге.   <br/> |
|[A](a-cell-geometry-section.md) <br/> |*X-координата* точки управления дуги; точка на дуге. Точка управления расположена на полпути между началом и окончанием вершин дуги. В противном случае дуга может вырасти до крайнего размера, чтобы пройти через точку управления с непредсказуемыми результатами.  <br/> |
|[B](b-cell-geometry-section.md) <br/> |Y-координата точки управления дуги.   <br/> |
|[C](c-cell-geometry-section.md) <br/> |Угол основной оси дуги относительно  *оси x-axis*  родительской.  <br/> |
|[D](d-cell-geometry-section.md) <br/> |Отношение основной оси дуги к ее малой оси. Несмотря на обычное значение этих слов, "основная" ось не должна быть больше оси "minor", поэтому это соотношение не должно быть больше 1. Установка этой ячейки на значение меньше 0 или более 1000 может привести к непредсказуемым результатам.  <br/> |
   

