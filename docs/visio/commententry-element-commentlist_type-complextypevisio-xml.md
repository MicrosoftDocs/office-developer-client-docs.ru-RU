---
title: Элемент Комментентри (Комментлист_типе complexType) (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: b0653622-fa94-4889-68c2-94f3e7a83119
description: Задает свойства, используемые для идентификации комментария в документе.
ms.openlocfilehash: 79d15b95f986826a4848c2dfbb003255d3482134
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32329542"
---
# <a name="commententry-element-commentlisttype-complextype-visio-xml"></a>Элемент Комментентри (Комментлист_типе complexType) (' Visio XML ')

Задает свойства, используемые для идентификации комментария в документе.
  
## <a name="element-information"></a>Сведения об элементе

|||
|:-----|:-----|
|**Тип элемента** <br/> |[Комментентри_типе](commententry_type-complextypevisio-xml.md) <br/> |
|**Пространство имен** <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
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
|[Комментлист](commentlist-element-comments_type-complextypevisio-xml.md) <br/> |[Комментлист_типе](commentlist_type-complextypevisio-xml.md) <br/> |Задает комментарии в документе.  <br/> |
   
### <a name="child-elements"></a>Дочерние элементы

Нет.
  
### <a name="attributes"></a>Атрибуты

|**Атрибут**|**Тип**|**Обязательный**|**Описание**|**Возможные значения**|
|:-----|:-----|:-----|:-----|:-----|
|Аусорид  <br/> |XSD: Унсигнединт  <br/> |Обязательный  <br/> |Значение с отзначением от единицы, идентифицирующее автора.  <br/> |Значения типа XSD: Унсигнединт.  <br/> |
|Комментид  <br/> |XSD: Унсигнединт  <br/> |Обязательный  <br/> |Уникальное значение, идентифицирующее комментарий на странице документа.  <br/> |Значения типа XSD: Унсигнединт.  <br/> |
|Дата  <br/> |XSD: dateTime  <br/> |Обязательный  <br/> |Указывает, когда был создан комментарий.  <br/> |Значения типа XSD: dateTime.  <br/> |
|Готово  <br/> |XSD: Boolean  <br/> |необязательный  <br/> |Задает текущее состояние комментария.  <br/> |Значения типа XSD: Boolean.  <br/> |
|EditDate  <br/> |XSD: dateTime  <br/> |необязательный  <br/> |Указывает время последнего изменения комментария.  <br/> |Значения типа XSD: dateTime.  <br/> |
|PageID  <br/> |XSD: Унсигнединт  <br/> |Обязательный  <br/> |Значение, идентифицирующее страницу документа, к которой относится комментарий.  <br/> |Значения типа XSD: Унсигнединт.  <br/> |
|Шапеид  <br/> |XSD: Унсигнединт  <br/> |необязательный  <br/> |Значение, определяющее фигуру, в которой находится комментарий. Если Шапеид не указан, комментарий ссылается на страницу документа.  <br/> |Значения типа XSD: Унсигнединт.  <br/> |
   

