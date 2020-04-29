---
title: RelQuadBezTo Row (Geometry Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 5ae57707-5a50-43f0-8c78-516790b5034e
description: Содержит координаты x и y конечной точки квадратичной кривой Безье относительно ширины и высоты фигуры, а также координат x и y контрольной точки кривой относительно ширины и высоты фигуры.
ms.openlocfilehash: f517fa006c6630a26e9162adfbb1be2139487e63
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33423358"
---
# <a name="relquadbezto-row-geometry-section"></a>RelQuadBezTo Row (Geometry Section)

Содержит координаты *x* и *y* конечной точки квадратичной кривой Безье относительно ширины и высоты фигуры, а также координат *x* и *y* контрольной точки кривой относительно ширины и высоты фигуры. 
  
> [!NOTE]
> Строку **строка relquadbezto** можно хранить только в форматах vsdx, vsdm, vstx, vstm, vssx и vssm. При сохранении файла в форматах Visio 2003-2010 строка **строка relquadbezto** преобразуется в строку [NURBSTo](nurbsto-row-geometry-section.md) . 
  
Строка **строка relquadbezto** содержит следующие ячейки. 
  
|**Cell**|**Описание**|
|:-----|:-----|
|[X](x-cell-geometry-section.md) <br/> |Координата *x* конечной вершины кривой Безье второго уровня относительно ширины фигуры.  <br/> |
|[Y (да)](y-cell-geometry-section.md) <br/> |Координата *y* конечной вершины кривой Безье второго уровня относительно высоты фигуры.  <br/> |
|[Определенно](a-cell-geometry-section.md) <br/> |Координата *x* контрольной точки кривой относительно ширины фигуры; точка на дуги. Контрольная точка лучше всего расположена около посередине между начальным и конечным вершинами дуги.  <br/> |
|[З](b-cell-geometry-section.md) <br/> |Координата *y* контрольной точки кривой относительно высоты фигуры.  <br/> |
   

