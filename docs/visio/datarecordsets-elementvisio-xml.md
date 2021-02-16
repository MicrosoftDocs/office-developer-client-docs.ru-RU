---
title: Элемент DataRecordSets (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: c75b3233-9ac5-d29c-a658-d554e86e6be4
description: Содержит все элементы DataRecordset в документе.
ms.openlocfilehash: efa7d58eabc1b1192862dbbe090ddd5008947c1d
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/29/2019
ms.locfileid: "34542445"
---
# <a name="datarecordsets-element-visio-xml"></a>Элемент DataRecordSets (Visio XML)

Содержит все **элементы DataRecordset** в документе. 
  
## <a name="element-information"></a>Сведения об элементе

|||
|:-----|:-----|
|**Тип элемента** <br/> |[DataRecordSets_Type](datarecordsets_type-complextypevisio-xml.md) <br/> |
|**Пространство имен** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Файл схемы** <br/> |VisioSchema15.xsd  <br/> |
|**Части документа** <br/> |recordsets.xml  <br/> |
   
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
|[DataRecordSet](datarecordset-element-datarecordsets_type-complextypevisio-xml.md) <br/> |[DataRecordSet_Type](datarecordset_type-complextypevisio-xml.md) <br/> |Содержит все **элементы DataRecordset** в документе.  <br/> |
   
### <a name="attributes"></a>Атрибуты

|**Атрибут**|**Тип**|**Обязательный**|**Описание**|**Возможные значения**|
|:-----|:-----|:-----|:-----|:-----|
|ActiveRecordsetID  <br/> |xsd:unsignedInt  <br/> |необязательный  <br/> |ИД активного наборов записей  данных в окне внешних данных при закрытии окна, чтобы его можно было восстановить при следующем открываемом окне.  <br/> |Значения типа xsd:unsignedInt.  <br/> |
|DataWindowOrder  <br/> |xsd:string  <br/> |необязательный  <br/> |Порядок наборов записей данных, отображаемого на вкладке окна **внешних** данных. Упорядоченный список ИД наборов записей данных, разделенных за двоеточием.  <br/> |Значения типа xsd:string.  <br/> |
|NextID  <br/> |xsd:unsignedInt  <br/> |Обязательный  <br/> |Следующий доступный ИД для нового наборов записей данных.  <br/> |Значения типа xsd:unsignedInt.  <br/> |
   

