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
|**Тип элемента** <br/> |[Тригжер_типе](trigger_type-complextypevisio-xml.md) <br/> |
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
|[Shape](shape-element-shapes_type-complextypevisio-xml.md) <br/> |[Шапешит_типе](shapesheet_type-complextypevisio-xml.md) <br/> |Задает элементы Cell, которые предоставляют сведения для определения фигуры.  <br/> |
|[DocumentSheet](documentsheet-element-visiodocument_type-complextypevisio-xml.md) <br/> |[Документшит_типе](documentsheet_type-complextypevisio-xml.md) <br/> |Определяет структуру DocumentSheet.  <br/> |
|[Применение](stylesheet-element-stylesheets_type-complextypevisio-xml.md) <br/> |[Стилешит_типе](stylesheets_type-complextypevisio-xml.md) <br/> |Представляет стиль, определенный в документе.  <br/> |
|[PageSheet (Мастер_типе complexType)](pagesheet-element-master_type-complextypevisio-xml.md) <br/> |[Пажешит_типе](pagesheet_type-complextypevisio-xml.md) <br/> |Задает свойства страницы документа, связанной с образцом.  <br/> |
|[PageSheet (Паже_типе complexType)](pagesheet-element-page_type-complextypevisio-xml.md) <br/> |[Пажешит_типе](pagesheet_type-complextypevisio-xml.md) <br/> |Задает свойства страницы документа, связанной со страницей документа.  <br/> |
   
### <a name="child-elements"></a>Дочерние элементы

|**Элемент**|**Тип**|**Описание**|
|:-----|:-----|:-----|
|[RefBy](refby-element-trigger_type-complextypevisio-xml.md) <br/> |[Рефби_типе](refby_type-complextypevisio-xml.md) <br/> |Указывает ссылку на страницу таблицы ссылок в документе.  <br/> |
   
### <a name="attributes"></a>Атрибуты

|**Атрибут**|**Тип**|**Обязательный**|**Описание**|**Возможные значения**|
|:-----|:-----|:-----|:-----|:-----|
|N  <br/> |XSD: строка  <br/> |Обязательный  <br/> |Имя формулы, вызываемой при активации триггера.  <br/> Ознакомьтесь с разделом "Примечания".  <br/> |Значения типа String: XSD.  <br/> |
   
## <a name="remarks"></a>Примечания

Атрибут **N** этого элемента **Trigger** должен быть одним из ограниченных наборов значений, соответствующих инструкциям триггера. Используйте приведенную ниже таблицу, чтобы определить значения атрибута **N** , разрешенные для этого элемента **Trigger** . 
  
