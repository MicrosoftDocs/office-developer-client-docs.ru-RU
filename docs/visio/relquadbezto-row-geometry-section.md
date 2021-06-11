---
title: RelQuadBezTo Row (Geometry Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 5ae57707-5a50-43f0-8c78-516790b5034e
description: Содержит x - и y-координаты конечной точки квадратной кривой Bézier относительно ширины и высоты фигуры, а также x - и y-координаты точки управления ширины и высоты кривой относительной формы.
ms.openlocfilehash: f517fa006c6630a26e9162adfbb1be2139487e63
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33423358"
---
# <a name="relquadbezto-row-geometry-section"></a>RelQuadBezTo Row (Geometry Section)

Содержит *x* - и y-координаты конечной точки квадратной кривой Bézier относительно ширины и высоты фигуры, а также x *-* и *y-координаты* точки управления ширины и высоты кривой относительной формы.  
  
> [!NOTE]
> Строка **RelQuadBezTo** может сохраняться только в форматах файлов .vsdx, .vsdm, .vstx, .vstm, .vssx и .vssm. Если файл сохранен в форматах 2003-2010 Visio, строка **RelQuadBezTo** преобразуется в строку [NURBSTo.](nurbsto-row-geometry-section.md) 
  
Строка **RelQuadBezTo** содержит следующие ячейки. 
  
|**Cell**|**Описание**|
|:-----|:-----|
|[X](x-cell-geometry-section.md) <br/> |X-координата конечной вершины квадратной кривой Bézier относительно ширины фигуры.   <br/> |
|[Да](y-cell-geometry-section.md) <br/> |y-координата конечной вершины квадратной кривой Bézier относительно высоты фигуры.   <br/> |
|[A](a-cell-geometry-section.md) <br/> |X-координата точки управления кривой относительно ширины фигуры;  точка на дуге. Точка управления расположена на полпути между началом и окончанием вершин дуги.  <br/> |
|[B](b-cell-geometry-section.md) <br/> |Y-координата точки управления кривой относительно высоты фигуры.   <br/> |
   

