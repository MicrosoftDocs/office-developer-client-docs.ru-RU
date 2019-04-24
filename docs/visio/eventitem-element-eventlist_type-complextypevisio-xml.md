---
title: Элемент Евентитем (Евентлист_типе complexType) (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6b347117-a1c1-d090-0d71-ea8528ac70c6
description: Инкапсулирует код события.
ms.openlocfilehash: 6ed539bd6cb4524b2498b636295442bed917c72a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32337200"
---
# <a name="eventitem-element-eventlisttype-complextype-visio-xml"></a>Элемент Евентитем (Евентлист_типе complexType) (' Visio XML ')

Инкапсулирует код события.
  
## <a name="element-information"></a>Сведения об элементе

|||
|:-----|:-----|
|**Тип элемента** <br/> |[Евентитем_типе](eventitem_type-complextypevisio-xml.md) <br/> |
|**Пространство имен** <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
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
|Действие  <br/> |xsd:unsignedShort  <br/> |Обязательный  <br/> |Задает код действия родительского элемента **евентитем** .  <br/> |Значения для типа xsd:unsignedShort.  <br/> |
|Включена  <br/> |XSD: Boolean  <br/> |необязательный  <br/> |Представляет флаг, указывающий, включено или отключено событие.  <br/> |Значения типа XSD: Boolean.  <br/> |
|Евенткоде  <br/> |xsd:unsignedShort  <br/> |Обязательный  <br/> |Код, указывающий на событие, которое запускает надстройку.  <br/> |Значения для типа xsd:unsignedShort.  <br/> |
|ИД  <br/> |XSD: Унсигнединт  <br/> |Обязательный  <br/> |Идентификатор события.  <br/> |Значения типа XSD: Унсигнединт.  <br/> |
|Target  <br/> |XSD: строка  <br/> |Обязательный  <br/> |Указывает целевой объект события.  <br/> |Значения типа String: XSD.  <br/> |
|TargetArgs  <br/> |XSD: строка  <br/> |Обязательный  <br/> |Указывает строку, содержащую аргументы, которые необходимо отправить в цель события.  <br/> |Значения типа String: XSD.  <br/> |
   

