---
title: Элемент Rel (ForeignData_Type complexType) ('Visio XML»)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 7ed604ef-e001-f379-92c3-391a18f22bb3
description: Указывает отношение между фигурой и части документа, который содержит данные изображения, связанного с формой.
ms.openlocfilehash: 2667d5b0b940384f10df62dfc0fbf6acfa7d4ba6
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25383445"
---
# <a name="rel-element-foreigndatatype-complextype-visio-xml"></a>Элемент Rel (ForeignData_Type complexType) ('Visio XML»)

Указывает отношение между фигурой и части документа, который содержит данные изображения, связанного с формой.
  
## <a name="element-information"></a>Сведения об элементе

|||
|:-----|:-----|
|**Тип элемента** <br/> |[Rel_Type](rel_type-complextypevisio-xml.md) <br/> |
|**Пространство имен** <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Файл схемы** <br/> |VisioSchema15.xsd  <br/> |
|**Части документа** <br/> |Pages.XML, masters.xml, recordsets.xml, страницы # .xml, главные # .xml  <br/> |
   
## <a name="definition"></a>Определение

```XML
< xs:element name="Rel" type="Rel_Type" minOccurs="1" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a>Элементы и атрибуты

Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений. 
  
### <a name="parent-elements"></a>Родительские элементы

|**Элемент**|**Тип**|**Описание**|
|:-----|:-----|:-----|
|[ForeignData](foreigndata-element-shapesheet_type-complextypevisio-xml.md) <br/> |[ForeignData_Type](foreigndata_type-complextypevisio-xml.md) <br/> |Один экземпляр данных изображения, хранящиеся в документе.  <br/> |
   
### <a name="child-elements"></a>Дочерние элементы

Нет.
  
### <a name="attributes"></a>Атрибуты

|**Атрибут**|**Тип**|**Обязательный**|**Описание**|**Возможные значения**|
|:-----|:-----|:-----|:-----|:-----|
|r: код  <br/> |XSD:String  <br/> См. раздел "Замечания".  <br/> |Обязательный  <br/> |Указывает связь с частью.  <br/> |«Удалить #»  <br/> См. раздел "Замечания".  <br/> |
   
## <a name="remarks"></a>Замечания

Значение атрибута **r: id** должен быть указан тип **простом типе ST_RelationshipID** . Тип **простом типе ST_RelationshipID** — это строка, которая должна быть в формате «избавиться #», где последний символ, должно быть числом. Номер должен быть уникальным во все элементы одного уровня элемента **Rel** . 
  
Дополнительные сведения о типе простом типе ST_RelationshipID можно найти в [спецификации ISO/IEC 29500 часть 1](https://www.iso.org/iso/home/store/catalogue_tc/catalogue_detail.md?csnumber=61750).
  

