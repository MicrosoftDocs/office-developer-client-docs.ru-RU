---
title: Элемент DocumentSheet (VisioDocument_Type complexType) ('Visio XML»)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 9b8673e1-b913-52db-2d1d-b3e8f4b8f952
description: Определяет структуру DocumentSheet.
ms.openlocfilehash: a2594e0325cc2743036a03998eb7ac71ed2183c8
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25383466"
---
# <a name="documentsheet-element-visiodocumenttype-complextype-visio-xml"></a>Элемент DocumentSheet (VisioDocument_Type complexType) ('Visio XML»)

Определяет структуру DocumentSheet.
  
## <a name="element-information"></a>Сведения об элементе

|||
|:-----|:-----|
|**Тип элемента** <br/> |[DocumentSheet_Type](documentsheet_type-complextypevisio-xml.md) <br/> |
|**Пространство имен** <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Файл схемы** <br/> |VisioSchema15.xsd  <br/> |
|**Части документа** <br/> |Document.XML  <br/> |
   
## <a name="definition"></a>Определение

```XML
< xs:element name="DocumentSheet" type="DocumentSheet_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a>Элементы и атрибуты

Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений. 
  
### <a name="parent-elements"></a>Родительские элементы

|**Элемент**|**Тип**|**Описание**|
|:-----|:-----|:-----|
|[VisioDocument](visiodocument-elementvisio-xml.md) <br/> |[VisioDocument_Type](visiodocument_type-complextypevisio-xml.md) <br/> |Корневой элемент документа Microsoft Visio.  <br/> |
   
### <a name="child-elements"></a>Дочерние элементы

|**Элемент**|**Тип**|**Описание**|
|:-----|:-----|:-----|
|[Cell](cell-elementvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Указывает ячейку в DocumentSheet.  <br/> |
   
### <a name="attributes"></a>Атрибуты

|**Атрибут**|**Тип**|**Обязательный**|**Описание**|**Возможные значения**|
|:-----|:-----|:-----|:-----|:-----|
|IsCustomName  <br/> |XSD:Boolean  <br/> |необязательный  <br/> |Описание, настроен ли имя пользователя.  <br/> |Значения типа xsd:Boolean.  <br/> |
|IsCustomNameU  <br/> |XSD:Boolean  <br/> |необязательный  <br/> |Описание, настроен ли универсального имени пользователя.  <br/> |Значения типа xsd:Boolean.  <br/> |
|Имя  <br/> |XSD:String  <br/> |необязательный  <br/> |Задает имя зависит от языка DocumentSheet.  <br/> |Значения типа xsd:string.  <br/> |
|NameU  <br/> |XSD:String  <br/> |необязательный  <br/> |Задает имя зависящего от языка DocumentSheet.  <br/> |Значения типа xsd:string.  <br/> |
|Уникальный идентификатор  <br/> |XSD:String  <br/> |необязательный  <br/> |Необязательный атрибут типа string. GUID (глобальный уникальный идентификатор), идентифицирующий фигуры.  <br/> |Значения типа xsd:string.  <br/> |
   

