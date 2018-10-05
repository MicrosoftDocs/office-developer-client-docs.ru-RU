---
title: Элемент CommentEntry (CommentList_Type complexType) ('Visio XML»)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: b0653622-fa94-4889-68c2-94f3e7a83119
description: Задает свойства, используемые для идентификации комментария в документ.
ms.openlocfilehash: 79d15b95f986826a4848c2dfbb003255d3482134
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25397046"
---
# <a name="commententry-element-commentlisttype-complextype-visio-xml"></a>Элемент CommentEntry (CommentList_Type complexType) ('Visio XML»)

Задает свойства, используемые для идентификации комментария в документ.
  
## <a name="element-information"></a>Сведения об элементе

|||
|:-----|:-----|
|**Тип элемента** <br/> |[CommentEntry_Type](commententry_type-complextypevisio-xml.md) <br/> |
|**Пространство имен** <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Файл схемы** <br/> |VisioSchema15.xsd  <br/> |
|**Части документа** <br/> |Comments.XML  <br/> |
   
## <a name="definition"></a>Определение

```XML
< xs:element name="CommentEntry" type="CommentEntry_Type" minOccurs="0" maxOccurs="unbounded" >
< /xs:element >
```

## <a name="elements-and-attributes"></a>Элементы и атрибуты

Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений. 
  
### <a name="parent-elements"></a>Родительские элементы

|**Элемент**|**Тип**|**Описание**|
|:-----|:-----|:-----|
|[CommentList](commentlist-element-comments_type-complextypevisio-xml.md) <br/> |[CommentList_Type](commentlist_type-complextypevisio-xml.md) <br/> |Указывает комментарии в документе.  <br/> |
   
### <a name="child-elements"></a>Дочерние элементы

Нет.
  
### <a name="attributes"></a>Атрибуты

|**Атрибут**|**Тип**|**Обязательный**|**Описание**|**Возможные значения**|
|:-----|:-----|:-----|:-----|:-----|
|AuthorID  <br/> |XSD:unsignedInt  <br/> |Обязательный  <br/> |На основе одно значение, идентифицирующее автора.  <br/> |Значения типа xsd:unsignedInt.  <br/> |
|CommentID  <br/> |XSD:unsignedInt  <br/> |Обязательный  <br/> |Уникальное значение, определяющее комментария в страницу документа.  <br/> |Значения типа xsd:unsignedInt.  <br/> |
|Date  <br/> |XSD: DateTime  <br/> |Обязательный  <br/> |Указывает время создания комментария.  <br/> |Значения типа XSD: DateTime.  <br/> |
|done  <br/> |XSD:Boolean  <br/> |необязательный  <br/> |Указывает текущее состояние комментария.  <br/> |Значения типа xsd:boolean.  <br/> |
|EditDate  <br/> |XSD: DateTime  <br/> |необязательный  <br/> |Указывает время последнего изменения комментария.  <br/> |Значения типа XSD: DateTime.  <br/> |
|PageID  <br/> |XSD:unsignedInt  <br/> |Обязательный  <br/> |Значение, указывающее странице документа комментарий — на.  <br/> |Значения типа xsd:unsignedInt.  <br/> |
|ShapeID  <br/> |XSD:unsignedInt  <br/> |необязательный  <br/> |Значение, указывающее фигуры комментария включен. Если не ShapeID не указан, то comment указывает на странице документа.  <br/> |Значения типа xsd:unsignedInt.  <br/> |
   

