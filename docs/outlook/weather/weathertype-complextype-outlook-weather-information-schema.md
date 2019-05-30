---
title: Веасертипе complexType (схема сведений о погоде Outlook)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: b94d848e-868a-5d5e-ad82-39ed9bd5b357
description: Задает условия для расположения в прогнозе погоды.
ms.openlocfilehash: ac7b8f37e71da203db0f6aefc8e20b29e810c3cf
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/29/2019
ms.locfileid: "34542949"
---
# <a name="weathertype-complextype-outlook-weather-information-schema"></a>Веасертипе complexType (схема сведений о погоде Outlook)

Задает условия для расположения в прогнозе погоды.
  
## <a name="type-information"></a>Сведения о типе

|||
|:-----|:-----|
|**Пространство имен** <br/> |http://schemas.microsoft.com/office/outlook/15/getweatherinfo.xsd  <br/> |
|**Файл схемы** <br/> |жетвеасеринфо. xsd  <br/> |
|**Базовый элемент расширения** <br/> |Отсутствует  <br/> |
   
## <a name="definition"></a>Определение

```XML
           <xs:complexType name="weatherType">
           <xs:sequence>
     <xs:element name="current"      type="currentType">
  </xs:element>  
     <xs:element name="forecast"      type="forecastType" minOccurs="3"     maxOccurs="unbounded"    >
  </xs:element>  
       </xs:sequence>
     <xs:attribute name="weatherlocationcode"   type="xs:string"      use="required"     />
     <xs:attribute name="timezone"   type="xs:integer"      use="required"     />
     <xs:attribute name="attribution"   type="xs:string"      use="required"     />
     <xs:attribute name="degreetype"   type="xs:string"      use="required"     />
     <xs:attribute name="imagerelativeurl"   type="xs:string"      use="required"     />
     <xs:attribute name="url"   type="xs:string"      use="required"     />
     <xs:attribute name="weatherlocationname"   type="xs:string"      use="required"     />
       </xs:complexType>

```

## <a name="elements-and-attributes"></a>Элементы и атрибуты

Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений. 
  
### <a name="child-elements"></a>Дочерние элементы

|**Элемент**|**Тип**|**Описание**|
|:-----|:-----|:-----|
|[этой](current-element-weathertype-complextypeoutlook-weather-information-schema.md) <br/> |[Курренттипе](currenttype-complextype-outlook-weather-information-schema.md) <br/> |Задает текущие условия погоды.  <br/> |
|[прогнозирует](forecast-element-weathertype-complextypeoutlook-weather-information-schema.md) <br/> |[Форекасттипе](forecasttype-complextype-outlook-weather-information-schema.md) <br/> |Указывает будущие условия прогноза по крайней мере за три дня вперед, включая сегодняшние, завтра, завтра, после завтрашнего дня.  <br/> |
   
### <a name="attributes"></a>Атрибуты

|**Атрибут**|**Тип**|**Обязательный**|**Описание**|**Возможные значения**|
|:-----|:-----|:-----|:-----|:-----|
|Attribution  <br/> |xs: String  <br/> |Обязательный  <br/> |Указывает источник сведений о погоде.  <br/> |Значение типа xs: String.  <br/> |
|дегритипе  <br/> |xs: String  <br/> |Обязательный  <br/> |Задает единицу измерения температуры местоположения, например "Цельсия".  <br/> |C, F  <br/> |
|имажерелативеурл  <br/> |xs: String  <br/> |Обязательный  <br/> |Задает URL-адрес изображения для расположения.  <br/> |Значение типа xs: String.  <br/> |
|часовой  <br/> |xs: integer  <br/> |Обязательный  <br/> |Указывает смещение GMT.  <br/> |Значение в диапазоне от – 11 до 12 включительно  <br/> |
|url  <br/> |xs: String  <br/> |Обязательный  <br/> |Задает URL-адрес веб-страницы службы погоды, содержащей сведения о погоде для указанного расположения.  <br/> |Значение типа xs: String.  <br/> |
|веасерлокатионкоде  <br/> |xs: String  <br/> |Обязательный  <br/> |Указывает код, связанный с расположением, используемым для различения нескольких расположений с одинаковыми именами.  <br/> |Значение типа xs: String.  <br/> |
|веасерлокатионнаме  <br/> |xs: String  <br/> |Обязательный  <br/> |Задает имя расположения, которое отображается в раскрывающемся элементе управления.  <br/> |Значение типа xs: String.  <br/> |
   

