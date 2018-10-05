---
title: Прогноз элемент (weatherType complexType) (схема сведения о погоде Outlook)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 9124fa30-d58b-8354-91e9-8d2237a8251d
description: 'Указывает будущих погоды по крайней мере три дня издержек, включая сегодня: сегодня, завтра, послезавтра.'
ms.openlocfilehash: 01604796d4460cc14005ee00ea6b8f46f04d4742
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25398327"
---
# <a name="forecast-element-weathertype-complextype-outlook-weather-information-schema"></a>Прогноз элемент (weatherType complexType) (схема сведения о погоде Outlook)

Указывает будущих погоды по крайней мере три дня издержек, включая сегодня: сегодня, завтра, послезавтра.
  
## <a name="element-information"></a>Сведения об элементе

|||
|:-----|:-----|
|**Тип элемента** <br/> |[forecastType](forecasttype-complextype-outlook-weather-information-schema.md) <br/> |
|**Пространство имен** <br/> |https://schemas.microsoft.com/office/outlook/15/getweatherinfo.xsd  <br/> |
|**Файл схемы** <br/> |GetWeatherInfo.xsd  <br/> |
   
## <a name="definition"></a>Определение

```XML
<xs:element name="forecast"      type="forecastType" minOccurs="3"     maxOccurs="unbounded"    >
  </xs:element>  

```

## <a name="elements-and-attributes"></a>Элементы и атрибуты

Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений. 
  
### <a name="parent-elements"></a>Родительские элементы

|**Элемент**|**Тип**|**Описание**|
|:-----|:-----|:-----|
|[прогноза погоды](weather-element-weatherdata-elementoutlook-weather-information-schema.md) <br/> |[weatherType](weathertype-complextype-outlook-weather-information-schema.md) <br/> |Задает погоды расположения.  <br/> |
   
### <a name="child-elements"></a>Дочерние элементы

Нет.
  
### <a name="attributes"></a>Атрибуты

|**Атрибут**|**Тип**|**Обязательный**|**Описание**|**Возможные значения**|
|:-----|:-----|:-----|:-----|:-----|
|date  <br/> |xs: Date  <br/> |Обязательный  <br/> |Указывает дату для прогноза.  <br/> |Значения типа xs: Date  <br/> |
|день  <br/> |xs:string  <br/> |Обязательный  <br/> |Задает день для прогноза.  <br/> |Значения типа xs: String  <br/> |
|Высокая  <br/> |xs:integer  <br/> |Обязательный  <br/> |Задает прогнозируемому количеству наибольший температуры.  <br/> |Значения типа xs: Integer  <br/> |
|Низкая  <br/> |xs:integer  <br/> |Обязательный  <br/> |Задает прогнозируемому количеству низшего температуры.  <br/> |Значения типа xs: Integer  <br/> |
|precip  <br/> |xs:integer  <br/> |Обязательный  <br/> |Указывает процент возможность precipitation.  <br/> |Значения типа xs: Integer  <br/> |
|shortday  <br/> |xs:string  <br/> |Обязательный  <br/> |Задает день сокращенную форму.  <br/> |Значения типа xs: String  <br/> |
|skycodeday  <br/> |xs:integer  <br/> |Обязательный  <br/> |Указывает код прогнозируемому количеству условий.  <br/> |Значения типа xs: Integer  <br/> |
|skytextday  <br/> |xs:string  <br/> |Обязательный  <br/> |Указывает один или два слова, которые описывают прогнозируемому количеству условий.  <br/> |Значения типа xs: String  <br/> |
   

