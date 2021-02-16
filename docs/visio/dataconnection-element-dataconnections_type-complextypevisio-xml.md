---
title: Элемент DataConnection (DataConnections_Type complexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6aab8be3-b236-029b-1df3-b6860d4f4586
description: Абстрагировать связь между одним или более элементами DataRecordset и источником данных, не относяющимися к XML.
ms.openlocfilehash: 619f3b4e3d9c93831cc23bc38fba3670107b2b51
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/29/2019
ms.locfileid: "34538405"
---
# <a name="dataconnection-element-dataconnections_type-complextype-visio-xml"></a>Элемент DataConnection (DataConnections_Type complexType) (Visio XML)

Абстрагировать связь между одним или более **элементами DataRecordset** и источником данных, не относяющимися к XML. 
  
## <a name="element-information"></a>Сведения об элементе

|||
|:-----|:-----|
|**Тип элемента** <br/> |[DataConnection_Type](dataconnection_type-complextypevisio-xml.md) <br/> |
|**Пространство имен** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Файл схемы** <br/> |VisioSchema15.xsd  <br/> |
|**Части документа** <br/> |connections.xml  <br/> |
   
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
|[DataConnections](dataconnections-elementvisio-xml.md) <br/> |[DataConnections_Type](dataconnections_type-complextypevisio-xml.md) <br/> |Содержит элементы **DataConnection** для документа.  <br/> |
   
### <a name="child-elements"></a>Дочерние элементы

Нет.
  
### <a name="attributes"></a>Атрибуты

|**Атрибут**|**Тип**|**Обязательный**|**Описание**|**Возможные значения**|
|:-----|:-----|:-----|:-----|:-----|
|AlwaysUseConnectionFile  <br/> |xsd:boolean  <br/> |необязательный  <br/> |Значение по умолчанию  false. Дополнительные сведения см. в примечаиях.  <br/> |Значения типа xsd:boolean.  <br/> |
|Команда  <br/> |xsd:string  <br/> |необязательный  <br/> |Строка команды, используемая для запроса источника данных.  <br/> |Значения типа xsd:string.  <br/> |
|ConnectionString  <br/> |xsd:string  <br/> |необязательный  <br/> |Строка подключения, которая определяет параметры, необходимые для подключения к источнику данных.  <br/> |Значения типа xsd:string.  <br/> |
|FileName  <br/> |xsd:string  <br/> |Обязательный  <br/> |Имя файла подключения. Дополнительные сведения см. в примечаиях.  <br/> |Значения типа xsd:string.  <br/> |
|FriendlyName  <br/> |xsd:string  <br/> |необязательный  <br/> |Имя, предоставленное пользователем для подключения к данным.  <br/> |Значения типа xsd:string.  <br/> |
|ID  <br/> |xsd:unsignedInt  <br/> |Обязательный  <br/> |ИД, присвоенный Visio для заданного подключения, уникальный в документе.  <br/> |Значения типа xsd:unsignedInt.  <br/> |
|Timeout  <br/> |xsd:unsignedInt  <br/> |необязательный  <br/> |Время ожидания в минутах при попытке установить подключение перед прерыванием попытки.  <br/> |Значения типа xsd:unsignedInt.  <br/> |
   

