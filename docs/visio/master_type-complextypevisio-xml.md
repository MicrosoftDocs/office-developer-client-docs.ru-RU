---
title: Мастер_типе complexType (XML для Visio)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 2d799074-13d9-3c98-3bee-b57af9966c81
ms.openlocfilehash: 22b619149fc5393f085ca6e245c65ed6058538ae
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/29/2019
ms.locfileid: "34538069"
---
# <a name="mastertype-complextype-visio-xml"></a>Мастер_типе complexType (XML для Visio)

## <a name="type-information"></a>Сведения о типе

|||
|:-----|:-----|
|**Пространство имен** <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|**Файл схемы** <br/> |VisioSchema15-2012-06-05.xsd  <br/> |
|**Базовый элемент расширения** <br/> |Отсутствует  <br/> |
   
## <a name="definition"></a>Определение

```XML
          <xs:complexType name="Master_Type">
          
          <xs:all>
    <xs:element name="PageSheet"  type="PageSheet_Type"
     minOccurs="0"
     maxOccurs="1"
    >
    </xs:element>
    
    <xs:element name="Rel"  type="Rel_Type"
     minOccurs="1"
     maxOccurs="1"
    >
    </xs:element>
    
    <xs:element name="Icon"  type="Icon_Type"
     minOccurs="0"
     maxOccurs="1"
    >
    </xs:element>
    
      </xs:all>
    <xs:attribute name="ID"
  type="xsd:unsignedInt"
     use="required"
    />
    <xs:attribute name="BaseID"
  type="xsd:string"
    />
    <xs:attribute name="UniqueID"
  type="xsd:string"
    />
    <xs:attribute name="MatchByName"
  type="xsd:boolean"
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
    <xs:attribute name="IconSize"
  type="xsd:unsignedShort"
    />
    <xs:attribute name="PatternFlags"
  type="xsd:unsignedShort"
    />
    <xs:attribute name="Prompt"
  type="xsd:string"
    />
    <xs:attribute name="Hidden"
  type="xsd:boolean"
    />
    <xs:attribute name="IconUpdate"
  type="xsd:boolean"
    />
    <xs:attribute name="AlignName"
  type="xsd:unsignedShort"
    />
    <xs:attribute name="MasterType"
  type="xsd:unsignedShort"
    />
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a>Элементы и атрибуты

Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений. 
  
### <a name="child-elements"></a>Дочерние элементы

|**Элемент**|**Тип**|**Описание**|
|:-----|:-----|:-----|
|[Icon](icon-element-master_type-complextypevisio-xml.md) <br/> |[Икон_типе](icon_type-complextypevisio-xml.md) <br/> ||
|[PageSheet](pagesheet-element-master_type-complextypevisio-xml.md) <br/> |[Пажешит_типе](pagesheet_type-complextypevisio-xml.md) <br/> ||
|[Rel](rel-element-master_type-complextypevisio-xml.md) <br/> |[Рел_типе](rel_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a>Атрибуты

|**Атрибут**|**Тип**|**Обязательный**|**Описание**|**Возможные значения**|
|:-----|:-----|:-----|:-----|:-----|
|AlignName  <br/> |xsd:unsignedShort  <br/> |необязательный  <br/> ||Значения для типа xsd:unsignedShort.  <br/> |
|BaseID  <br/> |XSD: строка  <br/> |необязательный  <br/> ||Значения типа String: XSD.  <br/> |
|Hidden  <br/> |XSD: Boolean  <br/> |необязательный  <br/> ||Значения типа XSD: Boolean.  <br/> |
|IconSize  <br/> |xsd:unsignedShort  <br/> |необязательный  <br/> ||Значения для типа xsd:unsignedShort.  <br/> |
|IconUpdate  <br/> |XSD: Boolean  <br/> |необязательный  <br/> ||Значения типа XSD: Boolean.  <br/> |
|ID  <br/> |XSD: Унсигнединт  <br/> |Обязательный  <br/> ||Значения типа XSD: Унсигнединт.  <br/> |
|Искустомнаме  <br/> |XSD: Boolean  <br/> |необязательный  <br/> ||Значения типа XSD: Boolean.  <br/> |
|Искустомнамеу  <br/> |XSD: Boolean  <br/> |необязательный  <br/> ||Значения типа XSD: Boolean.  <br/> |
|MasterType  <br/> |xsd:unsignedShort  <br/> |необязательный  <br/> ||Значения для типа xsd:unsignedShort.  <br/> |
|MatchByName  <br/> |XSD: Boolean  <br/> |необязательный  <br/> ||Значения типа XSD: Boolean.  <br/> |
|Имя  <br/> |XSD: строка  <br/> |необязательный  <br/> ||Значения типа String: XSD.  <br/> |
|NameU  <br/> |XSD: строка  <br/> |необязательный  <br/> ||Значения типа String: XSD.  <br/> |
|PatternFlags  <br/> |xsd:unsignedShort  <br/> |необязательный  <br/> ||Значения для типа xsd:unsignedShort.  <br/> |
|Prompt  <br/> |XSD: строка  <br/> |необязательный  <br/> ||Значения типа String: XSD.  <br/> |
|UniqueID  <br/> |XSD: строка  <br/> |необязательный  <br/> ||Значения типа String: XSD.  <br/> |
   

