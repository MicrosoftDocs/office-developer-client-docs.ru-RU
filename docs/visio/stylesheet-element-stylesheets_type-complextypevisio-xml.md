---
title: Элемент таблицы стилей (StyleSheets_Type complexType) ('Visio XML»)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 323e1ccd-8ddd-46d3-1032-5d68d01cf4bd
description: Представляет стиль, определенный в документе.
ms.openlocfilehash: 2513c7421dc8f890b7ba63f19cf3d31d23ce65ac
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19814971"
---
# <a name="stylesheet-element-stylesheetstype-complextype-visio-xml"></a>Элемент таблицы стилей (StyleSheets_Type complexType) ('Visio XML»)

Представляет стиль, определенный в документе.
  
## <a name="element-information"></a>Сведения об элементе

|||
|:-----|:-----|
|**Тип элемента** <br/> |[StyleSheet_Type](stylesheet_type-complextypevisio-xml.md) <br/> |
|**Пространство имен** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Файл схемы** <br/> |VisioSchema15.xsd  <br/> |
|**Части документа** <br/> |Document.XML  <br/> |
   
## <a name="definition"></a>Определение

```XML
< xs:element name="StyleSheet" Type="StyleSheet_Type" minOccurs="0" maxOccurs="unbounded" ></xs:element >
```

## <a name="elements-and-attributes"></a>Элементы и атрибуты

Если схема определяет специальные требования, такие как **последовательность**, **minOccurs**, **maxOccurs**и **выбора**, обратитесь к разделу определение. 
  
### <a name="parent-elements"></a>Родительские элементы

|**Элемент**|**Тип**|**Описание**|
|:-----|:-----|:-----|
|[Таблицы стилей](stylesheets-element-visiodocument_type-complextypevisio-xml.md) <br/> |[StyleSheets_Type](stylesheets_type-complextypevisio-xml.md) <br/> |Содержит коллекцию элементов **таблицы стилей** для документа.  <br/> |
   
### <a name="child-elements"></a>Дочерние элементы

|**Элемент**|**Тип**|**Описание**|
|:-----|:-----|:-----|
|[Cell](cell-elementvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Задает отдельное свойство.  <br/> |
|[Раздел](section-element-sheet_type-complextypevisio-xml.md) <br/> |[Section_Type](section_type-complextypevisio-xml.md) <br/> |Задает коллекцию свойств, связанных с ними.  <br/> |
   
### <a name="attributes"></a>Атрибуты

|**Атрибут**|**Тип**|**Обязательное**|**Описание**|**Возможные значения**|
|:-----|:-----|:-----|:-----|:-----|
|FillStyle  <br/> |XSD:unsignedInt  <br/> |необязательный  <br/> |Идентификатор элемента таблицы стилей, из которой этот стиль наследует форматирование заливки.  <br/> |Значения типа xsd:unsignedInt.  <br/> |
|ID  <br/> |XSD:unsignedInt  <br/> |Обязательный  <br/> |Уникальный идентификатор элемента в рамках родительского элемента.  <br/> |Значения типа xsd:unsignedInt.  <br/> |
|IsCustomName  <br/> |XSD:Boolean  <br/> |необязательный  <br/> |Указывает, настроен ли имя пользователя.  <br/> |Значения типа xsd:boolean.  <br/> |
|IsCustomNameU  <br/> |XSD:Boolean  <br/> |необязательный  <br/> |Указывает, настроен ли универсального имени пользователя.  <br/> |Значения типа xsd:boolean.  <br/> |
|Стиль линии  <br/> |XSD:unsignedInt  <br/> |необязательный  <br/> |Идентификатор элемента таблицы стилей, из которой этот стиль наследует форматирование линий.  <br/> |Значения типа xsd:unsignedInt.  <br/> |
|Имя  <br/> |XSD:String  <br/> |необязательный  <br/> |Имя элемента.  <br/> |Значения типа xsd:string.  <br/> |
|NameU  <br/> |XSD:String  <br/> |необязательный  <br/> |Универсальные имя элемента.  <br/> |Значения типа xsd:string.  <br/> |
|Стиля текста  <br/> |XSD:unsignedInt  <br/> |необязательный  <br/> |Идентификатор элемента таблицы стилей, из которой этот стиль наследует параметры форматирования текста.  <br/> |Значения типа xsd:unsignedInt.  <br/> |
   

