---
title: Фаценаме_типе complexType (XML для Visio)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: d24f350c-35bf-ab16-2469-39fd5344e5fe
ms.openlocfilehash: f0a136cec6d620ba7001ed0e6fae01af82c2180d
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/29/2019
ms.locfileid: "34542900"
---
# <a name="facenametype-complextype-visio-xml"></a>Фаценаме_типе complexType (XML для Visio)

## <a name="type-information"></a>Сведения о типе

|||
|:-----|:-----|
|**Пространство имен** <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|**Файл схемы** <br/> |VisioSchema15-2012-06-05.xsd  <br/> |
|**Базовый элемент расширения** <br/> |Отсутствует  <br/> |
   
## <a name="definition"></a>Определение

```XML
      <xs:complexType name="FaceName_Type">
    <xs:attribute name="NameU"
  type="xsd:string"
     use="required"
    />
    <xs:attribute name="UnicodeRanges"
  type="xsd:string"
    />
    <xs:attribute name="CharSets"
  type="xsd:string"
    />
    <xs:attribute name="Panos"
  type="xsd:string"
    />
    <xs:attribute name="Panose"
  type="xsd:string"
    />
    <xs:attribute name="Flags"
  type="xsd:unsignedInt"
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
|Чарсетс  <br/> |XSD: строка  <br/> |необязательный  <br/> ||Значения типа String: XSD.  <br/> |
|Flags  <br/> |XSD: Унсигнединт  <br/> |необязательный  <br/> ||Значения типа XSD: Унсигнединт.  <br/> |
|NameU  <br/> |XSD: строка  <br/> |Обязательный  <br/> ||Значения типа String: XSD.  <br/> |
|Панос  <br/> |XSD: строка  <br/> |необязательный  <br/> ||Значения типа String: XSD.  <br/> |
|Паносе  <br/> |XSD: строка  <br/> |необязательный  <br/> ||Значения типа String: XSD.  <br/> |
|Уникодеранжес  <br/> |XSD: строка  <br/> |необязательный  <br/> ||Значения типа String: XSD.  <br/> |
   

