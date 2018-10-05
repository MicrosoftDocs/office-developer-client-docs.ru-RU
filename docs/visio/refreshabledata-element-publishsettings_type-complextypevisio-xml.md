---
title: Элемент RefreshableData (PublishSettings_Type complexType) ('Visio XML»)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 9a3b9d5a-fcba-eb18-3199-bd5a7f889af8
description: Указывает, является ли набор записей обновляемый, с помощью служб Visio в Microsoft SharePoint Server 2013.
ms.openlocfilehash: b402e2c9d65bf868c0ac33c782b87857ab6aed75
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25384875"
---
# <a name="refreshabledata-element-publishsettingstype-complextype-visio-xml"></a>Элемент RefreshableData (PublishSettings_Type complexType) ('Visio XML»)

Указывает, является ли набор записей обновляемый, с помощью служб Visio в Microsoft SharePoint Server 2013.
  
## <a name="element-information"></a>Сведения об элементе

|||
|:-----|:-----|
|**Тип элемента** <br/> |[RefreshableData_Type](refreshabledata_type-complextypevisio-xml.md) <br/> |
|**Пространство имен** <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Файл схемы** <br/> |VisioSchema15.xsd  <br/> |
|**Части документа** <br/> |Document.XML  <br/> |
   
## <a name="definition"></a>Определение

```XML
<xs:element name="RefreshableData" type="RefreshableData_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >

```

## <a name="elements-and-attributes"></a>Элементы и атрибуты

Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений. 
  
### <a name="parent-elements"></a>Родительские элементы

|**Элемент**|**Тип**|**Описание**|
|:-----|:-----|:-----|
|[PublishSettings](publishsettings-element-visiodocument_type-complextypevisio-xml.md) <br/> |[PublishSettings_Type](publishsettings_type-complextypevisio-xml.md) <br/> |Задает параметры, используемые при открытии диаграммы с помощью служб Visio.  <br/> |
   
### <a name="child-elements"></a>Дочерние элементы

Нет.
  
### <a name="attributes"></a>Атрибуты

|**Атрибут**|**Тип**|**Обязательный**|**Описание**|**Возможные значения**|
|:-----|:-----|:-----|:-----|:-----|
|ID  <br/> |XSD:unsignedInt  <br/> |Обязательный  <br/> |Идентификатор набора записей.  <br/> |Значения типа xsd:unsignedInt.  <br/> |
   

