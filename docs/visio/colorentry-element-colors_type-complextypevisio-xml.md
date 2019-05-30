---
title: Элемент Колорентри (Колорс_типе complexType) (XML для Visio)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 3f325ad8-bbc7-28bf-9e48-1fde4fbdbdc0
description: Содержит запись таблицы цветов.
ms.openlocfilehash: f2221d8d32823e5eec4a100eaf4e8f62b914df28
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/29/2019
ms.locfileid: "34540184"
---
# <a name="colorentry-element-colorstype-complextype-visio-xml"></a>Элемент Колорентри (Колорс_типе complexType) (XML для Visio)

Содержит запись таблицы цветов.
  
## <a name="element-information"></a>Сведения об элементе

|||
|:-----|:-----|
|**Тип элемента** <br/> |[Колорентри_типе](colorentry_type-complextypevisio-xml.md) <br/> |
|**Пространство имен** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Файл схемы** <br/> |VisioSchema15. xsd  <br/> |
|**Части документа** <br/> |Document. XML  <br/> |
   
## <a name="definition"></a>Определение

```XML
< xs:element name="ColorEntry" type="ColorEntry_Type" minOccurs="1" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a>Элементы и атрибуты

Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений. 
  
### <a name="parent-elements"></a>Родительские элементы

|**Элемент**|**Тип**|**Описание**|
|:-----|:-----|:-----|
|[Colors](colors-element-visiodocument_type-complextypevisio-xml.md) <br/> |[Колорс_типе](colors_type-complextypevisio-xml.md) <br/> |Содержит таблицу цветов документа.  <br/> |
   
### <a name="child-elements"></a>Дочерние элементы

Нет.
  
### <a name="attributes"></a>Атрибуты

|**Атрибут**|**Тип**|**Обязательный**|**Описание**|**Возможные значения**|
|:-----|:-----|:-----|:-----|:-----|
|IX  <br/> |XSD: Унсигнединт  <br/> |Обязательный  <br/> |Отсчитываемый от нуля индекс элемента в его родительском элементе.  <br/> |Значения типа XSD: Унсигнединт.  <br/> |
|RGB  <br/> |XSD: строка  <br/> |Обязательный  <br/> |Шестнадцатеричное значение записи таблицы цветов.  <br/> |Значения типа String: XSD.  <br/> |
   

