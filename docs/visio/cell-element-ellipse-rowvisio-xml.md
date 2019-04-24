---
title: Элемент Cell (строка Ellipse) (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 210e6731-7c94-90b1-c7c4-635df974fdb6
description: Содержит координаты x и y центральной точки эллипса и две точки эллипса.
ms.openlocfilehash: 75c3cf86b7c8668b70915117e1fc70b07d2cef0b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32356121"
---
# <a name="cell-element-ellipse-row-visio-xml"></a>Элемент Cell (строка Ellipse) (' Visio XML ')

Содержит координаты x и y центральной точки эллипса и две точки эллипса.
  
## <a name="element-information"></a>Сведения об элементе

|||
|:-----|:-----|
|**Тип элемента** <br/> |[Целл_типе](cell_type-complextypevisio-xml.md) <br/> |
|**Пространство имен** <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Файл схемы** <br/> |VisioSchema15. xsd  <br/> |
|**Части документа** <br/> |Master #. XML, Page #. XML  <br/> |
   
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
|[Элемент Row (геометрия)](row-element-geometry-sectionvisio-xml.md) <br/> |[Еллипсе_типе](ellipse_type-complextypevisio-xml.md) <br/> |Содержит координаты x и y центральной точки эллипса и две точки эллипса.  <br/> |
   
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
  
|**Value**|**Описание**|**Дополнительные сведения**|
|:-----|:-----|:-----|
|X  <br/> |Координата x центральной точки.  <br/> |[Ellipse Row (Geometry Section)](ellipse-row-geometry-section.md) <br/> |
|Да  <br/> |Координата y центральной точки.  <br/> |[Ellipse Row (Geometry Section)](ellipse-row-geometry-section.md) <br/> |
|А  <br/> |Координата x первой точки эллипса; Связывание с координатой y, представленной в ячейке B.  <br/> |[Ellipse Row (Geometry Section)](ellipse-row-geometry-section.md) <br/> |
|B  <br/> |Координата y первой точки эллипса; Связывание с координатой x, представленной ячейкой.  <br/> |[Ellipse Row (Geometry Section)](ellipse-row-geometry-section.md) <br/> |
|C  <br/> |Координата x второй точки эллипса; Связывание с координатой y, представленной ячейкой D.  <br/> |[Ellipse Row (Geometry Section)](ellipse-row-geometry-section.md) <br/> |
|D  <br/> |Координата y второй точки эллипса; Связывание с координатой y, представленной в ячейке C.  <br/> |[Ellipse Row (Geometry Section)](ellipse-row-geometry-section.md) <br/> |
   

