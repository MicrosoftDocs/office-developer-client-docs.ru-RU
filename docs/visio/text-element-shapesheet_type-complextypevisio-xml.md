---
title: Элемент text (Шапешит_типе complexType) (XML для Visio)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 46211968-9ad8-07da-f725-3ad136b7a8a1
description: Содержит текст фигуры.
ms.openlocfilehash: 4b03bc2539b80e49daae9d14f3e2ad07a51de9f1
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/29/2019
ms.locfileid: "34541927"
---
# <a name="text-element-shapesheettype-complextype-visio-xml"></a>Элемент text (Шапешит_типе complexType) (XML для Visio)

Содержит текст фигуры.
  
## <a name="element-information"></a>Сведения об элементе

|||
|:-----|:-----|
|**Тип элемента** <br/> |[Текст_типе](text_type-complextypevisio-xml.md) <br/> |
|**Пространство имен** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
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
  

