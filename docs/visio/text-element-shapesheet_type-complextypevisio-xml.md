---
title: Элемент text (Шапешит_типе complexType) (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 46211968-9ad8-07da-f725-3ad136b7a8a1
description: Содержит текст фигуры.
ms.openlocfilehash: f2c809d7db895a3635a5898d83d4583cd38f1249
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32332373"
---
# <a name="text-element-shapesheettype-complextype-visio-xml"></a>Элемент text (Шапешит_типе complexType) (' Visio XML ')

Содержит текст фигуры.
  
## <a name="element-information"></a>Сведения об элементе

|||
|:-----|:-----|
|**Тип элемента** <br/> |[Текст_типе](text_type-complextypevisio-xml.md) <br/> |
|**Пространство имен** <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Файл схемы** <br/> |VisioSchema15. xsd  <br/> |
|**Части документа** <br/> |страница #. XML, Master #. XML  <br/> |
   
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
|[Shape](shape-element-shapes_type-complextypevisio-xml.md) <br/> |[Шапешит_типе](shapesheet_type-complextypevisio-xml.md) <br/> |Содержит элементы, определяющие фигуру в **главной**, **странице**или элементе фигуры группы.  <br/> |
   
### <a name="child-elements"></a>Дочерние элементы

|**Элемент**|**Тип**|**Описание**|
|:-----|:-----|:-----|
|[CP](cp-element-text_type-complextypevisio-xml.md) <br/> |[Кп_типе](cp_type-complextypevisio-xml.md) <br/> |Помечает начало свойства знака, которое отформатировано в соответствии с соответствующим элементом char.  <br/> |
|[FLD](fld-element-text_type-complextypevisio-xml.md) <br/> |[Флд_типе](fld_type-complextypevisio-xml.md) <br/> |Указывает точку вставки текстового поля для соответствующего элемента Field.  <br/> |
|[PP](pp-element-text_type-complextypevisio-xml.md) <br/> |[Пп_типе](pp_type-complextypevisio-xml.md) <br/> |Задает начало работы со свойствами абзаца.  <br/> |
|[Пи](tp-element-text_type-complextypevisio-xml.md) <br/> |[Тп_типе](tp_type-complextypevisio-xml.md) <br/> |Задает начало работы со свойствами вкладок.  <br/> |
   
### <a name="attributes"></a>Атрибуты

Нет.
  

