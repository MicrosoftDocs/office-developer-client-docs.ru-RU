---
title: Элемент Cell (Field Section) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 1a51a5ca-6b68-d2d8-befb-2b1d9cda1b8e
description: Отображает функции и формулы, вставленные в текст фигуры с помощью диалогового окна Field.
ms.openlocfilehash: b3bae89d20a4defed591e95ce0155f70d806e6f2
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/29/2019
ms.locfileid: "34540058"
---
# <a name="cell-element-field-section-visio-xml"></a>Элемент Cell (Field Section) (Visio XML)

Отображает функции и формулы, вставленные в текст фигуры с помощью диалогового окна Field.
  
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
|[Элемент Row (Полевой раздел)](row-element-field-sectionvisio-xml.md) <br/> |[FieldRow_Type](fieldrow_type-complextypevisio-xml.md) <br/> |Отображает функции и формулы, вставленные в текст фигуры с помощью диалогового окна Field.  <br/> |
   
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
|Календарь  <br/> |Определяет календарь, используемый для текстового поля, когда тип данных — Дата.  <br/> |[Calendar Cell (Text Fields Section)](calendar-cell-text-fields-section.md) <br/> |
|Формат  <br/> |Указывает форматирование текстового поля, которое является строкой, номером, датой или временем, продолжительностью или валютой.  <br/> |[Format Cell (Text Fields Section)](format-cell-text-fields-section.md) <br/> |
|ObjectKind  <br/> |Указывает тип текстового поля.  <br/> |[ObjectKind Cell (Text Fields Section)](objectkind-cell-text-fields-section.md) <br/> |
|Тип  <br/> |Указывает тип данных для значения текстового поля.  <br/> |[Type Cell (Text Fields Section)](type-cell-text-fields-section.md) <br/> |
|UICat  <br/> |Определяет категорию вставленного поля. Эта ячейка используется диалогами формата Field и Data для определения сведений о поле и категориях.  <br/> |[UICategory Cell (Text Fields Section)](uicategory-cell-text-fields-section.md) <br/> |
|UICod  <br/> |Определяет код вставленного поля. Эта ячейка используется диалогами формата Field и Data для определения сведений о поле и категориях.  <br/> |[UICode Cell (Text Fields Section)](uicode-cell-text-fields-section.md) <br/> |
|UIFmt  <br/> |Определяет формат вставленного поля. Эта ячейка используется диалогами формата Field и Data для определения поля и  <br/> |[UIFormat Cell (Text Fields Section)](uiformat-cell-text-fields-section.md) <br/> |
|Значение  <br/> |Содержит функцию для поля.  <br/> |[Value Cell (Text Fields Section)](value-cell-text-fields-section.md) <br/> |
   

