---
title: Элемент Cell (Control Row) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 3c04d243-002c-bb00-a4be-0bcb8e156402
description: Содержит свойство для определенной ручки управления, определенной для фигуры.
ms.openlocfilehash: 662dfe730c92ae25b3d243364bf1fa22a5eb8605
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/29/2019
ms.locfileid: "34541837"
---
# <a name="cell-element-controls-row-visio-xml"></a>Элемент Cell (Control Row) (Visio XML)

Содержит свойство для определенной ручки управления, определенной для фигуры.
  
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
|[Элемент Row (Раздел элементов управления)](row-element-controls-sectionvisio-xml.md) <br/> |[ControlRow_Type](controlrow_type-complextypevisio-xml.md) <br/> |Содержит свойство для определенной ручки управления, определенной для фигуры.  <br/> |
   
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
|CanGlue  <br/> |Определяет, можно ли приклеить ручку управления к другим фигурам.  <br/> |[Can Glue Cell (Controls Section)](can-glue-cell-controls-section.md) <br/> |
|Prompt  <br/> |Представляет текстовую строку описательный, которая появляется в виде ToolTip, когда пользователь приостанавливет указатель над ручкой управления фигурой.  <br/> |[Tip Cell (Controls Section)](tip-cell-controls-section.md) <br/> |
|X  <br/> |Представляет x-координату, которая указывает расположение ручки управления фигуры в локальных координатах.  <br/> |[X Cell (Controls Section)](x-cell-controls-section.md) <br/> |
|xCon  <br/> |Указывает тип поведения, который х-координаты выставит ручка управления после ее перемещений.  <br/> |Нет.  <br/> |
|xDyn  <br/> |Представляет x-координату для якорной точки ручки управления в локальных координатах.  <br/> |[X Dynamics Cell (Controls Section)](x-dynamics-cell-controls-section.md) <br/> |
|Да  <br/> |Представляет y-координату, которая указывает расположение ручки управления фигуры в локальных координатах.  <br/> |[Y Cell (Controls Section)](y-cell-controls-section.md) <br/> |
|YCon  <br/> |Указывает тип поведения, который выставит y-координата ручки управления после ее перемещений.  <br/> |Нет.  <br/> |
|YDyn  <br/> |Представляет точку якоря y-coordinate для якорной точки ручки управления в локальных координатах.  <br/> |[Y Dynamics Cell (Controls Section)](y-dynamics-cell-controls-section.md) <br/> |
   

