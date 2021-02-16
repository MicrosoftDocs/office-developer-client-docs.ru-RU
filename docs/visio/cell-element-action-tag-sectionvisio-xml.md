---
title: Элемент Cell (Action Tag Section) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6210ff71-fbcd-2c97-6dde-1e334891e08d
description: Определяет одно свойство для тега действия на фигуре или странице.
ms.openlocfilehash: 3b43206838dae432df677a3ff8792c85328db53b
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/29/2019
ms.locfileid: "34538804"
---
# <a name="cell-element-action-tag-section-visio-xml"></a>Элемент Cell (Action Tag Section) (Visio XML)

Определяет одно свойство для тега действия на фигуре или странице.
  
## <a name="element-information"></a>Сведения об элементе

|||
|:-----|:-----|
|**Тип элемента** <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |
|**Пространство имен** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Файл схемы** <br/> |VisioSchema15.xsd  <br/> |
|**Части документа** <br/> |masters.xml, master#.xml, pages.xml, page#.xml  <br/> |
   
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
|[Элемент Row (Раздел ActionTag)](row-element-action-tag-sectionvisio-xml.md) <br/> |[ActionTagRow_Type](actiontag_type-complextypevisio-xml.md) <br/> |Определяет тег действия на фигуре или странице.  <br/> |
   
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
|ButtonFace  <br/> |Содержит ИД изображения лица кнопки, которое отображается на кнопке тега действия.  <br/> |[ButtonFace Cell (Action Tags Section)](buttonface-cell-action-tags-section.md) <br/> |
|Описание  <br/> |Содержит строку, описываемую тегом действия, который отображается как подсказка, когда пользователь нанося указатель на тег.  <br/> |[Description Cell (Action Tags Section)](description-cell-action-tags-section.md) <br/> |
|Отключено  <br/> |Указывает, отображается ли тег действия в окне рисования.  <br/> |[Disabled Cell (Action Tags Section)](disabled-cell-action-tags-section.md) <br/> |
|DisplayMode  <br/> |Определяет, отображается ли тег действия, когда пользователь нанося указатель на тег, когда фигура выбрана, или все время.  <br/> |[DisplayMode Cell (Action Tags Section)](displaymode-cell-action-tags-section.md) <br/> |
|TagName  <br/> |Имя тега действия, который используется в качестве ключа для связываия тега действия с его действиями.  <br/> |[TagName Cell (Action Tags Section)](tagname-cell-action-tags-section.md) <br/> |
|X  <br/> |Положение x-координаты в локальных координатах фигуры, вокруг которых расположена кнопка тега действия.  <br/> |[X Cell (Action Tags Section)](x-cell-action-tags-section.md) <br/> |
|XJustify  <br/> |Смещение x кнопки тега действия относительно точки, определяемой ячейками X и Y.  <br/> |[X Justify Cell (Action Tags Section)](x-justify-cell-action-tags-section.md) <br/> |
|Да  <br/> |Положение Y в локальных координатах фигуры, вокруг которых расположена кнопка тега действия.  <br/> |[Y Cell (Action Tags Section)](y-cell-action-tags-section.md) <br/> |
|YJustify  <br/> |Смещение y кнопки тега действия относительно точки, определяемой ячейками X и Y.  <br/> |[Y Justify Cell (Action Tags Section)](y-justify-cell-action-tags-section.md) <br/> |
   

