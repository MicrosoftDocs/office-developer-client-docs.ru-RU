---
title: Элемент ValidationProperties (Validation_Type complexType) ('Visio XML»)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: a51a60c9-479b-7d7b-860f-bb46fc8b4d63
description: Инкапсулирует свойства, которые связаны с проверки документа.
ms.openlocfilehash: 9eccb85bd7463411d81c867eda3216d6c9a207f2
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25385223"
---
# <a name="validationproperties-element-validationtype-complextype-visio-xml"></a>Элемент ValidationProperties (Validation_Type complexType) ('Visio XML»)

Инкапсулирует свойства, которые связаны с проверки документа.
  
## <a name="element-information"></a>Сведения об элементе

|||
|:-----|:-----|
|**Тип элемента** <br/> |[ValidationProperties_Type](validationproperties_type-complextypevisio-xml.md) <br/> |
|**Пространство имен** <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Файл схемы** <br/> |VisioSchema15.xsd  <br/> |
|**Части документа** <br/> |Validation.XML  <br/> |
   
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
|[Проверка](validation-elementvisio-xml.md) <br/> |[Validation_Type](validation_type-complextypevisio-xml.md) <br/> |Сохранение информации о проверки схемы для документа.  <br/> |
   
### <a name="child-elements"></a>Дочерние элементы

Нет.
  
### <a name="attributes"></a>Атрибуты

|**Атрибут**|**Тип**|**Обязательный**|**Описание**|**Возможные значения**|
|:-----|:-----|:-----|:-----|:-----|
|LastValidated  <br/> |XSD: DateTime  <br/> |Обязательный  <br/> |Дата и время последнего прошел проверку документа.  <br/> |Значения типа XSD: DateTime.  <br/> |
|ShowIgnored  <br/> |XSD:Boolean  <br/> |Обязательный  <br/> |Указывает, следует ли показывать проблемы игнорируемыми проверки в окно вопросов.  <br/> |Значения типа xsd:boolean.  <br/> |
   

