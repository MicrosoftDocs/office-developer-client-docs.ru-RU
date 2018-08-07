---
title: Элемент CommentEntry (CommentList_Type complexType) ('Visio XML»)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: b0653622-fa94-4889-68c2-94f3e7a83119
description: Задает свойства, используемые для идентификации комментария в документ.
ms.openlocfilehash: b2ab1925c8b3b9a9c2d67ac48c1db1768f5916b2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19813420"
---
# <a name="commententry-element-commentlisttype-complextype-visio-xml"></a>Элемент CommentEntry (CommentList_Type complexType) ('Visio XML»)

Задает свойства, используемые для идентификации комментария в документ.
  
## <a name="element-information"></a>Сведения об элементе

|||
|:-----|:-----|
|**Тип элемента** <br/> |[CommentEntry_Type](commententry_type-complextypevisio-xml.md) <br/> |
|**Пространство имен** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Файл схемы** <br/> |VisioSchema15.xsd  <br/> |
|**Части документа** <br/> |Comments.XML  <br/> |
   
## <a name="definition"></a>Определение

```XML
< xs:element name="CommentEntry" type="CommentEntry_Type" minOccurs="0" maxOccurs="unbounded" >
< /xs:element >
```

## <a name="elements-and-attributes"></a>Элементы и атрибуты

Если схема определяет специальные требования, такие как **последовательность**, **minOccurs**, **maxOccurs**и **выбора**, обратитесь к разделу определение. 
  
### <a name="parent-elements"></a>Родительские элементы

|**Элемент**|**Тип**|**Описание**|
|:-----|:-----|:-----|
|[CommentList](commentlist-element-comments_type-complextypevisio-xml.md) <br/> |[CommentList_Type](commentlist_type-complextypevisio-xml.md) <br/> |Указывает комментарии в документе.  <br/> |
   
### <a name="child-elements"></a>Дочерние элементы

Нет.
  
### <a name="attributes"></a>Атрибуты

|**Атрибут**|**Тип**|**Обязательное**|**Описание**|**Возможные значения**|
|:-----|:-----|:-----|:-----|:-----|
|AuthorID  <br/> |XSD:unsignedInt  <br/> |Обязательный  <br/> |На основе одно значение, идентифицирующее автора.  <br/> |Значения типа xsd:unsignedInt.  <br/> |
|CommentID  <br/> |XSD:unsignedInt  <br/> |Обязательный  <br/> |Уникальное значение, определяющее комментария в страницу документа.  <br/> |Значения типа xsd:unsignedInt.  <br/> |
|Date  <br/> |XSD: DateTime  <br/> |Обязательный  <br/> |Указывает время создания комментария.  <br/> |Значения типа XSD: DateTime.  <br/> |
|done  <br/> |XSD:Boolean  <br/> |необязательный  <br/> |Указывает текущее состояние комментария.  <br/> |Значения типа xsd:boolean.  <br/> |
|EditDate  <br/> |XSD: DateTime  <br/> |необязательный  <br/> |Указывает время последнего изменения комментария.  <br/> |Значения типа XSD: DateTime.  <br/> |
|PageID  <br/> |XSD:unsignedInt  <br/> |Обязательный  <br/> |Значение, указывающее странице документа комментарий — на.  <br/> |Значения типа xsd:unsignedInt.  <br/> |
|ShapeID  <br/> |XSD:unsignedInt  <br/> |необязательный  <br/> |Значение, указывающее фигуры комментария включен. Если не ShapeID не указан, то comment указывает на странице документа.  <br/> |Значения типа xsd:unsignedInt.  <br/> |
   

