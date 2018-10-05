---
title: Элемент Rule (RuleSet_Type complexType) ('Visio XML»)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: fcd22f3a-c8e8-1133-160c-fe26e612a15d
description: Представляет правило одного проверки в набор правил проверки схемы.
ms.openlocfilehash: 92d52456164b89ff2aad31fa8d8f02f818c8bd1c
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25395912"
---
# <a name="rule-element-rulesettype-complextype-visio-xml"></a>Элемент Rule (RuleSet_Type complexType) ('Visio XML»)

Представляет правило одного проверки в набор правил проверки схемы.
  
## <a name="element-information"></a>Сведения об элементе

|||
|:-----|:-----|
|**Тип элемента** <br/> |[Rule_Type](rule_type-complextypevisio-xml.md) <br/> |
|**Пространство имен** <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Файл схемы** <br/> |VisioSchema15.xsd  <br/> |
|**Части документа** <br/> |Validation.XML  <br/> |
   
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
|[Набор правил](ruleset-element-rulesets_type-complextypevisio-xml.md) <br/> |[RuleSet_Type](ruleset_type-complextypevisio-xml.md) <br/> |Представляет один набор правил проверки схемы.  <br/> |
   
### <a name="child-elements"></a>Дочерние элементы

|**Элемент**|**Тип**|**Описание**|
|:-----|:-----|:-----|
|[RuleFilter](rulefilter-element-rule_type-complextypevisio-xml.md) <br/> |[RuleFilter_Type](rulefilter_type-complextypevisio-xml.md) <br/> |Задает логическое выражение, которое определяет, применяется ли правило проверки на целевой объект.  <br/> |
|[RuleTest](ruletest-element-rule_type-complextypevisio-xml.md) <br/> |[RuleTest_Type](ruletest_type-complextypevisio-xml.md) <br/> |Задает логическое выражение, которое определяет, удовлетворяет ли целевой объект правила проверки.  <br/> |
   
### <a name="attributes"></a>Атрибуты

|**Атрибут**|**Тип**|**Обязательный**|**Описание**|**Возможные значения**|
|:-----|:-----|:-----|:-----|:-----|
|Категория  <br/> |XSD:String  <br/> |необязательный  <br/> |Задает текст, отображаемый в столбце **категории** окно вопросов. Значение по умолчанию — пустая строка.  <br/> |Значения типа xsd:string.  <br/> |
|Описание  <br/> |XSD:String  <br/> |необязательный  <br/> |Задает описание правила проверки, который отображается в пользовательском интерфейсе. Значение по умолчанию — «Неизвестно».  <br/> |Значения типа xsd:string.  <br/> |
|ID  <br/> |XSD:unsignedInt  <br/> |Обязательный  <br/> |Задает уникальный идентификатор для правила проверки.  <br/> |Значения типа xsd:unsignedInt.  <br/> |
|Игнорируется  <br/> |XSD:Boolean  <br/> |необязательный  <br/> |Указывает, учитывается ли правило проверки. Значение по умолчанию — False.  <br/> |Значения типа xsd:boolean.  <br/> |
|NameU  <br/> |XSD:String  <br/> |Обязательный  <br/> |Задает имя универсальные правила проверки.  <br/> |Значения типа xsd:string.  <br/> |
|RuleTarget  <br/> |XSD: int  <br/> |необязательный  <br/> |Указывает тип объекта, к которому применяется правило проверки.  <br/> |Значения типа XSD: int.  <br/> |
   

