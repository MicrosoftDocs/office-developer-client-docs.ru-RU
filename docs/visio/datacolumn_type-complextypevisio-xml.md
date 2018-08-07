---
title: DataColumn_Type complexType ('Visio XML»)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: bee50623-cdf7-b9d7-867a-70c86922cbac
ms.openlocfilehash: 9d334190b686f3b2c5e25a31336c668c957e820f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19813533"
---
# <a name="datacolumntype-complextype-visio-xml"></a>DataColumn_Type complexType ('Visio XML»)

## <a name="type-information"></a>Сведения о типе

|||
|:-----|:-----|
|**Пространство имен** <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|**Файл схемы** <br/> |VisioSchema15-2012-06-05.xsd  <br/> |
|**База расширения** <br/> |Нет  <br/> |
   
## <a name="definition"></a>Определение

```XML
      <xs:complexType name="DataColumn_Type">
    <xs:attribute name="ColumnNameID"
  type="xsd:string"
     use="required"
    />
    <xs:attribute name="Name"
  type="xsd:string"
     use="required"
    />
    <xs:attribute name="Label"
  type="xsd:string"
     use="required"
    />
    <xs:attribute name="OrigLabel"
  type="xsd:string"
    />
    <xs:attribute name="LangID"
  type="xsd:unsignedInt"
    />
    <xs:attribute name="Calendar"
  type="xsd:unsignedShort"
    />
    <xs:attribute name="DataType"
  type="xsd:unsignedShort"
    />
    <xs:attribute name="UnitType"
  type="xsd:string"
    />
    <xs:attribute name="Currency"
  type="xsd:unsignedShort"
    />
    <xs:attribute name="Degree"
  type="xsd:unsignedInt"
    />
    <xs:attribute name="DisplayWidth"
  type="xsd:unsignedInt"
    />
    <xs:attribute name="DisplayOrder"
  type="xsd:unsignedInt"
    />
    <xs:attribute name="Mapped"
  type="xsd:boolean"
    />
    <xs:attribute name="Hyperlink"
  type="xsd:boolean"
    />
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a>Элементы и атрибуты

Если схема определяет специальные требования, такие как **последовательность**, **minOccurs**, **maxOccurs**и **выбора**, обратитесь к разделу определение. 
  
### <a name="child-elements"></a>Дочерние элементы

Нет.
  
### <a name="attributes"></a>Атрибуты

|**Атрибут**|**Тип**|**Обязательное**|**Описание**|**Возможные значения**|
|:-----|:-----|:-----|:-----|:-----|
|Календарь  <br/> |XSD:unsignedShort  <br/> |необязательный  <br/> ||Значения типа xsd:unsignedShort.  <br/> |
|ColumnNameID  <br/> |XSD:String  <br/> |Обязательный  <br/> ||Значения типа xsd:string.  <br/> |
|Денежный  <br/> |XSD:unsignedShort  <br/> |необязательный  <br/> ||Значения типа xsd:unsignedShort.  <br/> |
|DataType  <br/> |XSD:unsignedShort  <br/> |необязательный  <br/> ||Значения типа xsd:unsignedShort.  <br/> |
|Степень  <br/> |XSD:unsignedInt  <br/> |необязательный  <br/> ||Значения типа xsd:unsignedInt.  <br/> |
|DisplayOrder  <br/> |XSD:unsignedInt  <br/> |необязательный  <br/> ||Значения типа xsd:unsignedInt.  <br/> |
|DisplayWidth  <br/> |XSD:unsignedInt  <br/> |необязательный  <br/> ||Значения типа xsd:unsignedInt.  <br/> |
|Гиперссылка  <br/> |XSD:Boolean  <br/> |необязательный  <br/> ||Значения типа xsd:boolean.  <br/> |
|Метка  <br/> |XSD:String  <br/> |Обязательный  <br/> ||Значения типа xsd:string.  <br/> |
|LangID  <br/> |XSD:unsignedInt  <br/> |необязательный  <br/> ||Значения типа xsd:unsignedInt.  <br/> |
|Сопоставленные  <br/> |XSD:Boolean  <br/> |необязательный  <br/> ||Значения типа xsd:boolean.  <br/> |
|Имя  <br/> |XSD:String  <br/> |Обязательный  <br/> ||Значения типа xsd:string.  <br/> |
|OrigLabel  <br/> |XSD:String  <br/> |необязательный  <br/> ||Значения типа xsd:string.  <br/> |
|UnitType  <br/> |XSD:String  <br/> |необязательный  <br/> ||Значения типа xsd:string.  <br/> |
   

