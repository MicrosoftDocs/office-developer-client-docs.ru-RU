---
title: Элемент раздела (Sheet_Type complexType) ('Visio XML»)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 2e7e5dcc-f667-a08c-caa0-4b81e3126ef9
description: Задает коллекцию свойств, связанных с ними.
ms.openlocfilehash: 7cb5e1c30960e69b252abc7af38e021607fd3502
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19814742"
---
# <a name="section-element-sheettype-complextype-visio-xml"></a>Элемент раздела (Sheet_Type complexType) ('Visio XML»)

Задает коллекцию свойств, связанных с ними.
  
## <a name="element-information"></a>Сведения об элементе

|||
|:-----|:-----|
|**Тип элемента** <br/> |[Section_Type](section_type-complextypevisio-xml.md) <br/> |
|**Пространство имен** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Файл схемы** <br/> |VisioSchema15.xsd  <br/> |
|**Части документа** <br/> |Document.XML, masters.xml, главные # .xml, pages.xml, страницы # .xml  <br/> |
   
## <a name="definition"></a>Определение

```XML
< xs:element name="Section" type="Section_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a>Элементы и атрибуты

Если схема определяет специальные требования, такие как **последовательность**, **minOccurs**, **maxOccurs**и **выбора**, обратитесь к разделу определение. 
  
### <a name="parent-elements"></a>Родительские элементы

|**Элемент**|**Тип**|**Описание**|
|:-----|:-----|:-----|
|[DocumentSheet](documentsheet-element-visiodocument_type-complextypevisio-xml.md) <br/> |[DocumentSheet_Type](documentsheet_type-complextypevisio-xml.md) <br/> |Задает свойства документа.  <br/> |
|[PageSheet](pagesheet-element-page_type-complextypevisio-xml.md) <br/> |[PageSheet_Type](pagesheet_type-complextypevisio-xml.md) <br/> |Задает свойства страницы в документе.  <br/> |
|[PageSheet](pagesheet-element-master_type-complextypevisio-xml.md) <br/> |[Master_Type complexType](master_type-complextypevisio-xml.md) <br/> |Задает свойства страницы рисунка, связанного с шаблоном.  <br/> |
|[Фигура](shape-element-shapes_type-complextypevisio-xml.md) <br/> |[ShapeSheet_Type](shapesheet_type-complextypevisio-xml.md) <br/> |Задает набор свойств, связанных с фигурой.  <br/> |
|[Лист](shape-element-shapes_type-complextypevisio-xml.md) <br/> |[Sheet_Type](sheet_type-complextypevisio-xml.md) <br/> |Задает набор свойств, связанных с стиль, документа, размеры страницы или фигуры.  <br/> |
|[Таблица стилей](stylesheet-element-stylesheets_type-complextypevisio-xml.md) <br/> |[StyleSheet_Type](stylesheet_type-complextypevisio-xml.md) <br/> |Задает таблицу стилей.  <br/> |
   
### <a name="child-elements"></a>Дочерние элементы

|**Элемент**|**Тип**|**Описание**|
|:-----|:-----|:-----|
|[Cell](http://msdn.microsoft.com/library/70a9d6d6-a4ff-2b0d-febc-789a04a2f5b0%28Office.15%29.aspx) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Задает отдельное свойство.  <br/> |
|[Row](http://msdn.microsoft.com/library/c978e3eb-b895-8fb7-e2ba-88c50e57b3db%28Office.15%29.aspx) <br/> |[Row_Type](row_type-complextypevisio-xml.md) <br/> |Задает коллекцию элементов **Cell_Type** .  <br/> |
   
### <a name="attributes"></a>Атрибуты

|**Атрибут**|**Тип**|**Обязательное**|**Описание**|**Возможные значения**|
|:-----|:-----|:-----|:-----|:-----|
|DEL  <br/> |XSD:Boolean  <br/> |необязательный  <br/> |Указывает, ли удалять коллекции, в противном случае будут унаследованы. Оно должно быть равно 0 или 1. Значение 1 указывает, что коллекция не используется и не следует учитывать. Значение 0 указывает, что набор свойств, является допустимым для фигуры. Если атрибут **Del** не указан, значение равно 0.  <br/> |Значения типа xsd:boolean.  <br/> |
|IX  <br/> |XSD:unsignedInt  <br/> |необязательный  <br/> |Указывает, начинающийся с нуля индекс элемента. Он должен быть уникальным для всех элементов **Section_Type** с тем же атрибутом **N** содержащего **Sheet_Type**. ДОЛЖНО быть больше, чем атрибут **IX** любой предыдущий элемент **Section_Type** с тем же атрибутом **N** содержащего **Sheet_Type**.  <br/> |Значения типа xsd:unsignedInt.  <br/> |
|N  <br/> |XSD:String  <br/> |Обязательный  <br/> |Задает имя зависящего от языка набор свойств. Он должен быть уникальным для всех элементов **Section_Type** **Sheet_Type** элемент-контейнер, если оно не равно «Геометрия». Он должен быть равен подзаголовка в **разделах**.  <br/> |Значения типа xsd:string.  <br/> |
   
### <a name="remarks"></a>Замечания

Атрибут **N** элемента в этом **разделе** должен быть один из ограниченный набор значений, которые соответствуют ячейки **таблицы свойств фигуры** . Обратитесь к таблице ниже для определения значений атрибутов **N** , разрешенных для элемента в этом **разделе** . 
  
|**Значение**|**Описание**|**Дополнительные сведения**|
|:-----|:-----|:-----|
|Действия  <br/> |Набор свойств, которые используются для вычисления. Она должна иметь **ShapeSheet_Type** или **PageSheet_Type** родительского элемента.  <br/> |[Раздел "Действия"](actions-section.md) <br/> |
|ActionTag  <br/> |Набор свойств, которые используются для вычисления только. Она должна иметь **ShapeSheet_Type** или **PageSheet_Type** родительского элемента.  <br/> |[Раздел "Теги действий"](action-tag-section.md) <br/> |
|Подключения  <br/> |Набор свойств, которые используются для вычисления только. Она должна иметь **ShapeSheet_Type** родительского элемента.  <br/> ||
|Элементы управления  <br/> |Набор свойств, которые используются для вычисления только. Она должна иметь **ShapeSheet_Type** родительского элемента.  <br/> |[Раздел "Элементы управления"](controls-section.md) <br/> |
|Гиперссылка  <br/> |Коллекция связанных свойств, которые задают гиперссылки фигуры. Она должна иметь **ShapeSheet_Type** родительского элемента.  <br/> |[Раздел "Гиперссылки"](hyperlinks-section.md) <br/> |
|ShapeData  <br/> |Коллекция связанных свойств, которые определяют данные фигуры. Она должна иметь **ShapeSheet_Type** родительского элемента.  <br/> |[Раздел "Данные фигуры"](shape-data-section.md) <br/> |
|Пользователь  <br/> |Набор свойств, которые используются для вычисления. Она должна иметь **DocumentSheet_Type**, **PageSheet_Type**или **ShapeSheet_Type** родительского элемента.  <br/> |[Раздел "Пользовательские ячейки"](user-defined-cells-section.md) <br/> |
   
Атрибут **IX** элемента в этом **разделе** должен быть один из ограниченный набор значений, которые соответствуют ячейки **таблицы свойств фигуры** . Обратитесь к таблице ниже для определения значений атрибутов **IX** , разрешенных для элемента в этом **разделе** . 
  
|**Значение**|**Описание**|**Дополнительные сведения**|
|:-----|:-----|:-----|
|Annotation  <br/> |Набор свойств, которые содержат сведения о комментарии, вставляется на страницу документа.  <br/> |[Раздел "Примечание"](annotation-section.md) <br/> |
|Знак  <br/> |Коллекция связанных свойств, которые задают свойства символ текста фигуры. Она должна иметь родительский элемент **ShapeSheet_Type** или **StyleSheet_Type** родительского элемента.  <br/> |[Раздел "Символ"](character-section.md) <br/> |
|Подключения  <br/> |Набор свойств, которые используются для вычисления только. Она должна иметь **ShapeSheet_Type** родительского элемента.  <br/> |[Раздел "Точки соединения"](connection-points-section.md) <br/> |
|Поле  <br/> |Коллекция связанных свойств, которые задают текстовых полей фигуры. Она должна иметь **ShapeSheet_Type** родительского элемента.  <br/> |[Раздел "Текстовые поля"](text-fields-section.md) <br/> |
|FillGradient  <br/> |Набор свойств, которые задают градиентные цвета заливки фигуры. Она должна иметь **ShapeSheet_Type** или **StyleSheet_Type** родительского элемента.  <br/> |[Раздел "Градиентная заливка"](fill-gradient-section.md) <br/> |
|Геометрия  <br/> |Коллекция связанных свойств, которые задают визуализации геометрии. Она должна иметь **ShapeSheet_Type** родительского элемента. Первый **Row_Type** дочерний элемент этого элемента должно иметь тип MoveTo, RelMoveTo, эллипс или InfiniteLine.  <br/> |[Раздел "Геометрия"](geometry-section.md) <br/> |
|Слои  <br/> |Набор свойств, которые все слои, определенные на странице документа. Это должен быть дочерний элемент **PageSheet_Type** .  <br/> |[Раздел "Слои"](layers-section.md) <br/> |
|Градиентные строки  <br/> |Коллекция связанных свойств, которые задают строки градиента фигуры. Она должна иметь **ShapeSheet_Type** или **StyleSheet_Type** родительского элемента.  <br/> |[Раздел "Градиентная линия"](line-gradient-section.md) <br/> |
|Абзац  <br/> |Коллекция связанных свойств, которые задают свойств абзаца текста фигуры. Она должна иметь родительский элемент **ShapeSheet_Type** или **StyleSheet_Type** родительского элемента.  <br/> |[Раздел "Абзац"](paragraph-section.md) <br/> |
|Редактор  <br/> |Набор свойств, которые используются для вычисления. Она должна иметь **DocumentSheet_Type** родительского элемента.  <br/> |[Раздел "Рецензент"](reviewer-section.md) <br/> |
|Нуля  <br/> |Набор свойств, которые используются для вычисления. Она должна иметь **DocumentSheet_Type**, **PageSheet_Type**или **ShapeSheet_Type** родительского элемента.  <br/> |[Раздел "Вспомогательный"](scratch-section.md) <br/> |
|Вкладки  <br/> |Коллекция связанных свойств, которые задают свойства вкладки текста фигуры. Она должна иметь родительский элемент **ShapeSheet_Type** или **StyleSheet_Type** родительского элемента.  <br/> |[Раздел "Вкладки"](tabs-section.md) <br/> |
   

