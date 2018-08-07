---
title: Элемент ячейки (строка PolyLineTo) ('Visio XML»)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: a62fbb51-e2a7-cdae-3516-5ce9ba30f26d
description: Содержит x или y координаты точки ломаной или формулы ломаной.
ms.openlocfilehash: 485682b43db045893bfc968cfb0859cf8cb2ce2d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19813347"
---
# <a name="cell-element-polylineto-row-visio-xml"></a>Элемент ячейки (строка PolyLineTo) ('Visio XML»)

Содержит x или y координаты точки ломаной или формулы ломаной.
  
## <a name="element-information"></a>Сведения об элементе

|||
|:-----|:-----|
|**Тип элемента** <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |
|**Пространство имен** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Файл схемы** <br/> |VisioSchema15.xsd  <br/> |
|**Части документа** <br/> |главные # .xml, страницы # .xml  <br/> |
   
## <a name="definition"></a>Определение

```XML
< xs:element name="Cell" type="Cell_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a>Элементы и атрибуты

Если схема определяет специальные требования, такие как **последовательность**, **minOccurs**, **maxOccurs**и **выбора**, обратитесь к разделу определение. 
  
### <a name="parent-elements"></a>Родительские элементы

|**Элемент**|**Тип**|**Описание**|
|:-----|:-----|:-----|
|[Элемент Row (Геометрия)](row-element-geometry-sectionvisio-xml.md) <br/> |[PolylineTo_Type](polylineto_type-complextypevisio-xml.md) <br/> |Содержит x или y координаты точки ломаной или формулы ломаной.  <br/> |
   
### <a name="child-elements"></a>Дочерние элементы

|**Элемент**|**Тип**|**Описание**|
|:-----|:-----|:-----|
|[RefBy](refby-element-cell_type-complextypevisio-xml.md) <br/> |[RefBy_Type](refby_type-complextypevisio-xml.md) <br/> |Задает ссылку на странице документа.  <br/> |
   
### <a name="attributes"></a>Атрибуты

|**Атрибут**|**Тип**|**Обязательное**|**Описание**|**Возможные значения**|
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
   

