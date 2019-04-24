---
title: Элемент Issue (Иссуес_типе complexType) (' XML ' Visio ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 5c4d07bf-4edc-e241-7827-017f96c11957
description: Представляет одну ошибку проверки в документе.
ms.openlocfilehash: 4ebe7d2d8b2b4627fb9c9e12113ef23ce19db52e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32317908"
---
# <a name="issue-element-issuestype-complextype-visio-xml"></a>Элемент Issue (Иссуес_типе complexType) (' XML ' Visio ')

Представляет одну ошибку проверки в документе.
  
## <a name="element-information"></a>Сведения об элементе

|||
|:-----|:-----|
|**Тип элемента** <br/> |[Иссуе_типе](issue_type-complextypevisio-xml.md) <br/> |
|**Пространство имен** <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
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
|ИД  <br/> |XSD: Унсигнединт  <br/> |Обязательный  <br/> |Указывает уникальный идентификатор для ошибки проверки.  <br/> |Значения типа XSD: Унсигнединт.  <br/> |
|Игнорирован  <br/> |XSD: Boolean  <br/> |необязательный  <br/> |Задает сведения о правиле проверки, к которым относится ошибка родительской проверки.  <br/> |Значения типа XSD: Boolean.  <br/> |
   

