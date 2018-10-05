---
title: Элемент Text (ShapeSheet_Type complexType) ('Visio XML»)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 46211968-9ad8-07da-f725-3ad136b7a8a1
description: Содержит текст фигуры.
ms.openlocfilehash: f2c809d7db895a3635a5898d83d4583cd38f1249
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25385916"
---
# <a name="text-element-shapesheettype-complextype-visio-xml"></a>Элемент Text (ShapeSheet_Type complexType) ('Visio XML»)

Содержит текст фигуры.
  
## <a name="element-information"></a>Сведения об элементе

|||
|:-----|:-----|
|**Тип элемента** <br/> |[Text_Type](text_type-complextypevisio-xml.md) <br/> |
|**Пространство имен** <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Файл схемы** <br/> |VisioSchema15.xsd  <br/> |
|**Части документа** <br/> |страницы # .xml, главные # .xml  <br/> |
   
## <a name="definition"></a>Определение

```XML
< xs:element name="Text" type="Text_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a>Элементы и атрибуты

Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений. 
  
### <a name="parent-elements"></a>Родительские элементы

|**Элемент**|**Тип**|**Описание**|
|:-----|:-----|:-----|
|[Фигура](shape-element-shapes_type-complextypevisio-xml.md) <br/> |[ShapeSheet_Type](shapesheet_type-complextypevisio-xml.md) <br/> |Содержит элементы, определяющие фигуры в **Образец**, **страница**или элемент группы фигур.  <br/> |
   
### <a name="child-elements"></a>Дочерние элементы

|**Элемент**|**Тип**|**Описание**|
|:-----|:-----|:-----|
|[позиции символа](cp-element-text_type-complextypevisio-xml.md) <br/> |[cp_Type](cp_type-complextypevisio-xml.md) <br/> |Метки в начале символ свойства запустите то есть отформатированное в соответствии с соответствующих элементов (знак).  <br/> |
|[Fld](fld-element-text_type-complextypevisio-xml.md) <br/> |[fld_Type](fld_type-complextypevisio-xml.md) <br/> |Указывает точку вставки текстового поля для соответствующего элемента Field.  <br/> |
|[PP](pp-element-text_type-complextypevisio-xml.md) <br/> |[pp_Type](pp_type-complextypevisio-xml.md) <br/> |Выполнение в начале свойств абзаца.  <br/> |
|[TP](tp-element-text_type-complextypevisio-xml.md) <br/> |[tp_Type](tp_type-complextypevisio-xml.md) <br/> |Задает начало вкладок свойств, запустите.  <br/> |
   
### <a name="attributes"></a>Атрибуты

Нет.
  

