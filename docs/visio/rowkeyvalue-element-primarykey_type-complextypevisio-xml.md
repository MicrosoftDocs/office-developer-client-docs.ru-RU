---
title: Элемент Ровкэйвалуе (Примарикэй_типе complexType) (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 9077ad4b-c539-c0c8-d268-9a009990abdd
description: Задает значение первичного ключа для отдельной строки набора записей.
ms.openlocfilehash: 12d60bb0ccccdcd8c1790678cae4ad1e887e73b6
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32283505"
---
# <a name="rowkeyvalue-element-primarykeytype-complextype-visio-xml"></a>Элемент Ровкэйвалуе (Примарикэй_типе complexType) (' Visio XML ')

Задает значение первичного ключа для отдельной строки набора записей.
  
## <a name="element-information"></a>Сведения об элементе

|||
|:-----|:-----|
|**Тип элемента** <br/> |[Ровкэйвалуе_типе](rowkeyvalue_type-complextypevisio-xml.md) <br/> |
|**Пространство имен** <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Файл схемы** <br/> |VisioSchema15. xsd  <br/> |
|**Части документа** <br/> |Recordset. XML  <br/> |
   
## <a name="definition"></a>Определение

```XML
< xs:element name="RowKeyValue" type="RowKeyValue_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a>Элементы и атрибуты

Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений. 
  
### <a name="parent-elements"></a>Родительские элементы

|**Элемент**|**Тип**|**Описание**|
|:-----|:-----|:-----|
|[PrimaryKey](primarykey-element-datarecordset_type-complextypevisio-xml.md) <br/> |[Примарикэй_типе](primarykey_type-complextypevisio-xml.md) <br/> |Задает первичный ключ набора записей.  <br/> |
   
### <a name="child-elements"></a>Дочерние элементы

Нет.
  
### <a name="attributes"></a>Атрибуты

|**Атрибут**|**Тип**|**Обязательный**|**Описание**|**Возможные значения**|
|:-----|:-----|:-----|:-----|:-----|
|RowID  <br/> |XSD: Унсигнединт  <br/> |Обязательный  <br/> |Уникальное значение, идентифицирующее строку в наборе записей.  <br/> |Значения типа XSD: Унсигнединт.  <br/> |
|Значение  <br/> |XSD: строка  <br/> |Обязательный  <br/> |Значение первичного ключа для этой строки набора записей.  <br/> |Значения типа String: XSD.  <br/> |
   

