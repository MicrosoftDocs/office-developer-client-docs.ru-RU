---
title: Элемент Рулеинфо (Иссуе_типе complexType) (XML для Visio)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: aec47b43-adbe-3344-fbac-29554f244c99
description: Задает сведения о правиле проверки, к которым относится ошибка родительской проверки.
ms.openlocfilehash: 29454fdb82d9e12d46fa9eedf73f8a31e8befd95
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/29/2019
ms.locfileid: "34541689"
---
# <a name="ruleinfo-element-issuetype-complextype-visio-xml"></a>Элемент Рулеинфо (Иссуе_типе complexType) (XML для Visio)

Задает сведения о правиле проверки, к которым относится ошибка родительской проверки.
  
## <a name="element-information"></a>Сведения об элементе

|||
|:-----|:-----|
|**Тип элемента** <br/> |[Рулеинфо_типе](ruleinfo_type-complextypevisio-xml.md) <br/> |
|**Пространство имен** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Файл схемы** <br/> |VisioSchema15. xsd  <br/> |
|**Части документа** <br/> |Проверка. XML  <br/> |
   
## <a name="definition"></a>Определение

```XML
< xs:element name="RuleInfo" type="RuleInfo_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a>Элементы и атрибуты

Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений. 
  
### <a name="parent-elements"></a>Родительские элементы

|**Элемент**|**Тип**|**Описание**|
|:-----|:-----|:-----|
|[Проблема](issue-element-issues_type-complextypevisio-xml.md) <br/> |[Иссуе_типе](issue_type-complextypevisio-xml.md) <br/> |Представляет одну ошибку проверки в документе.  <br/> |
   
### <a name="child-elements"></a>Дочерние элементы

Нет.
  
### <a name="attributes"></a>Атрибуты

|**Атрибут**|**Тип**|**Обязательный**|**Описание**|**Возможные значения**|
|:-----|:-----|:-----|:-----|:-----|
|RuleID  <br/> |XSD: Унсигнединт  <br/> |Обязательный  <br/> |Задает уникальный идентификатор правила проверки, к которому относится родительская ошибка.  <br/> |Значения типа XSD: Унсигнединт.  <br/> |
|Рулесетид  <br/> |XSD: Унсигнединт  <br/> |Обязательный  <br/> |Задает уникальный идентификатор набора правил проверки, к которому относится родительская ошибка.  <br/> |Значения типа XSD: Унсигнединт.  <br/> |
   

