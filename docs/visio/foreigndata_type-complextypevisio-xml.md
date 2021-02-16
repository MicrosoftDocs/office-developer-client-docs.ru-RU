---
title: ForeignData_Type complexType (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 21b394a6-6f95-fc17-482c-4cb648a0d9bb
ms.openlocfilehash: 39396ef0db5b78d6f32d8828103eecd105f8b91d
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/29/2019
ms.locfileid: "34539865"
---
# <a name="foreigndata_type-complextype-visio-xml"></a>ForeignData_Type complexType (Visio XML)

## <a name="type-information"></a>Сведения о типе

|||
|:-----|:-----|
|**Пространство имен** <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|**Файл схемы** <br/> |VisioSchema15-2012-06-05.xsd  <br/> |
|**Базовый элемент расширения** <br/> |Отсутствует  <br/> |
   
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

Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений. 
  
### <a name="child-elements"></a>Дочерние элементы

|**Элемент**|**Тип**|**Описание**|
|:-----|:-----|:-----|
|[Rel](rel-element-foreigndata_type-complextypevisio-xml.md) <br/> |[Rel_Type](rel_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a>Атрибуты

|**Атрибут**|**Тип**|**Обязательный**|**Описание**|**Возможные значения**|
|:-----|:-----|:-----|:-----|:-----|
|CompressionLevel  <br/> |xsd:double  <br/> |необязательный  <br/> ||Значения типа xsd:double.  <br/> |
|CompressionType  <br/> |xsd:token  <br/> |необязательный  <br/> ||Значения типа xsd:token.  <br/> |
|ExtentX  <br/> |xsd:double  <br/> |необязательный  <br/> ||Значения типа xsd:double.  <br/> |
|ExtentY  <br/> |xsd:double  <br/> |необязательный  <br/> ||Значения типа xsd:double.  <br/> |
|ForeignType  <br/> |xsd:token  <br/> |Обязательный  <br/> ||Значения типа xsd:token.  <br/> |
|MappingMode  <br/> |xsd:unsignedShort  <br/> |необязательный  <br/> ||Значения для типа xsd:unsignedShort.  <br/> |
|ObjectHeight  <br/> |xsd:double  <br/> |необязательный  <br/> ||Значения типа xsd:double.  <br/> |
|ObjectType  <br/> |xsd:unsignedInt  <br/> |необязательный  <br/> ||Значения типа xsd:unsignedInt.  <br/> |
|ObjectWidth  <br/> |xsd:double  <br/> |необязательный  <br/> ||Значения типа xsd:double.  <br/> |
|ShowAsIcon  <br/> |xsd:boolean  <br/> |необязательный  <br/> ||Значения типа xsd:boolean.  <br/> |
   

