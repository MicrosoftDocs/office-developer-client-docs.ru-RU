---
title: Элемент проблему (Issues_Type complexType) ('Visio XML»)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 5c4d07bf-4edc-e241-7827-017f96c11957
description: Представляет ошибки проверки одного документа.
ms.openlocfilehash: 904b42c969bdf97fcfa1e34bad97f73242b17cc2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19814010"
---
# <a name="issue-element-issuestype-complextype-visio-xml"></a>Элемент проблему (Issues_Type complexType) ('Visio XML»)

Представляет ошибки проверки одного документа.
  
## <a name="element-information"></a>Сведения об элементе

|||
|:-----|:-----|
|**Тип элемента** <br/> |[Issue_Type](issue_type-complextypevisio-xml.md) <br/> |
|**Пространство имен** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Файл схемы** <br/> |VisioSchema15.xsd  <br/> |
|**Части документа** <br/> |Validation.XML  <br/> |
   
## <a name="definition"></a>Определение

```XML
< xs:element name="Issue" type="Issue_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a>Элементы и атрибуты

Если схема определяет специальные требования, такие как **последовательность**, **minOccurs**, **maxOccurs**и **выбора**, обратитесь к разделу определение. 
  
### <a name="parent-elements"></a>Родительские элементы

|**Элемент**|**Тип**|**Описание**|
|:-----|:-----|:-----|
|[Проблемы](issues-element-validation_type-complextypevisio-xml.md) <br/> |[Issues_Type](issues_type-complextypevisio-xml.md) <br/> |Содержит все элементы **проблему** для документа.  <br/> |
   
### <a name="child-elements"></a>Дочерние элементы

|**Элемент**|**Тип**|**Описание**|
|:-----|:-----|:-----|
|[IssueTarget](issuetarget-element-issue_type-complextypevisio-xml.md) <br/> |[IssueTarget_Type](issuetarget_type-complextypevisio-xml.md) <br/> |В зависимости от целевого родительский ошибки проверки указывает либо страницы или страницы и фигуры, связанного с родительской ошибки проверки.  <br/> |
|[RuleInfo](ruleinfo-element-issue_type-complextypevisio-xml.md) <br/> |[RuleInfo_Type](ruleinfo_type-complextypevisio-xml.md) <br/> |Задает сведения о правиле проверки, относящимися ошибки проверки родительского.  <br/> |
   
### <a name="attributes"></a>Атрибуты

|**Атрибут**|**Тип**|**Обязательное**|**Описание**|**Возможные значения**|
|:-----|:-----|:-----|:-----|:-----|
|ID  <br/> |XSD:unsignedInt  <br/> |Обязательный  <br/> |Задает уникальный идентификатор ошибки проверки.  <br/> |Значения типа xsd:unsignedInt.  <br/> |
|Игнорируется  <br/> |XSD:Boolean  <br/> |необязательный  <br/> |Задает сведения о правиле проверки, относящимися ошибки проверки родительского.  <br/> |Значения типа xsd:boolean.  <br/> |
   

