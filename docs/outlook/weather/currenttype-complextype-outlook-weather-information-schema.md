---
title: currentType complexType (схема сведения о погоде Outlook)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 9f4663ac-13d3-6c46-f839-ba6bca4047a3
description: Определяет параметры о текущем погоды расположения.
ms.openlocfilehash: 55ea2cfa6904d88c695268675bc7a893fa643010
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19812850"
---
# <a name="currenttype-complextype-outlook-weather-information-schema"></a>currentType complexType (схема сведения о погоде Outlook)

Определяет параметры о текущем погоды расположения.
  
## <a name="type-information"></a>Сведения о типе

|||
|:-----|:-----|
|**Пространство имен** <br/> |http://schemas.microsoft.com/office/outlook/15/getweatherinfo.xsd  <br/> |
|**Файл схемы** <br/> |GetWeatherInfo.xsd  <br/> |
|**База расширения** <br/> |Нет  <br/> |
   
## <a name="definition"></a>Определение

```XML
       <xs:complexType name="currentType">
     <xs:attribute name="winddisplay"   type="xs:string"      use="required"     />
     <xs:attribute name="windspeed"   type="xs:integer"      use="required"     />
     <xs:attribute name="humidity"   type="xs:integer"      use="required"     />
     <xs:attribute name="feelslike"   type="xs:integer"      use="required"     />
     <xs:attribute name="observationpoint"   type="xs:string"      use="required"     />
     <xs:attribute name="observationtime"   type="xs:time"      use="required"     />
     <xs:attribute name="date"   type="xs:date"      use="required"     />
     <xs:attribute name="skytext"   type="xs:string"      use="required"     />
     <xs:attribute name="skycode"   type="xs:integer"      use="required"     />
     <xs:attribute name="temperature"   type="xs:integer"      use="required"     />
     <xs:attribute name="shortday"   type="xs:string"      use="optional"     />
     <xs:attribute name="day"   type="xs:string"      use="optional"     />
       </xs:complexType>

```

## <a name="elements-and-attributes"></a>Элементы и атрибуты

Если схема определяет специальные требования, такие как **последовательность**, **minOccurs**, **maxOccurs**и **выбора**, обратитесь к разделу определение. 
  
### <a name="child-elements"></a>Дочерние элементы

Нет.
  
### <a name="attributes"></a>Атрибуты

|**Атрибут**|**Тип**|**Обязательное**|**Описание**|**Возможные значения**|
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
   

