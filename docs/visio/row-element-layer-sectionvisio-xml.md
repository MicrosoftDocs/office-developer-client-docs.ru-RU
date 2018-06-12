---
title: Элемент Row (раздел Layer) ('Visio XML»)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 9b884be2-3eed-0864-6a6c-877b43d9065f
description: Содержит элементы, определяющие одного уровня и его свойства для страницы.
ms.openlocfilehash: ed8368c0c7215068cbbfcdd89c1f5b56969b5a06
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19814685"
---
# <a name="row-element-layer-section-visio-xml"></a>Элемент Row (раздел Layer) ('Visio XML»)

Содержит элементы, определяющие одного уровня и его свойства для страницы.
  
## <a name="element-information"></a>Сведения об элементе

|||
|:-----|:-----|
|**Тип элемента** <br/> |[LayerRow_Type](layerrow_type-complextypevisio-xml.md) <br/> |
|**Пространство имен** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Файл схемы** <br/> |VisioSchema15.xsd  <br/> |
|**Части документа** <br/> |Masters.XML, pages.xml  <br/> |
   
## <a name="definition"></a>Определение

```XML
< xs:element name="Row" type="LayerRow_Type" >
</xs:element >
```

## <a name="elements-and-attributes"></a>Элементы и атрибуты

Если схема определяет специальные требования, такие как **последовательность**, **minOccurs**, **maxOccurs**и **выбора**, обратитесь к разделу определение. 
  
### <a name="parent-elements"></a>Родительские элементы

|**Элемент**|**Тип**|**Описание**|
|:-----|:-----|:-----|
|[Раздел](section-element-sheet_type-complextypevisio-xml.md) <br/> |[Section_Type](section_type-complextypevisio-xml.md) <br/> |Содержит элементы, определяющие одного уровня и его свойства для страницы.  <br/> |
   
### <a name="child-elements"></a>Дочерние элементы

|**Элемент**|**Тип**|**Описание**|
|:-----|:-----|:-----|
|[Cell](cell-element-layer-sectionvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Указывает одно свойство для слоя или его свойства для страницы.  <br/> |
   
### <a name="attributes"></a>Атрибуты

|**Атрибут**|**Тип**|**Обязательное**|**Описание**|**Возможные значения**|
|:-----|:-----|:-----|:-----|:-----|
|DEL  <br/> |XSD:Boolean  <br/> |необязательный  <br/> |Указывает, был ли удален строку, в противном случае будут унаследованы от образца фигуры.  <br/> |Значения типа xsd:boolean.  <br/> |
|IX  <br/> |XSD:unsignedInt  <br/> |необязательный  <br/> |Указывает идентификатор на основе одной строки. Оно должно быть unqiue и больше, чем другие идентификаторы в одном разделе. Атрибут IX используется только для разделов символ, подключения, поле, FillGradient, геометрии, уровень, LineGradient, абзаца, редактор, нуля и вкладок. Строка может иметь только один из атрибутов IX или N.  <br/> |Значения типа xsd:unsignedInt.  <br/> |
|LocalName  <br/> |XSD:String  <br/> |необязательный  <br/> |Указывает уникальное имя зависит от языка строки.  <br/> |Значения типа xsd:string.  <br/> |
|N  <br/> |XSD:String  <br/> |необязательный  <br/> |Указывает уникальное имя зависящего от языка строки. Атрибут N используется только для пользователя, свойство, действия, элемент управления, подключения, гиперссылки и ActionTag разделы. Строка может иметь только один из атрибутов IX или N.  <br/> |Значения типа xsd:string.  <br/> |
|T  <br/> |XSD:String  <br/> |необязательный  <br/> |Указывает тип геометрического пути представленного строкой и используется в геометрии визуализации. Атрибут T используется только для раздел геометрии.  <br/> |Значения типа xsd:string.  <br/> |
   

