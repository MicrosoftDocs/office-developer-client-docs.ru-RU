---
title: Элемент ColorEntry (Colors_Type complexType) ('Visio XML»)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 3f325ad8-bbc7-28bf-9e48-1fde4fbdbdc0
description: Содержит запись таблицы цвет.
ms.openlocfilehash: 14ef92069ce8d963ce4a0770324843321804c5cd
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25385342"
---
# <a name="colorentry-element-colorstype-complextype-visio-xml"></a>Элемент ColorEntry (Colors_Type complexType) ('Visio XML»)

Содержит запись таблицы цвет.
  
## <a name="element-information"></a>Сведения об элементе

|||
|:-----|:-----|
|**Тип элемента** <br/> |[ColorEntry_Type](colorentry_type-complextypevisio-xml.md) <br/> |
|**Пространство имен** <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Файл схемы** <br/> |VisioSchema15.xsd  <br/> |
|**Части документа** <br/> |Document.XML  <br/> |
   
## <a name="definition"></a>Определение

```XML
< xs:element name="ColorEntry" type="ColorEntry_Type" minOccurs="1" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a>Элементы и атрибуты

Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений. 
  
### <a name="parent-elements"></a>Родительские элементы

|**Элемент**|**Тип**|**Описание**|
|:-----|:-----|:-----|
|[цвета;](colors-element-visiodocument_type-complextypevisio-xml.md) <br/> |[Colors_Type](colors_type-complextypevisio-xml.md) <br/> |Содержит таблицы цветов документа.  <br/> |
   
### <a name="child-elements"></a>Дочерние элементы

Нет.
  
### <a name="attributes"></a>Атрибуты

|**Атрибут**|**Тип**|**Обязательный**|**Описание**|**Возможные значения**|
|:-----|:-----|:-----|:-----|:-----|
|IX  <br/> |XSD:unsignedInt  <br/> |Обязательный  <br/> |Отсчитываемый от нуля индекс элемента в рамках родительского элемента.  <br/> |Значения типа xsd:unsignedInt.  <br/> |
|RGB  <br/> |XSD:String  <br/> |Обязательный  <br/> |Шестнадцатеричное значение цвета из таблицы назначения.  <br/> |Значения типа xsd:string.  <br/> |
   

