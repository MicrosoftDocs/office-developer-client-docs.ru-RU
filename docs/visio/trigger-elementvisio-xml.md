---
title: Элемент триггера (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: d897d2d1-25ba-48d7-b87e-d3c533d88c15
description: Предоставляет инструкции корпорации Майкрософт Visio для пересчета связи между частями документов в Visio файле.
ms.openlocfilehash: e757331984586dc910ada7d14e6385761f15929f
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/29/2019
ms.locfileid: "34542907"
---
# <a name="trigger-element-visio-xml"></a>Элемент триггера (Visio XML)

Предоставляет инструкции корпорации Майкрософт Visio для пересчета связи между частями документов в Visio файле.
  
## <a name="element-information"></a>Сведения об элементе

|||
|:-----|:-----|
|**Тип элемента** <br/> |[Trigger_Type](trigger_type-complextypevisio-xml.md) <br/> |
|**Пространство имен** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Файл схемы** <br/> |VisioSchema15.xsd  <br/> |
|**Части документов** <br/> |master#.xml, page#.xml  <br/> |
   
## <a name="definition"></a>Определение

```XML
<xs:element name="Trigger" type="Trigger_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element>
```

## <a name="elements-and-attributes"></a>Элементы и атрибуты

Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений. 
  
### <a name="parent-elements"></a>Родительские элементы

|**Элемент**|**Тип**|**Описание**|
|:-----|:-----|:-----|
|[Shape](shape-element-shapes_type-complextypevisio-xml.md) <br/> |[ShapeSheet_Type](shapesheet_type-complextypevisio-xml.md) <br/> |Указывает элементы ячейки, которые предоставляют сведения для определения фигуры.  <br/> |
|[DocumentSheet](documentsheet-element-visiodocument_type-complextypevisio-xml.md) <br/> |[DocumentSheet_Type](documentsheet_type-complextypevisio-xml.md) <br/> |Определяет структуру DocumentSheet.  <br/> |
|[StyleSheet](stylesheet-element-stylesheets_type-complextypevisio-xml.md) <br/> |[StyleSheet_Type](stylesheets_type-complextypevisio-xml.md) <br/> |Представляет стиль, определенный в документе.  <br/> |
|[PageSheet (Master_Type complexType)](pagesheet-element-master_type-complextypevisio-xml.md) <br/> |[PageSheet_Type](pagesheet_type-complextypevisio-xml.md) <br/> |Указывает свойства страницы рисования, связанные с мастером.  <br/> |
|[PageSheet (Page_Type complexType)](pagesheet-element-page_type-complextypevisio-xml.md) <br/> |[PageSheet_Type](pagesheet_type-complextypevisio-xml.md) <br/> |Указывает свойства страницы рисования, связанные со страницей рисования.  <br/> |
   
### <a name="child-elements"></a>Дочерние элементы

|**Элемент**|**Тип**|**Описание**|
|:-----|:-----|:-----|
|[RefBy](refby-element-trigger_type-complextypevisio-xml.md) <br/> |[RefBy_Type](refby_type-complextypevisio-xml.md) <br/> |Указывает ссылку на страницу "Аа" в рисунке.  <br/> |
   
### <a name="attributes"></a>Атрибуты

|**Атрибут**|**Тип**|**Обязательный**|**Описание**|**Возможные значения**|
|:-----|:-----|:-----|:-----|:-----|
|Нет  <br/> |xsd:string  <br/> |Обязательный  <br/> |Имя формулы, которая будет вызываться при активации триггера.  <br/> См. раздел Замечания.  <br/> |Значения типа xsd:string.  <br/> |
   
## <a name="remarks"></a>Примечания

Атрибут **N** этого элемента **Trigger** должен быть одним из ограниченного набора значений, соответствующих инструкциям по запуску. Обратитесь к таблице ниже, чтобы определить значения атрибута **N,** разрешенные для этого элемента **Триггера.** 
  
|**Значение**|**Родительский элемент**|**Описание**|
|:-----|:-----|:-----|
|CategoryChanged  <br/> |[PageSheet (Page_Type complexType)](pagesheet-element-page_type-complextypevisio-xml.md) <br/> |Триггер, который появляется на фигуре, когда существует перекрестная ссылка с помощью **функции HASCATEGORIES.**  <br/> |
|RecalcBkgPageName  <br/> |[PageSheet (Page_Type complexType)](pagesheet-element-page_type-complextypevisio-xml.md) <br/> |Триггер, который появляется на странице при использовании функции **BKGPAGENAME**  <br/> |
|RecalcColor  <br/> |[PageSheet (Page_Type complexType)](pagesheet-element-page_type-complextypevisio-xml.md) <br/> |Триггер, который появляется на странице всякий раз, когда страница или любая из ее содержащихся фигур использует **функцию RGB.**  <br/> |
|RecalcCreateDT  <br/> |[DocumentSheet](documentsheet-element-visiodocument_type-complextypevisio-xml.md) <br/> |Триггер, который появляется на документе, когда существует перекрестная ссылка с помощью **функции DOCCREATION.**  <br/> |
|RecalcData1  <br/> |[Shape](shape-element-shapes_type-complextypevisio-xml.md) <br/> |Спусковой крючок, который появляется на фигуре, когда существует перекрестная ссылка с помощью **функции DATA1.**  <br/> |
|RecalcData2  <br/> |[Shape](shape-element-shapes_type-complextypevisio-xml.md) <br/> |Триггер, который появляется на фигуре при использовании функции **DATA2.**  <br/> |
|RecalcData3  <br/> |[Shape](shape-element-shapes_type-complextypevisio-xml.md) <br/> |Триггер, который появляется на фигуре, когда существует перекрестная ссылка с помощью **функции DATA3.**  <br/> |
|RecalcEditDT  <br/> |[DocumentSheet](documentsheet-element-visiodocument_type-complextypevisio-xml.md) <br/> |Триггер, который появляется на документе, когда существует перекрестная ссылка с помощью **функции DOCLASTEDIT.**  <br/> |
|RecalcID  <br/> |[Shape](shape-element-shapes_type-complextypevisio-xml.md) <br/> |Спусковой крючок, который появляется на фигуре, когда существует перекрестная ссылка с помощью **функции ID.**  <br/> |
|RecalcMasterName  <br/> |[Shape](shape-element-shapes_type-complextypevisio-xml.md) <br/> |Триггер, который появляется на фигуре при использовании функции **MASTERNAME.**  <br/> |
|RecalcName  <br/> |[Shape](shape-element-shapes_type-complextypevisio-xml.md) <br/> |Триггер, который появляется на фигуре, когда существует перекрестная ссылка с помощью **функции NAME.**  <br/> |
|RecalcNowAndRand  <br/> |[PageSheet (Page_Type complexType)](pagesheet-element-page_type-complextypevisio-xml.md) <br/> |Триггер, который отображается на странице, если страница или любая из ее содержащих фигур имеют функцию **NOW** или **RAND.**  <br/> |
|RecalcPageCount  <br/> |[DocumentSheet](documentsheet-element-visiodocument_type-complextypevisio-xml.md) <br/> |Триггер, который появляется на документе, когда существует перекрестная ссылка с помощью **функции PAGECOUNT.**  <br/> |
|RecalcPageName  <br/> |[PageSheet (Page_Type complexType)](pagesheet-element-page_type-complextypevisio-xml.md) <br/> [Shape](shape-element-shapes_type-complextypevisio-xml.md) <br/> |Триггер, который появляется на фигуре при использовании функции **PAGENAME.**  <br/> |
|RecalcPageNum  <br/> |[PageSheet (Page_Type complexType)](pagesheet-element-page_type-complextypevisio-xml.md) <br/> |Триггер, который появляется на странице, когда существует перекрестная ссылка с помощью **функции PAGENUMBER.**  <br/> |
|RecalcPath  <br/> |[DocumentSheet](documentsheet-element-visiodocument_type-complextypevisio-xml.md) <br/> |Триггер, который появляется на фигуре, когда существует перекрестная ссылка с помощью **POINTALONGPATH,** **PATHLENGTH** или **PATHSEGMENT.**  <br/> |
|RecalcPrintDT  <br/> |[DocumentSheet](documentsheet-element-visiodocument_type-complextypevisio-xml.md) <br/> |Триггер, который появляется на документе, когда существует перекрестная ссылка с помощью **функции DOCLASTPRINT.**  <br/> |
|RecalcSaveDT  <br/> |[DocumentSheet](documentsheet-element-visiodocument_type-complextypevisio-xml.md) <br/> |Триггер, который появляется на документе, когда существует перекрестная ссылка с помощью **функции DOCLASTSAVE.**  <br/> |
|RecalcSummary  <br/> |[DocumentSheet](documentsheet-element-visiodocument_type-complextypevisio-xml.md) <br/> |Триггер, который появляется на документе, когда существует перекрестная ссылка с помощью **функции CATEGORY**, **CREATOR**, **DESCRIPTION**, **KEYWORDS,** **SUBJECT** или **TITLE.**  <br/> |
|RecalcType  <br/> |[Shape](shape-element-shapes_type-complextypevisio-xml.md) <br/> |Триггер, который появляется на фигуре, когда существует перекрестная ссылка с помощью **функции TYPE.**  <br/> |
|RelChanged  <br/> |[Shape](shape-element-shapes_type-complextypevisio-xml.md) <br/> |Триггер, который появляется на фигуре, когда существует перекрестная ссылка с помощью **функции CONTAINERMEMBERCOUNT.**  <br/> |
|ZOrderChanged  <br/> |[PageSheet (Page_Type complexType)](pagesheet-element-page_type-complextypevisio-xml.md) <br/> |Триггер, который появляется на странице при использовании функции **CONTAINERSHEETREF.**  <br/> |
|Path  <br/> |[Shape](shape-element-shapes_type-complextypevisio-xml.md) <br/> |Триггер, который появляется на странице, когда существует перекрестная ссылка с помощью **POINTALONGPATH,** **PATHLENGTH** или **PATHSEGMENT.**  <br/> |
   

