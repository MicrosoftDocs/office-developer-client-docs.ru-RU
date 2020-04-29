---
title: Элемент Trigger (XML в Visio)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: d897d2d1-25ba-48d7-b87e-d3c533d88c15
description: В этой статье приведены инструкции по пересчету связей между частями документа в файле Visio в Microsoft Visio.
ms.openlocfilehash: e757331984586dc910ada7d14e6385761f15929f
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/29/2019
ms.locfileid: "34542907"
---
# <a name="trigger-element-visio-xml"></a>Элемент Trigger (XML в Visio)

В этой статье приведены инструкции по пересчету связей между частями документа в файле Visio в Microsoft Visio.
  
## <a name="element-information"></a>Сведения об элементе

|||
|:-----|:-----|
|**Тип элемента** <br/> |[Trigger_Type](trigger_type-complextypevisio-xml.md) <br/> |
|**Пространство имен** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Файл схемы** <br/> |VisioSchema15. xsd  <br/> |
|**Части документа** <br/> |Master #. XML, Page #. XML  <br/> |
   
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
|[Shape](shape-element-shapes_type-complextypevisio-xml.md) <br/> |[ShapeSheet_Type](shapesheet_type-complextypevisio-xml.md) <br/> |Задает элементы Cell, которые предоставляют сведения для определения фигуры.  <br/> |
|[DocumentSheet](documentsheet-element-visiodocument_type-complextypevisio-xml.md) <br/> |[DocumentSheet_Type](documentsheet_type-complextypevisio-xml.md) <br/> |Определяет структуру DocumentSheet.  <br/> |
|[Применение](stylesheet-element-stylesheets_type-complextypevisio-xml.md) <br/> |[StyleSheet_Type](stylesheets_type-complextypevisio-xml.md) <br/> |Представляет стиль, определенный в документе.  <br/> |
|[PageSheet (Master_Type complexType)](pagesheet-element-master_type-complextypevisio-xml.md) <br/> |[PageSheet_Type](pagesheet_type-complextypevisio-xml.md) <br/> |Задает свойства страницы документа, связанной с образцом.  <br/> |
|[PageSheet (Page_Type complexType)](pagesheet-element-page_type-complextypevisio-xml.md) <br/> |[PageSheet_Type](pagesheet_type-complextypevisio-xml.md) <br/> |Задает свойства страницы документа, связанной со страницей документа.  <br/> |
   
### <a name="child-elements"></a>Дочерние элементы

|**Элемент**|**Тип**|**Описание**|
|:-----|:-----|:-----|
|[RefBy](refby-element-trigger_type-complextypevisio-xml.md) <br/> |[RefBy_Type](refby_type-complextypevisio-xml.md) <br/> |Указывает ссылку на страницу таблицы ссылок в документе.  <br/> |
   
### <a name="attributes"></a>Атрибуты

|**Атрибут**|**Тип**|**Обязательный**|**Описание**|**Возможные значения**|
|:-----|:-----|:-----|:-----|:-----|
|N  <br/> |XSD: строка  <br/> |Обязательный  <br/> |Имя формулы, вызываемой при активации триггера.  <br/> Ознакомьтесь с разделом "Примечания".  <br/> |Значения типа String: XSD.  <br/> |
   
## <a name="remarks"></a>Примечания

Атрибут **N** этого элемента **Trigger** должен быть одним из ограниченных наборов значений, соответствующих инструкциям триггера. Используйте приведенную ниже таблицу, чтобы определить значения атрибута **N** , разрешенные для этого элемента **Trigger** . 
  
