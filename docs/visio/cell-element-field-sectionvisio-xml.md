---
title: Элемент Cell (раздел "поле") (XML-файл Visio)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 1a51a5ca-6b68-d2d8-befb-2b1d9cda1b8e
description: Отображает функции и формулы, вставленные в текст фигуры, с помощью диалогового окна "поле".
ms.openlocfilehash: b3bae89d20a4defed591e95ce0155f70d806e6f2
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/29/2019
ms.locfileid: "34540058"
---
# <a name="cell-element-field-section-visio-xml"></a>Элемент Cell (раздел "поле") (XML-файл Visio)

Отображает функции и формулы, вставленные в текст фигуры, с помощью диалогового окна "поле".
  
## <a name="element-information"></a>Сведения об элементе

|||
|:-----|:-----|
|**Тип элемента** <br/> |[Целл_типе](cell_type-complextypevisio-xml.md) <br/> |
|**Пространство имен** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Файл схемы** <br/> |VisioSchema15. xsd  <br/> |
|**Части документа** <br/> |Master #. XML, Page #. XML  <br/> |
   
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
|[Элемент Row (раздел "поле")](row-element-field-sectionvisio-xml.md) <br/> |[Фиелдров_типе](fieldrow_type-complextypevisio-xml.md) <br/> |Отображает функции и формулы, вставленные в текст фигуры, с помощью диалогового окна "поле".  <br/> |
   
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
|Календарь  <br/> |Определяет календарь, используемый для текстового поля, когда тип данных — Date.  <br/> |[Calendar Cell (Text Fields Section)](calendar-cell-text-fields-section.md) <br/> |
|Format  <br/> |Задает форматирование текстового поля, которое является строкой, числом, датой или временем, длительностью или валютой.  <br/> |[Format Cell (Text Fields Section)](format-cell-text-fields-section.md) <br/> |
|ObjectKind  <br/> |Указывает тип текстового поля.  <br/> |[ObjectKind Cell (Text Fields Section)](objectkind-cell-text-fields-section.md) <br/> |
|Тип  <br/> |Задает тип данных для значения текстового поля.  <br/> |[Type Cell (Text Fields Section)](type-cell-text-fields-section.md) <br/> |
|Уикат  <br/> |Определяет категорию вставленного поля. Эта ячейка используется в диалоговых окнах "поле" и "формат данных" для определения сведений о полях и категориях.  <br/> |[UICategory Cell (Text Fields Section)](uicategory-cell-text-fields-section.md) <br/> |
|Уикод  <br/> |Определяет код вставленного поля. Эта ячейка используется в диалоговых окнах "поле" и "формат данных" для определения сведений о полях и категориях.  <br/> |[UICode Cell (Text Fields Section)](uicode-cell-text-fields-section.md) <br/> |
|Уифмт  <br/> |Определяет формат вставленного поля. Эта ячейка используется в диалоговых окнах "поле" и "формат данных" для определения поля и  <br/> |[UIFormat Cell (Text Fields Section)](uiformat-cell-text-fields-section.md) <br/> |
|Значение  <br/> |Содержит функцию для поля.  <br/> |[Value Cell (Text Fields Section)](value-cell-text-fields-section.md) <br/> |
   

