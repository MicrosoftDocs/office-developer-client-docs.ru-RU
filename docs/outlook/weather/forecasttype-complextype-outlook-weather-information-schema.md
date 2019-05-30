---
title: Форекасттипе complexType (схема сведений о погоде Outlook)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 6301d6b6-34fa-af8d-e682-605d35cfdf47
description: Определяет параметры прогноза погоды для местоположения.
ms.openlocfilehash: e799ebbea72daa1788aedbdcadbc523b5e4dff0d
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/29/2019
ms.locfileid: "34540954"
---
# <a name="forecasttype-complextype-outlook-weather-information-schema"></a>Форекасттипе complexType (схема сведений о погоде Outlook)

Определяет параметры прогноза погоды для местоположения.
  
## <a name="type-information"></a>Сведения о типе

|||
|:-----|:-----|
|**Пространство имен** <br/> |http://schemas.microsoft.com/office/outlook/15/getweatherinfo.xsd  <br/> |
|**Файл схемы** <br/> |жетвеасеринфо. xsd  <br/> |
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
|date  <br/> |xs: Date  <br/> |Обязательный  <br/> |Указывает дату для прогноза.  <br/> |Значение типа xs: Date  <br/> |
|открыт  <br/> |xs: String  <br/> |Обязательный  <br/> |Указывает день для прогноза.  <br/> |Значение типа xs: String.  <br/> |
|высокоуровневых  <br/> |xs: integer  <br/> |Обязательный  <br/> |Указывает прогнозируемую максимальную температуру.  <br/> |Значение типа xs: integer  <br/> |
|потребление  <br/> |xs: integer  <br/> |Обязательный  <br/> |Указывает прогнозируемую минимальную температуру.  <br/> |Значение типа xs: integer  <br/> |
|преЦип  <br/> |xs: integer  <br/> |Обязательный  <br/> |Указывает процентное отношение возможности преЦипитатион.  <br/> |Значение типа xs: integer  <br/> |
|шортдай  <br/> |xs: String  <br/> |Обязательный  <br/> |Указывает день в сокращенной форме.  <br/> |Значение типа xs: String.  <br/> |
|скикодедай  <br/> |xs: integer  <br/> |Обязательный  <br/> |Указывает код для прогнозируемых условий.  <br/> |Значение типа xs: integer  <br/> |
|скитекстдай  <br/> |xs: String  <br/> |Обязательный  <br/> |Указывает одно на два слова, описывающих прогнозируемые условия.  <br/> |Значение типа xs: String.  <br/> |
   

