---
title: Элемент RefBy (Целл_типе complexType) (XML для Visio)
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
# <a name="refby-element-celltype-complextype-visio-xml"></a>Элемент RefBy (Целл_типе complexType) (XML для Visio)

Указывает ссылку на страницу в документе.
  
## <a name="element-information"></a>Сведения об элементе

|||
|:-----|:-----|
|**Тип элемента** <br/> |[Рефби_типе](refby_type-complextypevisio-xml.md) <br/> |
|**Пространство имен** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Файл схемы** <br/> |VisioSchema15. xsd  <br/> |
|**Части документа** <br/> |Document. XML, Master. XML, Master #. XML, Pages. XML, Page #. XML  <br/> |
   
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
|[Элемент Cell (раздел "теги действий")](cell-element-action-tag-sectionvisio-xml.md) <br/> |[Целл_типе](cell_type-complextypevisio-xml.md) <br/> |Определяет одно свойство для тега действия на фигуре или странице.  <br/> |
|[Элемент Cell (строка Actions)](cell-element-actions-rowvisio-xml.md) <br/> |[Целл_типе](cell_type-complextypevisio-xml.md) <br/> |Задает одно свойство действия, связанного с настраиваемой командой, в контекстном меню или меню тегов действий.  <br/> |
|[Элемент Cell (строка ArcTo)](cell-element-arcto-rowvisio-xml.md) <br/> |[Целл_типе](cell_type-complextypevisio-xml.md) <br/> |Содержит координату x, координату по оси y или дугу круговой дуги.  <br/> |
|[Элемент Cell (раздел "символ")](cell-element-character-sectionvisio-xml.md) <br/> |[Целл_типе](cell_type-complextypevisio-xml.md) <br/> |Задает атрибут форматирования для текстового запуска фигуры, например шрифт, цвет, стиль, регистр, положение относительно базовой линии или кегля.  <br/> |
|[Элемент Cell (строка Connection)](cell-element-connection-rowvisio-xml.md) <br/> |[Целл_типе](cell_type-complextypevisio-xml.md) <br/> |Содержит координаты x или y, горизонтальное или вертикальное направление или тип для одной точки подключения на фигуре.  <br/> |
|[Элемент Cell (строка Controls)](cell-element-controls-rowvisio-xml.md) <br/> |[Целл_типе](cell_type-complextypevisio-xml.md) <br/> |Содержит свойство для определенного управляющего маркера, определенного для фигуры.  <br/> |
|[Элемент Cell (строка Ellipse)](cell-element-ellipse-rowvisio-xml.md) <br/> |[Целл_типе](cell_type-complextypevisio-xml.md) <br/> |Содержит координаты x и y центральной точки эллипса и две точки эллипса.  <br/> |
|[Элемент Cell (строка EllipticalArcTo)](cell-element-ellipticalarcto-rowvisio-xml.md) <br/> |[Целл_типе](cell_type-complextypevisio-xml.md) <br/> |Содержит координаты x или y конечной точки эллиптической дуги, x или y элемента управления, указывающих на дугу, угол от оси x до основной оси эллипса или соотношение между основными и дополнительными осями эллипса.  <br/> |
|[Элемент Cell (раздел "поле")](cell-element-field-sectionvisio-xml.md) <br/> |[Целл_типе](cell_type-complextypevisio-xml.md) <br/> |Отображает функции и формулы, вставленные в текст фигуры, с помощью диалогового окна "поле".  <br/> |
|[Элемент Cell (раздел "Градиентная заливка")](cell-element-fill-gradient-sectionvisio-xml.md) <br/> |[Целл_типе](cell_type-complextypevisio-xml.md) <br/> |Содержит цвет, прозрачность и положение остановки градиента для градиента заливки.  <br/> |
|[Элемент Cell (раздел "геометрия")](cell-element-geometry-sectionvisio-xml.md) <br/> |[Целл_типе](cell_type-complextypevisio-xml.md) <br/> |Определяет свойства, которые определяют свойства форматирования и поведения по отношению к линиям и дуг, которые составляют раздел "геометрия".  <br/> |
|[Элемент Cell (строка Hyperlink)](cell-element-hyperlink-rowvisio-xml.md) <br/> |[Целл_типе](cell_type-complextypevisio-xml.md) <br/> |Содержит сведения об одной гиперссылке, связанной с фигурой. Фигура будет содержать одну строку гиперссылок для каждой гиперссылки.  <br/> |
|[Элемент Cell (строка InfiniteLine)](cell-element-infiniteline-rowvisio-xml.md) <br/> |[Целл_типе](cell_type-complextypevisio-xml.md) <br/> |Содержит координаты x или y по двум точкам в бесконечной линии.  <br/> |
|[Элемент Cell (раздел "слой")](cell-element-layer-sectionvisio-xml.md) <br/> |[Целл_типе](cell_type-complextypevisio-xml.md) <br/> |Задает одно свойство для слоя или его свойств для страницы.  <br/> |
|[Элемент Cell (раздел "градиентная линия")](cell-element-line-gradient-sectionvisio-xml.md) <br/> |[Целл_типе](cell_type-complextypevisio-xml.md) <br/> |Содержит цвет, прозрачность или положение остановки градиента для линейного градиента.  <br/> |
|[Элемент Cell (строка LineTo)](cell-element-lineto-rowvisio-xml.md) <br/> |[Целл_типе](cell_type-complextypevisio-xml.md) <br/> |Содержит координаты x или y конечной вершины сегмента прямой линии.  <br/> |
|[Элемент Cell (строка MoveTo)](cell-element-moveto-rowvisio-xml.md) <br/> |[Целл_типе](cell_type-complextypevisio-xml.md) <br/> |Содержит координаты x или y первой вершины фигуры или представляет координату x или y первой вершины после разрыва в пути.  <br/> |
|[Элемент Cell (строка NURBSTo)](cell-element-nurbsto-rowvisio-xml.md) <br/> |[Целл_типе](cell_type-complextypevisio-xml.md) <br/> |Содержит координаты x или y, позицию второго и последнего веса, положение последнего веса, положение первого Кнот, положение первого веса или формулу для неоднородного рационального B-сплайна (NURBS).  <br/> |
|[Элемент Cell (раздел "Абзац")](cell-element-paragraph-sectionvisio-xml.md) <br/> |[Целл_типе](cell_type-complextypevisio-xml.md) <br/> |Задает атрибут форматирования абзаца для текста фигуры, например отступы, междустрочный интервал, маркеры или горизонтальное выравнивание абзацев.  <br/> |
|[Элемент Cell (строка PolyLineTo)](cell-element-splineknot-rowvisio-xml.md) <br/> |[Целл_типе](cell_type-complextypevisio-xml.md) <br/> |Содержит координаты x или y последней точки ломаной линии или формулы ломаной линии.  <br/> |
|[Элемент Cell (строка RelCubBezTo)](cell-element-relcubbezto-rowvisio-xml.md) <br/> |[Целл_типе](cell_type-complextypevisio-xml.md) <br/> |Содержит координаты x или y конечной точки кривой Безье третьего порядка относительно ширины и высоты фигуры, а также координаты x или y точки управления начала относительной ширины и высоты фигуры, а также координаты x или y контрольной точки (x). конец значения ширины и высоты фигуры относительной кривой.  <br/> |
|[Элемент Cell (строка RelEllipticalArcTo)](cell-element-relellipticalarcto-rowvisio-xml.md) <br/> |[Целл_типе](cell_type-complextypevisio-xml.md) <br/> |Содержит координаты x или y конечной точки эллиптической дуги относительно ширины и высоты фигуры, а также координат x или y элемента управления на дуги относительно ширины и высоты фигуры, угла от оси x до основной оси эллипса или соотношения между Основные и дополнительные оси эллипса.  <br/> |
|[Элемент Cell (строка строка rellineto)](cell-element-rellineto-rowvisio-xml.md) [Cell](cell-element-rellineto-rowvisio-xml.md) (ячейка) <br/> |[Целл_типе](cell_type-complextypevisio-xml.md) <br/> |Содержит координаты x или y конечной вершины сегмента прямой линии относительно ширины и высоты фигуры.  <br/> |
|[Элемент Cell (строка RelMoveTo)](cell-element-relmoveto-rowvisio-xml.md) <br/> |[Целл_типе](cell_type-complextypevisio-xml.md) <br/> |Содержит координаты x или y первой вершины фигуры, а также координаты x или y первой вершины после разрыва в контуре относительно высоты и ширины фигуры.  <br/> |
|[Элемент Cell (раздел строка relquadbezto](cell-element-relquadbezto-rowvisio-xml.md) <br/> |[Целл_типе](cell_type-complextypevisio-xml.md) <br/> |Содержит координаты x или y конечной точки квадратичной кривой Безье относительно ширины и высоты фигуры, а также координат x или y контрольной точки кривой относительно ширины и высоты фигуры.  <br/> |
|[Элемент Cell (раздел "вспомогательный")](cell-element-scratch-sectionvisio-xml.md) <br/> |[Целл_типе](cell_type-complextypevisio-xml.md) <br/> |Задает рабочую область для ввода и тестирования формул, на которые можно ссылаться по другим ячейкам.  <br/> |
|[Элемент Cell (раздел "данные фигуры"](cell-element-shape-data-sectionvisio-xml.md) <br/> |[Целл_типе](cell_type-complextypevisio-xml.md) <br/> |Задает одно свойство данных фигуры.  <br/> |
|[Элемент Cell (строка SplineKnot)](cell-element-splineknot-rowvisio-xml.md) <br/> |[Целл_типе](cell_type-complextypevisio-xml.md) <br/> |Содержит координаты x или y для контрольной точки сплайна или кнотного сплайна.  <br/> |
|[Элемент Cell (раздел строка splinestart](cell-element-splinestart-rowvisio-xml.md) <br/> |[Целл_типе](cell_type-complextypevisio-xml.md) <br/> |Содержит координаты x или y для второй контрольной точки сплайна, второй Кнот, ее первый Кнот, последний кнот или степень сплайна.  <br/> |
|[Элемент Cell (раздел "вкладки")](cell-element-tabs-sectionvisio-xml.md) <br/> |[Целл_типе](cell_type-complextypevisio-xml.md) <br/> |Задает свойство, которое управляет положением позиции табуляции и ее выравниванием.  <br/> |
|[Элемент Cell (раздел "пользовательские ячейки")](cell-element-user-defined-cells-sectionvisio-xml.md) <br/> |[Целл_типе](cell_type-complextypevisio-xml.md) <br/> |Одно свойство указанного пользователем набора данных, на которые можно ссылаться по другим ячейкам и средствам надстроек.  <br/> |
   
### <a name="child-elements"></a>Дочерние элементы

Нет.
  
### <a name="attributes"></a>Атрибуты

|**Атрибут**|**Тип**|**Обязательный**|**Описание**|**Возможные значения**|
|:-----|:-----|:-----|:-----|:-----|
|ID  <br/> |XSD: Унсигнединт  <br/> |Обязательный  <br/> |Задает идентификатор страницы в документе.  <br/> |Значения типа XSD: Унсигнединт.  <br/> |
|Д  <br/> |XSD: строка  <br/> |Обязательный  <br/> |Указывает тип ссылки.  <br/> |Значения типа String: XSD.  <br/> |
   

