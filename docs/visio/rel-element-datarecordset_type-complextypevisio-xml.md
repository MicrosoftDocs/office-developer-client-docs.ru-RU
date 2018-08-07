---
title: Элемент Rel (DataRecordSet_Type complexType) ('Visio XML»)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 9148c73f-970d-61f8-b5da-e3bc748a6541
description: Указывает связь с частью с соответствующим набором записей и сведения о привязке данных.
ms.openlocfilehash: 1086f2e812fc4be4b291c7a783877f4ccd39c815
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19814545"
---
# <a name="rel-element-datarecordsettype-complextype-visio-xml"></a>Элемент Rel (DataRecordSet_Type complexType) ('Visio XML»)

Указывает связь с частью с соответствующим набором записей и сведения о привязке данных.
  
## <a name="element-information"></a>Сведения об элементе

|||
|:-----|:-----|
|**Тип элемента** <br/> |[Rel_Type](rel_type-complextypevisio-xml.md) <br/> |
|**Пространство имен** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Файл схемы** <br/> |VisioSchema15.xsd  <br/> |
|**Части документа** <br/> |Pages.XML, masters.xml, recordsets.xml, страницы # .xml, главные # .xml  <br/> |
   
## <a name="definition"></a>Определение

```XML
< xs:element name="Rel" type="Rel_Type" minOccurs="1" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a>Элементы и атрибуты

Если схема определяет специальные требования, такие как **последовательность**, **minOccurs**, **maxOccurs**и **выбора**, обратитесь к разделу определение. 
  
### <a name="parent-elements"></a>Родительские элементы

|**Элемент**|**Тип**|**Описание**|
|:-----|:-----|:-----|
|[Записей данных](datarecordset-element-datarecordsets_type-complextypevisio-xml.md) <br/> |[DataRecordSet_Type](datarecordset_type-complextypevisio-xml.md) <br/> |Задает один экземпляр набора записей и сведения о привязке данных, хранимых в документе.  <br/> |
   
### <a name="child-elements"></a>Дочерние элементы

Нет.
  
### <a name="attributes"></a>Атрибуты

|**Атрибут**|**Тип**|**Обязательное**|**Описание**|**Возможные значения**|
|:-----|:-----|:-----|:-----|:-----|
|r: код  <br/> |XSD:String  <br/> См. раздел "Замечания".  <br/> |Обязательный  <br/> |Указывает связь с частью.  <br/> |«Удалить #»  <br/> См. раздел "Замечания".  <br/> |
   
## <a name="remarks"></a>Замечания

Значение атрибута **r: id** должен быть указан тип **простом типе ST_RelationshipID** . Тип **простом типе ST_RelationshipID** — это строка, которая должна быть в формате «избавиться #», где последний символ, должно быть числом. Номер должен быть уникальным во все элементы одного уровня элемента **Rel** . 
  
Дополнительные сведения о типе простом типе ST_RelationshipID можно найти в [спецификации ISO/IEC 29500 часть 1](http://www.iso.org/iso/home/store/catalogue_tc/catalogue_detail.md?csnumber=61750).
  

