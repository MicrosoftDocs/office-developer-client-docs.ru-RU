---
title: RelQuadBezTo Row (Geometry Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 5ae57707-5a50-43f0-8c78-516790b5034e
description: Содержит координаты x и y конечной точки кривой Безье первого кадра относительно ширины и высоты фигуры, а также координат x и y контрольной точки относительной ширины и высоты кривой.
ms.openlocfilehash: f517fa006c6630a26e9162adfbb1be2139487e63
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33423358"
---
# <a name="relquadbezto-row-geometry-section"></a>RelQuadBezTo Row (Geometry Section)

Содержит координаты  *x*  и  *y*  конечной точки кривой Безье первого кадра относительно ширины и высоты фигуры, а также координат  *x*  и  *y*  контрольной точки относительной ширины и высоты кривой. 
  
> [!NOTE]
> Строка **RelQuadBezTo** может сохраняться только в форматах VSDX, VSDM, VSTX, VSTM, VSSX и VSSM. При сохранении файла в форматах Visio 2003-2010 строка **RelQuadBezTo** преобразуется в строку [NURBSTo.](nurbsto-row-geometry-section.md) 
  
Строка **RelQuadBezTo** содержит следующие ячейки. 
  
|**Cell**|**Описание**|
|:-----|:-----|
|[X](x-cell-geometry-section.md) <br/> |X-координата конечной вершины кривой Безье х относительно ширины фигуры.   <br/> |
|[Y](y-cell-geometry-section.md) <br/> |Y-координата конечной вершины кривой Безье Y относительно высоты фигуры.   <br/> |
|[A](a-cell-geometry-section.md) <br/> |X-координата контрольной точки кривой относительно ширины фигуры;  точка на дуге. Контрольная точка лучше всего расположена примерно на середине между началом и конечной вершиной дуги.  <br/> |
|[B](b-cell-geometry-section.md) <br/> |Координата  *Y*  контрольной точки кривой относительно высоты фигуры.  <br/> |
   

