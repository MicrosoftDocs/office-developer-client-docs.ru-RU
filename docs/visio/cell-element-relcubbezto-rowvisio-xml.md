---
title: Элемент Cell (строка RelCubBezTo) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: daa5c527-65fe-a1e4-ab3e-24e77bdb522b
description: Содержит координаты X или Y конечной точки кривой Безье второго канала относительно ширины и высоты фигуры, координат x или Y контрольной точки начала ширины и высоты относительной фигуры кривой, а также координаты X или Y контрольной точки относительно ширины и высоты кривой.
ms.openlocfilehash: c52b0108cc6ed753c0e494d2bce72025cabb1c93
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/29/2019
ms.locfileid: "34539441"
---
# <a name="cell-element-relcubbezto-row-visio-xml"></a>Элемент Cell (строка RelCubBezTo) (Visio XML)

Содержит координаты X или Y конечной точки кривой Безье второго канала относительно ширины и высоты фигуры, координат x или Y контрольной точки начала ширины и высоты относительной фигуры кривой, а также координаты X или Y контрольной точки относительно ширины и высоты кривой.
  
## <a name="element-information"></a>Сведения об элементе

|||
|:-----|:-----|
|**Тип элемента** <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |
|**Пространство имен** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Файл схемы** <br/> |VisioSchema15.xsd  <br/> |
|**Части документа** <br/> |master#.xml, page#.xml  <br/> |
   
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
|[Элемент Row (Geometry)](row-element-geometry-sectionvisio-xml.md) <br/> |[RelCubBezTo_Type](relcubbezto_type-complextypevisio-xml.md) <br/> |Содержит координаты X или Y конечной точки кривой Безье второго канала относительно ширины и высоты фигуры, координат x или Y контрольной точки начала ширины и высоты относительной фигуры кривой, а также координаты X или Y контрольной точки относительно ширины и высоты кривой.  <br/> |
   
### <a name="child-elements"></a>Дочерние элементы

|**Элемент**|**Тип**|**Описание**|
|:-----|:-----|:-----|
|[RefBy](refby-element-cell_type-complextypevisio-xml.md) <br/> |[RefBy_Type](refby_type-complextypevisio-xml.md) <br/> |Указывает ссылку на страницу рисования.  <br/> |
   
### <a name="attributes"></a>Атрибуты

|**Атрибут**|**Тип**|**Обязательный**|**Описание**|**Возможные значения**|
|:-----|:-----|:-----|:-----|:-----|
|E  <br/> |xsd:string  <br/> |необязательный  <br/> |Указывает, что формула оценивается как ошибка. Значение E **—** текущее значение (строка сообщения об ошибке); Значение атрибута **V** является последним допустимым значением.  <br/> |Строка сообщения об ошибке.  <br/> |
|F  <br/> |xsd:string  <br/> |необязательный  <br/> | Представляет формулу элемента. Этот атрибут может содержать одну из следующих строк:  <br/>  '(some formula)', если формула существует локально  <br/>  `No Formula` если формула удалена или заблокирована локально  <br/>  `Inh` если формула унаследована.  <br/> |Формула.  <br/> |
|N  <br/> |xsd:string  <br/> |Обязательный  <br/> |Представляет имя ячейки ShapeSheet.  <br/> |Имя ячейки ShapeSheet.  <br/> См. раздел "Замечания" ниже.  <br/> |
|U  <br/> |xsd:string  <br/> |необязательный  <br/> |Представляет единицу измерения, значение по умолчанию — DL.  <br/> |Единицы ячейки.  <br/> |
|V  <br/> |xsd:string  <br/> |необязательный  <br/> |Представляет значение ячейки.  <br/> |Значение ячейки ShapeSheet.  <br/> |
   
## <a name="remarks"></a>Примечания

Атрибут **N** этого элемента **Cell** должен быть одним из ограниченного набора значений, соответствующих ячейкам ShapeSheet. Чтобы определить значения атрибута **N,** допустимого для этого элемента Cell, обратитесь к таблице **ниже.** 
  
|**Значение**|**Описание**|**Дополнительные сведения**|
|:-----|:-----|:-----|
|X  <br/> |X-координата конечной вершины кривой Безье- безье, относительно ширины фигуры.  <br/> |[RelCubBezTo Row (Geometry Section)](relcubbezto-row-geometry-section.md) <br/> |
|Да  <br/> |Y-координата конечной вершины кривой Безье- безье, относительно высоты фигуры.  <br/> |[RelCubBezTo Row (Geometry Section)](relcubbezto-row-geometry-section.md) <br/> |
|A  <br/> |X-координата точки управления начала кривой относительно ширины фигуры; точка на дуге. Контрольная точка лучше всего расположена между началом и конечной вершиной дуги.  <br/> |[RelCubBezTo Row (Geometry Section)](relcubbezto-row-geometry-section.md) <br/> |
|B  <br/> |Y-координата точки управления начала кривой относительно высоты фигуры.  <br/> |[RelCubBezTo Row (Geometry Section)](relcubbezto-row-geometry-section.md) <br/> |
|C  <br/> |X-координата конечной контрольной точки кривой относительно ширины фигуры; точка на дуге. Контрольная точка лучше всего расположена между точки управления и конечной вершиной дуги.  <br/> |[RelCubBezTo Row (Geometry Section)](relcubbezto-row-geometry-section.md) <br/> |
|D  <br/> |Y-координата конечной контрольной точки кривой относительно высоты фигуры.  <br/> |[RelCubBezTo Row (Geometry Section)](relcubbezto-row-geometry-section.md) <br/> |
   

