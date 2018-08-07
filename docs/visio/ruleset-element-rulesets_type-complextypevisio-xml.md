---
title: Элемент набора правил (RuleSets_Type complexType) ('Visio XML»)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 5ca63b8a-782e-211f-be7a-8e177b61d8fc
description: Представляет один набор правил проверки схемы.
ms.openlocfilehash: ae8fc52dd665e51f38c7eeae2f12ff778937d565
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19814708"
---
# <a name="ruleset-element-rulesetstype-complextype-visio-xml"></a>Элемент набора правил (RuleSets_Type complexType) ('Visio XML»)

Представляет один набор правил проверки схемы.
  
## <a name="element-information"></a>Сведения об элементе

|||
|:-----|:-----|
|**Тип элемента** <br/> |[RuleSet_Type](ruleset_type-complextypevisio-xml.md) <br/> |
|**Пространство имен** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Файл схемы** <br/> |VisioSchema15.xsd  <br/> |
|**Части документа** <br/> |Validation.XML  <br/> |
   
## <a name="definition"></a>Определение

```XML
< xs:element name="RuleSet" type="RuleSet_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a>Элементы и атрибуты

Если схема определяет специальные требования, такие как **последовательность**, **minOccurs**, **maxOccurs**и **выбора**, обратитесь к разделу определение. 
  
### <a name="parent-elements"></a>Родительские элементы

|**Элемент**|**Тип**|**Описание**|
|:-----|:-----|:-----|
|[Наборы правил](rulesets-element-validation_type-complextypevisio-xml.md) <br/> |[RuleSets_Type](rulesets_type-complextypevisio-xml.md) <br/> |Включает в себя элемент **набора правил** для каждого правила проверки, задайте в документе.  <br/> |
   
### <a name="child-elements"></a>Дочерние элементы

|**Элемент**|**Тип**|**Описание**|
|:-----|:-----|:-----|
|[Rule](rule-element-ruleset_type-complextypevisio-xml.md) <br/> |[Rule_Type](rule_type-complextypevisio-xml.md) <br/> |Представляет правило одного проверки в набор правил проверки схемы.  <br/> |
|[RuleSetFlags](rulesetflags-element-ruleset_type-complextypevisio-xml.md) <br/> |[RuleSetFlags_Type](rulesetflags_type-complextypevisio-xml.md) <br/> |Задает свойства набора правил.  <br/> |
   
### <a name="attributes"></a>Атрибуты

|**Атрибут**|**Тип**|**Обязательное**|**Описание**|**Возможные значения**|
|:-----|:-----|:-----|:-----|:-----|
|Описание  <br/> |XSD:String  <br/> |необязательный  <br/> |Указывает описание, которое отображается в пользовательском интерфейсе для набора правил проверки. Значение по умолчанию — пустая строка.  <br/> |Значения типа xsd:string.  <br/> |
|Включена  <br/> |XSD:Boolean  <br/> |необязательный  <br/> |Указывает, проверяются ли правила в наборе правил указанного проверки при проверке запускается для текущего документа. Значение по умолчанию — True.  <br/> |Значения типа xsd:boolean.  <br/> |
|ID  <br/> |XSD:unsignedInt  <br/> |Обязательный  <br/> |Задает уникальный идентификатор набора правил проверки.  <br/> |Значения типа xsd:unsignedInt.  <br/> |
|Имя  <br/> |XSD:String  <br/> |необязательный  <br/> |Указывает локальное имя набора правил проверки. По умолчанию используется значение атрибута NameU.  <br/> |Значения типа xsd:string.  <br/> |
|NameU  <br/> |XSD:String  <br/> |Обязательный  <br/> |Задает имя универсального набора правил проверки.  <br/> |Значения типа xsd:string.  <br/> |
   

