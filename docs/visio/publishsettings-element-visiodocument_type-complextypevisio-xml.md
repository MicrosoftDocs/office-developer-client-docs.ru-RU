---
title: Элемент Публишсеттингс (Висиодокумент_типе complexType) (XML для Visio)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: d0a41494-ffad-c56c-2074-135b3d0bffb9
description: Задает параметры, которые используются при открытии схемы с помощью служб Visio в Microsoft SharePoint Server 2013.
ms.openlocfilehash: 611dfe477228995bca6aedff27b468a2d57e7e85
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/29/2019
ms.locfileid: "34541360"
---
# <a name="publishsettings-element-visiodocumenttype-complextype-visio-xml"></a>Элемент Публишсеттингс (Висиодокумент_типе complexType) (XML для Visio)

Задает параметры, которые используются при открытии схемы с помощью служб Visio в Microsoft SharePoint Server 2013.
  
## <a name="element-information"></a>Сведения об элементе

|||
|:-----|:-----|
|**Тип элемента** <br/> |[Публишсеттингс_типе](publishsettings_type-complextypevisio-xml.md) <br/> |
|**Пространство имен** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Файл схемы** <br/> |VisioSchema15. xsd  <br/> |
|**Части документа** <br/> |Document. XML  <br/> |
   
## <a name="definition"></a>Определение

```XML
< xs:element name="PublishSettings" type="PublishSettings_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a>Элементы и атрибуты

Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений. 
  
### <a name="parent-elements"></a>Родительские элементы

|**Элемент**|**Тип**|**Описание**|
|:-----|:-----|:-----|
|[Висиодокумент](visiodocument-elementvisio-xml.md) <br/> |[Висиодокумент_типе](visiodocument_type-complextypevisio-xml.md) <br/> |Задает свойства рисунка.  <br/> |
   
### <a name="child-elements"></a>Дочерние элементы

|**Элемент**|**Тип**|**Описание**|
|:-----|:-----|:-----|
|[Публишедпаже](publishedpage-element-publishsettings_type-complextypevisio-xml.md) <br/> |[Публишедпаже_типе](publishedpage_type-complextypevisio-xml.md) <br/> |Указывает, будет ли страница документа видна в браузере с помощью служб Visio.  <br/> |
|[Рефрешабледата](refreshabledata-element-publishsettings_type-complextypevisio-xml.md) <br/> |[Рефрешабледата_типе](refreshabledata_type-complextypevisio-xml.md) <br/> |Указывает, следует ли обновлять набор записей с помощью служб Visio.  <br/> |
   
### <a name="attributes"></a>Атрибуты

Нет.
  

