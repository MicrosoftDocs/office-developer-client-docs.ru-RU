---
title: Элемент CommentEntry (CommentList_Type complexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: b0653622-fa94-4889-68c2-94f3e7a83119
description: Указывает свойства, используемые для идентификации комментария в документе.
ms.openlocfilehash: 6b4f20d632b54e7c96ef8181310e8ffab1abbd0f
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/29/2019
ms.locfileid: "34540114"
---
# <a name="commententry-element-commentlist_type-complextype-visio-xml"></a>Элемент CommentEntry (CommentList_Type complexType) (Visio XML)

Указывает свойства, используемые для идентификации комментария в документе.
  
## <a name="element-information"></a>Сведения об элементе

|||
|:-----|:-----|
|**Тип элемента** <br/> |[CommentEntry_Type](commententry_type-complextypevisio-xml.md) <br/> |
|**Пространство имен** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Файл схемы** <br/> |VisioSchema15.xsd  <br/> |
|**Части документа** <br/> |comments.xml  <br/> |
   
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
|AuthorID  <br/> |xsd:unsignedInt  <br/> |Обязательный  <br/> |Одно основанное на значении, идентифицирует автора.  <br/> |Значения типа xsd:unsignedInt.  <br/> |
|CommentID  <br/> |xsd:unsignedInt  <br/> |Обязательный  <br/> |Уникальное значение, идентифицирует комментарий на странице рисования.  <br/> |Значения типа xsd:unsignedInt.  <br/> |
|Дата  <br/> |xsd:dateTime  <br/> |Обязательный  <br/> |Указывает, когда был создан комментарий.  <br/> |Значения типа xsd:dateTime.  <br/> |
|Готово  <br/> |xsd:boolean  <br/> |необязательный  <br/> |Указывает текущее состояние комментария.  <br/> |Значения типа xsd:boolean.  <br/> |
|EditDate  <br/> |xsd:dateTime  <br/> |необязательный  <br/> |Указывает время последнего изменения комментария.  <br/> |Значения типа xsd:dateTime.  <br/> |
|PageID  <br/> |xsd:unsignedInt  <br/> |Обязательный  <br/> |Значение, определяя страницу рисования, на которую указывает комментарий.  <br/> |Значения типа xsd:unsignedInt.  <br/> |
|ShapeID  <br/> |xsd:unsignedInt  <br/> |необязательный  <br/> |Значение, определяя фигуру, в которую добавлен комментарий. Если shapeID не указан, комментарий ссылается на страницу рисования.  <br/> |Значения типа xsd:unsignedInt.  <br/> |
   

