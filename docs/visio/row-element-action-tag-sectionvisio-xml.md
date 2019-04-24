---
title: Элемент Row (раздел "теги действий") ("Visio XML")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 54c3315f-770f-6995-d0d8-ab66e4fe10d9
description: Определяет тег действия на фигуре или странице.
ms.openlocfilehash: 1ecdb256fbde4a667ade747c2c7216cd0d248fc2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32358438"
---
# <a name="row-element-action-tag-section-visio-xml"></a>Элемент Row (раздел "теги действий") ("Visio XML")

Определяет тег действия на фигуре или странице.
  
## <a name="element-information"></a>Сведения об элементе

|||
|:-----|:-----|
|**Тип элемента** <br/> |[Актионтагров_типе](actiontagrow_type-complextypevisio-xml.md) <br/> |
|**Пространство имен** <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Файл схемы** <br/> |VisioSchema15. xsd  <br/> |
|**Части документа** <br/> |Master. XML, Master #. XML, Pages. XML, Page #. XML  <br/> |
   
## <a name="definition"></a>Определение

```XML
< xs:element name="Row" type="ActionTagRow_Type" >
</xs:element >
```

## <a name="elements-and-attributes"></a>Элементы и атрибуты

Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений. 
  
### <a name="parent-elements"></a>Родительские элементы

|**Элемент**|**Тип**|**Описание**|
|:-----|:-----|:-----|
|[Section](section-element-sheet_type-complextypevisio-xml.md) <br/> |[Сектион_типе](section_type-complextypevisio-xml.md) <br/> |Определяет тег действия на фигуре или странице.  <br/> |
   
### <a name="child-elements"></a>Дочерние элементы

|**Элемент**|**Тип**|**Описание**|
|:-----|:-----|:-----|
|[Cell](cell-element-action-tag-sectionvisio-xml.md) <br/> |[Целл_типе](cell_type-complextypevisio-xml.md) <br/> |Определяет одно свойство для тега действия на фигуре или странице.  <br/> |
   
### <a name="attributes"></a>Атрибуты

|**Атрибут**|**Тип**|**Обязательный**|**Описание**|**Возможные значения**|
|:-----|:-----|:-----|:-----|:-----|
|Del  <br/> |XSD: Boolean  <br/> |необязательный  <br/> |Указывает, удалена ли строка, которая в противном случае была бы унаследована от основной фигуры.  <br/> |Значения типа XSD: Boolean.  <br/> |
|IX  <br/> |XSD: Унсигнединт  <br/> |необязательный  <br/> |Задает отсчитываемый от единицы идентификатор строки. Он должен быть уникальное и превышать другие идентификаторы в одном разделе. Атрибут IX используется только для разделов "символ", "подключение", "Филлградиент", "геометрия", "область", "Линеградиент", "Абзац", "фрагмент" и "вкладки". Строка может иметь только один из атрибутов IX или N.  <br/> |Значения типа XSD: Унсигнединт.  <br/> |
|LocalName  <br/> |XSD: строка  <br/> |необязательный  <br/> |Задает уникальное зависящее от языка имя строки.  <br/> |Значения типа String: XSD.  <br/> |
|N  <br/> |XSD: строка  <br/> |необязательный  <br/> |Задает уникальное имя строки, не зависящее от языка. Атрибут N используется только для разделов "пользователь", "свойство", "действия", "элементы управления", "гиперссылка" и "Актионтаг". Строка может иметь только один из атрибутов IX или N.  <br/> |Значения типа String: XSD.  <br/> |
|Д  <br/> |XSD: строка  <br/> |необязательный  <br/> |Указывает тип геометрического пути, представленного строкой и используемый в визуализации геометрии. Атрибут T используется только для раздела Geometry.  <br/> |Значения типа String: XSD.  <br/> |
   

