---
title: Элемент PageSheet (Page_Type complexType) ('Visio XML»)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 99a6549b-099b-1546-cc30-db0010fe3ce1
description: Задает свойства страницы рисунка, связанного с странице документа.
ms.openlocfilehash: ef926af0238b1a44bbaa5c2eae9c0f7c90dc0c08
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19814345"
---
# <a name="pagesheet-element-pagetype-complextype-visio-xml"></a>Элемент PageSheet (Page_Type complexType) ('Visio XML»)

Задает свойства страницы рисунка, связанного с странице документа.
  
## <a name="element-information"></a>Сведения об элементе

|||
|:-----|:-----|
|**Тип элемента** <br/> |[PageSheet_Type](pagesheet_type-complextypevisio-xml.md) <br/> |
|**Пространство имен** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Файл схемы** <br/> |VisioSchema15.xsd  <br/> |
|**Части документа** <br/> |Pages.XML  <br/> |
   
## <a name="definition"></a>Определение

```XML
< xs:element name="PageSheet" type="PageSheet_Type" minOccurs="0" maxOccurs="1" >
</xs:element > 
```

## <a name="elements-and-attributes"></a>Элементы и атрибуты

Если схема определяет специальные требования, такие как **последовательность**, **minOccurs**, **maxOccurs**и **выбора**, обратитесь к разделу определение. 
  
### <a name="parent-elements"></a>Родительские элементы

|**Элемент**|**Тип**|**Описание**|
|:-----|:-----|:-----|
|[Страница](page-element-pages_type-complextypevisio-xml.md) <br/> |[Page_Type](page_type-complextypevisio-xml.md) <br/> |Содержит элементы, определяющие страницы в документе.  <br/> |
   
### <a name="child-elements"></a>Дочерние элементы

Нет.
  
### <a name="attributes"></a>Атрибуты

|**Атрибут**|**Тип**|**Обязательное**|**Описание**|**Возможные значения**|
|:-----|:-----|:-----|:-----|:-----|
|FillStyle  <br/> |XSD:unsignedInt  <br/> |необязательный  <br/> |Задает идентификатор таблицы стилей для наследования заливки форматирования. Оно должно быть значение атрибута **ID** , связанный с **StyleSheet_Type** в документе.  <br/> |Значения типа xsd:unsignedInt.  <br/> |
|Стиль линии  <br/> |XSD:unsignedInt  <br/> |необязательный  <br/> |Задает идентификатор таблицы стилей для наследования форматирование линий. Оно должно быть значение атрибута **ID** , связанный с **StyleSheet_Type** в документе.  <br/> |Значения типа xsd:unsignedInt.  <br/> |
|Стиля текста  <br/> |XSD:unsignedInt  <br/> |необязательный  <br/> |Задает идентификатор таблицы стилей для наследования форматирование текста. Оно должно быть значение атрибута **ID** , связанный с **StyleSheet_Type** в документе.  <br/> |Значения типа xsd:unsignedInt.  <br/> |
|Уникальный идентификатор  <br/> |XSD:String  <br/> |необязательный  <br/> |Уникальный идентификатор элемента в рамках родительского элемента.  <br/> |Значения типа xsd:string.  <br/> |
   