|**Значение**|**Родительский элемент**|**Описание**|
|:-----|:-----|:-----|
|Категоричанжед  <br/> |[PageSheet (Паже_типе complexType)](pagesheet-element-page_type-complextypevisio-xml.md) <br/> |Триггер, который отображается на фигуре при наличии ссылки на несколько частей с помощью функции **хаскатегориес** .  <br/> |
|Рекалкбкгпаженаме  <br/> |[PageSheet (Паже_типе complexType)](pagesheet-element-page_type-complextypevisio-xml.md) <br/> |Триггер, который отображается на странице при наличии ссылки между частями с помощью функции **BKGPAGENAME**  <br/> |
|Рекалкколор  <br/> |[PageSheet (Паже_типе complexType)](pagesheet-element-page_type-complextypevisio-xml.md) <br/> |Триггер, который отображается на странице, когда страница или любая из содержащихся в ней фигур используют функцию **RGB** .  <br/> |
|Рекалккреатедт  <br/> |[DocumentSheet](documentsheet-element-visiodocument_type-complextypevisio-xml.md) <br/> |Триггер, который отображается в документе при наличии ссылки между частями с помощью функции **DOCCREATION** .  <br/> |
|RecalcData1  <br/> |[Shape](shape-element-shapes_type-complextypevisio-xml.md) <br/> |Триггер, который отображается на фигуре при наличии ссылки на несколько частей с помощью функции **файл1** .  <br/> |
|RecalcData2  <br/> |[Shape](shape-element-shapes_type-complextypevisio-xml.md) <br/> |Триггер, который отображается на фигуре при наличии ссылки на несколько частей с помощью функции **файл2** .  <br/> |
|RecalcData3  <br/> |[Shape](shape-element-shapes_type-complextypevisio-xml.md) <br/> |Триггер, который отображается на фигуре при наличии ссылки на несколько частей с помощью функции **DATA3** .  <br/> |
|Рекалцедитдт  <br/> |[DocumentSheet](documentsheet-element-visiodocument_type-complextypevisio-xml.md) <br/> |Триггер, который отображается в документе при наличии ссылки между частями с помощью функции **DOCLASTEDIT** .  <br/> |
|РекалЦид  <br/> |[Shape](shape-element-shapes_type-complextypevisio-xml.md) <br/> |Триггер, который отображается на фигуре при наличии ссылки на несколько частей с помощью функции **ID** .  <br/> |
|Рекалкмастернаме  <br/> |[Shape](shape-element-shapes_type-complextypevisio-xml.md) <br/> |Триггер, который отображается на фигуре при наличии ссылки на несколько частей с помощью функции **MASTERNAME** .  <br/> |
|Рекалкнаме  <br/> |[Shape](shape-element-shapes_type-complextypevisio-xml.md) <br/> |Триггер, который отображается на фигуре при наличии ссылки на несколько частей с помощью функции **Name** .  <br/> |
|Рекалкновандранд  <br/> |[PageSheet (Паже_типе complexType)](pagesheet-element-page_type-complextypevisio-xml.md) <br/> |Триггер, который отображается на странице, если либо страница, либо содержащаяся в ней фигуре, **** имеют функцию Rand или функция **Rand** .  <br/> |
|Рекалкпажекаунт  <br/> |[DocumentSheet](documentsheet-element-visiodocument_type-complextypevisio-xml.md) <br/> |Триггер, который отображается в документе при наличии ссылки между частями с помощью функции **PAGECOUNT** .  <br/> |
|Рекалкпаженаме  <br/> |[PageSheet (Паже_типе complexType)](pagesheet-element-page_type-complextypevisio-xml.md) <br/> [Shape](shape-element-shapes_type-complextypevisio-xml.md) <br/> |Триггер, который отображается на фигуре при наличии ссылки на несколько частей с помощью функции **PAGENAME** .  <br/> |
|Рекалкпаженум  <br/> |[PageSheet (Паже_типе complexType)](pagesheet-element-page_type-complextypevisio-xml.md) <br/> |Триггер, который отображается на странице при наличии ссылки между частями с помощью функции **PAGENUMBER** .  <br/> |
|Рекалкпас  <br/> |[DocumentSheet](documentsheet-element-visiodocument_type-complextypevisio-xml.md) <br/> |Триггер, который отображается на фигуре при наличии ссылки на несколько частей с помощью функции **POINTALONGPATH**, **PATHLENGTH**или **PATHSEGMENT** .  <br/> |
|Рекалкпринтдт  <br/> |[DocumentSheet](documentsheet-element-visiodocument_type-complextypevisio-xml.md) <br/> |Триггер, который отображается в документе при наличии ссылки между частями с помощью функции **DOCLASTPRINT** .  <br/> |
|Рекалксаведт  <br/> |[DocumentSheet](documentsheet-element-visiodocument_type-complextypevisio-xml.md) <br/> |Триггер, который отображается в документе при наличии ссылки между частями с помощью функции **DOCLASTSAVE** .  <br/> |
|Рекалксуммари  <br/> |[DocumentSheet](documentsheet-element-visiodocument_type-complextypevisio-xml.md) <br/> |Триггер, который отображается в документе при наличии ссылки на несколько частей с использованием **категории**, **создателя**, **описания**, **ключевых слов**, **темы**или названия функции **Title** .  <br/> |
|Рекалктипе  <br/> |[Shape](shape-element-shapes_type-complextypevisio-xml.md) <br/> |Триггер, который отображается на фигуре при наличии ссылки на несколько частей с помощью функции **Type** .  <br/> |
|Релчанжед  <br/> |[Shape](shape-element-shapes_type-complextypevisio-xml.md) <br/> |Триггер, который отображается на фигуре при наличии ссылки на несколько частей с помощью функции **CONTAINERMEMBERCOUNT** .  <br/> |
|Зордерчанжед  <br/> |[PageSheet (Паже_типе complexType)](pagesheet-element-page_type-complextypevisio-xml.md) <br/> |Триггер, который отображается на странице при наличии ссылки между частями с помощью функции **CONTAINERSHEETREF** .  <br/> |
|Путь  <br/> |[Shape](shape-element-shapes_type-complextypevisio-xml.md) <br/> |Триггер, который отображается на странице при наличии ссылки на несколько частей с помощью функции **POINTALONGPATH**, **PATHLENGTH**или **PATHSEGMENT** .  <br/> |
   

