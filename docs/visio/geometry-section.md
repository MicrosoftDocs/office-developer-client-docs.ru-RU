---
title: Раздел геометрии
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm2055
localization_priority: Normal
ms.assetid: 75601a1e-6b1a-27ee-a2bd-69e569315982
description: Содержит строки, в которых перечислены координаты грани для линий и дуг, образующих фигуру.
ms.openlocfilehash: 59f85c512b7038f6cfddcb657435730a2e724bd6
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19813839"
---
# <a name="geometry-section"></a>Раздел геометрии

Содержит строки, в которых перечислены координаты грани для линий и дуг, образующих фигуру. 
  
Геометрия фигуры может быть выражено в нескольких разделах **геометрии** . Несколько путей можно использовать при нескольких путей иметь различные свойства (например, пути [кадрирование изображений](clippingpath-cell-foreign-image-info-section.md) ). 
  
## <a name="remarks"></a>Замечания

Раздел **геометрии** содержит следующие типы строки. Дополнительные сведения см в разделах строки. 
  
|**Row**|**Описание**|
|:-----|:-----|
|[MoveTo](moveto-row-geometry-section.md) <br/> |Перемещение координаты.  <br/> |
|[LineTo](lineto-row-geometry-section.md) <br/> |Линии координаты.  <br/> |
|[ArcTo](arcto-row-geometry-section.md) <br/> |Нарисуйте дугу координаты.  <br/> |
|[EllipticalArcTo](ellipticalarcto-row-geometry-section.md) <br/> |Создайте руководство, чтобы координаты.  <br/> |
|[PolylineTo](polylineto-row-geometry-section.md) <br/> |Рисование ломаной или последовательных строк для координаты.  <br/> |
|[NURBSTo](nurbsto-row-geometry-section.md) <br/> |Создавать неоднородной rational-сплайн (NURBS), чтобы координаты.  <br/> |
|[SplineStart](splinestart-row-geometry-section.md) <br/> |Запустите сплайна.  <br/> |
|[SplineKnot](splineknot-row-geometry-section.md) <br/> |Нарисуйте сегмента сплайна координата число узлов.  <br/> |
|[InfiniteLine](infiniteline-row-geometry-section.md) <br/> |Рисование бесконечное строки из одного координат в другую.  <br/> |
|[Эллипс](ellipse-row-geometry-section.md) <br/> |Рисование эллипсы из центра координат и основные и вспомогательные оси.  <br/> |
|[RelCubBezTo](relcubbezto-row-geometry-section.md) <br/> |Рисование кубические Безье график относительно ширину и высоту фигуры.  <br/> |
|[RelEllipticalArcTo](relellipticalarcto-row-geometry-section.md) <br/> |Рисование руководство для координат относительно высоту и ширину фигуры.  <br/> |
|[RelLineTo](rellineto-row-geometry-section.md) <br/> |Линии координат относительно высоту и ширину фигуры.  <br/> |
|[RelMoveTo](relmoveto-row-geometry-section.md) <br/> |Перемещение координат относительно ширину и высоту фигуры.  <br/> |
|[RelQuadBezTo](relquadbezto-row-geometry-section.md) <br/> |Рисование кривой Безье второго относительно ширину и высоту фигуры.  <br/> |
   
Чтобы изменить тип строки в этом разделе, щелкните правой кнопкой мыши строку и нажмите кнопку **Изменить тип строки** в контекстном меню. 
  

