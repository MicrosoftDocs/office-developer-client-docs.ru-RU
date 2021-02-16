---
title: Элемент Cell (Character Section) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6b452591-cf0c-9e1c-c203-e9cf608d3cc3
description: Указывает атрибут форматирования для текстового запуска фигуры, например шрифт, цвет, стиль, случай, положение относительно базового плана или размера точки.
ms.openlocfilehash: a7d67aa3c53f3a4c673151afc991202904f0557b
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/29/2019
ms.locfileid: "34540086"
---
# <a name="cell-element-character-section-visio-xml"></a>Элемент Cell (Character Section) (Visio XML)

Указывает атрибут форматирования для текстового запуска фигуры, например шрифт, цвет, стиль, случай, положение относительно базового плана или размера точки.
  
## <a name="element-information"></a>Сведения об элементе

|||
|:-----|:-----|
|**Тип элемента** <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |
|**Пространство имен** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Файл схемы** <br/> |VisioSchema15.xsd  <br/> |
|**Части документа** <br/> |document.xml, master#.xml, page#.xml  <br/> |
   
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
|[Элемент Row (Character Section)](row-element-character-sectionvisio-xml.md) <br/> |[CharacterRow_Type](characterrow_type-complextypevisio-xml.md) <br/> |Указывает атрибут форматирования для текстового запуска фигуры, например шрифт, цвет, стиль, случай, положение относительно базового плана или размера точки.  <br/> |
   
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
|AsianFont  <br/> |Содержит enumeration шрифта, используемого для форматирования текста, содержащего азиатские символы.  <br/> |[AsianFont Cell (Character Section)](asianfont-cell-character-section.md) <br/> |
|Ситуация  <br/> |Определяет случай запуска текста фигуры.  <br/> |[Case Cell (Character Section)](case-cell-character-section.md) <br/> |
|Цвет  <br/> |Определяет цвет, используемый для запуска текста фигуры.  <br/> |[Color Cell (Character Section)](color-cell-character-section.md) <br/> |
|ColorTrans  <br/> |Определяет степень прозрачности для цвета прогона текста слоя или фигуры от 0 (полностью непрозрачная) до 1 (полностью прозрачная).  <br/> |Нет.  <br/> |
|ComplexScriptFont  <br/> |Содержит количество шрифтов, используемых для формата текстового запуска, состоящего из сложных символов скрипта.  <br/> |[ComplexScriptFont Cell (Character Section)](complexscriptfont-cell-character-section.md) <br/> |
|ComplexScriptSize  <br/> |Размер шрифта, используемого для формата текстового запуска, состоящего из сложных символов скрипта.  <br/> |[ComplexScriptSize Cell (Character Section)](complexscriptsize-cell-character-section.md) <br/> |
|DblUnderline  <br/> |Определяет, имеет ли диапазон текстового запуска двойной подчеркнутой линией под ней.  <br/> |[DoubleULine Cell (Character Section)](doubleuline-cell-character-section.md) <br/> |
|DoubleStrikethrough  <br/> |Определяет, отформатирован ли текстовый запуск в формате двойного загона.  <br/> |[DoubleStrikethrough Cell (Character Section)](doublestrikethrough-cell-character-section.md) <br/> |
|Шрифт  <br/> |Представляет число шрифта, используемого для формата текстового запуска.  <br/> |[Font Cell (Character Section)](font-cell-character-section.md) <br/> |
|FontScale  <br/> |Указывает ширину шрифта.  <br/> |Нет.  <br/> |
|LangID  <br/> |Указывает язык, на котором был введен текстовый запуск.  <br/> |[LangID Cell (Character Section)](langid-cell-character-section.md) <br/> |
|Letterspace  <br/> |Указывает объем пространства между двумя или более символами. Пространство можно добавлять или вычитать с 1/20-й точки.  <br/> |Нет.  <br/> |
|Overline  <br/> |Определяет, есть ли строка над текстовым запуском.  <br/> |[Overline Cell (Character Section)](overline-cell-character-section.md) <br/> |
|Pos  <br/> |Определяет положение текста фигуры относительно базового плана.  <br/> |[Pos Cell (Character Section)](pos-cell-character-section.md) <br/> |
|Size  <br/> |Определяет размер текста, запускаемого в текстовом блоке фигуры.  <br/> |[Size Cell (Character Section)](size-cell-character-section.md) <br/> |
|Strikethru  <br/> |Определяет, отформатирован ли текстовый запуск в виде загона.  <br/> |[Strikethru Cell (Character Section)](strikethru-cell-character-section.md) <br/> |
|Style  <br/> |Отображает форматирование символов, применяемого к диапазону текста, который работает в текстовом блоке фигуры.  <br/> |[Style Cell (Character Section)](style-cell-character-section.md) <br/> |
   

