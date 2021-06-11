---
title: Элемент section (Sheet_Type ComplexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 2e7e5dcc-f667-a08c-caa0-4b81e3126ef9
description: Указывает коллекцию связанных свойств.
ms.openlocfilehash: 2862d2ccf10d235996c2a6fb26691d498bdfdbcf
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/29/2019
ms.locfileid: "34539035"
---
# <a name="section-element-sheet_type-complextype-visio-xml"></a>Элемент section (Sheet_Type ComplexType) (Visio XML)

Указывает коллекцию связанных свойств.
  
## <a name="element-information"></a>Сведения об элементе

|||
|:-----|:-----|
|**Тип элемента** <br/> |[Section_Type](section_type-complextypevisio-xml.md) <br/> |
|**Пространство имен** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Файл схемы** <br/> |VisioSchema15.xsd  <br/> |
|**Части документов** <br/> |document.xml, masters.xml, master#.xml, pages.xml, page#.xml  <br/> |
   
## <a name="definition"></a>Определение

```XML
< xs:element name="Section" type="Section_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a>Элементы и атрибуты

Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений. 
  
### <a name="parent-elements"></a>Родительские элементы

|**Элемент**|**Тип**|**Описание**|
|:-----|:-----|:-----|
|[DocumentSheet](documentsheet-element-visiodocument_type-complextypevisio-xml.md) <br/> |[DocumentSheet_Type](documentsheet_type-complextypevisio-xml.md) <br/> |Указывает свойства рисунка.  <br/> |
|[PageSheet](pagesheet-element-page_type-complextypevisio-xml.md) <br/> |[PageSheet_Type](pagesheet_type-complextypevisio-xml.md) <br/> |Указывает свойства страницы в рисунке.  <br/> |
|[PageSheet](pagesheet-element-master_type-complextypevisio-xml.md) <br/> |[Master_Type complexType](master_type-complextypevisio-xml.md) <br/> |Указывает свойства страницы рисования, связанные с мастером.  <br/> |
|[Shape](shape-element-shapes_type-complextypevisio-xml.md) <br/> |[ShapeSheet_Type](shapesheet_type-complextypevisio-xml.md) <br/> |Указывает коллекцию свойств, связанных с фигурой.  <br/> |
|[Sheet](shape-element-shapes_type-complextypevisio-xml.md) <br/> |[Sheet_Type](sheet_type-complextypevisio-xml.md) <br/> |Указывает коллекцию свойств, связанных со стилем, рисованием, страницей рисования или формой.  <br/> |
|[StyleSheet](stylesheet-element-stylesheets_type-complextypevisio-xml.md) <br/> |[StyleSheet_Type](stylesheet_type-complextypevisio-xml.md) <br/> |Указывает лист стилей.  <br/> |
   
### <a name="child-elements"></a>Дочерние элементы

|**Элемент**|**Тип**|**Описание**|
|:-----|:-----|:-----|
|[Cell](cell-elementvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Указывает одно свойство.  <br/> |
|[Row](https://msdn.microsoft.com/library/c978e3eb-b895-8fb7-e2ba-88c50e57b3db%28Office.15%29.aspx) <br/> |[Row_Type](row_type-complextypevisio-xml.md) <br/> |Указывает коллекцию **Cell_Type** элементов.  <br/> |
   
### <a name="attributes"></a>Атрибуты

|**Атрибут**|**Тип**|**Обязательный**|**Описание**|**Возможные значения**|
|:-----|:-----|:-----|:-----|:-----|
|Del  <br/> |xsd:boolean  <br/> |необязательный  <br/> |Указывает, была ли удалена коллекция, которая в противном случае была бы унаследована. Она должна быть равно 0 или 1. Значение 1 указывает, что коллекция неиспользована и должна быть проигнорирована. Значение 0 указывает, что коллекция свойств действительна для фигуры. Если атрибут **Del** не присутствует, значение 0.  <br/> |Значения типа xsd:boolean.  <br/> |
|IX  <br/> |xsd:unsignedInt  <br/> |необязательный  <br/> |Указывает нулевой индекс элемента. Он должен быть уникальным среди  всех Section_Type элементов с тем же **атрибутом N** содержащего Sheet_Type **.** Он должен быть больше атрибута **IX**  любого предыдущего элемента Section_Type с тем же атрибутом **N** содержащего Sheet_Type **.**  <br/> |Значения типа xsd:unsignedInt.  <br/> |
|Нет  <br/> |xsd:string  <br/> |Обязательный  <br/> |Указывает независимое от языка имя коллекции свойств. Он должен быть уникальным среди  всех Section_Type элементов  содержащего Sheet_Type, если он не равен "Геометрия". Она должна быть равна подзаголовок в **разделах**.  <br/> |Значения типа xsd:string.  <br/> |
   
### <a name="remarks"></a>Примечания

Атрибут **N** этого элемента **Раздела** должен быть одним из ограниченного набора значений, соответствующих ячейкам **ShapeSheet.** Обратитесь к таблице ниже, чтобы определить значения атрибута **N,** разрешенные для этого **элемента Раздела.** 
  
|**Значение**|**Описание**|**Дополнительные сведения**|
|:-----|:-----|:-----|
|Actions  <br/> |Коллекция свойств, используемых для оценки формулы. Он должен иметь **ShapeSheet_Type** или **PageSheet_Type** родительский элемент.  <br/> |[Actions Section](actions-section.md) <br/> |
|ActionTag  <br/> |Коллекция свойств, используемых только для оценки формул. Он должен иметь **ShapeSheet_Type** или **PageSheet_Type** родительский элемент.  <br/> |[Action Tag Section](action-tag-section.md) <br/> |
|Подключения  <br/> |Коллекция свойств, используемых только для оценки формул. Он должен иметь **ShapeSheet_Type** родительский элемент.  <br/> ||
|Элементы управления  <br/> |Коллекция свойств, используемых только для оценки формул. Он должен иметь **ShapeSheet_Type** родительский элемент.  <br/> |[Controls Section](controls-section.md) <br/> |
|Hyperlink  <br/> |Коллекция связанных свойств, которые указывают гиперссылки формы. Он должен иметь **ShapeSheet_Type** родительский элемент.  <br/> |[Hyperlinks Section](hyperlinks-section.md) <br/> |
|ShapeData  <br/> |Коллекция связанных свойств с указанием данных фигуры. Он должен иметь **ShapeSheet_Type** родительский элемент.  <br/> |[Shape Data Section](shape-data-section.md) <br/> |
|Пользователь.  <br/> |Коллекция свойств, используемых для оценки формулы. Он должен иметь **DocumentSheet_Type,** **PageSheet_Type** или **ShapeSheet_Type** родительского элемента.  <br/> |[User-defined Cells Section](user-defined-cells-section.md) <br/> |
   
Атрибут **IX** этого элемента **Раздела** должен быть одним из ограниченного набора значений, соответствующих ячейкам **ShapeSheet.** Обратитесь к таблице ниже, чтобы определить значения атрибута **IX,** разрешенные для этого **элемента Раздела.** 
  
|**Значение**|**Описание**|**Дополнительные сведения**|
|:-----|:-----|:-----|
|Annotation  <br/> |Коллекция свойств, содержащих сведения о комментариях, вставленных на страницу документа.  <br/> |[Annotation Section](annotation-section.md) <br/> |
|Знак  <br/> |Коллекция связанных свойств, которые указывают свойства символов текста фигуры. Он должен иметь **родительский ShapeSheet_Type** или **StyleSheet_Type** родительский элемент.  <br/> |[Character Section](character-section.md) <br/> |
|Подключения  <br/> |Коллекция свойств, используемых только для оценки формул. Он должен иметь **ShapeSheet_Type** родительский элемент.  <br/> |[Connection Points Section](connection-points-section.md) <br/> |
|Поле  <br/> |Коллекция связанных свойств с указанием текстовых полей фигуры. Он должен иметь **ShapeSheet_Type** родительский элемент.  <br/> |[Text Fields Section](text-fields-section.md) <br/> |
|FillGradient  <br/> |Коллекция свойств с указанием градиента цвета заполнения фигуры. Он должен иметь **ShapeSheet_Type** **или StyleSheet_Type** родительский элемент.  <br/> |[Fill Gradient Section](fill-gradient-section.md) <br/> |
|Геометрия  <br/> |Коллекция связанных свойств, которые указывают визуализацию геометрии. Он должен иметь **ShapeSheet_Type** родительский элемент. Первый элемент **Row_Type** этого элемента должен быть типа MoveTo, RelMoveTo, Ellipse или InfiniteLine.  <br/> |[Geometry Section](geometry-section.md) <br/> |
|Слои  <br/> |Коллекция свойств, которые показывают все уровни, определенные на странице рисования. Он должен быть ребенком элемента **PageSheet_Type.**  <br/> |[Layers Section](layers-section.md) <br/> |
|Градиентная линия  <br/> |Коллекция связанных свойств с указанием градиента цвета строки формы. Он должен иметь **ShapeSheet_Type** **или StyleSheet_Type** родительский элемент.  <br/> |[Line Gradient Section](line-gradient-section.md) <br/> |
|Paragraph  <br/> |Коллекция связанных свойств, которые указывают свойства абзаца текста фигуры. Он должен иметь **родительский ShapeSheet_Type** или **StyleSheet_Type** родительский элемент.  <br/> |[Paragraph Section](paragraph-section.md) <br/> |
|Reviewer  <br/> |Коллекция свойств, используемых для оценки формулы. Он должен иметь **DocumentSheet_Type** родительский элемент.  <br/> |[Reviewer Section](reviewer-section.md) <br/> |
|Scratch  <br/> |Коллекция свойств, используемых для оценки формулы. Он должен иметь **DocumentSheet_Type,** **PageSheet_Type** или **ShapeSheet_Type** родительского элемента.  <br/> |[Scratch Section](scratch-section.md) <br/> |
|Вкладки  <br/> |Коллекция связанных свойств, которые указывают свойства вкладок текста фигуры. Он должен иметь **родительский ShapeSheet_Type** или **StyleSheet_Type** родительский элемент.  <br/> |[Tabs Section](tabs-section.md) <br/> |
   

