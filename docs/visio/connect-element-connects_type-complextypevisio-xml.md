---
title: Подключение (Connects_Type complexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6e1ad47b-ee28-6b9a-f2f9-642e09ca28d4
description: Представляет связь между двумя фигурами в рисунке, например строкой и полем в диаграмме организации.
ms.openlocfilehash: 3450a07e042fc633b9cd4952d9b3ad6b8190ed1e
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/29/2019
ms.locfileid: "34541997"
---
# <a name="connect-element-connects_type-complextype-visio-xml"></a>Подключение (Connects_Type complexType) (Visio XML)

Представляет связь между двумя фигурами в рисунке, например строкой и полем в диаграмме организации.
  
## <a name="element-information"></a>Сведения об элементе

|||
|:-----|:-----|
|**Тип элемента** <br/> |[Connect_Type](connect_type-complextypevisio-xml.md) <br/> |
|**Пространство имен** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Файл схемы** <br/> |VisioSchema15.xsd  <br/> |
|**Части документов** <br/> |page#.xml, master#.xml  <br/> |
   
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
|[Connects](connects-element-pagecontents_type-complextypevisio-xml.md) <br/> |[Connects_Type](connects_type-complextypevisio-xml.md) <br/> |Содержит элемент **Подключение** для каждого подключения между двумя фигурами в рисунке.  <br/> |
   
### <a name="child-elements"></a>Дочерние элементы

Нет.
  
### <a name="attributes"></a>Атрибуты

|**Атрибут**|**Тип**|**Обязательный**|**Описание**|**Возможные значения**|
|:-----|:-----|:-----|:-----|:-----|
|FromCell  <br/> |xsd:string  <br/> |необязательный  <br/> |Ячейка, из которой возникает подключение.  <br/> |Значения типа xsd:string.  <br/> |
|FromPart  <br/> |xsd:int  <br/> |необязательный  <br/> |Часть фигуры, из которой возникает подключение.  <br/> |Значения типа xsd:int.  <br/> |
|FromSheet  <br/> |xsd:unsignedInt  <br/> |Обязательный  <br/> |ID формы, из которой происходит подключение или подключение.  <br/> |Значения типа xsd:unsignedInt.  <br/> |
|ToCell  <br/> |xsd:string  <br/> |необязательный  <br/> |Ячейка, к которой подключено подключение.  <br/> |Значения типа xsd:string.  <br/> |
|ToPart  <br/> |xsd:int  <br/> |необязательный  <br/> |Часть фигуры, к которой выполнено подключение.  <br/> |Значения типа xsd:Int.  <br/> |
|ToSheet  <br/> |xsd:unsignedInt  <br/> |Обязательный  <br/> |ID формы, к которой выполнено одно или несколько подключений.  <br/> |Значения типа xsd:unsignedInt.  <br/> |
   

