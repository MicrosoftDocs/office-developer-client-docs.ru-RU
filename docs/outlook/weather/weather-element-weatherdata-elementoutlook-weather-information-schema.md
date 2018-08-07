---
title: элемент прогноза погоды (weatherdata элемент) (схема сведения о погоде Outlook)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: de3c35ef-84a3-b991-7c98-3eca720c9ba0
description: Задает погоды расположения.
ms.openlocfilehash: c19db6657860dd35f90832aef0614f4fb88d87b4
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19812923"
---
# <a name="weather-element-weatherdata-element-outlook-weather-information-schema"></a>элемент прогноза погоды (weatherdata элемент) (схема сведения о погоде Outlook)

Задает погоды расположения.
  
## <a name="element-information"></a>Сведения об элементе

|||
|:-----|:-----|
|**Тип элемента** <br/> |[weatherType](weathertype-complextype-outlook-weather-information-schema.md) <br/> |
|**Пространство имен** <br/> |http://schemas.microsoft.com/office/outlook/15/getweatherinfo.xsd  <br/> |
|**Файл схемы** <br/> |GetWeatherInfo.xsd  <br/> |
   
## <a name="definition"></a>Определение

```XML
<xs:element name="weather"      type="weatherType">
  </xs:element>  

```

## <a name="elements-and-attributes"></a>Элементы и атрибуты

Если схема определяет специальные требования, такие как **последовательность**, **minOccurs**, **maxOccurs**и **выбора**, обратитесь к разделу определение. 
  
### <a name="parent-elements"></a>Родительские элементы

|**Элемент**|**Тип**|**Описание**|
|:-----|:-----|:-----|
|[WeatherData](weatherdata-element-outlook-weather-information-schema.md) <br/> ||Определяет элемент прогноза погоды.  <br/> |
   
### <a name="child-elements"></a>Дочерние элементы

|**Элемент**|**Тип**|**Описание**|
|:-----|:-----|:-----|
|[current](current-element-weathertype-complextypeoutlook-weather-information-schema.md) <br/> |[currentType](currenttype-complextype-outlook-weather-information-schema.md) <br/> |Указывает текущий погоды.  <br/> |
|[Прогноз](forecast-element-weathertype-complextypeoutlook-weather-information-schema.md) <br/> |[forecastType](forecasttype-complextype-outlook-weather-information-schema.md) <br/> |Указывает будущих погоды по крайней мере три дня издержек, включая сегодня: сегодня, завтра, послезавтра.  <br/> |
   
### <a name="attributes"></a>Атрибуты

|**Атрибут**|**Тип**|**Обязательное**|**Описание**|**Возможные значения**|
|:-----|:-----|:-----|:-----|:-----|
|атрибуты  <br/> |xs:string  <br/> |Обязательный  <br/> |Указывает источник сведений о погоде.  <br/> |Значения типа xs: String  <br/> |
|degreetype  <br/> |xs:string  <br/> |Обязательный  <br/> |Определяет единицу измерения для температуры расположения, например градусы Цельсия.  <br/> |C, F  <br/> |
|imagerelativeurl  <br/> |xs:string  <br/> |Обязательный  <br/> |URL-адрес изображения для расположения.  <br/> |Значения типа xs: String  <br/> |
|часовой пояс  <br/> |xs:integer  <br/> |Обязательный  <br/> |Задает смещение GMT.  <br/> |Значение в диапазоне от -11 и 12 включительно  <br/> |
|url  <br/> |xs:string  <br/> |Обязательный  <br/> |Задает URL-адрес для веб-страницы, которая содержит информацию о погоде для заданного расположения службы прогноза погоды.  <br/> |Значения типа xs: String  <br/> |
|weatherlocationcode  <br/> |xs:string  <br/> |Обязательный  <br/> |Указывает код, который связан с расположением, используемых для различения нескольких расположения, с одинаковыми именами.  <br/> |Значения типа xs: String  <br/> |
|weatherlocationname  <br/> |xs:string  <br/> |Обязательный  <br/> |Указывает имя расположения, которое отображается в элементе управления раскрывающегося списка.  <br/> |Значения типа xs: String  <br/> |
   

