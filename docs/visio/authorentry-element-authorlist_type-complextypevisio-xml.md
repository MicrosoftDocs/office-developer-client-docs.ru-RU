---
title: Элемент Аусорентри (Аусорлист_типе complexType) (XML для Visio)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 21ca601b-27f0-b30b-a99e-56359bdf594c
description: Задает свойства, используемые для идентификации автора комментария в документе.
ms.openlocfilehash: 29dc4459d0df3b914d61140cb2c5f33cc3e1306e
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/29/2019
ms.locfileid: "34537908"
---
# <a name="authorentry-element-authorlisttype-complextype-visio-xml"></a>Элемент Аусорентри (Аусорлист_типе complexType) (XML для Visio)

Задает свойства, используемые для идентификации автора комментария в документе.
  
## <a name="element-information"></a>Сведения об элементе

|||
|:-----|:-----|
|**Тип элемента** <br/> |[Аусорентри_типе](authorentry_type-complextypevisio-xml.md) <br/> |
|**Пространство имен** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Файл схемы** <br/> |VisioSchema15. xsd  <br/> |
|**Части документа** <br/> |Comments. XML  <br/> |
   
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
|[Аусорлист](authorlist-element-comments_type-complextypevisio-xml.md) <br/> |[Аусорлист_типе](authorlist_type-complextypevisio-xml.md) <br/> |Указывает авторов в документе.  <br/> |
   
### <a name="child-elements"></a>Дочерние элементы

Нет.
  
### <a name="attributes"></a>Атрибуты

|**Атрибут**|**Тип**|**Обязательный**|**Описание**|**Возможные значения**|
|:-----|:-----|:-----|:-----|:-----|
|ID  <br/> |XSD: Унсигнединт  <br/> |Обязательный  <br/> |Значение с отзначением от единицы, идентифицирующее автора.  <br/> |Значения типа XSD: Унсигнединт.  <br/> |
|Инициалы  <br/> |XSD: строка  <br/> |необязательный  <br/> |Инициалы автора.  <br/> |Значения типа String: XSD.  <br/> |
|Имя  <br/> |XSD: строка  <br/> |необязательный  <br/> |Имя автора.  <br/> |Значения типа String: XSD.  <br/> |
|Ресолутионид  <br/> |XSD: строка  <br/> |необязательный  <br/> |Уникальный идентификатор автора.  <br/> |Значения типа String: XSD.  <br/> |
   

