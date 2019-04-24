---
title: Элемент Валидатионпропертиес (Валидатион_типе complexType) (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: a51a60c9-479b-7d7b-860f-bb46fc8b4d63
description: Инкапсулирует свойства, связанные с проверкой документа.
ms.openlocfilehash: 9eccb85bd7463411d81c867eda3216d6c9a207f2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32355960"
---
# <a name="validationproperties-element-validationtype-complextype-visio-xml"></a>Элемент Валидатионпропертиес (Валидатион_типе complexType) (' Visio XML ')

Инкапсулирует свойства, связанные с проверкой документа.
  
## <a name="element-information"></a>Сведения об элементе

|||
|:-----|:-----|
|**Тип элемента** <br/> |[Валидатионпропертиес_типе](validationproperties_type-complextypevisio-xml.md) <br/> |
|**Пространство имен** <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Файл схемы** <br/> |VisioSchema15. xsd  <br/> |
|**Части документа** <br/> |Проверка. XML  <br/> |
   
## <a name="definition"></a>Определение

```XML
< xs:element name="ValidationProperties" type="ValidationProperties_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a>Элементы и атрибуты

Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений. 
  
### <a name="parent-elements"></a>Родительские элементы

|**Элемент**|**Тип**|**Описание**|
|:-----|:-----|:-----|
|[Validation](validation-elementvisio-xml.md) <br/> |[Валидатион_типе](validation_type-complextypevisio-xml.md) <br/> |Сохраняет сведения о проверке схемы для документа.  <br/> |
   
### <a name="child-elements"></a>Дочерние элементы

Нет.
  
### <a name="attributes"></a>Атрибуты

|**Атрибут**|**Тип**|**Обязательный**|**Описание**|**Возможные значения**|
|:-----|:-----|:-----|:-----|:-----|
|Ластвалидатед  <br/> |XSD: dateTime  <br/> |Обязательный  <br/> |Дата и время последней проверки документа.  <br/> |Значения типа XSD: dateTime.  <br/> |
|Шовигноред  <br/> |XSD: Boolean  <br/> |Обязательный  <br/> |Указывает, следует ли отображать пропущенные проблемы при проверке в окне "проблемы".  <br/> |Значения типа XSD: Boolean.  <br/> |
   

