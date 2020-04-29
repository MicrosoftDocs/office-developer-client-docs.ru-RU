---
title: Элемент Ровмап (DataRecordSet_Type complexType) (XML для Visio)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: f90dc76b-7f0b-dead-38c0-97062a7b76a6
description: Сопоставляет строку набора записей данных с фигурой.
ms.openlocfilehash: 178ceb06d64bfc9ef50f75dd22f8bd94f09f5c33
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/29/2019
ms.locfileid: "34540772"
---
# <a name="rowmap-element-datarecordset_type-complextype-visio-xml"></a>Элемент Ровмап (DataRecordSet_Type complexType) (XML для Visio)

Сопоставляет строку набора записей данных с фигурой.
  
## <a name="element-information"></a>Сведения об элементе

|||
|:-----|:-----|
|**Тип элемента** <br/> |[RowMap_Type](rowmap_type-complextypevisio-xml.md) <br/> |
|**Пространство имен** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Файл схемы** <br/> |VisioSchema15. xsd  <br/> |
|**Части документа** <br/> |Recordset. XML  <br/> |
   
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
|[DataRecordSet](datarecordset-element-datarecordsets_type-complextypevisio-xml.md) <br/> |[DataRecordSet_Type](datarecordset_type-complextypevisio-xml.md) <br/> |Хранение, форматирование, обновление и предоставление данных, запрашиваемых из базы данных в Microsoft Visio.  <br/> |
   
### <a name="child-elements"></a>Дочерние элементы

Нет.
  
### <a name="attributes"></a>Атрибуты

|**Атрибут**|**Тип**|**Обязательный**|**Описание**|**Возможные значения**|
|:-----|:-----|:-----|:-----|:-----|
|PageID  <br/> |XSD: Унсигнединт  <br/> |Обязательный  <br/> |Идентификатор страницы, связанной с данными в строке набора записей данных, определяемой **ROWID**.  <br/> |Значения типа XSD: Унсигнединт.  <br/> |
|RowID  <br/> |XSD: Унсигнединт  <br/> |Обязательный  <br/> |Идентификатор строки, уникальный в пределах набора данных.  <br/> |Значения типа XSD: Унсигнединт.  <br/> |
|шапеид  <br/> |XSD: Унсигнединт  <br/> |Обязательный  <br/> |ИДЕНТИФИКАТОР фигуры для фигуры, связанной с данными в строке набора записей Data, которая указана в **ROWID**.  <br/> |Значения типа XSD: Унсигнединт.  <br/> |
   

