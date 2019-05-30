---
title: Элемент Connection (Датаконнектионс_типе complexType) (XML для Visio)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6aab8be3-b236-029b-1df3-b6860d4f4586
description: Создает абстракцию для связи между одним или несколькими элементами записи данных и источником данных, не относящимся к XML.
ms.openlocfilehash: 619f3b4e3d9c93831cc23bc38fba3670107b2b51
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/29/2019
ms.locfileid: "34538405"
---
# <a name="dataconnection-element-dataconnectionstype-complextype-visio-xml"></a>Элемент Connection (Датаконнектионс_типе complexType) (XML для Visio)

Создает абстракцию для связи между одним или несколькими элементами **записи** данных и источником данных, не относящимся к XML. 
  
## <a name="element-information"></a>Сведения об элементе

|||
|:-----|:-----|
|**Тип элемента** <br/> |[Датаконнектион_типе](dataconnection_type-complextypevisio-xml.md) <br/> |
|**Пространство имен** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Файл схемы** <br/> |VisioSchema15. xsd  <br/> |
|**Части документа** <br/> |Connections. XML  <br/> |
   
## <a name="definition"></a>Определение

```XML
< xs:element name="DataConnection" type="DataConnection_Type" minOccurs="1" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a>Элементы и атрибуты

Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений. 
  
### <a name="parent-elements"></a>Родительские элементы

|**Элемент**|**Тип**|**Описание**|
|:-----|:-----|:-----|
|[DataConnections](dataconnections-elementvisio-xml.md) <br/> |[Датаконнектионс_типе](dataconnections_type-complextypevisio-xml.md) <br/> |Содержит элементы **подключения** к документу.  <br/> |
   
### <a name="child-elements"></a>Дочерние элементы

Нет.
  
### <a name="attributes"></a>Атрибуты

|**Атрибут**|**Тип**|**Обязательный**|**Описание**|**Возможные значения**|
|:-----|:-----|:-----|:-----|:-----|
|AlwaysUseConnectionFile  <br/> |XSD: Boolean  <br/> |необязательный  <br/> |Значение по умолчанию  false. Дополнительные сведения см.  <br/> |Значения типа XSD: Boolean.  <br/> |
|Command  <br/> |XSD: строка  <br/> |необязательный  <br/> |Командная строка, используемая для запроса к источнику данных.  <br/> |Значения типа String: XSD.  <br/> |
|ConnectionString  <br/> |XSD: строка  <br/> |необязательный  <br/> |Строка подключения, определяющая параметры, необходимые для подключения к источнику данных.  <br/> |Значения типа String: XSD.  <br/> |
|FileName  <br/> |XSD: строка  <br/> |Обязательный  <br/> |Имя файла подключения. Дополнительные сведения см.  <br/> |Значения типа String: XSD.  <br/> |
|FriendlyName  <br/> |XSD: строка  <br/> |необязательный  <br/> |Имя, указанное пользователем для подключения к данным.  <br/> |Значения типа String: XSD.  <br/> |
|ID  <br/> |XSD: Унсигнединт  <br/> |Обязательный  <br/> |Идентификатор, назначенный Visio для данного подключения, уникальный в пределах документа.  <br/> |Значения типа XSD: Унсигнединт.  <br/> |
|Timeout  <br/> |XSD: Унсигнединт  <br/> |необязательный  <br/> |Время ожидания в минутах при попытке установить подключение перед завершением попытки.  <br/> |Значения типа XSD: Унсигнединт.  <br/> |
   