|**Значение**|**Родительский элемент**|**Описание**|
|:-----|:-----|:-----|
|категоричанжед  <br/> |[PageSheet (Page_Type complexType)](pagesheet-element-page_type-complextypevisio-xml.md) <br/> |Триггер, который отображается на фигуре при наличии ссылки на несколько частей с помощью функции **хаскатегориес** .  <br/> |
|рекалкбкгпаженаме  <br/> |[PageSheet (Page_Type complexType)](pagesheet-element-page_type-complextypevisio-xml.md) <br/> |Триггер, который отображается на странице при наличии ссылки между частями с помощью функции **BKGPAGENAME**  <br/> |
|рекалкколор  <br/> |[PageSheet (Page_Type complexType)](pagesheet-element-page_type-complextypevisio-xml.md) <br/> |Триггер, который отображается на странице, когда страница или любая из содержащихся в ней фигур используют функцию **RGB** .  <br/> |
|рекалккреатедт  <br/> |[DocumentSheet](documentsheet-element-visiodocument_type-complextypevisio-xml.md) <br/> |Триггер, который отображается в документе при наличии ссылки между частями с помощью функции **DOCCREATION** .  <br/> |
|RecalcData1  <br/> |[Shape](shape-element-shapes_type-complextypevisio-xml.md) <br/> |Триггер, который отображается на фигуре при наличии ссылки на несколько частей с помощью функции **файл1** .  <br/> |
|RecalcData2  <br/> |[Shape](shape-element-shapes_type-complextypevisio-xml.md) <br/> |Триггер, который отображается на фигуре при наличии ссылки на несколько частей с помощью функции **файл2** .  <br/> |
|RecalcData3  <br/> |[Shape](shape-element-shapes_type-complextypevisio-xml.md) <br/> |Триггер, который отображается на фигуре при наличии ссылки на несколько частей с помощью функции **DATA3** .  <br/> |
|рекалцедитдт  <br/> |[DocumentSheet](documentsheet-element-visiodocument_type-complextypevisio-xml.md) <br/> |Триггер, который отображается в документе при наличии ссылки между частями с помощью функции **DOCLASTEDIT** .  <br/> |
|рекалЦид  <br/> |[Shape](shape-element-shapes_type-complextypevisio-xml.md) <br/> |Триггер, который отображается на фигуре при наличии ссылки на несколько частей с помощью функции **ID** .  <br/> |
|рекалкмастернаме  <br/> |[Shape](shape-element-shapes_type-complextypevisio-xml.md) <br/> |Триггер, который отображается на фигуре при наличии ссылки на несколько частей с помощью функции **MASTERNAME** .  <br/> |
|рекалкнаме  <br/> |[Shape](shape-element-shapes_type-complextypevisio-xml.md) <br/> |Триггер, который отображается на фигуре при наличии ссылки на несколько частей с помощью функции **Name** .  <br/> |
|рекалкновандранд  <br/> |[PageSheet (Page_Type complexType)](pagesheet-element-page_type-complextypevisio-xml.md) <br/> |Триггер, который отображается на **странице, если** либо страница, либо содержащаяся в ней фигуре, имеют функцию Rand или функция **Rand** .  <br/> |
|рекалкпажекаунт  <br/> |[DocumentSheet](documentsheet-element-visiodocument_type-complextypevisio-xml.md) <br/> |Триггер, который отображается в документе при наличии ссылки между частями с помощью функции **PAGECOUNT** .  <br/> |
|рекалкпаженаме  <br/> |[PageSheet (Page_Type complexType)](pagesheet-element-page_type-complextypevisio-xml.md) <br/> [Shape](shape-element-shapes_type-complextypevisio-xml.md) <br/> |Триггер, который отображается на фигуре при наличии ссылки на несколько частей с помощью функции **PAGENAME** .  <br/> |
|рекалкпаженум  <br/> |[PageSheet (Page_Type complexType)](pagesheet-element-page_type-complextypevisio-xml.md) <br/> |Триггер, который отображается на странице при наличии ссылки между частями с помощью функции **PAGENUMBER** .  <br/> |
|рекалкпас  <br/> |[DocumentSheet](documentsheet-element-visiodocument_type-complextypevisio-xml.md) <br/> |Триггер, который отображается на фигуре при наличии ссылки на несколько частей с помощью функции **POINTALONGPATH**, **PATHLENGTH**или **PATHSEGMENT** .  <br/> |
|рекалкпринтдт  <br/> |[DocumentSheet](documentsheet-element-visiodocument_type-complextypevisio-xml.md) <br/> |Триггер, который отображается в документе при наличии ссылки между частями с помощью функции **DOCLASTPRINT** .  <br/> |
|рекалксаведт  <br/> |[DocumentSheet](documentsheet-element-visiodocument_type-complextypevisio-xml.md) <br/> |Триггер, который отображается в документе при наличии ссылки между частями с помощью функции **DOCLASTSAVE** .  <br/> |
|рекалксуммари  <br/> |[DocumentSheet](documentsheet-element-visiodocument_type-complextypevisio-xml.md) <br/> |Триггер, который отображается в документе при наличии ссылки на несколько частей с использованием **категории**, **создателя**, **описания**, **ключевых слов**, **темы**или названия функции **Title** .  <br/> |
|рекалктипе  <br/> |[Shape](shape-element-shapes_type-complextypevisio-xml.md) <br/> |Триггер, который отображается на фигуре при наличии ссылки на несколько частей с помощью функции **Type** .  <br/> |
|релчанжед  <br/> |[Shape](shape-element-shapes_type-complextypevisio-xml.md) <br/> |Триггер, который отображается на фигуре при наличии ссылки на несколько частей с помощью функции **CONTAINERMEMBERCOUNT** .  <br/> |
|зордерчанжед  <br/> |[PageSheet (Page_Type complexType)](pagesheet-element-page_type-complextypevisio-xml.md) <br/> |Триггер, который отображается на странице при наличии ссылки между частями с помощью функции **CONTAINERSHEETREF** .  <br/> |
|Путь  <br/> |[Shape](shape-element-shapes_type-complextypevisio-xml.md) <br/> |Триггер, который отображается на странице при наличии ссылки на несколько частей с помощью функции **POINTALONGPATH**, **PATHLENGTH**или **PATHSEGMENT** .  <br/> |
   

