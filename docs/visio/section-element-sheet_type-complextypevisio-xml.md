---
title: Элемент Section (Sheet_Type complexType) (XML для Visio)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 2e7e5dcc-f667-a08c-caa0-4b81e3126ef9
description: Задает коллекцию связанных свойств.
ms.openlocfilehash: 2862d2ccf10d235996c2a6fb26691d498bdfdbcf
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/29/2019
ms.locfileid: "34539035"
---
# <a name="section-element-sheet_type-complextype-visio-xml"></a>Элемент Section (Sheet_Type complexType) (XML для Visio)

Задает коллекцию связанных свойств.
  
## <a name="element-information"></a>Сведения об элементе

|||
|:-----|:-----|
|**Тип элемента** <br/> |[Section_Type](section_type-complextypevisio-xml.md) <br/> |
|**Пространство имен** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Файл схемы** <br/> |VisioSchema15. xsd  <br/> |
|**Части документа** <br/> |Document. XML, Master. XML, Master #. XML, Pages. XML, Page #. XML  <br/> |
   
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
|[DocumentSheet](documentsheet-element-visiodocument_type-complextypevisio-xml.md) <br/> |[DocumentSheet_Type](documentsheet_type-complextypevisio-xml.md) <br/> |Задает свойства рисунка.  <br/> |
|[PageSheet](pagesheet-element-page_type-complextypevisio-xml.md) <br/> |[PageSheet_Type](pagesheet_type-complextypevisio-xml.md) <br/> |Задает свойства страницы в документе.  <br/> |
|[PageSheet](pagesheet-element-master_type-complextypevisio-xml.md) <br/> |[Master_Type complexType](master_type-complextypevisio-xml.md) <br/> |Задает свойства страницы документа, связанной с образцом.  <br/> |
|[Shape](shape-element-shapes_type-complextypevisio-xml.md) <br/> |[ShapeSheet_Type](shapesheet_type-complextypevisio-xml.md) <br/> |Задает коллекцию свойств, связанных с фигурой.  <br/> |
|[Sheet](shape-element-shapes_type-complextypevisio-xml.md) <br/> |[Sheet_Type](sheet_type-complextypevisio-xml.md) <br/> |Задает коллекцию свойств, связанных со стилем, изображением, страницей документа или фигурой.  <br/> |
|[Применение](stylesheet-element-stylesheets_type-complextypevisio-xml.md) <br/> |[StyleSheet_Type](stylesheet_type-complextypevisio-xml.md) <br/> |Указывает таблицу стилей.  <br/> |
   
### <a name="child-elements"></a>Дочерние элементы

