---
title: Элемент Row (Geometry Section) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 2b273958-1997-7c63-4a61-d231f023a81f
description: Содержит строки, которые перечисляют координаты вершин для линий и дуг, которые составляют фигуру.
ms.openlocfilehash: 6dbf18b749ed072645c4941922729010f74fc0ae
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/29/2019
ms.locfileid: "34540856"
---
# <a name="row-element-geometry-section-visio-xml"></a>Элемент Row (Geometry Section) (Visio XML)

Содержит строки, которые перечисляют координаты вершин для линий и дуг, которые составляют фигуру.
  
## <a name="element-information"></a>Сведения об элементе

|||
|:-----|:-----|
|**Тип элемента** <br/> |[GeometryRow_Type](geometry_type-complextypevisio-xml.md) <br/> |
|**Пространство имен** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Файл схемы** <br/> |VisioSchema15.xsd  <br/> |
|**Части документа** <br/> |master#.xml, page#.xml  <br/> |
   
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
|[Section](section-element-sheet_type-complextypevisio-xml.md) <br/> |[Section_Type](section_type-complextypevisio-xml.md) <br/> |Содержит строки, которые перечисляют координаты вершин для линий и дуг, которые составляют фигуру.  <br/> |
   
### <a name="child-elements"></a>Дочерние элементы

> [!NOTE]
> Элемент Cell — единственный его дитя. В зависимости от атрибута "T" этого элемента, значения элементов Cell различаются. В приведенной ниже таблице паратетический текст в имени элемента соответствует значению "T", к которому применяется раздел. 
  
