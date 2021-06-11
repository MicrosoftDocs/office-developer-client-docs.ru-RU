---
title: Geometry Section
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm2055
localization_priority: Normal
ms.assetid: 75601a1e-6b1a-27ee-a2bd-69e569315982
description: Содержит строки, которые перечисляют координаты вершин для линий и дуг, которые составляют фигуру.
ms.openlocfilehash: d45f960ecc697dc6f0f5a0efa18e6cbbc6e4fff0
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/29/2019
ms.locfileid: "34542284"
---
# <a name="geometry-section"></a>Geometry Section

Содержит строки, которые перечисляют координаты вершин для линий и дуг, которые составляют фигуру. 
  
Геометрия фигуры может быть выражена в нескольких **разделах Геометрия.** Несколько путей могут быть полезны, если несколько путей имеют различные свойства (например, пути [вырезки изображений).](clippingpath-cell-foreign-image-info-section.md) 
  
## <a name="remarks"></a>Примечания

Раздел **Geometry** содержит следующие типы строк. Подробные сведения см. в разделе строки. 
  
|Строка|Описание|
|:-----|:-----|
|[MoveTo](moveto-row-geometry-section.md) <br/> |Перемещение в координаты.  <br/> |
|[LineTo](lineto-row-geometry-section.md) <br/> |Нарисуйте строку в координату.  <br/> |
|[ArcTo](arcto-row-geometry-section.md) <br/> |Нарисуйте круговую дугу в координаты.  <br/> |
|[EllipticalArcTo](ellipticalarcto-row-geometry-section.md) <br/> |Нарисуйте эллиптическую дугу в координаты.  <br/> |
|[PolylineTo](polylineto-row-geometry-section.md) <br/> |Нарисуйте в координате полилин или последовательные строки.  <br/> |
|[NURBSTo](nurbsto-row-geometry-section.md) <br/> |Нарисуйте не однородный рациональный B-spline (NURBS) в координату.  <br/> |
|[SplineStart](splinestart-row-geometry-section.md) <br/> |Запустите spline.  <br/> |
|[SplineKnot](splineknot-row-geometry-section.md) <br/> |Нарисуйте сегмент spline в координату узла.  <br/> |
|[InfiniteLine](infiniteline-row-geometry-section.md) <br/> |Нарисуйте бесконечную линию из одной координаты в другую.  <br/> |
|[Ellipse](ellipse-row-geometry-section.md) <br/> |Нарисуйте эллипс из центральной координаты и оси мажор/минор.  <br/> |
|[RelCubBezTo](relcubbezto-row-geometry-section.md) <br/> |Нарисуйте кубический кривой Безье относительно ширины и высоты фигуры.  <br/> |
|[RelEllipticalArcTo](relellipticalarcto-row-geometry-section.md) <br/> |Нарисуйте эллиптическую дугу в координату относительно высоты и ширины фигуры.  <br/> |
|[RelLineTo](rellineto-row-geometry-section.md) <br/> |Нарисуйте строку в координате относительно высоты и ширины фигуры.  <br/> |
|[RelMoveTo](relmoveto-row-geometry-section.md) <br/> |Перемещение в координаты относительно ширины и высоты фигуры.  <br/> |
|[RelQuadBezTo](relquadbezto-row-geometry-section.md) <br/> |Рисует квадратную кривую Безье относительно ширины и высоты фигуры.  <br/> |
   
Чтобы изменить тип строки в этом разделе, щелкните правой кнопкой мыши строку и нажмите **кнопку Изменить** строку в меню ярлыка. 
  

