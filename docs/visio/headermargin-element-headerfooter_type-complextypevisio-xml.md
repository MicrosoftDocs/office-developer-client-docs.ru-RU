---
title: Элемент HeaderMargin (Хеадерфутер_типе complexType) (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 2bb0f4c5-eacf-e09b-2fce-dcff2d927557
description: Задает поле заголовка документа.
ms.openlocfilehash: d8126ae73b1fb330234698343d14468fcbb3eed8
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32351669"
---
# <a name="headermargin-element-headerfootertype-complextype-visio-xml"></a>Элемент HeaderMargin (Хеадерфутер_типе complexType) (' Visio XML ')

Задает поле заголовка документа.
  
## <a name="element-information"></a>Сведения об элементе

|||
|:-----|:-----|
|**Тип элемента** <br/> |[Хеадермаргин_типе](headermargin_type-complextypevisio-xml.md) <br/> |
|**Пространство имен** <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Файл схемы** <br/> |VisioSchema15. xsd  <br/> |
|**Части документа** <br/> |Document. XML  <br/> |
   
## <a name="definition"></a>Определение

```XML
< xs:element name="HeaderMargin" type="HeaderMargin_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a>Элементы и атрибуты

Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений. 
  
### <a name="parent-elements"></a>Родительские элементы

|**Элемент**|**Тип**|**Описание**|
|:-----|:-----|:-----|
|[HeaderFooter](headerfooter-element-visiodocument_type-complextypevisio-xml.md) <br/> |[Хеадерфутер_типе](headerfooter_type-complextypevisio-xml.md) <br/> |Содержит элементы для верхнего и нижнего колонтитулов документа.  <br/> |
   
### <a name="child-elements"></a>Дочерние элементы

Нет.
  
### <a name="attributes"></a>Атрибуты

|**Атрибут**|**Тип**|**Обязательный**|**Описание**|**Возможные значения**|
|:-----|:-----|:-----|:-----|:-----|
|Устройств  <br/> |XSD: строка  <br/> |необязательный  <br/> |Представляет единицу измерения. Значение по умолчанию — DP.  <br/> |Значения типа String: XSD.  <br/> |
   

