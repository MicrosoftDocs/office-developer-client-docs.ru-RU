---
title: Current Element (Веасертипе complexType) (схема сведений о погоде Outlook)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: d592a396-f935-c44c-409f-b849c327cfbd
description: Задает текущие условия погоды.
ms.openlocfilehash: ce92bdd49ee37f939748586c2d63d8a664f664d2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32351473"
---
# <a name="current-element-weathertype-complextype-outlook-weather-information-schema"></a>Current Element (Веасертипе complexType) (схема сведений о погоде Outlook)

Задает текущие условия погоды.
  
## <a name="element-information"></a>Сведения об элементе

|||
|:-----|:-----|
|**Тип элемента** <br/> |[Курренттипе](currenttype-complextype-outlook-weather-information-schema.md) <br/> |
|**Пространство имен** <br/> |https://schemas.microsoft.com/office/outlook/15/getweatherinfo.xsd  <br/> |
|**Файл схемы** <br/> |жетвеасеринфо. xsd  <br/> |
   
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
|[Погода](weather-element-weatherdata-elementoutlook-weather-information-schema.md) <br/> |[Веасертипе](weathertype-complextype-outlook-weather-information-schema.md) <br/> |Задает условия для расположения в прогнозе погоды.  <br/> |
   
### <a name="child-elements"></a>Дочерние элементы

Нет.
  
### <a name="attributes"></a>Атрибуты

|**Атрибут**|**Тип**|**Обязательный**|**Описание**|**Возможные значения**|
|:-----|:-----|:-----|:-----|:-----|
|дата  <br/> |xs: Date  <br/> |Обязательный  <br/> |Указывает сегодняшнюю дату.  <br/> |Значение типа xs: Date  <br/> |
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
   

