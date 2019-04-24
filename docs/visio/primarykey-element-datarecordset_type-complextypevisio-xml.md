---
title: Элемент PrimaryKey (Датарекордсет_типе complexType) (' XML ' Visio ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 47533e6e-0a48-af61-a0c2-b2cec140ae4b
description: Определяет один или несколько столбцов первичного ключа в наборе записей данных.
ms.openlocfilehash: c001c343c33e65c3990744b885f1c345575b1ab3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32355999"
---
# <a name="primarykey-element-datarecordsettype-complextype-visio-xml"></a>Элемент PrimaryKey (Датарекордсет_типе complexType) (' XML ' Visio ')

Определяет один или несколько столбцов первичного ключа в наборе записей данных.
  
## <a name="element-information"></a>Сведения об элементе

|||
|:-----|:-----|
|**Тип элемента** <br/> |[Примарикэй_типе](primarykey_type-complextypevisio-xml.md) <br/> |
|**Пространство имен** <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Файл схемы** <br/> |VisioSchema15. xsd  <br/> |
|**Части документа** <br/> |Recordset. XML  <br/> |
   
## <a name="definition"></a>Определение

```XML
< xs:element name="PrimaryKey" type="PrimaryKey_Type" minOccurs="0" maxOccurs="unbounded" >
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
|[Ровкэйвалуе](rowkeyvalue-element-primarykey_type-complextypevisio-xml.md) <br/> |[Ровкэйвалуе_типе](rowkeyvalue_type-complextypevisio-xml.md) <br/> |Задает значение этого компонента первичного ключа для отдельной строки набора записей. ДОЛЖЕН быть хотя бы один экземпляр этого дочернего элемента.  <br/> |
   
### <a name="attributes"></a>Атрибуты

|**Атрибут**|**Тип**|**Обязательный**|**Описание**|**Возможные значения**|
|:-----|:-----|:-----|:-----|:-----|
|Колумннамеид  <br/> |XSD: строка  <br/> |необязательный  <br/> |Задает имя поля, которое является компонентом первичного ключа. Он должен быть значением атрибута **колумннамеид** элемента потомков Датаколумн_типе элемента датарекордсет_типе, для которого указывается первичный ключ.  <br/> |Значения типа String: XSD.  <br/> |
   

