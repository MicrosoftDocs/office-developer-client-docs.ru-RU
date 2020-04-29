---
title: элемент ПРЕДСКАЗ (Веасертипе complexType) (схема сведений о погоде Outlook)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 9124fa30-d58b-8354-91e9-8d2237a8251d
description: Указывает будущие условия прогноза по крайней мере за три дня вперед, включая сегодняшние, завтра, завтра, после завтрашнего дня.
ms.openlocfilehash: 5e442ee5995bbd51c5e518162286bc199a625dbd
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/29/2019
ms.locfileid: "34540982"
---
# <a name="forecast-element-weathertype-complextype-outlook-weather-information-schema"></a>элемент ПРЕДСКАЗ (Веасертипе complexType) (схема сведений о погоде Outlook)

Указывает будущие условия прогноза по крайней мере за три дня вперед, включая сегодняшние, завтра, завтра, после завтрашнего дня.
  
## <a name="element-information"></a>Сведения об элементе

|||
|:-----|:-----|
|**Тип элемента** <br/> |[форекасттипе](forecasttype-complextype-outlook-weather-information-schema.md) <br/> |
|**Пространство имен** <br/> |http://schemas.microsoft.com/office/outlook/15/getweatherinfo.xsd  <br/> |
|**Файл схемы** <br/> |жетвеасеринфо. xsd  <br/> |
   
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
|[Погода](weather-element-weatherdata-elementoutlook-weather-information-schema.md) <br/> |[веасертипе](weathertype-complextype-outlook-weather-information-schema.md) <br/> |Задает условия для расположения в прогнозе погоды.  <br/> |
   
### <a name="child-elements"></a>Дочерние элементы

Нет.
  
### <a name="attributes"></a>Атрибуты

|**Атрибут**|**Тип**|**Обязательный**|**Описание**|**Возможные значения**|
|:-----|:-----|:-----|:-----|:-----|
|date  <br/> |xs: Date  <br/> |Обязательный  <br/> |Указывает дату для прогноза.  <br/> |Значение типа xs: Date  <br/> |
|открыт  <br/> |xs: String  <br/> |Обязательный  <br/> |Указывает день для прогноза.  <br/> |Значение типа xs: String.  <br/> |
|высокоуровневых  <br/> |xs: integer  <br/> |Обязательный  <br/> |Указывает прогнозируемую максимальную температуру.  <br/> |Значение типа xs: integer  <br/> |
|потребление  <br/> |xs: integer  <br/> |Обязательный  <br/> |Указывает прогнозируемую минимальную температуру.  <br/> |Значение типа xs: integer  <br/> |
|преЦип  <br/> |xs: integer  <br/> |Обязательный  <br/> |Указывает процентное отношение возможности преЦипитатион.  <br/> |Значение типа xs: integer  <br/> |
|шортдай  <br/> |xs: String  <br/> |Обязательный  <br/> |Указывает день в сокращенной форме.  <br/> |Значение типа xs: String.  <br/> |
|скикодедай  <br/> |xs: integer  <br/> |Обязательный  <br/> |Указывает код для прогнозируемых условий.  <br/> |Значение типа xs: integer  <br/> |
|скитекстдай  <br/> |xs: String  <br/> |Обязательный  <br/> |Указывает одно на два слова, описывающих прогнозируемые условия.  <br/> |Значение типа xs: String.  <br/> |
   

