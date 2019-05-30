---
title: Элемент Page (Пажес_типе complexType) (XML для Visio)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6e4ac41f-3855-05d8-e659-02c265b8750c
description: Содержит элементы, определяющие страницу в документе.
ms.openlocfilehash: f32cf3ed7bbf1e68ddca3fc8f5a1c50ce45fe73e
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/29/2019
ms.locfileid: "34538027"
---
# <a name="page-element-pagestype-complextype-visio-xml"></a>Элемент Page (Пажес_типе complexType) (XML для Visio)

Содержит элементы, определяющие страницу в документе.
  
## <a name="element-information"></a>Сведения об элементе

|||
|:-----|:-----|
|**Тип элемента** <br/> |[Паже_типе](page_type-complextypevisio-xml.md) <br/> |
|**Пространство имен** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Файл схемы** <br/> |VisioSchema15. xsd  <br/> |
|**Части документа** <br/> |Pages. XML  <br/> |
   
## <a name="definition"></a>Определение

```XML
< xs:element name="Page" type="Page_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a>Элементы и атрибуты

Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений. 
  
### <a name="parent-elements"></a>Родительские элементы

|**Элемент**|**Тип**|**Описание**|
|:-----|:-----|:-----|
|[Pages](pages-elementvisio-xml.md) <br/> |[Пажес_типе](pages_type-complextypevisio-xml.md) <br/> |Содержит элементы **страницы** для документа.  <br/> |
   
### <a name="child-elements"></a>Дочерние элементы

|**Элемент**|**Тип**|**Описание**|
|:-----|:-----|:-----|
|[PageSheet](pagesheet-element-page_type-complextypevisio-xml.md) <br/> |[Пажешит_типе](pagesheet_type-complextypevisio-xml.md) <br/> |Содержит элементы, определяющие лист страницы для элемента **Page** .  <br/> |
   
### <a name="attributes"></a>Атрибуты

|**Атрибут**|**Тип**|**Обязательный**|**Описание**|**Возможные значения**|
|:-----|:-----|:-----|:-----|:-----|
|Фон  <br/> |XSD: Boolean  <br/> |необязательный  <br/> |Флаг, указывающий, является ли страница страницей фона.  <br/> |Значения типа XSD: Boolean.  <br/> |
|BackPage  <br/> |XSD: Унсигнединт  <br/> |необязательный  <br/> |Идентификатор фоновой страницы этой страницы.  <br/> |Значения типа XSD: Унсигнединт.  <br/> |
|ID  <br/> |XSD: Унсигнединт  <br/> |Обязательный  <br/> |Уникальный идентификатор элемента в родительском элементе.  <br/> |Значения типа XSD: Унсигнединт.  <br/> |
|Искустомнаме  <br/> |XSD: Boolean  <br/> |необязательный  <br/> |Указывает, настроено ли имя пользователем.  <br/> |Значения типа XSD: Boolean.  <br/> |
|Искустомнамеу  <br/> |XSD: Boolean  <br/> |необязательный  <br/> |Указывает, настроено ли универсальное имя пользователем.  <br/> |Значения типа XSD: Boolean.  <br/> |
|Имя  <br/> |XSD: строка  <br/> |необязательный  <br/> |Имя элемента.  <br/> |Значения типа String: XSD.  <br/> |
|NameU  <br/> |XSD: строка  <br/> |необязательный  <br/> |Универсальное имя элемента.  <br/> |Значения типа String: XSD.  <br/> |
|ReviewerID  <br/> |XSD: Унсигнединт  <br/> |необязательный  <br/> |Идентификатор проверяющего, связанный с наложением разметки.  <br/> |Значения типа XSD: Унсигнединт.  <br/> |
|Виевцентеркс  <br/> |XSD: Double  <br/> |необязательный  <br/> |**Виевцентеркс** и **виевцентери** указывают центральную точку на странице, которая предполагается при открытии нового представления (окна).  <br/> |Значения типа XSD: Double.  <br/> |
|Виевцентери  <br/> |XSD: Double  <br/> |необязательный  <br/> |**Виевцентеркс** и **виевцентери** указывают центральную точку на странице, которая предполагается при открытии нового представления (окна).  <br/> |Значения типа XSD: Double.  <br/> |
|Виевскале  <br/> |XSD: Double  <br/> |необязательный  <br/> |Фактор увеличения по умолчанию, используемый при открытии нового представления (окна) страницы. Например, 1 = 100%; 1,5 = 150% и т. д.  <br/> |Значения типа XSD: Double.  <br/> |
   

