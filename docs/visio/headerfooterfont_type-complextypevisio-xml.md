---
title: HeaderFooterFont_Type complexType (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 1e4134be-fb18-768e-b477-f9f40f72548d
ms.openlocfilehash: dd99d87e0d80aad3bcde31e4834337ee59088da2
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/29/2019
ms.locfileid: "34541073"
---
# <a name="headerfooterfont_type-complextype-visio-xml"></a>HeaderFooterFont_Type complexType (Visio XML)

## <a name="type-information"></a>Сведения о типе

|||
|:-----|:-----|
|**Пространство имен** <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|**Файл схемы** <br/> |VisioSchema15-2012-06-05.xsd  <br/> |
|**Базовый элемент расширения** <br/> |Отсутствует  <br/> |
   
## <a name="definition"></a>Определение

```XML
      <xs:complexType name="HeaderFooterFont_Type">
    <xs:attribute name="Height"
  type="xsd:int"
    />
    <xs:attribute name="Width"
  type="xsd:int"
    />
    <xs:attribute name="Escapement"
  type="xsd:int"
    />
    <xs:attribute name="Orientation"
  type="xsd:int"
    />
    <xs:attribute name="Weight"
  type="xsd:int"
    />
    <xs:attribute name="Italic"
  type="xsd:unsignedByte"
    />
    <xs:attribute name="Underline"
  type="xsd:unsignedByte"
    />
    <xs:attribute name="StrikeOut"
  type="xsd:unsignedByte"
    />
    <xs:attribute name="CharSet"
  type="xsd:unsignedByte"
    />
    <xs:attribute name="OutPrecision"
  type="xsd:unsignedByte"
    />
    <xs:attribute name="ClipPrecision"
  type="xsd:unsignedByte"
    />
    <xs:attribute name="Quality"
  type="xsd:unsignedByte"
    />
    <xs:attribute name="PitchAndFamily"
  type="xsd:unsignedByte"
    />
    <xs:attribute name="FaceName"
  type="xsd:string"
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
|CharSet  <br/> |xsd:unsignedByte  <br/> |необязательный  <br/> ||Значения типа xsd:unsignedByte.  <br/> |
|ClipPrecision  <br/> |xsd:unsignedByte  <br/> |необязательный  <br/> ||Значения типа xsd:unsignedByte.  <br/> |
|Escapement  <br/> |xsd:int  <br/> |необязательный  <br/> ||Значения типа xsd:int.  <br/> |
|FaceName  <br/> |xsd:string  <br/> |необязательный  <br/> ||Значения типа xsd:string.  <br/> |
|Height  <br/> |xsd:int  <br/> |необязательный  <br/> ||Значения типа xsd:int.  <br/> |
|Курсив  <br/> |xsd:unsignedByte  <br/> |необязательный  <br/> ||Значения типа xsd:unsignedByte.  <br/> |
|Вводное обучение  <br/> |xsd:int  <br/> |необязательный  <br/> ||Значения типа xsd:int.  <br/> |
|OutPrecision  <br/> |xsd:unsignedByte  <br/> |необязательный  <br/> ||Значения типа xsd:unsignedByte.  <br/> |
|PitchAndFamily  <br/> |xsd:unsignedByte  <br/> |необязательный  <br/> ||Значения типа xsd:unsignedByte.  <br/> |
|Качество  <br/> |xsd:unsignedByte  <br/> |необязательный  <br/> ||Значения типа xsd:unsignedByte.  <br/> |
|StrikeOut  <br/> |xsd:unsignedByte  <br/> |необязательный  <br/> ||Значения типа xsd:unsignedByte.  <br/> |
|Подчеркнутый  <br/> |xsd:unsignedByte  <br/> |необязательный  <br/> ||Значения типа xsd:unsignedByte.  <br/> |
|Насыщенность  <br/> |xsd:int  <br/> |необязательный  <br/> ||Значения типа xsd:int.  <br/> |
|Width  <br/> |xsd:int  <br/> |необязательный  <br/> ||Значения типа xsd:int.  <br/> |
   

