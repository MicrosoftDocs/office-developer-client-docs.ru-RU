---
title: Элемент DataConnection (DataConnections_Type complexType) ('Visio XML»)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6aab8be3-b236-029b-1df3-b6860d4f4586
description: Выделяет обмена данными между один или несколько элементов записей данных и источник данных не в формате XML.
ms.openlocfilehash: 74e15795e023517263d9b79e9f19557653e4e939
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19813551"
---
# <a name="dataconnection-element-dataconnectionstype-complextype-visio-xml"></a>Элемент DataConnection (DataConnections_Type complexType) ('Visio XML»)

Выделяет обмена данными между один или несколько элементов **записей данных** и источник данных не в формате XML. 
  
## <a name="element-information"></a>Сведения об элементе

|||
|:-----|:-----|
|**Тип элемента** <br/> |[DataConnection_Type](dataconnection_type-complextypevisio-xml.md) <br/> |
|**Пространство имен** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Файл схемы** <br/> |VisioSchema15.xsd  <br/> |
|**Части документа** <br/> |Connections.XML  <br/> |
   
## <a name="definition"></a>Определение

```XML
< xs:element name="DataConnection" type="DataConnection_Type" minOccurs="1" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a>Элементы и атрибуты

Если схема определяет специальные требования, такие как **последовательность**, **minOccurs**, **maxOccurs**и **выбора**, обратитесь к разделу определение. 
  
### <a name="parent-elements"></a>Родительские элементы

|**Элемент**|**Тип**|**Описание**|
|:-----|:-----|:-----|
|[DataConnections](dataconnections-elementvisio-xml.md) <br/> |[DataConnections_Type](dataconnections_type-complextypevisio-xml.md) <br/> |Содержит элементы **подключение данных** для документа.  <br/> |
   
### <a name="child-elements"></a>Дочерние элементы

Нет.
  
### <a name="attributes"></a>Атрибуты

|**Атрибут**|**Тип**|**Обязательное**|**Описание**|**Возможные значения**|
|:-----|:-----|:-----|:-----|:-----|
|AlwaysUseConnectionFile  <br/> |XSD:Boolean  <br/> |необязательный  <br/> |Значение по умолчанию — false. Для получения дополнительных сведений см.  <br/> |Значения типа xsd:boolean.  <br/> |
|Команда  <br/> |XSD:String  <br/> |необязательный  <br/> |Командную строку, используемую для запроса источника данных.  <br/> |Значения типа xsd:string.  <br/> |
|ConnectionString  <br/> |XSD:String  <br/> |необязательный  <br/> |Строка подключения, который определяет параметры, необходимые для подключения к источнику данных.  <br/> |Значения типа xsd:string.  <br/> |
|FileName  <br/> |XSD:String  <br/> |Обязательный  <br/> |Имя файла подключения. Для получения дополнительных сведений см.  <br/> |Значения типа xsd:string.  <br/> |
|FriendlyName  <br/> |XSD:String  <br/> |необязательный  <br/> |Предоставляются имя пользователя для подключения к данным.  <br/> |Значения типа xsd:string.  <br/> |
|ID  <br/> |XSD:unsignedInt  <br/> |Обязательный  <br/> |Идентификатор, назначенный с Visio для данного подключения, уникальные в документе.  <br/> |Значения типа xsd:unsignedInt.  <br/> |
|Timeout  <br/> |XSD:unsignedInt  <br/> |необязательный  <br/> |Время ожидания в минутах при попытке установить подключение завершается.  <br/> |Значения типа xsd:unsignedInt.  <br/> |
   

