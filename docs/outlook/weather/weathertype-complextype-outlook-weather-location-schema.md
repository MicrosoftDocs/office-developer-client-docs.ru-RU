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
ms.openlocfilehash: c3d640789cb68891878c3dca5210ab9dea280180
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25387715"
---
# <a name="weathertype-complextype-outlook-weather-location-schema"></a>weatherType complexType (схема местоположения погоды Outlook)

Определяет параметры о погоды расположения.
  
## <a name="type-information"></a>Сведения о типе

|||
|:-----|:-----|
|**Пространство имен** <br/> |https://schemas.microsoft.com/office/outlook/15/getweatherlocation.xsd  <br/> |
|**Файл схемы** <br/> |getweatherlocation.xsd  <br/> |
|**Базовый элемент расширения** <br/> |Отсутствует  <br/> |
   
## <a name="definition"></a>Определение

```XML
       <xs:complexType name="weatherType">
     <xs:attribute name="weatherlocationname"   type="xs:string"      use="required"     />
     <xs:attribute name="weatherlocationcode"   type="xs:string"      use="required"     />
       </xs:complexType>

```

## <a name="elements-and-attributes"></a>Элементы и атрибуты

Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений. 
  
### <a name="child-elements"></a>Дочерние элементы

Нет.
  
### <a name="attributes"></a>Атрибуты

|**Атрибут**|**Тип**|**Обязательный**|**Описание**|**Возможные значения**|
|:-----|:-----|:-----|:-----|:-----|
|weatherlocationcode  <br/> |xs:string  <br/> |Обязательный  <br/> |Указывает код, связанный с расположением для различения нескольких расположений с тем же именем.  <br/> |Значения типа xs: String  <br/> |
|weatherlocationname  <br/> |xs:string  <br/> |Обязательный  <br/> |Указывает имя расположения.  <br/> |Значения типа xs: String  <br/> |
   

