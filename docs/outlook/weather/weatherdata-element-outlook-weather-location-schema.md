---
title: элемент WeatherData (схема местоположения погоды Outlook)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 14e0c469-31dc-fbe2-0d45-da602df04f13
description: Определяет элемент прогноза погоды.
ms.openlocfilehash: ade57264fab592d3314aa9a3376e129a5f3719c0
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25391313"
---
# <a name="weatherdata-element-outlook-weather-location-schema"></a>элемент WeatherData (схема местоположения погоды Outlook)

Определяет элемент прогноза погоды.
  
## <a name="element-information"></a>Сведения об элементе

|||
|:-----|:-----|
|**Тип элемента** <br/> ||
|**Пространство имен** <br/> |https://schemas.microsoft.com/office/outlook/15/getweatherlocation.xsd  <br/> |
|**Файл схемы** <br/> |getweatherlocation.xsd  <br/> |
   
## <a name="definition"></a>Определение

```XML
    <xs:element name="weatherdata"
    >
          <xs:complexType>
          <xs:sequence>
    <xs:element name="weather"
     type="weatherType" maxOccurs="unbounded"
      >
    </xs:element>
    
      </xs:sequence>
      </xs:complexType>
    </xs:element>
    
```

## <a name="elements-and-attributes"></a>Элементы и атрибуты

Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений. 
  
### <a name="parent-elements"></a>Родительские элементы

Нет.
  
### <a name="child-elements"></a>Дочерние элементы

|**Элемент**|**Тип**|**Описание**|
|:-----|:-----|:-----|
|[прогноза погоды](weather-element-weatherdata-elementoutlook-weather-location-schema.md) <br/> |[weatherType](weathertype-complextype-outlook-weather-location-schema.md) <br/> |Указывает местоположение для прогноза погоды отчет на.  <br/> |
   
### <a name="attributes"></a>Атрибуты

Нет.
  

