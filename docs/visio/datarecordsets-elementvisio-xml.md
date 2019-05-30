---
title: Элемент RecordSets (XML для Visio)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: c75b3233-9ac5-d29c-a658-d554e86e6be4
description: Содержит все элементы Record в документе.
ms.openlocfilehash: efa7d58eabc1b1192862dbbe090ddd5008947c1d
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/29/2019
ms.locfileid: "34542445"
---
# <a name="datarecordsets-element-visio-xml"></a>Элемент RecordSets (XML для Visio)

Содержит все элементы **Record** в документе. 
  
## <a name="element-information"></a>Сведения об элементе

|||
|:-----|:-----|
|**Тип элемента** <br/> |[Датарекордсетс_типе](datarecordsets_type-complextypevisio-xml.md) <br/> |
|**Пространство имен** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Файл схемы** <br/> |VisioSchema15. xsd  <br/> |
|**Части документа** <br/> |Recordset. XML  <br/> |
   
## <a name="definition"></a>Определение

```XML
< xs:element name="DataRecordSets" type="DataRecordSets_Type" >
</xs:element >
```

## <a name="elements-and-attributes"></a>Элементы и атрибуты

Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений. 
  
### <a name="parent-elements"></a>Родительские элементы

Нет.
  
### <a name="child-elements"></a>Дочерние элементы

|**Элемент**|**Тип**|**Описание**|
|:-----|:-----|:-----|
|[DataRecordSet](datarecordset-element-datarecordsets_type-complextypevisio-xml.md) <br/> |[Датарекордсет_типе](datarecordset_type-complextypevisio-xml.md) <br/> |Содержит все элементы **Record** в документе.  <br/> |
   
### <a name="attributes"></a>Атрибуты

|**Атрибут**|**Тип**|**Обязательный**|**Описание**|**Возможные значения**|
|:-----|:-----|:-----|:-----|:-----|
|Активерекордсетид  <br/> |XSD: Унсигнединт  <br/> |необязательный  <br/> |ИДЕНТИФИКАТОР активного набора данных в окне " **Внешние данные** " при закрытии окна, чтобы его можно было восстановить при следующем открытии окна.  <br/> |Значения типа XSD: Унсигнединт.  <br/> |
|Датавиндовордер  <br/> |XSD: строка  <br/> |необязательный  <br/> |Порядок наборов записей данных, отображаемых на вкладках окна " **Внешние данные** ". Упорядоченный список идентификаторов записей данных, разделенных точкой с запятой.  <br/> |Значения типа String: XSD.  <br/> |
|Некстид  <br/> |XSD: Унсигнединт  <br/> |Обязательный  <br/> |Следующий доступный идентификатор для нового набора записей данных.  <br/> |Значения типа XSD: Унсигнединт.  <br/> |
   

