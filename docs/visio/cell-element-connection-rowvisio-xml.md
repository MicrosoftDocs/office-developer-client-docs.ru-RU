---
title: Элемент ячейки (строка подключения) ('Visio XML»)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 7cafaa31-c56b-ebb0-3bfb-c339cc93038e
description: Содержит координаты x и y, горизонтальный или вертикальный направление или тип для одна точка подключения на фигуры.
ms.openlocfilehash: 52328e50b185a96ebb06634248b93a4332ac35c2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19813328"
---
# <a name="cell-element-connection-row-visio-xml"></a>Элемент ячейки (строка подключения) ('Visio XML»)

Содержит координаты x и y, горизонтальный или вертикальный направление или тип для одна точка подключения на фигуры.
  
## <a name="element-information"></a>Сведения об элементе

|||
|:-----|:-----|
|**Тип элемента** <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |
|**Пространство имен** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Файл схемы** <br/> |VisioSchema15.xsd  <br/> |
|**Части документа** <br/> |главные # .xml, страницы # .xml  <br/> |
   
## <a name="definition"></a>Определение

```XML
< xs:element name="Cell" type="Cell_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a>Элементы и атрибуты

Если схема определяет специальные требования, такие как **последовательность**, **minOccurs**, **maxOccurs**и **выбора**, обратитесь к разделу определение. 
  
### <a name="parent-elements"></a>Родительские элементы

|**Элемент**|**Тип**|**Описание**|
|:-----|:-----|:-----|
|[Элемент Row (раздел "Соединение")](row-element-connection-sectionvisio-xml.md) <br/> |[ConnectionRow_Type](connectionrow_type-complextypevisio-xml.md) <br/> |Содержит координаты x и y, направление горизонтальных и вертикальных и тип одна точка подключения на фигуры.  <br/> |
   
### <a name="child-elements"></a>Дочерние элементы

|**Элемент**|**Тип**|**Описание**|
|:-----|:-----|:-----|
|[RefBy](refby-element-cell_type-complextypevisio-xml.md) <br/> |[RefBy_Type](refby_type-complextypevisio-xml.md) <br/> |Содержит координаты x и y, направление горизонтальных и вертикальных и тип одна точка подключения на фигуры.  <br/> |
   
### <a name="attributes"></a>Атрибуты

|**Атрибут**|**Тип**|**Обязательное**|**Описание**|**Возможные значения**|
|:-----|:-----|:-----|:-----|:-----|
|E  <br/> |XSD:String  <br/> |необязательный  <br/> |Указывает, что формулы оценивается как ошибка. Значение **E** является текущим значением (строка сообщения об ошибке); значение атрибута **V** — это последний допустимое значение.  <br/> |Строка сообщения об ошибке.  <br/> |
|F  <br/> |XSD:String  <br/> |необязательный  <br/> | Представляет элемент формулы. Этот атрибут может содержать один из следующих строк:  <br/>  (Некоторые формулы) Если формула существует локально  <br/>  `No Formula`Если формула локально удален или заблокирован  <br/>  `Inh`Если наследуется формулу.  <br/> |Формула.  <br/> |
|N  <br/> |XSD:String  <br/> |Обязательный  <br/> |Представляет имя ячейки таблицы свойств фигуры.  <br/> |Имя ячейки таблицы свойств фигуры.  <br/> В разделе замечания ниже.  <br/> |
|U  <br/> |XSD:String  <br/> |необязательный  <br/> |Представляет единицы измерения по умолчанию — это список Рассылки.  <br/> |Единицы ячейки.  <br/> |
|V  <br/> |XSD:String  <br/> |необязательный  <br/> |Представляет значение ячейки.  <br/> |Значение ячейки таблицы свойств фигуры.  <br/> |
   
## <a name="remarks"></a>Замечания

Атрибут **N** этого элемента **ячейки** должен быть один из ограниченный набор значений, которые соответствуют ячейки таблицы свойств фигуры. Обратитесь к таблице ниже для определения значений атрибутов **N** , разрешенных для этого элемента **ячейки** . 
  
|**Значение**|**Описание**|**Дополнительные сведения**|
|:-----|:-----|:-----|
|AutoGen  <br/> |Указывает, является ли автоматически создавать точку подключения. Значение 1 указывает точку подключения создается автоматически.  <br/> |Нет.  <br/> |
|DirX  <br/> |Определяет компонент x для вектор Обязательное выравнивание совпадающих точки подключения.  <br/> |[Ячейка DirX / A (раздел "Точки соединения")](dirxa-cell-connection-points-section.md) <br/> |
|DirY  <br/> |Определяет компонент y для вектор Обязательное выравнивание совпадающих точки подключения.  <br/> |[Ячейка DirY / B (раздел "Точки соединения")](diryb-cell-connection-points-section.md) <br/> |
|Запрос  <br/> |Этот атрибут зарезервирован для будущего использования.  <br/> |Нет.  <br/> |
|Тип  <br/> |Определяет тип точки подключения.  <br/> |[Ячейка Type / C (раздел "Точки соединения")](typec-cell-connection-points-section.md) <br/> |
|X   <br/> |Представляет координаты x точки подключения в локальной системе координат.  <br/> |[Ячейка X (раздел "Точки соединения")](x-cell-connection-points-section.md) <br/> |
|Да  <br/> |Определяет координаты y для точки подключения в локальной системе координат.  <br/> |[Ячейка Y (раздел "Точки соединения")](y-cell-connection-points-section.md) <br/> |
   
