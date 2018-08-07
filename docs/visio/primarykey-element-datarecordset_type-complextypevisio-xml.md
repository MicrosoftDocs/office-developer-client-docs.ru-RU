---
title: Элемент PrimaryKey (DataRecordSet_Type complexType) ('Visio XML»)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 47533e6e-0a48-af61-a0c2-b2cec140ae4b
description: Определяет один или несколько столбцы первичных ключей в записей данных.
ms.openlocfilehash: f720636bbdf2c55baca6d98aa7d0761607e53ffc
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19814496"
---
# <a name="primarykey-element-datarecordsettype-complextype-visio-xml"></a>Элемент PrimaryKey (DataRecordSet_Type complexType) ('Visio XML»)

Определяет один или несколько столбцы первичных ключей в записей данных.
  
## <a name="element-information"></a>Сведения об элементе

|||
|:-----|:-----|
|**Тип элемента** <br/> |[PrimaryKey_Type](primarykey_type-complextypevisio-xml.md) <br/> |
|**Пространство имен** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Файл схемы** <br/> |VisioSchema15.xsd  <br/> |
|**Части документа** <br/> |recordsets.XML  <br/> |
   
## <a name="definition"></a>Определение

```XML
< xs:element name="PrimaryKey" type="PrimaryKey_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a>Элементы и атрибуты

Если схема определяет специальные требования, такие как **последовательность**, **minOccurs**, **maxOccurs**и **выбора**, обратитесь к разделу определение. 
  
### <a name="parent-elements"></a>Родительские элементы

|**Элемент**|**Тип**|**Описание**|
|:-----|:-----|:-----|
|[Записей данных](datarecordset-element-datarecordsets_type-complextypevisio-xml.md) <br/> |[DataRecordSet_Type](datarecordset_type-complextypevisio-xml.md) <br/> |Сохранение, форматы, обновляет и предоставляет доступ к данным из базы данных в Microsoft Visio.  <br/> |
   
### <a name="child-elements"></a>Дочерние элементы

|**Элемент**|**Тип**|**Описание**|
|:-----|:-----|:-----|
|[RowKeyValue](rowkeyvalue-element-primarykey_type-complextypevisio-xml.md) <br/> |[RowKeyValue_Type](rowkeyvalue_type-complextypevisio-xml.md) <br/> |Указывает значение этот компонент основной ключ для отдельных строк набора записей. НЕОБХОДИМО быть по крайней мере одно вхождение дочернего элемента.  <br/> |
   
### <a name="attributes"></a>Атрибуты

|**Атрибут**|**Тип**|**Обязательное**|**Описание**|**Возможные значения**|
|:-----|:-----|:-----|:-----|:-----|
|ColumnNameID  <br/> |XSD:String  <br/> |необязательный  <br/> |Указывает имя поля, который является частью первичного ключа. Оно должно быть значение атрибута **ColumnNameID** элемента DataColumn_Type потомкам из DataRecordSet_Type, указано, первичный ключ.  <br/> |Значения типа xsd:string.  <br/> |
   

