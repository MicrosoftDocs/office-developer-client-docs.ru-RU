---
title: Элемент weather (элемент weatherdata) (схема сведений о погоде в Outlook)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: de3c35ef-84a3-b991-7c98-3eca720c9ba0
description: Указывает погоду расположения.
ms.openlocfilehash: 18669dfc4636c28e03a582bc0c8df512aa38a4e4
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/29/2019
ms.locfileid: "34541269"
---
# <a name="weather-element-weatherdata-element-outlook-weather-information-schema"></a>Элемент weather (элемент weatherdata) (схема сведений о погоде в Outlook)

Указывает погоду расположения.
  
## <a name="element-information"></a>Сведения об элементе

|||
|:-----|:-----|
|**Тип элемента** <br/> |[weatherType](weathertype-complextype-outlook-weather-information-schema.md) <br/> |
|**Пространство имен** <br/> |http://schemas.microsoft.com/office/outlook/15/getweatherinfo.xsd  <br/> |
|**Файл схемы** <br/> |getweatherinfo.xsd  <br/> |
   
## <a name="definition"></a>Определение

```XML
<xs:element name="weather"      type="weatherType">
  </xs:element>  

```

## <a name="elements-and-attributes"></a>Элементы и атрибуты

Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений. 
  
### <a name="parent-elements"></a>Родительские элементы

|**Элемент**|**Тип**|**Описание**|
|:-----|:-----|:-----|
|[weatherdata](weatherdata-element-outlook-weather-information-schema.md) <br/> ||Определяет элемент прогноза погоды.  <br/> |
   
### <a name="child-elements"></a>Дочерние элементы

|**Элемент**|**Тип**|**Описание**|
|:-----|:-----|:-----|
|[current](current-element-weathertype-complextypeoutlook-weather-information-schema.md) <br/> |[currentType](currenttype-complextype-outlook-weather-information-schema.md) <br/> |Указывает текущие прогнозы погоды.  <br/> |
|[forecast](forecast-element-weathertype-complextypeoutlook-weather-information-schema.md) <br/> |[forecastType](forecasttype-complextype-outlook-weather-information-schema.md) <br/> |Указывает будущие прогнозы погоды по крайней мере на три дня вперед, включая сегодня: сегодня, завтра, день после завтра.  <br/> |
   
### <a name="attributes"></a>Атрибуты

|**Атрибут**|**Тип**|**Обязательный**|**Описание**|**Возможные значения**|
|:-----|:-----|:-----|:-----|:-----|
|attribution  <br/> |xs:string  <br/> |Обязательный  <br/> |Указывает источник сведений о погоде.  <br/> |Значение типа xs:string  <br/> |
|degreetype  <br/> |xs:string  <br/> |Обязательный  <br/> |Указывает единицу температуры расположения, например Цельсия.  <br/> |C, F  <br/> |
|imagerelativeurl  <br/> |xs:string  <br/> |Обязательный  <br/> |Указывает URL-адрес изображения для расположения.  <br/> |Значение типа xs:string  <br/> |
|timezone  <br/> |xs:integer  <br/> |Обязательный  <br/> |Указывает смещение GMT.  <br/> |Значение от -11 до 12 включительно  <br/> |
|url  <br/> |xs:string  <br/> |Обязательный  <br/> |Указывает URL-адрес веб-страницы службы прогноза погоды, которая содержит сведения о погоде для указанного расположения.  <br/> |Значение типа xs:string  <br/> |
|weatherlocationcode  <br/> |xs:string  <br/> |Обязательный  <br/> |Указывает код, связанный с расположением, используемым для различенного расположения с одинаковым именем.  <br/> |Значение типа xs:string  <br/> |
|weatherlocationname  <br/> |xs:string  <br/> |Обязательный  <br/> |Указывает имя расположения, которое отображается в выпадаемом оке.  <br/> |Значение типа xs:string  <br/> |
   

