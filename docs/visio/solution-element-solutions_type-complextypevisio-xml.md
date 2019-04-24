---
title: Элемент Solution (Солутионс_типе complexType) (' XML ' Visio ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 46bf34be-761e-9d44-ab06-83d4c8932cab
description: Задает один экземпляр XML-файла решения, хранящегося в документе.
ms.openlocfilehash: bb3cd512ff6109467c9d6465ba72c764d83abf96
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32335268"
---
# <a name="solution-element-solutionstype-complextype-visio-xml"></a>Элемент Solution (Солутионс_типе complexType) (' XML ' Visio ')

Задает один экземпляр XML-файла решения, хранящегося в документе.
  
## <a name="element-information"></a>Сведения об элементе

|||
|:-----|:-----|
|**Тип элемента** <br/> |[Солутион_типе](solution_type-complextypevisio-xml.md) <br/> |
|**Пространство имен** <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Файл схемы** <br/> |VisioSchema15. xsd  <br/> |
|**Части документа** <br/> |Solutions. XML  <br/> |
   
## <a name="definition"></a>Определение

```XML
< xs:element name="Solution"  type="Solution_Type" minOccurs="0" maxOccurs="unbounded" ></xs:element >
```

## <a name="elements-and-attributes"></a>Элементы и атрибуты

Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений. 
  
### <a name="parent-elements"></a>Родительские элементы

|**Элемент**|**Тип**|**Описание**|
|:-----|:-----|:-----|
|[Решения](solutions-elementvisio-xml.md) <br/> |[Солутионс_типе](solutions_type-complextypevisio-xml.md) <br/> |Хранит свойства решений, хранящихся в документе.  <br/> |
   
### <a name="child-elements"></a>Дочерние элементы

|**Элемент**|**Тип**|**Описание**|
|:-----|:-----|:-----|
|[Rel](rel-element-solution_type-complextypevisio-xml.md) <br/> |[Рел_типе](rel_type-complextypevisio-xml.md) <br/> |Задает отношение к части с XML-ДОКУМЕНТом решения, связанным с этим решением.  <br/> |
   
### <a name="attributes"></a>Атрибуты

|**Атрибут**|**Тип**|**Обязательный**|**Описание**|**Возможные значения**|
|:-----|:-----|:-----|:-----|:-----|
|Имя  <br/> |XSD: строка  <br/> |Обязательный  <br/> |Имя решения.  <br/> |Значения типа String: XSD.  <br/> |
   

