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
  
Геометрия фигуры может быть выражена в нескольких **разделах геометрии.** Несколько путей могут быть полезны, если у нескольких путей [](clippingpath-cell-foreign-image-info-section.md) разные свойства (например, пути обрезки изображений). 
  
## <a name="remarks"></a>Примечания

Раздел **"Геометрия"** содержит следующие типы строк. Подробные сведения см. в темах по строкам. 
  
|Строка|Описание|
|:-----|:-----|
|[MoveTo](moveto-row-geometry-section.md) <br/> |Перейти к координате.  <br/> |
|[LineTo](lineto-row-geometry-section.md) <br/> |Нарисуйте линию в координату.  <br/> |
|[ArcTo](arcto-row-geometry-section.md) <br/> |Нарисуйте циклическая дуга к координате.  <br/> |
|[EllipticalArcTo](ellipticalarcto-row-geometry-section.md) <br/> |Нарисуйте эллиптическую дугу в координате.  <br/> |
|[PolylineTo](polylineto-row-geometry-section.md) <br/> |Нарисуйте многолинейную или последовательные линии в координате.  <br/> |
|[NURBSTo](nurbsto-row-geometry-section.md) <br/> |Нарисуйте не однородный логический B-spline (NURBS) в координате.  <br/> |
|[SplineStart](splinestart-row-geometry-section.md) <br/> |Запустите spline.  <br/> |
|[SplineKnot](splineknot-row-geometry-section.md) <br/> |Отрисовка сегмента сплайна в координате координаты координаты.  <br/> |
|[InfiniteLine](infiniteline-row-geometry-section.md) <br/> |Нарисуйте бесконечное число строк из одной координаты в другую.  <br/> |
|[Ellipse](ellipse-row-geometry-section.md) <br/> |Нарисуйте эллипс из центральной координаты и основной или второстепенной оси.  <br/> |
|[RelCubBezTo](relcubbezto-row-geometry-section.md) <br/> |Нарисуйте кривая Безье по ширине и высоте фигуры.  <br/> |
|[RelEllipticalArcTo](relellipticalarcto-row-geometry-section.md) <br/> |Нарисуйте эллиптическую дугу к координате относительно высоты и ширины фигуры.  <br/> |
|[RelLineTo](rellineto-row-geometry-section.md) <br/> |Нарисуйте линию к координате относительно высоты и ширины фигуры.  <br/> |
|[RelMoveTo](relmoveto-row-geometry-section.md) <br/> |Перемещение к координате относительно ширины и высоты фигуры.  <br/> |
|[RelQuadBezTo](relquadbezto-row-geometry-section.md) <br/> |Рисует кривую Безье четверного безье относительно ширины и высоты фигуры.  <br/> |
   
Чтобы изменить тип строки в этом разделе, щелкните  ее правой кнопкой мыши и выберите пункт "Изменить тип строки" в ярлыковом меню. 
  

