---
title: Элемент DataRecordSets ('Visio XML»)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: c75b3233-9ac5-d29c-a658-d554e86e6be4
description: Содержит все элементы записей данных в документе.
ms.openlocfilehash: 7730e55f0025181db193a1e64226e879f9072e90
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25401491"
---
# <a name="datarecordsets-element-visio-xml"></a>Элемент DataRecordSets ('Visio XML»)

Содержит все элементы **записей данных** в документе. 
  
## <a name="element-information"></a>Сведения об элементе

|||
|:-----|:-----|
|**Тип элемента** <br/> |[DataRecordSets_Type](datarecordsets_type-complextypevisio-xml.md) <br/> |
|**Пространство имен** <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Файл схемы** <br/> |VisioSchema15.xsd  <br/> |
|**Части документа** <br/> |recordsets.XML  <br/> |
   
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
|[Записей данных](datarecordset-element-datarecordsets_type-complextypevisio-xml.md) <br/> |[DataRecordSet_Type](datarecordset_type-complextypevisio-xml.md) <br/> |Содержит все элементы **записей данных** в документе.  <br/> |
   
### <a name="attributes"></a>Атрибуты

|**Атрибут**|**Тип**|**Обязательный**|**Описание**|**Возможные значения**|
|:-----|:-----|:-----|:-----|:-----|
|ActiveRecordsetID  <br/> |XSD:unsignedInt  <br/> |необязательный  <br/> |Открывает идентификатор набора записей активных данных в окно **Внешних данных** , когда окно закроется, так что он может быть восстановлена следующем окне.  <br/> |Значения типа xsd:unsignedInt.  <br/> |
|DataWindowOrder  <br/> |XSD:String  <br/> |необязательный  <br/> |Порядок наборов записей данных, отображаемых на вкладках окно **Внешних данных** . Упорядоченный список идентификаторов данных записей, разделенных точкой с запятой.  <br/> |Значения типа xsd:string.  <br/> |
|NextID  <br/> |XSD:unsignedInt  <br/> |Обязательный  <br/> |Далее доступные идентификатор нового набора записей данных.  <br/> |Значения типа xsd:unsignedInt.  <br/> |
   

