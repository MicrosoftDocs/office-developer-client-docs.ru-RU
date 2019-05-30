---
title: Элемент Cell (раздел "символ") (XML-файл Visio)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6b452591-cf0c-9e1c-c203-e9cf608d3cc3
description: Задает атрибут форматирования для текстового запуска фигуры, например шрифт, цвет, стиль, регистр, положение относительно базовой линии или кегля.
ms.openlocfilehash: a7d67aa3c53f3a4c673151afc991202904f0557b
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/29/2019
ms.locfileid: "34540086"
---
# <a name="cell-element-character-section-visio-xml"></a>Элемент Cell (раздел "символ") (XML-файл Visio)

Задает атрибут форматирования для текстового запуска фигуры, например шрифт, цвет, стиль, регистр, положение относительно базовой линии или кегля.
  
## <a name="element-information"></a>Сведения об элементе

|||
|:-----|:-----|
|**Тип элемента** <br/> |[Целл_типе](cell_type-complextypevisio-xml.md) <br/> |
|**Пространство имен** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Файл схемы** <br/> |VisioSchema15. xsd  <br/> |
|**Части документа** <br/> |Document. XML, Master #. XML, Page #. XML  <br/> |
   
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
|[Элемент Row (раздел "символ")](row-element-character-sectionvisio-xml.md) <br/> |[Чарактерров_типе](characterrow_type-complextypevisio-xml.md) <br/> |Задает атрибут форматирования для текстового запуска фигуры, например шрифт, цвет, стиль, регистр, положение относительно базовой линии или кегля.  <br/> |
   
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
|AsianFont  <br/> |Содержит перечисление шрифта, используемого для форматирования текста Run, содержащего восточноазиатские символы.  <br/> |[AsianFont Cell (Character Section)](asianfont-cell-character-section.md) <br/> |
|Ситуация  <br/> |Определяет регистр текстового запуска фигуры.  <br/> |[Case Cell (Character Section)](case-cell-character-section.md) <br/> |
|Цвет  <br/> |Определяет цвет, используемый для текстового запуска фигуры.  <br/> |[Color Cell (Character Section)](color-cell-character-section.md) <br/> |
|Колортранс  <br/> |Определяет степень прозрачности для цвета выполнения текста слоя или фигуры от 0 (полностью непрозрачна) до 1 (полностью прозрачно).  <br/> |Нет.  <br/> |
|ComplexScriptFont  <br/> |Содержит номер шрифта, используемого для форматирования текстового фрагмента, состоящего из сложных символов.  <br/> |[ComplexScriptFont Cell (Character Section)](complexscriptfont-cell-character-section.md) <br/> |
|ComplexScriptSize  <br/> |Размер шрифта, используемого для форматирования текстового фрагмента, состоящего из сложных символов.  <br/> |[ComplexScriptSize Cell (Character Section)](complexscriptsize-cell-character-section.md) <br/> |
|Дблундерлине  <br/> |Определяет, имеет ли диапазон текстовой цепочки двойное подчеркивание.  <br/> |[DoubleULine Cell (Character Section)](doubleuline-cell-character-section.md) <br/> |
|DoubleStrikethrough  <br/> |Определяет, отформатирован ли текст двойным зачеркиванием.  <br/> |[DoubleStrikethrough Cell (Character Section)](doublestrikethrough-cell-character-section.md) <br/> |
|Шрифт  <br/> |Представляет номер шрифта, используемого для форматирования текстового запуска.  <br/> |[Font Cell (Character Section)](font-cell-character-section.md) <br/> |
|Фонтскале  <br/> |Задает ширину шрифта.  <br/> |Нет.  <br/> |
|LangID  <br/> |Указывает язык, на котором было введено текстовое выполнение.  <br/> |[LangID Cell (Character Section)](langid-cell-character-section.md) <br/> |
|Леттерспаце  <br/> |Задает расстояние между двумя или более символами. Место можно добавить или вычесть с шагом 1/20-й точки.  <br/> |Нет.  <br/> |
|Overline  <br/> |Определяет, содержит ли текстовая цепочка линию над ним.  <br/> |[Overline Cell (Character Section)](overline-cell-character-section.md) <br/> |
|Терминал  <br/> |Определяет положение текста фигуры, выполняемого относительно базового плана.  <br/> |[Pos Cell (Character Section)](pos-cell-character-section.md) <br/> |
|Размер  <br/> |Определяет размер текста, выполняемого в блоке текста фигуры.  <br/> |[Size Cell (Character Section)](size-cell-character-section.md) <br/> |
|Strikethru  <br/> |Определяет, отформатирован ли текст с зачеркиванием.  <br/> |[Strikethru Cell (Character Section)](strikethru-cell-character-section.md) <br/> |
|Стиль  <br/> |Показывает форматирование символов, применяемое к диапазону текста Run в блоке текста фигуры.  <br/> |[Style Cell (Character Section)](style-cell-character-section.md) <br/> |
   

