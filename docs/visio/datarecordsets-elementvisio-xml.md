---
title: Элемент DataRecordSets ('Visio XML»)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: c75b3233-9ac5-d29c-a658-d554e86e6be4
description: Содержит все элементы записей данных в документе.
ms.openlocfilehash: 205c4d963f111490698627040c190f322f2f36a1
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19813546"
---
# <a name="datarecordsets-element-visio-xml"></a>Элемент DataRecordSets ('Visio XML»)

Содержит все элементы **записей данных** в документе. 
  
## <a name="element-information"></a>Сведения об элементе

|||
|:-----|:-----|
|**Тип элемента** <br/> |[DataRecordSets_Type](datarecordsets_type-complextypevisio-xml.md) <br/> |
|**Пространство имен** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Файл схемы** <br/> |VisioSchema15.xsd  <br/> |
|**Части документа** <br/> |recordsets.XML  <br/> |
   
## <a name="definition"></a>Определение

```XML
< xs:element name="DataRecordSets" type="DataRecordSets_Type" >
</xs:element >
```

## <a name="elements-and-attributes"></a>Элементы и атрибуты

Если схема определяет специальные требования, такие как **последовательность**, **minOccurs**, **maxOccurs**и **выбора**, обратитесь к разделу определение. 
  
### <a name="parent-elements"></a>Родительские элементы

Нет.
  
### <a name="child-elements"></a>Дочерние элементы

|**Элемент**|**Тип**|**Описание**|
|:-----|:-----|:-----|
|[Записей данных](datarecordset-element-datarecordsets_type-complextypevisio-xml.md) <br/> |[DataRecordSet_Type](datarecordset_type-complextypevisio-xml.md) <br/> |Содержит все элементы **записей данных** в документе.  <br/> |
   
### <a name="attributes"></a>Атрибуты

|**Атрибут**|**Тип**|**Обязательное**|**Описание**|**Возможные значения**|
|:-----|:-----|:-----|:-----|:-----|
|ActiveRecordsetID  <br/> |XSD:unsignedInt  <br/> |необязательный  <br/> |Открывает идентификатор набора записей активных данных в окно **Внешних данных** , когда окно закроется, так что он может быть восстановлена следующем окне.  <br/> |Значения типа xsd:unsignedInt.  <br/> |
|DataWindowOrder  <br/> |XSD:String  <br/> |необязательный  <br/> |Порядок наборов записей данных, отображаемых на вкладках окно **Внешних данных** . Упорядоченный список идентификаторов данных записей, разделенных точкой с запятой.  <br/> |Значения типа xsd:string.  <br/> |
|NextID  <br/> |XSD:unsignedInt  <br/> |Обязательный  <br/> |Далее доступные идентификатор нового набора записей данных.  <br/> |Значения типа xsd:unsignedInt.  <br/> |
   

