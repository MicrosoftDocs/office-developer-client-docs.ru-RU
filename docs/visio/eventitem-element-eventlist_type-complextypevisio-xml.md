---
title: Элемент EventItem (EventList_Type complexType) (Visio XML)
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
# <a name="eventitem-element-eventlist_type-complextype-visio-xml"></a>Элемент EventItem (EventList_Type complexType) (Visio XML)

Инкапсулирует код события.
  
## <a name="element-information"></a>Сведения об элементе

|||
|:-----|:-----|
|**Тип элемента** <br/> |[EventItem_Type](eventitem_type-complextypevisio-xml.md) <br/> |
|**Пространство имен** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Файл схемы** <br/> |VisioSchema15.xsd  <br/> |
|**Части документа** <br/> |document.xml  <br/> |
   
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
|[EventList](eventlist-element-visiodocument_type-complextypevisio-xml.md) <br/> |[EventList_Type](eventlist_type-complextypevisio-xml.md) <br/> |Содержит элемент **EventItem** для каждого события, на которое должен реагировать объект.  <br/> |
   
### <a name="child-elements"></a>Дочерние элементы

Нет.
  
### <a name="attributes"></a>Атрибуты

|**Атрибут**|**Тип**|**Обязательный**|**Описание**|**Возможные значения**|
|:-----|:-----|:-----|:-----|:-----|
|Action  <br/> |xsd:unsignedShort  <br/> |Обязательный  <br/> |Указывает код действия родительского **элемента EventItem.**  <br/> |Значения для типа xsd:unsignedShort.  <br/> |
|Включено  <br/> |xsd:boolean  <br/> |необязательный  <br/> |Представляет флаг, указывающий, включено или отключено событие.  <br/> |Значения типа xsd:boolean.  <br/> |
|EventCode  <br/> |xsd:unsignedShort  <br/> |Обязательный  <br/> |Код, указывающий событие, запускающее надстройки.  <br/> |Значения для типа xsd:unsignedShort.  <br/> |
|ID  <br/> |xsd:unsignedInt  <br/> |Обязательный  <br/> |ИД события.  <br/> |Значения типа xsd:unsignedInt.  <br/> |
|Target  <br/> |xsd:string  <br/> |Обязательный  <br/> |Указывает целевой объект события.  <br/> |Значения типа xsd:string.  <br/> |
|TargetArgs  <br/> |xsd:string  <br/> |Обязательный  <br/> |Указывает строку, содержащую аргументы, которые необходимо отправить в целевой объект события.  <br/> |Значения типа xsd:string.  <br/> |
   

