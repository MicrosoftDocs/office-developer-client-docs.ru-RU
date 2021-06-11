---
title: Элемент Cell (Строка подключения) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 7cafaa31-c56b-ebb0-3bfb-c339cc93038e
description: Содержит x- или y-координаты, горизонтальное или вертикальное направление или введите для одной точки подключения на фигуре.
ms.openlocfilehash: 0c8177767d5c85d505ba8a2a430946fd29cf44aa
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/29/2019
ms.locfileid: "34541878"
---
# <a name="cell-element-connection-row-visio-xml"></a>Элемент Cell (Строка подключения) (Visio XML)

Содержит x- или y-координаты, горизонтальное или вертикальное направление или введите для одной точки подключения на фигуре.
  
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
|[Элемент Row (Раздел Подключения)](row-element-connection-sectionvisio-xml.md) <br/> |[ConnectionRow_Type](connectionrow_type-complextypevisio-xml.md) <br/> |Содержит x- и y-координаты, горизонтальное и вертикальное направление и введите для одной точки подключения на фигуре.  <br/> |
   
### <a name="child-elements"></a>Дочерние элементы

|**Элемент**|**Тип**|**Описание**|
|:-----|:-----|:-----|
|[RefBy](refby-element-cell_type-complextypevisio-xml.md) <br/> |[RefBy_Type](refby_type-complextypevisio-xml.md) <br/> |Содержит x- или y-координаты, горизонтальное и вертикальное направление и введите для одной точки подключения на фигуре.  <br/> |
   
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
|AutoGen  <br/> |Указывает, создается ли точка подключения автоматически. Значение 1 указывает, что точка подключения создается автоматически.  <br/> |Нет.  <br/> |
|DirX  <br/> |Определяет x-компонент для необходимого вектора выравнивания точки подключения.  <br/> |[DirX / A Cell (Connection Points Section)](dirxa-cell-connection-points-section.md) <br/> |
|DirY  <br/> |Определяет y-компонент для необходимого вектора выравнивания точки подключения.  <br/> |[DirY / B Cell (Connection Points Section)](diryb-cell-connection-points-section.md) <br/> |
|Prompt  <br/> |Этот атрибут зарезервирован для будущего использования.  <br/> |Нет.  <br/> |
|Тип  <br/> |Определяет тип точки подключения.  <br/> |[Type / C Cell (Connection Points Section)](typec-cell-connection-points-section.md) <br/> |
|X  <br/> |Представляет x-координату для точки подключения в локальных координатах.  <br/> |[X Cell (Connection Points Section)](x-cell-connection-points-section.md) <br/> |
|Да  <br/> |Определяет y-координату точки подключения в локальных координатах.  <br/> |[Y Cell (Connection Points Section)](y-cell-connection-points-section.md) <br/> |
   

