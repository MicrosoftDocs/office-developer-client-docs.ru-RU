---
title: Курренттипе complexType (схема сведений о погоде Outlook)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 9f4663ac-13d3-6c46-f839-ba6bca4047a3
description: Определяет параметры для текущего положения прогноза погоды.
ms.openlocfilehash: 6dec923ce45ddc6470d80e1c973528246e01672f
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/29/2019
ms.locfileid: "34540989"
---
# <a name="currenttype-complextype-outlook-weather-information-schema"></a>Курренттипе complexType (схема сведений о погоде Outlook)

Определяет параметры для текущего положения прогноза погоды.
  
## <a name="type-information"></a>Сведения о типе

|||
|:-----|:-----|
|**Пространство имен** <br/> |http://schemas.microsoft.com/office/outlook/15/getweatherinfo.xsd  <br/> |
|**Файл схемы** <br/> |жетвеасеринфо. xsd  <br/> |
|**Базовый элемент расширения** <br/> |Отсутствует  <br/> |
   
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

Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений. 
  
### <a name="child-elements"></a>Дочерние элементы

Нет.
  
### <a name="attributes"></a>Атрибуты

|**Атрибут**|**Тип**|**Обязательный**|**Описание**|**Возможные значения**|
|:-----|:-----|:-----|:-----|:-----|
|date  <br/> |xs: Date  <br/> |Обязательный  <br/> |Указывает сегодняшнюю дату.  <br/> |Значение типа xs: Date  <br/> |
|открыт  <br/> |xs: String  <br/> |необязательный  <br/> |Указывает день для прогноза.  <br/> |Значение типа xs: String.  <br/> |
|филслике  <br/> |xs: integer  <br/> |Обязательный  <br/> |Указывает температуру, с которой понравится Текущая погода.  <br/> |Значение типа xs: integer  <br/> |
|хранени  <br/> |xs: integer  <br/> |Обязательный  <br/> |Задает текущее числовое значение влажности.  <br/> |Значение типа xs: integer  <br/> |
|обсерватионпоинт  <br/> |xs: String  <br/> |Обязательный  <br/> |Указывает, с каких сведений отражается текущая информация о погоде.  <br/> |Значение типа xs: String.  <br/> |
|обсерватионтиме  <br/> |xs: Time  <br/> |Обязательный  <br/> |Указывает, когда отражается текущая информация о погоде.  <br/> |Значение типа xs: Time  <br/> |
|шортдай  <br/> |xs: String  <br/> |необязательный  <br/> |Указывает день в сокращенной форме.  <br/> |Значение типа xs: String.  <br/> |
|скикоде  <br/> |xs: integer  <br/> |Обязательный  <br/> |Задает целочисленный код для текущих условий погоды.  <br/> |Значение типа xs: integer  <br/> |
|скитекст  <br/> |xs: String  <br/> |Обязательный  <br/> |Указывает одно на два слова, описывающих текущие условия погоды.  <br/> |Значение типа xs: String.  <br/> |
|Рабочая  <br/> |xs: integer  <br/> |Обязательный  <br/> |Задает текущую температуру расположения.  <br/> |Значение типа xs: integer  <br/> |
|винддисплай  <br/> |xs: String  <br/> |Обязательный  <br/> |Строка, описывающая текущие условия обмотки.  <br/> |Значение типа xs: String.  <br/> |
|виндспид  <br/> |xs: integer  <br/> |Обязательный  <br/> |Задает текущее числовое значение скорости обмотки.  <br/> |Значение типа xs: integer  <br/> |
   

