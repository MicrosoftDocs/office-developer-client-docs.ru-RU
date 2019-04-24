---
title: Элемент RefBy (Тригжер_типе complexType) (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 09f2430a-184d-eaa2-2cb9-51bb24345c51
description: Указывает ссылку на страницу в документе.
ms.openlocfilehash: d987825345b64bd6e202970fc786aedaf49c6a94
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32348407"
---
# <a name="refby-element-triggertype-complextype-visio-xml"></a>Элемент RefBy (Тригжер_типе complexType) (' Visio XML ')

Указывает ссылку на страницу в документе.
  
## <a name="element-information"></a>Сведения об элементе

|||
|:-----|:-----|
|**Тип элемента** <br/> |[Рефби_типе](refby_type-complextypevisio-xml.md) <br/> |
|**Пространство имен** <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Файл схемы** <br/> |VisioSchema15. xsd  <br/> |
|**Части документа** <br/> ||
   
## <a name="definition"></a>Определение

```XML
< xs:element name="RefBy" type="RefBy_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a>Элементы и атрибуты

Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений. 
  
### <a name="parent-elements"></a>Родительские элементы

|**Элемент**|**Тип**|**Описание**|
|:-----|:-----|:-----|
|[Trigger](trigger-elementvisio-xml.md) <br/> |[Тригжер_типе](trigger_type-complextypevisio-xml.md) <br/> |В этой статье приведены инструкции по пересчету связей между частями документа в файле Visio в Microsoft Visio.  <br/> |

   
### <a name="child-elements"></a>Дочерние элементы

Нет.
  
### <a name="attributes"></a>Атрибуты

|**Атрибут**|**Тип**|**Обязательный**|**Описание**|**Возможные значения**|
|:-----|:-----|:-----|:-----|:-----|
|ИД  <br/> |XSD: Унсигнединт  <br/> |Обязательный  <br/> |Задает атрибут ID страницы в документе.  <br/> |Значения типа XSD: Унсигнединт.  <br/> |
|Д  <br/> |XSD: строка  <br/> |Обязательный  <br/> |Указывает тип ссылки.  <br/> |Значения типа String: XSD.  <br/> |
   

