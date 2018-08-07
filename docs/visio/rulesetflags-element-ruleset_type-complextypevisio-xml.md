---
title: Элемент RuleSetFlags (RuleSet_Type complexType) ('Visio XML»)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: c18d3a84-2088-13f7-7b14-1f4c129537b4
description: Задает свойства набора правил.
ms.openlocfilehash: f656e8ace045d45460ab353444c39c760448aa7b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19814704"
---
# <a name="rulesetflags-element-rulesettype-complextype-visio-xml"></a>Элемент RuleSetFlags (RuleSet_Type complexType) ('Visio XML»)

Задает свойства набора правил.
  
## <a name="element-information"></a>Сведения об элементе

|||
|:-----|:-----|
|**Тип элемента** <br/> |[RuleSetFlags_Type](rulesetflags_type-complextypevisio-xml.md) <br/> |
|**Пространство имен** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Файл схемы** <br/> |VisioSchema15.xsd  <br/> |
|**Части документа** <br/> |Validation.XML  <br/> |
   
## <a name="definition"></a>Определение

```XML
< xs:element name="RuleSetFlags" type="RuleSetFlags_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a>Элементы и атрибуты

Если схема определяет специальные требования, такие как **последовательность**, **minOccurs**, **maxOccurs**и **выбора**, обратитесь к разделу определение. 
  
### <a name="parent-elements"></a>Родительские элементы

|**Элемент**|**Тип**|**Описание**|
|:-----|:-----|:-----|
|[Набор правил](ruleset-element-rulesets_type-complextypevisio-xml.md) <br/> |[RuleSet_Type](ruleset_type-complextypevisio-xml.md) <br/> |Представляет один набор правил проверки схемы.  <br/> |
   
### <a name="child-elements"></a>Дочерние элементы

Нет.
  
### <a name="attributes"></a>Атрибуты

|**Атрибут**|**Тип**|**Обязательное**|**Описание**|**Возможные значения**|
|:-----|:-----|:-----|:-----|:-----|
|Hidden  <br/> |XSD:Boolean  <br/> |необязательный  <br/> |Указывает, отображается ли набор правил в правилах для контрольного списка.  <br/> |Значения типа xsd:boolean.  <br/> |
   

