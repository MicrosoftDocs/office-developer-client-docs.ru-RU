---
title: CommentEntry_Type complexType (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6d9e99b8-fcd6-f36b-960e-bcf3a23afe04
ms.openlocfilehash: 840f660d72acbda052d4729846d8a26686d82b2a
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/29/2019
ms.locfileid: "34540128"
---
# <a name="commententry_type-complextype-visio-xml"></a>CommentEntry_Type complexType (Visio XML)

## <a name="type-information"></a>Сведения о типе

|||
|:-----|:-----|
|**Пространство имен** <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|**Файл схемы** <br/> |VisioSchema15-2012-06-05.xsd  <br/> |
|**Базовый элемент расширения** <br/> |xsd:string  <br/> |
   
## <a name="definition"></a>Определение

```XML
      <xs:complexType name="CommentEntry_Type">
        <xs:complexContent>
        <xs:extension base="xsd:string">
      
    <xs:attribute name="AuthorID"
  type="xsd:unsignedInt"
     use="required"
    />
    <xs:attribute name="PageID"
  type="xsd:unsignedInt"
     use="required"
    />
    <xs:attribute name="ShapeID"
  type="xsd:unsignedInt"
    />
    <xs:attribute name="Date"
  type="xsd:dateTime"
     use="required"
    />
    <xs:attribute name="EditDate"
  type="xsd:dateTime"
    />
    <xs:attribute name="Done"
  type="xsd:boolean"
    />
    <xs:attribute name="CommentID"
  type="xsd:unsignedInt"
     use="required"
    />
    <xs:attribute name="AutoCommentType"
  type="xsd:unsignedInt"
    />
        </xs:extension>
        </xs:complexContent>
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a>Элементы и атрибуты

Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений. 
  
### <a name="child-elements"></a>Дочерние элементы

Нет.
  
### <a name="attributes"></a>Атрибуты

|**Атрибут**|**Тип**|**Обязательный**|**Описание**|**Возможные значения**|
|:-----|:-----|:-----|:-----|:-----|
|AuthorID  <br/> |xsd:unsignedInt  <br/> |Обязательный  <br/> ||Значения типа xsd:unsignedInt.  <br/> |
|AutoCommentType  <br/> |xsd:unsignedInt  <br/> |необязательный  <br/> ||Значения типа xsd:unsignedInt.  <br/> |
|CommentID  <br/> |xsd:unsignedInt  <br/> |Обязательный  <br/> ||Значения типа xsd:unsignedInt.  <br/> |
|Дата  <br/> |xsd:dateTime  <br/> |Обязательный  <br/> ||Значения типа xsd:dateTime.  <br/> |
|Готово  <br/> |xsd:boolean  <br/> |необязательный  <br/> ||Значения типа xsd:boolean.  <br/> |
|EditDate  <br/> |xsd:dateTime  <br/> |необязательный  <br/> ||Значения типа xsd:dateTime.  <br/> |
|PageID  <br/> |xsd:unsignedInt  <br/> |Обязательный  <br/> ||Значения типа xsd:unsignedInt.  <br/> |
|ShapeID  <br/> |xsd:unsignedInt  <br/> |необязательный  <br/> ||Значения типа xsd:unsignedInt.  <br/> |
   

