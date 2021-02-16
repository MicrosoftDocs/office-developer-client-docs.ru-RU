---
title: Элемент Cell (Shape Data Section) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 98643832-7861-385d-3a52-0060ea413e2e
description: Указывает одно свойство данных фигуры.
ms.openlocfilehash: 3a6238f19f27d001d3c9eebcbcec720822a0ed40
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/29/2019
ms.locfileid: "34539378"
---
# <a name="cell-element-shape-data-section-visio-xml"></a>Элемент Cell (Shape Data Section) (Visio XML)

Указывает одно свойство данных фигуры.
  
## <a name="element-information"></a>Сведения об элементе

|||
|:-----|:-----|
|**Тип элемента** <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |
|**Пространство имен** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Файл схемы** <br/> |VisioSchema15.xsd  <br/> |
|**Части документа** <br/> |master#.xml, page#.xml  <br/> |
   
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
|[Элемент Row (Shape Data Section)](row-element-shape-data-sectionvisio-xml.md) <br/> |[Фигуры Data_Type](propertyrow_type-complextypevisio-xml.md) <br/> |Указывает одну запись данных фигуры для связи данных с фигурой.  <br/> |
   
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
|Календарь  <br/> |Указывает тип календаря, используемый, когда типом элемента данных фигуры является "Дата".  <br/> |[Calendar Cell (Shape Data Section)](calendar-cell-shape-data-section.md) <br/> |
|DataLinked  <br/> |Указывает, связана ли в данный момент строка "Данные фигуры" с полем в наборе записей данных.  <br/> ||
|Format  <br/> |Указывает форматирование элемента данных фигуры, который является строкой, фиксированным списком, числом, списком переменных, датой или временем, продолжительностью или валютой.  <br/> |[Format Cell (Shape Data Section)](format-cell-shape-data-section.md) <br/> |
|Invisible  <br/> |Указывает, виден ли элемент данных фигуры в окне "Данные фигуры".  <br/> |[Invisible Cell (Shape Data Section)](invisible-cell-shape-data-section.md) <br/> |
|Метка  <br/> |Указывает метку, которая отображается для пользователей в окне "Данные фигуры". Метка состоит из букв и цифр, включая символ подчеркиваия (_).  <br/> |[Label Cell (Shape Data Section)](label-cell-shape-data-section.md) <br/> |
|LangID  <br/> |Указывает язык, на котором ввели значение данных фигуры.  <br/> |[LangID Cell (Shape Data Section)](langid-cell-shape-data-section.md) <br/> |
|Prompt  <br/> |Указывает описательный или инструктивный текст, который отображается как подсказка при приостановке мыши над значением в окне "Данные фигуры".  <br/> |[Prompt Cell (Shape Data Section)](prompt-cell-shape-data-section.md) <br/> |
|SortKey  <br/> |Оценивается в виде строки, которая влияет на порядок, в котором перечислены элементы в окне "Данные фигуры".  <br/> |[SortKey Cell (Shape Data Section)](sortkey-cell-shape-data-section.md) <br/> |
|Type  <br/> |Указывает тип данных для значения данных фигуры.  <br/> |[Type Cell (Shape Data Section)](type-cell-shape-data-section.md) <br/> |
|Значение  <br/> |Содержит значение элемента данных фигуры, введенное в диалоговом окне "Определение данных фигуры".  <br/> |[Value Cell (Shape Data Section)](value-cell-shape-data-section.md) <br/> |
|Проверка  <br/> |Указывает, запрашивается ли у пользователя ввод сведений о настраиваемом свойстве для фигуры при ее формировании или копировании.  <br/> |Нет.  <br/> |
   

