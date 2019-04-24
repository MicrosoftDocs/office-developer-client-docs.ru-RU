---
title: Элемент Комментлист (Комментс_типе complexType) (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 49fee70d-6556-887b-003f-4f56916d541d
description: Задает комментарии в документе.
ms.openlocfilehash: 424eb10ab356fc2b7f07a1fae27a8e2715e3f2fd
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359432"
---
# <a name="commentlist-element-commentstype-complextype-visio-xml"></a>Элемент Комментлист (Комментс_типе complexType) (' Visio XML ')

Задает комментарии в документе.
  
## <a name="element-information"></a>Сведения об элементе

|||
|:-----|:-----|
|**Тип элемента** <br/> |[Комментлист_типе](commentlist_type-complextypevisio-xml.md) <br/> |
|**Пространство имен** <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Файл схемы** <br/> |VisioSchema15. xsd  <br/> |
|**Части документа** <br/> |Comments. XML  <br/> |
   
## <a name="definition"></a>Определение

```XML
< xs:element name="CommentList" type="CommentList_Type" minOccurs="0" maxOccurs="1" >
< /xs:element >
```

## <a name="elements-and-attributes"></a>Элементы и атрибуты

Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений. 
  
### <a name="parent-elements"></a>Родительские элементы

|**Элемент**|**Тип**|**Описание**|
|:-----|:-----|:-----|
|[Comments](comments-element-comments_type-complextypevisio-xml.md) <br/> |[Комментс_типе](comments_type-complextypevisio-xml.md) <br/> |Задает свойства, используемые для идентификации авторов и комментариев в документе.  <br/> |
   
### <a name="child-elements"></a>Дочерние элементы

|**Элемент**|**Тип**|**Описание**|
|:-----|:-----|:-----|
|[Комментентри](commententry-element-commentlist_type-complextypevisio-xml.md) <br/> |[Комментентри_типе](commententry_type-complextypevisio-xml.md) <br/> |Задает свойства, используемые для идентификации комментария в документе.  <br/> |
   
### <a name="attributes"></a>Атрибуты

Нет.
  

