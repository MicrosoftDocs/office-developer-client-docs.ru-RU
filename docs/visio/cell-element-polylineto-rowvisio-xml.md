---
title: Элемент ячейки (строка PolyLineTo) ('Visio XML»)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: a62fbb51-e2a7-cdae-3516-5ce9ba30f26d
description: Содержит x или y координаты точки ломаной или формулы ломаной.
ms.openlocfilehash: 7a27cc5a4c2b6c9833263a28bbcadc40f08d8e70
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25398656"
---
# <a name="cell-element-polylineto-row-visio-xml"></a>Элемент ячейки (строка PolyLineTo) ('Visio XML»)

Содержит x или y координаты точки ломаной или формулы ломаной.
  
## <a name="element-information"></a>Сведения об элементе

|||
|:-----|:-----|
|**Тип элемента** <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |
|**Пространство имен** <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Файл схемы** <br/> |VisioSchema15.xsd  <br/> |
|**Части документа** <br/> |главные # .xml, страницы # .xml  <br/> |
   
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
|[Элемент Row (Геометрия)](row-element-geometry-sectionvisio-xml.md) <br/> |[PolylineTo_Type](polylineto_type-complextypevisio-xml.md) <br/> |Содержит x или y координаты точки ломаной или формулы ломаной.  <br/> |
   
### <a name="child-elements"></a>Дочерние элементы

|**Элемент**|**Тип**|**Описание**|
|:-----|:-----|:-----|
|[RefBy](refby-element-cell_type-complextypevisio-xml.md) <br/> |[RefBy_Type](refby_type-complextypevisio-xml.md) <br/> |Задает ссылку на странице документа.  <br/> |
   
### <a name="attributes"></a>Атрибуты

|**Атрибут**|**Тип**|**Обязательный**|**Описание**|**Возможные значения**|
|:-----|:-----|:-----|:-----|:-----|
|E  <br/> |XSD:String  <br/> |необязательный  <br/> |Указывает, что формулы оценивается как ошибка. Значение **E** является текущим значением (строка сообщения об ошибке); значение атрибута **V** — это последний допустимое значение.  <br/> |Строка сообщения об ошибке.  <br/> |
|F  <br/> |XSD:String  <br/> |необязательный  <br/> | Представляет элемент формулы. Этот атрибут может содержать один из следующих строк:  <br/>  (Некоторые формулы) Если формула существует локально  <br/>  `No Formula`Если формула локально удален или заблокирован  <br/>  `Inh`Если наследуется формулу.  <br/> |Формула.  <br/> |
|N  <br/> |XSD:String  <br/> |Обязательный  <br/> |Представляет имя ячейки таблицы свойств фигуры.  <br/> |Имя ячейки таблицы свойств фигуры.  <br/> В разделе замечания ниже.  <br/> |
|U  <br/> |XSD:String  <br/> |необязательный  <br/> |Представляет единицы измерения по умолчанию — это список Рассылки.  <br/> |Единицы ячейки.  <br/> |
|V  <br/> |XSD:String  <br/> |необязательный  <br/> |Представляет значение ячейки.  <br/> |Значение ячейки таблицы свойств фигуры.  <br/> |
   
## <a name="remarks"></a>Замечания

Атрибут **N** этого элемента **ячейки** должен быть один из ограниченный набор значений, которые соответствуют ячейки таблицы свойств фигуры. Обратитесь к таблице ниже для определения значений атрибутов **N** , разрешенных для этого элемента **ячейки** . 
  
|**Значение**|**Описание**|**Дополнительные сведения**|
|:-----|:-----|:-----|
|X   <br/> |X координата конца вершины ломаной.  <br/> |[Строка PolylineTo (раздел "Геометрия")](polylineto-row-geometry-section.md) <br/> |
|Да  <br/> |Конечный вершины ломаной по оси y.  <br/> |[Строка PolylineTo (раздел "Геометрия")](polylineto-row-geometry-section.md) <br/> |
|A  <br/> |Формула ломаной.  <br/> |[Строка PolylineTo (раздел "Геометрия")](polylineto-row-geometry-section.md) <br/> |
   

