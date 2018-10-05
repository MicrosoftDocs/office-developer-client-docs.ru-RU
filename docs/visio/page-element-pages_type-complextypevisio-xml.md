---
title: Элемент страницы (Pages_Type complexType) ('Visio XML»)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6e4ac41f-3855-05d8-e659-02c265b8750c
description: Содержит элементы, определяющие страницы в документе.
ms.openlocfilehash: 800e4ab2c6446ab298747f0492800000bb44cca3
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25398012"
---
# <a name="page-element-pagestype-complextype-visio-xml"></a>Элемент страницы (Pages_Type complexType) ('Visio XML»)

Содержит элементы, определяющие страницы в документе.
  
## <a name="element-information"></a>Сведения об элементе

|||
|:-----|:-----|
|**Тип элемента** <br/> |[Page_Type](page_type-complextypevisio-xml.md) <br/> |
|**Пространство имен** <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Файл схемы** <br/> |VisioSchema15.xsd  <br/> |
|**Части документа** <br/> |Pages.XML  <br/> |
   
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
|[Страницы](pages-elementvisio-xml.md) <br/> |[Pages_Type](pages_type-complextypevisio-xml.md) <br/> |Содержит элементы **страницы** для документа.  <br/> |
   
### <a name="child-elements"></a>Дочерние элементы

|**Элемент**|**Тип**|**Описание**|
|:-----|:-----|:-----|
|[PageSheet](pagesheet-element-page_type-complextypevisio-xml.md) <br/> |[PageSheet_Type](pagesheet_type-complextypevisio-xml.md) <br/> |Содержит элементы, определяющие таблице страницы элемента **страницы** .  <br/> |
   
### <a name="attributes"></a>Атрибуты

|**Атрибут**|**Тип**|**Обязательный**|**Описание**|**Возможные значения**|
|:-----|:-----|:-----|:-----|:-----|
|Общие сведения  <br/> |XSD:Boolean  <br/> |необязательный  <br/> |Флаг, указывающий, является ли страница фоновой страницы.  <br/> |Значения типа xsd:boolean.  <br/> |
|Обратная сторона  <br/> |XSD:unsignedInt  <br/> |необязательный  <br/> |Идентификатор страницы фона на этой странице.  <br/> |Значения типа xsd:unsignedInt.  <br/> |
|ID  <br/> |XSD:unsignedInt  <br/> |Обязательный  <br/> |Уникальный идентификатор элемента в рамках родительского элемента.  <br/> |Значения типа xsd:unsignedInt.  <br/> |
|IsCustomName  <br/> |XSD:Boolean  <br/> |необязательный  <br/> |Указывает, настроен ли имя пользователя.  <br/> |Значения типа xsd:Boolean.  <br/> |
|IsCustomNameU  <br/> |XSD:Boolean  <br/> |необязательный  <br/> |Указывает, настроен ли универсального имени пользователя.  <br/> |Значения типа xsd:Boolean.  <br/> |
|Имя  <br/> |XSD:String  <br/> |необязательный  <br/> |Имя элемента.  <br/> |Значения типа xsd:string.  <br/> |
|NameU  <br/> |XSD:String  <br/> |необязательный  <br/> |Универсальные имя элемента.  <br/> |Значения типа xsd:string.  <br/> |
|ReviewerID  <br/> |XSD:unsignedInt  <br/> |необязательный  <br/> |Идентификатор проверяющий, связанные с наложением разметки.  <br/> |Значения типа xsd:unsignedInt.  <br/> |
|ViewCenterX  <br/> |XSD: double  <br/> |необязательный  <br/> |**ViewCenterX** и **ViewCenterY** укажите центральной точки на странице, новое представление (окно) предполагается, что при его открытии.  <br/> |Значения типа XSD: double.  <br/> |
|ViewCenterY  <br/> |XSD: double  <br/> |необязательный  <br/> |**ViewCenterX** и **ViewCenterY** укажите центральной точки на странице, новое представление (окно) предполагается, что при его открытии.  <br/> |Значения типа XSD: double.  <br/> |
|ViewScale  <br/> |XSD: double  <br/> |необязательный  <br/> |Масштаб по умолчанию для использования при открытии нового представления (окно) страницы. Например 1 = 100%. 1,5 = 150% и т. д.  <br/> |Значения типа XSD: double.  <br/> |
   

