---
title: Элемент ячейки (заливки градиента раздел) ('Visio XML»)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: d085f83a-f77b-9bf9-07dc-4561b83e288c
description: Содержит цвет, прозрачность и положение градиента для градиентной заливки.
ms.openlocfilehash: c5366d1d3fcf5a4cd453bc62467353b940e89792
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19813334"
---
# <a name="cell-element-fill-gradient-section-visio-xml"></a>Элемент ячейки (заливки градиента раздел) ('Visio XML»)

Содержит цвет, прозрачность и положение градиента для градиентной заливки.
  
## <a name="element-information"></a>Сведения об элементе

|||
|:-----|:-----|
|**Тип элемента** <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |
|**Пространство имен** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Файл схемы** <br/> |VisioSchema15.xsd  <br/> |
|**Части документа** <br/> |Document.XML, главные # .xml, страницы # .xml  <br/> |
   
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
|[Элемент Row (раздел FillGradient)](row-element-fill-gradient-sectionvisio-xml.md) <br/> |[FillGradientRow_Type](fillgradientrow_type-complextypevisio-xml.md) <br/> |Содержит цвет, прозрачность и положение градиента для градиентной заливки.  <br/> |
   
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
|GradientStopColor  <br/> |Значение цвета градиента. Это значение может быть выражено как номер индекса цвета в палитре документа или с помощью функции **RGB**, **THEMEVAL**или **HSL** .  <br/> |[Строка Gradient Stop (раздел "Градиентная заливка")](gradient-stop-row-fill-gradient-section.md) <br/> |
|GradientStopColorTrans  <br/> |Объем прозрачность точку градиента цвета в процентном выражении.  <br/> |[Строка Gradient Stop (раздел "Градиентная заливка")](gradient-stop-row-fill-gradient-section.md) <br/> |
|GradientStopPosition  <br/> |Позиция градиента по направление градиента строки в процентном соотношении от точки origin градиента для внешнего края градиента.  <br/> |[Строка Gradient Stop (раздел "Градиентная заливка")](gradient-stop-row-fill-gradient-section.md) <br/> |
   

