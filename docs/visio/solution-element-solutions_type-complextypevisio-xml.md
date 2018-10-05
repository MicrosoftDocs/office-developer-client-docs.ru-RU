---
title: Элемент Solution (Solutions_Type complexType) ('Visio XML»)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 46bf34be-761e-9d44-ab06-83d4c8932cab
description: Задает один экземпляр решение, которое XML хранятся в документе.
ms.openlocfilehash: bb3cd512ff6109467c9d6465ba72c764d83abf96
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25397200"
---
# <a name="solution-element-solutionstype-complextype-visio-xml"></a>Элемент Solution (Solutions_Type complexType) ('Visio XML»)

Задает один экземпляр решение, которое XML хранятся в документе.
  
## <a name="element-information"></a>Сведения об элементе

|||
|:-----|:-----|
|**Тип элемента** <br/> |[Solution_Type](solution_type-complextypevisio-xml.md) <br/> |
|**Пространство имен** <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Файл схемы** <br/> |VisioSchema15.xsd  <br/> |
|**Части документа** <br/> |Solutions.XML  <br/> |
   
## <a name="definition"></a>Определение

```XML
< xs:element name="Solution"  type="Solution_Type" minOccurs="0" maxOccurs="unbounded" ></xs:element >
```

## <a name="elements-and-attributes"></a>Элементы и атрибуты

Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений. 
  
### <a name="parent-elements"></a>Родительские элементы

|**Элемент**|**Тип**|**Описание**|
|:-----|:-----|:-----|
|[Решения](solutions-elementvisio-xml.md) <br/> |[Solutions_Type](solutions_type-complextypevisio-xml.md) <br/> |Хранилище свойств решений, хранимого в документе.  <br/> |
   
### <a name="child-elements"></a>Дочерние элементы

|**Элемент**|**Тип**|**Описание**|
|:-----|:-----|:-----|
|[Rel](rel-element-solution_type-complextypevisio-xml.md) <br/> |[Rel_Type](rel_type-complextypevisio-xml.md) <br/> |Указывает связь с частью с решение, которое XML связанного с решением.  <br/> |
   
### <a name="attributes"></a>Атрибуты

|**Атрибут**|**Тип**|**Обязательный**|**Описание**|**Возможные значения**|
|:-----|:-----|:-----|:-----|:-----|
|Имя  <br/> |XSD:String  <br/> |Обязательный  <br/> |Имя решения.  <br/> |Значения типа xsd:string.  <br/> |
   

