---
title: Элемент Публишсеттингс (Висиодокумент_типе complexType) (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: d0a41494-ffad-c56c-2074-135b3d0bffb9
description: Задает параметры, которые используются при открытии схемы с помощью служб Visio в Microsoft SharePoint Server 2013.
ms.openlocfilehash: 7e926021180d0f32c5e8754fd856081908f4925d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32345460"
---
# <a name="publishsettings-element-visiodocumenttype-complextype-visio-xml"></a>Элемент Публишсеттингс (Висиодокумент_типе complexType) (' Visio XML ')

Задает параметры, которые используются при открытии схемы с помощью служб Visio в Microsoft SharePoint Server 2013.
  
## <a name="element-information"></a>Сведения об элементе

|||
|:-----|:-----|
|**Тип элемента** <br/> |[Публишсеттингс_типе](publishsettings_type-complextypevisio-xml.md) <br/> |
|**Пространство имен** <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
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
  

