---
title: Элемент Cell (строка Actions) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 5ae2b4db-03f4-1b8a-1274-7eb1521f2f59
description: Указывает одно свойство действия, связанное с настраиваемой командой в меню ярлыка или тега действия.
ms.openlocfilehash: 8cce85bdfb7d0ce54d968e00cda56e4e6c2455bc
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/29/2019
ms.locfileid: "34538783"
---
# <a name="cell-element-actions-row-visio-xml"></a>Элемент Cell (строка Actions) (Visio XML)

Указывает одно свойство действия, связанное с настраиваемой командой в меню ярлыка или тега действия.
  
## <a name="element-information"></a>Сведения об элементе

|||
|:-----|:-----|
|**Тип элемента** <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |
|**Пространство имен** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Файл схемы** <br/> |VisioSchema15.xsd  <br/> |
|**Части документа** <br/> |masters.xml, master#.xml, pages.xml, page#.xml  <br/> |
   
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
|[Элемент Row (Actions Section)](row-element-actions-sectionvisio-xml.md) <br/> |[ActionsRow_Type](actionsrow_type-complextypevisio-xml.md) <br/> |Указывает одно свойство действия, связанное с настраиваемой командой в меню ярлыка или тега действия.  <br/> |
   
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
|Action  <br/> |Содержит формулу, которая будет выполняться, когда пользователь выбирает команду в меню ярлыка или тега действия.  <br/> |[Action Cell (Actions Section)](action-cell-actions-section.md) <br/> |
|BeginGroup  <br/> |Указывает, вставлен ли в меню над этим действием сепаратор.  <br/> |[BeginGroup Cell (Actions Section)](begingroup-cell-actions-section.md) <br/> |
|ButtonFace  <br/> |Определяет значок, который отображается рядом с элементом в меню ярлыка или тега действия.  <br/> |[ButtonFace Cell (Actions Section)](buttonface-cell-actions-section.md) <br/> |
|Checked  <br/> |Указывает, проверяется ли элемент в меню ярлыка или тега действия.  <br/> |[Checked Cell (Actions Section)](checked-cell-actions-section.md) <br/> |
|Отключено  <br/> |Указывает, отключен ли элемент в меню ярлыка или тега действия.  <br/> |[Disabled Cell (Actions Section)](disabled-cell-actions-section.md) <br/> |
|FlyoutChild  <br/> |Определяет, является ли строка "child flyout menu" последней строки над ней, которая не является его дитя.  <br/> |[FlyoutChild Cell (Actions Section)](flyoutchild-cell-actions-section.md) <br/> |
|Invisible  <br/> |Указывает, отображается ли действие в теге действия или в ярлыке меню.  <br/> |[Invisible Cell (Actions Section)](invisible-cell-actions-section.md) <br/> |
|Меню  <br/> |Определяет имя элемента меню, которое отображается в ярлыке или меню тегов действий для фигуры или страницы.  <br/> |[Menu Cell (Actions Section)](menu-cell-actions-section.md) <br/> |
|ReadOnly  <br/> |Управляет тем, является ли действие над тегом действия или ярлыком меню только для чтения.  <br/> |[ReadOnly Cell (Actions Section)](readonly-cell-actions-section.md) <br/> |
|SortKey  <br/> |Число, которое определяет порядок действий, которые отображаются в меню ярлыка или тега действия.  <br/> |[SortKey Cell (Actions Section) SortKey Cell (Actions Section)](sortkey-cell-actions-section.md) <br/> |
|TagName  <br/> |Содержит имя тега действия, с помощью которого связано это действие.  <br/> |[TagName Cell (Actions Section)](tagname-cell-actions-section.md) <br/> |
   

