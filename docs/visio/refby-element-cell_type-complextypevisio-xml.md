---
title: Элемент RefBy (Cell_Type complexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: ea2a63d3-d319-4420-1929-013dc832b308
description: Указывает ссылку на страницу в рисунке.
ms.openlocfilehash: cb47919a97b8ad42f62bcb1337cd8e6b3596f5ff
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/29/2019
ms.locfileid: "34538314"
---
# <a name="refby-element-cell_type-complextype-visio-xml"></a>Элемент RefBy (Cell_Type complexType) (Visio XML)

Указывает ссылку на страницу в рисунке.
  
## <a name="element-information"></a>Сведения об элементе

|||
|:-----|:-----|
|**Тип элемента** <br/> |[RefBy_Type](refby_type-complextypevisio-xml.md) <br/> |
|**Пространство имен** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Файл схемы** <br/> |VisioSchema15.xsd  <br/> |
|**Части документов** <br/> |document.xml, masters.xml, master#.xml, pages.xml, page#.xml  <br/> |
   
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
|[Элемент Cell (Раздел Тег действия)](cell-element-action-tag-sectionvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Определяет одно свойство для тега действий на форме или странице.  <br/> |
|[Элемент Cell (строка Actions)](cell-element-actions-rowvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Указывает одно свойство действия, связанного с настраиваемой командой в меню ярлыка или тега действий.  <br/> |
|[Элемент Cell (строка ArcTo)](cell-element-arcto-rowvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Содержит координаты x, координаты y или лук круговой дуги.  <br/> |
|[Элемент Cell (Раздел символов)](cell-element-character-sectionvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Указывает атрибут форматирования для текстового запуска фигуры, например шрифта, цвета, стиля, дела, позиции по отношению к базовому или размеру точки.  <br/> |
|[Элемент Cell (строка Connection)](cell-element-connection-rowvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Содержит x- или y-координаты, горизонтальное или вертикальное направление или введите для одной точки подключения на фигуре.  <br/> |
|[Элемент Cell (строка Controls)](cell-element-controls-rowvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Содержит свойство для определенной ручки управления, определенной для фигуры.  <br/> |
|[Элемент Cell (строка Ellipse)](cell-element-ellipse-rowvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Содержит x или y-координаты центральной точки эллипса и две точки на эллипсе.  <br/> |
|[Элемент Cell (строка EllipticalArcTo)](cell-element-ellipticalarcto-rowvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Содержит x- или y-координаты конечной точки эллиптической дуги, x или y-координаты точек управления на дуге, угол от оси x до основной оси эллипса или соотношение между основными и небольшими осями эллипса.  <br/> |
|[Элемент Cell (Полевой раздел)](cell-element-field-sectionvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Отображает функции и формулы, вставленные в текст фигуры с помощью диалогового окна Field.  <br/> |
|[Элемент Cell (Раздел Заполнения Градиента)](cell-element-fill-gradient-sectionvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Содержит цвет, прозрачность и расположение остановки градиента для градиента заполнения.  <br/> |
|[Элемент Cell (Раздел Геометрия)](cell-element-geometry-sectionvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Определяет свойства, определяющих форматирование и поведенческие свойства в отношении линий и дуг, которые составляют раздел Геометрия.  <br/> |
|[Элемент Cell (строка Hyperlink)](cell-element-hyperlink-rowvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Содержит сведения для одной гиперссылки, связанной с фигурой. Фигура будет содержать одну строку гиперссылки для каждой гиперссылки.  <br/> |
|[Элемент Cell (строка InfiniteLine)](cell-element-infiniteline-rowvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Содержит x или y-координаты двух точек на бесконечной строке.  <br/> |
|[Элемент Cell (Раздел Layer)](cell-element-layer-sectionvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Указывает одно свойство для слоя или его свойств для страницы.  <br/> |
|[Элемент Cell (раздел Line Gradient)](cell-element-line-gradient-sectionvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Содержит цвет, прозрачность или положение остановки градиента для градиента строки.  <br/> |
|[Элемент Cell (строка LineTo)](cell-element-lineto-rowvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Содержит x-или y-координаты конечной вершины сегмента прямой линии.  <br/> |
|[Элемент Cell (строка MoveTo)](cell-element-moveto-rowvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Содержит x или y-координаты первой вершины фигуры или представляет x- или y-координаты первой вершины после разрыва пути.  <br/> |
|[Элемент Cell (строка NURBSTo)](cell-element-nurbsto-rowvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Содержит x- или y-координаты, положение второго до последнего узла, положение последнего веса, положение первого узла, положение первого веса или формулу для неинформированной рациональной B-spline (NURBS).  <br/> |
|[Элемент Cell (Раздел Абзац)](cell-element-paragraph-sectionvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Указывает атрибут форматирования абзаца для текста фигуры, например вмятины, интервалы строк, пули или горизонтальное выравнивание абзацев.  <br/> |
|[Элемент Cell (строка PolyLineTo)](cell-element-splineknot-rowvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Содержит x или y-координаты последней точки полилиновой или полилиновой формулы.  <br/> |
|[Элемент Cell (строка RelCubBezTo)](cell-element-relcubbezto-rowvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Содержит x- или y-координаты конечной точки кривой кубического Bézier относительно ширины и высоты фигуры, x- или y-координаты точки управления в начале ширины и высоты относительной формы кривой или x-или y-координаты точки управления окончанием ширины и высоты кривой относительной формы.  <br/> |
|[Элемент Cell (строка RelEllipticalArcTo)](cell-element-relellipticalarcto-rowvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Содержит x- или y-координаты конечной точки эллиптической дуги относительно ширины и высоты фигуры, x- или y-координат пунктов управления на дуге относительно ширины и высоты фигуры, угла от оси x до основной оси эллипса или соотношения между основными и небольшими осями эллипса.  <br/> |
|[Элемент Cell (RelLineTo Row)](cell-element-rellineto-rowvisio-xml.md)[Cell](cell-element-rellineto-rowvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Содержит x-или y-координаты конечной вершины сегмента прямой линии относительно ширины и высоты фигуры.  <br/> |
|[Элемент Cell (строка RelMoveTo)](cell-element-relmoveto-rowvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Содержит x- или y-координаты первой вершины фигуры или x- или y-координаты первой вершины после перерыва в пути, относительно высоты и ширины фигуры.  <br/> |
|[Элемент Cell (Раздел RelQuadBezTo](cell-element-relquadbezto-rowvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Содержит x или y-координаты конечной точки квадратной кривой Bézier по отношению к ширине и высоте фигуры или x- или y-координатам точки управления ширины и высоты кривой относительной формы.  <br/> |
|[Элемент Cell (Scratch Section)](cell-element-scratch-sectionvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Указывает область работы для ввода и тестирования формул, на которые могут ссылаться другие ячейки.  <br/> |
|[Элемент Cell (Раздел Фигура данных](cell-element-shape-data-sectionvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Указывает одно свойство данных фигуры.  <br/> |
|[Элемент Cell (строка SplineKnot)](cell-element-splineknot-rowvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Содержит x или y-координаты для точки управления spline или узла spline.  <br/> |
|[Элемент Cell (Раздел SplineStart](cell-element-splinestart-rowvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Содержит x- или y-координаты для второй точки управления spline, ее второго узла, первого узла, последнего узла или степени spline.  <br/> |
|[Элемент Cell (Раздел Вкладок)](cell-element-tabs-sectionvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Указывает свойство, которое управляет положением остановки или выравниванием стоп-вкладок формы и стиля.  <br/> |
|[Элемент Cell (Раздел ячейки, определяемой пользователем)](cell-element-user-defined-cells-sectionvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Одно свойство указанного пользователем фрагмента информации, на которое можно ссылаться другими ячейками и средствами надстройки.  <br/> |
   
### <a name="child-elements"></a>Дочерние элементы

Нет.
  
### <a name="attributes"></a>Атрибуты

|**Атрибут**|**Тип**|**Обязательный**|**Описание**|**Возможные значения**|
|:-----|:-----|:-----|:-----|:-----|
|ID  <br/> |xsd:unsignedInt  <br/> |Обязательный  <br/> |Указывает ID страницы в рисунке.  <br/> |Значения типа xsd:unsignedInt.  <br/> |
|T  <br/> |xsd:string  <br/> |Обязательный  <br/> |Указывает тип ссылки.  <br/> |Значения типа xsd:string.  <br/> |
   