|**Элемент**|**Тип**|**Описание**|
|:-----|:-----|:-----|
|[Элемент Cell (строка ArcTo)](arcto-row-geometry-section.md) <br/> |[Cell_Type](https://msdn.microsoft.com/library/6f23bcc4-af93-4023-a380-3e78a228e166%28Office.15%29.aspx) <br/> |Содержит координаты x и y и лук цикловой дуги.  <br/> |
|[Элемент Cell (строка Ellipse)](ellipse-row-geometry-section.md) <br/> |[Cell_Type](https://msdn.microsoft.com/library/6f23bcc4-af93-4023-a380-3e78a228e166%28Office.15%29.aspx) <br/> |Содержит координаты X и Y центральной точки эллипса и две точки эллипса.  <br/> |
|[Элемент Cell (строка EllipticalArcTo)](ellipticalarcto-row-geometry-section.md) <br/> |[Cell_Type](https://msdn.microsoft.com/library/6f23bcc4-af93-4023-a380-3e78a228e166%28Office.15%29.aspx) <br/> |Содержит координаты X и Y конечной точки эллиптической дуги, координат x и y контрольных точек на дуге, угол от оси X до основной оси эллипса и соотношение между основной и второстепенной осями эллипса.  <br/> |
|[Элемент Cell (строка InfiniteLine)](infiniteline-row-geometry-section.md) <br/> |[Cell_Type](https://msdn.microsoft.com/library/6f23bcc4-af93-4023-a380-3e78a228e166%28Office.15%29.aspx) <br/> |Содержит координаты x и y двух точек на бесконечной линии.  <br/> |
|[Элемент Cell (строка LineTo)](lineto-row-geometry-section.md) <br/> |[Cell_Type](https://msdn.microsoft.com/library/6f23bcc4-af93-4023-a380-3e78a228e166%28Office.15%29.aspx) <br/> |Содержит координаты x и y конечной вершины сегмента прямой линии.  <br/> |
|[Элемент Cell (строка MoveTo)](moveto-row-geometry-section.md) <br/> |[Cell_Type](https://msdn.microsoft.com/library/6f23bcc4-af93-4023-a380-3e78a228e166%28Office.15%29.aspx) <br/> |Содержит координаты X и Y первой вершины фигуры или представляет координаты X и Y первой вершины после разрыва пути.  <br/> |
|[Элемент Cell (строка NURBSTo)](nurbsto-row-geometry-section.md) <br/> |[Cell_Type](https://msdn.microsoft.com/library/6f23bcc4-af93-4023-a380-3e78a228e166%28Office.15%29.aspx) <br/> |Содержит координаты x и y, положение от второго до последнего степеней, положение последнего веса, положение первого степеня, положение первого веса и формулу для несвязаного рационального B-spline (NURBS).  <br/> |
|[Элемент Cell (строка PolyLineTo)](polylineto-row-geometry-section.md) <br/> |[Cell_Type](https://msdn.microsoft.com/library/6f23bcc4-af93-4023-a380-3e78a228e166%28Office.15%29.aspx) <br/> |Содержит координаты X и Y последней точки многолинейной и многолинейной формулы.  <br/> |
|[Элемент Cell (строка RelCubBezTo)](relcubbezto-row-geometry-section.md) <br/> |[Cell_Type](https://msdn.microsoft.com/library/6f23bcc4-af93-4023-a380-3e78a228e166%28Office.15%29.aspx) <br/> |Содержит координаты X и Y конечной точки кривой Безье второго канала относительно ширины и высоты фигуры, координат x и y контрольной точки начала относительной ширины и высоты кривой, а также координаты X и Y контрольной точки относительно ширины и высоты кривой.  <br/> |
|[Элемент Cell (строка RelQuadBezTo)](relquadbezto-row-geometry-section.md) <br/> |[Cell_Type](https://msdn.microsoft.com/library/6f23bcc4-af93-4023-a380-3e78a228e166%28Office.15%29.aspx) <br/> |Содержит координаты x и y конечной точки кривой Безье 1 относительно ширины и высоты фигуры, а также координат x и y контрольной точки относительной ширины и высоты кривой.  <br/> |
|[Элемент Cell (строка RelEllipticalArcTo)](relellipticalarcto-row-geometry-section.md) <br/> |[Cell_Type](https://msdn.microsoft.com/library/6f23bcc4-af93-4023-a380-3e78a228e166%28Office.15%29.aspx) <br/> |Содержит координаты X и Y конечной точки эллиптической дуги относительно ширины и высоты фигуры, координат x и Y контрольных точек на дуге относительно ширины и высоты фигуры, угла от оси x до основной оси эллипса и соотношения между основной и второстепенной осями эллипса.  <br/> |
|[Элемент Cell (строка RelLineTo)](rellineto-row-geometry-section.md) <br/> |[Cell_Type](https://msdn.microsoft.com/library/6f23bcc4-af93-4023-a380-3e78a228e166%28Office.15%29.aspx) <br/> |Содержит координаты x и y конечной вершины сегмента прямой линии относительно ширины и высоты фигуры.  <br/> |
|[Элемент Cell (строка RelMoveTo)](relmoveto-row-geometry-section.md) <br/> |[Cell_Type](https://msdn.microsoft.com/library/6f23bcc4-af93-4023-a380-3e78a228e166%28Office.15%29.aspx) <br/> |Содержит координаты X и Y первой вершины фигуры или координаты X и Y первой вершины после разрыва пути относительно высоты и ширины фигуры.  <br/> |
|[Элемент Cell (строка RelQuadBezTo)](relquadbezto-row-geometry-section.md) <br/> |[Cell_Type](https://msdn.microsoft.com/library/6f23bcc4-af93-4023-a380-3e78a228e166%28Office.15%29.aspx) <br/> |Содержит координаты x и y конечной точки кривой Безье 1 относительно ширины и высоты фигуры, а также координат x и y контрольной точки относительной ширины и высоты кривой.  <br/> |
|[Элемент Cell (строка SplineKnot)](splineknot-row-geometry-section.md) <br/> |[Cell_Type](https://msdn.microsoft.com/library/6f23bcc4-af93-4023-a380-3e78a228e166%28Office.15%29.aspx) <br/> |Содержит координаты x и y для точки управления сплайна и замещести сплайна.  <br/> |
|[Элемент Cell (строка SplineStart)](splinestart-row-geometry-section.md) <br/> |[Cell_Type](https://msdn.microsoft.com/library/6f23bcc4-af93-4023-a380-3e78a228e166%28Office.15%29.aspx) <br/> |Содержит координаты x- и y для второй контрольной точки сплайна, второй подмайки, первой степени, последнего степеня и степени сплайна.  <br/> |
   
### <a name="attributes"></a>Атрибуты

|**Атрибут**|**Тип**|**Обязательный**|**Описание**|**Возможные значения**|
|:-----|:-----|:-----|:-----|:-----|
|Del  <br/> |xsd:boolean  <br/> |необязательный  <br/> |Указывает, была ли удалена строка, которая в противном случае была бы унаследована от этаго фигуры.  <br/> |Значения типа xsd:boolean.  <br/> |
|IX  <br/> |xsd:unsignedInt  <br/> |необязательный  <br/> |Указывает идентификатор строки, основанный на одном. Оно должно быть неподдерживаемо и больше других идентификаторов в том же разделе. Атрибут IX используется только для разделов Character, Connection, Field, FillGradient, Geometry, Layer, LineGradient, Paragraph, Reviewer, Scratch и Tabs. Строка может иметь только один из атрибутов IX или N.  <br/> |Значения типа xsd:unsignedInt.  <br/> |
|LocalName  <br/> |xsd:string  <br/> |необязательный  <br/> |Указывает уникальное имя строки, зависимое от языка.  <br/> |Значения типа xsd:string.  <br/> |
|N  <br/> |xsd:string  <br/> |необязательный  <br/> |Указывает уникальное независимое от языка имя строки. Атрибут N используется только для разделов "Пользователь", "Свойство", "Действия", "Управление", "Подключение", "Гиперссылка" и "ActionTag". Строка может иметь только один из атрибутов IX или N.  <br/> |Значения типа xsd:string.  <br/> |
|T  <br/> |xsd:string  <br/> |необязательный  <br/> |Указывает тип геометрического пути, представленного строкой и используемого при визуализации геометрии. Атрибут T используется только для раздела "Геометрия".  <br/> |Значения типа xsd:string.  <br/> |
   
## <a name="remarks"></a>Примечания

Атрибут **T** этого элемента **Row** должен быть одним из ограниченного набора значений, соответствующих строкам ShapeSheet. Чтобы определить значения атрибута **T,** разрешенные для этого элемента **Row,** обратитесь к таблице ниже. 
  
|**Значение**|**Описание**|**Дополнительные сведения**|
|:-----|:-----|:-----|
|ArcTo  <br/> |Содержит координаты x и y и лук цикловой дуги.  <br/> |[ArcTo Row (Geometry Section)](arcto-row-geometry-section.md) <br/> |
|Ellipse  <br/> |Содержит координаты X и Y центральной точки эллипса и две точки эллипса.  <br/> |[Ellipse Row (Geometry Section)](ellipse-row-geometry-section.md) <br/> |
|EllipticalArcTo  <br/> |Содержит координаты X и Y конечной точки эллиптической дуги, координат x и y контрольных точек на дуге, угол от оси X до основной оси эллипса и соотношение между основной и второстепенной осями эллипса.  <br/> |[EllipticalArcTo Row (Geometry Section)](ellipticalarcto-row-geometry-section.md) <br/> |
|InfiniteLine  <br/> |Содержит координаты x и y двух точек на бесконечной линии.  <br/> |[InfiniteLine Row (Geometry Section)](infiniteline-row-geometry-section.md) |
|LineTo  <br/> |Содержит координаты x и y конечной вершины сегмента прямой линии.  <br/> |[LineTo Row (Geometry Section)](lineto-row-geometry-section.md) <br/> |
|MoveTo  <br/> |Содержит координаты X и Y первой вершины фигуры или представляет координаты X и Y первой вершины после разрыва пути.  <br/> |[MoveTo Row (Geometry Section)](moveto-row-geometry-section.md) <br/> |
|NURBSTo  <br/> |Содержит координаты x и y, положение от второго до последнего степеней, положение последнего веса, положение первого степеня, положение первого веса и формулу для несвязаного рационального B-spline (NURBS).  <br/> |[NURBSTo Row (Geometry Section)](nurbsto-row-geometry-section.md) <br/> |
|PolylineTo  <br/> |Содержит координаты X и Y последней точки многолинейной и многолинейной формулы.  <br/> |[PolylineTo Row (Geometry Section)](polylineto-row-geometry-section.md) <br/> |
|RelCubBezTo  <br/> |Содержит координаты X и Y конечной точки кривой Безье второго канала относительно ширины и высоты фигуры, координат x и y контрольной точки начала относительной ширины и высоты кривой, а также координаты X и Y контрольной точки относительно ширины и высоты кривой.  <br/> |[RelCubBezTo Row (Geometry Section)](relcubbezto-row-geometry-section.md) <br/> |
|RelEllipticalArcTo  <br/> |Содержит координаты X и Y конечной точки эллиптической дуги относительно ширины и высоты фигуры, координат x и Y контрольных точек на дуге относительно ширины и высоты фигуры, угла от оси x до основной оси эллипса и соотношения между основной и второстепенной осями эллипса.  <br/> |[RelEllipticalArcTo Row (Geometry Section)](relellipticalarcto-row-geometry-section.md) <br/> |
|RelLineTo  <br/> |Содержит координаты x и y конечной вершины сегмента прямой линии относительно ширины и высоты фигуры.  <br/> |[RelLineTo Row (Geometry Section)](rellineto-row-geometry-section.md) <br/> |
|RelMoveTo  <br/> |Содержит координаты X и Y первой вершины фигуры или координаты X и Y первой вершины после разрыва пути относительно высоты и ширины фигуры.  <br/> |[RelMoveTo Row (Geometry Section)](relmoveto-row-geometry-section.md) <br/> |
|RelQuadBezTo  <br/> |Содержит координаты x и y конечной точки кривой Безье 1 относительно ширины и высоты фигуры, а также координат x и y контрольной точки относительной ширины и высоты кривой.  <br/> |[RelQuadBezTo Row (Geometry Section)](relquadbezto-row-geometry-section.md) <br/> |
|SplineKnot  <br/> |Содержит координаты x и y для точки управления сплайна и замещести сплайна.  <br/> |[SplineKnot Row (Geometry Section)](splineknot-row-geometry-section.md) <br/> |
|SplineStart  <br/> |Содержит координаты x- и y для второй контрольной точки сплайна, второй подмайки, первой степени, последнего степеня и степени сплайна.  <br/> |[SplineStart Row (Geometry Section)](splinestart-row-geometry-section.md) <br/> |
   

