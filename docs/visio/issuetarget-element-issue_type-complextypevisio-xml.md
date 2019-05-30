---
title: Элемент Иссуетаржет (Иссуе_типе complexType) (XML для Visio)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: bd9a5d5f-16fe-29b4-5af0-913b14d2be16
description: В зависимости от цели родительской ошибки проверки указывает либо страницу, либо и фигуру, и страницу, связанную с ошибкой родительской проверки. Если целью родительской ошибки проверки является документ, Иссуетаржет спеЦифес ни страницу, ни фигуру.
ms.openlocfilehash: 686f37afee43d9cee3f58979d5856602f571eec8
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/29/2019
ms.locfileid: "34542956"
---
# <a name="issuetarget-element-issuetype-complextype-visio-xml"></a>Элемент Иссуетаржет (Иссуе_типе complexType) (XML для Visio)

В зависимости от цели родительской ошибки проверки указывает либо страницу, либо и фигуру, и страницу, связанную с ошибкой родительской проверки. Если целью родительской ошибки проверки является документ, **иссуетаржет** спеЦифес ни страницу, ни фигуру. 
  
## <a name="element-information"></a>Сведения об элементе

|||
|:-----|:-----|
|**Тип элемента** <br/> |[Иссуетаржет_типе](issuetarget_type-complextypevisio-xml.md) <br/> |
|**Пространство имен** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Файл схемы** <br/> |VisioSchema15. xsd  <br/> |
|**Части документа** <br/> |Проверка. XML  <br/> |
   
## <a name="definition"></a>Определение

```XML
< xs:element name="IssueTarget" type="IssueTarget_Type" minOccurs="0" maxOccurs="1" >
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
|PageID  <br/> |XSD: Унсигнединт  <br/> |Обязательный  <br/> |Задает уникальный идентификатор страницы, связанной с ошибкой родительской проверки. Если целевым объектом является документ, значение Пажеид может быть 0xFFFFFFFF.  <br/> |Значения типа XSD: Унсигнединт.  <br/> |
|Шапеид  <br/> |XSD: Унсигнединт  <br/> |Обязательный  <br/> |Задает уникальный идентификатор фигуры, связанной с ошибкой родительской проверки. Если целевым объектом является документ или страница, значение Шапеид может быть 0xFFFFFFFF.  <br/> |Значения типа XSD: Унсигнединт.  <br/> |
   

