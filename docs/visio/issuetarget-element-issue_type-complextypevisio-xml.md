---
title: Элемент IssueTarget (Issue_Type ComplexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: bd9a5d5f-16fe-29b4-5af0-913b14d2be16
description: В зависимости от цели родительской проблемы проверки указывается страница или страница и форма, связанные с родительской проблемой проверки. Если целью родительской проблемы проверки является документ, IssueTarget не задает ни страницы, ни фигуры.
ms.openlocfilehash: 686f37afee43d9cee3f58979d5856602f571eec8
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/29/2019
ms.locfileid: "34542956"
---
# <a name="issuetarget-element-issue_type-complextype-visio-xml"></a>Элемент IssueTarget (Issue_Type ComplexType) (Visio XML)

В зависимости от цели родительской проблемы проверки указывается страница или страница и форма, связанные с родительской проблемой проверки. Если целью родительской проблемы проверки является документ, **IssueTarget** не задает ни страницы, ни фигуры. 
  
## <a name="element-information"></a>Сведения об элементе

|||
|:-----|:-----|
|**Тип элемента** <br/> |[IssueTarget_Type](issuetarget_type-complextypevisio-xml.md) <br/> |
|**Пространство имен** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Файл схемы** <br/> |VisioSchema15.xsd  <br/> |
|**Части документов** <br/> |validation.xml  <br/> |
   
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
|[Проблема](issue-element-issues_type-complextypevisio-xml.md) <br/> |[Issue_Type](issue_type-complextypevisio-xml.md) <br/> |Представляет одну проблему проверки в документе.  <br/> |
   
### <a name="child-elements"></a>Дочерние элементы

Нет.
  
### <a name="attributes"></a>Атрибуты

|**Атрибут**|**Тип**|**Обязательный**|**Описание**|**Возможные значения**|
|:-----|:-----|:-----|:-----|:-----|
|PageID  <br/> |xsd:unsignedInt  <br/> |Обязательный  <br/> |Указывает уникальный идентификатор страницы, связанной с родительской проблемой проверки. Если целью является документ, значение PageID может быть 0xFFFFFFFF.  <br/> |Значения типа xsd:unsignedInt.  <br/> |
|ShapeID  <br/> |xsd:unsignedInt  <br/> |Обязательный  <br/> |Указывает уникальный идентификатор формы, связанной с родительской проблемой проверки. Если целью является документ или страница, значение ShapeID может быть 0xFFFFFFFF.  <br/> |Значения типа xsd:unsignedInt.  <br/> |
   

