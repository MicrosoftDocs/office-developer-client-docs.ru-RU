---
title: элемент Weather (элемент веасердата) (схема расположений о погоде Outlook)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 1127956a-37aa-c39e-60b4-343dcc4ead82
description: Указывает расположение для отчета о погоде.
ms.openlocfilehash: f6642b3f477b9fe45ed0e6a43efcd40e21559b7e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32355211"
---
# <a name="weather-element-weatherdata-element-outlook-weather-location-schema"></a>элемент Weather (элемент веасердата) (схема расположений о погоде Outlook)

Указывает расположение для отчета о погоде.
  
## <a name="element-information"></a>Сведения об элементе

|||
|:-----|:-----|
|**Тип элемента** <br/> |[Веасертипе](weathertype-complextype-outlook-weather-location-schema.md) <br/> |
|**Пространство имен** <br/> |https://schemas.microsoft.com/office/outlook/15/getweatherlocation.xsd  <br/> |
|**Файл схемы** <br/> |жетвеасерлокатион. xsd  <br/> |
   
## <a name="definition"></a>Определение

```XML
<xs:element name="weather"      type="weatherType" maxOccurs="unbounded"    >
  </xs:element>  

```

## <a name="elements-and-attributes"></a>Элементы и атрибуты

Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений. 
  
### <a name="parent-elements"></a>Родительские элементы

|**Элемент**|**Тип**|**Описание**|
|:-----|:-----|:-----|
|[веасердата](weatherdata-element-outlook-weather-location-schema.md) <br/> ||Определяет элемент weather.  <br/> |
   
### <a name="child-elements"></a>Дочерние элементы

Нет.
  
### <a name="attributes"></a>Атрибуты

|**Атрибут**|**Тип**|**Обязательный**|**Описание**|**Возможные значения**|
|:-----|:-----|:-----|:-----|:-----|
|веасерлокатионкоде  <br/> |xs: String  <br/> |Обязательный  <br/> |Указывает код, связанный с расположением, для различения нескольких расположений с одинаковыми именами.  <br/> |Значение типа xs: String.  <br/> |
|веасерлокатионнаме  <br/> |xs: String  <br/> |Обязательный  <br/> |Задает имя расположения.  <br/> |Значение типа xs: String.  <br/> |
   

