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
ms.openlocfilehash: 01604796d4460cc14005ee00ea6b8f46f04d4742
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32339566"
---
# <a name="forecast-element-weathertype-complextype-outlook-weather-information-schema"></a>элемент ПРЕДСКАЗ (Веасертипе complexType) (схема сведений о погоде Outlook)

Указывает будущие условия прогноза по крайней мере за три дня вперед, включая сегодняшние, завтра, завтра, после завтрашнего дня.
  
## <a name="element-information"></a>Сведения об элементе

|||
|:-----|:-----|
|**Тип элемента** <br/> |[Форекасттипе](forecasttype-complextype-outlook-weather-information-schema.md) <br/> |
|**Пространство имен** <br/> |https://schemas.microsoft.com/office/outlook/15/getweatherinfo.xsd  <br/> |
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
|[Погода](weather-element-weatherdata-elementoutlook-weather-information-schema.md) <br/> |[Веасертипе](weathertype-complextype-outlook-weather-information-schema.md) <br/> |Задает условия для расположения в прогнозе погоды.  <br/> |
   
### <a name="child-elements"></a>Дочерние элементы

Нет.
  
### <a name="attributes"></a>Атрибуты

|**Атрибут**|**Тип**|**Обязательный**|**Описание**|**Возможные значения**|
|:-----|:-----|:-----|:-----|:-----|
|дата  <br/> |xs: Date  <br/> |Обязательный  <br/> |Указывает дату для прогноза.  <br/> |Значение типа xs: Date  <br/> |
|открыт  <br/> |xs: String  <br/> |Обязательный  <br/> |Указывает день для прогноза.  <br/> |Значение типа xs: String.  <br/> |
|высокоуровневых  <br/> |xs: integer  <br/> |Обязательный  <br/> |Указывает прогнозируемую максимальную температуру.  <br/> |Значение типа xs: integer  <br/> |
|потребление  <br/> |xs: integer  <br/> |Обязательный  <br/> |Указывает прогнозируемую минимальную температуру.  <br/> |Значение типа xs: integer  <br/> |
|преЦип  <br/> |xs: integer  <br/> |Обязательный  <br/> |Указывает процентное отношение возможности преЦипитатион.  <br/> |Значение типа xs: integer  <br/> |
|шортдай  <br/> |xs: String  <br/> |Обязательный  <br/> |Указывает день в сокращенной форме.  <br/> |Значение типа xs: String.  <br/> |
|скикодедай  <br/> |xs: integer  <br/> |Обязательный  <br/> |Указывает код для прогнозируемых условий.  <br/> |Значение типа xs: integer  <br/> |
|скитекстдай  <br/> |xs: String  <br/> |Обязательный  <br/> |Указывает одно на два слова, описывающих прогнозируемые условия.  <br/> |Значение типа xs: String.  <br/> |
   

