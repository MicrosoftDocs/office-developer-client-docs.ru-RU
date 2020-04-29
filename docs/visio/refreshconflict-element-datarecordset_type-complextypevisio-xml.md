---
title: Элемент Рефрешконфликт (DataRecordSet_Type complexType) (XML для Visio)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 373983f7-fc0c-95f6-7665-7ed47de82e5e
description: Указывает строку в наборе записей данных, связанную с фигурой, которая находится в конфликте после обновления набора записей данных.
ms.openlocfilehash: f966ca4a9f23de7a96273615b2404041d1045652
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/29/2019
ms.locfileid: "34542837"
---
# <a name="refreshconflict-element-datarecordset_type-complextype-visio-xml"></a>Элемент Рефрешконфликт (DataRecordSet_Type complexType) (XML для Visio)

Указывает строку в наборе записей данных, связанную с фигурой, которая находится в конфликте после обновления набора записей данных.
  
## <a name="element-information"></a>Сведения об элементе

|||
|:-----|:-----|
|**Тип элемента** <br/> |[RefreshConflict_Type](refreshconflict_type-complextypevisio-xml.md) <br/> |
|**Пространство имен** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
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
|[DataRecordSet](datarecordset-element-datarecordsets_type-complextypevisio-xml.md) <br/> |[DataRecordSet_Type](datarecordset_type-complextypevisio-xml.md) <br/> |Хранение, форматирование, обновление и предоставление данных, запрашиваемых из базы данных в Microsoft Visio.  <br/> |
   
### <a name="child-elements"></a>Дочерние элементы

Нет.
  
### <a name="attributes"></a>Атрибуты

|**Атрибут**|**Тип**|**Обязательный**|**Описание**|**Возможные значения**|
|:-----|:-----|:-----|:-----|:-----|
|PageID  <br/> |XSD: Унсигнединт  <br/> |Обязательный  <br/> |Идентификатор страницы, участвующей в конфликте.  <br/> |Значения типа XSD: Унсигнединт.  <br/> |
|RowID  <br/> |XSD: Унсигнединт  <br/> |Обязательный  <br/> |После обновления данных идентификатор исходной строки в конфликте.  <br/> |Значения типа XSD: Унсигнединт.  <br/> |
|шапеид  <br/> |XSD: Унсигнединт  <br/> |Обязательный  <br/> |ИДЕНТИФИКАТОР фигуры, участвующей в конфликте.  <br/> |Значения типа XSD: Унсигнединт.  <br/> |
   

