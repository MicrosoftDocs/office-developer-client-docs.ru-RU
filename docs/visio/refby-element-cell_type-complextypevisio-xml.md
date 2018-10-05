---
title: Элемент RefBy (Cell_Type complexType) ('Visio XML»)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: ea2a63d3-d319-4420-1929-013dc832b308
description: Задает ссылку на страницу в документе.
ms.openlocfilehash: 1731bd20a5ba4358c72370dfcdc6d8a6fc791e2f
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25385860"
---
# <a name="refby-element-celltype-complextype-visio-xml"></a>Элемент RefBy (Cell_Type complexType) ('Visio XML»)

Задает ссылку на страницу в документе.
  
## <a name="element-information"></a>Сведения об элементе

|||
|:-----|:-----|
|**Тип элемента** <br/> |[RefBy_Type](refby_type-complextypevisio-xml.md) <br/> |
|**Пространство имен** <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Файл схемы** <br/> |VisioSchema15.xsd  <br/> |
|**Части документа** <br/> |Document.XML, masters.xml, главные # .xml, pages.xml, страницы # .xml  <br/> |
   
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
|[Элемент Cell (раздел "Теги действий")](cell-element-action-tag-sectionvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Определяет одно свойство для тега действие на фигуры или страницы.  <br/> |
|[Элемент Cell (строка Actions)](cell-element-actions-rowvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Указывает одно свойство действие, связанное с пользовательской команды меню тега ярлык или действие.  <br/> |
|[Элемент Cell (строка ArcTo)](cell-element-arcto-rowvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Содержит x координата по оси y и галстук дугу.  <br/> |
|[Элемент Cell (раздел "Символ")](cell-element-character-sectionvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Указывает атрибут форматирования для выполнения текста фигуры, такие как шрифт, цвет, стиль, case, позиция относительно базового плана или размер текста.  <br/> |
|[Элемент Cell (строка Connection)](cell-element-connection-rowvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Содержит координаты x и y, горизонтальный или вертикальный направление или тип для одна точка подключения на фигуры.  <br/> |
|[Элемент Cell (строка Controls)](cell-element-controls-rowvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Содержит свойство для определенного элемента управления дескриптор, определенных для фигуры.  <br/> |
|[Элемент Cell (строка Ellipse)](cell-element-ellipse-rowvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Содержит x - или координаты y центральной точки и два аспекта на эллипс эллипса.  <br/> |
|[Элемент Cell (строка EllipticalArcTo)](cell-element-ellipticalarcto-rowvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Содержит или y координаты x руководство пользователя конечной точки или y координаты x элемента управления указывает на дуги, угол оси основные эллипса или отношение между эллипса основной и дополнительной осей.  <br/> |
|[Элемент Cell (раздел "Поле")](cell-element-field-sectionvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Отображает функций и формул вставлен в тексте фигуры с помощью диалогового окна поля.  <br/> |
|[Элемент Cell (раздел "Градиентная заливка")](cell-element-fill-gradient-sectionvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Содержит цвет, прозрачность и положение градиента для градиентной заливки.  <br/> |
|[Элемент Cell (раздел "Геометрия")](cell-element-geometry-sectionvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Определяет свойства, которые определяют свойства форматирования и поведения по отношению к линий и дуг, которые составляют раздел геометрии.  <br/> |
|[Элемент Cell (строка Hyperlink)](cell-element-hyperlink-rowvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Содержит данные об одной гиперссылки, связанной с фигурой. Фигура будет содержать одну строку гиперссылок для каждой гиперссылки.  <br/> |
|[Элемент Cell (строка InfiniteLine)](cell-element-infiniteline-rowvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Содержит x или y координаты двух точек на строку не ограничен.  <br/> |
|[Элемент Cell (раздел "Слои")](cell-element-layer-sectionvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Указывает одно свойство для слоя или его свойства для страницы.  <br/> |
|[Элемент Cell (раздел "Градиентная линия")](cell-element-line-gradient-sectionvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Содержит цвет, прозрачность или положение градиента для градиента строки.  <br/> |
|[Элемент Cell (строка LineTo)](cell-element-lineto-rowvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Содержит x- или y координаты окончания вершины прямой сегмент.  <br/> |
|[Элемент Cell (строка MoveTo)](cell-element-moveto-rowvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Содержит x и y координаты первой вершины фигуры или представляет x и y координаты первой вершины после приостановки пути.  <br/> |
|[Элемент Cell (строка NURBSTo)](cell-element-nurbsto-rowvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Содержит положение x и y координат, второй — к последней число узлов, Позиция последнего вес положение первого число узлов положение первого вес или формулу для неоднородной rational-сплайн (NURBS).  <br/> |
|[Элемент Cell (раздел "Абзац")](cell-element-paragraph-sectionvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Задает форматирование для текста фигуры, такие как отступы междустрочным интервалом, маркеры и выравнивание по горизонтали атрибут абзаца.  <br/> |
|[Элемент Cell (строка PolyLineTo)](cell-element-splineknot-rowvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Содержит x или y координаты точки ломаной или формулы ломаной.  <br/> |
|[Элемент Cell (строка RelCubBezTo)](cell-element-relcubbezto-rowvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Содержит x и y координаты конечной точки кубические Безье график относительно высоты и ширины фигуры, x и y координаты контрольной точки начала фигуры график относительно ширины и высоты или x и y координаты контрольной точки завершения фигуры график относительно ширины и высоты.  <br/> |
|[Элемент Cell (строка RelEllipticalArcTo)](cell-element-relellipticalarcto-rowvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Содержит или y координаты x конечной точки руководство пользователя относительно ширину и высоту фигуры, x и y координат элемента управления указывает на дугу относительно ширины и высоты, угол оси основные эллипса или отношение между фигуры основной и дополнительной осей эллипса.  <br/> |
|[Элемент ячейки (строка RelLineTo)](cell-element-rellineto-rowvisio-xml.md) [Ячейки](cell-element-rellineto-rowvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Содержит x- или y координаты окончания вершины отрезка прямой линии относительно ширины и высоты фигуры.  <br/> |
|[Элемент Cell (строка RelMoveTo)](cell-element-relmoveto-rowvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Содержит x и y координаты первой вершины фигуры или x и y координаты первой вершины после приостановки пути, относящиеся к высоту и ширину фигуры.  <br/> |
|[Элемент ячейки (RelQuadBezTo раздел](cell-element-relquadbezto-rowvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Содержит x или y координаты конечной точки кривая Безье относительно фигуры ширину и высоту или x и y координаты контрольной точки фигуры график относительно ширины и высоты.  <br/> |
|[Элемент Cell (раздел "Вспомогательный")](cell-element-scratch-sectionvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Задает рабочая область для ввода и проверки формул, которые могут использоваться в других ячеек.  <br/> |
|[Элемент ячейки (раздел данных, фигуры](cell-element-shape-data-sectionvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Указывает одно свойство данных фигуры.  <br/> |
|[Элемент Cell (строка SplineKnot)](cell-element-splineknot-rowvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Содержит x - или y координаты точки управления сплайн или число узлов сплайна.  <br/> |
|[Элемент ячейки (SplineStart раздел](cell-element-splinestart-rowvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Содержит x и y координат для второй контрольной точки сплайна, его второй число узлов, его первого число узлов, последний число узлов или степень сплайн.  <br/> |
|[Элемент Cell (раздел "Вкладки")](cell-element-tabs-sectionvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Указывает свойство, которое управляет фигуры и стиль позиции табуляции или выравнивание.  <br/> |
|[Элемент Cell (раздел "Пользовательские ячейки")](cell-element-user-defined-cells-sectionvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Одно свойство фрагмента определенные пользователем сведения, которые могут быть ссылается другие ячейки и надстройки.  <br/> |
   
### <a name="child-elements"></a>Дочерние элементы

Нет.
  
### <a name="attributes"></a>Атрибуты

|**Атрибут**|**Тип**|**Обязательный**|**Описание**|**Возможные значения**|
|:-----|:-----|:-----|:-----|:-----|
|ID  <br/> |XSD:unsignedInt  <br/> |Обязательный  <br/> |Задает идентификатор страницы в документе.  <br/> |Значения типа xsd:unsignedInt.  <br/> |
|T  <br/> |XSD:String  <br/> |Обязательный  <br/> |Указывает тип ссылки.  <br/> |Значения типа xsd:string.  <br/> |
   

