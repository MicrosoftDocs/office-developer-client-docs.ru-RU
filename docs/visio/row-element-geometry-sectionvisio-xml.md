---
title: Элемент Row (раздел "геометрия") (XML для Visio)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 2b273958-1997-7c63-4a61-d231f023a81f
description: Содержит строки, в которых перечислены координаты вершин для линий и дуг, составляющих фигуру.
ms.openlocfilehash: 6dbf18b749ed072645c4941922729010f74fc0ae
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/29/2019
ms.locfileid: "34540856"
---
# <a name="row-element-geometry-section-visio-xml"></a>Элемент Row (раздел "геометрия") (XML для Visio)

Содержит строки, в которых перечислены координаты вершин для линий и дуг, составляющих фигуру.
  
## <a name="element-information"></a>Сведения об элементе

|||
|:-----|:-----|
|**Тип элемента** <br/> |[GeometryRow_Type](geometry_type-complextypevisio-xml.md) <br/> |
|**Пространство имен** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Файл схемы** <br/> |VisioSchema15. xsd  <br/> |
|**Части документа** <br/> |Master #. XML, Page #. XML  <br/> |
   
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
|[Section](section-element-sheet_type-complextypevisio-xml.md) <br/> |[Section_Type](section_type-complextypevisio-xml.md) <br/> |Содержит строки, в которых перечислены координаты вершин для линий и дуг, составляющих фигуру.  <br/> |
   
### <a name="child-elements"></a>Дочерние элементы

> [!NOTE]
> Элемент Cell является единственным дочерним элементом этого элемента. В зависимости от атрибута "T" этого элемента, значение элементов ячеек различается. В приведенной ниже таблице текст парасетикал в имени элемента соответствует значению "T", к которому относится раздел. 
  
