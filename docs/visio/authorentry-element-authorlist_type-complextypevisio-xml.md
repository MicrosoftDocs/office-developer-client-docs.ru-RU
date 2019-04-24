---
title: Элемент Аусорентри (Аусорлист_типе complexType) (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 21ca601b-27f0-b30b-a99e-56359bdf594c
description: Задает свойства, используемые для идентификации автора комментария в документе.
ms.openlocfilehash: 81e5121a953102c7d2e3a5383ae9bc775af4ba41
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32338628"
---
# <a name="authorentry-element-authorlisttype-complextype-visio-xml"></a>Элемент Аусорентри (Аусорлист_типе complexType) (' Visio XML ')

Задает свойства, используемые для идентификации автора комментария в документе.
  
## <a name="element-information"></a>Сведения об элементе

|||
|:-----|:-----|
|**Тип элемента** <br/> |[Аусорентри_типе](authorentry_type-complextypevisio-xml.md) <br/> |
|**Пространство имен** <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
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
|ИД  <br/> |XSD: Унсигнединт  <br/> |Обязательный  <br/> |Значение с отзначением от единицы, идентифицирующее автора.  <br/> |Значения типа XSD: Унсигнединт.  <br/> |
|Инициалы  <br/> |XSD: строка  <br/> |необязательный  <br/> |Инициалы автора.  <br/> |Значения типа String: XSD.  <br/> |
|Имя  <br/> |XSD: строка  <br/> |необязательный  <br/> |Имя автора.  <br/> |Значения типа String: XSD.  <br/> |
|Ресолутионид  <br/> |XSD: строка  <br/> |необязательный  <br/> |Уникальный идентификатор автора.  <br/> |Значения типа String: XSD.  <br/> |
   

