---
title: ShapeSheet_Type complexType ('Visio XML»)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: fb394861-34d7-b7dd-1298-0c68a008528d
ms.openlocfilehash: c48af0def561e01fe5a92a57b7416faab40f1200
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25383634"
---
# <a name="shapesheettype-complextype-visio-xml"></a>ShapeSheet_Type complexType ('Visio XML»)

## <a name="type-information"></a>Сведения о типе

|||
|:-----|:-----|
|**Пространство имен** <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|**Файл схемы** <br/> |VisioSchema15-2012-06-05.xsd  <br/> |
|**Базовый элемент расширения** <br/> |Sheet_Type  <br/> |
   
## <a name="definition"></a>Определение

```XML
          <xs:complexType name="ShapeSheet_Type">
          
          <xs:complexContent>
          <xs:extension base="Sheet_Type">
          <xs:sequence>
    <xs:element name="Shapes"  type="Shapes_Type"
     minOccurs="0"
     maxOccurs="1"
    >
    </xs:element>
    
    <xs:element name="Text"  type="Text_Type"
     minOccurs="0"
     maxOccurs="1"
    >
    </xs:element>
    
    <xs:element name="Data1"  type="Data_Type"
     minOccurs="0"
     maxOccurs="1"
    >
    </xs:element>
    
    <xs:element name="Data2"  type="Data_Type"
     minOccurs="0"
     maxOccurs="1"
    >
    </xs:element>
    
    <xs:element name="Data3"  type="Data_Type"
     minOccurs="0"
     maxOccurs="1"
    >
    </xs:element>
    
    <xs:element name="ForeignData"  type="ForeignData_Type"
     minOccurs="0"
     maxOccurs="1"
    >
    </xs:element>
    
      </xs:sequence>
    <xs:attribute name="ID"
  type="xsd:unsignedInt"
     use="required"
    />
    <xs:attribute name="OriginalID"
  type="xsd:unsignedInt"
    />
    <xs:attribute name="Del"
  type="xsd:boolean"
    />
    <xs:attribute name="MasterShape"
  type="xsd:unsignedInt"
    />
    <xs:attribute name="UniqueID"
  type="xsd:string"
    />
    <xs:attribute name="Name"
  type="xsd:string"
    />
    <xs:attribute name="NameU"
  type="xsd:string"
    />
    <xs:attribute name="IsCustomName"
  type="xsd:boolean"
    />
    <xs:attribute name="IsCustomNameU"
  type="xsd:boolean"
    />
    <xs:attribute name="Master"
  type="xsd:unsignedInt"
    />
    <xs:attribute name="Type"
  type="xsd:token"
    />
      </xs:extension>
      </xs:complexContent>
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a>Элементы и атрибуты

Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений. 
  
### <a name="child-elements"></a>Дочерние элементы

|**Элемент**|**Тип**|**Описание**|
|:-----|:-----|:-----|
|[Бд1](data1-element-shapesheet_type-complextypevisio-xml.md) <br/> |[Data_Type](data_type-complextypevisio-xml.md) <br/> ||
|[Бд2](data2-element-shapesheet_type-complextypevisio-xml.md) <br/> |[Data_Type](data_type-complextypevisio-xml.md) <br/> ||
|[Data3](data3-element-shapesheet_type-complextypevisio-xml.md) <br/> |[Data_Type](data_type-complextypevisio-xml.md) <br/> ||
|[ForeignData](foreigndata-element-shapesheet_type-complextypevisio-xml.md) <br/> |[ForeignData_Type](foreigndata_type-complextypevisio-xml.md) <br/> ||
|[Фигур](shapes-element-shapesheet_type-complextypevisio-xml.md) <br/> |[Shapes_Type](shapes_type-complextypevisio-xml.md) <br/> ||
|[Text](text-element-shapesheet_type-complextypevisio-xml.md) <br/> |[Text_Type](text_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a>Атрибуты

|**Атрибут**|**Тип**|**Обязательный**|**Описание**|**Возможные значения**|
|:-----|:-----|:-----|:-----|:-----|
|DEL  <br/> |XSD:Boolean  <br/> |необязательный  <br/> ||Значения типа xsd:boolean.  <br/> |
|ID  <br/> |XSD:unsignedInt  <br/> |Обязательный  <br/> ||Значения типа xsd:unsignedInt.  <br/> |
|IsCustomName  <br/> |XSD:Boolean  <br/> |необязательный  <br/> ||Значения типа xsd:boolean.  <br/> |
|IsCustomNameU  <br/> |XSD:Boolean  <br/> |необязательный  <br/> ||Значения типа xsd:boolean.  <br/> |
|Master  <br/> |XSD:unsignedInt  <br/> |необязательный  <br/> ||Значения типа xsd:unsignedInt.  <br/> |
|MasterShape  <br/> |XSD:unsignedInt  <br/> |необязательный  <br/> ||Значения типа xsd:unsignedInt.  <br/> |
|Имя  <br/> |XSD:String  <br/> |необязательный  <br/> ||Значения типа xsd:string.  <br/> |
|NameU  <br/> |XSD:String  <br/> |необязательный  <br/> ||Значения типа xsd:string.  <br/> |
|OriginalID  <br/> |XSD:unsignedInt  <br/> |необязательный  <br/> ||Значения типа xsd:unsignedInt.  <br/> |
|Тип  <br/> |XSD:Token  <br/> |необязательный  <br/> ||Значения типа xsd:token.  <br/> |
|Уникальный идентификатор  <br/> |XSD:String  <br/> |необязательный  <br/> ||Значения типа xsd:string.  <br/> |
   

