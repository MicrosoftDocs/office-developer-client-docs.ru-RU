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
description: Содержит строки, в которых перечислены координаты вершин для линий и дуг, составляющих фигуру.
ms.openlocfilehash: 32a815015c7d1764399215767b674668b7235832
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33423911"
---
# <a name="geometry-section"></a>Geometry Section

Содержит строки, в которых перечислены координаты вершин для линий и дуг, составляющих фигуру. 
  
Геометрия фигуры может быть выражена в нескольких разделах **геометрии** . Несколько путей удобно использовать, если несколько путей имеют различные свойства (например, [обтравочные](clippingpath-cell-foreign-image-info-section.md) контуры изображений). 
  
## <a name="remarks"></a>Примечания

Раздел " **геометрия** " содержит следующие типы строк. Дополнительные сведения см. 
  
|**Строка**|**Описание**|
|:-----|:-----|
|[MoveTo](moveto-row-geometry-section.md) <br/> |Перейти к координате.  <br/> |
|[LineTo](lineto-row-geometry-section.md) <br/> |НаРисуйте линию по координатам.  <br/> |
|[ArcTo](arcto-row-geometry-section.md) <br/> |Рисование круговой дуги в координатах.  <br/> |
|[EllipticalArcTo](ellipticalarcto-row-geometry-section.md) <br/> |НаРисуйте эллиптическую дугу по координатам.  <br/> |
|[PolylineTo](polylineto-row-geometry-section.md) <br/> |Рисование ломаной линии или последовательных линий в координатах.  <br/> |
|[NURBSTo](nurbsto-row-geometry-section.md) <br/> |Рисование неоднородного рационального B-сплайна (NURBS) в координатах.  <br/> |
|[SplineStart](splinestart-row-geometry-section.md) <br/> |Начало сплайна.  <br/> |
|[SplineKnot](splineknot-row-geometry-section.md) <br/> |НаРисуйте сегмент сплайна в координату кнот.  <br/> |
|[InfiniteLine](infiniteline-row-geometry-section.md) <br/> |НаРисуйте бесконечную линию от одной координаты к другой.  <br/> |
|[Ellipse](ellipse-row-geometry-section.md) <br/> |Рисование эллипса по Центральной координате и основной или дополнительной оси.  <br/> |
|[RelCubBezTo](relcubbezto-row-geometry-section.md) <br/> |Рисование кривой Безье третьего порядка относительно ширины и высоты фигуры.  <br/> |
|[RelEllipticalArcTo](relellipticalarcto-row-geometry-section.md) <br/> |НаРисуйте эллиптическую дугу по координатам относительно высоты и ширины фигуры.  <br/> |
|[RelLineTo](rellineto-row-geometry-section.md) <br/> |Рисование линии по координатам относительно высоты и ширины фигуры.  <br/> |
|[RelMoveTo](relmoveto-row-geometry-section.md) <br/> |Переход на координату, связанную с шириной и высотой фигуры.  <br/> |
|[RelQuadBezTo](relquadbezto-row-geometry-section.md) <br/> |Рисует кривую Безье второго размера относительно ширины и высоты фигуры.  <br/> |
   
Чтобы изменить тип строки в этом разделе, щелкните строку правой кнопкой мыши и выберите в контекстном меню команду **изменить тип строки** . 
  

