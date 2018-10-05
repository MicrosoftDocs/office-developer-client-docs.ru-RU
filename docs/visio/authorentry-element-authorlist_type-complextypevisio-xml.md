---
title: Элемент AuthorEntry (AuthorList_Type complexType) ('Visio XML»)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 21ca601b-27f0-b30b-a99e-56359bdf594c
description: Задает свойства, используемые для идентификации автора комментария в документ.
ms.openlocfilehash: 81e5121a953102c7d2e3a5383ae9bc775af4ba41
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25386335"
---
# <a name="authorentry-element-authorlisttype-complextype-visio-xml"></a>Элемент AuthorEntry (AuthorList_Type complexType) ('Visio XML»)

Задает свойства, используемые для идентификации автора комментария в документ.
  
## <a name="element-information"></a>Сведения об элементе

|||
|:-----|:-----|
|**Тип элемента** <br/> |[AuthorEntry_Type](authorentry_type-complextypevisio-xml.md) <br/> |
|**Пространство имен** <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Файл схемы** <br/> |VisioSchema15.xsd  <br/> |
|**Части документа** <br/> |Comments.XML  <br/> |
   
## <a name="definition"></a>Определение

```XML
< xs:element name="AuthorEntry" type="AuthorEntry_Type" minOccurs="0" maxOccurs="unbounded" >
< /xs:element >
```

## <a name="elements-and-attributes"></a>Элементы и атрибуты

Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений. 
  
### <a name="parent-elements"></a>Родительские элементы

|**Элемент**|**Тип**|**Описание**|
|:-----|:-----|:-----|
|[AuthorList](authorlist-element-comments_type-complextypevisio-xml.md) <br/> |[AuthorList_Type](authorlist_type-complextypevisio-xml.md) <br/> |Задает авторы документа.  <br/> |
   
### <a name="child-elements"></a>Дочерние элементы

Нет.
  
### <a name="attributes"></a>Атрибуты

|**Атрибут**|**Тип**|**Обязательный**|**Описание**|**Возможные значения**|
|:-----|:-----|:-----|:-----|:-----|
|ID  <br/> |XSD:unsignedInt  <br/> |Обязательный  <br/> |На основе одно значение, идентифицирующее автора.  <br/> |Значения типа xsd:unsignedInt.  <br/> |
|Initials  <br/> |XSD:String  <br/> |необязательный  <br/> |Инициалы автора.  <br/> |Значения типа xsd:string.  <br/> |
|Имя  <br/> |XSD:String  <br/> |необязательный  <br/> |Имя автора.  <br/> |Значения типа xsd:string.  <br/> |
|ResolutionID  <br/> |XSD:String  <br/> |необязательный  <br/> |Уникальный идентификатор автора.  <br/> |Значения типа xsd:string.  <br/> |
   

