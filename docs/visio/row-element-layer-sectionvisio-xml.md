---
title: Элемент Row (раздел "слой") (XML-файл Visio)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 9b884be2-3eed-0864-6a6c-877b43d9065f
description: Содержит элементы, определяющие один слой и его свойства для страницы.
ms.openlocfilehash: edd076651838d7522af07013cda5fedd9a28de7f
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/29/2019
ms.locfileid: "34540865"
---
# <a name="row-element-layer-section-visio-xml"></a>Элемент Row (раздел "слой") (XML-файл Visio)

Содержит элементы, определяющие один слой и его свойства для страницы.
  
## <a name="element-information"></a>Сведения об элементе

|||
|:-----|:-----|
|**Тип элемента** <br/> |[LayerRow_Type](layerrow_type-complextypevisio-xml.md) <br/> |
|**Пространство имен** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Файл схемы** <br/> |VisioSchema15. xsd  <br/> |
|**Части документа** <br/> |файлы хозяев. XML, Pages. XML  <br/> |
   
## <a name="definition"></a>Определение

```XML
< xs:element name="Row" type="LayerRow_Type" >
</xs:element >
```

## <a name="elements-and-attributes"></a>Элементы и атрибуты

Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений. 
  
### <a name="parent-elements"></a>Родительские элементы

|**Элемент**|**Тип**|**Описание**|
|:-----|:-----|:-----|
|[Section](section-element-sheet_type-complextypevisio-xml.md) <br/> |[Section_Type](section_type-complextypevisio-xml.md) <br/> |Содержит элементы, определяющие один слой и его свойства для страницы.  <br/> |
   
### <a name="child-elements"></a>Дочерние элементы

|**Элемент**|**Тип**|**Описание**|
|:-----|:-----|:-----|
|[Cell](cell-element-layer-sectionvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Задает одно свойство для слоя или его свойств для страницы.  <br/> |
   
### <a name="attributes"></a>Атрибуты

|**Атрибут**|**Тип**|**Обязательный**|**Описание**|**Возможные значения**|
|:-----|:-----|:-----|:-----|:-----|
|Del  <br/> |XSD: Boolean  <br/> |необязательный  <br/> |Указывает, удалена ли строка, которая в противном случае была бы унаследована от основной фигуры.  <br/> |Значения типа XSD: Boolean.  <br/> |
|IX  <br/> |XSD: Унсигнединт  <br/> |необязательный  <br/> |Задает отсчитываемый от единицы идентификатор строки. Он должен быть уникальное и превышать другие идентификаторы в одном разделе. Атрибут IX используется только для разделов "символ", "подключение", "Филлградиент", "геометрия", "область", "Линеградиент", "Абзац", "фрагмент" и "вкладки". Строка может иметь только один из атрибутов IX или N.  <br/> |Значения типа XSD: Унсигнединт.  <br/> |
|LocalName  <br/> |XSD: строка  <br/> |необязательный  <br/> |Задает уникальное зависящее от языка имя строки.  <br/> |Значения типа String: XSD.  <br/> |
|N  <br/> |XSD: строка  <br/> |необязательный  <br/> |Задает уникальное имя строки, не зависящее от языка. Атрибут N используется только для разделов "пользователь", "свойство", "действия", "элементы управления", "гиперссылка" и "Актионтаг". Строка может иметь только один из атрибутов IX или N.  <br/> |Значения типа String: XSD.  <br/> |
|Д  <br/> |XSD: строка  <br/> |необязательный  <br/> |Указывает тип геометрического пути, представленного строкой и используемый в визуализации геометрии. Атрибут T используется только для раздела Geometry.  <br/> |Значения типа String: XSD.  <br/> |
   

