---
title: элемент прогноза погоды (weatherdata элемент) (схема местоположения погоды Outlook)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 1127956a-37aa-c39e-60b4-343dcc4ead82
description: Указывает местоположение для прогноза погоды отчет на.
ms.openlocfilehash: f6642b3f477b9fe45ed0e6a43efcd40e21559b7e
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25398299"
---
# <a name="weather-element-weatherdata-element-outlook-weather-location-schema"></a>элемент прогноза погоды (weatherdata элемент) (схема местоположения погоды Outlook)

Указывает местоположение для прогноза погоды отчет на.
  
## <a name="element-information"></a>Сведения об элементе

|||
|:-----|:-----|
|**Тип элемента** <br/> |[weatherType](weathertype-complextype-outlook-weather-location-schema.md) <br/> |
|**Пространство имен** <br/> |https://schemas.microsoft.com/office/outlook/15/getweatherlocation.xsd  <br/> |
|**Файл схемы** <br/> |getweatherlocation.xsd  <br/> |
   
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
|[WeatherData](weatherdata-element-outlook-weather-location-schema.md) <br/> ||Определяет элемент прогноза погоды.  <br/> |
   
### <a name="child-elements"></a>Дочерние элементы

Нет.
  
### <a name="attributes"></a>Атрибуты

|**Атрибут**|**Тип**|**Обязательный**|**Описание**|**Возможные значения**|
|:-----|:-----|:-----|:-----|:-----|
|weatherlocationcode  <br/> |xs:string  <br/> |Обязательный  <br/> |Указывает код, связанный с расположением для различения нескольких расположений с тем же именем.  <br/> |Значения типа xs: String  <br/> |
|weatherlocationname  <br/> |xs:string  <br/> |Обязательный  <br/> |Указывает имя расположения.  <br/> |Значения типа xs: String  <br/> |
   

