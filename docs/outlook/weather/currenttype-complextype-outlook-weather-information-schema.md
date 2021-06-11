---
title: currentType complexType (Outlook схема сведений о погоде)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 9f4663ac-13d3-6c46-f839-ba6bca4047a3
description: Определяет параметры текущих погодных условий расположения.
ms.openlocfilehash: 6dec923ce45ddc6470d80e1c973528246e01672f
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/29/2019
ms.locfileid: "34540989"
---
# <a name="currenttype-complextype-outlook-weather-information-schema"></a>currentType complexType (Outlook схема сведений о погоде)

Определяет параметры текущих погодных условий расположения.
  
## <a name="type-information"></a>Сведения о типе

|||
|:-----|:-----|
|**Пространство имен** <br/> |http://schemas.microsoft.com/office/outlook/15/getweatherinfo.xsd  <br/> |
|**Файл схемы** <br/> |getweatherinfo.xsd  <br/> |
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
|date  <br/> |xs:date  <br/> |Обязательный  <br/> |Указывает дату сегодняшнего дня.  <br/> |Значение типа xs:date  <br/> |
|день  <br/> |xs:string  <br/> |необязательный  <br/> |Указывает день для прогноза.  <br/> |Значение типа xs:string  <br/> |
|feelslike  <br/> |xs:integer  <br/> |Обязательный  <br/> |Указывает температуру текущего погодных условий.  <br/> |Значение типа xs:integer  <br/> |
|влажность  <br/> |xs:integer  <br/> |Обязательный  <br/> |Указывает текущее числовое значение влажности.  <br/> |Значение типа xs:integer  <br/> |
|точка наблюдения  <br/> |xs:string  <br/> |Обязательный  <br/> |Указывает, откуда наблюдается текущая информация о погоде.  <br/> |Значение типа xs:string  <br/> |
|время наблюдения  <br/> |xs:time  <br/> |Обязательный  <br/> |Указывает, когда наблюдается текущая информация о погоде.  <br/> |Значение типа xs:time  <br/> |
|shortday  <br/> |xs:string  <br/> |необязательный  <br/> |Указывает день в сокращенной форме.  <br/> |Значение типа xs:string  <br/> |
|skycode  <br/> |xs:integer  <br/> |Обязательный  <br/> |Указывает код для текущих погодных условий.  <br/> |Значение типа xs:integer  <br/> |
|skytext  <br/> |xs:string  <br/> |Обязательный  <br/> |Указывает от одного до двух слов, описывающих текущие погодные условия.  <br/> |Значение типа xs:string  <br/> |
|температура  <br/> |xs:integer  <br/> |Обязательный  <br/> |Указывает текущую температуру расположения.  <br/> |Значение типа xs:integer  <br/> |
|winddisplay  <br/> |xs:string  <br/> |Обязательный  <br/> |Строка, описывающая текущие условия ветра.  <br/> |Значение типа xs:string  <br/> |
|windspeed  <br/> |xs:integer  <br/> |Обязательный  <br/> |Указывает текущее числовое значение скорости ветра.  <br/> |Значение типа xs:integer  <br/> |
   

