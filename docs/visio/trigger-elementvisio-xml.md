---
title: Элемент Trigger ('Visio XML»)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: d897d2d1-25ba-48d7-b87e-d3c533d88c15
description: Инструкции для Microsoft Visio для пересчета отношение между частями документа в файл Visio.
ms.openlocfilehash: 909fff3ccec176cd3ce327fc208c176a68764fe3
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19815075"
---
# <a name="trigger-element-visio-xml"></a>Элемент Trigger ('Visio XML»)

Инструкции для Microsoft Visio для пересчета отношение между частями документа в файл Visio.
  
## <a name="element-information"></a>Сведения об элементе

|||
|:-----|:-----|
|**Тип элемента** <br/> |[Trigger_Type](trigger_type-complextypevisio-xml.md) <br/> |
|**Пространство имен** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Файл схемы** <br/> |VisioSchema15.xsd  <br/> |
|**Части документа** <br/> |главные # .xml, страницы # .xml  <br/> |
   
## <a name="definition"></a>Определение

```XML
<xs:element name="Trigger" type="Trigger_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element>
```

## <a name="elements-and-attributes"></a>Элементы и атрибуты

Если схема определяет специальные требования, такие как **последовательность**, **minOccurs**, **maxOccurs**и **выбора**, обратитесь к разделу определение. 
  
### <a name="parent-elements"></a>Родительские элементы

|**Элемент**|**Тип**|**Описание**|
|:-----|:-----|:-----|
|[Фигура](shape-element-shapes_type-complextypevisio-xml.md) <br/> |[ShapeSheet_Type](shapesheet_type-complextypevisio-xml.md) <br/> |Определяет элементы ячеек, которые содержат сведения для определения фигуры.  <br/> |
|[DocumentSheet](documentsheet-element-visiodocument_type-complextypevisio-xml.md) <br/> |[DocumentSheet_Type](documentsheet_type-complextypevisio-xml.md) <br/> |Определяет структуру DocumentSheet.  <br/> |
|[Таблица стилей](stylesheet-element-stylesheets_type-complextypevisio-xml.md) <br/> |[StyleSheet_Type](stylesheets_type-complextypevisio-xml.md) <br/> |Представляет стиль, определенный в документе.  <br/> |
|[PageSheet (Master_Type complexType)](pagesheet-element-master_type-complextypevisio-xml.md) <br/> |[PageSheet_Type](pagesheet_type-complextypevisio-xml.md) <br/> |Задает свойства страницы рисунка, связанного с шаблоном.  <br/> |
|[PageSheet (Page_Type complexType)](pagesheet-element-page_type-complextypevisio-xml.md) <br/> |[PageSheet_Type](pagesheet_type-complextypevisio-xml.md) <br/> |Задает свойства страницы рисунка, связанного с странице документа.  <br/> |
   
### <a name="child-elements"></a>Дочерние элементы

|**Элемент**|**Тип**|**Описание**|
|:-----|:-----|:-----|
|[RefBy](refby-element-trigger_type-complextypevisio-xml.md) <br/> |[RefBy_Type](refby_type-complextypevisio-xml.md) <br/> |Указывает страницу ссылку таблицы ссылок в документе.  <br/> |
   
### <a name="attributes"></a>Атрибуты

|**Атрибут**|**Тип**|**Обязательное**|**Описание**|**Возможные значения**|
|:-----|:-----|:-----|:-----|:-----|
|N  <br/> |XSD:String  <br/> |Обязательный  <br/> |Имя формулы, которая вызывается при активации триггера.  <br/> В разделе Примечания.  <br/> |Значения типа xsd:string.  <br/> |
   
## <a name="remarks"></a>Замечания

Атрибут **N** этого элемента **триггер** должен быть один из ограниченный набор значений, которые соответствуют триггер инструкции. Обратитесь к таблице ниже для определения значений атрибутов **N** , разрешенных для этого элемента **триггер** . 
  
|**Значение**|**Родительский элемент**|**Описание**|
|:-----|:-----|:-----|
|CategoryChanged  <br/> |[PageSheet (Page_Type complexType)](pagesheet-element-page_type-complextypevisio-xml.md) <br/> |Триггер, который отображается на фигуры, когда есть ссылка кросс часть, с помощью функции **HASCATEGORIES** .  <br/> |
|RecalcBkgPageName  <br/> |[PageSheet (Page_Type complexType)](pagesheet-element-page_type-complextypevisio-xml.md) <br/> |Триггер, который отображается на странице, когда есть ссылка кросс часть, с помощью функции **BKGPAGENAME**  <br/> |
|RecalcColor  <br/> |[PageSheet (Page_Type complexType)](pagesheet-element-page_type-complextypevisio-xml.md) <br/> |Триггер, который отображается на странице каждый раз, когда странице или к любому его автономные фигур используется функция **RGB** .  <br/> |
|RecalcCreateDT  <br/> |[DocumentSheet](documentsheet-element-visiodocument_type-complextypevisio-xml.md) <br/> |Триггер, который отображается в документе, когда есть ссылка кросс часть, с помощью функции **DOCCREATION** .  <br/> |
|RecalcData1  <br/> |[Фигура](shape-element-shapes_type-complextypevisio-xml.md) <br/> |Триггер, который отображается на фигуры, когда есть ссылка кросс часть, с помощью функции **бд1** .  <br/> |
|RecalcData2  <br/> |[Фигура](shape-element-shapes_type-complextypevisio-xml.md) <br/> |Триггер, который отображается на фигуры, когда есть ссылка кросс часть, с помощью функции **бд2** .  <br/> |
|RecalcData3  <br/> |[Фигура](shape-element-shapes_type-complextypevisio-xml.md) <br/> |Триггер, который отображается на фигуры, когда есть ссылка кросс часть, с помощью функции **DATA3** .  <br/> |
|RecalcEditDT  <br/> |[DocumentSheet](documentsheet-element-visiodocument_type-complextypevisio-xml.md) <br/> |Триггер, который отображается в документе, когда есть ссылка кросс часть, с помощью функции **DOCLASTEDIT** .  <br/> |
|RecalcID  <br/> |[Фигура](shape-element-shapes_type-complextypevisio-xml.md) <br/> |Триггер, который отображается на фигуры, когда есть ссылка кросс часть, с помощью функции **идентификатор** .  <br/> |
|RecalcMasterName  <br/> |[Фигура](shape-element-shapes_type-complextypevisio-xml.md) <br/> |Триггер, который отображается на фигуры, когда есть ссылка кросс часть, с помощью функции **ИМЯОБРАЗЦА** .  <br/> |
|RecalcName  <br/> |[Фигура](shape-element-shapes_type-complextypevisio-xml.md) <br/> |Триггер, который отображается на фигуры, когда есть ссылка кросс части с помощью **ИМЕНИ** функции.  <br/> |
|RecalcNowAndRand  <br/> |[PageSheet (Page_Type complexType)](pagesheet-element-page_type-complextypevisio-xml.md) <br/> |Триггер, который отображается на странице, если страницу или какие-либо его содержащего фигур **ТЕПЕРЬ** или функция **РЭНД** .  <br/> |
|RecalcPageCount  <br/> |[DocumentSheet](documentsheet-element-visiodocument_type-complextypevisio-xml.md) <br/> |Триггер, который отображается в документе, когда есть ссылка кросс часть, с помощью функции **PAGECOUNT** .  <br/> |
|RecalcPageName  <br/> |[PageSheet (Page_Type complexType)](pagesheet-element-page_type-complextypevisio-xml.md) <br/> [Фигура](shape-element-shapes_type-complextypevisio-xml.md) <br/> |Триггер, который отображается на фигуры, когда есть ссылка кросс часть, с помощью функции **ИМЯ_СТРАНИЦЫ** .  <br/> |
|RecalcPageNum  <br/> |[PageSheet (Page_Type complexType)](pagesheet-element-page_type-complextypevisio-xml.md) <br/> |Триггер, который отображается на странице, когда есть ссылка кросс часть, с помощью функции **PAGENUMBER** .  <br/> |
|RecalcPath  <br/> |[DocumentSheet](documentsheet-element-visiodocument_type-complextypevisio-xml.md) <br/> |Триггер, который отображается на фигуры при получении нескольких частей ссылки, с помощью функции **POINTALONGPATH**, **PATHLENGTH**или **PATHSEGMENT** существует.  <br/> |
|RecalcPrintDT  <br/> |[DocumentSheet](documentsheet-element-visiodocument_type-complextypevisio-xml.md) <br/> |Триггер, который отображается в документе, когда есть ссылка кросс часть, с помощью функции **DOCLASTPRINT** .  <br/> |
|RecalcSaveDT  <br/> |[DocumentSheet](documentsheet-element-visiodocument_type-complextypevisio-xml.md) <br/> |Триггер, который отображается в документе, когда есть ссылка кросс часть, с помощью функции **DOCLASTSAVE** .  <br/> |
|RecalcSummary  <br/> |[DocumentSheet](documentsheet-element-visiodocument_type-complextypevisio-xml.md) <br/> |Существует триггер, который отображается в документе, когда ссылка кросс части с помощью функции **категории**, **СОЗДАТЕЛЯ**, **Описание**, **ключевые слова**, **Тема**или **заголовок** .  <br/> |
|RecalcType  <br/> |[Фигура](shape-element-shapes_type-complextypevisio-xml.md) <br/> |Триггер, который отображается на фигуры, когда есть ссылка кросс часть, с помощью функции **ТИПА** .  <br/> |
|RelChanged  <br/> |[Фигура](shape-element-shapes_type-complextypevisio-xml.md) <br/> |Триггер, который отображается на фигуры, когда есть ссылка кросс часть, с помощью функции **CONTAINERMEMBERCOUNT** .  <br/> |
|ZOrderChanged  <br/> |[PageSheet (Page_Type complexType)](pagesheet-element-page_type-complextypevisio-xml.md) <br/> |Триггер, который отображается на странице, когда есть ссылка кросс часть, с помощью функции **CONTAINERSHEETREF** .  <br/> |
|Path  <br/> |[Фигура](shape-element-shapes_type-complextypevisio-xml.md) <br/> |Триггер, который отображается на странице при получении нескольких частей ссылки, с помощью функции **POINTALONGPATH**, **PATHLENGTH**или **PATHSEGMENT** существует.  <br/> |
   

