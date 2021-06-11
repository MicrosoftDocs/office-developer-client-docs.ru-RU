---
title: Элемент Cell (Раздел символов) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6b452591-cf0c-9e1c-c203-e9cf608d3cc3
description: Указывает атрибут форматирования для текстового запуска фигуры, например шрифта, цвета, стиля, дела, позиции по отношению к базовому или размеру точки.
ms.openlocfilehash: a7d67aa3c53f3a4c673151afc991202904f0557b
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/29/2019
ms.locfileid: "34540086"
---
# <a name="cell-element-character-section-visio-xml"></a>Элемент Cell (Раздел символов) (Visio XML)

Указывает атрибут форматирования для текстового запуска фигуры, например шрифта, цвета, стиля, дела, позиции по отношению к базовому или размеру точки.
  
## <a name="element-information"></a>Сведения об элементе

|||
|:-----|:-----|
|**Тип элемента** <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |
|**Пространство имен** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Файл схемы** <br/> |VisioSchema15.xsd  <br/> |
|**Части документов** <br/> |document.xml, master#.xml, page#.xml  <br/> |
   
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
|[Элемент Row (Раздел символов)](row-element-character-sectionvisio-xml.md) <br/> |[CharacterRow_Type](characterrow_type-complextypevisio-xml.md) <br/> |Указывает атрибут форматирования для текстового запуска фигуры, например шрифта, цвета, стиля, дела, позиции по отношению к базовому или размеру точки.  <br/> |
   
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
|AsianFont  <br/> |Содержит переоформление шрифта, используемого для форматирования текстового запуска, содержащего азиатские символы.  <br/> |[AsianFont Cell (Character Section)](asianfont-cell-character-section.md) <br/> |
|Дело  <br/> |Определяет случай запуска текста фигуры.  <br/> |[Case Cell (Character Section)](case-cell-character-section.md) <br/> |
|Цвет  <br/> |Определяет цвет, используемый для текстового запуска фигуры.  <br/> |[Color Cell (Character Section)](color-cell-character-section.md) <br/> |
|ColorTrans  <br/> |Определяет степень прозрачности для цвета текстового запуска слоя или формы от 0 (полностью непрозрачная) до 1 (полностью прозрачная).  <br/> |Нет.  <br/> |
|ComplexScriptFont  <br/> |Содержит число шрифта, используемого для формата текстового запуска, состоящего из сложных символов скрипта.  <br/> |[ComplexScriptFont Cell (Character Section)](complexscriptfont-cell-character-section.md) <br/> |
|ComplexScriptSize  <br/> |Размер шрифта, используемого для формата текстового запуска, состоящего из сложных символов скрипта.  <br/> |[ComplexScriptSize Cell (Character Section)](complexscriptsize-cell-character-section.md) <br/> |
|DblUnderline  <br/> |Определяет, имеет ли диапазон текстового запуска двойное подчеркнуть под ней.  <br/> |[DoubleULine Cell (Character Section)](doubleuline-cell-character-section.md) <br/> |
|DoubleStrikethrough  <br/> |Определяет, форматирован ли текстовый запуск в виде двойного забастовки.  <br/> |[DoubleStrikethrough Cell (Character Section)](doublestrikethrough-cell-character-section.md) <br/> |
|Font  <br/> |Представляет число шрифта, используемого для формата текстового запуска.  <br/> |[Font Cell (Character Section)](font-cell-character-section.md) <br/> |
|FontScale  <br/> |Указывает ширину шрифта.  <br/> |Нет.  <br/> |
|LangID  <br/> |Указывает язык, на котором был введен текстовый запуск.  <br/> |[LangID Cell (Character Section)](langid-cell-character-section.md) <br/> |
|Letterspace  <br/> |Указывает количество пространства между двумя или более символами. Пространство можно добавлять или вычитать в 1/20-й точке приращений.  <br/> |Нет.  <br/> |
|Overline  <br/> |Определяет, есть ли над текстом строка.  <br/> |[Overline Cell (Character Section)](overline-cell-character-section.md) <br/> |
|Pos  <br/> |Определяет положение текста фигуры по отношению к базовой.  <br/> |[Pos Cell (Character Section)](pos-cell-character-section.md) <br/> |
|Size  <br/> |Определяет размер текстового запуска в текстовом блоке фигуры.  <br/> |[Size Cell (Character Section)](size-cell-character-section.md) <br/> |
|Strikethru  <br/> |Определяет, форматирован ли текстовый запуск в виде strikethrough.  <br/> |[Strikethru Cell (Character Section)](strikethru-cell-character-section.md) <br/> |
|Style  <br/> |Показывает форматирование символов, применяемого к диапазону текста, запускаемого в текстовом блоке фигуры.  <br/> |[Style Cell (Character Section)](style-cell-character-section.md) <br/> |
   

