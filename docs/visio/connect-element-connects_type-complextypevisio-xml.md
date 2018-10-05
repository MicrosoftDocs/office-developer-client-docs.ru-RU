---
title: Подключение элемента (Connects_Type complexType) ('Visio XML»)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6e1ad47b-ee28-6b9a-f2f9-642e09ca28d4
description: Представляет подключение между двумя фигурами в документе, такие как строку и поле в организационной диаграммы.
ms.openlocfilehash: 82413f44f05f2ec6140e2b3981b7a1e8435becb0
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25399321"
---
# <a name="connect-element-connectstype-complextype-visio-xml"></a>Подключение элемента (Connects_Type complexType) ('Visio XML»)

Представляет подключение между двумя фигурами в документе, такие как строку и поле в организационной диаграммы.
  
## <a name="element-information"></a>Сведения об элементе

|||
|:-----|:-----|
|**Тип элемента** <br/> |[Connect_Type](connect_type-complextypevisio-xml.md) <br/> |
|**Пространство имен** <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Файл схемы** <br/> |VisioSchema15.xsd  <br/> |
|**Части документа** <br/> |страницы # .xml, главные # .xml  <br/> |
   
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
|[Осуществляет подключение](connects-element-pagecontents_type-complextypevisio-xml.md) <br/> |[Connects_Type](connects_type-complextypevisio-xml.md) <br/> |Содержит элемент **подключение** для каждого подключения между двумя фигурами в документе.  <br/> |
   
### <a name="child-elements"></a>Дочерние элементы

Нет.
  
### <a name="attributes"></a>Атрибуты

|**Атрибут**|**Тип**|**Обязательный**|**Описание**|**Возможные значения**|
|:-----|:-----|:-----|:-----|:-----|
|FromCell  <br/> |XSD:String  <br/> |необязательный  <br/> |Ячейка, из которого создается подключение.  <br/> |Значения типа xsd:string.  <br/> |
|FromPart  <br/> |XSD: int  <br/> |необязательный  <br/> |Часть фигуры, из которого создается подключение.  <br/> |Значения типа XSD: int.  <br/> |
|FromSheet  <br/> |XSD:unsignedInt  <br/> |Обязательный  <br/> |Идентификатор фигуры, из которого создаются и подключения.  <br/> |Значения типа xsd:unsignedInt.  <br/> |
|ToCell  <br/> |XSD:String  <br/> |необязательный  <br/> |Ячейка, к которому выполняется подключение.  <br/> |Значения типа xsd:string.  <br/> |
|ToPart  <br/> |XSD: int  <br/> |необязательный  <br/> |Часть фигуры, к которому выполняется подключение.  <br/> |Значения типа XSD: int.  <br/> |
|ToSheet  <br/> |XSD:unsignedInt  <br/> |Обязательный  <br/> |Идентификатор фигуры, к которой один или несколько подключения.  <br/> |Значения типа xsd:unsignedInt.  <br/> |
   

