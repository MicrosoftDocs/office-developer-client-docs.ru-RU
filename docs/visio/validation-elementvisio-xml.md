---
title: Элемент Validation (XML в Visio)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: db6292c7-9f4c-c287-803b-64fa41c0a269
description: Сохраняет сведения о проверке схемы для документа.
ms.openlocfilehash: b1b1bcbd70d57d7a7316e91d137cf8c3c3750722
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/29/2019
ms.locfileid: "34538552"
---
# <a name="validation-element-visio-xml"></a>Элемент Validation (XML в Visio)

Сохраняет сведения о проверке схемы для документа.
  
## <a name="element-information"></a>Сведения об элементе

|||
|:-----|:-----|
|**Тип элемента** <br/> |[Валидатион_типе](validation_type-complextypevisio-xml.md) <br/> |
|**Пространство имен** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Файл схемы** <br/> |VisioSchema15. xsd  <br/> |
|**Части документа** <br/> |Проверка. XML  <br/> |
   
## <a name="definition"></a>Определение

```XML
< xs:element name="Validation" type="Validation_Type" > </xs:element >
```

## <a name="elements-and-attributes"></a>Элементы и атрибуты

Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений. 
  
### <a name="parent-elements"></a>Родительские элементы

Нет.
  
### <a name="child-elements"></a>Дочерние элементы

|**Элемент**|**Тип**|**Описание**|
|:-----|:-----|:-----|
|[Issues](issues-element-validation_type-complextypevisio-xml.md) <br/> |[Иссуес_типе](issues_type-complextypevisio-xml.md) <br/> |Содержит все элементы **issue** для документа.  <br/> |
|[RuleSets](rulesets-element-validation_type-complextypevisio-xml.md) <br/> |[Рулесетс_типе](rulesets_type-complextypevisio-xml.md) <br/> |Включает элемент **RuleSet** для каждого набора правил проверки в документе.  <br/> |
|[Валидатионпропертиес](validationproperties-element-validation_type-complextypevisio-xml.md) <br/> |[Валидатионпропертиес_типе](validationproperties_type-complextypevisio-xml.md) <br/> |Инкапсулирует свойства, связанные с проверкой документа.  <br/> |
   
### <a name="attributes"></a>Атрибуты

Нет.
  

