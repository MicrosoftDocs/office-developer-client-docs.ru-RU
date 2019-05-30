---
title: Элемент Connect (Коннектс_типе complexType) (XML для Visio)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6e1ad47b-ee28-6b9a-f2f9-642e09ca28d4
description: Представляет соединение между двумя фигурами в документе, например линии и поле на организационной диаграмме.
ms.openlocfilehash: 3450a07e042fc633b9cd4952d9b3ad6b8190ed1e
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/29/2019
ms.locfileid: "34541997"
---
# <a name="connect-element-connectstype-complextype-visio-xml"></a>Элемент Connect (Коннектс_типе complexType) (XML для Visio)

Представляет соединение между двумя фигурами в документе, например линии и поле на организационной диаграмме.
  
## <a name="element-information"></a>Сведения об элементе

|||
|:-----|:-----|
|**Тип элемента** <br/> |[Коннект_типе](connect_type-complextypevisio-xml.md) <br/> |
|**Пространство имен** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Файл схемы** <br/> |VisioSchema15. xsd  <br/> |
|**Части документа** <br/> |страница #. XML, Master #. XML  <br/> |
   
## <a name="definition"></a>Определение

```XML
< xs:element name="Connect" type="Connect_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a>Элементы и атрибуты

Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений. 
  
### <a name="parent-elements"></a>Родительские элементы

|**Элемент**|**Тип**|**Описание**|
|:-----|:-----|:-----|
|[Connects](connects-element-pagecontents_type-complextypevisio-xml.md) <br/> |[Коннектс_типе](connects_type-complextypevisio-xml.md) <br/> |Содержит элемент **Connect** для каждого подключения между двумя фигурами в документе.  <br/> |
   
### <a name="child-elements"></a>Дочерние элементы

Нет.
  
### <a name="attributes"></a>Атрибуты

|**Атрибут**|**Тип**|**Обязательный**|**Описание**|**Возможные значения**|
|:-----|:-----|:-----|:-----|:-----|
|FromCell  <br/> |XSD: строка  <br/> |необязательный  <br/> |Ячейка, из которой исходит подключение.  <br/> |Значения типа String: XSD.  <br/> |
|FromPart  <br/> |XSD: int  <br/> |необязательный  <br/> |Часть фигуры, из которой происходит подключение.  <br/> |Значения типа XSD: int.  <br/> |
|FromSheet  <br/> |XSD: Унсигнединт  <br/> |Обязательный  <br/> |ИДЕНТИФИКАТОР фигуры, из которой происходят подключения.  <br/> |Значения типа XSD: Унсигнединт.  <br/> |
|ToCell  <br/> |XSD: строка  <br/> |необязательный  <br/> |Ячейка, к которой выполняется подключение.  <br/> |Значения типа String: XSD.  <br/> |
|ToPart  <br/> |XSD: int  <br/> |необязательный  <br/> |Часть фигуры, к которой выполняется подключение.  <br/> |Значения типа XSD: int.  <br/> |
|ToSheet  <br/> |XSD: Унсигнединт  <br/> |Обязательный  <br/> |ИДЕНТИФИКАТОР фигуры, для которой выполняется одно или несколько подключений.  <br/> |Значения типа XSD: Унсигнединт.  <br/> |
   

