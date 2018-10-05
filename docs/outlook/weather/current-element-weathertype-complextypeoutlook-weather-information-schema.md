---
title: текущий элемент (weatherType complexType) (схема сведения о погоде Outlook)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: d592a396-f935-c44c-409f-b849c327cfbd
description: Указывает текущий погоды.
ms.openlocfilehash: ce92bdd49ee37f939748586c2d63d8a664f664d2
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25401092"
---
# <a name="current-element-weathertype-complextype-outlook-weather-information-schema"></a>текущий элемент (weatherType complexType) (схема сведения о погоде Outlook)

Указывает текущий погоды.
  
## <a name="element-information"></a>Сведения об элементе

|||
|:-----|:-----|
|**Тип элемента** <br/> |[currentType](currenttype-complextype-outlook-weather-information-schema.md) <br/> |
|**Пространство имен** <br/> |https://schemas.microsoft.com/office/outlook/15/getweatherinfo.xsd  <br/> |
|**Файл схемы** <br/> |GetWeatherInfo.xsd  <br/> |
   
## <a name="definition"></a>Определение

```XML
<xs:element name="current"      type="currentType">
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
|date  <br/> |xs: Date  <br/> |Обязательный  <br/> |Задает текущую дату.  <br/> |Значения типа xs: Date  <br/> |
|день  <br/> |xs:string  <br/> |необязательный  <br/> |Задает день для прогноза.  <br/> |Значения типа xs: String  <br/> |
|feelslike  <br/> |xs:integer  <br/> |Обязательный  <br/> |Указывает, как текущий прогноза погоды, в том числе как температуры.  <br/> |Значения типа xs: Integer  <br/> |
|влажность  <br/> |xs:integer  <br/> |Обязательный  <br/> |Задает текущее значение числовых влажность.  <br/> |Значения типа xs: Integer  <br/> |
|observationpoint  <br/> |xs:string  <br/> |Обязательный  <br/> |Указывает, где наблюдается из текущей информации о погоде.  <br/> |Значения типа xs: String  <br/> |
|observationtime  <br/> |xs: Time  <br/> |Обязательный  <br/> |Указывает, когда наблюдаемое текущей информации о погоде в.  <br/> |Значения типа xs: Time  <br/> |
|shortday  <br/> |xs:string  <br/> |необязательный  <br/> |Задает день сокращенную форму.  <br/> |Значения типа xs: String  <br/> |
|skycode  <br/> |xs:integer  <br/> |Обязательный  <br/> |Указывает целочисленный код для текущей погоды.  <br/> |Значения типа xs: Integer  <br/> |
|skytext  <br/> |xs:string  <br/> |Обязательный  <br/> |Задает один или два слова, описывающие сводки погоды.  <br/> |Значения типа xs: String  <br/> |
|температура  <br/> |xs:integer  <br/> |Обязательный  <br/> |Задает текущую температуру расположения.  <br/> |Значения типа xs: Integer  <br/> |
|winddisplay  <br/> |xs:string  <br/> |Обязательный  <br/> |Строка, описывающая текущие условия устройство.  <br/> |Значения типа xs: String  <br/> |
|windspeed  <br/> |xs:integer  <br/> |Обязательный  <br/> |Задает текущее значение скорости числовых устройство.  <br/> |Значения типа xs: Integer  <br/> |
   

