---
title: Элемент Row (Раздел Градиента строки) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 4d823766-5cb0-925c-f622-18025f44426c
description: Содержит цвет, прозрачность и расположение остановки градиента для градиента строки.
ms.openlocfilehash: bfaf3ab8cc16e11051310d7e838b9dddbf7e108d
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/29/2019
ms.locfileid: "34540828"
---
# <a name="row-element-line-gradient-section-visio-xml"></a>Элемент Row (Раздел Градиента строки) (Visio XML)

Содержит цвет, прозрачность и расположение остановки градиента для градиента строки.
  
## <a name="element-information"></a>Сведения об элементе

|||
|:-----|:-----|
|**Тип элемента** <br/> |[LineGradientRow_Type](linegradientrow_type-complextypevisio-xml.md) <br/> |
|**Пространство имен** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Файл схемы** <br/> |VisioSchema15.xsd  <br/> |
|**Части документов** <br/> |document.xml, master#.xml, page#.xml  <br/> |
   
## <a name="definition"></a>Определение

```XML
< xs:element name="Row" type="LineGradientRow_Type" >
</xs:element >
```

## <a name="elements-and-attributes"></a>Элементы и атрибуты

Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений. 
  
### <a name="parent-elements"></a>Родительские элементы

|**Элемент**|**Тип**|**Описание**|
|:-----|:-----|:-----|
|[Section](section-element-sheet_type-complextypevisio-xml.md) <br/> |[Section_Type](section_type-complextypevisio-xml.md) <br/> |Содержит цвет, прозрачность и расположение остановки градиента для градиента строки.  <br/> |
   
### <a name="child-elements"></a>Дочерние элементы

|**Элемент**|**Тип**|**Описание**|
|:-----|:-----|:-----|
|[Cell](cell-element-line-gradient-sectionvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Указывает одно свойство.  <br/> |
   
### <a name="attributes"></a>Атрибуты

|**Атрибут**|**Тип**|**Обязательный**|**Описание**|**Возможные значения**|
|:-----|:-----|:-----|:-----|:-----|
|Del  <br/> |xsd:boolean  <br/> |необязательный  <br/> |Указывает, была ли удалена строка, которая в противном случае была бы унаследована от мастер-фигуры.  <br/> |Значения типа xsd:boolean.  <br/> |
|IX  <br/> |xsd:unsignedInt  <br/> |необязательный  <br/> |Указывает идентификатор для строки на основе одного. Он должен быть unqiue и больше, чем другие идентификаторы в том же разделе. Атрибут IX используется только для разделов Character, Connection, Field, FillGradient, Geometry, Layer, LineGradient, Paragraph, Reviewer, Scratch и Tabs. Строка может иметь только один из атрибутов IX или N.  <br/> |Значения типа xsd:unsignedInt.  <br/> |
|LocalName  <br/> |xsd:string  <br/> |необязательный  <br/> |Указывает уникальное имя строки, зависящие от языка.  <br/> |Значения типа xsd:string.  <br/> |
|Нет  <br/> |xsd:string  <br/> |необязательный  <br/> |Указывает уникальное имя строки, независимое от языка. Атрибут N используется только для разделов User, Property, Actions, Control, Connection, Hyperlink и ActionTag. Строка может иметь только один из атрибутов IX или N.  <br/> |Значения типа xsd:string.  <br/> |
|T  <br/> |xsd:string  <br/> |необязательный  <br/> |Указывает тип геометрического пути, представленного строкой и используемого в визуализации геометрии. Атрибут T используется только для раздела Геометрия.  <br/> |Значения типа xsd:string.  <br/> |
   

