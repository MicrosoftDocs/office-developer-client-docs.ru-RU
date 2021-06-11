---
title: Элемент правила (RuleSet_Type Type) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: fcd22f3a-c8e8-1133-160c-fe26e612a15d
description: Представляет одно правило проверки в наборе правил проверки схемы.
ms.openlocfilehash: 0d848ce3309d7dfc5a89b201be30ce060ec6f88f
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/29/2019
ms.locfileid: "34541710"
---
# <a name="rule-element-ruleset_type-complextype-visio-xml"></a>Элемент правила (RuleSet_Type Type) (Visio XML)

Представляет одно правило проверки в наборе правил проверки схемы.
  
## <a name="element-information"></a>Сведения об элементе

|||
|:-----|:-----|
|**Тип элемента** <br/> |[Rule_Type](rule_type-complextypevisio-xml.md) <br/> |
|**Пространство имен** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Файл схемы** <br/> |VisioSchema15.xsd  <br/> |
|**Части документов** <br/> |validation.xml  <br/> |
   
## <a name="definition"></a>Определение

```XML
< xs:element name="Rule" type="Rule_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a>Элементы и атрибуты

Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений. 
  
### <a name="parent-elements"></a>Родительские элементы

|**Элемент**|**Тип**|**Описание**|
|:-----|:-----|:-----|
|[RuleSet](ruleset-element-rulesets_type-complextypevisio-xml.md) <br/> |[RuleSet_Type](ruleset_type-complextypevisio-xml.md) <br/> |Представляет один набор правил проверки диаграммы.  <br/> |
   
### <a name="child-elements"></a>Дочерние элементы

|**Элемент**|**Тип**|**Описание**|
|:-----|:-----|:-----|
|[RuleFilter](rulefilter-element-rule_type-complextypevisio-xml.md) <br/> |[RuleFilter_Type](rulefilter_type-complextypevisio-xml.md) <br/> |Указывает логическое выражение, которое определяет, следует ли применять правило проверки к целевому объекту.  <br/> |
|[RuleTest](ruletest-element-rule_type-complextypevisio-xml.md) <br/> |[RuleTest_Type](ruletest_type-complextypevisio-xml.md) <br/> |Указывает логическое выражение, которое определяет, удовлетворяет ли целевой объект правилу проверки.  <br/> |
   
### <a name="attributes"></a>Атрибуты

|**Атрибут**|**Тип**|**Обязательный**|**Описание**|**Возможные значения**|
|:-----|:-----|:-----|:-----|:-----|
|Category  <br/> |xsd:string  <br/> |необязательный  <br/> |Указывает текст, отображаемый в столбце **Категория** окна "Проблемы". По умолчанию это пустая строка.  <br/> |Значения типа xsd:string.  <br/> |
|Описание  <br/> |xsd:string  <br/> |необязательный  <br/> |Указывает описание правила проверки, которое отображается в пользовательском интерфейсе. По умолчанию значение "Неизвестно".  <br/> |Значения типа xsd:string.  <br/> |
|ID  <br/> |xsd:unsignedInt  <br/> |Обязательный  <br/> |Указывает уникальный идентификатор для правила проверки.  <br/> |Значения типа xsd:unsignedInt.  <br/> |
|Игнорирован  <br/> |xsd:boolean  <br/> |необязательный  <br/> |Указывает, игнорируется ли правило проверки в настоящее время. По умолчанию значение False.  <br/> |Значения типа xsd:boolean.  <br/> |
|NameU  <br/> |xsd:string  <br/> |Обязательный  <br/> |Указывает универсальное имя правила проверки.  <br/> |Значения типа xsd:string.  <br/> |
|RuleTarget  <br/> |xsd:int  <br/> |необязательный  <br/> |Указывает тип объекта, к которому применяется правило проверки.  <br/> |Значения типа xsd:int.  <br/> |
   

