---
title: Элемент RowMap (DataRecordSet_Type complexType) ('Visio XML»)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: f90dc76b-7f0b-dead-38c0-97062a7b76a6
description: Сопоставление строк набора записей данных фигуры.
ms.openlocfilehash: aefae8c625f35feacd6d0fdf04f128c423db299b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19814698"
---
# <a name="rowmap-element-datarecordsettype-complextype-visio-xml"></a>Элемент RowMap (DataRecordSet_Type complexType) ('Visio XML»)

Сопоставление строк набора записей данных фигуры.
  
## <a name="element-information"></a>Сведения об элементе

|||
|:-----|:-----|
|**Тип элемента** <br/> |[RowMap_Type](rowmap_type-complextypevisio-xml.md) <br/> |
|**Пространство имен** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Файл схемы** <br/> |VisioSchema15.xsd  <br/> |
|**Части документа** <br/> |recordsets.XML  <br/> |
   
## <a name="definition"></a>Определение

```XML
< xs:element name="RowMap" type="RowMap_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a>Элементы и атрибуты

Если схема определяет специальные требования, такие как **последовательность**, **minOccurs**, **maxOccurs**и **выбора**, обратитесь к разделу определение. 
  
### <a name="parent-elements"></a>Родительские элементы

****

|**Элемент**|**Тип**|**Описание**|
|:-----|:-----|:-----|
|[Записей данных](datarecordset-element-datarecordsets_type-complextypevisio-xml.md) <br/> |[DataRecordSet_Type](datarecordset_type-complextypevisio-xml.md) <br/> |Сохранение, форматы, обновляет и предоставляет доступ к данным из базы данных в Microsoft Visio.  <br/> |
   
### <a name="child-elements"></a>Дочерние элементы

Нет.
  
### <a name="attributes"></a>Атрибуты

|**Атрибут**|**Тип**|**Обязательное**|**Описание**|**Возможные значения**|
|:-----|:-----|:-----|:-----|:-----|
|PageID  <br/> |XSD:unsignedInt  <br/> |Обязательный  <br/> |Идентификатор страницы фигуры, связанная с данными в строки набора записей данных, **RowID**.  <br/> |Значения типа xsd:unsignedInt.  <br/> |
|RowID  <br/> |XSD:unsignedInt  <br/> |Обязательный  <br/> |Идентификатор строки строки, уникальных в пределах набора данных.  <br/> |Значения типа xsd:unsignedInt.  <br/> |
|ShapeID  <br/> |XSD:unsignedInt  <br/> |Обязательный  <br/> |Код фигуры фигуры, связанная с данными в строки набора записей данных, **RowID**.  <br/> |Значения типа xsd:unsignedInt.  <br/> |
   

