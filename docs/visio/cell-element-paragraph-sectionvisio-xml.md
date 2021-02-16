---
title: Элемент Cell (Paragraph Section) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: de0d3aac-1a0f-1bdf-da94-e6699a55d08e
description: Указывает атрибут форматирования абзаца для текста фигуры, например отступы, интервалы строк, маркеры или горизонтальное выравнивание абзацев.
ms.openlocfilehash: fbb837b96d40f412ddefdf1fac9da0d31a709e39
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/29/2019
ms.locfileid: "34539483"
---
# <a name="cell-element-paragraph-section-visio-xml"></a>Элемент Cell (Paragraph Section) (Visio XML)

Указывает атрибут форматирования абзаца для текста фигуры, например отступы, интервалы строк, маркеры или горизонтальное выравнивание абзацев.
  
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
|[Элемент Row (Paragraph Section)](row-element-paragraph-sectionvisio-xml.md) <br/> |[ParagraphRow_Type](paragraphrow_type-complextypevisio-xml.md) <br/> |Указывает атрибут форматирования абзаца для текста фигуры, например отступы, интервалы строк, маркеры или горизонтальное выравнивание абзацев.  <br/> |
   
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
|Bullet  <br/> |Определяет стиль маркера.  <br/> |[Bullet Cell (Paragraph Section)](bullet-cell-paragraph-section.md) <br/> |
|BulletFont  <br/> |Представляет число шрифта, используемого для формата текста при указании настраиваемой строки маркера, а значение в ячейке Bullet не является нулем.  <br/> |[BulletFont Cell (Paragraph Section)](bulletfont-cell-paragraph-section.md) <br/> |
|BulletFontSize  <br/> |Указывает размер маркера.  <br/> |[BulletSize Cell (Paragraph Section)](bulletsize-cell-paragraph-section.md) <br/> |
|BulletStr  <br/> |Позволяет создать настраиваемый стиль маркеров.  <br/> |[BulletString Cell (Paragraph Section)](bulletstring-cell-paragraph-section.md) <br/> |
|Flags  <br/> |Указывает, находится ли направление текста слева направо или справа налево.  <br/> |[Flags Cell (Paragraph Section)](flags-cell-paragraph-section.md) <br/> |
|HorzAlign  <br/> |Определяет горизонтальное выравнивание текста в текстовом блоке фигуры.  <br/> |[HAlign Cell (Paragraph Section)](halign-cell-paragraph-section.md) <br/> |
|IndFirst  <br/> |Представляет расстояние от левого отступа абзаца от первой строки каждого абзаца в текстовом блоке фигуры. Это значение не зависит от масштаба рисунка. При масштабе рисования отступ первой строки остается тем же.  <br/> |[IndFirst Cell (Paragraph Section)](indfirst-cell-paragraph-section.md) <br/> |
|IndLeft  <br/> |Представляет расстояние, на которое все строки текста в абзаце отступят от левого поля текстового блока. Это значение не зависит от масштаба рисунка. Если рисунок масштабировать, отступ слева остается тем же.  <br/> |[IndLeft Cell (Paragraph Section)](indleft-cell-paragraph-section.md) <br/> |
|IndRight  <br/> |Представляет расстояние, на которое все строки текста в абзаце отступят от правого поля текстового блока. Это значение не зависит от масштаба рисунка. Если рисунок масштабировать, правый отступ остается тем же.  <br/> |[IndRight Cell (Paragraph Section)](indright-cell-paragraph-section.md) <br/> |
|SpAfter  <br/> |Определяет объем пространства, вставляемого после каждого абзаца в текстовом блоке фигуры, в дополнение к пространству из ячейки SpLine и, если это последний абзац в текстовом блоке, ячейка BottomMargin.  <br/> |[SpAfter Cell (Paragraph Section)](spafter-cell-paragraph-section.md) <br/> |
|SpBefore  <br/> |Определяет объем пространства, вставляемого перед каждым абзацем в текстовом блоке фигуры, в дополнение к пространству из ячейки SpLine, если это первый абзац в текстовом блоке, ячейка TopMargin.  <br/> |[SpBefore Cell (Paragraph Section)](spbefore-cell-paragraph-section.md) <br/> |
|SpLine  <br/> |Определяет расстояние между одной строкой текста и следующей строкой в процентах, где 100 % — это высота текстовой строки.  <br/> |[SpLine Cell (Paragraph Section)](spline-cell-paragraph-section.md) <br/> |
|TextPosAfterBullet  <br/> |Представляет расстояние между первой строкой абзаца и маркером.  <br/> |[TextPosAfterBullet Cell (Paragraph Section)](textposafterbullet-cell-paragraph-section.md) <br/> |
   

