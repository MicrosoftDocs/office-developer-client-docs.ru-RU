---
title: Элемент ячейки (раздел данных фигуры) ('Visio XML»)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 98643832-7861-385d-3a52-0060ea413e2e
description: Указывает одно свойство данных фигуры.
ms.openlocfilehash: 899b518f86979c831c0c05913420c7a62f0ea717
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19813381"
---
# <a name="cell-element-shape-data-section-visio-xml"></a>Элемент ячейки (раздел данных фигуры) ('Visio XML»)

Указывает одно свойство данных фигуры.
  
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
|[Элемент Row (раздел "Данные фигуры")](row-element-shape-data-sectionvisio-xml.md) <br/> |[Data_Type фигуры](propertyrow_type-complextypevisio-xml.md) <br/> |Задает одной записи данных фигуры для связывания данных с фигурой.  <br/> |
   
### <a name="child-elements"></a>Дочерние элементы

|**Элемент**|**Тип**|**Описание**|
|:-----|:-----|:-----|
|[RefBy](refby-element-cell_type-complextypevisio-xml.md) <br/> |[RefBy_Type](refby_type-complextypevisio-xml.md) <br/> |Задает ссылку на странице документа.  <br/> |
   
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
|Календарь  <br/> |Указывает тип используется, если тип элемента данных фигуры даты календаря.  <br/> |[Ячейка Calendar (раздел "Данные фигуры")](calendar-cell-shape-data-section.md) <br/> |
|DataLinked  <br/> |Указывает ли строки данных фигуры в настоящее время связь с полем в набор данных.  <br/> ||
|Format  <br/> |Задает форматирование элемента данных фигуры, — это строка, фиксированный список, число, список переменных, даты или времени, длительность или currency.  <br/> |[Ячейка Format (раздел "Данные фигуры")](format-cell-shape-data-section.md) <br/> |
|Невидимое  <br/> |Указывает, видима ли данные фигуры в окне данных фигуры.  <br/> |[Ячейка Invisible (раздел "Данные фигуры")](invisible-cell-shape-data-section.md) <br/> |
|Метка  <br/> |Метка, которая отображается для пользователей в окне данных фигуры. Элемент label состоит из буквенно-цифровых символов, включая символ подчеркивания (_).  <br/> |[Ячейка Label (раздел "Данные фигуры")](label-cell-shape-data-section.md) <br/> |
|LangID  <br/> |Указывает язык, в котором было введено значение данных фигуры.  <br/> |[Ячейка LangID (раздел "Данные фигуры")](langid-cell-shape-data-section.md) <br/> |
|Запрос  <br/> |Задает описательный или управляющий текст, который отображается в виде подсказки при наведении курсора на значение в окне данных фигуры.  <br/> |[Ячейка Prompt (раздел "Данные фигуры")](prompt-cell-shape-data-section.md) <br/> |
|SortKey  <br/> |Представляет собой строку, которая влияет на порядок, в котором перечислены элементы в окне данных фигуры.  <br/> |[Ячейка SortKey (раздел "Данные фигуры")](sortkey-cell-shape-data-section.md) <br/> |
|Тип  <br/> |Указывает тип данных для значения данных фигуры.  <br/> |[Ячейка Type (раздел "Данные фигуры")](type-cell-shape-data-section.md) <br/> |
|Значение  <br/> |Содержит значение элемента данных фигуры, введенное в диалоговом окне "Определение данных фигуры".  <br/> |[Ячейка Value (раздел "Данные фигуры")](value-cell-shape-data-section.md) <br/> |
|Проверка  <br/> |Указывает, является ли пользователь получает запрос на введите сведения о настраиваемых свойств для фигуры при создании экземпляра или фигуры и копировании.  <br/> |Нет.  <br/> |
   
