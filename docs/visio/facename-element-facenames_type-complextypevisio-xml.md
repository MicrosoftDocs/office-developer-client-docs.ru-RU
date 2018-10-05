---
title: Элемент название значка (FaceNames_Type complexType) ('Visio XML»)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: b1783f05-ced1-917f-8298-eca4ecfa3912
description: Содержит сведения о шрифта.
ms.openlocfilehash: 4c8f047d655be167dc058b3e29ac62161887ce99
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25389780"
---
# <a name="facename-element-facenamestype-complextype-visio-xml"></a>Элемент название значка (FaceNames_Type complexType) ('Visio XML»)

Содержит сведения о шрифта.
  
## <a name="element-information"></a>Сведения об элементе

|||
|:-----|:-----|
|**Тип элемента** <br/> |[FaceName_Type](facename_type-complextypevisio-xml.md) <br/> |
|**Пространство имен** <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Файл схемы** <br/> |VisioSchema15.xsd  <br/> |
|**Части документа** <br/> |Document.XML  <br/> |
   
## <a name="definition"></a>Определение

```XML
< xs:element name="FaceName" type="FaceName_Type" minOccurs="1" maxOccurs="unbounded" >
</xs:element > 
```

## <a name="elements-and-attributes"></a>Элементы и атрибуты

Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений. 
  
### <a name="parent-elements"></a>Родительские элементы

|**Элемент**|**Тип**|**Описание**|
|:-----|:-----|:-----|
|[FaceNames](facenames-element-visiodocument_type-complextypevisio-xml.md) <br/> |[FaceNames_Type](facenames_type-complextypevisio-xml.md) <br/> |Содержит коллекцию элементов **Название значка** .  <br/> |
   
### <a name="child-elements"></a>Дочерние элементы

Нет.
  
### <a name="attributes"></a>Атрибуты

|**Атрибут**|**Тип**|**Обязательный**|**Описание**|**Возможные значения**|
|:-----|:-----|:-----|:-----|:-----|
|Наборов символов  <br/> |XSD:String  <br/> |необязательный  <br/> |Поддерживаемые кодировки шрифта.  <br/> |Значения типа xsd:string.  <br/> |
|Флаги  <br/> |XSD:unsignedInt  <br/> |необязательный  <br/> |Флаги, указывающие следующее: отсутствующие шрифта, шрифта по умолчанию, азиатских шрифтов, сложных шрифтов, вертикальной шрифт и тип шрифта.  <br/> |Значения типа xsd:unsignedInt.  <br/> |
|NameU  <br/> |XSD:String  <br/> |Обязательный  <br/> |Имя шрифта строки Юникод UTF-16.  <br/> ||
|Panos  <br/> |XSD:String  <br/> |необязательный  <br/> |Подпись сходстве для шрифта. Сходстве — это система классификации для гарнитуры, разделяет на их основе своих визуальных характеристик категории.  <br/> |Значения типа xsd:string.  <br/> |
|UnicodeRanges  <br/> |XSD:String  <br/> |необязательный  <br/> |Поддерживаемые Диапазоны Юникода шрифта.  <br/> |Значения типа xsd:string.  <br/> |
   