|**Элемент**|**Тип**|**Описание**|
|:-----|:-----|:-----|
|[Элемент Cell (строка ArcTo)](arcto-row-geometry-section.md) <br/> |[Cell_Type](https://msdn.microsoft.com/library/6f23bcc4-af93-4023-a380-3e78a228e166%28Office.15%29.aspx) <br/> |Содержит координаты x и y, а также арксинус круга.  <br/> |
|[Элемент Cell (строка Ellipse)](ellipse-row-geometry-section.md) <br/> |[Cell_Type](https://msdn.microsoft.com/library/6f23bcc4-af93-4023-a380-3e78a228e166%28Office.15%29.aspx) <br/> |Содержит координаты x и y центральной точки эллипса и две точки эллипса.  <br/> |
|[Элемент Cell (строка EllipticalArcTo)](ellipticalarcto-row-geometry-section.md) <br/> |[Cell_Type](https://msdn.microsoft.com/library/6f23bcc4-af93-4023-a380-3e78a228e166%28Office.15%29.aspx) <br/> |Содержит координаты x и y конечной точки эллиптической дуги, координаты x и y элемента управления, указывающие на дугу, угол от оси x до основной оси эллипса и соотношение между основными и дополнительными осями эллипса.  <br/> |
|[Элемент Cell (строка InfiniteLine)](infiniteline-row-geometry-section.md) <br/> |[Cell_Type](https://msdn.microsoft.com/library/6f23bcc4-af93-4023-a380-3e78a228e166%28Office.15%29.aspx) <br/> |Содержит координаты x и y по двум точкам в бесконечной линии.  <br/> |
|[Элемент Cell (строка LineTo)](lineto-row-geometry-section.md) <br/> |[Cell_Type](https://msdn.microsoft.com/library/6f23bcc4-af93-4023-a380-3e78a228e166%28Office.15%29.aspx) <br/> |Содержит координаты x и y конечной вершины сегмента прямой линии.  <br/> |
|[Элемент Cell (строка MoveTo)](moveto-row-geometry-section.md) <br/> |[Cell_Type](https://msdn.microsoft.com/library/6f23bcc4-af93-4023-a380-3e78a228e166%28Office.15%29.aspx) <br/> |Содержит координаты x и y первой вершины фигуры или представляет координаты x и y первой вершины после разрыва в контуре.  <br/> |
|[Элемент Cell (строка NURBSTo)](nurbsto-row-geometry-section.md) <br/> |[Cell_Type](https://msdn.microsoft.com/library/6f23bcc4-af93-4023-a380-3e78a228e166%28Office.15%29.aspx) <br/> |Содержит координаты x и y, положение секунды с последним весом, положение последнего веса, положение первого веса, положение первого Кнот, положение первого веса и формула для неоднородного рационального B-сплайна (NURBS).  <br/> |
|[Элемент Cell (строка PolyLineTo)](polylineto-row-geometry-section.md) <br/> |[Cell_Type](https://msdn.microsoft.com/library/6f23bcc4-af93-4023-a380-3e78a228e166%28Office.15%29.aspx) <br/> |Содержит координаты x и y последней точки ломаной линии и формулы ломаной линии.  <br/> |
|[Элемент Cell (строка RelCubBezTo)](relcubbezto-row-geometry-section.md) <br/> |[Cell_Type](https://msdn.microsoft.com/library/6f23bcc4-af93-4023-a380-3e78a228e166%28Office.15%29.aspx) <br/> |Содержит координаты x и y конечной точки кривой Безье третьего порядка относительно ширины и высоты фигуры, а также координаты x и y точки управления начала относительной ширины и высоты фигуры, а также координаты x и y конечной точки окончания ширины и высоты фигуры, заданной относительной и высотой.  <br/> |
|[Элемент Cell (строка RelQuadBezTo)](relquadbezto-row-geometry-section.md) <br/> |[Cell_Type](https://msdn.microsoft.com/library/6f23bcc4-af93-4023-a380-3e78a228e166%28Office.15%29.aspx) <br/> |Содержит координаты x и y конечной точки квадратичной кривой Безье относительно ширины и высоты фигуры, а также координат x и y контрольной точки кривой относительно ширины и высоты фигуры.  <br/> |
|[Элемент Cell (строка RelEllipticalArcTo)](relellipticalarcto-row-geometry-section.md) <br/> |[Cell_Type](https://msdn.microsoft.com/library/6f23bcc4-af93-4023-a380-3e78a228e166%28Office.15%29.aspx) <br/> |Содержит координаты x и y конечной точки эллиптической дуги относительно ширины и высоты фигуры, а также координат x и y элемента управления на дуги относительно ширины и высоты фигуры, угла от оси x до основной оси эллипса, а также соотношение между основными и дополнительными осями эллипса.  <br/> |
|[Элемент Cell (строка RelLineTo)](rellineto-row-geometry-section.md) <br/> |[Cell_Type](https://msdn.microsoft.com/library/6f23bcc4-af93-4023-a380-3e78a228e166%28Office.15%29.aspx) <br/> |Содержит координаты x и y конечной вершины сегмента прямой линии относительно ширины и высоты фигуры.  <br/> |
|[Элемент Cell (строка RelMoveTo)](relmoveto-row-geometry-section.md) <br/> |[Cell_Type](https://msdn.microsoft.com/library/6f23bcc4-af93-4023-a380-3e78a228e166%28Office.15%29.aspx) <br/> |Содержит координаты x и y первой вершины фигуры или координаты x и y первой вершины после разрыва в контуре, относительно высоты и ширины фигуры (относительно высоты и ширины).  <br/> |
|[Элемент Cell (строка RelQuadBezTo)](relquadbezto-row-geometry-section.md) <br/> |[Cell_Type](https://msdn.microsoft.com/library/6f23bcc4-af93-4023-a380-3e78a228e166%28Office.15%29.aspx) <br/> |Содержит координаты x и y конечной точки квадратичной кривой Безье относительно ширины и высоты фигуры, а также координат x и y контрольной точки кривой относительно ширины и высоты фигуры.  <br/> |
|[Элемент Cell (строка SplineKnot)](splineknot-row-geometry-section.md) <br/> |[Cell_Type](https://msdn.microsoft.com/library/6f23bcc4-af93-4023-a380-3e78a228e166%28Office.15%29.aspx) <br/> |Содержит координаты x и y для контрольной точки сплайна и кнотного сплайна.  <br/> |
|[Элемент Cell (строка SplineStart)](splinestart-row-geometry-section.md) <br/> |[Cell_Type](https://msdn.microsoft.com/library/6f23bcc4-af93-4023-a380-3e78a228e166%28Office.15%29.aspx) <br/> |Содержит координаты x и y для второй контрольной точки сплайна, второй Кнот, ее первый Кнот, последний кнот и степень сплайна.  <br/> |
   
### <a name="attributes"></a>Атрибуты

|**Атрибут**|**Тип**|**Обязательный**|**Описание**|**Возможные значения**|
|:-----|:-----|:-----|:-----|:-----|
|Del  <br/> |XSD: Boolean  <br/> |необязательный  <br/> |Указывает, удалена ли строка, которая в противном случае была бы унаследована от основной фигуры.  <br/> |Значения типа XSD: Boolean.  <br/> |
|IX  <br/> |XSD: Унсигнединт  <br/> |необязательный  <br/> |Задает отсчитываемый от единицы идентификатор строки. Он должен быть уникальное и превышать другие идентификаторы в одном разделе. Атрибут IX используется только для разделов "символ", "подключение", "Филлградиент", "геометрия", "область", "Линеградиент", "Абзац", "фрагмент" и "вкладки". Строка может иметь только один из атрибутов IX или N.  <br/> |Значения типа XSD: Унсигнединт.  <br/> |
|LocalName  <br/> |XSD: строка  <br/> |необязательный  <br/> |Задает уникальное зависящее от языка имя строки.  <br/> |Значения типа String: XSD.  <br/> |
|N  <br/> |XSD: строка  <br/> |необязательный  <br/> |Задает уникальное имя строки, не зависящее от языка. Атрибут N используется только для разделов "пользователь", "свойство", "действия", "элементы управления", "гиперссылка" и "Актионтаг". Строка может иметь только один из атрибутов IX или N.  <br/> |Значения типа String: XSD.  <br/> |
|Д  <br/> |XSD: строка  <br/> |необязательный  <br/> |Указывает тип геометрического пути, представленного строкой и используемый в визуализации геометрии. Атрибут T используется только для раздела Geometry.  <br/> |Значения типа String: XSD.  <br/> |
   
## <a name="remarks"></a>Примечания

Атрибут **T** элемента **Row** должен быть одним из ограниченных наборов значений, соответствующих строкам таблицы свойств фигуры. Используйте приведенную ниже таблицу, чтобы определить значения атрибута **T** , разрешенные для этого элемента **Row** . 
  
|**Значение**|**Описание**|**Дополнительные сведения**|
|:-----|:-----|:-----|
|ArcTo  <br/> |Содержит координаты x и y, а также арксинус круга.  <br/> |[ArcTo Row (Geometry Section)](arcto-row-geometry-section.md) <br/> |
|Ellipse  <br/> |Содержит координаты x и y центральной точки эллипса и две точки эллипса.  <br/> |[Ellipse Row (Geometry Section)](ellipse-row-geometry-section.md) <br/> |
|EllipticalArcTo  <br/> |Содержит координаты x и y конечной точки эллиптической дуги, координаты x и y элемента управления, указывающие на дугу, угол от оси x до основной оси эллипса и соотношение между основными и дополнительными осями эллипса.  <br/> |[EllipticalArcTo Row (Geometry Section)](ellipticalarcto-row-geometry-section.md) <br/> |
|InfiniteLine  <br/> |Содержит координаты x и y по двум точкам в бесконечной линии.  <br/> |[InfiniteLine Row (Geometry Section)](infiniteline-row-geometry-section.md) |
|LineTo  <br/> |Содержит координаты x и y конечной вершины сегмента прямой линии.  <br/> |[LineTo Row (Geometry Section)](lineto-row-geometry-section.md) <br/> |
|MoveTo  <br/> |Содержит координаты x и y первой вершины фигуры или представляет координаты x и y первой вершины после разрыва в контуре.  <br/> |[MoveTo Row (Geometry Section)](moveto-row-geometry-section.md) <br/> |
|NURBSTo  <br/> |Содержит координаты x и y, положение секунды с последним весом, положение последнего веса, положение первого веса, положение первого Кнот, положение первого веса и формула для неоднородного рационального B-сплайна (NURBS).  <br/> |[NURBSTo Row (Geometry Section)](nurbsto-row-geometry-section.md) <br/> |
|PolylineTo  <br/> |Содержит координаты x и y последней точки ломаной линии и формулы ломаной линии.  <br/> |[PolylineTo Row (Geometry Section)](polylineto-row-geometry-section.md) <br/> |
|RelCubBezTo  <br/> |Содержит координаты x и y конечной точки кривой Безье третьего порядка относительно ширины и высоты фигуры, а также координаты x и y точки управления начала относительной ширины и высоты фигуры, а также координаты x и y конечной точки окончания ширины и высоты фигуры, заданной относительной и высотой.  <br/> |[RelCubBezTo Row (Geometry Section)](relcubbezto-row-geometry-section.md) <br/> |
|RelEllipticalArcTo  <br/> |Содержит координаты x и y конечной точки эллиптической дуги относительно ширины и высоты фигуры, а также координат x и y элемента управления на дуги относительно ширины и высоты фигуры, угла от оси x до основной оси эллипса, а также соотношение между основными и дополнительными осями эллипса.  <br/> |[RelEllipticalArcTo Row (Geometry Section)](relellipticalarcto-row-geometry-section.md) <br/> |
|RelLineTo  <br/> |Содержит координаты x и y конечной вершины сегмента прямой линии относительно ширины и высоты фигуры.  <br/> |[RelLineTo Row (Geometry Section)](rellineto-row-geometry-section.md) <br/> |
|RelMoveTo  <br/> |Содержит координаты x и y первой вершины фигуры или координаты x и y первой вершины после разрыва в контуре, относительно высоты и ширины фигуры (относительно высоты и ширины).  <br/> |[RelMoveTo Row (Geometry Section)](relmoveto-row-geometry-section.md) <br/> |
|RelQuadBezTo  <br/> |Содержит координаты x и y конечной точки квадратичной кривой Безье относительно ширины и высоты фигуры, а также координат x и y контрольной точки кривой относительно ширины и высоты фигуры.  <br/> |[RelQuadBezTo Row (Geometry Section)](relquadbezto-row-geometry-section.md) <br/> |
|SplineKnot  <br/> |Содержит координаты x и y для контрольной точки сплайна и кнотного сплайна.  <br/> |[SplineKnot Row (Geometry Section)](splineknot-row-geometry-section.md) <br/> |
|SplineStart  <br/> |Содержит координаты x и y для второй контрольной точки сплайна, второй Кнот, ее первый Кнот, последний кнот и степень сплайна.  <br/> |[SplineStart Row (Geometry Section)](splinestart-row-geometry-section.md) <br/> |
   

