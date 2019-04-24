---
title: Элемент Рулефилтер (Руле_типе complexType) (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: b05497e6-722f-9203-e03c-0f14a712cddb
description: Задает логическое выражение, определяющее, следует ли применять правило проверки к целевому объекту.
ms.openlocfilehash: 8d4167fbb8dde54c55e49debb77fe307ecab6771
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32349387"
---
# <a name="rulefilter-element-ruletype-complextype-visio-xml"></a>Элемент Рулефилтер (Руле_типе complexType) (' Visio XML ')

Задает логическое выражение, определяющее, следует ли применять правило проверки к целевому объекту.
  
## <a name="element-information"></a>Сведения об элементе

|||
|:-----|:-----|
|**Тип элемента** <br/> |[Рулефилтер_типе](rulefilter_type-complextypevisio-xml.md) <br/> |
|**Пространство имен** <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Файл схемы** <br/> |VisioSchema15. xsd  <br/> |
|**Части документа** <br/> |Проверка. XML  <br/> |
   
## <a name="definition"></a>Определение

```XML
< xs:element name="RuleFilter" type="RuleFilter_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a>Элементы и атрибуты

Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений. 
  
### <a name="parent-elements"></a>Родительские элементы

|**Элемент**|**Тип**|**Описание**|
|:-----|:-----|:-----|
|[Rule](rule-element-ruleset_type-complextypevisio-xml.md) <br/> |[Руле_типе](rule_type-complextypevisio-xml.md) <br/> |Представляет одно правило проверки в наборе правил проверки схемы.  <br/> |
   
### <a name="child-elements"></a>Дочерние элементы

Нет.
  
### <a name="attributes"></a>Атрибуты

|**Атрибут**|**Тип**|**Обязательный**|**Описание**|**Возможные значения**|
|:-----|:-----|:-----|:-----|:-----|
|Формула  <br/> |XSD: строка  <br/> |необязательный  <br/> |Представляет формулу элемента.  <br/> |Значения объекта XSD: String.  <br/> |
   

