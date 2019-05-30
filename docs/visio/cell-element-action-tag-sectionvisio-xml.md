---
title: Элемент Cell (раздел "теги действий") (XML-файл Visio)
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
# <a name="cell-element-action-tag-section-visio-xml"></a>Элемент Cell (раздел "теги действий") (XML-файл Visio)

Определяет одно свойство для тега действия на фигуре или странице.
  
## <a name="element-information"></a>Сведения об элементе

|||
|:-----|:-----|
|**Тип элемента** <br/> |[Целл_типе](cell_type-complextypevisio-xml.md) <br/> |
|**Пространство имен** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Файл схемы** <br/> |VisioSchema15. xsd  <br/> |
|**Части документа** <br/> |Master. XML, Master #. XML, Pages. XML, Page #. XML  <br/> |
   
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
|[Элемент Row (раздел Актионтаг)](row-element-action-tag-sectionvisio-xml.md) <br/> |[Актионтагров_типе](actiontag_type-complextypevisio-xml.md) <br/> |Определяет тег действия на фигуре или странице.  <br/> |
   
### <a name="child-elements"></a>Дочерние элементы

|**Элемент**|**Тип**|**Описание**|
|:-----|:-----|:-----|
|[RefBy](refby-element-cell_type-complextypevisio-xml.md) <br/> |[Рефби_типе](refby_type-complextypevisio-xml.md) <br/> |Указывает ссылку на страницу документа.  <br/> |
   
### <a name="attributes"></a>Атрибуты

|**Атрибут**|**Тип**|**Обязательный**|**Описание**|**Возможные значения**|
|:-----|:-----|:-----|:-----|:-----|
|E  <br/> |XSD: строка  <br/> |необязательный  <br/> |Указывает, что формула возвращает ошибку. Значение **E** — это текущее значение (строка сообщения об ошибке); значение атрибута **V** — это Последнее допустимое значение.  <br/> |Строка сообщения об ошибке.  <br/> |
|F  <br/> |XSD: строка  <br/> |необязательный  <br/> | Представляет формулу элемента. Этот атрибут может содержать одну из следующих строк:  <br/>  ' (формула) ', если формула существует локально  <br/>  `No Formula`Если формула локально удалена или заблокирована  <br/>  `Inh`, если формула наследуется.  <br/> |Формула.  <br/> |
|N  <br/> |XSD: строка  <br/> |Обязательный  <br/> |Представляет имя ячейки таблицы свойств фигуры.  <br/> |Имя ячейки таблицы свойств фигуры.  <br/> Ознакомьтесь с разделом "Примечания" ниже.  <br/> |
|U  <br/> |XSD: строка  <br/> |необязательный  <br/> |Представляет единицу измерения. значение по умолчанию — DL.  <br/> |Единицы ячейки.  <br/> |
|V  <br/> |XSD: строка  <br/> |необязательный  <br/> |Представляет значение ячейки.  <br/> |Значение ячейки таблицы свойств фигуры.  <br/> |
   
## <a name="remarks"></a>Примечания

Атрибут **N** этого элемента **Cell** должен иметь ограниченный набор значений, соответствующих ячейкам таблицы свойств фигуры. Чтобы определить значения атрибута **N** , которые разрешено использовать для этого элемента **ячейки** , обратитесь к приведенной ниже таблице. 
  
|**Значение**|**Описание**|**Дополнительные сведения**|
|:-----|:-----|:-----|
|ButtonFace  <br/> |Содержит идентификатор изображения кнопки, которое отображается на кнопке тега действия.  <br/> |[ButtonFace Cell (Action Tags Section)](buttonface-cell-action-tags-section.md) <br/> |
|Описание  <br/> |Содержит строку, описывающую тег действия, который отображается как всплывающая подсказка, когда пользователь наводит указатель мыши на тег.  <br/> |[Description Cell (Action Tags Section)](description-cell-action-tags-section.md) <br/> |
|Отключена  <br/> |Указывает, отображается ли тег действия в окне документа.  <br/> |[Disabled Cell (Action Tags Section)](disabled-cell-action-tags-section.md) <br/> |
|DisplayMode  <br/> |Определяет, отображается ли тег action, когда пользователь наводит указатель мыши на тег, когда фигура выделена или все время.  <br/> |[DisplayMode Cell (Action Tags Section)](displaymode-cell-action-tags-section.md) <br/> |
|TagName  <br/> |Имя тега действия, используемого в качестве ключа для сопоставления тега действия с его действиями.  <br/> |[TagName Cell (Action Tags Section)](tagname-cell-action-tags-section.md) <br/> |
|X  <br/> |Положение координаты x в локальных координатах фигуры, вокруг которого размещается кнопка тега действия.  <br/> |[X Cell (Action Tags Section)](x-cell-action-tags-section.md) <br/> |
|Ксжустифи  <br/> |Смещение по оси x для кнопки тега действия относительно точки, заданной ячейками X и Y.  <br/> |[X Justify Cell (Action Tags Section)](x-justify-cell-action-tags-section.md) <br/> |
|Да  <br/> |Координата y в локальных координатах фигуры, вокруг которой размещается кнопка тега действия.  <br/> |[Y Cell (Action Tags Section)](y-cell-action-tags-section.md) <br/> |
|Ижустифи  <br/> |Смещение по оси y для кнопки тега действия относительно точки, заданной ячейками X и Y.  <br/> |[Y Justify Cell (Action Tags Section)](y-justify-cell-action-tags-section.md) <br/> |
   

