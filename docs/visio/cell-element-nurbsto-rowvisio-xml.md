---
title: Элемент cell (NURBSTo Row) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: e76bae8f-b9de-39ef-1f56-b00a6cd2ba6c
description: Содержит x- или y-координаты, положение второго до последнего узла, положение последнего веса, положение первого узла, положение первого веса или формулу для неинформированной рациональной B-spline (NURBS).
ms.openlocfilehash: 3128149d1e787dde7677c2a202a29ac8efa6da43
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/29/2019
ms.locfileid: "34539490"
---
# <a name="cell-element-nurbsto-row-visio-xml"></a>Элемент cell (NURBSTo Row) (Visio XML)

Содержит x- или y-координаты, положение второго до последнего узла, положение последнего веса, положение первого узла, положение первого веса или формулу для неинформированной рациональной B-spline (NURBS).
  
## <a name="element-information"></a>Сведения об элементе

|||
|:-----|:-----|
|**Тип элемента** <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |
|**Пространство имен** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Файл схемы** <br/> |VisioSchema15.xsd  <br/> |
|**Части документов** <br/> |master#.xml, page#.xml  <br/> |
   
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
|[Элемент Row (Геометрия)](row-element-geometry-sectionvisio-xml.md) <br/> |[NURBSTo_Type](nurbsto_type-complextypevisio-xml.md) <br/> |Содержит x- или y-координаты, положение второго до последнего узла, положение последнего веса, положение первого узла, положение первого веса или формулу для неинформированной рациональной B-spline (NURBS).  <br/> |
   
### <a name="child-elements"></a>Дочерние элементы

|**Элемент**|**Тип**|**Описание**|
|:-----|:-----|:-----|
|[RefBy](refby-element-cell_type-complextypevisio-xml.md) <br/> |[RefBy_Type](refby_type-complextypevisio-xml.md) <br/> |Указывает ссылку на страницу рисования.  <br/> |
   
### <a name="attributes"></a>Атрибуты

|**Атрибут**|**Тип**|**Обязательный**|**Описание**|**Возможные значения**|
|:-----|:-----|:-----|:-----|:-----|
|E  <br/> |xsd:string  <br/> |необязательный  <br/> |Указывает, что формула оценивается как ошибка. Значение **E —** текущее значение (строка сообщения об ошибке); Значение атрибута **V** является последним допустимым значением.  <br/> |Строка сообщения об ошибке.  <br/> |
|F  <br/> |xsd:string  <br/> |необязательный  <br/> | Представляет формулу элемента. Этот атрибут может содержать одну из следующих строк:  <br/>  "(некоторые формулы)", если формула существует локально  <br/>  `No Formula` если формула локально удалена или заблокирована  <br/>  `Inh` если формула наследуется.  <br/> |Формула.  <br/> |
|Нет  <br/> |xsd:string  <br/> |Обязательный  <br/> |Представляет имя ячейки ShapeSheet.  <br/> |Имя ячейки ShapeSheet.  <br/> См. раздел Замечания ниже.  <br/> |
|U  <br/> |xsd:string  <br/> |необязательный  <br/> |Представляет единицу измерения, по умолчанию — DL.  <br/> |Единицы ячейки.  <br/> |
|V  <br/> |xsd:string  <br/> |необязательный  <br/> |Представляет значение ячейки.  <br/> |Значение ячейки ShapeSheet.  <br/> |
   
## <a name="remarks"></a>Примечания

Атрибут **N** этого элемента **Cell** должен быть одним из ограниченного набора значений, соответствующих ячейкам ShapeSheet. Обратитесь к приведенной ниже таблице, чтобы определить значения атрибута **N,** разрешенные для этого элемента **Cell.** 
  
|**Значение**|**Описание**|**Дополнительные сведения**|
|:-----|:-----|:-----|
|X  <br/> |X-координата последней контрольной точки NURBS.  <br/> |[NURBSTo Row (Geometry Section)](nurbsto-row-geometry-section.md) <br/> |
|Да  <br/> |Y-координата последней точки управления NURBS.  <br/> |[NURBSTo Row (Geometry Section)](nurbsto-row-geometry-section.md) <br/> |
|A  <br/> |Второй до последнего узла NURBS.  <br/> |[NURBSTo Row (Geometry Section)](nurbsto-row-geometry-section.md) <br/> |
|B  <br/> |Последний вес NURBS.  <br/> |[NURBSTo Row (Geometry Section)](nurbsto-row-geometry-section.md) <br/> |
|C  <br/> |Первый узел NURBS.  <br/> |[NURBSTo Row (Geometry Section)](nurbsto-row-geometry-section.md) <br/> |
|D  <br/> |Первый вес NURBS.  <br/> |[NURBSTo Row (Geometry Section)](nurbsto-row-geometry-section.md) <br/> |
|E  <br/> |Формула NURBS.  <br/> |[NURBSTo Row (Geometry Section)](nurbsto-row-geometry-section.md) <br/> |
   

