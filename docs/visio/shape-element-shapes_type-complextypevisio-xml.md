---
title: Элемент Shape (Шапес_типе complexType) (' XML ' Visio ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 8074bd07-430a-779e-ad1f-e7e3a1c748b1
description: Содержит элементы, определяющие фигуру в главной, странице или элементе фигуры группы.
ms.openlocfilehash: 6308b8dd21c92f6ced9ea7f03ec8aa85773fa2bb
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32326574"
---
# <a name="shape-element-shapestype-complextype-visio-xml"></a>Элемент Shape (Шапес_типе complexType) (' XML ' Visio ')

Содержит элементы, определяющие фигуру в **главной**, **странице**или элементе фигуры группы.
  
## <a name="element-information"></a>Сведения об элементе

|||
|:-----|:-----|
|**Тип элемента** <br/> |[Шапешит_типе](shapesheet_type-complextypevisio-xml.md) <br/> |
|**Пространство имен** <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Файл схемы** <br/> |VisioSchema15. xsd  <br/> |
|**Части документа** <br/> |страница #. XML, Master #. XML  <br/> |
   
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
|[Shapes](shapes-element-pagecontents_type-complextypevisio-xml.md) <br/> |[Шапес_типе](shapes_type-complextypevisio-xml.md) <br/> |Задает коллекцию фигур.  <br/> |
|[Shapes](shapes-element-pagecontents_type-complextypevisio-xml.md) <br/> |[Шапес_типе](shapes_type-complextypevisio-xml.md) <br/> |Задает коллекцию фигур.  <br/> |
   
### <a name="child-elements"></a>Дочерние элементы

|**Элемент**|**Тип**|**Описание**|
|:-----|:-----|:-----|
|[Cell](cell-elementvisio-xml.md) <br/> |[Целл_типе](cell_type-complextypevisio-xml.md) <br/> |Задает одно свойство.  <br/> |
|[Data1](data1-element-shapesheet_type-complextypevisio-xml.md) <br/> |[Data_Type](data_type-complextypevisio-xml.md) <br/> |Содержит произвольное строковое значение, которое используется для предоставления дополнительных сведений о фигуре.  <br/> |
|[Data2](data2-element-shapesheet_type-complextypevisio-xml.md) <br/> |[Data_Type](data_type-complextypevisio-xml.md) <br/> |Содержит произвольное строковое значение, которое используется для предоставления дополнительных сведений о фигуре.  <br/> |
|[Data3](data3-element-shapesheet_type-complextypevisio-xml.md) <br/> |[Data_Type](data_type-complextypevisio-xml.md) <br/> |Содержит произвольное строковое значение, которое используется для предоставления дополнительных сведений о фигуре.  <br/> |
|[ForeignData](foreigndata-element-shapesheet_type-complextypevisio-xml.md) <br/> |[Фореигндата_типе](foreigndata_type-complextypevisio-xml.md) <br/> |Содержит зашифрованный большой ДВОИЧный объект MIME (многоцелевые поЧтовые расширения) для графических данных, таких как метафайл Windows, точечный рисунок или данные OLE.  <br/> |
|[Section](section-element-sheet_type-complextypevisio-xml.md) <br/> |[Сектион_типе](section_type-complextypevisio-xml.md) <br/> |Задает коллекцию связанных свойств.  <br/> |
|[Shapes](shapes-element-shapesheet_type-complextypevisio-xml.md) <br/> |[Шапес_типе](shapes_type-complextypevisio-xml.md) <br/> |Задает коллекцию фигур.  <br/> |
|[Text](text-element-shapesheet_type-complextypevisio-xml.md) <br/> |[Текст_типе](text_type-complextypevisio-xml.md) <br/> |Содержит текст фигуры.  <br/> |
   
### <a name="attributes"></a>Атрибуты

|**Атрибут**|**Тип**|**Обязательный**|**Описание**|**Возможные значения**|
|:-----|:-----|:-----|:-----|:-----|
|Del  <br/> |XSD: Boolean  <br/> |необязательный  <br/> |Флаг, указывающий на то, что элемент удален локально.  <br/> |Значения типа XSD: Boolean.  <br/> |
|FillStyle  <br/> |XSD: Унсигнединт  <br/> ||Идентификатор таблицы стилей, из которой эта фигура наследует форматирование заливки.  <br/> |Значения типа XSD: Унсигнединт.  <br/> |
|ИД  <br/> |XSD: Унсигнединт  <br/> |Обязательный  <br/> |Уникальный идентификатор элемента в родительском элементе.  <br/> |Значения типа XSD: Унсигнединт.  <br/> |
|Искустомнаме  <br/> |XSD: Boolean  <br/> |необязательный  <br/> |Указывает, настроено ли имя пользователем.  <br/> |Значения типа XSD: Boolean.  <br/> |
|Искустомнамеу  <br/> |XSD: Boolean  <br/> |необязательный  <br/> |Указывает, настроено ли универсальное имя пользователем..  <br/> |Значения типа XSD: Boolean.  <br/> |
|LineStyle  <br/> |XSD: Унсигнединт  <br/> ||Идентификатор таблицы стилей, из которой эта фигура наследует форматирование линий.  <br/> |Значения типа XSD: Унсигнединт.  <br/> |
|Master  <br/> |XSD: Унсигнединт  <br/> |необязательный  <br/> |Идентификатор элемента Master, из которого фигура наследует данные.  <br/> |Значения типа XSD: Унсигнединт.  <br/> |
|MasterShape  <br/> |XSD: Унсигнединт  <br/> |необязательный  <br/> |Идентификатор элемента Master, из которого фигура наследует данные.  <br/> |Значения типа XSD: Унсигнединт.  <br/> |
|Имя  <br/> |XSD: строка  <br/> |необязательный  <br/> |Имя элемента.  <br/> |Значения типа String: XSD.  <br/> |
|NameU  <br/> |XSD: строка  <br/> |необязательный  <br/> |Универсальное имя элемента.  <br/> |Значения типа String: XSD.  <br/> |
|TextStyle  <br/> |XSD: Унсигнединт  <br/> ||Идентификатор таблицы стилей, из которой эта фигура наследует форматирование текста.  <br/> |Значения типа XSD: Унсигнединт.  <br/> |
|Тип  <br/> |XSD: маркер  <br/> |необязательный  <br/> |Тип фигуры. Может принимать одно из следующих значений: Group, Shape, Guide или инородный.  <br/> |Значения типа маркера XSD:.  <br/> |
|UniqueID  <br/> |XSD: строка  <br/> |необязательный  <br/> |Идентификатор GUID (глобальный уникальный идентификатор), назначенный фигуре.  <br/> |Значения типа String: XSD.  <br/> |
   

