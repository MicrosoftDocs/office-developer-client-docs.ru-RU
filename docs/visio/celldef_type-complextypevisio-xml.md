---
title: Целлдеф_типе complexType (XML для Visio)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 87ea346d-1786-dc87-073d-8e7459b7fef1
ms.openlocfilehash: 7b437e35aadfef0390908cb1337cc738668382e5
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/29/2019
ms.locfileid: "34542298"
---
# <a name="celldeftype-complextype-visio-xml"></a>Целлдеф_типе complexType (XML для Visio)

## <a name="type-information"></a>Сведения о типе

|||
|:-----|:-----|
|**Пространство имен** <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|**Файл схемы** <br/> |VisioSchema15-2012-06-05.xsd  <br/> |
|**Базовый элемент расширения** <br/> |Отсутствует  <br/> |
   
## <a name="definition"></a>Определение

```XML
      <xs:complexType name="CellDef_Type">
    <xs:attribute name="N"
  type="xsd:string"
     use="required"
    />
    <xs:attribute name="T"
  type="xsd:token"
     use="required"
    />
    <xs:attribute name="F"
  type="xsd:string"
    />
    <xs:attribute name="IX"
  type="xsd:unsignedByte"
    />
    <xs:attribute name="S"
  type="xsd:unsignedByte"
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
|F  <br/> |XSD: строка  <br/> |необязательный  <br/> ||Значения типа String: XSD.  <br/> |
|IX  <br/> |XSD: Унсигнедбите  <br/> |необязательный  <br/> ||Значения типа XSD: Унсигнедбите.  <br/> |
|N  <br/> |XSD: строка  <br/> |Обязательный  <br/> ||Значения типа String: XSD.  <br/> |
|S  <br/> |XSD: Унсигнедбите  <br/> |необязательный  <br/> ||Значения типа XSD: Унсигнедбите.  <br/> |
|Д  <br/> |XSD: маркер  <br/> |Обязательный  <br/> ||Значения типа маркера XSD:.  <br/> |
   

