---
title: Элемент Section (Sheet_Type complexType) (Visio XML)
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
# <a name="section-element-sheet_type-complextype-visio-xml"></a>Элемент Section (Sheet_Type complexType) (Visio XML)

Указывает коллекцию связанных свойств.
  
## <a name="element-information"></a>Сведения об элементе

|||
|:-----|:-----|
|**Тип элемента** <br/> |[Section_Type](section_type-complextypevisio-xml.md) <br/> |
|**Пространство имен** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Файл схемы** <br/> |VisioSchema15.xsd  <br/> |
|**Части документа** <br/> |document.xml, masters.xml, master#.xml, pages.xml, page#.xml  <br/> |
   
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
|[PageSheet](pagesheet-element-page_type-complextypevisio-xml.md) <br/> |[PageSheet_Type](pagesheet_type-complextypevisio-xml.md) <br/> |Указывает свойства страницы в документе.  <br/> |
|[PageSheet](pagesheet-element-master_type-complextypevisio-xml.md) <br/> |[Master_Type complexType](master_type-complextypevisio-xml.md) <br/> |Указывает свойства страницы рисования, связанной с хозяином.  <br/> |
|[Shape](shape-element-shapes_type-complextypevisio-xml.md) <br/> |[ShapeSheet_Type](shapesheet_type-complextypevisio-xml.md) <br/> |Указывает коллекцию свойств, связанных с фигурой.  <br/> |
|[Sheet](shape-element-shapes_type-complextypevisio-xml.md) <br/> |[Sheet_Type](sheet_type-complextypevisio-xml.md) <br/> |Указывает коллекцию свойств, связанных со стилем, рисунком, страницей рисования или фигурой.  <br/> |
|[StyleSheet](stylesheet-element-stylesheets_type-complextypevisio-xml.md) <br/> |[StyleSheet_Type](stylesheet_type-complextypevisio-xml.md) <br/> |Указывает таблицу стилей.  <br/> |
   
### <a name="child-elements"></a>Дочерние элементы

