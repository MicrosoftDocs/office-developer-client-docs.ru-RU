---
title: Элемент название значка (FaceNames_Type complexType) ('Visio XML»)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: b1783f05-ced1-917f-8298-eca4ecfa3912
description: Содержит сведения о шрифта.
ms.openlocfilehash: 8a66d5294e239e4540939cc7053e1f67a777144d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19813709"
---
# <a name="facename-element-facenamestype-complextype-visio-xml"></a>Элемент название значка (FaceNames_Type complexType) ('Visio XML»)

Содержит сведения о шрифта.
  
## <a name="element-information"></a>Сведения об элементе

|||
|:-----|:-----|
|**Тип элемента** <br/> |[FaceName_Type](facename_type-complextypevisio-xml.md) <br/> |
|**Пространство имен** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Файл схемы** <br/> |VisioSchema15.xsd  <br/> |
|**Части документа** <br/> |Document.XML  <br/> |
   
## <a name="definition"></a>Определение

```XML
< xs:element name="FaceName" type="FaceName_Type" minOccurs="1" maxOccurs="unbounded" >
</xs:element > 
```

## <a name="elements-and-attributes"></a>Элементы и атрибуты

Если схема определяет специальные требования, такие как **последовательность**, **minOccurs**, **maxOccurs**и **выбора**, обратитесь к разделу определение. 
  
### <a name="parent-elements"></a>Родительские элементы

|**Элемент**|**Тип**|**Описание**|
|:-----|:-----|:-----|
|[FaceNames](facenames-element-visiodocument_type-complextypevisio-xml.md) <br/> |[FaceNames_Type](facenames_type-complextypevisio-xml.md) <br/> |Содержит коллекцию элементов **Название значка** .  <br/> |
   
### <a name="child-elements"></a>Дочерние элементы

Нет.
  
### <a name="attributes"></a>Атрибуты

|**Атрибут**|**Тип**|**Обязательное**|**Описание**|**Возможные значения**|
|:-----|:-----|:-----|:-----|:-----|
|Наборов символов  <br/> |XSD:String  <br/> |необязательный  <br/> |Поддерживаемые кодировки шрифта.  <br/> |Значения типа xsd:string.  <br/> |
|Флаги  <br/> |XSD:unsignedInt  <br/> |необязательный  <br/> |Флаги, указывающие следующее: отсутствующие шрифта, шрифта по умолчанию, азиатских шрифтов, сложных шрифтов, вертикальной шрифт и тип шрифта.  <br/> |Значения типа xsd:unsignedInt.  <br/> |
|NameU  <br/> |XSD:String  <br/> |Обязательный  <br/> |Имя шрифта строки Юникод UTF-16.  <br/> ||
|Panos  <br/> |XSD:String  <br/> |необязательный  <br/> |Подпись сходстве для шрифта. Сходстве — это система классификации для гарнитуры, разделяет на их основе своих визуальных характеристик категории.  <br/> |Значения типа xsd:string.  <br/> |
|UnicodeRanges  <br/> |XSD:String  <br/> |необязательный  <br/> |Поддерживаемые Диапазоны Юникода шрифта.  <br/> |Значения типа xsd:string.  <br/> |
   

