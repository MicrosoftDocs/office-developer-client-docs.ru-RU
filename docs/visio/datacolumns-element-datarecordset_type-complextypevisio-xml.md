---
title: Элемент DataColumns (Датарекордсет_типе complexType) (' XML ' Visio ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 34e25349-d0fa-b3a0-425b-778184e9f58f
description: Содержит все элементы DataColumn в наборе данных данных.
ms.openlocfilehash: a7a0a8faefdb965384e435ee3a9b059a3acbc3f0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32345250"
---
# <a name="datacolumns-element-datarecordsettype-complextype-visio-xml"></a>Элемент DataColumns (Датарекордсет_типе complexType) (' XML ' Visio ')

Содержит все элементы **DataColumn** в наборе данных данных. 
  
## <a name="element-information"></a>Сведения об элементе

|||
|:-----|:-----|
|**Тип элемента** <br/> |[Датаколумнс_типе](datacolumns_type-complextypevisio-xml.md) <br/> |
|**Пространство имен** <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Файл схемы** <br/> |VisioSchema15. xsd  <br/> |
|**Части документа** <br/> |Recordset. XML  <br/> |
   
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
|[DataRecordSet](datarecordset-element-datarecordsets_type-complextypevisio-xml.md) <br/> |[Датарекордсет_типе](datarecordset_type-complextypevisio-xml.md) <br/> |Хранение, форматирование, обновление и предоставление данных, запрашиваемых из базы данных в Microsoft Visio.  <br/> |
   
### <a name="child-elements"></a>Дочерние элементы

|**Элемент**|**Тип**|**Описание**|
|:-----|:-----|:-----|
|[DataColumn](datacolumn-element-datacolumns_type-complextypevisio-xml.md) <br/> |[Датаколумн_типе](datacolumn_type-complextypevisio-xml.md) <br/> |Определяет, как столбец данных отображается в окне " **Внешние данные** " в пользовательском интерфейсе Visio, и определяет данные в столбце, определяя тип данных и форматирование.  <br/> |
   
### <a name="attributes"></a>Атрибуты

|**Атрибут**|**Тип**|**Обязательный**|**Описание**|**Возможные значения**|
|:-----|:-----|:-----|:-----|:-----|
|Сортаск  <br/> |XSD: Boolean  <br/> |необязательный  <br/> |Столбец, по которому необходимо отсортировать данные.  <br/> |Значения типа XSD: Boolean.  <br/> |
|SortColumn  <br/> |XSD: строка  <br/> |необязательный  <br/> |Следует ли сортировать столбец **sortColumn** в порядке возрастания (1) или убыванию (0).  <br/> |Значения типа String: XSD.  <br/> |
   

