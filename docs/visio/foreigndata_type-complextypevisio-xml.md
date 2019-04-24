---
title: Фореигндата_типе complexType (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 21b394a6-6f95-fc17-482c-4cb648a0d9bb
ms.openlocfilehash: 6630c8b33dc1c4c7cbb12bb9727d4f0b1e1b19d2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32346013"
---
# <a name="foreigndatatype-complextype-visio-xml"></a>Фореигндата_типе complexType (' Visio XML ')

## <a name="type-information"></a>Сведения о типе

|||
|:-----|:-----|
|**Пространство имен** <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
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
|[Rel](rel-element-foreigndata_type-complextypevisio-xml.md) <br/> |[Рел_типе](rel_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a>Атрибуты

|**Атрибут**|**Тип**|**Обязательный**|**Описание**|**Возможные значения**|
|:-----|:-----|:-----|:-----|:-----|
|Компрессионлевел  <br/> |XSD: Double  <br/> |необязательный  <br/> ||Значения типа XSD: Double.  <br/> |
|Компрессионтипе  <br/> |XSD: маркер  <br/> |необязательный  <br/> ||Значения типа маркера XSD:.  <br/> |
|Екстенткс  <br/> |XSD: Double  <br/> |необязательный  <br/> ||Значения типа XSD: Double.  <br/> |
|Экстент  <br/> |XSD: Double  <br/> |необязательный  <br/> ||Значения типа XSD: Double.  <br/> |
|ForeignType  <br/> |XSD: маркер  <br/> |Обязательный  <br/> ||Значения типа маркера XSD:.  <br/> |
|Маппингмоде  <br/> |xsd:unsignedShort  <br/> |необязательный  <br/> ||Значения для типа xsd:unsignedShort.  <br/> |
|Обжексеигхт  <br/> |XSD: Double  <br/> |необязательный  <br/> ||Значения типа XSD: Double.  <br/> |
|ObjectType  <br/> |XSD: Унсигнединт  <br/> |необязательный  <br/> ||Значения типа XSD: Унсигнединт.  <br/> |
|Обжектвидс  <br/> |XSD: Double  <br/> |необязательный  <br/> ||Значения типа XSD: Double.  <br/> |
|Шовасикон  <br/> |XSD: Boolean  <br/> |необязательный  <br/> ||Значения типа XSD: Boolean.  <br/> |
   

