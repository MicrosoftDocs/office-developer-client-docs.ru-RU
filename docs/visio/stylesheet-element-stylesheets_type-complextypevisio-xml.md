---
title: Элемент StyleSheet (StyleSheets_Type complexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 323e1ccd-8ddd-46d3-1032-5d68d01cf4bd
description: Представляет стиль, определенный в документе.
ms.openlocfilehash: 939180d24972ae68d01b2a707e7806380b706d14
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/29/2019
ms.locfileid: "34541941"
---
# <a name="stylesheet-element-stylesheets_type-complextype-visio-xml"></a>Элемент StyleSheet (StyleSheets_Type complexType) (Visio XML)

Представляет стиль, определенный в документе.
  
## <a name="element-information"></a>Сведения об элементе

|||
|:-----|:-----|
|**Тип элемента** <br/> |[StyleSheet_Type](stylesheet_type-complextypevisio-xml.md) <br/> |
|**Пространство имен** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Файл схемы** <br/> |VisioSchema15.xsd  <br/> |
|**Части документа** <br/> |document.xml  <br/> |
   
## <a name="definition"></a>Определение

```XML
< xs:element name="StyleSheet" Type="StyleSheet_Type" minOccurs="0" maxOccurs="unbounded" ></xs:element >
```

## <a name="elements-and-attributes"></a>Элементы и атрибуты

Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений. 
  
### <a name="parent-elements"></a>Родительские элементы

|**Элемент**|**Тип**|**Описание**|
|:-----|:-----|:-----|
|[StyleSheets](stylesheets-element-visiodocument_type-complextypevisio-xml.md) <br/> |[StyleSheets_Type](stylesheets_type-complextypevisio-xml.md) <br/> |Содержит коллекцию **элементов StyleSheet** для документа.  <br/> |
   
### <a name="child-elements"></a>Дочерние элементы

|**Элемент**|**Тип**|**Описание**|
|:-----|:-----|:-----|
|[Cell](cell-elementvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Указывает одно свойство.  <br/> |
|[Section](section-element-sheet_type-complextypevisio-xml.md) <br/> |[Section_Type](section_type-complextypevisio-xml.md) <br/> |Указывает коллекцию связанных свойств.  <br/> |
   
### <a name="attributes"></a>Атрибуты

|**Атрибут**|**Тип**|**Обязательный**|**Описание**|**Возможные значения**|
|:-----|:-----|:-----|:-----|:-----|
|FillStyle  <br/> |xsd:unsignedInt  <br/> |необязательный  <br/> |ИД элемента StyleSheet, от которого этот стиль наследует форматирование заливки.  <br/> |Значения типа xsd:unsignedInt.  <br/> |
|ID  <br/> |xsd:unsignedInt  <br/> |Обязательный  <br/> |Уникальный ИД элемента в родительском элементе.  <br/> |Значения типа xsd:unsignedInt.  <br/> |
|IsCustomName  <br/> |xsd:boolean  <br/> |необязательный  <br/> |Указывает, было ли имя настроено пользователем.  <br/> |Значения типа xsd:boolean.  <br/> |
|IsCustomNameU  <br/> |xsd:boolean  <br/> |необязательный  <br/> |Указывает, настроено ли пользователем универсальное имя.  <br/> |Значения типа xsd:boolean.  <br/> |
|LineStyle  <br/> |xsd:unsignedInt  <br/> |необязательный  <br/> |ИД элемента StyleSheet, от которого этот стиль наследует форматирование строк.  <br/> |Значения типа xsd:unsignedInt.  <br/> |
|Имя  <br/> |xsd:string  <br/> |необязательный  <br/> |Имя элемента.  <br/> |Значения типа xsd:string.  <br/> |
|NameU  <br/> |xsd:string  <br/> |необязательный  <br/> |Универсальное имя элемента.  <br/> |Значения типа xsd:string.  <br/> |
|TextStyle  <br/> |xsd:unsignedInt  <br/> |необязательный  <br/> |ИД элемента StyleSheet, от которого этот стиль наследует форматирование текста.  <br/> |Значения типа xsd:unsignedInt.  <br/> |
   

