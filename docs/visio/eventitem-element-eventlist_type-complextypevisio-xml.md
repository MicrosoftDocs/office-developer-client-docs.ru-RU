---
title: Элемент EventItem (EventList_Type complexType) ('Visio XML»)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6b347117-a1c1-d090-0d71-ea8528ac70c6
description: Инкапсулирует код события.
ms.openlocfilehash: 6ed539bd6cb4524b2498b636295442bed917c72a
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25394400"
---
# <a name="eventitem-element-eventlisttype-complextype-visio-xml"></a>Элемент EventItem (EventList_Type complexType) ('Visio XML»)

Инкапсулирует код события.
  
## <a name="element-information"></a>Сведения об элементе

|||
|:-----|:-----|
|**Тип элемента** <br/> |[EventItem_Type](eventitem_type-complextypevisio-xml.md) <br/> |
|**Пространство имен** <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Файл схемы** <br/> |VisioSchema15.xsd  <br/> |
|**Части документа** <br/> |Document.XML  <br/> |
   
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
|[EventList](eventlist-element-visiodocument_type-complextypevisio-xml.md) <br/> |[EventList_Type](eventlist_type-complextypevisio-xml.md) <br/> |Содержит элемент **EventItem** для каждого события, к которому должны отвечать объекта.  <br/> |
   
### <a name="child-elements"></a>Дочерние элементы

Нет.
  
### <a name="attributes"></a>Атрибуты

|**Атрибут**|**Тип**|**Обязательный**|**Описание**|**Возможные значения**|
|:-----|:-----|:-----|:-----|:-----|
|Действие  <br/> |xsd:unsignedShort  <br/> |Обязательный  <br/> |Указывает код действия **EventItem** родительского элемента.  <br/> |Значения для типа xsd:unsignedShort.  <br/> |
|Включена  <br/> |XSD:Boolean  <br/> |необязательный  <br/> |Представляет флаг, указывающий, включен ли событие.  <br/> |Значения типа xsd:boolean.  <br/> |
|EventCode  <br/> |xsd:unsignedShort  <br/> |Обязательный  <br/> |Код, указывающий событие, которое запускает надстройки.  <br/> |Значения для типа xsd:unsignedShort.  <br/> |
|ID  <br/> |XSD:unsignedInt  <br/> |Обязательный  <br/> |Идентификатор события.  <br/> |Значения типа xsd:unsignedInt.  <br/> |
|Целевой объект  <br/> |XSD:String  <br/> |Обязательный  <br/> |Указывает целевую события.  <br/> |Значения типа xsd:string.  <br/> |
|TargetArgs  <br/> |XSD:String  <br/> |Обязательный  <br/> |Задает строку, содержащую аргументы для отправки конечного события.  <br/> |Значения типа xsd:string.  <br/> |
   

