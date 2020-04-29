---
title: Элемент Комментентри (CommentList_Type complexType) (XML для Visio)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: b0653622-fa94-4889-68c2-94f3e7a83119
description: Задает свойства, используемые для идентификации комментария в документе.
ms.openlocfilehash: 6b4f20d632b54e7c96ef8181310e8ffab1abbd0f
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/29/2019
ms.locfileid: "34540114"
---
# <a name="commententry-element-commentlist_type-complextype-visio-xml"></a>Элемент Комментентри (CommentList_Type complexType) (XML для Visio)

Задает свойства, используемые для идентификации комментария в документе.
  
## <a name="element-information"></a>Сведения об элементе

|||
|:-----|:-----|
|**Тип элемента** <br/> |[CommentEntry_Type](commententry_type-complextypevisio-xml.md) <br/> |
|**Пространство имен** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Файл схемы** <br/> |VisioSchema15. xsd  <br/> |
|**Части документа** <br/> |Comments. XML  <br/> |
   
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
|[комментлист](commentlist-element-comments_type-complextypevisio-xml.md) <br/> |[CommentList_Type](commentlist_type-complextypevisio-xml.md) <br/> |Задает комментарии в документе.  <br/> |
   
### <a name="child-elements"></a>Дочерние элементы

Нет.
  
### <a name="attributes"></a>Атрибуты

|**Атрибут**|**Тип**|**Обязательный**|**Описание**|**Возможные значения**|
|:-----|:-----|:-----|:-----|:-----|
|аусорид  <br/> |XSD: Унсигнединт  <br/> |Обязательный  <br/> |Значение с отзначением от единицы, идентифицирующее автора.  <br/> |Значения типа XSD: Унсигнединт.  <br/> |
|комментид  <br/> |XSD: Унсигнединт  <br/> |Обязательный  <br/> |Уникальное значение, идентифицирующее комментарий на странице документа.  <br/> |Значения типа XSD: Унсигнединт.  <br/> |
|Дата  <br/> |XSD: dateTime  <br/> |Обязательный  <br/> |Указывает, когда был создан комментарий.  <br/> |Значения типа XSD: dateTime.  <br/> |
|Готово  <br/> |XSD: Boolean  <br/> |необязательный  <br/> |Задает текущее состояние комментария.  <br/> |Значения типа XSD: Boolean.  <br/> |
|EditDate  <br/> |XSD: dateTime  <br/> |необязательный  <br/> |Указывает время последнего изменения комментария.  <br/> |Значения типа XSD: dateTime.  <br/> |
|PageID  <br/> |XSD: Унсигнединт  <br/> |Обязательный  <br/> |Значение, идентифицирующее страницу документа, к которой относится комментарий.  <br/> |Значения типа XSD: Унсигнединт.  <br/> |
|шапеид  <br/> |XSD: Унсигнединт  <br/> |необязательный  <br/> |Значение, определяющее фигуру, в которой находится комментарий. Если Шапеид не указан, комментарий ссылается на страницу документа.  <br/> |Значения типа XSD: Унсигнединт.  <br/> |
   

