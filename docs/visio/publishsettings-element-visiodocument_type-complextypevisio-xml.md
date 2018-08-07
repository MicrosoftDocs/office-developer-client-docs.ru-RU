---
title: Элемент PublishSettings (VisioDocument_Type complexType) ('Visio XML»)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: d0a41494-ffad-c56c-2074-135b3d0bffb9
description: Задает параметры, используемые при открытии диаграммы с помощью служб Visio в Microsoft SharePoint Server 2013.
ms.openlocfilehash: f2554facc47de23104f65b26ae19cfc71821bd37
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19814508"
---
# <a name="publishsettings-element-visiodocumenttype-complextype-visio-xml"></a>Элемент PublishSettings (VisioDocument_Type complexType) ('Visio XML»)

Задает параметры, используемые при открытии диаграммы с помощью служб Visio в Microsoft SharePoint Server 2013.
  
## <a name="element-information"></a>Сведения об элементе

|||
|:-----|:-----|
|**Тип элемента** <br/> |[PublishSettings_Type](publishsettings_type-complextypevisio-xml.md) <br/> |
|**Пространство имен** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Файл схемы** <br/> |VisioSchema15.xsd  <br/> |
|**Части документа** <br/> |Document.XML  <br/> |
   
## <a name="definition"></a>Определение

```XML
< xs:element name="PublishSettings" type="PublishSettings_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a>Элементы и атрибуты

Если схема определяет специальные требования, такие как **последовательность**, **minOccurs**, **maxOccurs**и **выбора**, обратитесь к разделу определение. 
  
### <a name="parent-elements"></a>Родительские элементы

|**Элемент**|**Тип**|**Описание**|
|:-----|:-----|:-----|
|[VisioDocument](visiodocument-elementvisio-xml.md) <br/> |[VisioDocument_Type](visiodocument_type-complextypevisio-xml.md) <br/> |Задает свойства документа.  <br/> |
   
### <a name="child-elements"></a>Дочерние элементы

|**Элемент**|**Тип**|**Описание**|
|:-----|:-----|:-----|
|[PublishedPage](publishedpage-element-publishsettings_type-complextypevisio-xml.md) <br/> |[PublishedPage_Type](publishedpage_type-complextypevisio-xml.md) <br/> |Указывает, является ли страницу документа для просмотра в браузере с помощью служб Visio.  <br/> |
|[RefreshableData](refreshabledata-element-publishsettings_type-complextypevisio-xml.md) <br/> |[RefreshableData_Type](refreshabledata_type-complextypevisio-xml.md) <br/> |Указывает, является ли набор записей обновляемый, с помощью служб Visio.  <br/> |
   
### <a name="attributes"></a>Атрибуты

Нет.
  

