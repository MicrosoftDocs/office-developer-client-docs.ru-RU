---
title: Элемент ячейки (строка NURBSTo) ('Visio XML»)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: e76bae8f-b9de-39ef-1f56-b00a6cd2ba6c
description: Содержит положение x и y координат, второй — к последней число узлов, Позиция последнего вес положение первого число узлов положение первого вес или формулу для неоднородной rational-сплайн (NURBS).
ms.openlocfilehash: f23f73d67d72f9536dc7ffe9e083058ea9306217
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25392804"
---
# <a name="cell-element-nurbsto-row-visio-xml"></a>Элемент ячейки (строка NURBSTo) ('Visio XML»)

Содержит положение x и y координат, второй — к последней число узлов, Позиция последнего вес положение первого число узлов положение первого вес или формулу для неоднородной rational-сплайн (NURBS).
  
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
|[Элемент Row (Геометрия)](row-element-geometry-sectionvisio-xml.md) <br/> |[NURBSTo_Type](nurbsto_type-complextypevisio-xml.md) <br/> |Содержит положение x и y координат, второй — к последней число узлов, Позиция последнего вес положение первого число узлов положение первого вес или формулу для неоднородной rational-сплайн (NURBS).  <br/> |
   
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
|X   <br/> |X координата последней контрольной точки NURBS.  <br/> |[Строка NURBSTo (раздел "Геометрия")](nurbsto-row-geometry-section.md) <br/> |
|Да  <br/> |Последний контрольной точки NURBS по оси y.  <br/> |[Строка NURBSTo (раздел "Геометрия")](nurbsto-row-geometry-section.md) <br/> |
|A  <br/> |Второй — к последней узлов NURBS.  <br/> |[Строка NURBSTo (раздел "Геометрия")](nurbsto-row-geometry-section.md) <br/> |
|B  <br/> |Последний вес NURBS.  <br/> |[Строка NURBSTo (раздел "Геометрия")](nurbsto-row-geometry-section.md) <br/> |
|C  <br/> |Первый узел NURBS.  <br/> |[Строка NURBSTo (раздел "Геометрия")](nurbsto-row-geometry-section.md) <br/> |
|D  <br/> |Первый вес NURBS.  <br/> |[Строка NURBSTo (раздел "Геометрия")](nurbsto-row-geometry-section.md) <br/> |
|E  <br/> |Формула NURBS.  <br/> |[Строка NURBSTo (раздел "Геометрия")](nurbsto-row-geometry-section.md) <br/> |
   

