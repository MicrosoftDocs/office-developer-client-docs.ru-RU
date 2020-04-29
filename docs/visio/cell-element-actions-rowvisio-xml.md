---
title: Элемент Cell (строка Actions) (XML-файл Visio)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 5ae2b4db-03f4-1b8a-1274-7eb1521f2f59
description: Задает одно свойство действия, связанного с настраиваемой командой, в контекстном меню или меню тегов действий.
ms.openlocfilehash: 8cce85bdfb7d0ce54d968e00cda56e4e6c2455bc
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/29/2019
ms.locfileid: "34538783"
---
# <a name="cell-element-actions-row-visio-xml"></a>Элемент Cell (строка Actions) (XML-файл Visio)

Задает одно свойство действия, связанного с настраиваемой командой, в контекстном меню или меню тегов действий.
  
## <a name="element-information"></a>Сведения об элементе

|||
|:-----|:-----|
|**Тип элемента** <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |
|**Пространство имен** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Файл схемы** <br/> |VisioSchema15. xsd  <br/> |
|**Части документа** <br/> |Master. XML, Master #. XML, Pages. XML, Page #. XML  <br/> |
   
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
|[Элемент Row (раздел "действия")](row-element-actions-sectionvisio-xml.md) <br/> |[ActionsRow_Type](actionsrow_type-complextypevisio-xml.md) <br/> |Задает одно свойство действия, связанного с настраиваемой командой, в контекстном меню или меню тегов действий.  <br/> |
   
### <a name="child-elements"></a>Дочерние элементы

|**Элемент**|**Тип**|**Описание**|
|:-----|:-----|:-----|
|[RefBy](refby-element-cell_type-complextypevisio-xml.md) <br/> |[RefBy_Type](refby_type-complextypevisio-xml.md) <br/> |Указывает ссылку на страницу документа.  <br/> |
   
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
|Action  <br/> |Содержит формулу, которая должна выполняться, когда пользователь выбирает команду в контекстном меню или меню тегов действий.  <br/> |[Action Cell (Actions Section)](action-cell-actions-section.md) <br/> |
|BeginGroup  <br/> |Указывает, вставляется ли разделитель в меню над этим действием.  <br/> |[BeginGroup Cell (Actions Section)](begingroup-cell-actions-section.md) <br/> |
|ButtonFace  <br/> |Определяет значок, который появляется рядом с элементом в контекстном меню или меню тегов действий.  <br/> |[ButtonFace Cell (Actions Section)](buttonface-cell-actions-section.md) <br/> |
|Checked  <br/> |Указывает, отмечен ли элемент в контекстном меню или меню тегов действий.  <br/> |[Checked Cell (Actions Section)](checked-cell-actions-section.md) <br/> |
|Отключено  <br/> |Указывает, отключен ли элемент в контекстном меню или меню тегов действий.  <br/> |[Disabled Cell (Actions Section)](disabled-cell-actions-section.md) <br/> |
|FlyoutChild  <br/> |Определяет, является ли строка дочерним всплывающим меню последней строки над ним, которое не является потомком всплывающего списка.  <br/> |[FlyoutChild Cell (Actions Section)](flyoutchild-cell-actions-section.md) <br/> |
|Скрытым  <br/> |Указывает, отображается ли действие в теге действия или в контекстном меню.  <br/> |[Invisible Cell (Actions Section)](invisible-cell-actions-section.md) <br/> |
|Меню  <br/> |Определяет имя элемента меню, которое отображается в контекстном меню или меню тегов действий для фигуры или страницы.  <br/> |[Menu Cell (Actions Section)](menu-cell-actions-section.md) <br/> |
|ReadOnly  <br/> |Определяет, является ли действие для тега действия или контекстного меню предназначенным только для чтения.  <br/> |[ReadOnly Cell (Actions Section)](readonly-cell-actions-section.md) <br/> |
|SortKey  <br/> |Число, определяющее порядок действий, отображаемых в контекстном меню или меню тегов действий.  <br/> |[Ячейка SortKey (раздел "действия") — ячейка SortKey (раздел "действия")](sortkey-cell-actions-section.md) <br/> |
|TagName  <br/> |Содержит имя тега действия, с которым связано это действие.  <br/> |[TagName Cell (Actions Section)](tagname-cell-actions-section.md) <br/> |
   

