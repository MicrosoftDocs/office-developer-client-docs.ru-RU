---
title: Элемент RuleSet (RuleSets_Type ComplexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 5ca63b8a-782e-211f-be7a-8e177b61d8fc
description: Представляет один набор правил проверки диаграммы.
ms.openlocfilehash: c6fc8df6d9c84f44496d69207dfb9cfb878659e3
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/29/2019
ms.locfileid: "34541640"
---
# <a name="ruleset-element-rulesets_type-complextype-visio-xml"></a>Элемент RuleSet (RuleSets_Type ComplexType) (Visio XML)

Представляет один набор правил проверки диаграммы.
  
## <a name="element-information"></a>Сведения об элементе

|||
|:-----|:-----|
|**Тип элемента** <br/> |[RuleSet_Type](ruleset_type-complextypevisio-xml.md) <br/> |
|**Пространство имен** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Файл схемы** <br/> |VisioSchema15.xsd  <br/> |
|**Части документов** <br/> |validation.xml  <br/> |
   
## <a name="definition"></a>Определение

```XML
< xs:element name="RuleSet" type="RuleSet_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a>Элементы и атрибуты

Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений. 
  
### <a name="parent-elements"></a>Родительские элементы

|**Элемент**|**Тип**|**Описание**|
|:-----|:-----|:-----|
|[RuleSets](rulesets-element-validation_type-complextypevisio-xml.md) <br/> |[RuleSets_Type](rulesets_type-complextypevisio-xml.md) <br/> |Включает элемент **RuleSet** для каждого правила проверки, за набором в документе.  <br/> |
   
### <a name="child-elements"></a>Дочерние элементы

|**Элемент**|**Тип**|**Описание**|
|:-----|:-----|:-----|
|[Rule](rule-element-ruleset_type-complextypevisio-xml.md) <br/> |[Rule_Type](rule_type-complextypevisio-xml.md) <br/> |Представляет одно правило проверки в наборе правил проверки схемы.  <br/> |
|[RuleSetFlags](rulesetflags-element-ruleset_type-complextypevisio-xml.md) <br/> |[RuleSetFlags_Type](rulesetflags_type-complextypevisio-xml.md) <br/> |Указывает свойства набора правил.  <br/> |
   
### <a name="attributes"></a>Атрибуты

|**Атрибут**|**Тип**|**Обязательный**|**Описание**|**Возможные значения**|
|:-----|:-----|:-----|:-----|:-----|
|Описание  <br/> |xsd:string  <br/> |необязательный  <br/> |Указывает описание, которое отображается в пользовательском интерфейсе для набора правил проверки. По умолчанию это пустая строка.  <br/> |Значения типа xsd:string.  <br/> |
|Включено  <br/> |xsd:boolean  <br/> |необязательный  <br/> |Указывает, проверяются ли правила в указанном наборе правил проверки при запуске проверки для текущего документа. Значение по умолчанию — True.  <br/> |Значения типа xsd:boolean.  <br/> |
|ID  <br/> |xsd:unsignedInt  <br/> |Обязательный  <br/> |Указывает уникальный идентификатор набора правил проверки.  <br/> |Значения типа xsd:unsignedInt.  <br/> |
|Имя  <br/> |xsd:string  <br/> |необязательный  <br/> |Указывает локальное имя набора правил проверки. Значение атрибута NameU по умолчанию.  <br/> |Значения типа xsd:string.  <br/> |
|NameU  <br/> |xsd:string  <br/> |Обязательный  <br/> |Указывает универсальное имя набора правил проверки.  <br/> |Значения типа xsd:string.  <br/> |
   

