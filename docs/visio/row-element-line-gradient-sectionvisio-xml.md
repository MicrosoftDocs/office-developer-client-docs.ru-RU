---
title: Элемент Row (строка градиента раздел) ('Visio XML»)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 4d823766-5cb0-925c-f622-18025f44426c
description: Содержит цвет, прозрачность и положение градиента для градиента строки.
ms.openlocfilehash: 105d93344343f223a6b5d909f1174f7df56ffb4d
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25383186"
---
# <a name="row-element-line-gradient-section-visio-xml"></a>Элемент Row (строка градиента раздел) ('Visio XML»)

Содержит цвет, прозрачность и положение градиента для градиента строки.
  
## <a name="element-information"></a>Сведения об элементе

|||
|:-----|:-----|
|**Тип элемента** <br/> |[LineGradientRow_Type](linegradientrow_type-complextypevisio-xml.md) <br/> |
|**Пространство имен** <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Файл схемы** <br/> |VisioSchema15.xsd  <br/> |
|**Части документа** <br/> |Document.XML, главные # .xml, страницы # .xml  <br/> |
   
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
|[Раздел](section-element-sheet_type-complextypevisio-xml.md) <br/> |[Section_Type](section_type-complextypevisio-xml.md) <br/> |Содержит цвет, прозрачность и положение градиента для градиента строки.  <br/> |
   
### <a name="child-elements"></a>Дочерние элементы

|**Элемент**|**Тип**|**Описание**|
|:-----|:-----|:-----|
|[Cell](cell-element-line-gradient-sectionvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Задает отдельное свойство.  <br/> |
   
### <a name="attributes"></a>Атрибуты

|**Атрибут**|**Тип**|**Обязательный**|**Описание**|**Возможные значения**|
|:-----|:-----|:-----|:-----|:-----|
|DEL  <br/> |XSD:Boolean  <br/> |необязательный  <br/> |Указывает, был ли удален строку, в противном случае будут унаследованы от образца фигуры.  <br/> |Значения типа xsd:boolean.  <br/> |
|IX  <br/> |XSD:unsignedInt  <br/> |необязательный  <br/> |Указывает идентификатор на основе одной строки. Оно должно быть unqiue и больше, чем другие идентификаторы в одном разделе. Атрибут IX используется только для разделов символ, подключения, поле, FillGradient, геометрии, уровень, LineGradient, абзаца, редактор, нуля и вкладок. Строка может иметь только один из атрибутов IX или N.  <br/> |Значения типа xsd:unsignedInt.  <br/> |
|LocalName  <br/> |XSD:String  <br/> |необязательный  <br/> |Указывает уникальное имя зависит от языка строки.  <br/> |Значения типа xsd:string.  <br/> |
|N  <br/> |XSD:String  <br/> |необязательный  <br/> |Указывает уникальное имя зависящего от языка строки. Атрибут N используется только для пользователя, свойство, действия, элемент управления, подключения, гиперссылки и ActionTag разделы. Строка может иметь только один из атрибутов IX или N.  <br/> |Значения типа xsd:string.  <br/> |
|T  <br/> |XSD:String  <br/> |необязательный  <br/> |Указывает тип геометрического пути представленного строкой и используется в геометрии визуализации. Атрибут T используется только для раздел геометрии.  <br/> |Значения типа xsd:string.  <br/> |
   

