---
title: Элемент Shape (Shapes_Type Type) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 8074bd07-430a-779e-ad1f-e7e3a1c748b1
description: Содержит элементы, определяющие фигуру в элементе Master, Page или group shape.
ms.openlocfilehash: aa7ffa539c9f82adc486bd0848dda66798bac165
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/29/2019
ms.locfileid: "34542074"
---
# <a name="shape-element-shapes_type-complextype-visio-xml"></a>Элемент Shape (Shapes_Type Type) (Visio XML)

Содержит элементы, определяющие фигуру в **элементе Master,** **Page** или group shape.
  
## <a name="element-information"></a>Сведения об элементе

|||
|:-----|:-----|
|**Тип элемента** <br/> |[ShapeSheet_Type](shapesheet_type-complextypevisio-xml.md) <br/> |
|**Пространство имен** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Файл схемы** <br/> |VisioSchema15.xsd  <br/> |
|**Части документов** <br/> |page#.xml, master#.xml  <br/> |
   
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
|[Фигуры](shapes-element-pagecontents_type-complextypevisio-xml.md) <br/> |[Shapes_Type](shapes_type-complextypevisio-xml.md) <br/> |Указывает коллекцию фигур.  <br/> |
|[Фигуры](shapes-element-pagecontents_type-complextypevisio-xml.md) <br/> |[Shapes_Type](shapes_type-complextypevisio-xml.md) <br/> |Указывает коллекцию фигур.  <br/> |
   
### <a name="child-elements"></a>Дочерние элементы

|**Элемент**|**Тип**|**Описание**|
|:-----|:-----|:-----|
|[Cell](cell-elementvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Указывает одно свойство.  <br/> |
|[Data1](data1-element-shapesheet_type-complextypevisio-xml.md) <br/> |[Data_Type](data_type-complextypevisio-xml.md) <br/> |Содержит произвольное значение строки, которое используется для получения дополнительных сведений о фигуре.  <br/> |
|[Data2](data2-element-shapesheet_type-complextypevisio-xml.md) <br/> |[Data_Type](data_type-complextypevisio-xml.md) <br/> |Содержит произвольное значение строки, которое используется для получения дополнительных сведений о фигуре.  <br/> |
|[Data3](data3-element-shapesheet_type-complextypevisio-xml.md) <br/> |[Data_Type](data_type-complextypevisio-xml.md) <br/> |Содержит произвольное значение строки, которое используется для получения дополнительных сведений о фигуре.  <br/> |
|[ForeignData](foreigndata-element-shapesheet_type-complextypevisio-xml.md) <br/> |[ForeignData_Type](foreigndata_type-complextypevisio-xml.md) <br/> |Содержит MIME (многоцелевые расширения интернет-почты), закодированные BLOB данных изображений, таких как Windows, bitmap или данные OLE.  <br/> |
|[Section](section-element-sheet_type-complextypevisio-xml.md) <br/> |[Section_Type](section_type-complextypevisio-xml.md) <br/> |Указывает коллекцию связанных свойств.  <br/> |
|[Фигуры](shapes-element-shapesheet_type-complextypevisio-xml.md) <br/> |[Shapes_Type](shapes_type-complextypevisio-xml.md) <br/> |Указывает коллекцию фигур.  <br/> |
|[Text](text-element-shapesheet_type-complextypevisio-xml.md) <br/> |[Text_Type](text_type-complextypevisio-xml.md) <br/> |Содержит текст фигуры.  <br/> |
   
### <a name="attributes"></a>Атрибуты

|**Атрибут**|**Тип**|**Обязательный**|**Описание**|**Возможные значения**|
|:-----|:-----|:-----|:-----|:-----|
|Del  <br/> |xsd:boolean  <br/> |необязательный  <br/> |Флаг, указывающий, удаляется ли элемент локально.  <br/> |Значения типа xsd:boolean.  <br/> |
|FillStyle  <br/> |xsd:unsignedInt  <br/> ||ID таблицы StyleSheet, от которой эта фигура наследует форматирование заполнения.  <br/> |Значения типа xsd:unsignedInt.  <br/> |
|ID  <br/> |xsd:unsignedInt  <br/> |Обязательный  <br/> |Уникальный ID элемента в родительском элементе.  <br/> |Значения типа xsd:unsignedInt.  <br/> |
|IsCustomName  <br/> |xsd:boolean  <br/> |необязательный  <br/> |Указывает, было ли имя настроено пользователем.  <br/> |Значения типа xsd:boolean.  <br/> |
|IsCustomNameU  <br/> |xsd:boolean  <br/> |необязательный  <br/> |Указывает, было ли универсальное имя настроено пользователем..  <br/> |Значения типа xsd:boolean.  <br/> |
|LineStyle  <br/> |xsd:unsignedInt  <br/> ||ID таблицы StyleSheet, от которой эта фигура наследует форматирование строк.  <br/> |Значения типа xsd:unsignedInt.  <br/> |
|Master  <br/> |xsd:unsignedInt  <br/> |необязательный  <br/> |ID элемента Master, от которого фигура наследует свои данные.  <br/> |Значения типа xsd:unsignedInt.  <br/> |
|MasterShape  <br/> |xsd:unsignedInt  <br/> |необязательный  <br/> |ID элемента Master, от которого фигура наследует свои данные.  <br/> |Значения типа xsd:unsignedInt.  <br/> |
|Имя  <br/> |xsd:string  <br/> |необязательный  <br/> |Имя элемента.  <br/> |Значения типа xsd:string.  <br/> |
|NameU  <br/> |xsd:string  <br/> |необязательный  <br/> |Универсальное имя элемента.  <br/> |Значения типа xsd:string.  <br/> |
|TextStyle  <br/> |xsd:unsignedInt  <br/> ||ID таблицы StyleSheet, из которой эта фигура наследует форматирование текста.  <br/> |Значения типа xsd:unsignedInt.  <br/> |
|Тип  <br/> |xsd:token  <br/> |необязательный  <br/> |Тип фигуры. Это может быть одно из следующих значений: Group, Shape, Guide или Foreign.  <br/> |Значения типа xsd:token.  <br/> |
|UniqueID  <br/> |xsd:string  <br/> |необязательный  <br/> |GuID (глобальный уникальный идентификатор), назначенное фигуре.  <br/> |Значения типа xsd:string.  <br/> |
   

