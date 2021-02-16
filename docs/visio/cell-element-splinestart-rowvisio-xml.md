---
title: Элемент Cell (строка SplineStart) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 021536b9-6724-4b8a-35c2-966e456e5232
description: Содержит координаты x или y для второй контрольной точки сплайна, второй подмайки, первой степени, последней затеи или степени сплайна.
ms.openlocfilehash: e3a99818d897af21e3064e0fc92d9d56ffcf5a15
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/29/2019
ms.locfileid: "34539357"
---
# <a name="cell-element-splinestart-row-visio-xml"></a>Элемент Cell (строка SplineStart) (Visio XML)

Содержит координаты x или y для второй контрольной точки сплайна, второй подмайки, первой степени, последней степени или градуса сплайна.
  
## <a name="element-information"></a>Сведения об элементе

|||
|:-----|:-----|
|**Тип элемента** <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |
|**Пространство имен** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Файл схемы** <br/> |VisioSchema15.xsd  <br/> |
|**Части документа** <br/> |master#.xml, page#.xml  <br/> |
   
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
|[Элемент Row (Geometry)](row-element-geometry-sectionvisio-xml.md) <br/> |[SplineStart_Type](splinestart_type-complextypevisio-xml.md) <br/> |Содержит координаты x или y для второй контрольной точки сплайна, второй подмайки, первой степени, последней затеи или степени сплайна.  <br/> |
   
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

Атрибут **N** этого элемента **Cell** должен быть одним из ограниченного набора значений, соответствующих ячейкам ShapeSheet. Чтобы определить значения атрибута **N,** допустимого для этого элемента **Cell,** обратитесь к приведенной ниже таблице. 
  
|**Значение**|**Описание**|**Дополнительные сведения**|
|:-----|:-----|:-----|
|X  <br/> |X-координата второй контрольной точки сплайна.  <br/> |[SplineStart Row (Geometry Section)](splinestart-row-geometry-section.md) <br/> |
|Да  <br/> |Y-координата второй контрольной точки сплайна.  <br/> |[SplineStart Row (Geometry Section)](splinestart-row-geometry-section.md) <br/> |
|A  <br/> |Вторая часть сплайна.  <br/> |[SplineStart Row (Geometry Section)](splinestart-row-geometry-section.md) <br/> |
|B  <br/> |Первая ветвь сплайна.  <br/> |[SplineStart Row (Geometry Section)](splinestart-row-geometry-section.md) <br/> |
|C  <br/> |Последняя часть сплайна.  <br/> |[RelEllipticalArcTo Row (Geometry Section)](splinestart-row-geometry-section.md) <br/> |
|D  <br/> |Степень сплайна (от 1 до 25).  <br/> |[SplineStart Row (Geometry Section)](splinestart-row-geometry-section.md) <br/> |
   

