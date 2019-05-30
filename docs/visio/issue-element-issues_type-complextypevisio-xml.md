---
title: Элемент Issue (Иссуес_типе complexType) (XML для Visio)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 5c4d07bf-4edc-e241-7827-017f96c11957
description: Представляет одну ошибку проверки в документе.
ms.openlocfilehash: 73c83fe47ebf9921686ea7b35c5f94a06b803623
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/29/2019
ms.locfileid: "34541129"
---
# <a name="issue-element-issuestype-complextype-visio-xml"></a>Элемент Issue (Иссуес_типе complexType) (XML для Visio)

Представляет одну ошибку проверки в документе.
  
## <a name="element-information"></a>Сведения об элементе

|||
|:-----|:-----|
|**Тип элемента** <br/> |[Иссуе_типе](issue_type-complextypevisio-xml.md) <br/> |
|**Пространство имен** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Файл схемы** <br/> |VisioSchema15. xsd  <br/> |
|**Части документа** <br/> |Проверка. XML  <br/> |
   
## <a name="definition"></a>Определение

```XML
< xs:element name="Issue" type="Issue_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a>Элементы и атрибуты

Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений. 
  
### <a name="parent-elements"></a>Родительские элементы

|**Элемент**|**Тип**|**Описание**|
|:-----|:-----|:-----|
|[Issues](issues-element-validation_type-complextypevisio-xml.md) <br/> |[Иссуес_типе](issues_type-complextypevisio-xml.md) <br/> |Содержит все элементы **issue** для документа.  <br/> |
   
### <a name="child-elements"></a>Дочерние элементы

|**Элемент**|**Тип**|**Описание**|
|:-----|:-----|:-----|
|[Иссуетаржет](issuetarget-element-issue_type-complextypevisio-xml.md) <br/> |[Иссуетаржет_типе](issuetarget_type-complextypevisio-xml.md) <br/> |В зависимости от цели родительской ошибки проверки указывает либо страницу, либо и фигуру, и страницу, связанную с ошибкой родительской проверки.  <br/> |
|[Рулеинфо](ruleinfo-element-issue_type-complextypevisio-xml.md) <br/> |[Рулеинфо_типе](ruleinfo_type-complextypevisio-xml.md) <br/> |Задает сведения о правиле проверки, к которым относится ошибка родительской проверки.  <br/> |
   
### <a name="attributes"></a>Атрибуты

|**Атрибут**|**Тип**|**Обязательный**|**Описание**|**Возможные значения**|
|:-----|:-----|:-----|:-----|:-----|
|ID  <br/> |XSD: Унсигнединт  <br/> |Обязательный  <br/> |Указывает уникальный идентификатор для ошибки проверки.  <br/> |Значения типа XSD: Унсигнединт.  <br/> |
|Игнорирован  <br/> |XSD: Boolean  <br/> |необязательный  <br/> |Задает сведения о правиле проверки, к которым относится ошибка родительской проверки.  <br/> |Значения типа XSD: Boolean.  <br/> |
   

