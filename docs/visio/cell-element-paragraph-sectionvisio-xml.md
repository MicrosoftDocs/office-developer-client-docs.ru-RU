---
title: Элемент Cell (раздел "Абзац") ("Visio XML")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: de0d3aac-1a0f-1bdf-da94-e6699a55d08e
description: Задает атрибут форматирования абзаца для текста фигуры, например отступы, междустрочный интервал, маркеры или горизонтальное выравнивание абзацев.
ms.openlocfilehash: 2647ce92b38234e4d6fc4d6bc59188d468332ca8
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32344844"
---
# <a name="cell-element-paragraph-section-visio-xml"></a>Элемент Cell (раздел "Абзац") ("Visio XML")

Задает атрибут форматирования абзаца для текста фигуры, например отступы, междустрочный интервал, маркеры или горизонтальное выравнивание абзацев.
  
## <a name="element-information"></a>Сведения об элементе

|||
|:-----|:-----|
|**Тип элемента** <br/> |[Целл_типе](cell_type-complextypevisio-xml.md) <br/> |
|**Пространство имен** <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
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
|[Элемент Row (раздел "Абзац")](row-element-paragraph-sectionvisio-xml.md) <br/> |[Параграфров_типе](paragraphrow_type-complextypevisio-xml.md) <br/> |Задает атрибут форматирования абзаца для текста фигуры, например отступы, междустрочный интервал, маркеры или горизонтальное выравнивание абзацев.  <br/> |
   
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
   
## <a name="remarks"></a>Комментарии

Атрибут **N** этого элемента **Cell** должен иметь ограниченный набор значений, соответствующих ячейкам таблицы свойств фигуры. Чтобы определить значения атрибута **N** , которые разрешено использовать для этого элемента **ячейки** , обратитесь к приведенной ниже таблице. 
  
|**Value**|**Описание**|**Дополнительные сведения**|
|:-----|:-----|:-----|
|Bullet  <br/> |Определяет стиль маркеров.  <br/> |[Bullet Cell (Paragraph Section)](bullet-cell-paragraph-section.md) <br/> |
|BulletFont  <br/> |Представляет номер шрифта, используемого для форматирования текста, если указана строка настраиваемого маркера, а значение в ячейке маркера не равно нулю.  <br/> |[BulletFont Cell (Paragraph Section)](bulletfont-cell-paragraph-section.md) <br/> |
|Буллетфонтсизе  <br/> |Задает размер маркера.  <br/> |[BulletSize Cell (Paragraph Section)](bulletsize-cell-paragraph-section.md) <br/> |
|Буллетстр  <br/> |Позволяет создавать пользовательские стили маркеров.  <br/> |[BulletString Cell (Paragraph Section)](bulletstring-cell-paragraph-section.md) <br/> |
|Flags  <br/> |Указывает, находится ли направление текста слева направо или справа налево.  <br/> |[Flags Cell (Paragraph Section)](flags-cell-paragraph-section.md) <br/> |
|Хорзалигн  <br/> |Определяет горизонтальное выравнивание текста в блоке текста фигуры.  <br/> |[HAlign Cell (Paragraph Section)](halign-cell-paragraph-section.md) <br/> |
|Индфирст  <br/> |Представляет расстояние отступа первой строки каждого абзаца в блоке текста фигуры слева от левого отступа абзаца. Это значение не зависит от масштаба рисунка. Если масштаб документа изменяется, отступ первой строки остается прежним.  <br/> |[IndFirst Cell (Paragraph Section)](indfirst-cell-paragraph-section.md) <br/> |
|IndLeft  <br/> |Представляет расстояние для всех строк текста в абзаце с отступом от левого поля блока текста. Это значение не зависит от масштаба рисунка. Если масштаб документа изменяется, отступ слева остается прежним.  <br/> |[IndLeft Cell (Paragraph Section)](indleft-cell-paragraph-section.md) <br/> |
|IndRight  <br/> |Представляет расстояние для всех строк текста в абзаце с отступом от правого поля блока текста. Это значение не зависит от масштаба рисунка. Если масштаб документа изменяется, отступ справа остается прежним.  <br/> |[IndRight Cell (Paragraph Section)](indright-cell-paragraph-section.md) <br/> |
|SpAfter  <br/> |Определяет объем пространства, вставленного после каждого абзаца в блоке текста фигуры, в дополнение к любому пробелу из ячейки сплайна и, если это последний абзац в текстовом блоке, ячейка BottomMargin.  <br/> |[SpAfter Cell (Paragraph Section)](spafter-cell-paragraph-section.md) <br/> |
|SpBefore  <br/> |Определяет количество пробелов, вставленных перед каждым абзацем в блоке текста фигуры, в дополнение к любому пробелу из ячейки сплайна, если это первый абзац в текстовом блоке, ячейка TopMargin.  <br/> |[SpBefore Cell (Paragraph Section)](spbefore-cell-paragraph-section.md) <br/> |
|Крив  <br/> |Определяет расстояние между одной строкой текста и следующим, выраженное в процентном выражении, где 100% — высота строки текста.  <br/> |[SpLine Cell (Paragraph Section)](spline-cell-paragraph-section.md) <br/> |
|TextPosAfterBullet  <br/> |Представляет расстояние между первой строкой абзаца и маркером.  <br/> |[TextPosAfterBullet Cell (Paragraph Section)](textposafterbullet-cell-paragraph-section.md) <br/> |
   

