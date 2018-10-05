---
title: Элемент Row (раздел геометрии) ('Visio XML»)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 2b273958-1997-7c63-4a61-d231f023a81f
description: Содержит строки, в которых перечислены координаты грани для линий и дуг, образующих фигуру.
ms.openlocfilehash: 53482b0db3f2deb3c8e2ba30f41be67f0d9e27a0
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25400091"
---
# <a name="row-element-geometry-section-visio-xml"></a>Элемент Row (раздел геометрии) ('Visio XML»)

Содержит строки, в которых перечислены координаты грани для линий и дуг, образующих фигуру.
  
## <a name="element-information"></a>Сведения об элементе

|||
|:-----|:-----|
|**Тип элемента** <br/> |[GeometryRow_Type](geometry_type-complextypevisio-xml.md) <br/> |
|**Пространство имен** <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Файл схемы** <br/> |VisioSchema15.xsd  <br/> |
|**Части документа** <br/> |главные # .xml, страницы # .xml  <br/> |
   
## <a name="definition"></a>Определение

```XML
< xs:element name="Row" type="GeometryRow_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a>Элементы и атрибуты

Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений. 
  
### <a name="parent-elements"></a>Родительские элементы

|**Элемент**|**Тип**|**Описание**|
|:-----|:-----|:-----|
|[Раздел](section-element-sheet_type-complextypevisio-xml.md) <br/> |[Section_Type](section_type-complextypevisio-xml.md) <br/> |Содержит строки, в которых перечислены координаты грани для линий и дуг, образующих фигуру.  <br/> |
   
### <a name="child-elements"></a>Дочерние элементы

> [!NOTE]
> Элемент ячейки является единственным дочерним этого элемента. В зависимости от атрибута «T» этот элемент значения ячейки элементов отличаться. В следующей таблице parathetical текст в имени элемента соответствует значению «T», к которому применяется тема. 
  
|**Элемент**|**Тип**|**Описание**|
|:-----|:-----|:-----|
|[Элемент Cell (строка ArcTo)](arcto-row-geometry-section.md) <br/> |[Cell_Type](https://msdn.microsoft.com/library/6f23bcc4-af93-4023-a380-3e78a228e166%28Office.15%29.aspx) <br/> |Содержит координаты x и y и галстук дугу.  <br/> |
|[Элемент Cell (строка Ellipse)](ellipse-row-geometry-section.md) <br/> |[Cell_Type](https://msdn.microsoft.com/library/6f23bcc4-af93-4023-a380-3e78a228e166%28Office.15%29.aspx) <br/> |Содержит x и y координаты центра эллипса и двумя точками на эллипс.  <br/> |
|[Элемент Cell (строка EllipticalArcTo)](ellipticalarcto-row-geometry-section.md) <br/> |[Cell_Type](https://msdn.microsoft.com/library/6f23bcc4-af93-4023-a380-3e78a228e166%28Office.15%29.aspx) <br/> |Содержит координаты x и y-руководство пользователя конечной точки координат x и y-элемента управления указывает на дуги угол главных осей эллипса и отношение между эллипса основной и дополнительной осей.  <br/> |
|[Элемент Cell (строка InfiniteLine)](infiniteline-row-geometry-section.md) <br/> |[Cell_Type](https://msdn.microsoft.com/library/6f23bcc4-af93-4023-a380-3e78a228e166%28Office.15%29.aspx) <br/> |Содержит x и y координаты двух точек на строку не ограничен.  <br/> |
|[Элемент Cell (строка LineTo)](lineto-row-geometry-section.md) <br/> |[Cell_Type](https://msdn.microsoft.com/library/6f23bcc4-af93-4023-a380-3e78a228e166%28Office.15%29.aspx) <br/> |Содержит x- и y окончания вершины прямой сегмент.  <br/> |
|[Элемент Cell (строка MoveTo)](moveto-row-geometry-section.md) <br/> |[Cell_Type](https://msdn.microsoft.com/library/6f23bcc4-af93-4023-a380-3e78a228e166%28Office.15%29.aspx) <br/> |Содержит x и y координаты первой вершины фигуры или представляет x и y координаты первой вершины после приостановки пути.  <br/> |
|[Элемент Cell (строка NURBSTo)](nurbsto-row-geometry-section.md) <br/> |[Cell_Type](https://msdn.microsoft.com/library/6f23bcc4-af93-4023-a380-3e78a228e166%28Office.15%29.aspx) <br/> |Содержит положение координаты x и y-, второй — к последней число узлов, Позиция последнего вес, положение первого число узлов, положение первого вес и формулу для неоднородной rational-сплайн (NURBS).  <br/> |
|[Элемент Cell (строка PolyLineTo)](polylineto-row-geometry-section.md) <br/> |[Cell_Type](https://msdn.microsoft.com/library/6f23bcc4-af93-4023-a380-3e78a228e166%28Office.15%29.aspx) <br/> |Содержит координаты x и y-последней точки ломаной и ломаной формулы.  <br/> |
|[Элемент Cell (строка RelCubBezTo)](relcubbezto-row-geometry-section.md) <br/> |[Cell_Type](https://msdn.microsoft.com/library/6f23bcc4-af93-4023-a380-3e78a228e166%28Office.15%29.aspx) <br/> |Содержит x и y координаты конечной точки кубические Безье график относительно высоты и ширины фигуры, x и y координаты контрольной точки начала фигуры график относительно ширины и высоты и x и y координаты элемента управления точка конца фигуры график относительно ширины и высоты.  <br/> |
|[Элемент Cell (строка RelQuadBezTo)](relquadbezto-row-geometry-section.md) <br/> |[Cell_Type](https://msdn.microsoft.com/library/6f23bcc4-af93-4023-a380-3e78a228e166%28Office.15%29.aspx) <br/> |Содержит x и y координаты конечной точки кривая Безье относительно фигуры ширины и высоты и x и y координаты контрольной точки фигуры график относительно ширины и высоты.  <br/> |
|[Элемент Cell (строка RelEllipticalArcTo)](relellipticalarcto-row-geometry-section.md) <br/> |[Cell_Type](https://msdn.microsoft.com/library/6f23bcc4-af93-4023-a380-3e78a228e166%28Office.15%29.aspx) <br/> |Содержит координаты x и y-руководство пользователя конечной точки относительно высоты и ширины фигуры, x и y координаты контрольные точки на arc относительно фигуры ширина и высота, угол оси основные эллипса и отношение между основной и дополнительной осей эллипса.  <br/> |
|[Элемент Cell (строка RelLineTo)](rellineto-row-geometry-section.md) <br/> |[Cell_Type](https://msdn.microsoft.com/library/6f23bcc4-af93-4023-a380-3e78a228e166%28Office.15%29.aspx) <br/> |Содержит x- и y окончания вершины отрезка прямой линии относительно ширины и высоты фигуры.  <br/> |
|[Элемент Cell (строка RelMoveTo)](relmoveto-row-geometry-section.md) <br/> |[Cell_Type](https://msdn.microsoft.com/library/6f23bcc4-af93-4023-a380-3e78a228e166%28Office.15%29.aspx) <br/> |Содержит x и y координаты первой вершины фигуры или x и y координаты первой вершины после приостановки пути, относящиеся к высоту и ширину фигуры.  <br/> |
|[Элемент Cell (строка RelQuadBezTo)](relquadbezto-row-geometry-section.md) <br/> |[Cell_Type](https://msdn.microsoft.com/library/6f23bcc4-af93-4023-a380-3e78a228e166%28Office.15%29.aspx) <br/> |Содержит x и y координаты конечной точки кривая Безье относительно фигуры ширины и высоты и x и y координаты контрольной точки фигуры график относительно ширины и высоты.  <br/> |
|[Элемент Cell (строка SplineKnot)](splineknot-row-geometry-section.md) <br/> |[Cell_Type](https://msdn.microsoft.com/library/6f23bcc4-af93-4023-a380-3e78a228e166%28Office.15%29.aspx) <br/> |Содержит координаты x и y-сплайн точки управления и число узлов сплайна.  <br/> |
|[Элемент Cell (строка SplineStart)](splinestart-row-geometry-section.md) <br/> |[Cell_Type](https://msdn.microsoft.com/library/6f23bcc4-af93-4023-a380-3e78a228e166%28Office.15%29.aspx) <br/> |Содержит координаты x и y — для второй контрольной точки сплайна, его второй число узлов, его первого число узлов, последний число узлов и степень сплайн.  <br/> |
   
### <a name="attributes"></a>Атрибуты

|**Атрибут**|**Тип**|**Обязательный**|**Описание**|**Возможные значения**|
|:-----|:-----|:-----|:-----|:-----|
|DEL  <br/> |XSD:Boolean  <br/> |необязательный  <br/> |Указывает, был ли удален строку, в противном случае будут унаследованы от образца фигуры.  <br/> |Значения типа xsd:boolean.  <br/> |
|IX  <br/> |XSD:unsignedInt  <br/> |необязательный  <br/> |Указывает идентификатор на основе одной строки. Оно должно быть unqiue и больше, чем другие идентификаторы в одном разделе. Атрибут IX используется только для разделов символ, подключения, поле, FillGradient, геометрии, уровень, LineGradient, абзаца, редактор, нуля и вкладок. Строка может иметь только один из атрибутов IX или N.  <br/> |Значения типа xsd:unsignedInt.  <br/> |
|LocalName  <br/> |XSD:String  <br/> |необязательный  <br/> |Указывает уникальное имя зависит от языка строки.  <br/> |Значения типа xsd:string.  <br/> |
|N  <br/> |XSD:String  <br/> |необязательный  <br/> |Указывает уникальное имя зависящего от языка строки. Атрибут N используется только для пользователя, свойство, действия, элемент управления, подключения, гиперссылки и ActionTag разделы. Строка может иметь только один из атрибутов IX или N.  <br/> |Значения типа xsd:string.  <br/> |
|T  <br/> |XSD:String  <br/> |необязательный  <br/> |Указывает тип геометрического пути представленного строкой и используется в геометрии визуализации. Атрибут T используется только для раздел геометрии.  <br/> |Значения типа xsd:string.  <br/> |
   
## <a name="remarks"></a>Замечания

Атрибут **T** этого элемента **строки** должен быть один из ограниченный набор значений, которые соответствуют строкам таблицы свойств фигуры. Обратитесь к таблице ниже для определения значений атрибутов **T** , разрешенных для этого элемента **строки** . 
  
|**Значение**|**Описание**|**Дополнительные сведения**|
|:-----|:-----|:-----|
|ArcTo  <br/> |Содержит координаты x и y и галстук дугу.  <br/> |[Строка ArcTo (раздел "Геометрия")](arcto-row-geometry-section.md) <br/> |
|Ellipse  <br/> |Содержит x и y координаты центра эллипса и двумя точками на эллипс.  <br/> |[Строка Ellipse (раздел "Геометрия")](ellipse-row-geometry-section.md) <br/> |
|EllipticalArcTo  <br/> |Содержит координаты x и y-руководство пользователя конечной точки координат x и y-элемента управления указывает на дуги угол главных осей эллипса и отношение между эллипса основной и дополнительной осей.  <br/> |[Строка EllipticalArcTo (раздел "Геометрия")](ellipticalarcto-row-geometry-section.md) <br/> |
|InfiniteLine  <br/> |Содержит x и y координаты двух точек на строку не ограничен.  <br/> |[Строка InfiniteLine (раздел "Геометрия")](infiniteline-row-geometry-section.md) |
|LineTo  <br/> |Содержит x- и y окончания вершины прямой сегмент.  <br/> |[Строка LineTo (раздел "Геометрия")](lineto-row-geometry-section.md) <br/> |
|MoveTo  <br/> |Содержит x и y координаты первой вершины фигуры или представляет x и y координаты первой вершины после приостановки пути.  <br/> |[Строка MoveTo (раздел "Геометрия")](moveto-row-geometry-section.md) <br/> |
|NURBSTo  <br/> |Содержит положение координаты x и y-, второй — к последней число узлов, Позиция последнего вес, положение первого число узлов, положение первого вес и формулу для неоднородной rational-сплайн (NURBS).  <br/> |[Строка NURBSTo (раздел "Геометрия")](nurbsto-row-geometry-section.md) <br/> |
|PolylineTo  <br/> |Содержит координаты x и y-последней точки ломаной и ломаной формулы.  <br/> |[Строка PolylineTo (раздел "Геометрия")](polylineto-row-geometry-section.md) <br/> |
|RelCubBezTo  <br/> |Содержит x и y координаты конечной точки кубические Безье график относительно высоты и ширины фигуры, x и y координаты контрольной точки начала фигуры график относительно ширины и высоты и x и y координаты элемента управления точка конца фигуры график относительно ширины и высоты.  <br/> |[Строка RelCubBezTo (раздел "Геометрия")](relcubbezto-row-geometry-section.md) <br/> |
|RelEllipticalArcTo  <br/> |Содержит координаты x и y-руководство пользователя конечной точки относительно высоты и ширины фигуры, x и y координаты контрольные точки на arc относительно фигуры ширина и высота, угол оси основные эллипса и отношение между основной и дополнительной осей эллипса.  <br/> |[Строка RelEllipticalArcTo (раздел "Геометрия")](relellipticalarcto-row-geometry-section.md) <br/> |
|RelLineTo  <br/> |Содержит x- и y окончания вершины отрезка прямой линии относительно ширины и высоты фигуры.  <br/> |[Строка RelLineTo (раздел "Геометрия")](rellineto-row-geometry-section.md) <br/> |
|RelMoveTo  <br/> |Содержит x и y координаты первой вершины фигуры или x и y координаты первой вершины после приостановки пути, относящиеся к высоту и ширину фигуры.  <br/> |[Строка RelMoveTo (раздел "Геометрия")](relmoveto-row-geometry-section.md) <br/> |
|RelQuadBezTo  <br/> |Содержит x и y координаты конечной точки кривая Безье относительно фигуры ширины и высоты и x и y координаты контрольной точки фигуры график относительно ширины и высоты.  <br/> |[Строка RelQuadBezTo (раздел "Геометрия")](relquadbezto-row-geometry-section.md) <br/> |
|SplineKnot  <br/> |Содержит координаты x и y-сплайн точки управления и число узлов сплайна.  <br/> |[Строка SplineKnot (раздел "Геометрия")](splineknot-row-geometry-section.md) <br/> |
|SplineStart  <br/> |Содержит координаты x и y — для второй контрольной точки сплайна, его второй число узлов, его первого число узлов, последний число узлов и степень сплайн.  <br/> |[Строка SplineStart (раздел "Геометрия")](splinestart-row-geometry-section.md) <br/> |
   

