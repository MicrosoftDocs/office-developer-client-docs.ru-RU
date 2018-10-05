---
title: Элемент объектам DataColumn (DataRecordSet_Type complexType) ('Visio XML»)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 34e25349-d0fa-b3a0-425b-778184e9f58f
description: Содержит все элементы DataColumn в записей данных.
ms.openlocfilehash: a7a0a8faefdb965384e435ee3a9b059a3acbc3f0
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25382521"
---
# <a name="datacolumns-element-datarecordsettype-complextype-visio-xml"></a>Элемент объектам DataColumn (DataRecordSet_Type complexType) ('Visio XML»)

Содержит все элементы **DataColumn** в записей данных. 
  
## <a name="element-information"></a>Сведения об элементе

|||
|:-----|:-----|
|**Тип элемента** <br/> |[DataColumns_Type](datacolumns_type-complextypevisio-xml.md) <br/> |
|**Пространство имен** <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Файл схемы** <br/> |VisioSchema15.xsd  <br/> |
|**Части документа** <br/> |recordsets.XML  <br/> |
   
## <a name="definition"></a>Определение

```XML
< xs:element name="DataColumns" type="DataColumns_Type" minOccurs="1" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a>Элементы и атрибуты

Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений. 
  
### <a name="parent-elements"></a>Родительские элементы

|**Элемент**|**Тип**|**Описание**|
|:-----|:-----|:-----|
|[Записей данных](datarecordset-element-datarecordsets_type-complextypevisio-xml.md) <br/> |[DataRecordSet_Type](datarecordset_type-complextypevisio-xml.md) <br/> |Сохранение, форматы, обновляет и предоставляет доступ к данным из базы данных в Microsoft Visio.  <br/> |
   
### <a name="child-elements"></a>Дочерние элементы

|**Элемент**|**Тип**|**Описание**|
|:-----|:-----|:-----|
|[DataColumn](datacolumn-element-datacolumns_type-complextypevisio-xml.md) <br/> |[DataColumn_Type](datacolumn_type-complextypevisio-xml.md) <br/> |Определяет, как столбец данных отображается в окне **Внешних данных** в пользовательском интерфейсе Visio и определяет данные в столбце путем определения его типа данных и форматирования.  <br/> |
   
### <a name="attributes"></a>Атрибуты

|**Атрибут**|**Тип**|**Обязательный**|**Описание**|**Возможные значения**|
|:-----|:-----|:-----|:-----|:-----|
|SortAsc  <br/> |XSD:Boolean  <br/> |необязательный  <br/> |Столбец, по которому выполняется сортировка данных.  <br/> |Значения типа xsd:boolean.  <br/> |
|SortColumn  <br/> |XSD:String  <br/> |необязательный  <br/> |Требуется ли для сортировки столбца **SortColumn** в порядке возрастания (1) или убыванию (0).  <br/> |Значения типа xsd:string.  <br/> |
   

