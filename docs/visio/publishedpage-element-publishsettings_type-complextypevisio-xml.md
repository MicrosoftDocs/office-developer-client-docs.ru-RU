---
title: Элемент Публишедпаже (Публишсеттингс_типе complexType) (XML для Visio)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: c1eca66b-5840-790a-459f-e06680d11c05
description: Указывает, будет ли страница документа видна в браузере с помощью служб Visio в Microsoft SharePoint Server 2013.
ms.openlocfilehash: 614c01f12b9a7525620704e5417a106e8703c983
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/29/2019
ms.locfileid: "34538377"
---
# <a name="publishedpage-element-publishsettingstype-complextype-visio-xml"></a>Элемент Публишедпаже (Публишсеттингс_типе complexType) (XML для Visio)

Указывает, будет ли страница документа видна в браузере с помощью служб Visio в Microsoft SharePoint Server 2013.
  
## <a name="element-information"></a>Сведения об элементе

|||
|:-----|:-----|
|**Тип элемента** <br/> |[Публишедпаже_типе](publishedpage_type-complextypevisio-xml.md) <br/> |
|**Пространство имен** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Файл схемы** <br/> |VisioSchema15. xsd  <br/> |
|**Части документа** <br/> |Document. XML  <br/> |
   
## <a name="definition"></a>Определение

```XML
< xs:element name="PublishedPage" type="PublishedPage_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a>Элементы и атрибуты

Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений. 
  
### <a name="parent-elements"></a>Родительские элементы

|**Элемент**|**Тип**|**Описание**|
|:-----|:-----|:-----|
|[Публишсеттингс](publishsettings-element-visiodocument_type-complextypevisio-xml.md) <br/> |[Публишсеттингс_типе](publishsettings_type-complextypevisio-xml.md) <br/> |Задает параметры, которые используются при открытии схемы с помощью служб Visio.  <br/> |
   
### <a name="child-elements"></a>Дочерние элементы

Нет.
  
### <a name="attributes"></a>Атрибуты

|**Атрибут**|**Тип**|**Обязательный**|**Описание**|**Возможные значения**|
|:-----|:-----|:-----|:-----|:-----|
|ID  <br/> |XSD: Унсигнединт  <br/> |Обязательный  <br/> |Идентификатор страницы документа.  <br/> |Значения типа XSD: Унсигнединт.  <br/> |
   

