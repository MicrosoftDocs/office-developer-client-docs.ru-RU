---
title: forecastType complexType (схема сведения о погоде Outlook)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 6301d6b6-34fa-af8d-e682-605d35cfdf47
description: Определяет параметры о прогноза погоды расположения.
ms.openlocfilehash: 75f20d7857fac85e1e95d23cf5ac826336648132
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25390627"
---
# <a name="forecasttype-complextype-outlook-weather-information-schema"></a>forecastType complexType (схема сведения о погоде Outlook)

Определяет параметры о прогноза погоды расположения.
  
## <a name="type-information"></a>Сведения о типе

|||
|:-----|:-----|
|**Пространство имен** <br/> |https://schemas.microsoft.com/office/outlook/15/getweatherinfo.xsd  <br/> |
|**Файл схемы** <br/> |GetWeatherInfo.xsd  <br/> |
|**Базовый элемент расширения** <br/> |Отсутствует  <br/> |
   
## <a name="definition"></a>Определение

```XML
       <xs:complexType name="forecastType">
     <xs:attribute name="shortday"   type="xs:string"      use="required"     />
     <xs:attribute name="day"   type="xs:string"      use="required"     />
     <xs:attribute name="date"   type="xs:date"      use="required"     />
     <xs:attribute name="precip"   type="xs:integer"      use="required"     />
     <xs:attribute name="skytextday"   type="xs:string"      use="required"     />
     <xs:attribute name="skycodeday"   type="xs:integer"      use="required"     />
     <xs:attribute name="high"   type="xs:integer"      use="required"     />
     <xs:attribute name="low"   type="xs:integer"      use="required"     />
       </xs:complexType>

```

## <a name="elements-and-attributes"></a>Элементы и атрибуты

Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений. 
  
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
   

