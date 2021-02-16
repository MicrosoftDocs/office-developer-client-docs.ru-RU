---
title: Элемент RefBy (Cell_Type complexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: ea2a63d3-d319-4420-1929-013dc832b308
description: Указывает ссылку на страницу в документе.
ms.openlocfilehash: cb47919a97b8ad42f62bcb1337cd8e6b3596f5ff
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/29/2019
ms.locfileid: "34538314"
---
# <a name="refby-element-cell_type-complextype-visio-xml"></a>Элемент RefBy (Cell_Type complexType) (Visio XML)

Указывает ссылку на страницу в документе.
  
## <a name="element-information"></a>Сведения об элементе

|||
|:-----|:-----|
|**Тип элемента** <br/> |[RefBy_Type](refby_type-complextypevisio-xml.md) <br/> |
|**Пространство имен** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Файл схемы** <br/> |VisioSchema15.xsd  <br/> |
|**Части документа** <br/> |document.xml, masters.xml, master#.xml, pages.xml, page#.xml  <br/> |
   
## <a name="definition"></a>Определение

```XML
< xs:element name="RefBy" type="RefBy_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a>Элементы и атрибуты

Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений. 
  
### <a name="parent-elements"></a>Родительские элементы

|**Элемент**|**Тип**|**Описание**|
|:-----|:-----|:-----|
|[Элемент Cell (Action Tag Section)](cell-element-action-tag-sectionvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Определяет одно свойство для тега действия на фигуре или странице.  <br/> |
|[Элемент Cell (строка Actions)](cell-element-actions-rowvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Указывает одно свойство действия, связанное с настраиваемой командой в меню ярлыка или тега действия.  <br/> |
|[Элемент Cell (строка ArcTo)](cell-element-arcto-rowvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Содержит координату x, координату y или лук цикловой дуги.  <br/> |
|[Элемент Cell (Character Section)](cell-element-character-sectionvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Указывает атрибут форматирования для текстового запуска фигуры, например шрифт, цвет, стиль, случай, положение относительно базового плана или размера точки.  <br/> |
|[Элемент Cell (строка Connection)](cell-element-connection-rowvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Содержит координаты X или Y, горизонтальные или вертикальные направления или тип для одной точки подключения фигуры.  <br/> |
|[Элемент Cell (строка Controls)](cell-element-controls-rowvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Содержит свойство для определенного работки управления, определенной для фигуры.  <br/> |
|[Элемент Cell (строка Ellipse)](cell-element-ellipse-rowvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Содержит координаты X или Y центральной точки эллипса и две точки эллипса.  <br/> |
|[Элемент Cell (строка EllipticalArcTo)](cell-element-ellipticalarcto-rowvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Содержит координаты X или Y конечной точки эллиптической дуги, координат x или Y контрольных точек на дуге, угол от оси X до основной оси эллипса или соотношение между основной и второстепенной осями эллипса.  <br/> |
|[Элемент Cell (Field Section)](cell-element-field-sectionvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Отображает функции и формулы, вставленные в текст фигуры, с помощью диалогового окна "Поле".  <br/> |
|[Элемент Cell (Fill Gradient Section)](cell-element-fill-gradient-sectionvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Содержит цвет, прозрачность и положение остановки градиента для градиента заливки.  <br/> |
|[Элемент Cell (Geometry Section)](cell-element-geometry-sectionvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Определяет свойства, которые определяют свойства форматирования и поведения по отношению к линиям и дугам, которые составляют раздел геометрии.  <br/> |
|[Элемент Cell (строка Hyperlink)](cell-element-hyperlink-rowvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Содержит сведения для одной гиперссылки, связанной с фигурой. Фигура будет содержать одну строку гиперссылки для каждой гиперссылки.  <br/> |
|[Элемент Cell (строка InfiniteLine)](cell-element-infiniteline-rowvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Содержит координаты X или Y двух точек на бесконечной линии.  <br/> |
|[Элемент Cell (Layer Section)](cell-element-layer-sectionvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Указывает одно свойство для уровня или его свойств для страницы.  <br/> |
|[Элемент Cell (Line Gradient Section)](cell-element-line-gradient-sectionvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Содержит цвет, прозрачность или положение остановки градиента для градиента линии.  <br/> |
|[Элемент Cell (строка LineTo)](cell-element-lineto-rowvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Содержит координаты X или Y конечной вершины сегмента прямой линии.  <br/> |
|[Элемент Cell (строка MoveTo)](cell-element-moveto-rowvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Содержит координаты X или Y первой вершины фигуры или представляет координаты X или Y первой вершины после разрыва пути.  <br/> |
|[Элемент Cell (строка NURBSTo)](cell-element-nurbsto-rowvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Содержит координаты x или y, положение второго до последнего сегвея, положение последнего веса, положение первого степеня, положение первого веса или формулу для несвязавного рационального B-spline (NURBS).  <br/> |
|[Элемент Cell (Paragraph Section)](cell-element-paragraph-sectionvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Указывает атрибут форматирования абзаца для текста фигуры, например отступы, интервалы строк, маркеры или горизонтальное выравнивание абзацев.  <br/> |
|[Элемент Cell (строка PolyLineTo)](cell-element-splineknot-rowvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Содержит координаты X или Y последней точки многолинейной или многолинейной формулы.  <br/> |
|[Элемент Cell (строка RelCubBezTo)](cell-element-relcubbezto-rowvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Содержит координаты X или Y конечной точки кривой Безье второго канала относительно ширины и высоты фигуры, координат x или Y контрольной точки начала ширины и высоты относительной фигуры кривой, а также координаты X или Y контрольной точки относительно ширины и высоты кривой.  <br/> |
|[Элемент Cell (строка RelEllipticalArcTo)](cell-element-relellipticalarcto-rowvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Содержит координаты X или Y конечной точки эллиптической дуги относительно ширины и высоты фигуры, координат x или Y контрольных точек на дуге относительно ширины и высоты фигуры, угла от оси x до основной оси эллипса или соотношения между основной и второстепенной осями эллипса.  <br/> |
|[Элемент Cell (строка RelLineTo)](cell-element-rellineto-rowvisio-xml.md)[Cell](cell-element-rellineto-rowvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Содержит координаты X или Y конечной вершины сегмента прямой линии относительно ширины и высоты фигуры.  <br/> |
|[Элемент Cell (строка RelMoveTo)](cell-element-relmoveto-rowvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Содержит координаты X или Y первой вершины фигуры или координаты X или Y первой вершины после разрыва пути относительно высоты и ширины фигуры.  <br/> |
|[Элемент Cell (Раздел RelQuadBezTo](cell-element-relquadbezto-rowvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Содержит координаты X или Y конечной точки кривой Безье 1 относительно ширины и высоты фигуры или координат x или y контрольной точки относительной ширины и высоты кривой.  <br/> |
|[Элемент Cell (Scratch Section)](cell-element-scratch-sectionvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Указывает область работы для ввода и тестирования формул, на которые могут ссылиться другие ячейки.  <br/> |
|[Элемент Cell (Shape Data Section](cell-element-shape-data-sectionvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Указывает одно свойство данных фигуры.  <br/> |
|[Элемент Cell (строка SplineKnot)](cell-element-splineknot-rowvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Содержит координаты X или Y для точки управления сплайна или загона сплайна.  <br/> |
|[Элемент Cell (Раздел SplineStart)](cell-element-splinestart-rowvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Содержит координаты x или y для второй контрольной точки сплайна, второй подмайки, первой степени, последней затеи или степени сплайна.  <br/> |
|[Элемент Cell (Раздел "Вкладки")](cell-element-tabs-sectionvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Указывает свойство, которое управляет положением остановки или выравниванием табули для фигуры и стиля.  <br/> |
|[Элемент Cell (User-defined Cells Section)](cell-element-user-defined-cells-sectionvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Одно свойство определенного пользователем фрагмента информации, на которое могут ссылаться другие ячейки и средства надстройки.  <br/> |
   
### <a name="child-elements"></a>Дочерние элементы

Нет.
  
### <a name="attributes"></a>Атрибуты

|**Атрибут**|**Тип**|**Обязательный**|**Описание**|**Возможные значения**|
|:-----|:-----|:-----|:-----|:-----|
|ID  <br/> |xsd:unsignedInt  <br/> |Обязательный  <br/> |Указывает ИД страницы в документе.  <br/> |Значения типа xsd:unsignedInt.  <br/> |
|T  <br/> |xsd:string  <br/> |Обязательный  <br/> |Указывает тип ссылки.  <br/> |Значения типа xsd:string.  <br/> |
   

