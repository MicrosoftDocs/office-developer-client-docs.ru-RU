---
title: Элемент Row (Раздел геометрии) (Visio XML)
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
# <a name="row-element-geometry-section-visio-xml"></a>Элемент Row (Раздел геометрии) (Visio XML)

Содержит строки, которые перечисляют координаты вершин для линий и дуг, которые составляют фигуру.
  
## <a name="element-information"></a>Сведения об элементе

|||
|:-----|:-----|
|**Тип элемента** <br/> |[GeometryRow_Type](geometry_type-complextypevisio-xml.md) <br/> |
|**Пространство имен** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Файл схемы** <br/> |VisioSchema15.xsd  <br/> |
|**Части документов** <br/> |master#.xml, page#.xml  <br/> |
   
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
> Элемент Cell является единственным ребенком этого элемента. В зависимости от атрибута "T" этого элемента значение элементов Cell различается. В приведенной ниже таблице паратетический текст в имени элемента соответствует значению "T", к которому применяется тема. 
  
|**Элемент**|**Тип**|**Описание**|
|:-----|:-----|:-----|
|[Элемент Cell (строка ArcTo)](arcto-row-geometry-section.md) <br/> |[Cell_Type](https://msdn.microsoft.com/library/6f23bcc4-af93-4023-a380-3e78a228e166%28Office.15%29.aspx) <br/> |Содержит x- и y-координаты и нос круговой дуги.  <br/> |
|[Элемент Cell (строка Ellipse)](ellipse-row-geometry-section.md) <br/> |[Cell_Type](https://msdn.microsoft.com/library/6f23bcc4-af93-4023-a380-3e78a228e166%28Office.15%29.aspx) <br/> |Содержит x и y-координаты центральной точки эллипса и две точки на эллипсе.  <br/> |
|[Элемент Cell (строка EllipticalArcTo)](ellipticalarcto-row-geometry-section.md) <br/> |[Cell_Type](https://msdn.microsoft.com/library/6f23bcc4-af93-4023-a380-3e78a228e166%28Office.15%29.aspx) <br/> |Содержит x и y-координаты конечной точки эллиптической дуги, x и y-координаты точек управления на дуге, угол от оси x до основной оси эллипса и соотношение между основными и небольшими осями эллипса.  <br/> |
|[Элемент Cell (строка InfiniteLine)](infiniteline-row-geometry-section.md) <br/> |[Cell_Type](https://msdn.microsoft.com/library/6f23bcc4-af93-4023-a380-3e78a228e166%28Office.15%29.aspx) <br/> |Содержит x и y-координаты двух точек на бесконечной строке.  <br/> |
|[Элемент Cell (строка LineTo)](lineto-row-geometry-section.md) <br/> |[Cell_Type](https://msdn.microsoft.com/library/6f23bcc4-af93-4023-a380-3e78a228e166%28Office.15%29.aspx) <br/> |Содержит x-and y-координаты конечной вершины сегмента прямой линии.  <br/> |
|[Элемент Cell (строка MoveTo)](moveto-row-geometry-section.md) <br/> |[Cell_Type](https://msdn.microsoft.com/library/6f23bcc4-af93-4023-a380-3e78a228e166%28Office.15%29.aspx) <br/> |Содержит x и y-координаты первой вершины фигуры или представляет x- и y-координаты первого вершины после перерыва в пути.  <br/> |
|[Элемент Cell (строка NURBSTo)](nurbsto-row-geometry-section.md) <br/> |[Cell_Type](https://msdn.microsoft.com/library/6f23bcc4-af93-4023-a380-3e78a228e166%28Office.15%29.aspx) <br/> |Содержит x- и y-координаты, положение второго до последнего узла, положение последнего веса, положение первого узла, положение первого веса и формулу для неинформированной рациональной B-spline (NURBS).  <br/> |
|[Элемент Cell (строка PolyLineTo)](polylineto-row-geometry-section.md) <br/> |[Cell_Type](https://msdn.microsoft.com/library/6f23bcc4-af93-4023-a380-3e78a228e166%28Office.15%29.aspx) <br/> |Содержит x и y-координаты последней точки полилиновой и полилиновой формулы.  <br/> |
|[Элемент Cell (строка RelCubBezTo)](relcubbezto-row-geometry-section.md) <br/> |[Cell_Type](https://msdn.microsoft.com/library/6f23bcc4-af93-4023-a380-3e78a228e166%28Office.15%29.aspx) <br/> |Содержит x и y-координаты конечной точки кривой кубического Bézier относительно ширины и высоты фигуры, x- и y-координаты точки управления в начале ширины и высоты кривой относительной формы, а также x- и y-координаты точки управления окончанием ширины и высоты кривой относительной формы.  <br/> |
|[Элемент Cell (строка RelQuadBezTo)](relquadbezto-row-geometry-section.md) <br/> |[Cell_Type](https://msdn.microsoft.com/library/6f23bcc4-af93-4023-a380-3e78a228e166%28Office.15%29.aspx) <br/> |Содержит x и y-координаты конечной точки квадратной кривой Bézier по отношению к ширине и высоте фигуры, а также x- и y-координатам точки управления ширины и высоты кривой относительной формы.  <br/> |
|[Элемент Cell (строка RelEllipticalArcTo)](relellipticalarcto-row-geometry-section.md) <br/> |[Cell_Type](https://msdn.microsoft.com/library/6f23bcc4-af93-4023-a380-3e78a228e166%28Office.15%29.aspx) <br/> |Содержит x и y-координаты конечной точки эллиптической дуги по отношению к ширине и высоте фигуры, x- и y-координаты точек управления на дуге относительно ширины и высоты фигуры, угол от оси x до основной оси эллипса, а также соотношение между основными и небольшими осями эллипса.  <br/> |
|[Элемент Cell (строка RelLineTo)](rellineto-row-geometry-section.md) <br/> |[Cell_Type](https://msdn.microsoft.com/library/6f23bcc4-af93-4023-a380-3e78a228e166%28Office.15%29.aspx) <br/> |Содержит x-и y-координаты конечной вершины сегмента прямой линии относительно ширины и высоты фигуры.  <br/> |
|[Элемент Cell (строка RelMoveTo)](relmoveto-row-geometry-section.md) <br/> |[Cell_Type](https://msdn.microsoft.com/library/6f23bcc4-af93-4023-a380-3e78a228e166%28Office.15%29.aspx) <br/> |Содержит x- и y-координаты первой вершины формы или x- и y-координаты первого вершины после перерыва в пути, относительно высоты и ширины фигуры.  <br/> |
|[Элемент Cell (строка RelQuadBezTo)](relquadbezto-row-geometry-section.md) <br/> |[Cell_Type](https://msdn.microsoft.com/library/6f23bcc4-af93-4023-a380-3e78a228e166%28Office.15%29.aspx) <br/> |Содержит x и y-координаты конечной точки квадратной кривой Bézier по отношению к ширине и высоте фигуры, а также x- и y-координатам точки управления ширины и высоты кривой относительной формы.  <br/> |
|[Элемент Cell (строка SplineKnot)](splineknot-row-geometry-section.md) <br/> |[Cell_Type](https://msdn.microsoft.com/library/6f23bcc4-af93-4023-a380-3e78a228e166%28Office.15%29.aspx) <br/> |Содержит x и y-координаты для точки управления spline и узла spline.  <br/> |
|[Элемент Cell (строка SplineStart)](splinestart-row-geometry-section.md) <br/> |[Cell_Type](https://msdn.microsoft.com/library/6f23bcc4-af93-4023-a380-3e78a228e166%28Office.15%29.aspx) <br/> |Содержит x и y-координаты для второй точки управления spline, ее второго узла, первого узла, последнего узла и степени spline.  <br/> |
   
### <a name="attributes"></a>Атрибуты

|**Атрибут**|**Тип**|**Обязательный**|**Описание**|**Возможные значения**|
|:-----|:-----|:-----|:-----|:-----|
|Del  <br/> |xsd:boolean  <br/> |необязательный  <br/> |Указывает, была ли удалена строка, которая в противном случае была бы унаследована от мастер-фигуры.  <br/> |Значения типа xsd:boolean.  <br/> |
|IX  <br/> |xsd:unsignedInt  <br/> |необязательный  <br/> |Указывает идентификатор для строки на основе одного. Он должен быть unqiue и больше, чем другие идентификаторы в том же разделе. Атрибут IX используется только для разделов Character, Connection, Field, FillGradient, Geometry, Layer, LineGradient, Paragraph, Reviewer, Scratch и Tabs. Строка может иметь только один из атрибутов IX или N.  <br/> |Значения типа xsd:unsignedInt.  <br/> |
|LocalName  <br/> |xsd:string  <br/> |необязательный  <br/> |Указывает уникальное имя строки, зависящие от языка.  <br/> |Значения типа xsd:string.  <br/> |
|Нет  <br/> |xsd:string  <br/> |необязательный  <br/> |Указывает уникальное имя строки, независимое от языка. Атрибут N используется только для разделов User, Property, Actions, Control, Connection, Hyperlink и ActionTag. Строка может иметь только один из атрибутов IX или N.  <br/> |Значения типа xsd:string.  <br/> |
|T  <br/> |xsd:string  <br/> |необязательный  <br/> |Указывает тип геометрического пути, представленного строкой и используемого в визуализации геометрии. Атрибут T используется только для раздела Геометрия.  <br/> |Значения типа xsd:string.  <br/> |
   
## <a name="remarks"></a>Примечания

Атрибут **T** этого элемента **Row** должен быть одним из ограниченного набора значений, соответствующих строкам ShapeSheet. Обратитесь к приведенной ниже таблице, чтобы определить значения атрибута **T,** разрешенные для этого элемента **Row.** 
  
|**Значение**|**Описание**|**Дополнительные сведения**|
|:-----|:-----|:-----|
|ArcTo  <br/> |Содержит x- и y-координаты и нос круговой дуги.  <br/> |[ArcTo Row (Geometry Section)](arcto-row-geometry-section.md) <br/> |
|Ellipse  <br/> |Содержит x и y-координаты центральной точки эллипса и две точки на эллипсе.  <br/> |[Ellipse Row (Geometry Section)](ellipse-row-geometry-section.md) <br/> |
|EllipticalArcTo  <br/> |Содержит x и y-координаты конечной точки эллиптической дуги, x и y-координаты точек управления на дуге, угол от оси x до основной оси эллипса и соотношение между основными и небольшими осями эллипса.  <br/> |[EllipticalArcTo Row (Geometry Section)](ellipticalarcto-row-geometry-section.md) <br/> |
|InfiniteLine  <br/> |Содержит x и y-координаты двух точек на бесконечной строке.  <br/> |[InfiniteLine Row (Geometry Section)](infiniteline-row-geometry-section.md) |
|LineTo  <br/> |Содержит x-and y-координаты конечной вершины сегмента прямой линии.  <br/> |[LineTo Row (Geometry Section)](lineto-row-geometry-section.md) <br/> |
|MoveTo  <br/> |Содержит x и y-координаты первой вершины фигуры или представляет x- и y-координаты первого вершины после перерыва в пути.  <br/> |[MoveTo Row (Geometry Section)](moveto-row-geometry-section.md) <br/> |
|NURBSTo  <br/> |Содержит x- и y-координаты, положение второго до последнего узла, положение последнего веса, положение первого узла, положение первого веса и формулу для неинформированной рациональной B-spline (NURBS).  <br/> |[NURBSTo Row (Geometry Section)](nurbsto-row-geometry-section.md) <br/> |
|PolylineTo  <br/> |Содержит x и y-координаты последней точки полилиновой и полилиновой формулы.  <br/> |[PolylineTo Row (Geometry Section)](polylineto-row-geometry-section.md) <br/> |
|RelCubBezTo  <br/> |Содержит x и y-координаты конечной точки кривой кубического Bézier относительно ширины и высоты фигуры, x- и y-координаты точки управления в начале ширины и высоты кривой относительной формы, а также x- и y-координаты точки управления окончанием ширины и высоты кривой относительной формы.  <br/> |[RelCubBezTo Row (Geometry Section)](relcubbezto-row-geometry-section.md) <br/> |
|RelEllipticalArcTo  <br/> |Содержит x и y-координаты конечной точки эллиптической дуги по отношению к ширине и высоте фигуры, x- и y-координаты точек управления на дуге относительно ширины и высоты фигуры, угол от оси x до основной оси эллипса, а также соотношение между основными и небольшими осями эллипса.  <br/> |[RelEllipticalArcTo Row (Geometry Section)](relellipticalarcto-row-geometry-section.md) <br/> |
|RelLineTo  <br/> |Содержит x-и y-координаты конечной вершины сегмента прямой линии относительно ширины и высоты фигуры.  <br/> |[RelLineTo Row (Geometry Section)](rellineto-row-geometry-section.md) <br/> |
|RelMoveTo  <br/> |Содержит x- и y-координаты первой вершины формы или x- и y-координаты первого вершины после перерыва в пути, относительно высоты и ширины фигуры.  <br/> |[RelMoveTo Row (Geometry Section)](relmoveto-row-geometry-section.md) <br/> |
|RelQuadBezTo  <br/> |Содержит x и y-координаты конечной точки квадратной кривой Bézier по отношению к ширине и высоте фигуры, а также x- и y-координатам точки управления ширины и высоты кривой относительной формы.  <br/> |[RelQuadBezTo Row (Geometry Section)](relquadbezto-row-geometry-section.md) <br/> |
|SplineKnot  <br/> |Содержит x и y-координаты для точки управления spline и узла spline.  <br/> |[SplineKnot Row (Geometry Section)](splineknot-row-geometry-section.md) <br/> |
|SplineStart  <br/> |Содержит x и y-координаты для второй точки управления spline, ее второго узла, первого узла, последнего узла и степени spline.  <br/> |[SplineStart Row (Geometry Section)](splinestart-row-geometry-section.md) <br/> |
   

