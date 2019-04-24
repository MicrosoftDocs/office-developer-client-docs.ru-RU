---
title: Элемент Рефрешконфликт (Датарекордсет_типе complexType) (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 373983f7-fc0c-95f6-7665-7ed47de82e5e
description: Указывает строку в наборе записей данных, связанную с фигурой, которая находится в конфликте после обновления набора записей данных.
ms.openlocfilehash: 2da6f98cf7b047564331aaf5a4167e392927a155
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360139"
---
# <a name="refreshconflict-element-datarecordsettype-complextype-visio-xml"></a>Элемент Рефрешконфликт (Датарекордсет_типе complexType) (' Visio XML ')

Указывает строку в наборе записей данных, связанную с фигурой, которая находится в конфликте после обновления набора записей данных.
  
## <a name="element-information"></a>Сведения об элементе

|||
|:-----|:-----|
|**Тип элемента** <br/> |[Рефрешконфликт_типе](refreshconflict_type-complextypevisio-xml.md) <br/> |
|**Пространство имен** <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Файл схемы** <br/> |VisioSchema15. xsd  <br/> |
|**Части документа** <br/> |Recordset. XML  <br/> |
   
## <a name="definition"></a>Определение

```XML
< xs:element name="RefreshConflict" type="RefreshConflict_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element>
```

## <a name="elements-and-attributes"></a>Элементы и атрибуты

Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений. 
  
### <a name="parent-elements"></a>Родительские элементы

|**Элемент**|**Тип**|**Описание**|
|:-----|:-----|:-----|
|[DataRecordSet](datarecordset-element-datarecordsets_type-complextypevisio-xml.md) <br/> |[Датарекордсет_типе](datarecordset_type-complextypevisio-xml.md) <br/> |Хранение, форматирование, обновление и предоставление данных, запрашиваемых из базы данных в Microsoft Visio.  <br/> |
   
### <a name="child-elements"></a>Дочерние элементы

Нет.
  
### <a name="attributes"></a>Атрибуты

|**Атрибут**|**Тип**|**Обязательный**|**Описание**|**Возможные значения**|
|:-----|:-----|:-----|:-----|:-----|
|PageID  <br/> |XSD: Унсигнединт  <br/> |Обязательный  <br/> |Идентификатор страницы, участвующей в конфликте.  <br/> |Значения типа XSD: Унсигнединт.  <br/> |
|RowID  <br/> |XSD: Унсигнединт  <br/> |Обязательный  <br/> |После обновления данных идентификатор исходной строки в конфликте.  <br/> |Значения типа XSD: Унсигнединт.  <br/> |
|Шапеид  <br/> |XSD: Унсигнединт  <br/> |Обязательный  <br/> |ИДЕНТИФИКАТОР фигуры, участвующей в конфликте.  <br/> |Значения типа XSD: Унсигнединт.  <br/> |
   

