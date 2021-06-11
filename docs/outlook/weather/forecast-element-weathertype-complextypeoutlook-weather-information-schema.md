---
title: Элемент forecast (weatherType complexType) (Outlook схема сведений о погоде)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 9124fa30-d58b-8354-91e9-8d2237a8251d
description: 'Указывает будущие погодные условия по крайней мере на три дня вперед, в том числе сегодня: сегодня, завтра, послезавтра.'
ms.openlocfilehash: 5e442ee5995bbd51c5e518162286bc199a625dbd
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/29/2019
ms.locfileid: "34540982"
---
# <a name="forecast-element-weathertype-complextype-outlook-weather-information-schema"></a>Элемент forecast (weatherType complexType) (Outlook схема сведений о погоде)

Указывает будущие погодные условия по крайней мере на три дня вперед, в том числе сегодня: сегодня, завтра, послезавтра.
  
## <a name="element-information"></a>Сведения об элементе

|||
|:-----|:-----|
|**Тип элемента** <br/> |[forecastType](forecasttype-complextype-outlook-weather-information-schema.md) <br/> |
|**Пространство имен** <br/> |http://schemas.microsoft.com/office/outlook/15/getweatherinfo.xsd  <br/> |
|**Файл схемы** <br/> |getweatherinfo.xsd  <br/> |
   
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
|[погода](weather-element-weatherdata-elementoutlook-weather-information-schema.md) <br/> |[weatherType](weathertype-complextype-outlook-weather-information-schema.md) <br/> |Указывает погодные условия расположения.  <br/> |
   
### <a name="child-elements"></a>Дочерние элементы

Нет.
  
### <a name="attributes"></a>Атрибуты

|**Атрибут**|**Тип**|**Обязательный**|**Описание**|**Возможные значения**|
|:-----|:-----|:-----|:-----|:-----|
|date  <br/> |xs:date  <br/> |Обязательный  <br/> |Указывает дату прогноза.  <br/> |Значение типа xs:date  <br/> |
|день  <br/> |xs:string  <br/> |Обязательный  <br/> |Указывает день для прогноза.  <br/> |Значение типа xs:string  <br/> |
|высокая  <br/> |xs:integer  <br/> |Обязательный  <br/> |Указывает прогнозируемую наивысшую температуру.  <br/> |Значение типа xs:integer  <br/> |
|низкий  <br/> |xs:integer  <br/> |Обязательный  <br/> |Указывает прогнозируемую минимальную температуру.  <br/> |Значение типа xs:integer  <br/> |
|precip  <br/> |xs:integer  <br/> |Обязательный  <br/> |Указывает процентную вероятность осадков.  <br/> |Значение типа xs:integer  <br/> |
|shortday  <br/> |xs:string  <br/> |Обязательный  <br/> |Указывает день в сокращенной форме.  <br/> |Значение типа xs:string  <br/> |
|skycodeday  <br/> |xs:integer  <br/> |Обязательный  <br/> |Указывает код для прогнозируемых условий.  <br/> |Значение типа xs:integer  <br/> |
|skytextday  <br/> |xs:string  <br/> |Обязательный  <br/> |Указывает от одного до двух слов, описывая прогнозируемые условия.  <br/> |Значение типа xs:string  <br/> |
   

