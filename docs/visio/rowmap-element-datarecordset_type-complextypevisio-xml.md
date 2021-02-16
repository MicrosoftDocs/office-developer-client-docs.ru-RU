---
title: Элемент RowMap (DataRecordSet_Type complexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: f90dc76b-7f0b-dead-38c0-97062a7b76a6
description: Сопописывая строка наборов данных с фигурой.
ms.openlocfilehash: 178ceb06d64bfc9ef50f75dd22f8bd94f09f5c33
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/29/2019
ms.locfileid: "34540772"
---
# <a name="rowmap-element-datarecordset_type-complextype-visio-xml"></a>Элемент RowMap (DataRecordSet_Type complexType) (Visio XML)

Сопописывая строка наборов данных с фигурой.
  
## <a name="element-information"></a>Сведения об элементе

|||
|:-----|:-----|
|**Тип элемента** <br/> |[RowMap_Type](rowmap_type-complextypevisio-xml.md) <br/> |
|**Пространство имен** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Файл схемы** <br/> |VisioSchema15.xsd  <br/> |
|**Части документа** <br/> |recordsets.xml  <br/> |
   
## <a name="definition"></a>Определение

```XML
< xs:element name="RowMap" type="RowMap_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a>Элементы и атрибуты

Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений. 
  
### <a name="parent-elements"></a>Родительские элементы

****

|**Элемент**|**Тип**|**Описание**|
|:-----|:-----|:-----|
|[DataRecordSet](datarecordset-element-datarecordsets_type-complextypevisio-xml.md) <br/> |[DataRecordSet_Type](datarecordset_type-complextypevisio-xml.md) <br/> |Хранит, форматирует, обновляет и предоставляет данные, запрашиваемые из базы данных в Microsoft Visio.  <br/> |
   
### <a name="child-elements"></a>Дочерние элементы

Нет.
  
### <a name="attributes"></a>Атрибуты

|**Атрибут**|**Тип**|**Обязательный**|**Описание**|**Возможные значения**|
|:-----|:-----|:-----|:-----|:-----|
|PageID  <br/> |xsd:unsignedInt  <br/> |Обязательный  <br/> |Page ID of the shape linked to data in the data-recordset row identified by **RowID**.  <br/> |Значения типа xsd:unsignedInt.  <br/> |
|RowID  <br/> |xsd:unsignedInt  <br/> |Обязательный  <br/> |Уникальный ИД строки в наборе записей данных.  <br/> |Значения типа xsd:unsignedInt.  <br/> |
|ShapeID  <br/> |xsd:unsignedInt  <br/> |Обязательный  <br/> |ИД фигуры, связанной с данными в строке наборов записей данных, заданной **rowID.**  <br/> |Значения типа xsd:unsignedInt.  <br/> |
   