|**Элемент**|**Тип**|**Описание**|
|:-----|:-----|:-----|
|[Cell](cell-elementvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Задает одно свойство.  <br/> |
|[Row](https://msdn.microsoft.com/library/c978e3eb-b895-8fb7-e2ba-88c50e57b3db%28Office.15%29.aspx) <br/> |[Row_Type](row_type-complextypevisio-xml.md) <br/> |Задает коллекцию элементов **Cell_Type** .  <br/> |
   
### <a name="attributes"></a>Атрибуты

|**Атрибут**|**Тип**|**Обязательный**|**Описание**|**Возможные значения**|
|:-----|:-----|:-----|:-----|:-----|
|Del  <br/> |XSD: Boolean  <br/> |необязательный  <br/> |Указывает, удалена ли коллекция, которая в ином случае была бы унаследованной. Он должен быть равен 0 или 1. Значение 1 указывает, что коллекция не используется и должна игнорироваться. Значение 0 указывает, что коллекция свойств является допустимой для фигуры. Если атрибут **Del** отсутствует, значение равно 0.  <br/> |Значения типа XSD: Boolean.  <br/> |
|IX  <br/> |XSD: Унсигнединт  <br/> |необязательный  <br/> |Задает отсчитываемый от нуля индекс элемента. Он должен быть уникальным среди всех элементов **Section_Type** с одинаковым атрибутом **N** содержащего **Sheet_Type**. Он должен быть больше, чем атрибут **IX** любого предыдущего элемента **Section_Type** с тем же атрибутом **N** содержащего **Sheet_Type**.  <br/> |Значения типа XSD: Унсигнединт.  <br/> |
|N  <br/> |XSD: строка  <br/> |Обязательный  <br/> |Указывает имя коллекции свойств, не зависящее от языка. Он должен быть уникальным среди всех элементов **Section_Type** содержащего элемента **Sheet_Type** , если он не равен "Geometry". Он должен совпадать с подзаголовоком в **разделах**.  <br/> |Значения типа String: XSD.  <br/> |
   
### <a name="remarks"></a>Примечания

Атрибут **N** этого элемента **section** должен быть одним из ограниченных наборов значений, соответствующих ячейкам **таблицы свойств фигуры** . Используйте приведенную ниже таблицу, чтобы определить значения атрибута **N** , разрешенные для этого элемента **section** . 
  
|**Значение**|**Описание**|**Дополнительные сведения**|
|:-----|:-----|:-----|
|Действия  <br/> |Коллекция свойств, которые используются для оценки формул. Он должен иметь **ShapeSheet_Type** или **PageSheet_Type** родительский элемент.  <br/> |[Actions Section](actions-section.md) <br/> |
|актионтаг  <br/> |Коллекция свойств, которые используются только для оценки формул. Он должен иметь **ShapeSheet_Type** или **PageSheet_Type** родительский элемент.  <br/> |[Action Tag Section](action-tag-section.md) <br/> |
|Connections  <br/> |Коллекция свойств, которые используются только для оценки формул. Он должен иметь **ShapeSheet_Type** родительский элемент.  <br/> ||
|Элементы управления  <br/> |Коллекция свойств, которые используются только для оценки формул. Он должен иметь **ShapeSheet_Type** родительский элемент.  <br/> |[Controls Section](controls-section.md) <br/> |
|Hyperlink  <br/> |Коллекция связанных свойств, указывающих гиперссылки на фигуры. Он должен иметь **ShapeSheet_Type** родительский элемент.  <br/> |[Hyperlinks Section](hyperlinks-section.md) <br/> |
|шапедата  <br/> |Коллекция связанных свойств, которые задают данные фигуры. Он должен иметь **ShapeSheet_Type** родительский элемент.  <br/> |[Shape Data Section](shape-data-section.md) <br/> |
|User  <br/> |Коллекция свойств, которые используются для оценки формул. Он должен иметь **DocumentSheet_Type**, **PageSheet_Type**или **ShapeSheet_Type** родительский элемент.  <br/> |[User-defined Cells Section](user-defined-cells-section.md) <br/> |
   
Атрибут **IX** этого элемента **section** должен быть одним из ограниченных наборов значений, соответствующих ячейкам **таблицы свойств фигуры** . Используйте приведенную ниже таблицу, чтобы определить значения атрибута **IX** , разрешенные для этого элемента **section** . 
  
|**Значение**|**Описание**|**Дополнительные сведения**|
|:-----|:-----|:-----|
|Метка  <br/> |Коллекция свойств, которые содержат сведения о комментариях, вставленных в страницу документа.  <br/> |[Annotation Section](annotation-section.md) <br/> |
|Знак  <br/> |Коллекция связанных свойств, которые задают свойства символов текста фигуры. Он должен иметь **ShapeSheet_Type** родительский элемент или **StyleSheet_Type** родительский элемент.  <br/> |[Character Section](character-section.md) <br/> |
|Connections  <br/> |Коллекция свойств, которые используются только для оценки формул. Он должен иметь **ShapeSheet_Type** родительский элемент.  <br/> |[Connection Points Section](connection-points-section.md) <br/> |
|Поле  <br/> |Коллекция связанных свойств, которые задают текстовые поля фигуры. Он должен иметь **ShapeSheet_Type** родительский элемент.  <br/> |[Text Fields Section](text-fields-section.md) <br/> |
|филлградиент  <br/> |Коллекция свойств, которые задают градиентный цвет заливки фигуры. Он должен иметь **ShapeSheet_Type** или **StyleSheet_Type** родительский элемент.  <br/> |[Fill Gradient Section](fill-gradient-section.md) <br/> |
|Геометрия  <br/> |Коллекция связанных свойств, указывающих визуализацию геометрии. Он должен иметь **ShapeSheet_Type** родительский элемент. Первый дочерний элемент **Row_Type** этого элемента должен иметь тип moveTo, строка relmoveto, эллипс или строка infiniteline.  <br/> |[Geometry Section](geometry-section.md) <br/> |
|Слои  <br/> |Коллекция свойств, которые отображают все слои, определенные на странице документа. Он должен быть дочерним элементом элемента **PageSheet_Type** .  <br/> |[Layers Section](layers-section.md) <br/> |
|Градиентная линия  <br/> |Коллекция связанных свойств, указывающих градиентную цвет линии фигуры. Он должен иметь **ShapeSheet_Type** или **StyleSheet_Type** родительский элемент.  <br/> |[Line Gradient Section](line-gradient-section.md) <br/> |
|Абзац  <br/> |Коллекция связанных свойств, которые задают свойства абзаца текста фигуры. Он должен иметь **ShapeSheet_Type** родительский элемент или **StyleSheet_Type** родительский элемент.  <br/> |[Paragraph Section](paragraph-section.md) <br/> |
|Reviewer  <br/> |Коллекция свойств, которые используются для оценки формул. Он должен иметь **DocumentSheet_Type** родительский элемент.  <br/> |[Reviewer Section](reviewer-section.md) <br/> |
|Непосредственно  <br/> |Коллекция свойств, которые используются для оценки формул. Он должен иметь **DocumentSheet_Type**, **PageSheet_Type**или **ShapeSheet_Type** родительский элемент.  <br/> |[Scratch Section](scratch-section.md) <br/> |
|Вкладки  <br/> |Коллекция связанных свойств, которые задают свойства вкладок текста фигуры. Он должен иметь **ShapeSheet_Type** родительский элемент или **StyleSheet_Type** родительский элемент.  <br/> |[Tabs Section](tabs-section.md) <br/> |
   

