---
title: Элемент PageSheet (Master_Type complexType) ('Visio XML»)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 824fbeb0-1a2f-35a0-50e3-c57143dc21ab
description: Задает свойства страницы рисунка, связанного с шаблоном.
ms.openlocfilehash: ab20cfe4561cd5fd0eeb6edad0b3a608428b0e8e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19814385"
---
# <a name="pagesheet-element-mastertype-complextype-visio-xml"></a>Элемент PageSheet (Master_Type complexType) ('Visio XML»)

Задает свойства страницы рисунка, связанного с шаблоном.
  
## <a name="element-information"></a>Сведения об элементе

|||
|:-----|:-----|
|**Тип элемента** <br/> |[PageSheet_Type](pagesheet_type-complextypevisio-xml.md) <br/> |
|**Пространство имен** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Файл схемы** <br/> |VisioSchema15.xsd  <br/> |
|**Части документа** <br/> |Masters.XML  <br/> |
   
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
|[Master](master-element-masters_type-complextypevisio-xml.md) <br/> |[Master_Type](master_type-complextypevisio-xml.md) <br/> |Задает шаблон документа.  <br/> |
   
### <a name="child-elements"></a>Дочерние элементы

Нет.
  
### <a name="attributes"></a>Атрибуты

|**Атрибут**|**Тип**|**Обязательное**|**Описание**|**Возможные значения**|
|:-----|:-----|:-----|:-----|:-----|
|FillStyle  <br/> |XSD:unsignedInt  <br/> |необязательный  <br/> |Задает идентификатор таблицы стилей для наследования заливки форматирования. Оно должно быть значение атрибута **ID** , связанный с **StyleSheet_Type** в документе.  <br/> |Значения типа xsd:unsignedInt.  <br/> |
|Стиль линии  <br/> |XSD:unsignedInt  <br/> |необязательный  <br/> |Задает идентификатор таблицы стилей для наследования форматирование линий. Оно должно быть значение атрибута **ID** , связанный с **StyleSheet_Type** в документе.  <br/> |Значения типа xsd:unsignedInt.  <br/> |
|Стиля текста  <br/> |XSD:unsignedInt  <br/> |необязательный  <br/> |Задает идентификатор таблицы стилей для наследования форматирование текста. Оно должно быть значение атрибута **ID** , связанный с **StyleSheet_Type** в документе.  <br/> |Значения типа xsd:unsignedInt.  <br/> |
|Уникальный идентификатор  <br/> |XSD:String  <br/> |необязательный  <br/> |Уникальный идентификатор элемента в рамках родительского элемента.  <br/> |Значения типа xsd:string.  <br/> |
   

