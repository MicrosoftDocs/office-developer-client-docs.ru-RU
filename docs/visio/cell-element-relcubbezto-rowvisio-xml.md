---
title: Элемент cell (RelCubBezTo Row) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: daa5c527-65fe-a1e4-ab3e-24e77bdb522b
description: Содержит x- или y-координаты конечной точки кривой кубического Bézier относительно ширины и высоты фигуры, x- или y-координаты точки управления в начале ширины и высоты относительной формы кривой или x-или y-координаты точки управления окончанием ширины и высоты кривой относительной формы.
ms.openlocfilehash: c52b0108cc6ed753c0e494d2bce72025cabb1c93
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/29/2019
ms.locfileid: "34539441"
---
# <a name="cell-element-relcubbezto-row-visio-xml"></a>Элемент cell (RelCubBezTo Row) (Visio XML)

Содержит x- или y-координаты конечной точки кривой кубического Bézier относительно ширины и высоты фигуры, x- или y-координаты точки управления в начале ширины и высоты относительной формы кривой или x-или y-координаты точки управления окончанием ширины и высоты кривой относительной формы.
  
## <a name="element-information"></a>Сведения об элементе

|||
|:-----|:-----|
|**Тип элемента** <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |
|**Пространство имен** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Файл схемы** <br/> |VisioSchema15.xsd  <br/> |
|**Части документов** <br/> |master#.xml, page#.xml  <br/> |
   
## <a name="definition"></a>Определение

```XML
< xs:element name="Cell" type="Cell_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a>Элементы и атрибуты

Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений. 
  
### <a name="parent-elements"></a>Родительские элементы

|**Элемент**|**Тип**|**Описание**|
|:-----|:-----|:-----|
|[Элемент Row (Геометрия)](row-element-geometry-sectionvisio-xml.md) <br/> |[RelCubBezTo_Type](relcubbezto_type-complextypevisio-xml.md) <br/> |Содержит x- или y-координаты конечной точки кривой кубического Bézier относительно ширины и высоты фигуры, x- или y-координаты точки управления в начале ширины и высоты относительной формы кривой или x-или y-координаты точки управления окончанием ширины и высоты кривой относительной формы.  <br/> |
   
### <a name="child-elements"></a>Дочерние элементы

|**Элемент**|**Тип**|**Описание**|
|:-----|:-----|:-----|
|[RefBy](refby-element-cell_type-complextypevisio-xml.md) <br/> |[RefBy_Type](refby_type-complextypevisio-xml.md) <br/> |Указывает ссылку на страницу рисования.  <br/> |
   
### <a name="attributes"></a>Атрибуты

|**Атрибут**|**Тип**|**Обязательный**|**Описание**|**Возможные значения**|
|:-----|:-----|:-----|:-----|:-----|
|E  <br/> |xsd:string  <br/> |необязательный  <br/> |Указывает, что формула оценивается как ошибка. Значение **E —** текущее значение (строка сообщения об ошибке); Значение атрибута **V** является последним допустимым значением.  <br/> |Строка сообщения об ошибке.  <br/> |
|F  <br/> |xsd:string  <br/> |необязательный  <br/> | Представляет формулу элемента. Этот атрибут может содержать одну из следующих строк:  <br/>  "(некоторые формулы)", если формула существует локально  <br/>  `No Formula` если формула локально удалена или заблокирована  <br/>  `Inh` если формула наследуется.  <br/> |Формула.  <br/> |
|Нет  <br/> |xsd:string  <br/> |Обязательный  <br/> |Представляет имя ячейки ShapeSheet.  <br/> |Имя ячейки ShapeSheet.  <br/> См. раздел Замечания ниже.  <br/> |
|U  <br/> |xsd:string  <br/> |необязательный  <br/> |Представляет единицу измерения, по умолчанию — DL.  <br/> |Единицы ячейки.  <br/> |
|V  <br/> |xsd:string  <br/> |необязательный  <br/> |Представляет значение ячейки.  <br/> |Значение ячейки ShapeSheet.  <br/> |
   
## <a name="remarks"></a>Примечания

Атрибут **N** этого элемента **Cell** должен быть одним из ограниченного набора значений, соответствующих ячейкам ShapeSheet. Обратитесь к приведенной ниже таблице, чтобы определить значения атрибута **N,** разрешенные для этого элемента **Cell.** 
  
|**Значение**|**Описание**|**Дополнительные сведения**|
|:-----|:-----|:-----|
|X  <br/> |X-координата конечной вершины кривой кубического Bézier относительно ширины фигуры.  <br/> |[RelCubBezTo Row (Geometry Section)](relcubbezto-row-geometry-section.md) <br/> |
|Да  <br/> |Y-координата конечной вершины кривой кубического Bézier относительно высоты фигуры.  <br/> |[RelCubBezTo Row (Geometry Section)](relcubbezto-row-geometry-section.md) <br/> |
|A  <br/> |X-координата точки начала управления кривой относительно ширины фигуры; точка на дуге. Точка управления лучше всего расположена между началом и окончанием вершин дуги.  <br/> |[RelCubBezTo Row (Geometry Section)](relcubbezto-row-geometry-section.md) <br/> |
|B  <br/> |Y-координата точки начала управления кривой относительно высоты фигуры.  <br/> |[RelCubBezTo Row (Geometry Section)](relcubbezto-row-geometry-section.md) <br/> |
|C  <br/> |X-координата конечной точки управления кривой относительно ширины фигуры; точка на дуге. Точка управления лучше всего расположена между точкой начала управления и конечной вершиной дуги.  <br/> |[RelCubBezTo Row (Geometry Section)](relcubbezto-row-geometry-section.md) <br/> |
|D  <br/> |Y-координата конечной точки управления кривой относительно высоты фигуры.  <br/> |[RelCubBezTo Row (Geometry Section)](relcubbezto-row-geometry-section.md) <br/> |
   

