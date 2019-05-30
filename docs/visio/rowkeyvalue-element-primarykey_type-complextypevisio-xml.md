---
title: Элемент Ровкэйвалуе (Примарикэй_типе complexType) (XML для Visio)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 9077ad4b-c539-c0c8-d268-9a009990abdd
description: Задает значение первичного ключа для отдельной строки набора записей.
ms.openlocfilehash: b21f479a9c0404dc8a3b737208e4d0d634b556f4
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/29/2019
ms.locfileid: "34538132"
---
# <a name="rowkeyvalue-element-primarykeytype-complextype-visio-xml"></a>Элемент Ровкэйвалуе (Примарикэй_типе complexType) (XML для Visio)

Задает значение первичного ключа для отдельной строки набора записей.
  
## <a name="element-information"></a>Сведения об элементе

|||
|:-----|:-----|
|**Тип элемента** <br/> |[Ровкэйвалуе_типе](rowkeyvalue_type-complextypevisio-xml.md) <br/> |
|**Пространство имен** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
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
   

