---
title: Элемент Евентитем (Евентлист_типе complexType) (XML для Visio)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6b347117-a1c1-d090-0d71-ea8528ac70c6
description: Инкапсулирует код события.
ms.openlocfilehash: 0db88a175d3e0330cb648f870559d9d2bd4dc1d8
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/29/2019
ms.locfileid: "34541843"
---
# <a name="eventitem-element-eventlisttype-complextype-visio-xml"></a>Элемент Евентитем (Евентлист_типе complexType) (XML для Visio)

Инкапсулирует код события.
  
## <a name="element-information"></a>Сведения об элементе

|||
|:-----|:-----|
|**Тип элемента** <br/> |[Евентитем_типе](eventitem_type-complextypevisio-xml.md) <br/> |
|**Пространство имен** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Файл схемы** <br/> |VisioSchema15. xsd  <br/> |
|**Части документа** <br/> |Document. XML  <br/> |
   
## <a name="definition"></a>Определение

```XML
< xs:element name="EventItem" type="EventItem_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a>Элементы и атрибуты

Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений. 
  
### <a name="parent-elements"></a>Родительские элементы

|**Элемент**|**Тип**|**Описание**|
|:-----|:-----|:-----|
|[EventList](eventlist-element-visiodocument_type-complextypevisio-xml.md) <br/> |[Евентлист_типе](eventlist_type-complextypevisio-xml.md) <br/> |Содержит элемент **евентитем** для каждого события, на которое должен отвечать объект.  <br/> |
   
### <a name="child-elements"></a>Дочерние элементы

Нет.
  
### <a name="attributes"></a>Атрибуты

|**Атрибут**|**Тип**|**Обязательный**|**Описание**|**Возможные значения**|
|:-----|:-----|:-----|:-----|:-----|
|Action  <br/> |xsd:unsignedShort  <br/> |Обязательный  <br/> |Задает код действия родительского элемента **евентитем** .  <br/> |Значения для типа xsd:unsignedShort.  <br/> |
|Включен  <br/> |XSD: Boolean  <br/> |необязательный  <br/> |Представляет флаг, указывающий, включено или отключено событие.  <br/> |Значения типа XSD: Boolean.  <br/> |
|Евенткоде  <br/> |xsd:unsignedShort  <br/> |Обязательный  <br/> |Код, указывающий на событие, которое запускает надстройку.  <br/> |Значения для типа xsd:unsignedShort.  <br/> |
|ID  <br/> |XSD: Унсигнединт  <br/> |Обязательный  <br/> |Идентификатор события.  <br/> |Значения типа XSD: Унсигнединт.  <br/> |
|Target  <br/> |XSD: строка  <br/> |Обязательный  <br/> |Указывает целевой объект события.  <br/> |Значения типа String: XSD.  <br/> |
|TargetArgs  <br/> |XSD: строка  <br/> |Обязательный  <br/> |Указывает строку, содержащую аргументы, которые необходимо отправить в цель события.  <br/> |Значения типа String: XSD.  <br/> |
   

