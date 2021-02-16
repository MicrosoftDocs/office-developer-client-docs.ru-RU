---
title: Элемент ValidationProperties (Validation_Type complexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: a51a60c9-479b-7d7b-860f-bb46fc8b4d63
description: Инкапсулирует свойства, связанные с проверкой документа.
ms.openlocfilehash: 35e6f3f13eecef826fdef0d664bba35fceb0e069
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/29/2019
ms.locfileid: "34538524"
---
# <a name="validationproperties-element-validation_type-complextype-visio-xml"></a>Элемент ValidationProperties (Validation_Type complexType) (Visio XML)

Инкапсулирует свойства, связанные с проверкой документа.
  
## <a name="element-information"></a>Сведения об элементе

|||
|:-----|:-----|
|**Тип элемента** <br/> |[ValidationProperties_Type](validationproperties_type-complextypevisio-xml.md) <br/> |
|**Пространство имен** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Файл схемы** <br/> |VisioSchema15.xsd  <br/> |
|**Части документа** <br/> |validation.xml  <br/> |
   
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
|[Validation](validation-elementvisio-xml.md) <br/> |[Validation_Type](validation_type-complextypevisio-xml.md) <br/> |Хранит сведения о проверке схемы для документа.  <br/> |
   
### <a name="child-elements"></a>Дочерние элементы

Нет.
  
### <a name="attributes"></a>Атрибуты

|**Атрибут**|**Тип**|**Обязательный**|**Описание**|**Возможные значения**|
|:-----|:-----|:-----|:-----|:-----|
|LastValidated  <br/> |xsd:dateTime  <br/> |Обязательный  <br/> |Дата и время последней проверки документа.  <br/> |Значения типа xsd:dateTime.  <br/> |
|ShowIgnored  <br/> |xsd:boolean  <br/> |Обязательный  <br/> |Указывает, следует ли показывать пропущенные проблемы проверки в окне "Проблемы".  <br/> |Значения типа xsd:boolean.  <br/> |
   

