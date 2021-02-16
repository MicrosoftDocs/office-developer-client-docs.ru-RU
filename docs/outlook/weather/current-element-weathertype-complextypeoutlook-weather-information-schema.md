---
title: current element (weatherType complexType) (Outlook Weather Information Schema)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: d592a396-f935-c44c-409f-b849c327cfbd
description: Указывает текущие прогнозы погоды.
ms.openlocfilehash: 1303212da1336112599ae5328498cca0d4ab5f89
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/29/2019
ms.locfileid: "34541010"
---
# <a name="current-element-weathertype-complextype-outlook-weather-information-schema"></a>current element (weatherType complexType) (Outlook Weather Information Schema)

Указывает текущие прогнозы погоды.
  
## <a name="element-information"></a>Сведения об элементе

|||
|:-----|:-----|
|**Тип элемента** <br/> |[currentType](currenttype-complextype-outlook-weather-information-schema.md) <br/> |
|**Пространство имен** <br/> |http://schemas.microsoft.com/office/outlook/15/getweatherinfo.xsd  <br/> |
|**Файл схемы** <br/> |getweatherinfo.xsd  <br/> |
   
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
|[погода](weather-element-weatherdata-elementoutlook-weather-information-schema.md) <br/> |[weatherType](weathertype-complextype-outlook-weather-information-schema.md) <br/> |Указывает погоду расположения.  <br/> |
   
### <a name="child-elements"></a>Дочерние элементы

Нет.
  
### <a name="attributes"></a>Атрибуты

|**Атрибут**|**Тип**|**Обязательный**|**Описание**|**Возможные значения**|
|:-----|:-----|:-----|:-----|:-----|
|date  <br/> |xs:date  <br/> |Обязательный  <br/> |Указывает сегодня.  <br/> |Значение типа xs:date  <br/> |
|day  <br/> |xs:string  <br/> |необязательный  <br/> |Указывает день для прогноза.  <br/> |Значение типа xs:string  <br/> |
|feelslike  <br/> |xs:integer  <br/> |Обязательный  <br/> |Указывает температуру текущей погоды.  <br/> |Значение типа xs:integer  <br/> |
|humidity  <br/> |xs:integer  <br/> |Обязательный  <br/> |Указывает текущее числовое значение влажности.  <br/> |Значение типа xs:integer  <br/> |
|observationpoint  <br/> |xs:string  <br/> |Обязательный  <br/> |Указывает, откуда наблюдается текущая информация о погоде.  <br/> |Значение типа xs:string  <br/> |
|observationtime  <br/> |xs:time  <br/> |Обязательный  <br/> |Указывает, когда будут наблюдаться текущие сведения о погоде.  <br/> |Значение типа xs:time  <br/> |
|shortday  <br/> |xs:string  <br/> |необязательный  <br/> |Указывает день в сокращенной форме.  <br/> |Значение типа xs:string  <br/> |
|skycode  <br/> |xs:integer  <br/> |Обязательный  <br/> |Указывает код для текущего состояния погоды.  <br/> |Значение типа xs:integer  <br/> |
|skytext  <br/> |xs:string  <br/> |Обязательный  <br/> |Указывает от одного до двух слов, описывающих текущие прогнозы погоды.  <br/> |Значение типа xs:string  <br/> |
|temperature  <br/> |xs:integer  <br/> |Обязательный  <br/> |Указывает текущую температуру расположения.  <br/> |Значение типа xs:integer  <br/> |
|winddisplay  <br/> |xs:string  <br/> |Обязательный  <br/> |Строка, описывающая текущие условия ветвей.  <br/> |Значение типа xs:string  <br/> |
|edpeed  <br/> |xs:integer  <br/> |Обязательный  <br/> |Указывает текущее числовое значение скорости ветвей.  <br/> |Значение типа xs:integer  <br/> |
   

