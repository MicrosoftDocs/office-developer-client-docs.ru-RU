---
title: HeaderFooterFont_Type complexType (XML для Visio)
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
# <a name="headerfooterfont_type-complextype-visio-xml"></a>HeaderFooterFont_Type complexType (XML для Visio)

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
|CharSet  <br/> |XSD: Унсигнедбите  <br/> |необязательный  <br/> ||Значения типа XSD: Унсигнедбите.  <br/> |
|клиппреЦисион  <br/> |XSD: Унсигнедбите  <br/> |необязательный  <br/> ||Значения типа XSD: Унсигнедбите.  <br/> |
|Последовательное преобразование  <br/> |XSD: int  <br/> |необязательный  <br/> ||Значения типа XSD: int.  <br/> |
|фаценаме  <br/> |XSD: строка  <br/> |необязательный  <br/> ||Значения типа String: XSD.  <br/> |
|Height  <br/> |XSD: int  <br/> |необязательный  <br/> ||Значения типа XSD: int.  <br/> |
|Курсив  <br/> |XSD: Унсигнедбите  <br/> |необязательный  <br/> ||Значения типа XSD: Унсигнедбите.  <br/> |
|Вводное обучение  <br/> |XSD: int  <br/> |необязательный  <br/> ||Значения типа XSD: int.  <br/> |
|Точность  <br/> |XSD: Унсигнедбите  <br/> |необязательный  <br/> ||Значения типа XSD: Унсигнедбите.  <br/> |
|PitchAndFamily  <br/> |XSD: Унсигнедбите  <br/> |необязательный  <br/> ||Значения типа XSD: Унсигнедбите.  <br/> |
|Качество  <br/> |XSD: Унсигнедбите  <br/> |необязательный  <br/> ||Значения типа XSD: Унсигнедбите.  <br/> |
|Зачеркнутый  <br/> |XSD: Унсигнедбите  <br/> |необязательный  <br/> ||Значения типа XSD: Унсигнедбите.  <br/> |
|Подчеркнутый  <br/> |XSD: Унсигнедбите  <br/> |необязательный  <br/> ||Значения типа XSD: Унсигнедбите.  <br/> |
|Насыщенность  <br/> |XSD: int  <br/> |необязательный  <br/> ||Значения типа XSD: int.  <br/> |
|Width  <br/> |XSD: int  <br/> |необязательный  <br/> ||Значения типа XSD: int.  <br/> |
   

