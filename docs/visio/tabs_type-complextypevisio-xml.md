---
title: Tabs_Type complexType ('Visio XML»)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: b97155ce-f0d2-e35c-bc58-e288f653ce2c
ms.openlocfilehash: ea55169051c66f7434a1e1ba11ff5a23dee0e9c8
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25386777"
---
# <a name="tabstype-complextype-visio-xml"></a>Tabs_Type complexType ('Visio XML»)

## <a name="type-information"></a>Сведения о типе

|||
|:-----|:-----|
|**Пространство имен** <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|**Файл схемы** <br/> |VisioSchema15-2012-06-05.xsd  <br/> |
|**Базовый элемент расширения** <br/> |Section_Type  <br/> |
   
## <a name="definition"></a>Определение

```XML
          <xs:complexType name="Tabs_Type">
          
          <xs:complexContent>
          <xs:extension base="Section_Type">
          <xs:sequence minOccurs="0" maxOccurs="unbounded">
    <xs:element name="Row"  type="TabsRow_Type"
    >
    </xs:element>
    
      </xs:sequence>
      </xs:extension>
      </xs:complexContent>
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a>Элементы и атрибуты

Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений. 
  
### <a name="child-elements"></a>Дочерние элементы

|**Элемент**|**Тип**|**Описание**|
|:-----|:-----|:-----|
|[Строка](row-element-tabs-sectionvisio-xml.md) <br/> |[TabsRow_Type](tabsrow_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a>Атрибуты

Нет.
  

