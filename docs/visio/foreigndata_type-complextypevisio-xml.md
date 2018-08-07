---
title: ForeignData_Type complexType ('Visio XML»)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 21b394a6-6f95-fc17-482c-4cb648a0d9bb
ms.openlocfilehash: 1d9358de2f88a1b9e035ecf4966544ea935f8b2b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19813819"
---
# <a name="foreigndatatype-complextype-visio-xml"></a>ForeignData_Type complexType ('Visio XML»)

## <a name="type-information"></a>Сведения о типе

|||
|:-----|:-----|
|**Пространство имен** <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|**Файл схемы** <br/> |VisioSchema15-2012-06-05.xsd  <br/> |
|**База расширения** <br/> |Нет  <br/> |
   
## <a name="definition"></a>Определение

```XML
          <xs:complexType name="ForeignData_Type">
          
          <xs:sequence>
    <xs:element name="Rel"  type="Rel_Type"
     minOccurs="1"
     maxOccurs="1"
    >
    </xs:element>
    
      </xs:sequence>
    <xs:attribute name="ForeignType"
  type="xsd:token"
     use="required"
    />
    <xs:attribute name="ObjectType"
  type="xsd:unsignedInt"
    />
    <xs:attribute name="ShowAsIcon"
  type="xsd:boolean"
    />
    <xs:attribute name="ObjectWidth"
  type="xsd:double"
    />
    <xs:attribute name="ObjectHeight"
  type="xsd:double"
    />
    <xs:attribute name="MappingMode"
  type="xsd:unsignedShort"
    />
    <xs:attribute name="ExtentX"
  type="xsd:double"
    />
    <xs:attribute name="ExtentY"
  type="xsd:double"
    />
    <xs:attribute name="CompressionType"
  type="xsd:token"
    />
    <xs:attribute name="CompressionLevel"
  type="xsd:double"
    />
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a>Элементы и атрибуты

Если схема определяет специальные требования, такие как **последовательность**, **minOccurs**, **maxOccurs**и **выбора**, обратитесь к разделу определение. 
  
### <a name="child-elements"></a>Дочерние элементы

|**Элемент**|**Тип**|**Описание**|
|:-----|:-----|:-----|
|[Rel](rel-element-foreigndata_type-complextypevisio-xml.md) <br/> |[Rel_Type](rel_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a>Атрибуты

|**Атрибут**|**Тип**|**Обязательное**|**Описание**|**Возможные значения**|
|:-----|:-----|:-----|:-----|:-----|
|CompressionLevel  <br/> |XSD: double  <br/> |необязательный  <br/> ||Значения типа XSD: double.  <br/> |
|CompressionType  <br/> |XSD:Token  <br/> |необязательный  <br/> ||Значения типа xsd:token.  <br/> |
|ExtentX  <br/> |XSD: double  <br/> |необязательный  <br/> ||Значения типа XSD: double.  <br/> |
|ExtentY  <br/> |XSD: double  <br/> |необязательный  <br/> ||Значения типа XSD: double.  <br/> |
|ForeignType  <br/> |XSD:Token  <br/> |Обязательный  <br/> ||Значения типа xsd:token.  <br/> |
|MappingMode  <br/> |XSD:unsignedShort  <br/> |необязательный  <br/> ||Значения типа xsd:unsignedShort.  <br/> |
|ObjectHeight  <br/> |XSD: double  <br/> |необязательный  <br/> ||Значения типа XSD: double.  <br/> |
|Тип объекта  <br/> |XSD:unsignedInt  <br/> |необязательный  <br/> ||Значения типа xsd:unsignedInt.  <br/> |
|ObjectWidth  <br/> |XSD: double  <br/> |необязательный  <br/> ||Значения типа XSD: double.  <br/> |
|ShowAsIcon  <br/> |XSD:Boolean  <br/> |необязательный  <br/> ||Значения типа xsd:boolean.  <br/> |
   

