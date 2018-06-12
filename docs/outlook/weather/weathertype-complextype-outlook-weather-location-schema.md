---
title: weatherType complexType (схема местоположения погоды Outlook)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f8054fd9-85ba-fcf6-c96d-a54095d5238c
description: Определяет параметры о погоды расположения.
ms.openlocfilehash: 39dcc63dfc9b7a97b9643e804329fd1795d39201
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19812935"
---
# <a name="weathertype-complextype-outlook-weather-location-schema"></a>weatherType complexType (схема местоположения погоды Outlook)

Определяет параметры о погоды расположения.
  
## <a name="type-information"></a>Сведения о типе

|||
|:-----|:-----|
|**Пространство имен** <br/> |http://schemas.microsoft.com/office/outlook/15/getweatherlocation.xsd  <br/> |
|**Файл схемы** <br/> |getweatherlocation.xsd  <br/> |
|**База расширения** <br/> |Нет  <br/> |
   
## <a name="definition"></a>Определение

```XML
       <xs:complexType name="weatherType">
     <xs:attribute name="weatherlocationname"   type="xs:string"      use="required"     />
     <xs:attribute name="weatherlocationcode"   type="xs:string"      use="required"     />
       </xs:complexType>

```

## <a name="elements-and-attributes"></a>Элементы и атрибуты

Если схема определяет специальные требования, такие как **последовательность**, **minOccurs**, **maxOccurs**и **выбора**, обратитесь к разделу определение. 
  
### <a name="child-elements"></a>Дочерние элементы

Нет.
  
### <a name="attributes"></a>Атрибуты

|**Атрибут**|**Тип**|**Обязательное**|**Описание**|**Возможные значения**|
|:-----|:-----|:-----|:-----|:-----|
|weatherlocationcode  <br/> |xs:string  <br/> |Обязательный  <br/> |Указывает код, связанный с расположением для различения нескольких расположений с тем же именем.  <br/> |Значения типа xs: String  <br/> |
|weatherlocationname  <br/> |xs:string  <br/> |Обязательный  <br/> |Указывает имя расположения.  <br/> |Значения типа xs: String  <br/> |
   

