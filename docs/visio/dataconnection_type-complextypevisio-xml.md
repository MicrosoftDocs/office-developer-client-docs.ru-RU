---
title: Датаконнектион_типе complexType (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 13683c47-2bc8-1345-ed0e-4175a06ea452
ms.openlocfilehash: 0253bf261868ec335bcc295c479cdfc98da79490
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32344606"
---
# <a name="dataconnectiontype-complextype-visio-xml"></a>Датаконнектион_типе complexType (' Visio XML ')

## <a name="type-information"></a>Сведения о типе

|||
|:-----|:-----|
|**Пространство имен** <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|**Файл схемы** <br/> |VisioSchema15-2012-06-05.xsd  <br/> |
|**Базовый элемент расширения** <br/> |Отсутствует  <br/> |
   
## <a name="definition"></a>Определение

```XML
      <xs:complexType name="DataConnection_Type">
    <xs:attribute name="ID"
  type="xsd:unsignedInt"
     use="required"
    />
    <xs:attribute name="FileName"
  type="xsd:string"
     use="required"
    />
    <xs:attribute name="ConnectionString"
  type="xsd:string"
    />
    <xs:attribute name="Command"
  type="xsd:string"
    />
    <xs:attribute name="FriendlyName"
  type="xsd:string"
    />
    <xs:attribute name="Timeout"
  type="xsd:unsignedInt"
    />
    <xs:attribute name="AlwaysUseConnectionFile"
  type="xsd:boolean"
    />
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a>Элементы и атрибуты

Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений. 
  
### <a name="child-elements"></a>Дочерние элементы

Нет.
  
### <a name="attributes"></a>Атрибуты

|**Атрибут**|**Тип**|**Обязательный**|**Описание**|**Возможные значения**|
|:-----|:-----|:-----|:-----|:-----|
|AlwaysUseConnectionFile  <br/> |XSD: Boolean  <br/> |необязательный  <br/> ||Значения типа XSD: Boolean.  <br/> |
|Command  <br/> |XSD: строка  <br/> |необязательный  <br/> ||Значения типа String: XSD.  <br/> |
|ConnectionString  <br/> |XSD: строка  <br/> |необязательный  <br/> ||Значения типа String: XSD.  <br/> |
|FileName  <br/> |XSD: строка  <br/> |Обязательный  <br/> ||Значения типа String: XSD.  <br/> |
|FriendlyName  <br/> |XSD: строка  <br/> |необязательный  <br/> ||Значения типа String: XSD.  <br/> |
|ИД  <br/> |XSD: Унсигнединт  <br/> |Обязательный  <br/> ||Значения типа XSD: Унсигнединт.  <br/> |
|Timeout  <br/> |XSD: Унсигнединт  <br/> |необязательный  <br/> ||Значения типа XSD: Унсигнединт.  <br/> |
   

