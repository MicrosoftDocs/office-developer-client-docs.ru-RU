---
title: Элемент Cell (строка EllipticalArcTo) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 3c0aa7a3-cc54-ffac-2c62-917b3d0a357e
description: Содержит координаты X или Y конечной точки эллиптической дуги, координат x или Y контрольных точек на дуге, угол от оси X до основной оси эллипса или соотношение между основной и второстепенной осями эллипса.
ms.openlocfilehash: 396575c069925fe472fa3df0543e29303881dad3
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/29/2019
ms.locfileid: "34539830"
---
# <a name="cell-element-ellipticalarcto-row-visio-xml"></a>Элемент Cell (строка EllipticalArcTo) (Visio XML)

Содержит координаты X или Y конечной точки эллиптической дуги, координат x или Y контрольных точек на дуге, угол от оси X до основной оси эллипса или соотношение между основной и второстепенной осями эллипса.
  
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
|[Элемент Row (Geometry)](row-element-geometry-sectionvisio-xml.md) <br/> |[EllipticalArcTo_Type](ellipticalarcto_type-complextypevisio-xml.md) <br/> |Содержит координаты X или Y конечной точки эллиптической дуги, координат x или Y контрольных точек на дуге, угол от оси X до основной оси эллипса или соотношение между основной и второстепенной осями эллипса.  <br/> |
   
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
|X  <br/> |X-координата конечной вершины на дуге.  <br/> |[EllipticalArcTo Row (Geometry Section)](ellipticalarcto-row-geometry-section.md) <br/> |
|Да  <br/> |Y-координата конечной вершины на дуге.  <br/> |[EllipticalArcTo Row (Geometry Section)](ellipticalarcto-row-geometry-section.md) <br/> |
|A  <br/> |X-координата контрольной точки дуги; точка на дуге. Контрольная точка лучше всего расположена примерно на середине между началом и конечной вершиной дуги. В противном случае дуга может увеличиваться до крайнего размера, чтобы пройти через контрольную точку с непредсказуемыми результатами.  <br/> |[EllipticalArcTo Row (Geometry Section)](ellipticalarcto-row-geometry-section.md) <br/> |
|B  <br/> |Y-координата контрольной точки дуги.  <br/> |[EllipticalArcTo Row (Geometry Section)](ellipticalarcto-row-geometry-section.md) <br/> |
|C  <br/> |Угол основной оси дуги относительно оси X родительской фигуры.  <br/> |[EllipticalArcTo Row (Geometry Section)](ellipticalarcto-row-geometry-section.md) <br/> |
|D  <br/> |Отношение основной оси дуги к ее второстепенной оси. Несмотря на обычное значение этих слов, "основная" ось не должна быть больше оси "minor", поэтому это соотношение не должно быть больше 1. Установка для этой ячейки значения, меньшего или равного 0 или больше 1000, может привести к непредсказуемым результатам.  <br/> |[EllipticalArcTo Row (Geometry Section)](ellipticalarcto-row-geometry-section.md) <br/> |
   