|**Элемент**|**Тип**|**Описание**|
|:-----|:-----|:-----|
|[Cell](cell-elementvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Указывает одно свойство.  <br/> |
|[Row](https://msdn.microsoft.com/library/c978e3eb-b895-8fb7-e2ba-88c50e57b3db%28Office.15%29.aspx) <br/> |[Row_Type](row_type-complextypevisio-xml.md) <br/> |Указывает коллекцию **Cell_Type** элементов.  <br/> |
   
### <a name="attributes"></a>Атрибуты

|**Атрибут**|**Тип**|**Обязательный**|**Описание**|**Возможные значения**|
|:-----|:-----|:-----|:-----|:-----|
|Del  <br/> |xsd:boolean  <br/> |необязательный  <br/> |Указывает, была ли удалена коллекция, которая в противном случае была бы унаследована. Должно быть равно 0 или 1. Значение 1 указывает, что коллекция неиспользована и ДОЛЖНА игнорироваться. Значение 0 указывает, что коллекция свойств действительна для фигуры. Если атрибут **Del** не существует, значение будет 0.  <br/> |Значения типа xsd:boolean.  <br/> |
|IX  <br/> |xsd:unsignedInt  <br/> |необязательный  <br/> |Указывает индекс элемента с нуля. Он ДОЛЖЕН быть уникальным среди  всех Section_Type элементов с одинаковым **атрибутом N** содержащего **Sheet_Type.** Он ДОЛЖЕН быть больше атрибута **IX**  любого предыдущего Section_Type с  тем же N-атрибутом содержащего **Sheet_Type.**  <br/> |Значения типа xsd:unsignedInt.  <br/> |
|N  <br/> |xsd:string  <br/> |Обязательный  <br/> |Указывает независимое от языка имя коллекции свойств. Он ДОЛЖЕН быть уникальным среди  всех Section_Type элементов,  содержащих Sheet_Type, если он не равен "Geometry". Он ДОЛЖЕН быть равен подзаголовку в **разделах.**  <br/> |Значения типа xsd:string.  <br/> |
   
### <a name="remarks"></a>Примечания

Атрибут **N** этого **элемента Section** должен быть одним из ограниченных наборов значений, соответствующих ячейкам **ShapeSheet.** Чтобы определить значения атрибута **N,** допустимого для этого элемента **Section,** обратитесь к приведенной ниже таблице. 
  
|**Значение**|**Описание**|**Дополнительные сведения**|
|:-----|:-----|:-----|
|Действия  <br/> |Коллекция свойств, используемых для оценки формулы. Он ДОЛЖЕН иметь **ShapeSheet_Type** или **PageSheet_Type** родительского элемента.  <br/> |[Actions Section](actions-section.md) <br/> |
|ActionTag  <br/> |Коллекция свойств, которые используются только для оценки формулы. Он ДОЛЖЕН иметь **ShapeSheet_Type** или **PageSheet_Type** родительского элемента.  <br/> |[Action Tag Section](action-tag-section.md) <br/> |
|Connections  <br/> |Коллекция свойств, которые используются только для оценки формулы. Он ДОЛЖЕН иметь **ShapeSheet_Type** родительского элемента.  <br/> ||
|Элементы управления  <br/> |Коллекция свойств, которые используются только для оценки формулы. Он ДОЛЖЕН иметь **ShapeSheet_Type** родительского элемента.  <br/> |[Controls Section](controls-section.md) <br/> |
|Hyperlink  <br/> |Коллекция связанных свойств, которые указывают гиперссылки фигуры. Он ДОЛЖЕН иметь **ShapeSheet_Type** родительского элемента.  <br/> |[Hyperlinks Section](hyperlinks-section.md) <br/> |
|ShapeData  <br/> |Коллекция связанных свойств, которые указывают данные фигуры. Он ДОЛЖЕН иметь **ShapeSheet_Type** родительского элемента.  <br/> |[Shape Data Section](shape-data-section.md) <br/> |
|Пользователь  <br/> |Коллекция свойств, используемых для оценки формулы. Он ДОЛЖЕН иметь **DocumentSheet_Type,** **PageSheet_Type** или **ShapeSheet_Type** родительского элемента.  <br/> |[User-defined Cells Section](user-defined-cells-section.md) <br/> |
   
Атрибут **IX** этого **элемента Section** должен быть одним из ограниченных наборов значений, соответствующих ячейкам **ShapeSheet.** Чтобы определить значения атрибута **IX,** допустимого для этого элемента **Section,** обратитесь к приведенной ниже таблице. 
  
|**Значение**|**Описание**|**Дополнительные сведения**|
|:-----|:-----|:-----|
|Annotation  <br/> |Коллекция свойств, содержащих сведения о комментариях, вставленных на страницу документа.  <br/> |[Annotation Section](annotation-section.md) <br/> |
|Знак  <br/> |Коллекция связанных свойств, которые указывают свойства символов текста фигуры. Он ДОЛЖЕН иметь **ShapeSheet_Type** или **StyleSheet_Type** родительского элемента.  <br/> |[Character Section](character-section.md) <br/> |
|Connections  <br/> |Коллекция свойств, которые используются только для оценки формулы. Он ДОЛЖЕН иметь **ShapeSheet_Type** родительского элемента.  <br/> |[Connection Points Section](connection-points-section.md) <br/> |
|Поле  <br/> |Коллекция связанных свойств, которые указывают текстовые поля фигуры. Он ДОЛЖЕН иметь **ShapeSheet_Type** родительского элемента.  <br/> |[Text Fields Section](text-fields-section.md) <br/> |
|FillGradient  <br/> |Коллекция свойств, которые определяют градиент цвета заливки фигуры. Он ДОЛЖЕН иметь **ShapeSheet_Type** или **StyleSheet_Type** родительского элемента.  <br/> |[Fill Gradient Section](fill-gradient-section.md) <br/> |
|Геометрия  <br/> |Коллекция связанных свойств, которые определяют визуализацию геометрии. Он ДОЛЖЕН иметь **ShapeSheet_Type** родительского элемента. Первый **Row_Type** этого элемента ДОЛЖЕН иметь тип MoveTo, RelMoveTo, Ellipse или InfiniteLine.  <br/> |[Geometry Section](geometry-section.md) <br/> |
|Слои  <br/> |Коллекция свойств, которые показывают все уровни, определенные на странице рисования. Он ДОЛЖЕН быть PageSheet_Type **элемента.**  <br/> |[Layers Section](layers-section.md) <br/> |
|Градиентная линия  <br/> |Коллекция связанных свойств, которые определяют градиент цвета линии фигуры. Он ДОЛЖЕН иметь **ShapeSheet_Type** или **StyleSheet_Type** родительского элемента.  <br/> |[Line Gradient Section](line-gradient-section.md) <br/> |
|Абзац  <br/> |Коллекция связанных свойств, которые указывают свойства абзаца текста фигуры. Он ДОЛЖЕН иметь **ShapeSheet_Type** или **StyleSheet_Type** родительского элемента.  <br/> |[Paragraph Section](paragraph-section.md) <br/> |
|Reviewer  <br/> |Коллекция свойств, используемых для оценки формулы. Он ДОЛЖЕН иметь **DocumentSheet_Type** родительского элемента.  <br/> |[Reviewer Section](reviewer-section.md) <br/> |
|Scratch  <br/> |Коллекция свойств, используемых для оценки формулы. Он ДОЛЖЕН иметь **DocumentSheet_Type,** **PageSheet_Type** или **ShapeSheet_Type** родительского элемента.  <br/> |[Scratch Section](scratch-section.md) <br/> |
|Вкладки  <br/> |Коллекция связанных свойств, которые определяют свойства вкладок текста фигуры. Он ДОЛЖЕН иметь **ShapeSheet_Type** или **StyleSheet_Type** родительского элемента.  <br/> |[Tabs Section](tabs-section.md) <br/> |
   

