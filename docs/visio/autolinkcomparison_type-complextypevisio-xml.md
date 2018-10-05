---
title: AutoLinkComparison_Type complexType ('Visio XML»)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 319b4bfb-a798-4f6c-52be-45708ac40869
ms.openlocfilehash: 235b63777d21955a2f2062757d6a54e899b169ac
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25389752"
---
# <a name="autolinkcomparisontype-complextype-visio-xml"></a>AutoLinkComparison_Type complexType ('Visio XML»)

## <a name="type-information"></a>Сведения о типе

|||
|:-----|:-----|
|**Пространство имен** <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|**Файл схемы** <br/> |VisioSchema15-2012-06-05.xsd  <br/> |
|**Базовый элемент расширения** <br/> |Отсутствует  <br/> |
   
## <a name="definition"></a>Определение

```XML
      <xs:complexType name="AutoLinkComparison_Type">
    <xs:attribute name="ColumnName"
  type="xsd:string"
     use="required"
    />
    <xs:attribute name="ContextType"
  type="xsd:unsignedInt"
     use="required"
    />
    <xs:attribute name="ContextTypeLabel"
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
|ColumnName  <br/> |XSD:String  <br/> |Обязательный  <br/> ||Значения типа xsd:string.  <br/> |
|ContextType  <br/> |XSD:unsignedInt  <br/> |Обязательный  <br/> ||Значения типа xsd:unsignedInt.  <br/> |
|ContextTypeLabel  <br/> |XSD:String  <br/> |необязательный  <br/> ||Значения типа xsd:string.  <br/> |
   

