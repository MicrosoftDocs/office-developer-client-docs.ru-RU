---
title: Элемент Cell (Строка гиперссылки) (XML-элемент Visio)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: d2089db4-39eb-06d3-d2f8-9465baef5c75
description: Содержит сведения для одной гиперссылки, связанной с фигурой. Фигура будет содержать одну строку гиперссылки для каждой гиперссылки.
ms.openlocfilehash: f9526b3e4bb7dc9216a0b72c0a816e136c6e89bf
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/29/2019
ms.locfileid: "34539795"
---
# <a name="cell-element-hyperlink-row-visio-xml"></a>Элемент Cell (Строка гиперссылки) (XML-элемент Visio)

Содержит сведения для одной гиперссылки, связанной с фигурой. Фигура будет содержать одну **строку гиперссылки** для каждой гиперссылки. 
  
## <a name="element-information"></a>Сведения об элементе

|||
|:-----|:-----|
|**Тип элемента** <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |
|**Пространство имен** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Файл схемы** <br/> |VisioSchema15.xsd  <br/> |
|**Части документа** <br/> |master#.xml, page#.xml  <br/> |
   
## <a name="definition"></a>Определение

```XML
< xs:element name="Cell" type="Cell_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a>Элементы и атрибуты

Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений. 
  
### <a name="parent-elements"></a>Родительские элементы

|**Элемент**|**Тип**|**Описание**|
|:-----|:-----|:-----|
|[Элемент Row (Hyperlink Section)](row-element-hyperlink-sectionvisio-xml.md) <br/> |[HyperlinkRow_Type](hyperlinkrow_type-complextypevisio-xml.md) <br/> |Содержит сведения для одной гиперссылки, связанной с фигурой. Фигура будет содержать одну **строку гиперссылки** для каждой гиперссылки.  <br/> |
   
### <a name="child-elements"></a>Дочерние элементы

|**Элемент**|**Тип**|**Описание**|
|:-----|:-----|:-----|
|[RefBy](refby-element-cell_type-complextypevisio-xml.md) <br/> |[RefBy_Type](refby_type-complextypevisio-xml.md) <br/> |Указывает ссылку на страницу рисования.  <br/> |
   
### <a name="attributes"></a>Атрибуты

|**Атрибут**|**Тип**|**Обязательный**|**Описание**|**Возможные значения**|
|:-----|:-----|:-----|:-----|:-----|
|E  <br/> |xsd:string  <br/> |необязательный  <br/> |Указывает, что формула оценивается как ошибка. Значение E **—** текущее значение (строка сообщения об ошибке); Значение атрибута **V** является последним допустимым значением.  <br/> |Строка сообщения об ошибке.  <br/> |
|F  <br/> |xsd:string  <br/> |необязательный  <br/> | Представляет формулу элемента. Этот атрибут может содержать одну из следующих строк:  <br/>  '(some formula)', если формула существует локально  <br/>  `No Formula` если формула удалена или заблокирована локально  <br/>  `Inh` если формула унаследована.  <br/> |Формула.  <br/> |
|N  <br/> |xsd:string  <br/> |Обязательный  <br/> |Представляет имя ячейки ShapeSheet.  <br/> |Имя ячейки ShapeSheet.  <br/> См. раздел "Замечания" ниже.  <br/> |
|U  <br/> |xsd:string  <br/> |необязательный  <br/> |Представляет единицу измерения, значение по умолчанию — DL.  <br/> |Единицы ячейки.  <br/> |
|V  <br/> |xsd:string  <br/> |необязательный  <br/> |Представляет значение ячейки.  <br/> |Значение ячейки ShapeSheet.  <br/> |
   
## <a name="remarks"></a>Примечания

Атрибут **N** этого элемента **Cell** должен быть одним из ограниченного набора значений, соответствующих ячейкам ShapeSheet. Чтобы определить значения атрибута **N,** допустимого для этого элемента Cell, обратитесь к таблице **ниже.** 
  
|**Значение**|**Описание**|**Дополнительные сведения**|
|:-----|:-----|:-----|
|Address  <br/> |Указывает URL-адрес, имя файла или UNC-путь, к которому необходимо перейти.  <br/> |[Address Cell (Hyperlinks Section)](address-cell-hyperlinks-section.md) <br/> |
|По умолчанию  <br/> |Определяет гиперссылки по умолчанию для фигуры или страницы.  <br/> |[Default Cell (Hyperlinks Section)](default-cell-hyperlinks-section.md) <br/> |
|Описание  <br/> |Представляет текстовую строку для гиперссылки.  <br/> |[Description Cell (Hyperlinks Section)](description-cell-hyperlinks-section.md) <br/> |
|ExtraInfo  <br/> |Представляет строку, которая передает сведения, используемые при разрешении URL-адреса, например координаты карты изображения.  <br/> |[ExtraInfo Cell (Hyperlinks Section)](extrainfo-cell-hyperlinks-section.md) <br/> |
|Frame  <br/> |Представляет имя кадра для цели, когда приложение открыто в качестве активного документа в приложении-контейнере. Значение по умолчанию — пустая строка.  <br/> |[Frame Cell (Hyperlinks Section)](frame-cell-hyperlinks-section.md) <br/> |
|Invisible  <br/> |Указывает, отображается ли гиперссылка в ярлыке для фигуры или страницы.  <br/> |[Invisible Cell (Hyperlinks Section)](invisible-cell-hyperlinks-section.md) <br/> |
|NewWindow  <br/> |Указывает, следует ли открывать гиперссылки в новом окне.  <br/> |[NewWindow Cell (Hyperlinks Section)](newwindow-cell-hyperlinks-section.md) <br/> |
|SortKey  <br/> |Число, которое определяет порядок гиперссылки, которые отображаются в ярлыке меню.  <br/> |[SortKey Cell (Hyperlinks Section)](sortkey-cell-hyperlinks-section.md) <br/> |
|SubAddress  <br/> |Указывает расположение в целевом документе, к который необходимо связать.  <br/> |[SubAddress Cell (Hyperlinks Section)](subaddress-cell-hyperlinks-section.md) <br/> |
   

