---
title: Элемент Cell (Line Gradient Section) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 8001249c-ea67-c5c0-3168-485400c43d8c
description: Содержит цвет, прозрачность или положение остановки градиента для градиента линии.
ms.openlocfilehash: d8ac664285d24e47a142c22b1483e2ff435aef48
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/29/2019
ms.locfileid: "34539504"
---
# <a name="cell-element-line-gradient-section-visio-xml"></a>Элемент Cell (Line Gradient Section) (Visio XML)

Содержит цвет, прозрачность или положение остановки градиента для градиента линии.
  
## <a name="element-information"></a>Сведения об элементе

|||
|:-----|:-----|
|**Тип элемента** <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |
|**Пространство имен** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Файл схемы** <br/> |VisioSchema15.xsd  <br/> |
|**Части документа** <br/> |document.xml, master#.xml, page#.xml  <br/> |
   
## <a name="definition"></a>Определение

```XML
< xs:element name="Cell"  type="Cell_Type" minOccurs="0" maxOccurs="unbounded">
</xs:element >
```

## <a name="elements-and-attributes"></a>Элементы и атрибуты

Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений. 
  
### <a name="parent-elements"></a>Родительские элементы

|**Элемент**|**Тип**|**Описание**|
|:-----|:-----|:-----|
|[Элемент Row (Line Gradient Section)](row-element-line-gradient-sectionvisio-xml.md) <br/> |[LineGradientRow_Type](linegradientrow_type-complextypevisio-xml.md) <br/> |Содержит цвет, прозрачность и положение остановки градиента для градиента линии.  <br/> |
   
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
|GradientStopColor  <br/> |Значение цвета остановки градиента.  <br/> |[Gradient Stop Row (Line Gradient Section)](gradient-stop-row-line-gradient-section.md) <br/> |
|GradientStopColorTrans  <br/> |Прозрачность цвета остановки градиента в процентах.  <br/> |[Gradient Stop Row (Line Gradient Section)](gradient-stop-row-line-gradient-section.md) <br/> |
|GradientStopPosition  <br/> |Положение градиента в направлении градиента линии в процентах от точки начала градиента до внешней границы градиента.  <br/> |[Gradient Stop Row (Line Gradient Section)](gradient-stop-row-line-gradient-section.md) <br/> |
   

