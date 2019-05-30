---
title: Элемент Cell (строка строка splinestart) (XML для Visio)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 021536b9-6724-4b8a-35c2-966e456e5232
description: Содержит координаты x или y для второй контрольной точки сплайна, второй Кнот, ее первый Кнот, последний кнот или степень сплайна.
ms.openlocfilehash: e3a99818d897af21e3064e0fc92d9d56ffcf5a15
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/29/2019
ms.locfileid: "34539357"
---
# <a name="cell-element-splinestart-row-visio-xml"></a>Элемент Cell (строка строка splinestart) (XML для Visio)

Содержит координаты x или y для второй контрольной точки сплайна, второй Кнот, ее первый Кнот, последний кнот или степень сплайна.
  
## <a name="element-information"></a>Сведения об элементе

|||
|:-----|:-----|
|**Тип элемента** <br/> |[Целл_типе](cell_type-complextypevisio-xml.md) <br/> |
|**Пространство имен** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Файл схемы** <br/> |VisioSchema15. xsd  <br/> |
|**Части документа** <br/> |Master #. XML, Page #. XML  <br/> |
   
## <a name="definition"></a>Определение

```XML
<xs:element name="Cell" type="Cell_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element>
```

## <a name="elements-and-attributes"></a>Элементы и атрибуты

Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений. 
  
### <a name="parent-elements"></a>Родительские элементы

|**Элемент**|**Тип**|**Описание**|
|:-----|:-----|:-----|
|[Элемент Row (геометрия)](row-element-geometry-sectionvisio-xml.md) <br/> |[Сплинестарт_типе](splinestart_type-complextypevisio-xml.md) <br/> |Содержит координаты x или y для второй контрольной точки сплайна, второй Кнот, ее первый Кнот, последний кнот или степень сплайна.  <br/> |
   
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
|X  <br/> |Координата x второй контрольной точки сплайна.  <br/> |[SplineStart Row (Geometry Section)](splinestart-row-geometry-section.md) <br/> |
|Да  <br/> |Координата y второй контрольной точки сплайна.  <br/> |[SplineStart Row (Geometry Section)](splinestart-row-geometry-section.md) <br/> |
|A  <br/> |Второй кнот сплайна.  <br/> |[SplineStart Row (Geometry Section)](splinestart-row-geometry-section.md) <br/> |
|B  <br/> |Первый кнот сплайна.  <br/> |[SplineStart Row (Geometry Section)](splinestart-row-geometry-section.md) <br/> |
|C  <br/> |Последний кнот сплайна.  <br/> |[RelEllipticalArcTo Row (Geometry Section)](splinestart-row-geometry-section.md) <br/> |
|D  <br/> |Степень сплайна (целое число от 1 до 25).  <br/> |[SplineStart Row (Geometry Section)](splinestart-row-geometry-section.md) <br/> |
   

