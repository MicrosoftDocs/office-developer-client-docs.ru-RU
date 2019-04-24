---
title: Элемент Висиодокумент (' XML ' Visio ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: f5954685-3a2d-7848-388f-5dd7e536551c
description: Корневой элемент документа Microsoft Visio.
ms.openlocfilehash: 9829fa8960d78777e0fff4306b96978da90a647d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32285315"
---
# <a name="visiodocument-element-visio-xml"></a>Элемент Висиодокумент (' XML ' Visio ')

Корневой элемент документа Microsoft Visio.
  
## <a name="element-information"></a>Сведения об элементе

|||
|:-----|:-----|
|**Тип элемента** <br/> |[Висиодокумент_типе](visiodocument_type-complextypevisio-xml.md) <br/> |
|**Пространство имен** <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Файл схемы** <br/> |VisioSchema15. xsd  <br/> |
|**Части документа** <br/> |Document. XML  <br/> |
   
## <a name="definition"></a>Определение

```XML
< xs:element name="VisioDocument" type="VisioDocument_Type" >
</xs:element >
```

## <a name="elements-and-attributes"></a>Элементы и атрибуты

Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений. 
  
### <a name="parent-elements"></a>Родительские элементы

Нет.
  
### <a name="child-elements"></a>Дочерние элементы

|**Элемент**|**Тип**|**Описание**|
|:-----|:-----|:-----|
|[Colors](colors-element-visiodocument_type-complextypevisio-xml.md) <br/> |[Колорс_типе](colors_type-complextypevisio-xml.md) <br/> |Содержит таблицу цветов документа.  <br/> |
|[Документсеттингс](documentsettings-element-visiodocument_type-complextypevisio-xml.md) <br/> |[Документсеттингс_типе](documentsettings_type-complextypevisio-xml.md) <br/> |Содержит элементы, определяющие параметры документа.  <br/> |
|[DocumentSheet](documentsheet-element-visiodocument_type-complextypevisio-xml.md) <br/> |[Документшит_типе](documentsheet_type-complextypevisio-xml.md) <br/> |Указывает структуру **таблицы свойств фигуры** .  <br/> |
|[EventList](eventlist-element-visiodocument_type-complextypevisio-xml.md) <br/> |[Евентлист_типе](eventlist_type-complextypevisio-xml.md) <br/> |Содержит элемент **евентитем** для каждого события, на которое должен отвечать объект.  <br/> |
|[Фаценамес](facenames-element-visiodocument_type-complextypevisio-xml.md) <br/> |[Фаценамес_типе](facenames_type-complextypevisio-xml.md) <br/> |Содержит коллекцию элементов **фаценаме** .  <br/> |
|[HeaderFooter](headerfooter-element-visiodocument_type-complextypevisio-xml.md) <br/> |[Хеадерфутер_типе](headerfooter_type-complextypevisio-xml.md) <br/> |Содержит элементы для верхнего и нижнего колонтитулов документа.  <br/> |
|[Публишсеттингс](publishsettings-element-visiodocument_type-complextypevisio-xml.md) <br/> |[Публишсеттингс_типе](publishsettings_type-complextypevisio-xml.md) <br/> |Задает набор доступных для обновления и набора наборов записей, доступных для обновления в документе.  <br/> |
|[StyleSheets](stylesheets-element-visiodocument_type-complextypevisio-xml.md) <br/> |[Стилешитс_типе](stylesheets_type-complextypevisio-xml.md) <br/> |Содержит коллекцию элементов StyleSheet для документа.  <br/> |
   
### <a name="attributes"></a>Атрибуты

Нет.
  

