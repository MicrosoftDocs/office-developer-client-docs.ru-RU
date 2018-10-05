---
title: Элемент фигуры (Shapes_Type complexType) ('Visio XML»)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 8074bd07-430a-779e-ad1f-e7e3a1c748b1
description: Содержит элементы, определяющие фигуры в образец, страница или элемент группы фигур.
ms.openlocfilehash: 6308b8dd21c92f6ced9ea7f03ec8aa85773fa2bb
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25399685"
---
# <a name="shape-element-shapestype-complextype-visio-xml"></a>Элемент фигуры (Shapes_Type complexType) ('Visio XML»)

Содержит элементы, определяющие фигуры в **Образец**, **страница**или элемент группы фигур.
  
## <a name="element-information"></a>Сведения об элементе

|||
|:-----|:-----|
|**Тип элемента** <br/> |[ShapeSheet_Type](shapesheet_type-complextypevisio-xml.md) <br/> |
|**Пространство имен** <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Файл схемы** <br/> |VisioSchema15.xsd  <br/> |
|**Части документа** <br/> |страницы # .xml, главные # .xml  <br/> |
   
## <a name="definition"></a>Определение

```XML
< xs:element name="Shape" type="ShapeSheet_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a>Элементы и атрибуты

Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений. 
  
### <a name="parent-elements"></a>Родительские элементы

|**Элемент**|**Тип**|**Описание**|
|:-----|:-----|:-----|
|[Фигур](shapes-element-pagecontents_type-complextypevisio-xml.md) <br/> |[Shapes_Type](shapes_type-complextypevisio-xml.md) <br/> |Задает коллекцию фигур.  <br/> |
|[Фигур](shapes-element-pagecontents_type-complextypevisio-xml.md) <br/> |[Shapes_Type](shapes_type-complextypevisio-xml.md) <br/> |Задает коллекцию фигур.  <br/> |
   
### <a name="child-elements"></a>Дочерние элементы

|**Элемент**|**Тип**|**Описание**|
|:-----|:-----|:-----|
|[Cell](cell-elementvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Задает отдельное свойство.  <br/> |
|[Бд1](data1-element-shapesheet_type-complextypevisio-xml.md) <br/> |[Data_Type](data_type-complextypevisio-xml.md) <br/> |Содержит произвольное строковое значение, которое используется для предоставления дополнительной информации о фигуры.  <br/> |
|[Бд2](data2-element-shapesheet_type-complextypevisio-xml.md) <br/> |[Data_Type](data_type-complextypevisio-xml.md) <br/> |Содержит произвольное строковое значение, которое используется для предоставления дополнительной информации о фигуры.  <br/> |
|[Data3](data3-element-shapesheet_type-complextypevisio-xml.md) <br/> |[Data_Type](data_type-complextypevisio-xml.md) <br/> |Содержит произвольное строковое значение, которое используется для предоставления дополнительной информации о фигуры.  <br/> |
|[ForeignData](foreigndata-element-shapesheet_type-complextypevisio-xml.md) <br/> |[ForeignData_Type](foreigndata_type-complextypevisio-xml.md) <br/> |Содержит MIME (Multipurpose Internet Mail Extensions) закодированный большого двоичного ОБЪЕКТА данных изображения, например метафайла Windows, точечного рисунка или данных OLE.  <br/> |
|[Раздел](section-element-sheet_type-complextypevisio-xml.md) <br/> |[Section_Type](section_type-complextypevisio-xml.md) <br/> |Задает коллекцию свойств, связанных с ними.  <br/> |
|[Фигур](shapes-element-shapesheet_type-complextypevisio-xml.md) <br/> |[Shapes_Type](shapes_type-complextypevisio-xml.md) <br/> |Задает коллекцию фигур.  <br/> |
|[Text](text-element-shapesheet_type-complextypevisio-xml.md) <br/> |[Text_Type](text_type-complextypevisio-xml.md) <br/> |Содержит текст фигуры.  <br/> |
   
### <a name="attributes"></a>Атрибуты

|**Атрибут**|**Тип**|**Обязательный**|**Описание**|**Возможные значения**|
|:-----|:-----|:-----|:-----|:-----|
|DEL  <br/> |XSD:Boolean  <br/> |необязательный  <br/> |Флаг, указывающий, является ли элемент удаляется локально.  <br/> |Значения типа xsd:boolean.  <br/> |
|FillStyle  <br/> |XSD:unsignedInt  <br/> ||Идентификатор таблицы стилей, из которого эта фигура наследует форматирование заливки.  <br/> |Значения типа xsd:unsignedInt.  <br/> |
|ID  <br/> |XSD:unsignedInt  <br/> |Обязательный  <br/> |Уникальный идентификатор элемента в рамках родительского элемента.  <br/> |Значения типа xsd:unsignedInt.  <br/> |
|IsCustomName  <br/> |XSD:Boolean  <br/> |необязательный  <br/> |Указывает, настроен ли имя пользователя.  <br/> |Значения типа xsd:boolean.  <br/> |
|IsCustomNameU  <br/> |XSD:Boolean  <br/> |необязательный  <br/> |Указывает, настроен ли универсального имени пользователя.  <br/> |Значения типа xsd:boolean.  <br/> |
|Стиль линии  <br/> |XSD:unsignedInt  <br/> ||Идентификатор таблицы стилей, из которого эта фигура наследует форматирование линий.  <br/> |Значения типа xsd:unsignedInt.  <br/> |
|Master  <br/> |XSD:unsignedInt  <br/> |необязательный  <br/> |Идентификатор основной элемент, из которого фигуры наследует его данных.  <br/> |Значения типа xsd:unsignedInt.  <br/> |
|MasterShape  <br/> |XSD:unsignedInt  <br/> |необязательный  <br/> |Идентификатор основной элемент, из которого фигуры наследует его данных.  <br/> |Значения типа xsd:unsignedInt.  <br/> |
|Имя  <br/> |XSD:String  <br/> |необязательный  <br/> |Имя элемента.  <br/> |Значения типа xsd:string.  <br/> |
|NameU  <br/> |XSD:String  <br/> |необязательный  <br/> |Универсальные имя элемента.  <br/> |Значения типа xsd:string.  <br/> |
|Стиля текста  <br/> |XSD:unsignedInt  <br/> ||Идентификатор таблицы стилей, из которого эта фигура наследует форматирование текста.  <br/> |Значения типа xsd:unsignedInt.  <br/> |
|Тип  <br/> |XSD:Token  <br/> |необязательный  <br/> |Тип фигуры. Это может быть одно из следующих значений: группа, фигуры, руководство по или внешнего.  <br/> |Значения типа xsd:token.  <br/> |
|Уникальный идентификатор  <br/> |XSD:String  <br/> |необязательный  <br/> |Идентификатор GUID (глобальный уникальный идентификатор) назначается фигуры.  <br/> |Значения типа xsd:string.  <br/> |
   

